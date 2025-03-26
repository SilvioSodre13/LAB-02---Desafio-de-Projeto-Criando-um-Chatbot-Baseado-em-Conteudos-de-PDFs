Microsoft Certification Challenge #3 DP-100
# LAB-02-Criando-um-Chatbot-Baseado-em-Conteudos-de-PDFs
Este projeto consiste em desenvolver um sistema de chatbot capaz de responder perguntas com base em informações extraídas de documentos PDF

## Descrição 
O processo envolve a utilização de técnicas de Processamento de Linguagem Natural (NLP) para analisar e compreender o conteúdo dos PDFs. 
Um modelo de Machine Learning é treinado para interpretar perguntas e encontrar as respostas mais relevantes no texto. 
O chatbot pode ser implantado como um serviço web, permitindo interações em tempo real. Tecnologias como APIs de NLP, serviços de armazenamento em nuvem e frameworks de Machine Learning são utilizadas para construir e escalar a solução.

## Objetivo

Utilizar o *Azure Foundry* e a *Inteligência Artificial Generativa* para estruturar a pesquisa, organizar as informações e identificar conexões relevantes entre os artigos, otimizando o desenvolvimento de um possivel TCC de maneira mais eficiente.

Para isso, temos 05 artigos academicos que versam sobre o tema escolhido a **Teoria da Fronteira Eficiente de Markovitz** . Essa teoria busca otimizar a alocação de ativos de um investidor, equilibrando risco e retorno.


# Preparando o Ambiente no Azure Foundry

​O Azure AI Foundry é uma plataforma inovadora da Microsoft projetada para simplificar o desenvolvimento, a implantação e a gestão de soluções de Inteligência Artificial (IA). Fonte : https://smartbridge.com/what-is-azure-ai-foundry/?utm_source=chatgpt.com

Passos anteriores que devemsem respeitados antes de acessar o Microsoft Azure AI Foundry:

* Ter uma conta ativa da Azure
* Ter um grupo de recursos criado
* Depois dos passos anteriores voce pode pesquisar Azure AI Foundry pelo nome e clicar em criar e dai em diante preencher os campos solicitados. Se restou alguma duvida ainda. A documentação pode ser consultada : https://learn.microsoft.com/pt-br/azure/ai-foundry/what-is-ai-foundry

  


![image](https://github.com/user-attachments/assets/ab906afe-ed9c-4161-8d5a-c19c880f06be)


No Foundry será necessario criar um **HUB** para criar o projeto

![image](https://github.com/user-attachments/assets/fa1a3a2c-b4f2-40d1-bb42-86c7dfc8c3e0)

![image](https://github.com/user-attachments/assets/aacaee9e-174f-4e28-9720-ddf779672468)

![image](https://github.com/user-attachments/assets/bc85e7f5-8537-4282-8f43-dba1085f6a27)

![image](https://github.com/user-attachments/assets/ea765cf4-06c8-4a44-a823-b790abf78755)

Depois disso clicar em *Go to resource*

![image](https://github.com/user-attachments/assets/46cbe837-cbca-4e04-b668-bd3bb0d18711)

Vai ser apresentado a tela abaixo : 

![image](https://github.com/user-attachments/assets/a8de030c-b223-47ec-b36d-33bff814044d)


Clicar em novo projeto  e seguir as orientações de preenchimento : 

![image](https://github.com/user-attachments/assets/77dcea5d-3d05-44e4-a652-4e45f2c1c58a)

![image](https://github.com/user-attachments/assets/861d3cef-cc04-4c35-8ac0-743575305c1f)

Depois disso voce vai acessar a barra lateral e clicar em **Modelos e Pontos de Extremidade** e vai clicar em Implante o modelo.

![image](https://github.com/user-attachments/assets/f36db22f-337b-4a7d-a359-4e8708635372)

Foi escolhido para este projeto o ***gpt-4o***

![image](https://github.com/user-attachments/assets/1ad89276-0279-4cd8-80d1-a8bb87673cbe)

![image](https://github.com/user-attachments/assets/f134d55a-f53d-4e15-8719-12d5848041fa)

É necessario também  um modelo avançado de incorporação de texto. Por isso, foi incorporado o ***text-embedding-3-large***


![image](https://github.com/user-attachments/assets/19501bcf-1fa9-4a11-aa23-908d31481dda)

![image](https://github.com/user-attachments/assets/025c6880-c72b-419d-bc7b-ea35c8b04126)

Aqui conseguimos ver os dois modelos implantados : 


![image](https://github.com/user-attachments/assets/1d1d8870-fbeb-4d07-97a1-3db3ab994e43)

Na aula lateral depois de acessar **Playgrounds** vai ser possivel visualizar o chat com os modelos implantados.

Foi configurado a seguinte instrução de contexto do modelo :

**Você é um analista financeiro especializado em Teoria Moderna de Portfólio, com profundo conhecimento sobre a teoria da fronteira eficiente. Sua missão é fornecer análises precisas e fundamentadas, explicando conceitos, estratégias de alocação de ativos e a aplicação da fronteira eficiente na otimização de carteiras de investimento.**


![image](https://github.com/user-attachments/assets/d165fa26-27d1-463c-b65a-10ef3c7c8bc2)

Fiz um teste com esse resultado : 

![image](https://github.com/user-attachments/assets/53a140fe-5ca9-4c84-961c-f2a187444ee7)


Agora preciso adicionar os artigos academicos sobre o assunto.  No proprio **Playgrounds** temos a opção de adicionar os dados é só seguir as orientações

![image](https://github.com/user-attachments/assets/bfa0eacd-6153-4964-99fd-c5983a5f8edc)

![image](https://github.com/user-attachments/assets/6f0714c8-bef6-46e6-aded-d44ae3a7f033)

![image](https://github.com/user-attachments/assets/3b208399-0fca-44dc-b5a9-1a0cfa3348c5)

Foi necessario criar um **search service**

![image](https://github.com/user-attachments/assets/5f1d47a5-d54e-45fa-80a0-c221c5599142)

![image](https://github.com/user-attachments/assets/2f9372f9-72b7-40fa-92ee-4090b167e6f5)

![image](https://github.com/user-attachments/assets/2b9f110f-3559-434b-ad20-56accd7ec4bf)

![image](https://github.com/user-attachments/assets/56bb2652-2781-428d-811d-80b23977cdb2)

Depois vinculamos esse serviço de pesquisa para finalizarmos o processo.

![image](https://github.com/user-attachments/assets/d9327dee-c0d3-46b9-bcee-63bd19ab8667)

![image](https://github.com/user-attachments/assets/c53dc17f-66ea-4485-959e-42969d63cf0b)

![image](https://github.com/user-attachments/assets/e7ad0910-93dd-4605-a7b5-342a4cb53e6f)
![image](https://github.com/user-attachments/assets/4dd26dc6-0a82-4752-a596-cdabb78023b8)

# Testando o chatbot


Depois de finalizadas as etapas anteriores  e a hora de testar o chatbot e verificar se ele esta funcionando como previsto,
ou seja, entregando as respostas com base nos dados e informando as referencias.

Para isso foram feitas 04 perguntas ao chatbot, a saber : 

1. Quem foi Markowitz?

   ![image](https://github.com/user-attachments/assets/5e1a9684-9b7e-4693-be31-46ce12334c57)


2. O que é a teoria da fronteira eficiente?

   ![image](https://github.com/user-attachments/assets/3dab605a-2429-41b2-a159-91a39a7b8f1b)


3. Qual a importância da teoria da fronteira eficiente no mercado financeiro atual?

![image](https://github.com/user-attachments/assets/092f980d-a9af-4a9d-995c-a0bf18c002fe)


4. Como selecionar ativos para uma carteira de investimentos com base na teoria da fronteira eficiente?

   ![image](https://github.com/user-attachments/assets/f7412502-884e-41f4-beb4-89dc8dee34fe)


   ![image](https://github.com/user-attachments/assets/18c35480-e9c9-4609-83ca-98d5c414b695)


   # Conclusão

   O Chatbot conseguiu responder as perguntas e citar os artigos.





    



   




   

   

   









































































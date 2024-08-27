# 307_CriandoAssistenteDeliveryAWSStepFunctionsBedrock
Criando um Assistente de Delivery com AWS Step Functions e Bedrock



- CONTEÚDOS
- INFORMAÇÕES

###### DESCRIÇÃO

Neste desafio prático, você será responsável por criar um Assistente de Delivery utilizando AWS Step Functions e Amazon Bedrock. O projeto consiste em orquestrar diferentes serviços AWS para automatizar e gerenciar um fluxo de pedidos de delivery, desde a recepção do pedido até a entrega final. Utilizando Step Functions, você irá coordenar tarefas como validação de pedidos, integração com serviços de pagamento e atualização de status. O Amazon Bedrock será empregado para aprimorar a personalização e a eficiência do assistente, proporcionando uma experiência otimizada ao cliente.

**Amazon Bedrock**

------

###### Full-Stack

###### Básico

------

###### ESPECIALISTA

![author](https://hermes.dio.me/users/author/photos/e0aa7c57-89e3-41ff-a60b-09dc7a9bc6e9.jpg)

###### Felipe Aguiar

Tech Educator, DIO[**](https://web.dio.me/project/criando-um-assistente-de-delivery-com-aws-step-functions-e-bedrock/learning/www.linkedin.com/in/felipeaguiar-exe) [**](https://github.com/felipeAguiarCode)



https://web.dio.me/project/criando-um-assistente-de-delivery-com-aws-step-functions-e-bedrock/learning/54f25128-779d-4000-a1b3-460d808abbc0?back=/track/engenharia-prompts-aws



 [README.md](..\README.md) 



# Entendendo o Desafio

**Agora é a sua hora de brilhar e construir um perfil de destaque na DIO! Explore todos os conceitos explorados até aqui e replique (ou melhore, porque não?) este projeto prático. Para isso, crie seu próprio repositório e aumente ainda mais seu portfólio de projetos no GitHub, o qual pode fazer toda diferença em suas entrevistas técnicas** 😎

 

## Links Úteis

**AWS Step Functions:** https://aws.amazon.com/pt/step-functions/

**AWS Step Functions Examples:** https://github.com/aws-samples/aws-stepfunctions-examples

**Serverless e Amazon Bedrock:** https://aws.amazon.com/pt/blogs/aws-brasil/como-criar-um-assistente-virtual-de-baixa-latencia-com-multiplos-modelos-usando-serverless-e-amazon-bedrock/

 

Bons estudos 😉





[**](https://web.dio.me/track/engenharia-prompts-aws)

##### Criando um Assistente de Delivery com AWS Step Functions e Bedrock

**

**

**

<iframe id="ytc32" frameborder="0" allowfullscreen="" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" title="Bem Vindo ao Step Functions" width="100%" height="100%" src="https://www.youtube.com/embed/wruhHzM7IBQ?controls=0&amp;disablekb=1&amp;enablejsapi=1&amp;fs=0&amp;iv_load_policy=3&amp;modestbranding=1&amp;showinfo=0&amp;rel=0&amp;html5=1&amp;cc_load_policy=0&amp;origin=https%3A%2F%2Fweb.dio.me&amp;widgetid=1" data-gtm-yt-inspected-18="true" style="box-sizing: inherit; max-width: none; margin: 0px; padding: 0px; border: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; line-height: inherit; font-family: inherit; font-optical-sizing: inherit; font-kerning: inherit; font-feature-settings: inherit; font-variation-settings: inherit; font-size: 14px; vertical-align: baseline;"></iframe>



00:03

 

02:11





<iframe id="ytc44" frameborder="0" allowfullscreen="" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" title="Pré Requisitos" width="100%" height="100%" src="https://www.youtube.com/embed/8w20QjvPeXg?controls=0&amp;disablekb=1&amp;enablejsapi=1&amp;fs=0&amp;iv_load_policy=3&amp;modestbranding=1&amp;showinfo=0&amp;rel=0&amp;html5=1&amp;cc_load_policy=0&amp;origin=https%3A%2F%2Fweb.dio.me&amp;widgetid=1" data-gtm-yt-inspected-18="true" style="box-sizing: inherit; max-width: none; margin: 0px; padding: 0px; border: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; line-height: inherit; font-family: inherit; font-optical-sizing: inherit; font-kerning: inherit; font-feature-settings: inherit; font-variation-settings: inherit; font-size: 14px; vertical-align: baseline;"></iframe>



**

<iframe id="ytc56" frameborder="0" allowfullscreen="" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" title="Situação Problema" width="100%" height="100%" src="https://www.youtube.com/embed/ha8wb93qVKg?controls=0&amp;disablekb=1&amp;enablejsapi=1&amp;fs=0&amp;iv_load_policy=3&amp;modestbranding=1&amp;showinfo=0&amp;rel=0&amp;html5=1&amp;cc_load_policy=0&amp;origin=https%3A%2F%2Fweb.dio.me&amp;widgetid=1" data-gtm-yt-inspected-18="true" style="box-sizing: inherit; max-width: none; margin: 0px; padding: 0px; border: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; line-height: inherit; font-family: inherit; font-optical-sizing: inherit; font-kerning: inherit; font-feature-settings: inherit; font-variation-settings: inherit; font-size: 14px; vertical-align: baseline;"></iframe>



[**](https://web.dio.me/track/engenharia-prompts-aws)

##### Criando um Assistente de Delivery com AWS Step Functions e Bedrock

**

**

**

<iframe id="ytc68" frameborder="0" allowfullscreen="" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" title="Step Functions Oficial page" width="100%" height="100%" src="https://www.youtube.com/embed/0fZgDHGjw1k?controls=0&amp;disablekb=1&amp;enablejsapi=1&amp;fs=0&amp;iv_load_policy=3&amp;modestbranding=1&amp;showinfo=0&amp;rel=0&amp;html5=1&amp;cc_load_policy=0&amp;origin=https%3A%2F%2Fweb.dio.me&amp;widgetid=1" data-gtm-yt-inspected-18="true" style="box-sizing: inherit; max-width: none; margin: 0px; padding: 0px; border: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; line-height: inherit; font-family: inherit; font-optical-sizing: inherit; font-kerning: inherit; font-feature-settings: inherit; font-variation-settings: inherit; font-size: 14px; vertical-align: baseline;"></iframe>



[**](https://web.dio.me/track/engenharia-prompts-aws)

##### Criando um Assistente de Delivery com AWS Step Functions e Bedrock

**

**

**

<iframe id="ytc80" frameborder="0" allowfullscreen="" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" title="Documentação Oficial" width="100%" height="100%" src="https://www.youtube.com/embed/Ues4Fz5fXT8?controls=0&amp;disablekb=1&amp;enablejsapi=1&amp;fs=0&amp;iv_load_policy=3&amp;modestbranding=1&amp;showinfo=0&amp;rel=0&amp;html5=1&amp;cc_load_policy=0&amp;origin=https%3A%2F%2Fweb.dio.me&amp;widgetid=1" data-gtm-yt-inspected-18="true" style="box-sizing: inherit; max-width: none; margin: 0px; padding: 0px; border: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; line-height: inherit; font-family: inherit; font-optical-sizing: inherit; font-kerning: inherit; font-feature-settings: inherit; font-variation-settings: inherit; font-size: 14px; vertical-align: baseline;"></iframe>



[**](https://web.dio.me/track/engenharia-prompts-aws)

##### Criando um Assistente de Delivery com AWS Step Functions e Bedrock

**

**

**

<iframe id="ytc92" frameborder="0" allowfullscreen="" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" title="Localizando o Serviço" width="100%" height="100%" src="https://www.youtube.com/embed/Oip4HjrhLLA?controls=0&amp;disablekb=1&amp;enablejsapi=1&amp;fs=0&amp;iv_load_policy=3&amp;modestbranding=1&amp;showinfo=0&amp;rel=0&amp;html5=1&amp;cc_load_policy=0&amp;origin=https%3A%2F%2Fweb.dio.me&amp;widgetid=1" data-gtm-yt-inspected-18="true" style="box-sizing: inherit; max-width: none; margin: 0px; padding: 0px; border: 0px; font-style: inherit; font-variant: inherit; font-weight: inherit; font-stretch: inherit; line-height: inherit; font-family: inherit; font-optical-sizing: inherit; font-kerning: inherit; font-feature-settings: inherit; font-variation-settings: inherit; font-size: 14px; vertical-align: baseline;"></iframe>



00:01

 

01:59









normal

auto

BASIC

**•**[Upgrade](https://web.dio.me/pricing?source=upgrade-pro-player-projects)

XP 372768/380348

NÍVEL 39

**5/5**

- CONTEÚDOS
- INFORMAÇÕES

Bem Vindo ao Step FunctionsPré RequisitosSituação ProblemaStep Functions Oficial pageDocumentação OficialLocalizando o ServiçoComeçando com um projeto TemplateWorkflow Studio & ASLCriando um Hello WorldPrecificação e custosNível 1 de configuração - permissão de perfilNível 2 de configuração - disponibilidade de serviçoCriando um assistente de delivery na práticaComo entregar meu projetoEntendendo o Desafio

# Text Analytics with Azure AI services

[![LinkedIn](https://img.shields.io/badge/LinkedIn-000?style=for-the-badge&logo=LinkedIn&logoColor=30A3DC)](https://www.linkedin.com/in/jacqueline-ribeiro-743876247/)

Neste exercício, você explorará os recursos da Linguagem de IA do Azure analisando alguns exemplos de avaliações de hotéis. Você usará o Language Studio para entender se as avaliações são majoritariamente positivas ou negativas.

O Processamento de Linguagem Natural (PNL) é um ramo da IA que lida com a linguagem escrita e falada. Você pode usar a PNL para criar soluções que extraem significado semântico do texto ou da fala ou que formulem respostas significativas em linguagem natural.

Por exemplo, suponha que a agente de viagens fictícia Margie's Travel incentive os clientes a enviar avaliações para estadias em hotéis. Você pode usar o serviço Idioma para identificar frases-chave, determinar quais avaliações são positivas e quais são negativas ou analisar o texto de revisão em busca de menções a entidades conhecidas, como locais ou pessoas.

O Serviço de Linguagem de IA do Azure inclui análise de texto e recursos de PNL. Estes incluem a identificação de frases-chave no texto e a classificação do texto com base no sentimento.

## Criar um recurso de _idioma_

Você pode usar muitos recursos de Linguagem de IA do Azure com um recurso **de Idioma** ou **serviços de IA do Azure**. Há alguns casos em que apenas um recurso **de idioma** pode ser usado. Para o exercício abaixo, usaremos um recurso de linguagem. Se você ainda não tiver feito isso, crie um recurso de idioma em sua assinatura do Azure.

1. Em outra guia do navegador, abra o portal do Azure em [https://portal.azure.com](https://portal.azure.com), entrando com a conta da Microsoft associada à sua assinatura do Azure.

2. Clique no botão **+Criar um recurso** e procure Serviço de idioma. Selecione **Criar** um plano **de serviço de idioma**. Você será direcionado para uma página para **Selecionar recursos adicionais**. Mantenha a seleção padrão e clique em **Continuar para criar seu recurso.**

3. Na página **Criar Idioma**, configure-a com as seguintes configurações:

* **Assinatura**: sua assinatura do Azure.
* **Grupo de recursos**: selecione ou crie um grupo de recursos com um nome exclusivo.
* **Região**: Leste dos EUA.
* **Nome**: insira um nome exclusivo.
* **Nível de preços**: F0 ou S grátis se F0 gratuito não estiver disponível
* **Ao marcar esta caixa, reconheço que li e entendi todos os termos abaixo**: Selecionado.

4. Selecione **Revisar + criar** e, em seguida, **Criar** e aguarde a conclusão da implantação.

## Configurar seu recurso no Estúdio de Idiomas de IA do Azure

1. Em outra guia do navegador, abra o Language Studio no [https://language.cognitive.azure.com e entre]https://language.cognitive.azure.com e entre).

2. Quando solicitado com **Selecionar um recurso do Azure**, faça as seguintes configurações:

* **Diretório do Azure**: Diretório padrão, o diretório que você está usando
* **Assinatura do Azure**: selecione a assinatura que você está usando
* **Tipo de recurso**: Idioma
* **Nome do recurso**: selecione o recurso Serviço de idioma que você acabou de criar

Em seguida, selecione **Concluído**.

## Analisar avaliações no Language Studio

1. Em um navegador da Web, navegue até **Language Studio** em [https://language.cognitive.azure.com](https://language.cognitive.azure.com).

2. Na página **inicial Bem-vindo ao Language Studio**, selecione a guia **Classificar texto** e, em seguida, selecione o bloco **Analisar sentimento e minerar opiniões**.

3. Em _Selecionar idioma_ do texto, selecione **Inglês**.

4. Em _Selecione seu recurso do Azure_, selecione seu recurso.

5. Em _Digite seu próprio texto_, carregue um arquivo ou use um de nossos textos de exemplo, copie e cole a seguinte revisão:

**Código**
`` 
 Tired hotel with poor service
 The Royal Hotel, London, United Kingdom
 5/6/2018
 This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.`` 

6. Marque a caixa para confirmar que a demonstração incorrerá em uso e poderá incorrer em custos e, em seguida, selecione **Executar**.

7. Revise a saída. Observe que o documento é analisado quanto ao sentimento, assim como cada frase. Selecione **Frase 1** para mostrar a análise de sentimento dessa frase.

Observe que há um sentimento geral seguido de pontuações ao lado de três categorias, _pontuação positiva, pontuação neutra, pontuação negativa_. Em cada uma das categorias, é fornecida uma pontuação entre 0 e 1. Essas pontuações de confiança indicam a probabilidade de o texto fornecido ser um sentimento particular.

Selecione **Frase 1** novamente para fechar.

1. Role para cima até selecionar **Caixa de texto não** criptografado e copie e cole a seguinte revisão:

**Código**

`` Good Hotel and staff
 The Royal Hotel, London, UK
 3/2/2018
 Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.`` 
 
2. Selecione **Executar**. Revise o resultado e analise o sentimento e o nível de confiança.


Neste exercício, você usou o Language Studio para criar um novo recurso de idioma ou usar um recurso de idioma existente. Você habilitou o recurso em Configurações antes de experimentar o serviço de mineração de sentimento e opinião. Em seguida, você testou o serviço com três partes de texto.

## Insights:

1. Sentece:
   `` Tired hotel with poor service ``

   <img width="536" alt="image" src="https://github.com/jacquelinepalumbo/text-analysis/assets/119548193/ea99de16-3348-40ea-8152-bb120a016679">

* A análise foi considerada 96% negativa. O hóspede qualificou o hotel negativamente. O adjetivo 'poor' service qualificou o Hotel com um serviço abaixo do considerado satisfatório.


2. Sentence:
  `` The internet didn't work and had to come to one of their office rooms to check in for my flight home.``

<img width="489" alt="image" src="https://github.com/jacquelinepalumbo/text-analysis/assets/119548193/8d0e2428-d3b4-4408-bc49-053bec622b18">

* A análise foi considerada 99% negativa:ja que um dos serviços oferecidos pelo hotel, a internet, não funcionava. Reforçando, mais um vez, que o o serviço prestado pelo hotel é ruim.

3. Sentence:
     ``The website says it's close to the British Museum, but it's too far to walk.``

<img width="469" alt="image" src="https://github.com/jacquelinepalumbo/text-analysis/assets/119548193/5a48c343-2f3b-4c94-b934-9436a3fb1707">


* A análise foi considerada 91% negativa: No site do hotel informava que a localização do British Museum era próxima, mas na realidade era distante.
O que impussionou a insatisfação do hóspede com o local. Pois, além do serviço ser considerado ruim, a localização geográfica do hotel não favorecia a hospedagem do cliente em questão já que não atendia as necessidades deste consumidor.

# Referências:


[Explore text with Language Studio](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/06-text-analysis.html)

&nbsp;

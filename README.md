# Analisar texto com o Language Studio


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

`` Código
 Tired hotel with poor service
 The Royal Hotel, London, United Kingdom
 5/6/2018
 This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.`` 

6. Marque a caixa para confirmar que a demonstração incorrerá em uso e poderá incorrer em custos e, em seguida, selecione **Executar**.

7. Revise a saída. Observe que o documento é analisado quanto ao sentimento, assim como cada frase. Selecione **Frase 1** para mostrar a análise de sentimento dessa frase.

Observe que há um sentimento geral seguido de pontuações ao lado de três categorias, _pontuação positiva, pontuação neutra, pontuação negativa_. Em cada uma das categorias, é fornecida uma pontuação entre 0 e 1. Essas pontuações de confiança indicam a probabilidade de o texto fornecido ser um sentimento particular.

Selecione **Frase 1** novamente para fechar.

Role para cima até selecionar Caixa de texto não criptografado e copie e cole a seguinte revisão:

Código
 Good Hotel and staff
 The Royal Hotel, London, UK
 3/2/2018
 Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
Selecione Executar. Revise o resultado e analise o sentimento e o nível de confiança.

Selecione Limpar caixa de texto novamente e copie e cole a seguinte revisão:

Muito barulhento e os quartos são minúsculos The Lombard Hotel, São Francisco, EUA 9/5/2018 O hotel está localizado na rua Lombard, que é uma rua SIX lane muito movimentada diretamente da ponte Golden Gate. Trânsito desde o início da manhã até tarde da noite, especialmente nos fins de semana. O ruído não seria tão ruim se os quartos fossem mais bem isolados, mas não são. Tive que colocar bolas de algodão nos ouvidos para conseguir dormir – estava muito cansado para curtir a cidade no dia seguinte. Os quartos são TINY. Escolhi o quarto porque tinha duas camas queen size – mas o quarto mal tinha espaço para encaixá-las. Com família de quatro pessoas no quarto, era apertado. Com tudo isso dito, os quartos são limpos e eles fizeram um esforço para atualizá-los. O hotel fica no bairro de Marina, com muitos bons lugares para comer, a uma curta distância a pé do Presidio. Pode ser um bom hotel para jovens adultos com um orçamento

Selecione Executar e revise o sentimento junto com o nível de confiança. Dê uma olhada no texto e compare o texto com a análise de sentimento que o serviço retornou.

Neste exercício, você usou o Language Studio para criar um novo recurso de idioma ou usar um recurso de idioma existente. Você habilitou o recurso em Configurações antes de experimentar o serviço de mineração de sentimento e opinião. Em seguida, você testou o serviço com três partes de texto.

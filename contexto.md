# Contexto — palestra da Codecon

Este arquivo registra as decisões e o ponto atual da preparação para manter a continuidade entre conversas.

## Palestra

- **Título:** “Nem Tudo Precisa de IA Generativa: Visão Computacional na Medicina”
- **Duração:** cerca de 30 minutos, aproximadamente 27 minutos de apresentação e 3 minutos para perguntas.
- **Público:** pessoas de tecnologia com diferentes níveis de familiaridade com IA e medicina.
- **Tom:** conversa natural de meetup, visual, com storytelling e pouco texto por slide; evitar tom acadêmico, artificial ou corporativo.
- **Ideia central:** IA generativa é uma ferramenta, não uma obrigação. O problema deve orientar a escolha da tecnologia. Não demonizar IA generativa.

## Descrição aprovada

> Em pleno hype da IA generativa, será que precisamos mesmo de LLMs para criar soluções úteis?
>
> Nesta palestra, vou compartilhar a experiência de um projeto de visão computacional aplicado à análise de imagens médicas que, iniciado em 2019 e utilizando algoritmos já amplamente difundidos, conquistou prêmios, publicações científicas e oportunidades de inovação.
>
> Uma história sobre tecnologia, pesquisa e como soluções que não estão na última moda ainda podem gerar resultados surpreendentes.

## Perfil e bio

Engenheira de Software Sênior no Itaú Unibanco, formada em Engenharia de Computação e mestra pela UFSC. Transita entre o desenvolvimento de soluções escaláveis no setor financeiro e a pesquisa em Inteligência Artificial aplicada à saúde. Durante o mestrado, trabalhou com visão computacional e análise de imagens médicas, explorando como métodos tradicionais podem gerar resultados relevantes mesmo na era da IA generativa.

## Relevância para a Codecon

Em meio ao hype da IA generativa, é importante lembrar que existem diferentes caminhos para resolver problemas reais com tecnologia. A palestra compartilha uma experiência que une desenvolvimento, pesquisa acadêmica e inovação na saúde, mostrando que métodos conhecidos também podem gerar resultados relevantes e que transformar pesquisa em solução útil vai além de escolher a tecnologia da moda.

## Pesquisa

- **Dissertação:** “Desenvolvimento de um framework computacional para quantificação de biomarcadores em imagens histopatológicas de câncer de mama em ambiente web”
- **Autora:** Thaynara Tessaline Mitie Sei Soares
- **UFSC — Campus Araranguá — PPGTIC — 2026**
- **Repositório:** https://repositorio.ufsc.br/handle/123456789/275652
- Analisa imagens de imuno-histoquímica (IHQ) de câncer de mama e biomarcadores como ER/PR. A quantificação manual pode ser subjetiva e pouco reprodutível.
- A proposta investiga uma arquitetura de menor custo: smartphone acoplado ao microscópio, captura de microfotografias, processamento em nuvem, microsserviços e visualização web/mobile dos resultados.
- Foram comparados: (1) processamento clássico com limiarização adaptativa; (2) distância de Mahalanobis com expansão polinomial; (3) Deep Learning com Faster R-CNN.
- **Precisão conceitual:** o projeto usa IA, inclusive Deep Learning. Ele não depende de IA generativa ou LLMs.
- Resultados resumidos: recall inferior a 10% para células negativas no método clássico; F1 em torno de 0,76 no estatístico; acurácia global acima de 82% no Faster R-CNN, com maior robustez ao pleomorfismo celular.
- Foi criado um protótipo Mobile + Cloud. O método clássico foi integrado a um aplicativo móvel como prova de conceito para validar aquisição de imagens, orquestração em nuvem, processamento e visualização das máscaras.
- A conclusão aponta viabilidade técnica da arquitetura para contribuir com a democratização da patologia digital, condicionada a confiabilidade adequada dos mecanismos de inferência para eventual uso clínico.
- Não apresentar o trabalho como produto clínico pronto nem como substituto de patologistas.

## Sequência planejada

1. Capa.
2. Provocação: hoje parece que todo projeto precisa de LLM; será que todo problema precisa?
3. Começo em 2019 e origem pessoal do projeto.
4. **Em elaboração:** soluções atuais de digitalização de lâminas usam scanners WSI especializados e podem impor uma barreira de custo. Preparar a entrada de smartphone + microscópio + cloud.
5. Arquitetura Mobile + Cloud.
6. Três abordagens e a ideia de que IA não significa apenas IA generativa.
7. Resultados técnicos, explicados sem virar aula de métricas.
8. Demonstração visual: imagem IHQ → processamento → máscara/resultado.
9. Linha do tempo do projeto.
10. Conquistas: 1 registro de propriedade intelectual, prêmio de melhor projeto de aceleração de startup, 2 artigos IEEE, 1 pôster em congresso de patologia, 1 dissertação e 2 TCCs; mencionar oportunidades de inovação.
11. IA generativa como apoio à pesquisa e desenvolvimento, sem necessariamente ser o núcleo do produto.
12. Da pesquisa à inovação: potencial, sem alegar implantação clínica.
13. Fechamento: “Nem tudo precisa ser generativo. A melhor tecnologia não é necessariamente a mais nova. É aquela que faz sentido para o problema que queremos resolver.”

## Slide 4 — decisões e trabalho pendente

**Objetivo:** mostrar que há soluções comerciais de patologia digital, mas que digitalizar lâminas inteiras pode exigir investimento alto em scanners WSI e infraestrutura associada. Fazer surgir a pergunta: “Será que precisamos de toda essa infraestrutura para começar a trabalhar com imagens digitais?” Em seguida, introduzir smartphone + microscópio + cloud.

Custos a considerar além do scanner: armazenamento, infraestrutura de TI, processamento, software/licenças, manutenção e suporte.

Foram mencionadas referências na literatura com estimativas de cerca de US$ 50 mil ou mais e scanners de maior capacidade na faixa de US$ 100 mil a US$ 400 mil ou mais. **Esses números ainda não foram conferidos na dissertação.** Não atribuir valor exato à dissertação sem localizar a página/trecho. Se entrar um número no slide, tratar como faixa indicativa da literatura, variável conforme equipamento, capacidade, resolução, fabricante e recursos. Formulações possíveis: “dezenas a centenas de milhares de dólares” ou “≈ US$ 50 mil a US$ 400 mil+*”, com nota de contexto.

**Speech-base já elaborado:**

> Quando falamos em patologia digital, já existem soluções no mercado que permitem digitalizar uma lâmina inteira e trabalhar com essas imagens diretamente no computador.
>
> O problema é que essas soluções utilizam equipamentos bastante especializados, chamados scanners WSI, que podem custar dezenas ou até centenas de milhares de dólares.
>
> E não estamos falando apenas do equipamento. Também precisamos considerar armazenamento, infraestrutura, processamento e manutenção.
>
> Isso acaba criando uma barreira para laboratórios e instituições que não possuem tantos recursos para investir nesse tipo de tecnologia.
>
> E foi justamente nesse contexto que surgiu uma das motivações do nosso projeto: será que precisamos de toda essa infraestrutura para começar a trabalhar com imagens digitais e desenvolver soluções de análise?

**Transição aprovada:** “Foi aí que começamos a explorar uma alternativa: utilizar um smartphone acoplado a um microscópio e aproveitar a infraestrutura de processamento em nuvem.”

## Como trabalhar

Trabalhar um slide por vez. Para cada slide: definir objetivo, conteúdo visível, estrutura visual e speech; ajustar em conjunto; avançar apenas quando a usuária disser “vamos para o próximo slide”. Manter continuidade entre os speeches. Ao revisar frases sugeridas pela usuária, preservar a formulação e fazer apenas ajustes necessários.

## Arquivo HTML existente

Há uma apresentação em `apresentacao_codecon_thaynara.html` na pasta do projeto. A versão existente é anterior às decisões recentes e não deve ser alterada até que a usuária peça. A estrutura atual do HTML parece diferir da sequência descrita acima; ao receber pedido de atualização, conferir o arquivo real e preservar sua estrutura, fazendo somente os ajustes solicitados.

## Ponto atual

Estamos retomando pelo Slide 4: barreira de custo dos scanners WSI e preparação da transição para Mobile + Cloud. A dissertação/PDF não foi localizado nesta pasta; portanto, nenhum valor exato foi confirmado a partir dela.

## Atualização do HTML — 9 nov. 2026

- O slide do desafio/custo foi atualizado para destacar scanners WSI, a faixa indicativa “dezenas a centenas de milhares de dólares”, custos de infraestrutura associados e a pergunta de transição. O valor não é atribuído à dissertação.
- As notas do slide incluem o speech de custo e deixam explícito que a faixa precisa ser validada com fonte antes de qualquer atribuição específica.
- A transição para Mobile + Cloud foi adicionada às notas do slide de arquitetura.
- Foi inserido um slide explicando IHQ em linguagem simples. Em atualização posterior, ele foi movido para depois de “A origem” e passou a usar uma imagem única do Escore de Allred (`images/allred_score.jpeg`).
- A numeração dos slides foi atualizada. O arquivo agora contém 14 slides.
- Nas notas do slide “Não foi uma disputa entre ‘IA’ e ‘não IA’”, registrar que também foi considerada a possibilidade de usar IA generativa para a tarefa e deixar o espaço `[ADICIONAR LINK DO ARTIGO]` para uma referência sobre confiabilidade/segurança nesse contexto. Evitar generalizar que IA generativa é insegura.

## Atualização da abertura — 16 nov. 2026

- A capa original permanece como Slide 1.
- O Slide 2 abre com a imagem do problema e a pergunta sobre o que usar para detectar/quantificar: IA generativa, algoritmo clássico (“dev raiz”) ou rede neural.
- As notas orientam mostrar a imagem, apontar o que deve ser detectado, colher algumas respostas e ainda não revelar a solução.
- O antigo slide “A provocação” continua logo depois como Slide 3. Os seguintes foram renumerados; o deck agora tem 15 slides.
- No Slide 2, a imagem IHQ original deve ficar à esquerda e a imagem com células detectadas/contornadas à direita. A imagem original está em `images/slide-02-ihq-original.jpg`; a imagem de detecções é `images/Screenshot 2026-11-16 at 22.53.48.png`. Ambas estão referenciadas no HTML; há placeholders visíveis como fallback.
- Os cards do Slide 2 estão na ordem: algoritmo clássico, rede neural, IA generativa.
- Foram acrescentados três slides em sequência, repetindo as imagens e os cards na parte inferior: primeiro algoritmo clássico em destaque com os demais normais; depois rede neural em destaque com as outras opções apagadas; por último IA generativa em destaque com as outras opções apagadas. O deck agora tem 18 slides.
- No slide “Algoritmo clássico”, foi removido o gabarito positivo. As três imagens ficam lado a lado: `negative_plot_gabarito.jpg`, `Screenshot 2026-11-16 at 23.51.33.png` no centro e `negative_limiar_recalculado.jpg` à direita.
- No Slide 5 (“IA generativa”), as imagens `Gemini_Generated_Image_8k9mhh8k9mhh8k9m.jpg` e `Gemini_Generated_Image_d9rygnd9rygnd9ry.jpg` ficam lado a lado. O slide identifica os números exibidos como ilustrativos e não validados.
- No Slide 4 (“Rede neural”), `gt_IMG_5377_1_1_png.rf.4b4c85f68e8559f2e8f10cce290a2e09.jpg` aparece à esquerda como gabarito e `det_IMG_5377_1_1_png.rf.4b4c85f68e8559f2e8f10cce290a2e09.jpg` à direita como resultado.
- Foi acrescentada uma cópia do Slide 3 imediatamente após ele, com as mesmas imagens, cards e destaque do algoritmo clássico. A numeração foi atualizada e o deck agora tem 19 slides.
- No Slide 4, `Screenshot 2026-11-16 at 22.53.48.png` aparece à esquerda como gabarito e `5377_1_1_mahala.png` à direita como resultado da distância de Mahalanobis.
- No Slide 3, as imagens anteriores foram substituídas por `Screenshot 2026-11-16 at 22.53.48.png` à esquerda como gabarito e `5377_1_1_iou_classic.jpg` à direita como resultado do método clássico.

## Atualização do Slide 9 — 17 nov. 2026

- A seção de custo da dissertação apresenta a barreira financeira do WSI, mas não informa um preço numérico do scanner.
- Para exibir uma faixa verificável, o Slide 9 agora usa **US$ 100 mil–US$ 400 mil** para um scanner WSI de alta capacidade (>100 lâminas), estimativa do white paper da Digital Pathology Association (2021), com link no próprio slide. Não atribuir essa faixa diretamente à dissertação.
- Também foi incluído o resultado da revisão sistemática: 1.246 registros identificados; 41 estudos com métodos algorítmicos relevantes sem framework completo; 8 sistemas/ferramentas incluídos como soluções completas para usuário final. A fonte é o Capítulo 3, Tabelas 2–3 da dissertação, linkado no slide.
- A pergunta de transição no Slide 9 recebeu tamanho de fonte responsivo menor para evitar uma quebra visual desproporcional em telas mais estreitas.
- Na capa, foi fixada uma quebra de linha antes de “IA Generativa”, mantendo as duas palavras juntas na segunda linha.
- Os limites fixos de largura dos títulos, subtítulos, parágrafos e frases de destaque foram removidos para que o texto use toda a largura interna do slide e quebre apenas conforme o espaço disponível.
- No slide Mobile + Cloud, os componentes do fluxo foram ampliados e centralizados horizontalmente; o fluxo pode quebrar em linhas mantendo o alinhamento central em telas estreitas.
- Ajuste seguinte: o fluxo Mobile + Cloud deve permanecer sempre em uma única linha; em telas estreitas, usa rolagem horizontal em vez de quebrar/empilhar os componentes.
- O slide “Entendendo a imagem” foi movido para logo após “A origem”; os números dos slides de problema e arquitetura foram atualizados.
- O slide “O que os resultados mostraram” foi removido a pedido da usuária. Os slides posteriores foram renumerados; a apresentação agora tem 18 slides.
- Removido “A jornada” (linha do tempo); os slides seguintes foram renumerados. O contador está ajustado para 18 slides.
- O Slide 12 foi reformulado para mostrar, em linguagem intuitiva e sem métricas acadêmicas, as vantagens do método clássico, de Mahalanobis e do Faster R-CNN, com ressalvas nas notas do apresentador.
- Removido o slide “14 · Os resultados além do algoritmo”; os slides seguintes foram renumerados e o contador atualizado para 17 slides.
- O slide “O próximo passo” foi reformulado: editais públicos como ponto de partida para identificar temas priorizados e possíveis caminhos de fomento. O slide traz links oficiais da FAPESC e da Finep; as notas esclarecem que temas, prazos, elegibilidade e tipo de apoio variam conforme a chamada. Exemplos de temas recentes foram conferidos em páginas oficiais em 17/11/2026.
- Foram acrescentados às notas do slide “O próximo passo” links oficiais para a listagem de chamadas da FAPESC, chamadas específicas sobre educação e segurança pública, chamadas públicas da Finep e uma chamada recente da Finep usada como exemplo de temas.
- Removido o slide “13 · Na prática”; os slides seguintes foram renumerados e o contador atualizado para 16 slides.
- Foram inseridos três slides logo após a capa: dois espaços de imagem para publicações na IEEE CBMS; um para registro de software e dissertação; e um para prêmio de incentivo à inovação e prêmio da Sociedade Brasileira de Patologia. A pergunta que antes abria a parte técnica foi movida para depois desses slides, os kickers foram renumerados e o deck agora tem 19 slides. Os novos slides fazem a provocação de que um projeto sem IA generativa no núcleo pode gerar publicações, registro, dissertação e reconhecimento.
- Incluída nas notas do slide “Reconhecimento e inovação” a referência enviada pela usuária para os trabalhos premiados no CBPato 2024, da Sociedade Brasileira de Patologia: https://congressodepatologia.org.br/confira-a-relacao-de-trabalhos-premiados-no-cbpato-2024-sbp-news-05-06-2024/.

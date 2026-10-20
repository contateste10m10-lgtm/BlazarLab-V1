# BlazarLab 1.3.36 — navegação com ícones e microanimações

## V1.3.36 — menu com ícones e microanimações

- Adicionados ícones SVG decorativos com rótulos textuais preservados para as seis seções principais.
- Incluída microanimação apenas no ícone ativado; as cores são herdadas por `currentColor` e não são controladas pela animação.
- O efeito é desativado para usuários que preferem movimento reduzido; o cabeçalho compacto agora cobre a faixa até 1240 px.
- Teste `tests/navigation-icon-animation.cjs` adicionado à suíte automatizada.


- As regras tipográficas da matriz fonte × banda foram reunidas em uma única seção com um conjunto base e breakpoints explícitos.
- Mantida a estrutura acessível e interativa da tabela móvel sem diminuir células ou alterar os cálculos.
- Acrescentado `tests/mobile-matrix-css-regression.cjs` ao workflow de qualidade.

## V1.3.33 — estabilidade das animações e acessibilidade

- Um controlador único sincroniza a preferência de movimento reduzido e reinicia a camada apenas depois de atualizar o estado.
- Os timers de revelação são cancelados durante a limpeza.
- Cartões com interação própria usam entrada por opacidade para preservar hover/transform.
- O foco de teclado torna o contêiner visível antes da próxima pintura.
- Removidos `tabindex` redundantes de artigos introdutórios não interativos.


Esta versão V1.3.36 preserva a vitrine científica, os três métodos, as séries sintéticas, os gráficos e as preferências visuais; integra as correções de estabilidade, acessibilidade, matrizes móveis e navegação com ícones descritas no resumo desta versão. O histórico das auditorias anteriores é mantido abaixo.

## Atualização V1.3.31 — inspeção visual no Chromium

A página foi renderizada no Chromium em dez larguras entre 320 e 1440 px. A largura do documento permaneceu limitada à viewport; as matrizes científicas mantêm rolagem localizada. Tema claro/escuro e menu móvel foram exercitados, e as 18 suítes `.cjs` passaram. Como não foi reproduzido um defeito visual que justificasse correção, o HTML/CSS/JavaScript da interface e as animações foram preservados. Consulte `updates/AUDITORIA_CHROMIUM_1.3.31.md` para o método, os resultados e as limitações.

## Atualização V1.3.30

1. **Auditoria de links e recursos:** foi acrescentado `tests/link-asset-audit.cjs` para verificar âncoras internas, IDs duplicados, links vazios, recursos locais ausentes, links externos abertos em novas abas e metadados canônicos.
2. **Integração contínua:** o novo teste foi incluído em `.github/workflows/quality.yml`.
3. **Código público preservado:** não houve mudanças em HTML, CSS ou JavaScript da página, pois as verificações estáticas não encontraram um defeito que justificasse uma alteração especulativa. A revisão visual no Chromium não pôde ser concluída neste ambiente porque uma política administrativa bloqueou a navegação local.
4. **Animações adiadas:** nenhuma animação foi adicionada ou redesenhada; essa etapa fica para uma versão de teste posterior, conforme solicitado.
5. **Integridade científica:** nenhuma fórmula, parâmetro analítico ou série sintética foi alterada.

Detalhes, resultados e limitações em `updates/AUDITORIA_1.3.30.md`.

## Atualização V1.3.29

1. **Rastreabilidade bibliográfica:** os cartões dos resumos apontam para referências metodológicas verificadas por meio de âncoras internas; nenhum URL de manuscrito integral foi inventado.
2. **Transparência dos textos:** a seção explica que os cartões são resumos fornecidos pelo grupo e que esta versão não vincula URLs públicas verificadas para os textos integrais.
3. **Rótulo sintético:** a categoria antes identificada como “AGN” passa a aparecer como “AGN genérico”; a chave interna `AGN`, a quantidade de fontes e as curvas determinísticas permanecem iguais.
4. **Legibilidade móvel:** os rótulos de classe, fontes e valores do heatmap recebem dimensões mínimas ligeiramente maiores, preservando áreas de toque e rolagem localizada.
5. **Metadados de publicação:** o guia esclarece que `/BlazarLab_13/` é o endereço canônico de produção e `/teste-2000/` o endereço de revisão. Os metadados canônicos da página não foram alterados.
6. **Testes de regressão:** adicionada uma verificação para os rótulos científicos, os links metodológicos e a distinção entre endereço de revisão e produção.

## Base preservada da V1.3.28

- Corrigida a autoria bibliográfica de EntropyHub para Flood e Grimm (2021) e incluída a referência de Bandt–Pompe (2002).
- Rótulos inferiores do hero separados para evitar sobreposição.
- Unidade energética exibida uma única vez na matriz fonte × banda; alvos de toque do rodapé ampliados.
- Histórico do changelog consolidado; contagem de 144 pontos por banda preservada.
- Nenhuma fórmula científica, parâmetro analítico ou série sintética foi alterada.



## Publicação da V1.3.36

Extraia `blazarlab-public-v1.3.36-menu-icons-microanimacoes.zip` e copie o conteúdo da pasta `blazarlab_v1.3.36/` para a raiz do repositório configurado para o GitHub Pages, mantendo `index.html` na raiz. Use `README-GITHUB-UPLOAD.md` para executar a suíte de testes e distinguir o endereço de revisão do endereço canônico de produção. Publique juntos HTML, CSS, JavaScript, ativos locais e documentação desta mesma versão.

## Publicação histórica V1.3.31

As instruções a seguir descrevem uma publicação anterior; para a versão atual, siga o `README-GITHUB-UPLOAD.md` e utilize somente arquivos do mesmo pacote.


## V1.3.32 — versão experimental de animações

- Adicionada revelação progressiva para blocos editoriais selecionados à medida que entram na viewport; visualizações multibanda sob controle de abas não são ocultadas por essa camada.
- Adicionado traçado de entrada para a curva de luz estilizada do hero, pulso breve dos dois pontos ilustrativos e deriva orbital curta de execução única (sem movimento automático infinito).
- A camada só ativa se `IntersectionObserver` estiver disponível e a preferência de movimento permitir animações; não altera cálculos ou dados.
- Preservadas as animações de métodos existentes.
- Incluído `tests/experimental-motion-lab.cjs` e comando no workflow de qualidade.
- A auditoria registra separadamente os testes automatizados e a renderização Chromium usada para esta versão.

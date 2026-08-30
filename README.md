# Atualização V4.2 — potências nominais comerciais

A geração das cargas passou a utilizar pares nominais comerciais de motores em kW/cv. Exemplos: 2,2 kW = 3 cv; 4,0 kW = 5,5 cv; 5,5 kW = 7,5 cv; 11 kW = 15 cv; 18,5 kW = 25 cv; 22 kW = 30 cv. Projetos JSON importados de versões anteriores também têm o valor de cv normalizado pelo kW nominal.

# PEI Projetista Integrado V4 — Projeto em Trio / Empresa Fictícia

Esta versão foi preparada para avaliação em **trios**. Cada trio representa uma **empresa projetista fictícia** e recebe um único código PEI.

## Entregas produzidas pela plataforma

Ao final, o projeto completo reúne:

1. identificação da empresa projetista fictícia;
2. identificação dos três alunos, função, participação e responsabilidades;
3. identificação do responsável técnico didático;
4. dados do cliente industrial fictício;
5. situação-problema e cargas individualizadas;
6. Engenharia de Acionamentos (Partida Direta, Soft-starter ou Inversor de Frequência);
7. **Memorial Descritivo**;
8. **Memória de Cálculo**, com identificação do integrante responsável por cada cálculo;
9. **Quadro de Cargas** profissional;
10. QGBT;
11. CCM;
12. Subestação;
13. Luminotécnico;
14. SPDA, BEP e aterramento;
15. **Lista de Materiais** com item, TAG, descrição, quantidade, unidade, preço unitário e total;
16. orçamento global;
17. pranchas;
18. controle de revisão;
19. PDF completo.

## Como a equipe usa

1. O docente entrega um código ao trio, por exemplo `PEI-2026-T01`.
2. O trio abre **Código e cliente** e gera o projeto.
3. Informa o nome da empresa fictícia do trio.
4. Cadastra os três integrantes.
5. Define função, responsabilidades e percentual de participação de cada um. A soma deve ser **100%**.
6. Escolhe o integrante que aparecerá como **Responsável Técnico da equipe (didático)**.
7. Cadastra o cliente industrial fictício.
8. Em **Engenharia de Acionamentos**, analisa M01 a M10 e escolhe/justifica Partida Direta, Soft-starter ou Inversor.
9. Usa a **Calculadora Industrial**. Antes de registrar um cálculo, escolhe o integrante responsável no campo `Responsável pelo cálculo / registro`.
10. Completa quadro de cargas, QGBT, CCM, subestação, luminotécnico e SPDA/aterramento.
11. Atualiza a lista de materiais e informa preços.
12. Clica em **Gerar / atualizar texto** no Memorial Descritivo e revisa a redação.
13. Confere a Memória de Cálculo.
14. Vai em **Conferência e PDF** e corrige as pendências.
15. Gera o PDF completo.
16. Exporta também o JSON do projeto como backup.

## Regra de acionamentos da UC

- Partida Direta;
- Soft-starter;
- Inversor de Frequência.

Partida direta limitada a:
- 220 V → 5 cv;
- 380 V → 7,5 cv.

## GitHub + Vercel

Envie todos os arquivos e pastas deste pacote ao GitHub, incluindo `api/` e `assets/`.

Na Vercel:

1. Add New → Project;
2. importe o repositório;
3. Framework Preset: **Other**;
4. não defina Build Command;
5. não defina Output Directory;
6. Deploy.

A função `/api/evaluate-drive` será disponibilizada pela Vercel para a avaliação indicativa das decisões de acionamento. Se abrir o `index.html` diretamente, a plataforma funciona em modo local, sem avaliação completa do servidor.

## Salvamento

Os dados são salvos no navegador. Para mudar de computador, exporte o JSON e importe no outro dispositivo.


## Área do Docente V4.2

A pasta agora inclui `docente.html`, `docente.js` e `docente.css`.

Fluxo recomendado:
1. O docente abre `docente.html` e gera os códigos dos trios.
2. Entrega um código para cada equipe.
3. O trio desenvolve o projeto em `index.html`.
4. Ao final, clica em **Gerar entrega ao docente** e envia o arquivo `ENTREGA_...json` e o PDF do projeto.
5. O docente importa o JSON em `docente.html`.
6. A plataforma analisa 12 critérios e sugere uma nota de 0 a 100.
7. O docente pode ajustar cada critério, escrever comentários e homologar a nota.
8. A nota é apresentada em escala 0–100 e 0–10.
9. O relatório PDF informa, critério por critério, o que foi **ATINGIDO** e o que ficou **PENDENTE / PARCIAL**.

### Rubrica
- Empresa fictícia, trio e participação: 5 pontos
- Engenharia de acionamentos: 15 pontos
- Quadro de cargas e motores: 15 pontos
- QGBT: 10 pontos
- CCM: 12 pontos
- Subestação: 12 pontos
- Luminotécnico: 8 pontos
- SPDA/BEP/aterramento: 7 pontos
- Memória de cálculo: 7 pontos
- Memorial descritivo: 4 pontos
- Lista de materiais/orçamento: 3 pontos
- Coerência e entrega: 2 pontos
- Total: 100 pontos

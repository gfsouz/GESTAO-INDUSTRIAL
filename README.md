# Explicação do Funcionamento do Sistema de Gestão Industrial

O Sistema de Gestão Industrial é uma ferramenta desenvolvida para automatizar o controle de qualidade, registro e organização de peças em ambientes de produção. O sistema é composto por módulos integrados que permitem o gerenciamento eficiente das peças produzidas, garantindo que apenas aquelas que atendem aos padrões de qualidade sejam aprovadas e organizadas em caixas de armazenamento.

---

## Módulos do Sistema

### Módulo de Cadastro de Peças

Este módulo permite o registro de novas peças no sistema. Durante o cadastro, são solicitadas informações como ID, peso, cor e comprimento. O sistema valida automaticamente se a peça atende aos critérios de qualidade:

- **Peso**: Entre 95g e 105g.
- **Cor**: Apenas azul ou verde.
- **Comprimento**: Entre 10cm e 20cm.

Peças que atendem a todos os critérios são aprovadas e organizadas em caixas de armazenamento. Peças que não atendem a um ou mais critérios são reprovadas e registradas com o motivo específico da rejeição.

### Módulo de Listagem de Peças

Este módulo exibe todas as peças cadastradas, separando-as em aprovadas e reprovadas. Para cada peça, são exibidas informações detalhadas, como ID, peso, cor, comprimento, status e data de registro.

### Módulo de Remoção de Peças

Este módulo permite a remoção de uma peça específica pelo seu ID. Ao remover uma peça aprovada, o sistema ajusta automaticamente as caixas de armazenamento e os contadores, garantindo a consistência dos dados.

### Módulo de Listagem de Caixas

Este módulo mostra o conteúdo de cada caixa de armazenamento, incluindo o número da caixa, a quantidade de peças armazenadas e os IDs das peças contidas em cada caixa.

### Módulo de Geração de Relatórios

Este módulo fornece métricas consolidadas sobre a produção, como:

- Total de peças aprovadas e reprovadas.
- Quantidade de caixas utilizadas.
- Motivos de rejeição das peças (peso, cor ou comprimento).

### Módulo de Salvamento e Saída

Este módulo salva todos os dados no arquivo "dados_fabrica.json" e encerra o programa de forma segura, garantindo que nenhuma informação seja perdida.

---

# Como Rodar o Programa: Passo a Passo Detalhado para Executar em Python

Para executar o Sistema de Gestão Industrial, siga os passos detalhados abaixo:

---

## Pré-requisitos

Antes de iniciar a execução do sistema, certifique-se de que os seguintes pré-requisitos estejam atendidos:

1. **Python versão 3.11 ou superior** instalado no computador.
  - Para verificar a versão do Python instalada, abra o terminal ou prompt de comando e digite:
  - Caso o Python não esteja instalado, faça o download e a instalação a partir do site oficial: [python.org](https://www.python.org/downloads/).
2. **Permissão para leitura e escrita de arquivos** na pasta "src".
  - Certifique-se de que o usuário possui permissões adequadas para acessar e modificar arquivos na pasta "src".
3. **Ambiente de execução**:
  - O sistema pode ser executado em qualquer sistema operacional (Windows, macOS, Linux) que possua o Python instalado.

---

## Passos para Execução

### 1. Preparação do Ambiente

- **Baixar ou clonar o projeto**:
  - Caso o projeto tenha sido baixado como um arquivo compactado (ZIP), extraia-o para uma pasta de sua preferência.
  - Caso esteja utilizando um repositório Git, clone o projeto para sua máquina local utilizando o comando:
    ```bash
    git clone [URL_DO_REPOSITORIO]
    ```
- **Acessar a pasta "src"**:
  - Abra o terminal ou prompt de comando do seu sistema operacional.
  - Navegue até a pasta "src" utilizando o comando:
    ```bash
    cd caminho/para/a/pasta/GESTAO-INDUSTRIAL/src/
    ```
  - Substitua "caminho/para/a/pasta/" pelo caminho real onde o projeto foi salvo em sua máquina.

---

### 2. Execução do Sistema

- **Executar o sistema**:
  - Com o terminal aberto na pasta "src", execute o seguinte comando para iniciar o sistema:
    ```bash
    python sistema.py
    ```
  - Caso esteja utilizando um ambiente virtual, ative-o antes de executar o comando acima.
- **Verificar a execução**:
  - Após a execução do comando, o sistema será iniciado e um menu interativo será exibido no terminal.
  - O menu apresentará as seguintes opções:
    ```
    1. Cadastrar Peça
    2. Listar Peças
    3. Remover Peça
    4. Listar Caixas
    5. Gerar Relatório
    6. Salvar e Sair
    ```

---

### 3. Utilização do Menu Interativo

- **Cadastrar Peça**:
  - Selecione a opção 1 no menu.
  - Insira as informações solicitadas: ID, peso, cor e comprimento da peça.
  - O sistema validará automaticamente as informações e exibirá uma mensagem informando se a peça foi aprovada ou reprovada.
- **Listar Peças**:
  - Selecione a opção 2 no menu.
  - O sistema exibirá uma lista de todas as peças cadastradas, separando-as em aprovadas e reprovadas.
- **Remover Peça**:
  - Selecione a opção 3 no menu.
  - Insira o ID da peça que deseja remover.
  - O sistema removerá a peça e ajustará automaticamente as caixas e contadores.
- **Listar Caixas**:
  - Selecione a opção 4 no menu.
  - O sistema exibirá uma lista de todas as caixas, mostrando o número da caixa, a quantidade de peças armazenadas e os IDs das peças.
- **Gerar Relatório**:
  - Selecione a opção 5 no menu.
  - O sistema exibirá um relatório gerencial com métricas consolidadas sobre a produção.
- **Salvar e Sair**:
  - Selecione a opção 6 no menu.
  - O sistema salvará todos os dados no arquivo "dados_fabrica.json" e encerrará a execução.

---

### 4. Encerramento do Sistema

- **Salvar os dados**:
  - Sempre utilize a opção "Salvar e Sair" para encerrar o sistema. Isso garantirá que todos os dados sejam salvos corretamente no arquivo "dados_fabrica.json".
- **Verificar o arquivo de dados**:
  - Após encerrar o sistema, verifique se o arquivo "dados_fabrica.json" foi atualizado com as informações mais recentes.

---

# Exemplos de Entradas e Saídas

A seguir, são apresentados exemplos detalhados de entradas e saídas para cada uma das principais funcionalidades do sistema.

---

## Exemplo 1: Cadastro de Peça Aprovada

**Entrada**:

- ID: P001
- Peso: 100g
- Cor: azul
- Comprimento: 15cm

**Saída**:

```
Peça APROVADA! Registrada em 25/03/2026 10:30:45
```

**Descrição**:  
Neste exemplo, a peça com ID P001 atende a todos os critérios de qualidade (peso, cor e comprimento). Portanto, o sistema aprova a peça e a organiza em uma caixa de armazenamento.

---

## Exemplo 2: Cadastro de Peça Reprovada (Cor Inválida)

**Entrada**:

- ID: P004
- Peso: 102g
- Cor: rosa
- Comprimento: 15cm

**Saída**:

```
Peça REPROVADA! Motivo: COR
(A cor 'rosa' não é permitida. Apenas azul ou verde são aceitos.)
```

**Descrição**:  
Neste exemplo, a peça com ID P004 não atende ao critério de cor, pois a cor "rosa" não está entre as cores permitidas (azul e verde). Portanto, o sistema reprova a peça e registra o motivo da rejeição.

---

## Exemplo 3: Listagem de Peças

**Saída**:

```
PEÇAS APROVADAS:
ID: P001 | 100g | azul | 15cm | 25/03/2026 10:30:45
ID: P002 | 97g | verde | 13cm | 25/03/2026 10:35:22

PEÇAS REPROVADAS:
ID: P004 | Cor: rosa | Motivo: COR | 25/03/2026 10:40:10
```

**Descrição**:  
Neste exemplo, o sistema lista todas as peças cadastradas, separando-as em aprovadas e reprovadas. Para cada peça, são exibidas informações detalhadas, como ID, peso, cor, comprimento, status e data de registro.

---

## Exemplo 4: Listagem de Caixas

**Saída**:

```
STATUS DAS CAIXAS:
Caixa 1: [10/10] -> P001, P002, P010, P007, P006, P003, P547, P473, P009, P092
Caixa 2: [2/10] -> P011, P012
```

**Descrição**:  
Neste exemplo, o sistema lista o conteúdo de cada caixa de armazenamento, incluindo o número da caixa, a quantidade de peças armazenadas e os IDs das peças contidas em cada caixa. Quando uma caixa atinge a capacidade máxima de 10 peças, o sistema a fecha automaticamente e inicia uma nova caixa para continuar o armazenamento.

---

## Exemplo 5: Relatório Gerencial

**Saída**:

```
RELATÓRIO GERENCIAL:
Peças Aprovadas: 12
Peças Reprovadas (Total): 1
- Peso: 0
- Cor: 1
- Comprimento: 0
Caixas Utilizadas: 2
```

**Descrição**:  
Neste exemplo, o sistema gera um relatório gerencial com métricas consolidadas sobre a produção, como o total de peças aprovadas e reprovadas, a quantidade de caixas utilizadas e os motivos de rejeição das peças. O relatório mostra que há 12 peças aprovadas, 1 peça reprovada por cor, e que 2 caixas estão sendo utilizadas, sendo que a primeira caixa está cheia (10/10) e a segunda caixa contém 2 peças.
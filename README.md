# Gerador de Materiais para Armários (CMG)

Este aplicativo de desktop, desenvolvido em Python utilizando a biblioteca Tkinter, auxilia na geração de quantidades de materiais e estimativas de custos para a fabricação de armários. Com uma interface intuitiva, o usuário pode inserir preços de custo, margens de lucro, dimensões dos armários e especificações como número de prateleiras, gavetas e partições para obter resultados precisos e personalizados.

## Tabela de Conteúdos

1. [Funcionalidades](#funcionalidades)
2. [Tecnologias Utilizadas](#tecnologias-utilizadas)
3. [Instalação](#instalação)
4. [Como Usar](#como-usar)
    - [Passo 1: Executar o Aplicativo](#passo-1-executar-o-aplicativo)
    - [Passo 2: Inserir Preços de Custo e Margens](#passo-2-inserir-preços-de-custo-e-margens)
    - [Passo 3: Inserir Dimensões e Especificações do Armário](#passo-3-inserir-dimensões-e-especificações-do-armário)
    - [Passo 4: Calcular Preços de Venda](#passo-4-calcular-preços-de-venda)
    - [Passo 5: Calcular Saídas Totais](#passo-5-calcular-saídas-totais)
    - [Passo 6: Visualizar Resultados](#passo-6-visualizar-resultados)
5. [Tratamento de Erros](#tratamento-de-erros)
6. [Contribuindo](#contribuindo)
7. [Licença](#licença)
8. [Contato](#contato)

## Funcionalidades

- **Cálculo de Preços de Venda**: Insira os preços de custo e as margens desejadas para obter os preços de venda dos materiais.
- **Inserção de Dimensões**: Forneça as dimensões do armário (largura, profundidade e altura) para calcular a quantidade de materiais necessários.
- **Especificações Detalhadas**: Informe o número de prateleiras, gavetas, partições e lados expostos para um cálculo preciso.
- **Cálculo de Saídas Totais**: Gere quantidades totais de materiais e estimativas de custo baseadas nas entradas fornecidas.
- **Interface Intuitiva**: Utilize botões e campos de entrada claros para facilitar a operação mesmo para usuários sem experiência técnica.

## Tecnologias Utilizadas

- **Python 3**: Linguagem de programação principal.
- **Tkinter**: Biblioteca padrão do Python para criação de interfaces gráficas.
- **PIL (Pillow)**: Biblioteca para manipulação de imagens.
- **Math**: Biblioteca para operações matemáticas.
- **Dotenv**: Biblioteca para carregar variáveis de ambiente (opcional).

## Instalação

### Pré-requisitos

- **Python 3.7+**: Certifique-se de que o Python está instalado em seu sistema. Você pode baixar a versão mais recente [aqui](https://www.python.org/downloads/).

### Passos de Instalação

1. **Clone o Repositório**

   Clone este repositório para o seu computador usando o Git:

   ```
   git clone https://github.com/seu_usuario/cabinet-material-generator.git
   ```

2. **Navegue até o Diretório do Projeto**

   ```
   cd cabinet-material-generator
   ```

3. **Crie e Ative um Ambiente Virtual (Opcional, mas Recomendado)**

   - **No Windows:**

     ```
     python -m venv venv
     venv\Scripts\activate
     ```

   - **No macOS/Linux:**

     ```
     python3 -m venv venv
     source venv/bin/activate
     ```

4. **Instale as Dependências Necessárias**

   Certifique-se de que todas as bibliotecas necessárias estão instaladas:

   ```
   pip install pillow python-dotenv
   ```

   *Nota: A biblioteca `Tkinter` geralmente vem pré-instalada com o Python. Se não estiver, instale-a conforme a documentação do seu sistema operacional.*

5. **Configurar Variáveis de Ambiente (Opcional)**

   Se o aplicativo utiliza variáveis de ambiente, crie um arquivo `.env` na raiz do projeto e adicione as variáveis necessárias:

   ```
   # Exemplo de variáveis de ambiente
   VARIAVEL_EXEMPLO=valor
   ```

## Como Usar

### Passo 1: Executar o Aplicativo

Execute o arquivo `app.py` para iniciar a interface gráfica:

```
python app.py
```

Uma janela intitulada "Cabinet Material Generator (CMG)" será aberta.

### Passo 2: Inserir Preços de Custo e Margens

Na seção "SELLING PRICE CALCULATION":

1. **Particularidades**: Selecione o material que deseja calcular (por exemplo, 18mm BSB, 6mm BSB, 18mm OSR, FF Shutter, HF Shutter, Labor Charge).
2. **Preço de Custo (₹)**: Insira o preço de custo do material correspondente.
3. **Margem (%)**: Insira a margem de lucro desejada para calcular o preço de venda.
4. **Preço de Venda (₹)**: Este campo será preenchido automaticamente após o cálculo.

### Passo 3: Inserir Dimensões e Especificações do Armário

Na seção "CABINET DETAILS":

1. **DIMENSÕES DO ARMÁRIO**:
   - **WIDTH (mm)**: Insira a largura do armário em milímetros.
   - **DEPTH (mm)**: Insira a profundidade do armário em milímetros.
   - **HEIGHT (mm)**: Insira a altura do armário em milímetros.

2. **ESPECIFICAÇÕES**:
   - **Shelves**: Número de prateleiras.
   - **Partitions**: Número de partições.
   - **Drawers**: Número de gavetas.
   - **Exposed Sides**: Número de lados expostos.

### Passo 4: Calcular Preços de Venda

Clique no botão **"👉🏻 Calculate Selling Price 👈🏻"** para calcular os preços de venda com base nos preços de custo e margens inseridos.

### Passo 5: Calcular Saídas Totais

Após inserir todas as informações necessárias, clique no botão **"👉🏻 Calculate Output 👈🏻"** para gerar as quantidades totais de materiais e estimativas de custos.

### Passo 6: Visualizar Resultados

Os resultados dos cálculos serão exibidos nas seções de saída:

- **Particularidades**: Exibe os preços de venda, preços de custo e quantidades para cada material.
- **Totais**: Exibe os totais gerais de preços de venda, preços de custo e quantidades.
- **Metros Quadrados do Armário e Lados Expostos**: Exibe os cálculos de área em metros quadrados.
- **Lucro**: Exibe o lucro total calculado.

## Tratamento de Erros

O aplicativo possui tratamento básico de erros para garantir uma experiência de uso fluida:

- **Erro no Download da Imagem**: Se o aplicativo não conseguir baixar a imagem fornecida (caso aplicável), uma mensagem de erro será exibida.
- **Campos Obrigatórios**: Se informações obrigatórias não forem fornecidas, o botão de cálculo será desativado e uma mensagem de aviso será exibida.
- **Validação de Entradas**: Certifique-se de inserir valores numéricos válidos nos campos correspondentes para evitar erros de cálculo.

## Contribuindo

Contribuições são bem-vindas! Siga as etapas abaixo para contribuir com este projeto:

1. **Faça um Fork do Repositório**

   Clique no botão "Fork" no canto superior direito da página do repositório.

2. **Crie uma Nova Branch para sua Feature**

   ```
   git checkout -b feature/nome-da-feature
   ```

3. **Faça as Alterações Necessárias**

   Edite o código conforme necessário.

4. **Faça Commit das Suas Alterações**

   ```
   git commit -m "Descrição das alterações"
   ```

5. **Envie a Branch para o Repositório Remoto**

   ```
   git push origin feature/nome-da-feature
   ```

6. **Abra um Pull Request**

   Vá até o repositório original e abra um Pull Request descrevendo suas alterações.

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

# Teoria das Categorias no Brasil

Este repositório contém o código-fonte do site [Teoria das Categorias no Brasil](https://categorias-brasil.github.io/), um ponto central para conectar a comunidade de categoristas no país.

## Como Contribuir

Agradecemos o seu interesse em contribuir para o catálogo! Existem duas formas principais de catalogar pesquisadores e laboratórios:

### 1. Via GitHub (Recomendado)

Siga este passo a passo para adicionar ou atualizar informações:

1.  **Faça um Fork do repositório**: Clique no botão "Fork" no topo desta página para criar uma cópia em sua conta GitHub.
2.  **Clone o seu Fork**:
    ```bash
    git clone https://github.com/SEU-USUARIO/categorias-brasil.github.io.git
    cd categorias-brasil.github.io
    ```
3.  **Crie uma nova branch para sua alteração**:
    ```bash
    git checkout -b adicionar-perfil-nome
    ```
4.  **Adicione seu conteúdo**:
    - **Para Pesquisadores**:
      1. Crie um novo diretório dentro de `pesquisadores/` com o seu nome (ex: `pesquisadores/joao-silva/`).
      2. Dentro deste diretório, crie um arquivo `.qmd` com o mesmo nome (ex: `joao-silva.qmd`).
      3. Use o arquivo `pesquisadores/_pesquisadores-modelo.qmd` como base para o seu perfil.
    - **Para Laboratórios**:
      1. Crie um novo diretório dentro de `laboratorios/` com o nome do laboratório (ex: `laboratorios/meu-lab/`).
      2. Dentro deste diretório, crie um arquivo `.qmd` com o mesmo nome (ex: `meu-lab.qmd`).
      3. Use o arquivo `laboratorios/_laboratorios-modelo.qmd` como base.
    - **Imagens**: Se quiser incluir uma foto ou logo, salve o arquivo de imagem no **mesmo diretório** do seu arquivo `.qmd` e ajuste o campo `image` no cabeçalho (YAML) do arquivo.
5.  **Commit e Push**:
    ```bash
    git add .
    git commit -m "Adiciona perfil de [Seu Nome]"
    git push origin adicionar-perfil-nome
    ```
6.  **Abra um Pull Request**: Vá para o repositório original no GitHub e abra um Pull Request a partir da sua nova branch.

#### Preenchendo o Cabeçalho (YAML)

Os arquivos `.qmd` começam com um bloco entre `---`, chamado YAML. Veja o que preencher:

- `title`: Seu nome completo ou o nome do laboratório.
- `image`: O nome do arquivo de imagem que você colocou na pasta (ex: `"foto.jpg"`).
- `categories`: Uma lista de etiquetas para os filtros do site. 
  - Para pessoas, inclua: `["Cargo", "Área de Pesquisa", "Estado"]`.
  - Para laboratórios, inclua: `["Área", "Instituição"]`.
- `draft: true`: **Importante!** Os modelos vêm com `draft: true` para não serem publicados por acidente. Para que seu perfil apareça no site, você deve **remover esta linha** ou mudá-la para `false`.

### 2. Via E-mail

Se você prefere não lidar diretamente com o código, pode enviar todos os seus dados para:

**[categoriasbrasil@gmail.com](mailto:categoriasbrasil@gmail.com)**

No e-mail, inclua:

- **Nome** completo ou nome do laboratório;
- **Afiliação** institucional (universidade, instituto, etc.);
- **Link** para Currículo Lattes e/ou site pessoal;
- Principais **áreas de pesquisa** em Teoria das Categorias;
- *Opcional:* Uma **foto de perfil** ou logo do laboratório (anexo) e qualquer outra informação relevante.

## Estrutura do Projeto

- `pesquisadores/`: Perfis individuais de pesquisadores. Cada pesquisador deve ter sua própria pasta.
- `laboratorios/`: Perfis de grupos e laboratórios. Cada laboratório deve ter sua própria pasta.
- `blog/`: Postagens e tutoriais.
- `eventos/`: Informações sobre eventos da área.
- `_quarto.yml`: Arquivo de configuração principal do site.

Para mais informações, veja o tutorial no blog: [Como catalogar pesquisadores e laboratórios](https://categorias-brasil.github.io/blog/como-catalogar/).


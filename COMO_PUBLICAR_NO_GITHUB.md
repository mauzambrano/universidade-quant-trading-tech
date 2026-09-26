# Como publicar a Universidade Quant/Trading Tech no GitHub

## Opção A — pelo site do GitHub (mais fácil)

1. Entre no GitHub.
2. Clique em **New repository**.
3. Nome sugerido: `universidade-quant-trading-tech`
4. Escolha **Public** se quiser acessar o curso de qualquer lugar.
5. **Não marque** as opções de criar README, `.gitignore` ou licença — o pacote já contém esses arquivos.
6. Crie o repositório.
7. Na página vazia do repositório, escolha **uploading an existing file**.
8. Extraia este pacote no computador.
9. Arraste **todo o conteúdo da pasta do projeto**, e não a pasta externa inteira, para a área de upload.
10. Faça o commit na branch `main`.

## Opção B — pelo Git no computador

Abra o terminal dentro desta pasta e execute:

```bash
git init
git branch -M main
git add .
git commit -m "feat: cria Universidade Quant Trading Tech"
git remote add origin https://github.com/SEU_USUARIO/universidade-quant-trading-tech.git
git push -u origin main
```

Substitua `SEU_USUARIO` pelo seu usuário do GitHub.

## Ativar o site do curso

O projeto já possui o workflow:

```text
.github/workflows/pages.yml
```

Depois do primeiro `push`:

1. Abra **Settings** do repositório.
2. Entre em **Pages**.
3. Em **Build and deployment**, selecione **GitHub Actions**.
4. Aguarde o workflow terminar em **Actions**.
5. O GitHub mostrará o endereço publicado em **Pages**.

O site publicado usa:

```text
site/index.html
```

## Estrutura principal

```text
universidade-quant-trading-tech/
├── .github/
│   └── workflows/
│       └── pages.yml
├── docs/
│   ├── 00-fundamentos/
│   ├── 01-python/
│   ├── 02-dados-e-sql/
│   ├── 03-mercado/
│   ├── 04-quant/
│   ├── 05-machine-learning/
│   ├── 06-engenharia/
│   └── 07-trading-tech/
├── labs/
├── projetos/
├── obsidian/
├── site/
├── README.md
├── course.json
├── course-manifest.json
├── .gitignore
└── LICENSE
```

## Regra importante

No upload pelo navegador, envie os **arquivos e pastas que estão dentro de `Universidade_Quant_TradingTech`**. Não crie uma segunda pasta chamada `Universidade_Quant_TradingTech` dentro do repositório.

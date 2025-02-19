# 📩 Processador de E-mails e PDFs

Este projeto automatiza o processamento de e-mails recebidos, fazendo o download de anexos em PDF para um diretório principal. Caso existam senhas nos arquivos, é possível realizar a descriptografia com base no dicionário de senhas presente no arquivo pass.txt

Após a descriptografia, os arquivos são movidos para um diretório de "desbloqueados", onde seu conteúdo será organizado em pastas, seguindo uma estrutura de data extraída dos PDFs.

Exemplo: ANO > MES > DIA > NOME_PDF

## 🚀 Funcionalidades

- Conexão com servidor de e-mail via IMAP
- Download de anexos em PDF
- Extração de texto dos PDFs
- Organização de e-mails em pastas conforme os dados extraidos

## 📌 Pré-requisitos

- Python 3.8+
- Conta de e-mail compatível com IMAP
- Permissões para aplicativos de terceiros (caso necessário)

## 📚 Dependencias

```bash
pip install pdfplumber
pip install PyPDF2
pip install pillow
pip install pytesseract
pip install pdf2image
```

## 🛠️ Instalação

Clone este repositório:

```bash
git clone https://github.com/invazing/EmailPDFExtractor/
cd /EmailPDFExtractor/
```

## ⚙️ Configuração

Edite o arquivo email.env na raiz do projeto com as seguintes informações:

```ini
EMAIL_HOST=imap.seuprovedor.com
EMAIL_PORT=993
EMAIL_USER=seuemail@dominio.com
EMAIL_PASSWORD=sua_senha
SMTP_HOST=smtp.seuprovedor.com
SMTP_PORT=587
SMTP_USER=seuemail@dominio.com
SMTP_PASSWORD=sua_senha
```

## ▶️ Uso
Execute o script principal:

```python
python main.py
```

## 📝 Personalização
- Filtros de e-mail: Você pode alterar os filtros para renomear conforme o exemplo abaixo.

```bash
fornecedores = {
    "NOME_DO_PDF": ["PALAVRA_CHAVE_01, PALAVRA_CHAVE_02"]
	}
```

## 💰 Doações
- PIX: 21jdu82jd8sa9jd091jd90182dsa
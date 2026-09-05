# BISONX Lite

Assistente de IA **gratuito e focado em privacidade** que roda direto no seu
computador. As respostas são geradas **sem nuvem e sem assinatura**: modelos de
IA locais via [Ollama](https://ollama.com), instalados na sua própria máquina.
Ele consegue criar arquivos, criar projetos, ler/listar arquivos e rodar
scripts Python.

Uso pessoal liberado para o usuário final. O código-fonte não é público e está
protegido por termos de uso revogáveis (veja o arquivo [LICENSE](LICENSE)).

---

## O que o BISONX é

O BISONX é um assistente pessoal por IA. A **versão Lite** é a edição aberta e
gratuita, feita para qualquer pessoa instalar e usar sem depender de serviços
pagos. Tudo o que ele faz acontece na sua máquina: a conversa e a geração de
código usam apenas os modelos locais do Ollama (`phi3:mini` e `llama3.2`).

## Requisitos

- Windows 10 ou 11 (ou Linux/MacOS) com Python 3.8+
- [Ollama](https://ollama.com) instalado (gratuito)
- Os modelos locais baixados (comandos abaixo)

## Instalação

### 1. Python

Instale o Python 3.8 ou mais novo em https://www.python.org/downloads/

No Windows, na instalação, marque a opção **"Add python.exe to PATH"**.

### 2. Ollama

Instale o aplicativo em https://ollama.com/download/windows

Depois abra um terminal e baixe os modelos (uma vez só):

```powershell
ollama pull phi3:mini
ollama pull llama3.2
```

### 3. BISONX Lite

Baixe/descompacte esta pasta e, dentro dela:

```powershell
install.bat
```

O instalador confere se o Python e o Ollama estão no lugar e mostra como rodar.

## Como usar

| Comando | O que você digita |
|---|---|
| Conversar | `oi, tudo bem?` |
| Criar arquivo | `crie um arquivo hello.txt` |
| Criar projeto | `crie um projeto jogo_da_memoria` |
| Listar projetos | `quais são meus projetos` |
| Remover projeto | `remove projeto NOME` |
| Listar arquivos | `lista a pasta` |
| Ler arquivo | `leia o arquivo hello.txt` |
| Rodar Python | `rode o script main.py` |
| Status | `status` |
| Ajuda | `ajuda` |

### Terminal (modo texto)

```powershell
python bisonx_lite\motor.py
```

### Janela (modo visual)

```powershell
python bisonx_lite_gui.py
```

### Teste rápido

```powershell
python test_lite.py
```

Verifica se tudo está instalado e se o comando `crie um arquivo hello.txt`
funciona de ponta a ponta.

---

## Limites da versão Lite

| Recurso | Lite (gratuita) |
|---|---|
| Respostas da IA | Locais, na sua máquina (sem nuvem) |
| Integração com WhatsApp | Não |
| Modelos de IA | Somente locais (phi3:mini / llama3.2) |
| Comandos de programação | Até 50 por dia |
| Projetos ativos | Até 3 por vez |
| Código aberto | Não (uso com permissão, termos revogáveis) |

Os limites de comando e de projetos reiniciam sozinhos: os comandos voltam
todos os dias à 0h, e os projetos podem ser removidos a qualquer momento com
`remove projeto NOME` para liberar espaço.

## Termos de uso

O BISONX Lite é um programa original do autor. Você pode **usar** gratuitamente
no seu computador, mas **não pode copiar, modificar nem vender** o código, nem
publicá-lo em qualquer lugar. Você pode repassar o programa para outra pessoa,
desde que sem alterações e sem cobrança. A licença é **revogável a qualquer
momento** pelo autor — ao receber a revogação, você deve parar de usar e apagar
as cópias. O uso do programa significa que você aceita os termos completos do
arquivo [LICENSE](LICENSE).

## Privacidade e estatísticas de uso

As conversas e o que você digita **nunca** saem do seu computador — a IA roda
toda local. A única exceção, e só quando configurada pelo autor, é um
"bate-ponto diário" opcional: 1 vez por dia o programa pode enviar ao autor
**apenas** o número da matrícula da cópia, a data e a quantidade de comandos de
programação usados naquele dia (para estatísticas de uso). Nada do que você
digita é enviado. Você pode desativar na hora apagando o arquivo
`estado/telemetria.json`.

## Diferença entre Lite e Pro

A versão **Pro** (fechada) é a edição completa do BISONX com recursos
avançados, pensada para uso profissional:

| Recurso | Lite | Pro |
|---|---|---|
| Modelos de IA | Somente locais | Locais + nuvem (mais rápida) |
| WhatsApp | Não | Sim (envio com confirmação) |
| Comandos de programação | 50/dia | Ilimitados |
| Projetos ativos | 3 | Ilimitados |
| Foco | Aprendizado e uso leve | Automação profissional |

Para saber mais sobre a versão Pro, entre em contato pelo perfil do projeto:
https://github.com/robisonacquashop-ui

## Licença

Este é um programa original do autor, distribuído sob **Termos de Uso
revogáveis** (não é código aberto). Leia o arquivo [LICENSE](LICENSE) para os
termos completos. Em resumo: você pode **usar**, mas **não pode copiar,
modificar nem vender** o código, e a permissão de uso pode ser **revogada a
qualquer momento** pelo autor.
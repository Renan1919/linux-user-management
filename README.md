# 🚀 Automatizando a Gestão de Usuários e Permissões no Ubuntu 🚀

Olá! Seja bem-vindo(a)! 👋

Aqui, você vai encontrar um conjunto de scripts Bash super práticos que criei para facilitar a vida na hora de gerenciar usuários, grupos e permissões no seu sistema Ubuntu. A ideia é automatizar tarefas que, no dia a dia, podem tomar um tempão!

**Compatibilidade:** Os comandos utilizados nestes scripts são **padrão em sistemas Linux** e foram testados no Ubuntu. Eles são totalmente compatíveis com outras distribuições baseadas em Debian, como o próprio Debian, e a maioria das distribuições Linux em geral.

## O Que Você Vai Encontrar Aqui? 📂

Neste repositório, preparei dois scripts essenciais:

* `iac.sh`: Pense nele como seu "braço direito" para configurar a infraestrutura inicial. Ele cuida de criar diretórios organizados, os grupos de usuários que você precisa, e já deixa tudo com as permissões certas. É a sua Infraestrutura como Código (IaC) simplificada!
* `criar_user.sh`: Este script é perfeito para quando você precisa criar rapidamente alguns usuários "convidados" ou com configurações mais específicas. Tudo de forma rápida e eficiente.

## Antes de Começar, o Que Você Precisa? ✅

Para colocar esses scripts para rodar no seu sistema, você só vai precisar de algumas coisinhas:

* Um sistema rodando **Ubuntu** (ou outra distribuição Linux compatível, como Debian).
* Acesso ao seu sistema via terminal.
* **Atenção!** Como os scripts vão criar usuários, grupos e ajustar permissões, você precisará de **privilégios de superusuário (root)** para executá-los.

## Mãos à Obra! Como Usar os Scripts? 🧑‍💻

Siga este passo a passo para criar e executar os scripts no seu Ubuntu. É bem simples!

### 1. Acesse o Terminal 💻

Abra o terminal do seu Ubuntu. Você pode fazer isso procurando por "Terminal" no menu de aplicativos ou usando o atalho `Ctrl+Alt+T`.

### 2. Criar os scripts diretamente no terminal (Usando `nano`)

Vamos usar o editor de texto simples `nano` para criar e colar o conteúdo dos seus scripts diretamente no terminal.

#### Para criar o script `iac.sh`:

1.  Digite o comando abaixo e pressione `Enter`:
    ```bash
    nano iac.sh
    ```
2.  O editor `nano` será aberto. Agora, **cole todo o conteúdo do seu script `iac.sh`** (aquele que você me enviou anteriormente) dentro do editor.
3.  Para salvar o arquivo e sair, pressione `Ctrl+X`. O `nano` perguntará se você quer salvar; pressione `Y` (de "Yes") e, em seguida, `Enter` para confirmar o nome do arquivo.

#### Para criar o script `criar_user.sh`:

1.  Digite o comando abaixo e pressione `Enter`:
    ```bash
    nano criar_user.sh
    ```
2.  O editor `nano` será aberto novamente. Agora, **cole todo o conteúdo do seu script `criar_user.sh`** (o que você me enviou) dentro do editor.
3.  Para salvar o arquivo e sair, pressione `Ctrl+X`. Pressione `Y` para salvar e `Enter` para confirmar o nome do arquivo.

### Conceder Permissão de Execução ✨

Antes de rodar os scripts, precisamos dar a eles "permissão para executar". Faça isso com os seguintes comandos:

```bash
chmod +x iac.sh
chmod +x criar_user.sh
```

### Executar o Script iac.sh (A Configuração Principal!) 🛠️
Este script vai ser o primeiro a rodar. Ele vai configurar toda a estrutura inicial: diretórios, grupos e os primeiros usuários, além de definir as permissões certas. Lembre-se, execute como root (usando sudo):

```bash
sudo ./iac.sh
```

### Executar o Script criar_user.sh (Para os Convidados!) 👥
Agora, se precisar de usuários convidados, este script é perfeito. Também execute como root:

```bash
sudo ./criar_user.sh
```

* Criar os usuários guest10, guest11, guest12 e guest13.
* Definir a senha inicial de todos como "Senha123".
* Importante: A senha de cada "guest" será configurada para expirar no primeiro login, forçando-os a criar uma nova senha para sua própria segurança.

## 🚨 Pontos Cruciais Sobre Segurança! 🚨

**Para um ambiente de produção ou qualquer sistema que você valorize, por favor, considere estes pontos muito importantes:**

* **⚠️ Senhas nos scripts:** As senhas iniciais (`Senha123`) estão visíveis diretamente nos scripts. Em um ambiente real, **o ideal é que as senhas sejam geradas aleatoriamente e/ou que os usuários sejam forçados a definir suas próprias senhas no primeiro acesso.** Nunca use senhas fixas e óbvias em produção!
* **🚫 Permissão `777` em `/publico`:** Deixar um diretório com `777` significa que *qualquer um* pode ler, escrever e executar arquivos nele. Pense muito bem se essa é a permissão ideal para o seu caso de uso, pois **pode apresentar sérios riscos de segurança** se informações sensíveis forem armazenadas lá. Use com extrema cautela!
* **🔍 Sempre revise o código:** Antes de rodar **qualquer script** baixado da internet (inclusive os meus!), **SEMPRE revise o código linha por linha**. Entender exatamente o que ele faz é **crucial para a segurança do seu sistema**. Nunca execute um script sem entender suas ações!

---

Espero que estes scripts sejam extremamente úteis para você no seu cotidiano com o Linux! Sua contribuição é muito valorizada. Caso tenha dúvidas, sugestões de melhoria ou deseje colaborar, por favor, não hesite em abrir uma *issue* ou enviar um *pull request*.

Happy Hacking! ✨

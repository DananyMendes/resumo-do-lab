# Laboratório - Configurando Azure Storage

## **Objetivo**
Criar uma conta de armazenamento, configurar um blob container e carregar um arquivo.

---

## **Passo 1: Criar uma Conta de Armazenamento**
1. Acesse o **Portal do Azure**: [https://portal.azure.com](https://portal.azure.com).
2. Clique em **Criar um recurso** no menu superior esquerdo.
3. Pesquise por **Conta de Armazenamento** e selecione.
4. Preencha as seguintes informações:
   - **Assinatura**: Escolha a sua assinatura.
   - **Grupo de Recursos**: Crie um novo ou use um existente (exemplo: `rg-armazenamento`).
   - **Nome da Conta de Armazenamento**: Escolha um nome único (exemplo: `minhaconta123`).
   - **Região**: Escolha uma região próxima (exemplo: `East US`).
   - **Desempenho**: Standard.
   - **Redundância**: LRS (Locally Redundant Storage).
5. Clique em **Revisar + Criar** e depois em **Criar**.

---

## **Passo 2: Criar um Blob Container**
1. Após a criação da conta de armazenamento, clique nela para acessá-la.
2. No menu lateral, selecione **Containers**.
3. Clique em **+ Container** e preencha:
   - **Nome**: `meus-arquivos`.
   - **Nível de acesso público**: Private (sem acesso público).
4. Clique em **Criar**.

---

## **Passo 3: Carregar um Arquivo**
1. Acesse o container `meus-arquivos`.
2. Clique em **Carregar** (Upload).
3. Escolha um arquivo do seu computador (exemplo: `exemplo.txt`).
4. Clique em **Carregar**.

---

## **Passo 4: Gerar uma SAS (Shared Access Signature)**
1. Na conta de armazenamento, clique em **Shared Access Signature (SAS)** no menu lateral.
2. Configure as permissões:
   - **Permissões**: Leitura, escrita.
   - **Intervalo de Tempo**: Configure 1 dia a partir do momento atual.
3. Clique em **Gerar SAS e URL**.
4. Copie o **Blob SAS URL** gerado.

---

## **Passo 5: Testar o Acesso ao Arquivo**
1. Abra o URL gerado no navegador.
2. Verifique se o arquivo está acessível (exemplo: exibe o conteúdo do `exemplo.txt`).

---

## **Passo 6: Limpar os Recursos**
1. Exclua o container `meus-arquivos`.
2. Exclua a conta de armazenamento.
3. Exclua o grupo de recursos `rg-armazenamento`.

---

## **Resultado Final**
- Criamos uma conta de armazenamento.
- Configuramos um container de blob privado.
- Carregamos um arquivo e acessamos via SAS.

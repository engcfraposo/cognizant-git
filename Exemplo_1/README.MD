
1. **Crie um repositório Git e um arquivo de texto**:

   Primeiro, crie um diretório e inicie um repositório Git nele:

   ```bash
   mkdir meu-repositorio
   cd meu-repositorio
   git init
   ```

   Em seguida, crie um arquivo de texto chamado "exemplo.txt" e adicione algum conteúdo a ele:

   ```bash
   echo "Este é o conteúdo inicial do arquivo." > exemplo.txt
   ```

2. **Adicione o arquivo ao Stage e faça um Commit**:

   Adicione o arquivo ao stage e faça um commit inicial:

   ```bash
   git add exemplo.txt
   git commit -m "Adicionando arquivo de exemplo"
   ```

3. **Edite o arquivo de texto**:

   Abra o arquivo "exemplo.txt" em um editor de texto e faça as edições desejadas. Por exemplo, você pode adicionar mais texto ou fazer alterações no conteúdo existente.

4. **Verifique o status das alterações**:

   Use o seguinte comando para verificar o status das alterações:

   ```bash
   git status
   ```

   Isso mostrará que o arquivo "exemplo.txt" foi modificado.

5. **Adicione as alterações ao Stage e faça um novo Commit**:

   Adicione as alterações ao stage e faça um novo commit com uma mensagem que descreva as alterações feitas:

   ```bash
   git add exemplo.txt
   git commit -m "Atualizando o arquivo de exemplo"
   ```

Agora, você editou com sucesso o arquivo de texto "exemplo.txt" e registrou essas alterações usando o Git. O histórico de versões do arquivo será mantido no repositório Git.

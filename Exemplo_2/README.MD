Suponha que você tenha dois branches: `branch-feature` e `branch-master`, e você deseja mesclar as alterações de `branch-feature` em `branch-master`.

1. **Criar e alternar para o branch de recurso (feature):**

   ```bash
   git checkout -b branch-feature
   ```

   Faça algumas alterações no arquivo `exemplo.txt` no branch de recurso e faça um commit:

   ```bash
   echo "Conteúdo no branch de recurso." >> exemplo.txt
   git add exemplo.txt
   git commit -m "Alterações no branch de recurso"
   ```

2. **Alternar para o branch principal (master):**

   ```bash
   git checkout master
   ```

   Faça algumas alterações no mesmo arquivo `exemplo.txt` no branch principal e faça um commit:

   ```bash
   echo "Conteúdo no branch principal." >> exemplo.txt
   git add exemplo.txt
   git commit -m "Alterações no branch principal"
   ```

3. **Mesclar o branch de recurso (feature) no branch principal (master):**

   ```bash
   git merge branch-feature
   ```

   Isso resultará em um conflito, já que ambos os branches modificaram a mesma parte do arquivo `exemplo.txt`.

4. **Resolução de conflitos:**

   Abra o arquivo `exemplo.txt` em um editor de texto. Você verá marcações que indicam as partes conflitantes, semelhantes a isso:

   ```plaintext
   Conteúdo no branch principal.
   <<<<<<< HEAD
   Conteúdo no branch de recurso.
   =======
   >>>>>>> branch-feature
   ```

   Edite o arquivo para manter as partes que deseja manter, removendo as marcações de conflito e as partes indesejadas. Por exemplo:

   ```plaintext
   Conteúdo no branch principal.
   Conteúdo no branch de recurso.
   ```

5. **Adicionar e fazer commit das alterações de resolução de conflitos:**

   Após editar o arquivo para resolver o conflito, adicione o arquivo e faça um commit:

   ```bash
   git add exemplo.txt
   git commit -m "Resolvido conflito de mesclagem"
   ```

Agora as alterações do branch de recurso foram mescladas com sucesso no branch principal após a resolução do conflito. Isso é uma prática comum ao trabalhar em projetos colaborativos com o Git.

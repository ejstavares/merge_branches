# merge_branches
# Guia: Criando e Mesclando uma Nova Branch no Git

Este guia descreve o processo para trabalhar com branches novas para desenvolver nela e depois mesclá-la (merge) ao branch `main`.

## Passos

### 1. Certifique-se de estar na branch `main` e atualizado
```bash
git checkout main
```
```bash
git pull origin main
```

### 2. Crie e mude para a nova branch `newFeatureEder`
```bash
git checkout -b newFeatureEder
```

### 3. Desenvolva suas alterações
Edite ou adicione arquivos conforme necessário.

### 4. Adicione e faça commit das mudanças
```bash
git add .
```
```bash
git commit -m "Adicionando nova funcionalidade na branch newFeatureEder"
```

### 5. Envie a branch para o repositório remoto
```bash
git push origin newFeatureEder
```

### 6. Volte para a branch `main` e atualize
```bash
git checkout main
```
```bash
git pull origin main
```

### 7. Faça o merge da branch `newFeatureEder` na `main`
```bash
git merge newFeatureEder
```

### 8. Resolva conflitos (se houver)
Caso o Git avise sobre conflitos, edite os arquivos manualmente, depois:
```bash
git add .
```
```bash
git commit -m "Resolvendo conflitos no merge da newFeatureEder"
```

### 9. Envie as alterações para o repositório remoto
```bash
git push origin main
```

### 10. (Opcional) Apague a branch `newFeatureEder`
Se não precisar mais da branch, pode removê-la:
```bash
git branch -d newFeatureEder
```
```bash
git push origin --delete newFeatureEder
```

Agora sua funcionalidade foi integrada na `main`. 🚀

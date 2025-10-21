```markdown
# Checklist de Prioridades

Aplicativo web simples (HTML/CSS/JS) para gerenciar tarefas:
- Adicionar tarefas;
- Marcar concluídas (checkbox) — texto riscado;
- Excluir tarefas individualmente;
- Reordenar tarefas por arrastar (drag & drop) para definir prioridades;
- Salvar / Baixar em `.txt` com formato: `1. [X] Tarefa (priority)`;
- Fazer Upload de um `.txt` gerado pelo app — o site lê e importa as tarefas.

Como usar localmente
1. Abra `index.html` em um navegador moderno (Chrome, Firefox, Edge, Safari).
2. Use o input para digitar tarefas e o botão "Adicionar" (ou Enter).
3. Use a alça (≡) para arrastar e definir ordem (topo = prioridade 1).
4. Clique "💾 Salvar / Baixar" para gerar `minhas_tarefas.txt`.
5. Clique "📤 Upload" para importar um `.txt` no mesmo formato (aceita variantes).

Publicar no GitHub (passo a passo - via terminal)
Substitua SEU_EMAIL e SEU_NOME quando necessário (opcional).

```bash
# 1) criar pasta local e inicializar git
mkdir checklist-prioridades
cd checklist-prioridades

# 2) cole aqui index.html e README.md (ou salve os arquivos fornecidos)

git init
git add .
git commit -m "Initial commit: checklist app"

# 3) criar repositório remoto no GitHub e enviar (opção com gh CLI):
gh repo create victorsantos5-hash/checklist-prioridades --public --source=. --remote=origin --push

# Se não usar gh CLI, crie o repo no site do GitHub e então:
# git remote add origin git@github.com:SEU_USUARIO/checklist-prioridades.git
# git branch -M main
# git push -u origin main
```

Publicar como site (GitHub Pages)
1. No repositório do GitHub, vá em Settings → Pages.
2. Em "Build and deployment", escolha Branch: `main` e pasta `/ (root)`.
3. Salve. O site estará disponível em https://<seu-usuario>.github.io/checklist-prioridades/ (pode demorar alguns minutos).

Observações
- O parser de upload aceita linhas com ou sem prefixo numérico, reconhece `[X]` como concluída e aceita prioridade em parênteses (ex.: `(high)` ou `(alta)`).
- Se quiser eu posso:
  - Gerar um arquivo ZIP contendo index.html e README.md para você baixar,
  - Gerar os mesmos comandos mas com SSH/HTTPS explicitados conforme sua preferência.
```
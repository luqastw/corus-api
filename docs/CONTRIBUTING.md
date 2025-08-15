# 💾 Boas Práticas com Git e GitHub.

## Estrutura do projeto e exemplo de fluxo Git:

1. **Branch principal (`main`)**:  
   É a versão estável do código, a que está pronta para produção.

2. **Branches de funcionalidade:**  
   Crie novas branches a partir da `main` para realizar cada tarefa.
   Exemplo:

   - `feature/nome-da-funcionalidade`
   - `bugfix/nome-do-bug`
   - `hotfix/nome-da-correção`

3. **Fluxo de trabalho:**

   - Atualize a `main` antes de iniciar a tarefa:
     ```bash
     git checkout main
     git pull origin main
     ```
   - Crie sua branch:
     ```bash
     git checkout -b feature/nome-da-funcionalidade
     ```
   - Faça commits frequentes, claros e pequenos para melhor entendimento de todos.
   - Atualize sua branch com as últimas mudanças da `main` antes do Pull Request.
     ```bash
     git checkout main
     git pull origin main
     git checkout feature/nome-da-funcionalidade
     git merge main
     ```
   - Abra um Pull Request para revisão da sua modificação na main.

4. **Pull Requests:**

   - Os códigos vão passar por uma revisão geral por todos.
   - Nenhum merge vai ser feito diretamente na `main` sem essa revisão.

5. **Resolução de conflitos:**

   - Os conflitos vão ser resolvidos manualmente por você mesmo antes de fazer o envio do código.
   - Teste o código após resolver pra evitar quaisquer problemas futuros.

---

## Boas práticas de commit:

- Use mensagens descritivas e em português, usando as mesmas tags de antes já citadas. Exemplo:
  ```
  feat: adicionar sistema de login
  fix: corrigir erro de validação no formulário
  docs: atualizar README com instruções
  ```
- Faça commits pequenos a cada alteração feita, sem que sejam acumuladas várias alterações.

---

# Modelo de Pull Request (PR):

**Título:**  
`[Tag da alteração] descrição`

Exemplos:

- `[feat] Implementa autenticação via OAuth`
- `[fix] Corrige bug na validação do formulário`

**Descrição:**

- Qual problema a mudança resolve?
- Como foi implementado?
- Passos para testar.
- Issues relacionadas (ex: #123).

---

# Checklist para Revisão de Código:

- [ ] O código está funcionando e testado?
- [ ] As mensagens de commit são claras e coerentes?
- [ ] Código está formatado e segue padrões da equipe?
- [ ] Não há código morto ou comentários desnecessários?
- [ ] Alterações impactam outras áreas? Se sim, foram testadas?
- [ ] Segurança e performance foram consideradas?
- [ ] O PR está vinculado a uma issue relevante?
- [ ] As documentações (README, comentários) foram atualizadas?

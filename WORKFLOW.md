WORKFLOW.md

Catálogo de Cursos da Faculdade — projeto com as seções: Áreas, Curso Detalhado e Contato.

1. Modelo de workflow

A gente vai usar o GitHub Flow, porque é mais simples e a gente é só dupla, não precisa de um monte de branch complicada tipo Git Flow.

Regra é essa:

main sempre tem que ficar funcionando, sem bug.
Quer mexer em algo? Cria uma branch nova a partir da main.
Termina a parte, testa, dá merge de volta na main.

2. Estratégia de branches

Nome da branch segue esse padrão:
tipo/nome-curto-da-tarefa

Exemplos:
feat/pagina-areas
fix/erro-menu-contato
docs/atualizar-readme

Merge sempre é: branch da tarefa → main. Nunca commit direto na main, só merge.

3. Quando atualizar a main
Só sobe pra main quando a parte tá pronta e testada (abriu no navegador e não quebrou nada).
Antes de começar uma branch nova, dá um git pull na main pra não ficar com código velho.

4. Revisão / integração
Como é só dupla, a regra é: antes de dar merge, manda mensagem pro outro avisando "vou subir tal coisa". Se dois mexeram no mesmo arquivo, um dos dois olha o código antes de aceitar o merge, só pra não sobrescrever nada.

5. Commits Semânticos

Sintaxe usada:
tipo(escopo): descrição
Exemplo: feat(areas): adiciona lista de áreas do catálogo

Tipos comuns usados

Tipo	Quando usar
feat	quando adiciona algo novo no site
fix	quando conserta um bug
docs	quando mexe em documentação (README, WORKFLOW)
style	quando muda só visual/CSS, sem mudar funcionalidade
refactor	quando organiza o código sem mudar o que ele faz
chore	tarefa de manutenção, tipo configurar coisa do projeto

Tipos inéditos criados pro projeto
Tipo	Quando usar
curso	quando mexe nos dados/conteúdo de um curso (nome, descrição, carga horária etc)
area	quando mexe nas áreas do catálogo (adicionar área nova, editar área)
contato	quando mexe na seção de contato (formulário, telefone, e-mail, endereço)

Esses 3 a gente criou porque o projeto tem seção específica pra cada coisa (áreas, curso, contato), então separar ajuda a saber rapidinho o que mudou só de ler o commit.

6. Histórico de commits do projeto
first-commit — commit inicial do repositório
add: markdown.md — criação do arquivo de documentação
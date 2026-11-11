# Tech-2D

Projetos escolares feitos para acompanhar as atividades da turma e consultar os horários dos professores.

| Projeto | Para que serve | Onde mexer |
| --- | --- | --- |
| [Agenda da turma](https://tech-2d.github.io/Agenda/) | Calendário, atividades, avisos e ferramentas dos representantes | [Tech-2D/Agenda](https://github.com/Tech-2D/Agenda) |
| [Cadê o professor?](https://tech-2d.github.io/professores/) | Busca de professores, horários e salas por turma ou matéria | [Tech-2D/professores](https://github.com/Tech-2D/professores) |

## Primeiros passos para contribuir

1. Abra o site que você quer melhorar e localize a tela ou o fluxo em questão.
2. Clone o repositório correspondente. Os dois sites usam React, TypeScript e Vite. Com o Node.js 22, rode `npm ci` e `npm run dev` na pasta do projeto.
3. Use uma branch para a sua alteração. Rode `npm test`, `npm run lint` e `npm run build` antes de abrir o pull request.
4. No pull request, descreva como conferir a mudança. Para alterações visuais, inclua uma captura de tela. O GitHub Actions publica os sites no GitHub Pages a partir da `main`.

Para propor uma melhoria ou relatar um problema, abra uma issue no repositório do site com a tela afetada e os passos para reproduzir. [Issues da Agenda](https://github.com/Tech-2D/Agenda/issues) · [Issues de Cadê o professor?](https://github.com/Tech-2D/professores/issues)

## Como os projetos se conectam

- **Sites.** O calendário, os avisos e o painel dos representantes ficam no repositório Agenda. As buscas e a administração dos horários ficam no repositório professores.
- **Dados e login.** Os dados dos sites ficam no PostgreSQL. A API roda no Cloudflare Workers e o Firebase Authentication gerencia as contas. A API compartilhada dos dois sites fica no repositório privado [Tech-2D/api](https://github.com/Tech-2D/api).
- **Serviços de apoio.** Recuperação de senha, anexos, consultas e automações da Agenda têm repositórios próprios. Com acesso à organização, consulte a aba [Repositórios](https://github.com/orgs/Tech-2D/repositories) e use os tópicos `frontend`, `backend`, `agenda` e `automacao` para encontrar o projeto certo.

Para testar fluxos que dependem do backend, alinhe com a equipe o ambiente e a conta de teste. Mantenha credenciais, dados de alunos e capturas com informações pessoais fora de issues e pull requests públicos.

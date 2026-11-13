# Tech-2D

Projetos escolares feitos para acompanhar as atividades da turma, consultar os horários dos professores e calcular as notas.

| Projeto | Para que serve | Onde mexer |
| --- | --- | --- |
| [Agenda da turma](https://tech-2d.github.io/Agenda/) | Calendário, atividades, avisos e ferramentas dos representantes | [Tech-2D/Agenda](https://github.com/Tech-2D/Agenda) |
| [Cadê o professor?](https://tech-2d.github.io/professores/) | Busca de professores, horários e salas por turma ou matéria | [Tech-2D/professores](https://github.com/Tech-2D/professores) |
| [Pegaki](https://tech-2d.github.io/pegaki/) | Médias do semestre e do ano, nota que falta para passar, importação do boletim em PDF e exportação no modelo da escola | [Tech-2D/pegaki](https://github.com/Tech-2D/pegaki) |

## Primeiros passos para contribuir

1. Abra o site que você quer melhorar e localize a tela ou o fluxo em questão.
2. Clone o repositório correspondente. Os sites usam React, TypeScript e Vite. Com o Node.js 22, rode `npm ci` e `npm run dev` na pasta do projeto.
3. Use uma branch para a sua alteração. Rode `npm test` e `npm run build` antes de abrir o pull request, além de `npm run lint` nos projetos que têm esse script.
4. No pull request, descreva como conferir a mudança. Para alterações visuais, inclua uma captura de tela. O GitHub Actions publica os sites no GitHub Pages a partir da `main`.

Para propor uma melhoria ou relatar um problema, abra uma issue no repositório do site com a tela afetada e os passos para reproduzir. [Issues da Agenda](https://github.com/Tech-2D/Agenda/issues) · [Issues de Cadê o professor?](https://github.com/Tech-2D/professores/issues) · [Issues do Pegaki](https://github.com/Tech-2D/pegaki/issues)

## Como os projetos se conectam

- **Sites.** O calendário, os avisos e o painel dos representantes ficam no repositório Agenda. As buscas e a administração dos horários ficam no repositório professores.
- **Dados e login.** Os dados da Agenda e do Cadê o professor? ficam no PostgreSQL. A API roda no Cloudflare Workers e o Firebase Authentication gerencia as contas. A API compartilhada dos dois sites fica no repositório privado [Tech-2D/api](https://github.com/Tech-2D/api).
- **Pegaki.** Roda só no navegador, sem API nem login. As notas ficam salvas no próprio navegador e o PDF do boletim é lido ali mesmo, sem ser enviado para nenhum servidor.
- **Serviços de apoio.** Recuperação de senha, anexos, consultas e automações da Agenda têm repositórios próprios. Com acesso à organização, consulte a aba [Repositórios](https://github.com/orgs/Tech-2D/repositories) e use os tópicos `frontend`, `backend`, `agenda` e `automacao` para encontrar o projeto certo.

Para testar fluxos que dependem do backend, alinhe com a equipe o ambiente e a conta de teste. Mantenha credenciais, dados de alunos e capturas com informações pessoais fora de issues e pull requests públicos.

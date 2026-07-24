# Fluxo — Gestão inteligente

Aplicação de CRM estática construída com HTML, CSS e JavaScript puros. Não requer Docker, banco de dados ou servidor: abra o arquivo `index.html` diretamente em um navegador moderno.

## Acessos de demonstração

| Perfil | E-mail | Senha | Permissões |
| --- | --- | --- | --- |
| Administrador | `admin@simplify.com` | `Simplify@2026` | Opera o CRM, gerencia usuários e consulta a auditoria. |
| Operador | `operador@simplify.com` | `Operador@2026` | Opera dashboard, clientes, catálogo e carrinho. |

Antes de entrar, resolva o CAPTCHA matemático exibido no formulário. O desafio pode ser renovado pelo botão `↻`.

## Recursos

- Dashboard interativo e gestão de clientes.
- Cadastro, edição, atualização de status e exclusão com confirmações SweetAlert2.
- Telefone com máscara, consulta de CEP pela ViaCEP e preenchimento assistido de endereço.
- Dados de clientes persistidos no `localStorage` do navegador, com carga inicial de usuários da [Fake Store API](https://fakestoreapi.com/users).
- Catálogo conectado à [Fake Store API](https://fakestoreapi.com/).
- Drawer lateral de produto, galeria com navegação quando a API disponibiliza fotos extras e carrinho persistente, com ajuste de quantidades e cálculo do total.
- Controle de acesso por perfil: administradores podem criar, editar e listar usuários, além de consultar a auditoria; operadores não veem essas áreas.
- Log de auditoria persistente para ações de acesso, clientes, endereços, carrinho e usuários.
- Login demonstrativo com senhas derivadas com PBKDF2, CAPTCHA e bloqueio temporário após tentativas inválidas.

> O login, os perfis e o CAPTCHA são proteções de demonstração para uma aplicação 100% estática. Usuários, hashes de senha e permissões ficam no `localStorage` deste navegador. Em produção, credenciais, permissões e verificações devem ser validadas por um backend seguro.

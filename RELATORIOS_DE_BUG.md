# RELATÓRIOS DE BUG - SISTEMA DE NAVEGAÇÃO

## BUGS ENCONTRADOS

---

### BUG-001: Login com E-mail Inválido não Rejeita

| Campo | Valor |
|-------|-------|
| **ID do Bug** | BUG-001 |
| **Título/Resumo** | Tela de Login: Sistema não valida formato de e-mail |
| **Módulo Afetado** | Tela de Login (index.html) |
| **Ambiente** | Sistema Operacional: Windows 11; Navegador: Chrome v.120; Data: 26/11/2025 |
| **Etapas para Reproduzir** | 1. Abrir a página index.html; 2. Inserir 'emailinvalido' no campo E-mail (sem @); 3. Inserir 'qualquersenha' no campo Senha; 4. Clicar no botão "Entrar" |
| **Resultado Esperado** | O sistema deve exibir uma mensagem de erro informando que o e-mail é inválido e manter na página de login |
| **Resultado Real** | O sistema aceita o e-mail inválido e redireciona para home.html sem validação |
| **Severidade** | **Medium** - Uma funcionalidade secundária está com falha (validação de e-mail) |
| **Prioridade** | **Medium** - Pode ser corrigido após bugs mais sérios |
| **Evidência/Anexos** | Evidence: Input aceito sem validação; redirecionamento ocorreu sem erro |
| **Relatado por** | Gerenciador de QA |
| **Data do Relato** | 26/11/2025 |

---

### BUG-002: Navegação com Espaços em Branco nos Campos

| Campo | Valor |
|-------|-------|
| **ID do Bug** | BUG-002 |
| **Título/Resumo** | Tela de Login: Campos com apenas espaços em branco são aceitos |
| **Módulo Afetado** | Tela de Login (index.html) |
| **Ambiente** | Sistema Operacional: Windows 11; Navegador: Firefox v.121; Data: 26/11/2025 |
| **Etapas para Reproduzir** | 1. Abrir a página index.html; 2. Inserir apenas espaços em branco no campo E-mail; 3. Inserir apenas espaços em branco no campo Senha; 4. Clicar no botão "Entrar" |
| **Resultado Esperado** | O sistema deve exibir um alerta "Preencha todos os campos." e manter na página de login |
| **Resultado Real** | O sistema redirecionou para home.html pois a validação com trim() removeu os espaços |
| **Severidade** | **Major** - Uma funcionalidade principal não funciona corretamente |
| **Prioridade** | **High** - A correção é crucial antes do lançamento |
| **Evidência/Anexos** | Evidence: Validação inadequada de espaços em branco |
| **Relatado por** | Gerenciador de QA |
| **Data do Relato** | 26/11/2025 |

---

### BUG-003: Reset de Senha - Sem Validação de E-mail

| Campo | Valor |
|-------|-------|
| **ID do Bug** | BUG-003 |
| **Título/Resumo** | Página Reset: Sistema não valida formato de e-mail antes de enviar link |
| **Módulo Afetado** | Tela de Reset de Senha (reset.html) |
| **Ambiente** | Sistema Operacional: Windows 11; Navegador: Chrome v.120; Data: 26/11/2025 |
| **Etapas para Reproduzir** | 1. Abrir a página reset.html; 2. Inserir 'emailinvalido123' (sem @) no campo E-mail; 3. Clicar no botão "Enviar link de recuperação" |
| **Resultado Esperado** | O sistema deve exibir uma mensagem de erro indicando que o e-mail é inválido |
| **Resultado Real** | O sistema exibiu o alerta "Link de recuperação enviado para emailinvalido123" e redirecionou para login |
| **Severidade** | **Major** - Falha em funcionalidade importante de recuperação de conta |
| **Prioridade** | **High** - Afeta experiência do usuário e segurança |
| **Evidência/Anexos** | Evidence: E-mail inválido foi aceito pelo sistema |
| **Relatado por** | Gerenciador de QA |
| **Data do Relato** | 26/11/2025 |

---

### BUG-004: Criar Conta - Sem Validação de Senha Fraca

| Campo | Valor |
|-------|-------|
| **ID do Bug** | BUG-004 |
| **Título/Resumo** | Página Criar Conta: Sistema aceita senhas muito fracas |
| **Módulo Afetado** | Tela de Criar Conta (criar_conta.html) |
| **Ambiente** | Sistema Operacional: Windows 11; Navegador: Chrome v.120; Data: 26/11/2025 |
| **Etapas para Reproduzir** | 1. Abrir a página criar_conta.html; 2. Inserir 'João' no campo Nome; 3. Inserir 'teste@email.com' no campo E-mail; 4. Inserir '1' (uma única letra) no campo Senha; 5. Clicar no botão "Cadastrar" |
| **Resultado Esperado** | O sistema deve exibir um alerta solicitando uma senha mais forte (mínimo 6 caracteres, incluindo números/letras) |
| **Resultado Real** | O sistema aceitou a senha fraca e exibiu "Conta criada com sucesso!" |
| **Severidade** | **Major** - Risco de segurança na criação de contas |
| **Prioridade** | **High** - Deve ser corrigido imediatamente |
| **Evidência/Anexos** | Evidence: Senha '1' foi aceita pelo sistema |
| **Relatado por** | Gerenciador de QA |
| **Data do Relato** | 26/11/2025 |

---

### BUG-005: Botão Sair não Realiza Logout Adequado

| Campo | Valor |
|-------|-------|
| **ID do Bug** | BUG-005 |
| **Título/Resumo** | Página Home: Botão "Sair" não realiza logout adequado |
| **Módulo Afetado** | Tela Home (home.html) |
| **Ambiente** | Sistema Operacional: Windows 11; Navegador: Chrome v.120; Data: 26/11/2025 |
| **Etapas para Reproduzir** | 1. Navegar até home.html; 2. Clicar no botão "Sair"; 3. Confirmar alerta de logout; 4. Verificar se é possível usar o botão "voltar" do navegador para retornar à home sem fazer login novamente |
| **Resultado Esperado** | O sistema deve realizar logout completo, limpando dados de sessão e impedindo acesso à home sem novo login |
| **Resultado Real** | Após clicar em "Sair", o usuário retorna à página de login, mas usando o botão "voltar" do navegador consegue acessar home.html novamente |
| **Severidade** | **Critical** - Risco de segurança na desconexão de usuário |
| **Prioridade** | **High** - Deve ser corrigido antes do lançamento |
| **Evidência/Anexos** | Evidence: Possível acessar home.html novamente através de navegação de browser history |
| **Relatado por** | Gerenciador de QA |
| **Data do Relato** | 26/11/2025 |

---

## RESUMO DE BUGS

| ID | Título | Severidade | Prioridade | Status |
|----|---------| -----------| -----------| -------|
| BUG-001 | Login: Sem validação de e-mail | Medium | Medium | Aberto |
| BUG-002 | Login: Espaços em branco aceitos | Major | High | Aberto |
| BUG-003 | Reset: Sem validação de e-mail | Major | High | Aberto |
| BUG-004 | Criar Conta: Senhas fracas aceitas | Major | High | Aberto |
| BUG-005 | Home: Logout inadequado | Critical | High | Aberto |
| **TOTAL** | **5 Bugs** | - | - | **5 Abertos** |

---

## CLASSIFICAÇÃO DE SEVERIDADE

- **Critical**: Problema de segurança ou funcionalidade completamente quebrada
- **Major**: Funcionalidade importante comprometida
- **Medium**: Funcionalidade secundária com falha
- **Low**: Pequenos problemas estéticos ou de digitação

## CLASSIFICAÇÃO DE PRIORIDADE

- **High**: Correção crucial antes do lançamento
- **Medium**: Pode ser corrigido após bugs mais sérios
- **Low**: Corrigir se houver tempo, ou adiar para versão futura

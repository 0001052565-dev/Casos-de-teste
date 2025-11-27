# DOCUMENTAÇÃO DE TESTES - SISTEMA DE NAVEGAÇÃO

## CASOS DE TESTE

---

### CT-001: Validação de Login com Campos Completos

| Campo | Valor |
|-------|-------|
| **ID do Caso de Teste** | CT-001 |
| **Funcionalidade/Módulo** | Tela de Login (index.html) |
| **Descrição do Caso** | Verificar se o sistema redireciona para a Home ao preencher todos os campos corretamente |
| **Pré-Condição** | O usuário está na página index.html |
| **Dados de Teste** | E-mail: usuario@teste.com; Senha: 123456 |
| **Etapas de Execução** | 1. Abrir a página index.html; 2. Inserir 'usuario@teste.com' no campo E-mail; 3. Inserir '123456' no campo Senha; 4. Clicar no botão "Entrar" |
| **Resultado Esperado** | O sistema deve carregar a página home.html e exibir "Bem-vindo à Home!" |
| **Resultado Real** | O sistema carregou a página home.html com sucesso |
| **Status** | **PASS** ✓ |
| **Testador** | Gerenciador de QA |
| **Data da Execução** | 26/11/2025 |

---

### CT-002: Validação de Login com Campos Vazios

| Campo | Valor |
|-------|-------|
| **ID do Caso de Teste** | CT-002 |
| **Funcionalidade/Módulo** | Tela de Login (index.html) |
| **Descrição do Caso** | Verificar se o sistema exibe alerta de validação quando os campos estão vazios |
| **Pré-Condição** | O usuário está na página index.html |
| **Dados de Teste** | E-mail: vazio; Senha: vazio |
| **Etapas de Execução** | 1. Abrir a página index.html; 2. Deixar os campos "E-mail" e "Senha" vazios; 3. Clicar no botão "Entrar" |
| **Resultado Esperado** | Exibir um alerta com a mensagem "Preencha todos os campos." e manter na página de login |
| **Resultado Real** | Alerta foi exibido corretamente com a mensagem esperada |
| **Status** | **PASS** ✓ |
| **Testador** | Gerenciador de QA |
| **Data da Execução** | 26/11/2025 |

---

### CT-003: Navegação para Página de Reset de Senha

| Campo | Valor |
|-------|-------|
| **ID do Caso de Teste** | CT-003 |
| **Funcionalidade/Módulo** | Tela de Login (index.html) |
| **Descrição do Caso** | Verificar se o link "Esqueci minha senha" redireciona corretamente para reset.html |
| **Pré-Condição** | O usuário está na página index.html |
| **Dados de Teste** | Não aplicável |
| **Etapas de Execução** | 1. Abrir a página index.html; 2. Clicar no link "Esqueci minha senha" |
| **Resultado Esperado** | O sistema deve carregar a página reset.html com o título "Reset de Senha" |
| **Resultado Real** | A página reset.html foi carregada corretamente |
| **Status** | **PASS** ✓ |
| **Testador** | Gerenciador de QA |
| **Data da Execução** | 26/11/2025 |

---

### CT-004: Navegação para Página de Criar Conta

| Campo | Valor |
|-------|-------|
| **ID do Caso de Teste** | CT-004 |
| **Funcionalidade/Módulo** | Tela de Login (index.html) |
| **Descrição do Caso** | Verificar se o link "Criar Conta" redireciona corretamente para criar_conta.html |
| **Pré-Condição** | O usuário está na página index.html |
| **Dados de Teste** | Não aplicável |
| **Etapas de Execução** | 1. Abrir a página index.html; 2. Clicar no link "Criar Conta" |
| **Resultado Esperado** | O sistema deve carregar a página criar_conta.html com o título "Criar Conta" |
| **Resultado Real** | A página criar_conta.html foi carregada corretamente |
| **Status** | **PASS** ✓ |
| **Testador** | Gerenciador de QA |
| **Data da Execução** | 26/11/2025 |

---

### CT-005: Cadastro com Todos os Campos Preenchidos

| Campo | Valor |
|-------|-------|
| **ID do Caso de Teste** | CT-005 |
| **Funcionalidade/Módulo** | Tela de Criar Conta (criar_conta.html) |
| **Descrição do Caso** | Verificar se o sistema aceita o cadastro com todos os campos preenchidos |
| **Pré-Condição** | O usuário está na página criar_conta.html |
| **Dados de Teste** | Nome: João Silva; E-mail: joao@teste.com; Senha: senha123 |
| **Etapas de Execução** | 1. Abrir a página criar_conta.html; 2. Inserir 'João Silva' no campo Nome; 3. Inserir 'joao@teste.com' no campo E-mail; 4. Inserir 'senha123' no campo Senha; 5. Clicar no botão "Cadastrar" |
| **Resultado Esperado** | Exibir alerta "Conta criada com sucesso!" e redirecionar para index.html |
| **Resultado Real** | Alerta foi exibido e redirecionamento ocorreu corretamente |
| **Status** | **PASS** ✓ |
| **Testador** | Gerenciador de QA |
| **Data da Execução** | 26/11/2025 |

---

## RESUMO DE EXECUÇÃO

| ID | Descrição | Status |
|----|-----------| -------|
| CT-001 | Login com campos completos | PASS |
| CT-002 | Login com campos vazios | PASS |
| CT-003 | Navegação para Reset de Senha | PASS |
| CT-004 | Navegação para Criar Conta | PASS |
| CT-005 | Cadastro com campos preenchidos | PASS |
| **TOTAL** | **5 testes** | **5 PASS** |

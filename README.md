# Luxo - Aluguel de Iates 🛥️

Um sistema web institucional elegante para locação de iates de alto padrão, desenvolvido como projeto acadêmico. O sistema combina uma interface responsiva e imersiva em HTML5/CSS3 com funcionalidades dinâmicas de envio e leitura de mensagens consumindo uma API local através do jQuery.

🔗 **Link do Repositório:** [github.com/guilhermesantt/Projeto-Iates](https://github.com/guilhermesantt/Projeto-Iates)

---

## 🚀 Funcionalidades do Projeto

O projeto foi expandido para além das páginas estáticas institucionais, integrando lógica de negócios e persistência de dados simulada por meio de três implementações principais:

1. **Captação de Clientes (Contato):** * Formulário interativo na página de contato que captura o `Nome`, `E-mail` e `Mensagem`.
   * Envio assíncrono dos dados encapsulados em um objeto JavaScript utilizando a função global `inserirMensagem(mensagem)`.

2. **Autenticação Restrita (Painel Admin):**
   * Tela de login (`admin.html`) para usuários autorizados.
   * Validação de credenciais via objeto de login estruturado enviado para a função `validarUsuario(objLoginSenha)`.
   * Redirecionamento automático em caso de sucesso ou exibição de alerta de erro para dados inválidos.
   * **Credenciais de Teste:** * *E-mail:* `admin@admin.com`
     * *Senha:* `1234`

3. **Painel de Leitura Dinâmico (Mensagens):**
   * Ambiente restrito (`mensagens.html`) que consome o histórico de contatos através de `obterMensagens()`.
   * Construção dinâmica de tabelas em tempo de execução manipulando o DOM com loops jQuery (`$.each`), garantindo que novas mensagens apareçam instantaneamente sem necessidade de recarregar estruturas estáticas.

---

## 📂 Estrutura de Arquivos

```text
├── css/
│   └── default.css          # Centralização de toda a identidade visual e tabelas
├── images/                  # Identidade visual (iates, destinos e ícones)
├── js/
│   ├── jquery-3.6.4.min.js  # Biblioteca para manipulação simplificada do DOM
│   └── api.js               # Script fornecido com os métodos de persistência/validação
├── index.html               # Vitrine e página inicial do projeto
├── aluguel.html             # Catálogo dos tipos de iates disponíveis
├── destinos.html            # Guia visual com as rotas de navegação
├── admin.html               # Formulário de autenticação do administrador
└── mensagens.html           # Tabela de leitura das mensagens recebidas

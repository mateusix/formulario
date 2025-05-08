# 📧 Formulário de Envio de Email com EmailJS

Este projeto consiste em um formulário simples de contato em HTML, CSS e JavaScript, com suporte ao modo escuro, que envia e-mails automaticamente utilizando a API gratuita do [EmailJS](https://www.emailjs.com/).

https://github.com/user-attachments/assets/e182cc0d-5609-4532-ba08-5ab255a4f380

---

## 🚀 Funcionalidades

- Envio de mensagens via e-mail direto do navegador.
- Modo escuro (dark mode).
- Validação e formatação automática de telefone.
- Mensagens de sucesso e erro com sistema de notificações (toasts).
- Compatível com dispositivos móveis (responsivo).

---

## 🛠️ Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript (Vanilla)
- [EmailJS](https://www.emailjs.com/)
- Ícones: BoxIcons e FontAwesome

---
## ✉️ Configuração do EmailJS

Para que o envio funcione corretamente, é necessário configurar sua conta no EmailJS:

### 1. Crie uma conta

Acesse [https://www.emailjs.com/](https://www.emailjs.com/) e crie uma conta gratuita.

### 2. Configure um serviço de e-mail

Após o login:

- Vá em **Email Services** no painel.
- Clique em **Add new service**.
- Escolha o provedor (por exemplo: Gmail, Outlook, etc) e conecte sua conta.

📌 **Anote o `Service ID`.**

### 3. Crie um Template

- Vá em **Email Templates** > **Create new template**
- Adicione os campos que o formulário irá enviar:
  - `fullName`
  - `email`
  - `phoneNumber`
  - `subject`
  - `message`

📌 **Anote o `Template ID`.**

### 4. Integre com JavaScript

- Vá em **Account** > **API Keys** e copie sua **Public Key (User ID)**.

No seu script, preencha os valores de acordo com seu painel do EmailJS:

```javascript
var payload = {
    service_id: "SEU_SERVICE_ID",
    template_id: "SEU_TEMPLATE_ID",
    user_id: "SUA_USER_ID",
    template_params: {
        fullName: fullName,
        email: email,
        phoneNumber: phoneNumber,
        subject: subject,
        message: message
    }
};

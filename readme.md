# Gerador de Senhas

Este projeto é uma aplicação web interativa para gerar senhas seguras com base em critérios personalizados definidos pelo usuário, agora garantindo a criação de senhas **sem repetição de caracteres**.

## 🚀 Funcionalidades

- **Geração Sem Repetição:** Garante que a senha gerada contenha apenas caracteres únicos (sem duplicadas).
- **Personalização da Quantidade:** Define o comprimento da senha (entre 4 e 50 caracteres).
- **Seleção de Caracteres:** Permite incluir ou excluir:
  - Números (`0-9`)
  - Caracteres especiais (`!@#$%^&*`)
  - Letras maiúsculas (`A-Z`)
  - Letras minúsculas (`a-z`)
- **Validação Inteligente:** Alerta o usuário caso a quantidade de caracteres solicitada exceda o total de caracteres únicos disponíveis nos tipos selecionados.
- **Copiar para a Área de Transferência:** A senha é copiada automaticamente ao ser gerada. O botão integrado também permite copiá-la novamente, com suporte a navegadores modernos e fallback para compatibilidade em dispositivos mais antigos.
- **Atalho de Teclado:** Pressionar `Enter` aciona o gerador de senhas.
- **Design Responsivo:** Layout intuitivo e adaptável para telas de desktops e dispositivos móveis.

## 🛠️ Tecnologias Utilizadas

- **HTML5:** Estruturação semântica da interface.
- **CSS3:** Estilização moderna utilizando Flexbox, Grid, gradientes e animações de transição.
- **JavaScript (ES6+):** Lógica da aplicação, manipulação do DOM e algoritmo de embaralhamento *Fisher-Yates* para garantia de aleatoriedade e não repetição.

## 💻 Como Usar

1. Abra o arquivo `index.html` em qualquer navegador web.
2. Defina a quantidade de caracteres desejada para a senha.
3. Marque os tipos de caracteres que prefere utilizar.
4. Clique no botão **Gerar Senha** (ou pressione **Enter**).
5. A senha é copiada automaticamente; se precisar, clique no botão **Copiar** para copiá-la novamente.

---

## 👨‍💻 Desenvolvedor

**Fabio Castro**
# Super Alfa - Sistema de Click & Collect
Este repositório contém o frontend do sistema **Click & Collect** (Retirada em Loja) da **Super Alfa**, uma superloja fictícia criada para a disciplina de Fundamentos de Engenharia de Software.

O sistema Click & Collect foi projetado para oferecer uma experiência de compra ágil, prática e moderna. O sistema permite que clientes comprem online e retirem seus pedidos na loja física escolhida em até 1 hora.

O código aqui presente é apenas a versão exportada pelo Vite. Para o projeto completo, acesse o link: [Super Alfa](https://github.com/mauricioermel/super-alfa)

O projeto foi desenvolvido utilizando:
- **Vite** como Servidor de desenvolvimento, com o comando `npm run dev` rodando é possível visualizar em tempo real as mudanças no frontend. O Vite também serviu de Compilador de Vue.js e TailwindCSS, além é claro do seu papel como Bundler, empacotando o projeto para produção com o comando `npm run build`.
- **Vue.js 3** foi utilizado visando criar componentes rápidos, pois queria que a página da loja fosse *SPA* (Single Page Application). Atrelado a escolha do Vue vem o gerenciador de estado *Pinia* que permitiu mockar o sistema de login, carrinho de compras, estoque, pedidos e todos os outros sistemas que deveriam ser demonstrados, sem a necessidade de um backend real.
- **Tailwind CSS v4** permitiu uma criação ágil dos elementos da página e, por conta do seu viés mobile first, facilitou a portabilidade do sistema para mobile.
- **daisyUI v5** foi escolhido como a biblioteca de componentes neste projeto por conta da sua integração com o tailwind e o VueJS, além claro de permitir a personalização dos seus componentes que já são bem feitos.

---

## Roteiro de Testes
Utilize o checklist abaixo para testar as principais jornadas do sistema, utilizando as credenciais de demonstração fornecidas.
### 1. Fluxo do Cliente
1. **Navegação**: Navegue pela página inicial e clique em uma categoria (ex: *Eletrônicos*, *Mercearia*).
2. **Carrinho**: Adicione um ou mais produtos ao carrinho (não é necessário estar logado).
3. **Login para Continuar**: Abra o carrinho e clique no botão **"Entrar para Continuar"**. Você será redirecionado para a página de login.
4. **Autenticação**: Faça login com as credenciais de demonstração:
   - **E-mail**: `maria@email.com`
   - **Senha**: `123456`
5. **Finalização**: Selecione uma loja (clicando em **"Selecionar Loja"** ou **"Trocar Loja"** no carrinho), clique em **"Finalizar Compra"** e, na tela seguinte, confirme o pedido clicando em **"Confirmar Pedido"**.
6. **Código de Retirada**: Após a confirmação, o sistema exibirá seu **código de retirada de 8 dígitos**. Copie este código para utilizá-lo no fluxo do funcionário.
7. **Cancelamento**: Vá para a tela **Meus Pedidos** (através do menu ou barra de navegação), abra os detalhes do pedido recém-criado e experimente a funcionalidade de clicar em **"Cancelar Pedido"** (antes que o funcionário inicie a separação).
### 2. Fluxo do Funcionário
1. **Portal**: Na página de login do cliente, clique no botão **"Portal do Funcionário"** na parte inferior.
2. **Autenticação**: Faça login com as credenciais:
   - **E-mail**: `employee@superalfa.com`
   - **Senha**: `emp123`
3. **Separação**: No menu lateral, acesse **Pedidos Pendentes** e clique em **"Iniciar Separação"** no pedido desejado.
4. **Prontidão**: Acesse a aba **Em Separação** e clique no botão **"Marcar como Pronto"** para disponibilizar o pedido para retirada.
5. **Validação**: Vá até a aba **Validar Código**, insira o código de retirada de 8 dígitos gerado no fluxo do cliente e clique em **"Validar"**. Após validar as informações do pedido, clique em **"Confirmar Retirada"** para concluir a entrega.
### 3. Fluxo do Administrador
1. **Portal**: Na página de login do cliente, clique no botão **"Portal Admin"** na parte inferior.
2. **Autenticação**: Faça login com as credenciais:
   - **E-mail**: `admin@superalfa.com`
   - **Senha**: `admin123`
3. **Produtos**: Navegue até a aba **Produtos** para testar as ações de adicionar, editar ou remover produtos do catálogo.
4. **Estoque**: Navegue até a aba **Gestão de Estoque** para simular o ajuste de quantidade em estoque dos itens por loja.

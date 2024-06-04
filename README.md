# party-scheduler

## Introdução
* Sistema para gerar eventos como: aniversários, churrascos, baladas, etc ...

### Casos de Uso

#### 1. Cadastro de Usuário
**Descrição:** Permitir que novos usuários se registrem no sistema.
- **Ator Principal:** Usuário
- **Pré-condição:** Nenhuma
- **Fluxo Principal:**
  1. O usuário acessa a página de registro.
  2. O usuário insere os dados necessários (nome, email, senha, etc.).
  3. O sistema valida as informações e cria uma nova conta.
  4. O sistema envia um email de confirmação para o usuário.
  5. O usuário confirma o email.
- **Pós-condição:** O usuário está registrado e pode acessar o sistema.

#### 2. Login
**Descrição:** Permitir que usuários registrados façam login no sistema.
- **Ator Principal:** Usuário
- **Pré-condição:** O usuário deve estar registrado.
- **Fluxo Principal:**
  1. O usuário acessa a página de login.
  2. O usuário insere suas credenciais (email e senha).
  3. O sistema valida as credenciais.
  4. O sistema concede acesso ao usuário.
- **Pós-condição:** O usuário está logado no sistema.

#### 3. Criação de Evento
**Descrição:** Permitir que os usuários criem novos eventos.
- **Ator Principal:** Usuário
- **Pré-condição:** O usuário deve estar logado.
- **Fluxo Principal:**
  1. O usuário acessa a página de criação de evento.
  2. O usuário insere os detalhes do evento (nome, data, hora, local, descrição, etc.).
  3. O usuário envia o formulário.
  4. O sistema valida as informações e cria o evento.
  5. O sistema confirma a criação do evento.
- **Pós-condição:** O evento é criado e listado no perfil do usuário.

##### Cenários Personalizados para Cadastro de Eventos

###### 3.1. Aniversário
**Campos Específicos:**
- **Bolo:** Tipo de bolo, tamanho, sabor, decoração.
- **Decoração:** Tema, cores, itens de decoração específicos (balões, faixas, etc.).
- **Presentes:** Lista de presentes desejados, sugestões de presentes.
- **Atividades:** Jogos, brincadeiras, animação (palhaços, mágicos, etc.).
- **Comidas e Bebidas:** Cardápio de comidas, bebidas, opções para convidados com restrições alimentares.
- **Convites:** Design e envio de convites personalizados.
- **Fotógrafo:** Disponibilidade de fotógrafo ou serviço de fotografia.

**Exemplo de Fluxo de Cadastro:**
1. O organizador seleciona "Aniversário" como o tipo de evento.
2. O sistema apresenta campos específicos para detalhes do bolo, decoração, lista de presentes, etc.
3. O organizador preenche os campos relevantes.
4. O sistema salva o evento com todas as especificações.

###### 3.2. Churrasco
**Campos Específicos:**
- **Carne:** Tipos de carne (picanha, costela, frango, etc.), quantidade.
- **Acompanhamentos:** Saladas, pães, molhos, acompanhamentos típicos.
- **Bebidas:** Tipos de bebidas (cerveja, refrigerante, suco, etc.), quantidade.
- **Equipamentos:** Grelhas, espetos, carvão, gelo, mesas e cadeiras.
- **Entretenimento:** Música (playlist, banda ao vivo, DJ), jogos (futebol, vôlei, etc.).
- **Local:** Área externa, churrasqueira disponível, piscina.
- **Convidados:** Lista de convidados, confirmação de presença, restrições alimentares.

**Exemplo de Fluxo de Cadastro:**
1. O organizador seleciona "Churrasco" como o tipo de evento.
2. O sistema apresenta campos específicos para tipos de carne, acompanhamentos, bebidas, etc.
3. O organizador preenche os campos relevantes.
4. O sistema salva o evento com todas as especificações.

###### 3.3. Balada
**Campos Específicos:**
- **Música:** Banda, DJ, tipo de música, equipamento de som e luz.
- **Ingressos:** Venda de ingressos, controle de entrada, listas VIP.
- **Bebidas:** Tipos de bebidas, quantidade, bar, bartender.
- **Decoração:** Tema, iluminação, efeitos especiais (fogos, fumaça, etc.).
- **Segurança:** Equipe de segurança, controle de acesso.
- **Local:** Local da balada, capacidade, disposição dos espaços (pista de dança, áreas VIP).
- **Convidados:** Lista de convidados, confirmação de presença, restrições alimentares.

**Exemplo de Fluxo de Cadastro:**
1. O organizador seleciona "Balada" como o tipo de evento.
2. O sistema apresenta campos específicos para música, ingressos, bebidas, segurança, etc.
3. O organizador preenche os campos relevantes.
4. O sistema salva o evento com todas as especificações.

##### Considerações Adicionais
- **Personalização:** Permitir que os organizadores adicionem campos personalizados caso precisem de algo específico que não esteja no cenário padrão.
- **Templates:** Oferecer templates predefinidos que os organizadores podem usar como base e modificar conforme necessário.
- **Sugestões Automáticas:** Com base no tipo de evento, o sistema pode sugerir itens comuns que geralmente são esquecidos, como guardanapos, talheres, copos descartáveis, etc.

#### 4. Convite de Participantes
**Descrição:** Permitir que os organizadores de eventos convidem participantes.
- **Ator Principal:** Usuário (Organizador)
- **Pré-condição:** O evento deve estar criado.
- **Fluxo Principal:**
  1. O organizador acessa a página do evento.
  2. O organizador seleciona a opção de convidar participantes.
  3. O organizador insere os emails dos participantes a serem convidados.
  4. O sistema envia convites para os participantes.
- **Pós-condição:** Os participantes recebem um convite por email para o evento.

#### 5. Confirmação de Presença
**Descrição:** Permitir que os convidados confirmem sua presença no evento.
- **Ator Principal:** Usuário (Convidado)
- **Pré-condição:** O usuário deve ter recebido um convite para o evento.
- **Fluxo Principal:**
  1. O convidado recebe o convite por email.
  2. O convidado acessa o link de confirmação no email.
  3. O convidado confirma sua presença.
  4. O sistema atualiza a lista de participantes do evento.
- **Pós-condição:** A presença do convidado é confirmada para o evento.

#### 6. Gerenciamento de Eventos
**Descrição:** Permitir que os organizadores editem ou cancelem eventos existentes.
- **Ator Principal:** Usuário (Organizador)
- **Pré-condição:** O evento deve estar criado pelo organizador.
- **Fluxo Principal:**
  1. O organizador acessa a página do evento.
  2. O organizador seleciona a opção de editar ou cancelar o evento.
  3. O organizador faz as alterações necessárias ou confirma o cancelamento.
  4. O sistema atualiza as informações do evento ou o remove da lista de eventos.
- **Pós-condição:** As alterações são refletidas no sistema, ou o evento é removido.

#### 7. Visualização de Eventos
**Descrição:** Permitir que os usuários visualizem os detalhes dos eventos aos quais foram convidados.
- **Ator Principal:** Usuário (Convidado)
- **Pré-condição:** O usuário deve estar logado e ter sido convidado para um evento.
- **Fluxo Principal:**
  1. O usuário acessa a página de eventos.
  2. O usuário seleciona um evento para visualizar.
  3. O sistema exibe os detalhes do evento.
- **Pós-condição:** O usuário visualiza as informações detalhadas do evento.

### Considerações Adicionais
Além dos casos de uso, considere implementar:
- **Sistema de Notificações:** Notificações via email ou SMS para lembretes e atualizações de eventos.
- **Feedback dos Participantes:** Permitir que os participantes deixem comentários ou avaliações após o evento.
- **Integração com Redes Sociais:** Facilitar o compartilhamento de eventos em plataformas sociais.
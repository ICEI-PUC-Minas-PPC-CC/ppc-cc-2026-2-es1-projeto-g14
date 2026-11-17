# PRODUCT BACKLOG

## 1. Product Backlog Itens

> O objetivo desta tarefa é elaborar a versão preliminar do backlog do produto, contendo dez funcionalidades que atendam às necessidades do usuário. Utilize os modelos de tabela a seguir.

| #   | Persona (Quem) | Dor/Necessidade (Por Quê) | Expectativa (Para Quê) | Funcionalidade (O Quê - Ação) |
| --- | -------------- | ------------------------- | ---------------------- | ----------------------------- |
| F1  | Roberto Mendes (Profissional) | Falta de credibilidade e concorrência desleal com prestadores sem qualificação | Comprovar habilitação técnica e passar segurança aos clientes | Realizar cadastro profissional com envio e validação documental de identidade e registro (KYC) |
| F2  | Ana Lima (Cliente) | Dificuldade em descrever o problema e encontrar profissionais especializados | Publicar a necessidade detalhada com fotos/vídeos e receber atendimento direcionado | Criar e publicar pedido de serviço residencial por categoria, endereço e mídia descritiva |
| F3  | Roberto Mendes (Profissional) | Gastar tempo e dinheiro para enviar orçamentos que nunca são fechados | Ter acesso a demandas reais com limite justo de concorrência | Enviar propostas de orçamento gratuitas para pedidos abertos (limitado a até 3 prestadores por demanda) |
| F4  | Ana Lima (Cliente) | Preços abusivos, falta de transparência e cobrança indevida por visitas | Comparar condições de preço, prazo e reputação antes de fechar | Comparar e aceitar proposta de orçamento recebida de forma simples e transparente |
| F5  | Ana Lima e Roberto Mendes | Risco de calote do cliente e receio de pagamento antecipado sem entrega do serviço | Garantir que o valor está seguro e reservado até a conclusão do trabalho | Reter valor do serviço em custódia financeira protegida no momento do aceite |
| F6  | Ana Lima e Roberto Mendes | Falta de canal formal e seguro para alinhar detalhes de execução | Conversar sem expor dados pessoais antes do aceite final | Comunicar-se via chat em tempo real vinculado especificamente à ordem de serviço |
| F7  | Ana Lima e Roberto Mendes | Falta de comprovação do estado inicial e do resultado do trabalho | Evitar discussões sobre danos prévios ou serviços incompletos | Registrar e anexar evidências fotográficas do reparo ("Antes" e "Depois") na plataforma |
| F8  | Ana Lima e Roberto Mendes | Insegurança sobre o momento exato de pagar ou de receber pelo trabalho realizado | Confirmar a entrega presencial com consenso de ambas as partes | Liberar o pagamento em custódia ao profissional mediante validação de código PIN presencial |
| F9  | Ana Lima e Roberto Mendes | Avaliações falsas, vingativas ou manipuladas na internet | Ter uma reputação justa, auditada e bidirecional na plataforma | Avaliar mutuamente a experiência de atendimento por notas e comentários em sistema cego |
| F10 | Ana Lima e Roberto Mendes | Desamparo em caso de desacordo comercial, avaria ou desistência | Obter resolução justa com apoio de suporte e análise de evidências | Abrir chamado de suporte e mediação de disputa com bloqueio temporário da custódia |

## 2. Revisão Técnica, UX e Negócios

> Avalie as funcionalidades listadas na tabela anterior com base em quatro perspectivas: Valor para o Negócio, Esforço Técnico de Implementação, Experiência do Usuário (UX) e Nível de Confiança (O quê / Como).

**Métricas:**

- **Valor de Negócio:** `$` (Baixo) a `$$$` (Alto)
- **Esforço Técnico:** `E` (Baixo) a `EEE` (Alto)
- **Valor UX:** ❤️ (Baixo) a ❤️❤️❤️ (Alto)
- **Confiança:** 🟢 (Alto), 🟡 (Médio), 🔴 (Baixo)

| #       | Esforço Técnico | Valor UX | Valor de Negócio | Nível de Confiança (O que/Como) |
| :------ | :-------------- | :------- | :--------------- | :------------------------------ |
| **F1**  | EE              | ❤️❤️     | $$$              | 🟢 Alto/Alto                    |
| **F2**  | E               | ❤️❤️❤️   | $$$              | 🟢 Alto/Alto                    |
| **F3**  | EE              | ❤️❤️❤️   | $$$              | 🟢 Alto/Médio                   |
| **F4**  | E               | ❤️❤️❤️   | $$$              | 🟢 Alto/Alto                    |
| **F5**  | EE              | ❤️❤️     | $$$              | 🟡 Médio/Médio                  |
| **F6**  | EE              | ❤️❤️❤️   | $$               | 🟢 Alto/Médio                   |
| **F7**  | E               | ❤️❤️     | $$               | 🟢 Alto/Alto                    |
| **F8**  | E               | ❤️❤️❤️   | $$$              | 🟢 Alto/Alto                    |
| **F9**  | E               | ❤️❤️     | $$               | 🟢 Alto/Alto                    |
| **F10** | EE              | ❤️       | $$               | 🟡 Médio/Médio                  |

### Justificativas

> Justifique a análise da tabela acima para cada funcionalidade, explicando a racionalidade por trás das métricas atribuídas.

- **F1 (Cadastro e KYC Profissional):** É o alicerce de confiança da proposta de valor do negócio ($$$). O esforço técnico (EE) envolve upload seguro em bucket privado, validação de dados e gestão de status do prestador. UX importante (❤️❤️) com fluxo guiado e confiança 🟢 alta por ser domínio mapeado.
- **F2 (Criação de Pedidos):** Entrada principal do fluxo para clientes ($$$). UX prioritária (❤️❤️❤️) para cadastro intuitivo e ágil com foto e endereço. Esforço enxuto (E) utilizando persistência padrão em banco e confiança 🟢 alta.
- **F3 (Envio de Orçamentos Gratuitos):** Diferencial central de negócio ($$$) que atrai prestadores sem cobrar taxas de anúncio e encanta clientes (❤️❤️❤️) com até 3 propostas. Esforço moderado (EE) devido à trava de concorrência atômica no banco; confiança 🟢 alta/média.
- **F4 (Aceite de Orçamento):** Momento decisivo de conversão do marketplace ($$$) com interface clara e objetiva para decisão do cliente (❤️❤️❤️). Esforço baixo (E) e confiança 🟢 alta.
- **F5 (Custódia do Pagamento):** Garante a monetização (comissão de 12–15%) e elimina calotes ($$$). Esforço intermediário (EE) exigindo controle rigoroso de concorrência, reserva de saldo e idempotência contábil; confiança 🟡 média/média pelo impacto financeiro.
- **F6 (Chat Interno):** Facilita o alinhamento de escopo e horários com excelente retorno em UX (❤️❤️❤️) e retenção ($$). Esforço técnico moderado (EE) utilizando canal de mensagens em tempo real (Supabase Realtime) e confiança 🟢 alta/média.
- **F7 (Evidências Fotográficas):** Proteção comprobatória do serviço com baixo esforço técnico (E) de upload e associação à OS, alto valor de conformidade ($$) e boa experiência (❤️❤️) de transparência; confiança 🟢 alta.
- **F8 (Liberação por PIN Presencial):** Ponto culminante do serviço onde o cliente autoriza a liquidação do valor ao profissional ($$$). UX extremamente satisfatória e transparente (❤️❤️❤️) com esforço baixo (E) via verificação de hash/código de 4 dígitos e confiança 🟢 alta.
- **F9 (Avaliação Mútua Bidirecional):** Alimenta o ciclo virtuoso de reputação da plataforma ($$). Esforço reduzido (E) de formulário com notas e comentários exibidos após submissão de ambas as partes (sistema cego), ótima UX (❤️❤️) e confiança 🟢 alta.
- **F10 (Mediação de Disputas):** Mecanismo de salvaguarda jurídica e contenção de atritos ($$). Esforço moderado (EE) por requerer máquina de estados com congelamento de custódia e abertura de chamado; UX pontual para exceções (❤️) e confiança 🟡 média/média.

## 3. Product Backlog Itens (priorizado)

> Liste os itens do backlog do produto, priorizados conforme as regras do sequenciador vistas em aula. Ordene-os da maior para a menor prioridade dentro de cada onda.

**Regras do Sequenciador:**

- **Regra 1:** Uma onda pode conter, no máximo, três funcionalidade.
- **Regra 2:** Uma onda não pode conter mais de uma funcionalidade em vermelho.
- **Regra 3:** Uma onda não pode conter três funcionalidades em amarelo e vermelho.
- **Regra 4:** A soma de esforço dos cartões não pode ultrapassar cinco Es.
- **Regra 5:** A soma de valor dos cartões de uma onda não pode ser menos de quatro $s e quatro corações.
- **Regra 6:** Se um cartão depende de outro cartão, esse outro deve estar em alguma onda anterior.

| #       | Esforço<br>Técnico | Valor<br>UX | Valor de<br>Negócio | Nível de Confiança <br> (O que/Como) | Onda |
| :------ | :----------------- | :---------- | :------------------ | :----------------------------------- | :--: |
| **F2**  | E                  | ❤️❤️❤️      | $$$                 | 🟢 Alto/Alto                         |  1   |
| **F1**  | EE                 | ❤️❤️        | $$$                 | 🟢 Alto/Alto                         |  1   |
| **F4**  | E                  | ❤️❤️❤️      | $$$                 | 🟢 Alto/Alto                         |  2   |
| **F3**  | EE                 | ❤️❤️❤️      | $$$                 | 🟢 Alto/Médio                        |  2   |
| **F5**  | EE                 | ❤️❤️        | $$$                 | 🟡 Médio/Médio                       |  2   |
| **F8**  | E                  | ❤️❤️❤️      | $$$                 | 🟢 Alto/Alto                         |  3   |
| **F6**  | EE                 | ❤️❤️❤️      | $$                  | 🟢 Alto/Médio                        |  3   |
| **F7**  | E                  | ❤️❤️        | $$                  | 🟢 Alto/Alto                         |  3   |
| **F9**  | E                  | ❤️❤️        | $$                  | 🟢 Alto/Alto                         |  4   |
| **F10** | EE                 | ❤️          | $$                  | 🟡 Médio/Médio                       |  4   |

> **Verificação das Regras do Sequenciador:**
> - **Onda 1 (Fundação e Entrada):** 2 funcionalidades (<= 3), 0 vermelhos, Esforço = 3 Es (<= 5 Es), Valor = 6 $s e 5 ❤️s (>= 4 $s e 4 ❤️s). Não possui dependências prévias.
> - **Onda 2 (Cotação e Contratação):** 3 funcionalidades (<= 3), 0 vermelhos, 1 amarelo (F5), Esforço = 5 Es (<= 5 Es), Valor = 9 $s e 8 ❤️s (>= 4 $s e 4 ❤️s). F3, F4 e F5 dependem do cadastro e pedido criados na Onda 1.
> - **Onda 3 (Comunicação e Conclusão Presencial):** 3 funcionalidades (<= 3), 0 vermelhos, 0 amarelos, Esforço = 4 Es (<= 5 Es), Valor = 7 $s e 8 ❤️s (>= 4 $s e 4 ❤️s). F6, F7 e F8 dependem do serviço contratado na Onda 2.
> - **Onda 4 (Reputação e Pós-Serviço):** 2 funcionalidades (<= 3), 0 vermelhos, 1 amarelo (F10), Esforço = 3 Es (<= 5 Es), Valor = 4 $s e 4 ❤️s (>= 4 $s e 4 ❤️s). F9 e F10 dependem da conclusão ou intercorrência de ordens das ondas anteriores.

## 4. Especificação Suplementar de Requisitos Não Funcionais

> Especifique os requisitos não funcionais do produto de software, certificando-se de que atendam aos critérios SMART.

| Requisito não-funcional | Descrição | Categoria | Prioridade |
| :---------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------- | :--------- |
| RNF.1 | O tempo médio de resposta para carregamento das listas de pedidos e consultas de orçamentos não deverá exceder 2 segundos em conexões 4G/Wi-Fi estáveis. | Desempenho | Alta |
| RNF.2 | Todos os dados sensíveis dos usuários (dados bancários, documentos e senhas) devem ser transmitidos via protocolo seguro TLS 1.3 e armazenados com criptografia em repouso (AES-256). | Segurança | Alta |
| RNF.3 | A aplicação móvel deverá ser plenamente funcional e compatível com as versões do sistema operacional Android 8.0 (API level 26) ou superior e iOS 14.0 ou superior. | Suportabilidade | Alta |
| RNF.4 | As operações financeiras de reserva, retenção em custódia e liberação de saldo devem garantir consistência transacional atômica (propriedades ACID), impedindo duplicidades e saldo negativo. | Confiabilidade | Alta |
| RNF.5 | O endereço exato de residência do cliente e o código PIN de confirmação não poderão ser expostos publicamente, ficando visíveis apenas para as partes vinculadas à ordem aceita (LGPD). | Privacidade | Alta |

---

[⬅ Anterior](01_visao_do_produto.md) | [Próximo ➡](99_video_etapa_1.md)

# SaaS B2B — Visão do Produto e Roadmap

## Proposta do produto

Plataforma de gestão financeira e tributária simplificada para pequenos negócios, com foco inicial em **MEI e empresas do Simples Nacional**.

**Proposta de valor:** “Controle financeiro e impostos sem susto, em um só lugar.”

O produto deve ajudar o empreendedor a entender a saúde financeira do negócio, organizar receitas e despesas, acompanhar obrigações e tomar decisões com dados claros. A experiência é self-service: o próprio empreendedor configura e utiliza a plataforma, sem portal, fluxo ou área dedicada a contador.

## Público inicial

- MEIs que precisam organizar entradas, saídas e compromissos financeiros.
- Pequenas empresas optantes pelo Simples Nacional que precisam de visão consolidada do caixa e dos impostos.
- Empreendedores sem equipe financeira dedicada.

A expansão para Lucro Presumido pode ser considerada após validar o produto com o público inicial.

## Princípios de experiência

- Onboarding curto, com possibilidade de pular dados não essenciais e experimentar o simulador antes de concluir a configuração.
- Importação de extratos e configuração guiada, com categorias sugeridas.
- Linguagem simples e consistente: usar **“contagem regressiva”** para prazos e vencimentos; reservar “imposto” para obrigações tributárias.
- Separação clara entre finanças pessoais (PF) e empresariais (PJ), com tratamento explícito de transferências entre contas próprias.
- Interface responsiva, com experiência mobile/PWA de qualidade.
- Transparência sobre cálculos, fontes de dados, permissões e uso das informações.

## Módulos do produto

### 1. Dashboard e inteligência financeira

- Resumo de saldo, receitas, despesas e resultado do período.
- Comparativo com período anterior.
- Previsão de fluxo de caixa.
- Visão de contas a pagar e a receber.
- Metas financeiras, orçamento e alertas proativos.
- Indicadores e avisos configuráveis pelo usuário.
- Separação PF/PJ e identificação de transferências entre contas.

### 2. Transações e contas

- Cadastro manual de receitas e despesas.
- Importação de extratos por CSV e OFX.
- Integração bancária via Open Finance, sujeita à disponibilidade e contratação de provedor.
- Categorização automática inicial por regras e palavras-chave, com evolução para sugestões baseadas em IA.
- Regras personalizadas de categorização.
- Anexos de comprovantes, recibos e documentos.
- Transações recorrentes, parcelamentos, tags, centros de custo e rateios.
- Gestão de cartões de crédito, faturas e distinção entre regime de caixa e competência.
- Conciliação entre transações importadas e lançamentos registrados.
- OCR de recibos e notas como melhoria futura para uso mobile.

### 3. Gestão tributária

- Visão de tributos e obrigações relevantes para MEI e Simples Nacional.
- Simulador de tributos com premissas e limitações explicadas.
- Lembretes de vencimentos e acompanhamento de status.
- Simulador comparativo de regime tributário como evolução, sem substituir orientação profissional.
- Planejamento tributário avançado em etapa posterior.

### 4. Relatórios

- Relatórios financeiros por período, categoria e conta.
- Exportação em PDF e CSV.
- DRE com indicação explícita do critério utilizado (caixa ou competência).
- Pacote de exportação de dados para o próprio usuário.
- Links compartilháveis com controles de acesso e prazo de validade, quando aplicável.

### 5. Configurações e integrações

- Gestão de contas, categorias, tags e regras.
- Integrações planejadas com bancos, Pix, boletos, maquininhas, e-commerce e ERPs.
- Emissão de NFS-e/NF-e como módulo futuro, condicionada à viabilidade técnica, fiscal e às integrações disponíveis.
- API pública e webhooks em fase posterior.
- Exportação e exclusão da conta e dos dados conforme requisitos aplicáveis de privacidade.

### 6. Segurança, privacidade e qualidade

- Controle de acesso e isolamento dos dados por usuário/empresa (incluindo RLS quando aplicável).
- Autenticação de dois fatores (2FA).
- Criptografia de dados sensíveis em repouso e em trânsito.
- Rate limiting, validação de entradas e proteção contra abuso.
- Logs de auditoria e acesso.
- Política de retenção, transparência sobre subprocessadores e documentação de privacidade compatível com a LGPD.
- Backups, monitoramento, observabilidade e alertas operacionais.
- Testes unitários, de integração e ponta a ponta (Playwright).
- Procedimentos documentados de recuperação e resposta a incidentes.

## Escopo explicitamente fora do produto

O produto **não terá funcionalidades específicas para contadores ou escritórios contábeis**. Portanto, não fazem parte do escopo:

- Portal do contador, painel multiempresa para contadores ou programa de parceiros contábeis.
- Convites, permissões, comentários, solicitações ou checklists destinados a contadores.
- Envio automático de relatórios a contadores.
- Integrações contábeis específicas cujo objetivo seja alimentar sistemas de escritórios.
- Planos, marketplace ou white label voltados a escritórios contábeis.

O usuário principal e responsável pelo fluxo é o empreendedor/empresa cliente. Recursos multiusuário, caso implementados, serão voltados à equipe interna do próprio negócio, com permissões administrativas apropriadas.

## Onboarding e avaliação

- Permitir que o usuário explore um simulador sem finalizar todo o cadastro.
- Solicitar apenas dados essenciais no início.
- Oferecer importação de extrato como caminho guiado para configurar a plataforma.
- Avaliar trial de 14 dias após a primeira importação ou 30 dias para MEI; a regra final deve ser validada com métricas de ativação e conversão.

## Monetização — hipótese inicial

- Planos orientados ao porte e às necessidades do negócio, começando por MEI e Simples Nacional.
- Possíveis limites por CNPJ, volume de transações ou recursos.
- Add-ons futuros, como Open Finance e emissão de documentos fiscais, conforme custo operacional e demanda.
- Evitar precificação ou posicionamento direcionados a escritórios contábeis.

## Prioridades de desenvolvimento

### Curto prazo — MVP e validação

1. Consolidar onboarding simples e simulador acessível.
2. Implementar contas a pagar e a receber.
3. Fortalecer importação CSV/OFX e conciliação de lançamentos.
4. Evoluir categorização automática com regras e sugestões.
5. Criar previsão básica de fluxo de caixa e comparativos.
6. Implementar 2FA, auditoria, backups e monitoramento essenciais.
7. Adicionar lembretes de vencimento e notificações configuráveis.

### Médio prazo — expansão funcional

1. Integração Open Finance e conciliação bancária automatizada.
2. Orçamento, metas e alertas proativos.
3. Gestão completa de cartões, faturas e parcelamentos.
4. PWA/mobile robusto e OCR de comprovantes.
5. Emissão de NFS-e/NF-e, após validação técnica e fiscal.
6. API e webhooks.
7. Integrações selecionadas com plataformas financeiras e comerciais.

### Longo prazo — inteligência e escala

1. IA para categorização, detecção de padrões e previsão financeira.
2. Simulador e planejamento tributário mais avançados.
3. Integrações adicionais com ERPs e serviços de negócio.
4. Expansão gradual para outros regimes tributários, após validação do segmento inicial.

## Critérios de produto

- Priorizar funcionalidades que reduzam trabalho manual e incerteza financeira do empreendedor.
- Não apresentar estimativas tributárias como aconselhamento fiscal definitivo.
- Não marcar integrações como disponíveis antes de sua implementação e validação.
- Proteger dados financeiros como informação sensível e explicar claramente como são tratados.
- Entregar em etapas pequenas, com testes e validação antes de ampliar o escopo.

## Status

Este documento registra a visão e o roadmap proposto. Os itens listados não significam que as funcionalidades já estejam implementadas.

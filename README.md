# ☕ Holy Café Management & POS (Showcase)
**Sistema Integrado de PDV, Gestão de Produção e RH para Gastronomia**

> ⚠️ **Nota:** Este é um repositório de portfólio (Showcase). O Holy Café é um sistema operacional proprietário utilizado para a gestão real de uma cafeteria/confeitaria. O código-fonte original é privado. Abaixo, detalho a arquitetura de segurança, módulos de produção e integrações de hardware implementadas. Estou disponível para demonstração técnica do código.

---

## 📖 Resumo Executivo
O Holy Café Management é uma aplicação web responsiva (Mobile-First) que atua como o coração operacional de uma cafeteria de alto volume. Inspirado nas diretrizes de interface do iOS, o sistema integra em uma única plataforma: Ponto de Venda (PDV), Gestão de Encomendas, Painel de Produção (KDS), Analytics Gerencial e Gestão de RH.

## 💻 Stack Tecnológico
- **Front-end:** React (Vite + TypeScript), Tailwind CSS.
- **Back-end & Segurança:** Supabase (Auth, PostgreSQL, Row Level Security).
- **Relatórios & Documentos:** html2pdf.js (Geração de PDFs A4 e cupons térmicos).
- **Integrações:** WhatsApp API para notificações e envio de holerites.
- **Hardware:** Suporte nativo para impressão térmica (bobinas de 58mm/80mm).

## 🏗️ Módulos e Engenharia de Software

### 1. Segurança e Hierarquia (RBAC)
- **Controle de Acesso Baseado em Cargos:** Sistema de permissões onde o ambiente administrativo (Faturamento, RH e Acessos) é invisível e inacessível para usuários sem privilégios de `is_admin`.
- **Proteção de Rotas:** Middleware e validações no Supabase que barram tentativas de acesso direto via URL.

### 2. PDV Inteligente e Comanda Rápida
- **Divisão de Conta e Rateio:** Lógica matemática para divisão de conta entre múltiplas pessoas e formas de pagamento, incluindo rateio automático de taxas de entrega.
- **UX Operacional:** Layout otimizado para velocidade no balcão, gerando cupons térmicos formatados via CSS nativo e disparos automáticos de resumos para o WhatsApp do cliente.

### 3. Painel de Produção (KDS)
- **Gestão em Tempo Real:** Dashboard para a cozinha que agrupa pedidos por cronologia, com tags visuais dinâmicas (🔥 HOJE, ⚡ AMANHÃ).
- **Filtragem Inteligente:** Ocultação automática de pedidos concluídos/cancelados para manter o foco na produção ativa.

### 4. Motor de RH e Folha de Pagamento
- **Calculadora de Holerite Digital:** Sistema que processa salário base, horas extras, feriados e descontos, gerando um contracheque formatado.
- **Automação de Envio:** Integração que processa a matemática e envia o extrato de pagamento diretamente para o WhatsApp pessoal do colaborador.

### 5. Analytics Gerencial (Exclusivo Admin)
- **Motor de BI:** Cálculo de faturamento real (expurgando pedidos cancelados) e ranking de produtos mais vendidos.
- **Relatórios Estilo iFood:** Navegação entre meses com sistema de Accordion para rastrear a origem de cada centavo de receita.

---

## 📸 Demonstração do Produto
*

https://github.com/user-attachments/assets/5a1ee30a-c14a-4274-9d3d-dda7d47a5f3e

*

---
**Desenvolvido por:** [Patrick Fiuza Alves](https://github.com/codetrick95)

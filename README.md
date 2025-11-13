# Projeto-Integrador-Transdisciplinar-de-Engenharia-de-Software-II
PIT - Faculdade Cruzeiro do Sul Virtual

# 🧩 Solução do Problema 1

## 💡 Proposta

Diante da situação-problema 1 e da falta de tempo para um desenvolvimento tradicional, sugere-se o uso de uma **plataforma no-code**, como o **Bubble**, para criar rapidamente o módulo solicitado.

Essas plataformas permitem construir **aplicações web funcionais sem necessidade de programação**, utilizando recursos visuais e lógicos que facilitam o desenvolvimento. Assim, a equipe — mesmo sem experiência técnica — pode montar uma interface para **visualizar, editar e validar pedidos dos vendedores antes que se tornem ordens de serviço**.

Além disso, esse tipo de ferramenta oferece **integração com bancos de dados e APIs**, permitindo conectar o módulo ao sistema já existente. Dessa forma, o problema é resolvido de forma **ágil, colaborativa e com baixo custo de implementação**, sem depender da fila de demandas da equipe de TI.

---

## 🛠️ Plano de Desenvolvimento

### **Passo 1 – Definir o escopo mínimo**

**Objetivo:**
- Visualizar pedidos dos vendedores  
- Permitir editar / corrigir antes de virar ordem de serviço  
- Botão para “Confirmar / Transformar em OS”

**Campos obrigatórios:**
- `id_pedido`, `vendedor`, `cliente`, `itens[]`, `quantidade`, `preco_unitario`, `total`, `status`, `observacoes`, `data_pedido`

**Resultado esperado:**
- Lista de pedidos  
- Tela de edição  
- Ação “Enviar para OS”

---

### **Passo 2 – Escolher a ferramenta**

**Ferramenta:** [Bubble](https://bubble.io/)  
Plataforma full-stack no-code que permite **integrações com APIs, bancos de dados externos e fluxos automatizados.**

---

### **Passo 3 – Mapear dados e integração**

1. Listar as tabelas e endpoints existentes que contêm pedidos.  
2. Definir os pontos de integração entre o sistema atual e o Bubble.  

> 🔗 [Link do banco de dados do Bubble](https://bubble.io/page?id=pitengenharia-de-softwar&tab=Data&name=index&type=page&type_id=pedidos)

---

### **Passo 4 – Construção do módulo no Bubble**

- Criar página **“Lista de Pedidos”**: tabela com filtros (vendedor, data, status) + botão **“Editar / Validar”**  
- Criar página **“Edição de Pedido”**: campos editáveis, validações inline e área de logs/alterações  
- Botões:  
  - **“Salvar rascunho”** (não altera OS)  
  - **“Confirmar → Transformar em OS”** (chama endpoint)  
- Registrar log de auditoria (quem alterou, quando, antes/depois)  

> 🔗 [Link do editor do Bubble](https://bubble.io/page?id=pitengenharia-de-softwar&tab=Design&name=index&type=page)

---

### **Passo 5 – Regras de negócio e validações**

- Validar soma de itens = total  
- Validar estoque disponível (se aplicável)  
- Verificar campos obrigatórios e limites de preço/desconto  
- Implementar permissões:  
  - Vendedores/operadores → podem editar  
  - Aprovadores → podem converter em OS

---

### **Passo 6 – Testes rápidos**

**Fluxo principal:**
1. Buscar pedido  
2. Editar  
3. Salvar  
4. Confirmar  
5. Verificar criação da OS no sistema destino  

**Testes complementares:**
- Edição inválida  
- Conflito de edição concorrente  
- Perda de conexão  
- Implementar “Desfazer” ou correção de OS indevida  

---

### **Passo 7 – Documentação e treinamento**

- Criar documento com:  
  - Instruções de acesso  
  - Papéis e permissões  
  - Checklist de validação  
  - Passo a passo para transformar em OS  
- Treinamento rápido (30–60 min) para usuários responsáveis  

> 🔗 [Link da pasta do Git](https://github.com/Larissa-Anielly/Projeto-Integrador-Transdisciplinar-de-Engenharia-de-Software-II)

---

### **Passo 8 – Deploy e monitoramento**

- Lançar em ambiente de produção  
- Monitorar erros e comportamento nos primeiros dias  
- Coletar feedback e aplicar melhorias contínuas  

> 🔗 [Link do projeto PIT](https://pitengenharia-de-softwar.bubbleapps.io/version-test/)
---

## ⚡ Conclusão

Seguindo esse cronograma, a **implementação do módulo ocorrerá de forma rápida e eficiente**, garantindo uma entrega funcional em curto prazo, com baixo custo e sem necessidade de desenvolvimento tradicional.

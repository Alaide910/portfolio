# Documentação de Regras de Negócio e Stakeholders

# Stakeholders envolvidos
O sistema foi pensado para atender diferentes perfis dentro da operação do supermercado, cada um com uma responsabilidade específica:

Proprietário/Gestor: é quem toma as decisões mais estratégicas, aprova regras, acompanha resultados e analisa relatórios financeiros.

Administrador do Sistema: cuida do cadastro de produtos, usuários, permissões e configurações gerais da plataforma.

Operador de Estoque: faz o controle diário das entradas, saídas, conferências de validade e identificação de produtos danificados.

Controle de Qualidade: acompanha perdas, autoriza descartes e verifica se os processos de validade estão sendo seguidos corretamente.

Fornecedor: é responsável pelas entregas e pela emissão das notas fiscais.

Cliente Final: recebe o impacto direto de um estoque bem controlado, com produtos dentro da validade e em boas condições.

Auditor/Contador: confere a rastreabilidade das informações e a conformidade dos relatórios financeiros.

TI / Segurança da Informação: garante backups, segurança dos dados, integridade do banco e controle de acesso simultâneo.

# Regras de negócio
RN-01 — Controle de estoque inteligente
O estoque nunca pode ficar negativo. Além disso, cada produto deve ter quantidade mínima e máxima definidas, com atualização em tempo real e suporte para mais de um local de armazenamento.

RN-02 — Classificação das movimentações
Toda movimentação precisa ser identificada como Entrada, Saída ou Ajuste. Assim que registrada, ela altera o saldo do estoque e fica salva em um histórico que possa ser auditado depois.

RN-03 — Informações obrigatórias
Nenhum registro pode ser salvo sem dados essenciais, como data, hora, usuário responsável, tipo de movimentação, produto, quantidade, validade, lote, justificativa e condição do item.

RN-04 — Cálculo automático do custo médio
Sempre que houver uma nova entrada, o sistema recalcula automaticamente o custo médio ponderado do produto, atualizando os relatórios de valorização do estoque.

RN-05 — Alertas automáticos
O sistema deve emitir avisos no dashboard, por e-mail e WhatsApp quando houver estoque baixo, produtos sem movimentação, validade próxima, produtos vencidos, itens danificados ou diferenças na contagem.

RN-06 — Controle de acesso por perfil
Cada usuário deve acessar apenas o que faz parte da sua função. O administrador tem acesso total e pode autorizar descartes, enquanto o operador trabalha com permissões mais limitadas e não visualiza custos operacionais.

RN-07 — Multiestoque e transferências
O sistema deve controlar saldos separados por loja ou depósito, permitindo transferências entre unidades de forma rastreável e organizada.

RN-08 — Relatórios gerenciais
Devem ser gerados automaticamente relatórios de posição de estoque, movimentações, produtos mais e menos vendidos, giro de estoque, valorização e histórico de descartes.

RN-09 — Segurança e confiabilidade
O sistema precisa realizar backups diários automáticos, validar dados no backend, controlar acessos simultâneos ao mesmo produto e manter um histórico imutável de alterações.

RN-10 — Validade, produtos danificados e diferenças de estoque
O sistema deve seguir a regra FEFO: vender primeiro o produto que vence antes. Produtos vencidos precisam ser bloqueados automaticamente. Itens danificados devem ser registrados obrigatoriamente para ajuste de saldo. Se houver diferença maior que 5% entre a contagem física e o sistema, a situação deve ser investigada imediatamente.

# Regras com inteligência artificial
O sistema também usa inteligência artificial para ajudar o gestor a tomar decisões mais rápidas e assertivas no dia a dia, sem depender de planilhas ou de decisões baseadas em “achismo”.

NR-11 — Previsão de compras
A IA analisa histórico de vendas, datas especiais, clima e eventos da cidade para indicar com antecedência o que comprar e em qual quantidade.

NR-12 — Sugestão de promoções
A IA identifica produtos parados, perto da validade ou com queda nas vendas e sugere promoções automáticas, como descontos, combos ou ações do tipo “leve 3, pague 2”.

NR-13 — Comparação de preços
Se o sistema tiver acesso aos preços de outros supermercados, a IA pode comparar valores e alertar quando o preço estiver muito acima da concorrência, ajudando o gestor a ajustar a estratégia comercial.
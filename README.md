# Trilha PCPE 2026 — Árvore detalhada

Nova versão criada a partir de `ÁRVORE DE ASSUNTOS — PCPE 2026` enviada em 28/10/2026.

## Conteúdo e contagem
- **12 áreas de acompanhamento**.
- **705 itens marcáveis**, cada um com o marcador de origem preservado: `[EDITAL]`, `[COMPLEMENTO]`, `[JURISPRUDÊNCIA]` ou `[CEBRASPE]`.
- Os títulos dos subassuntos organizam os itens, mas não entram no cálculo.
- A seção 12 (súmulas e entendimentos) é uma lista de revisão transversal e foi mantida como área independente, mesmo quando algum entendimento também é mencionado em outra matéria.
- As seções 13 (orientações de uso) e 14 (fontes oficiais) são orientativas e não entram na contagem.

## Áreas e quantidade de itens
- Legislação Estadual: 32
- Noções de Direito Constitucional: 84
- Noções de Direito Administrativo: 86
- Noções de Direito Penal: 147
- Noções de Direito Processual Penal: 71
- Língua Portuguesa: 47
- Informática: 63
- Raciocínio Lógico: 69
- Contabilidade Geral: 55
- Estatística: 26
- Atualidades — somente para a prova discursiva: 11
- Súmulas e entendimentos: lista curta para revisão transversal: 14

## Recursos
- Responsivo para computador e celular.
- Percentual geral e por área.
- Marcação individual ou em lote por grupo.
- Busca, filtros de matéria e exibição de pendentes.
- Backup JSON e importação de backup da própria versão.
- Salvamento local e sincronização Supabase por conta autenticada.
- Etiquetas visuais para os marcadores de origem.

## Como publicar no GitHub Pages
1. Extraia o ZIP.
2. Para manter a trilha antiga e esta nova, abra o repositório `eliellmiranda/trilha-pcpe` no GitHub, escolha **Add file → Create new file** e, como nome do arquivo, use `arvore-detalhada/index.html`. Cole nele o conteúdo do `index.html` deste pacote e faça **Commit changes**. Assim, a trilha nova ficará em uma pasta separada e não substituirá a página atual.
3. A nova URL será `https://eliellmiranda.github.io/trilha-pcpe/arvore-detalhada/`. Se você preferir substituir a trilha antiga, envie o HTML para a raiz como `index.html` em vez de criar a subpasta.
4. Aguarde o GitHub Pages concluir a publicação e abra a URL correspondente.

## Como conectar ao Supabase
1. Esta versão usa a URL e a chave pública (`sb_publishable_...`) já informadas para o projeto Supabase existente. A chave pública foi inserida no HTML; nunca inserir `service_role` ou `sb_secret` no frontend.
2. No Supabase, abra **SQL Editor → New query**, abra `supabase-setup-detalhada.sql`, copie todo o conteúdo, cole como uma consulta nova e clique em **Run** uma vez. O script cria a tabela isolada `public.pcpe_2026_topic_progress`, com RLS, políticas por usuário e Realtime; não apaga nem altera a tabela anterior `public.study_topic_progress`.
5. Em **Authentication → URL Configuration**, mantenha o **Site URL** já usado pela trilha anterior e adicione `https://eliellmiranda.github.io/trilha-pcpe/arvore-detalhada/` em **Redirect URLs** (se publicar na subpasta). O cadastro já solicita que a confirmação de e-mail volte para a URL da página aberta.
6. Abra a trilha publicada, crie conta ou entre com a mesma conta Supabase e teste marcar um item no computador e conferir no celular.

## Separação do progresso anterior
Esta versão tem chaves de armazenamento local próprias e usa tabela independente no Supabase. Assim, o progresso da trilha anterior não é misturado nem excluído. As contas de autenticação Supabase continuam sendo as mesmas.

## Nota sobre backups
Os backups JSON desta versão contêm IDs próprios. Importe-os apenas nesta versão detalhada. Exporte um backup periódico para redundância.

# Meu Supermercado

Aplicativo web responsivo para montar listas de compras, ler códigos de barras pela câmera, acompanhar o total previsto, finalizar compras, consultar histórico e comparar preços.

## Tecnologia
- HTML, CSS e JavaScript
- Supabase Auth + PostgreSQL
- Supabase JS v2 (CDN)
- Leitura de código com BarcodeDetector (quando suportado pelo navegador)

## Configuração
O projeto já está configurado para o Supabase do aplicativo:
- Projeto: `vpvdzxspixyhgctirlvv`
- Região: `sa-east-1`
- Chave cliente: publishable key (não contém service_role)

Abra `index.html` em hospedagem HTTPS. No primeiro acesso, crie sua conta pelo próprio aplicativo. Os dados são isolados por usuário com Row Level Security.

## Publicação
Ative GitHub Pages nas configurações do repositório, usando a branch `main` e pasta `/ (root)`. O endereço será:
`https://gomessamu1-beep.github.io/meu-supermercado/`

## Recursos iniciais
- Conta por e-mail e senha
- Lista atual, itens, quantidade, preço e total
- Leitura de código de barras em navegadores compatíveis
- Cadastro automático de produtos a partir da lista
- Finalização da compra
- Histórico e comparação do menor/maior preço registrado

## Segurança
O cliente utiliza somente a chave publishable. Todas as tabelas possuem RLS e as políticas limitam acesso ao próprio `auth.uid()`.

# Deploy do Simulador de Investimentos Crypto no Vercel

## Passos para Deploy

1. Crie uma conta no [Vercel](https://vercel.com) (se ainda não tiver).

2. Faça login no Vercel CLI:
```bash
npm i -g vercel
vercel login
```

3. No diretório do projeto, execute:
```bash
vercel
```
Siga as instruções para configurar o projeto.

4. Para deploy em produção:
```bash
vercel --prod
```

## Configurações Importantes

- Certifique-se que o arquivo `next.config.ts` está configurado corretamente para produção.
- Configure variáveis de ambiente no painel do Vercel, se necessário.
- O app será acessível via URL gerada pelo Vercel.

## Alternativas

- Netlify
- AWS Amplify
- Heroku (menos recomendado para Next.js)

## Suporte

Para dúvidas, consulte a documentação oficial do Vercel: https://vercel.com/docs

---

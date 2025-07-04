# Simulador de Investimentos - Alpha Binance

Um aplicativo de simulação de investimentos em criptomoedas focado nos lançamentos Alpha da Binance, com parâmetros configuráveis e integração com carteira virtual.

## 🚀 Características

### Parâmetros de Investimento Configuráveis
- **Valor por Entrada**: $5 a $100 por projeto Alpha
- **Stop Loss**: 10% a 90% (configurável)
- **Trailing Stop**: 100% a 500% (configurável)
- **Capital Total**: $1.000 inicial

### Funcionalidades Principais
- ✅ Simulação de trading em tempo real
- ✅ Integração com conta Binance (simulada)
- ✅ Sistema de carteira virtual
- ✅ Gráfico de evolução do portfólio
- ✅ Histórico detalhado de operações
- ✅ Interface moderna e responsiva
- ✅ Configurações personalizáveis via sliders

### Tecnologias Utilizadas
- **Next.js 15** - Framework React
- **TypeScript** - Tipagem estática
- **Tailwind CSS** - Estilização
- **Recharts** - Gráficos interativos
- **Shadcn/ui** - Componentes de UI

## 🛠️ Instalação e Execução

### Pré-requisitos
- Node.js 18+ 
- npm ou yarn

### Passos para Executar

1. **Clone ou extraia o projeto**
```bash
# Se usando git
git clone <repository-url>
cd crypto-investment-simulator

# Ou extraia o arquivo ZIP e navegue até a pasta
```

2. **Instale as dependências**
```bash
npm install
```

3. **Execute o projeto em modo desenvolvimento**
```bash
npm run dev
```

4. **Acesse a aplicação**
```
http://localhost:3000
```

### Scripts Disponíveis

```bash
# Desenvolvimento
npm run dev

# Build para produção
npm run build

# Executar versão de produção
npm start

# Verificação de tipos
npm run type-check

# Linting
npm run lint
```

## 📱 Como Usar

### 1. Conectar Conta Binance (Simulada)
- Insira qualquer API Key e Secret Key para simular a conexão
- A carteira virtual será inicializada com $1.000

### 2. Configurar Parâmetros de Investimento
- **Valor por Entrada**: Use o slider para definir entre $5-$100
- **Stop Loss**: Configure a porcentagem de perda máxima (10%-90%)
- **Trailing Stop**: Defina quando ajustar o stop após lucros (100%-500%)
- Clique em "Aplicar Configurações"

### 3. Executar Simulação
- Clique em "Iniciar Simulação" para começar
- Acompanhe em tempo real:
  - Evolução do capital total
  - Gráfico de performance
  - Histórico de operações
- Use "Parar Simulação" para interromper
- "Reiniciar" para resetar todos os dados

### 4. Monitorar Resultados
- **Capital Total**: Valor atual do portfólio
- **Capital Investido**: Quanto está em operações ativas
- **Lucro/Prejuízo**: Resultado acumulado
- **Gráfico**: Evolução temporal do portfólio
- **Histórico**: Todas as operações com detalhes

## 🎯 Estratégia de Investimento

### Lógica da Simulação
1. **Compra**: Investe o valor configurado em projetos Alpha aleatórios
2. **Stop Loss**: Vende automaticamente se o preço cair abaixo do limite
3. **Trailing Stop**: Ajusta o stop loss conforme o preço sobe
4. **Gestão de Risco**: Nunca investe mais que o capital disponível

### Projetos Alpha Simulados
- Alpha-1, Alpha-2, Alpha-3, Alpha-4, Alpha-5
- Preços simulados com volatilidade realística
- Movimentos de preço baseados em probabilidades

## 🔧 Estrutura do Projeto

```
src/
├── app/                    # Páginas Next.js
│   ├── layout.tsx         # Layout principal
│   └── page.tsx           # Página inicial
├── components/            # Componentes React
│   ├── auth/              # Autenticação Binance
│   ├── ui/                # Componentes de UI (Shadcn)
│   └── InvestmentSettings.tsx
├── hooks/                 # Hooks customizados
│   ├── useBinanceWallet.ts
│   └── useInvestmentSimulation.ts
└── lib/                   # Utilitários
    └── utils.ts
```

## 🚀 Deploy

### Vercel (Recomendado)
```bash
npm run build
# Deploy via Vercel CLI ou GitHub integration
```

### Docker
```bash
# Build da imagem
docker build -t crypto-simulator .

# Executar container
docker run -p 3000:3000 crypto-simulator
```

## 📊 Métricas e Analytics

O simulador rastreia:
- Número total de operações
- Taxa de sucesso (lucro vs prejuízo)
- Valor médio por operação
- Tempo médio de operação
- Performance por projeto Alpha

## 🔒 Segurança

- **Simulação Apenas**: Nenhuma operação real é executada
- **Dados Locais**: Informações armazenadas apenas no navegador
- **API Keys**: Usadas apenas para demonstração (não conectam à Binance real)

## 🐛 Solução de Problemas

### Erro de Porta em Uso
```bash
# Matar processo na porta 3000
lsof -ti:3000 | xargs kill -9
```

### Erro de Dependências
```bash
# Limpar cache e reinstalar
rm -rf node_modules package-lock.json
npm install
```

### Erro de Build
```bash
# Verificar tipos TypeScript
npm run type-check
```

## 📝 Licença

Este projeto é para fins educacionais e de demonstração. Não deve ser usado para investimentos reais sem a devida diligência e consultoria financeira.

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature
3. Commit suas mudanças
4. Push para a branch
5. Abra um Pull Request

## 📞 Suporte

Para dúvidas ou problemas:
- Verifique a documentação acima
- Consulte os logs do console do navegador
- Verifique os logs do terminal durante desenvolvimento

---

**⚠️ Aviso Legal**: Este é um simulador educacional. Não execute operações reais de trading sem conhecimento adequado dos riscos envolvidos no mercado de criptomoedas.

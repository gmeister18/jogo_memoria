# 🧩 Jogo da Memória — Correção Gramatical

Um jogo interativo e educativo que combina o clássico **Jogo da Memória** com um **desafio de correção gramatical**. Perfeito para aprender e praticar português de forma divertida!

## 📋 Descrição

Este é um aplicativo web desenvolvido com **HTML5, CSS3 e JavaScript puro**, sem dependências externas. O jogo desafia os jogadores a encontrarem pares de cartas corretamente, e então corrigir frases com erros gramaticais para confirmar o acerto.

A aplicação oferece uma experiência responsiva, funcionando perfeitamente em dispositivos móveis, tablets e desktops.

## 🎮 Como Jogar

1. **Clique nas cartas** para virar e encontrar o par correto
2. **Encontre os 15 pares** de frases (cada par contém a mesma frase, uma com erro e outra corrigida)
3. **Corrija a frase** dentro do modal que aparece após encontrar um par
4. **Use as dicas** fornecidas para ajudar na correção
5. **Complete o jogo** corrigindo todas as 15 frases
6. **Ganha mais pontos** com menos jogadas!

### Mecânicas do Jogo

- **2 chances para acertar**: Você tem 2 tentativas para corrigir cada frase
- **Dicas contextuais**: Cada volta contém uma dica sobre o erro gramatical
- **Sistema de sistema de pontuação**: Rastreado por número de movimentos
- **Barra de progresso**: Visualize seu avanço em tempo real
- **Resposta revelada**: Se errar 2 vezes, a resposta correta é mostrada
- **Hint system**: Após 3 tentativas erradas com um par, o jogo destaca as cartas relacionadas

## ✨ Recursos

✅ **15 frases diferentes** com erros gramaticais variados  
✅ **Design responsivo** que se adapta a qualquer resolução  
✅ **Animações suaves** com flip 3D das cartas  
✅ **Modal interativo** para correção com feedback em tempo real  
✅ **Acessibilidade** com suporte a teclado (Enter/Espaço para virar cartas)  
✅ **Sem dependências externas** - apenas HTML, CSS e JS vanilla  
✅ **Armazenamento de estatísticas** do jogador na sessão  

## 🌐 Tecnologias

- **HTML5** - Estrutura semântica
- **CSS3** - Layout responsivo com Grid, Flexbox e animações
  - CSS custom properties (variáveis)
  - Transições e keyframes animadas
  - Media queries para responsividade
- **JavaScript (Vanilla)** - Lógica do jogo sem frameworks
  - Normalização de entrada para comparação de frases
  - Gerenciamento de estado do jogo
  - Manipulação do DOM

## 📁 Estrutura do Projeto

```
jogo_memoria/
├── index.html          # Arquivo principal (HTML + CSS + JavaScript)
└── README.md           # Este arquivo
```

## 🚀 Como Executar

### Opção 1: Abrir diretamente no navegador
Simplesmente clique duas vezes no arquivo `index.html` ou arraste-o para seu navegador.

### Opção 2: Usando um servidor local (recomendado)

**Com Python 3:**
```bash
python -m http.server 8000
```

**Com Node.js (http-server):**
```bash
npx http-server
```

**Com Live Server (VS Code):**
- Instale a extensão Live Server
- Clique em "Go Live" no canto inferior direito

Depois acesse no navegador:
```
http://localhost:8000
```

## 🎨 Personalizações

### Adicionar novas frases

Para adicionar mais frases ao jogo, edite o array `PHRASES` no `index.html`:

```javascript
const PHRASES = [
  { 
    wrong: "Frase com erro aqui.",
    correct: "Frase corrigida aqui.",
    hint: "💡 Dica sobre o erro gramatical"
  },
  // ... mais frases
];
```

### Mudar temas de cores

As cores são definidas em variáveis CSS no `:root`:

```css
:root{
  --color-primary: #e05c2a;      /* Cor laranja
  --color-accent: #2a7be0;       /* Cor azul
  --color-success: #3aab5c;      /* Cor verde
  /* ... etc */
}
```

## 📊 Regras Gramaticais Cobertas

O jogo aborda os seguintes tópicos gramaticais:

- ✓ Concordância nominal (gênero e número)
- ✓ Concordância verbal
- ✓ Regência verbal (preposições)
- ✓ Uso de pronomes oblíquos
- ✓ Distinção entre "pra/para"
- ✓ Uso correto de "de" vs "em"
- ✓ Conjugação verbal no subjuntivo
- ✓ Tempo verbal adequado
- ✓ Pluralizações irregulares
- ✓ Registro formal vs informal

## 🎯 Experiência do Usuário

- **Mobile-first**: Otimizado para smartphones e tablets
- **Touch-friendly**: Sem necessidade de hover, idealmente para toque
- **Acessível**: Suporte a navegação por teclado
- **Performance**: Sem carregamentos, tudo em um único arquivo HTML
- **Responsivo**: Gride adaptativo que muda de 3 a 6 colunas conforme a tela

## 📝 Notas Sobre a Implementação

- A comparação de respostas é **case-insensitive** e **ignora acentos** para maior flexibilidade
- Pontuação e erros de pontuação são ignorados na verificação
- O jogo rastreia tentativas erradas e oferece dicas progressivas
- Sem persistência de dados (os dados são perdidos ao recarregar a página)

## 🔄 Fluxo do Jogo

```
1. Carregar página
2. Renderizar tabuleiro com 30 cartas (15 pares)
3. Jogador clica em cartas
4. Quando 2 cartas são viradas:
   ├─ Se forem par → Modal de correção
   ├─ Se não forem → Desvirar após 700ms
5. Modal pede correção da frase
   ├─ Certo → Marcar par como encontrado
   ├─ Errado (1ª vez) → Limpar input e deixar tentar novamente
   ├─ Errado (2ª vez) → Revelar resposta
   └─ Continuar → Fechar modal e voltar ao jogo
6. Repetir até encontrar todos os 15 pares
7. Tela de vitória com pontuação final
```

## 💡 Dicas para Melhorar a Pontuação

- Preste atenção nas frases com erro para reconhecer o padrão
- Use as dicas fornecidas para aprender sobre regras gramaticais
- Tente memorizar a localização das cartas
- Se estiver preso, revele a resposta e aprenda com ela

## 🌟 Futuras Melhorias Possíveis

- [ ] Sistema de diferentes níveis de dificuldade
- [ ] Modo multiplayer
- [ ] Persistência de dados (Local Storage)
- [ ] Diferentes categorias de erros gramaticais
- [ ] Ranking de pontuações
- [ ] Som e efeitos visuais adicionais
- [ ] Modo escuro
- [ ] Tradução para outros idiomas

## 📜 Licença

Este projeto está disponível sob a licença MIT. Sinta-se livre para usar, modificar e distribuir.

---

**Desenvolvido com ❤️ para tornar o aprendizado de português mais divertido!**
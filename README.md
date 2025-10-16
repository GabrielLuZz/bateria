# Português

## Descrição
Este projeto é uma bateria virtual simples construída com HTML, CSS e JavaScript. As teclas Q, W, E, A, S, D, Z, X e C reproduzem sons específicos. Quando um som é tocado, a tecla correspondente é destacada visualmente por 300 ms. Você também pode criar uma composição digitando uma sequência de letras minúsculas no campo de texto e clicando em "Tocar"; cada caractere será reproduzido em série com um intervalo de 250 ms entre as notas.

## Requisitos
- Navegador moderno (Chrome, Firefox, Edge) com suporte a áudio.
- Nenhuma dependência externa ou backend.
- Opcional: servidor local de arquivos estáticos para desenvolvimento.

## Estrutura do projeto
```
bateria/
├── index.html
├── style.css
├── script.js
└── sounds/
    ├── keya.wav
    ├── keyc.wav
    ├── keyd.wav
    ├── keye.wav
    ├── keyq.wav
    ├── keys.wav
    ├── keyw.wav
    ├── keyx.wav
    └── keyz.wav
```

## Como executar
1) Método direto: abra o arquivo `index.html` em um navegador.
2) Método recomendado (servidor estático):
   - Python 3:
     ```bash
     python3 -m http.server 8000
     # Acesse: http://localhost:8000/index.html
     ```
   - Node (npx serve):
     ```bash
     npx serve .
     # Acesse a URL exibida no terminal
     ```

## Mapeamento de teclas
- Q → `sounds/keyq.wav` (elementos: `#s_keyq`, `data-key="keyq"`)
- W → `sounds/keyw.wav`
- E → `sounds/keye.wav`
- A → `sounds/keya.wav`
- S → `sounds/keys.wav`
- D → `sounds/keyd.wav`
- Z → `sounds/keyz.wav`
- X → `sounds/keyx.wav`
- C → `sounds/keyc.wav`

## Uso
- Pelo teclado: pressione Q, W, E, A, S, D, Z, X ou C para tocar os sons e ver o destaque visual.
- Pela composição: digite uma sequência de letras minúsculas (por exemplo, `qweasdzxc`) no campo de texto e clique em "Tocar". O sistema reproduz cada caractere com um intervalo de 250 ms.

Observações:
- A composição aceita apenas caracteres minúsculos que correspondam às teclas suportadas; caracteres não suportados (por exemplo, espaço) serão ignorados.
- O destaque visual da tecla permanece por 300 ms.

## Personalização
- Para adicionar uma nova tecla (por exemplo, R):
  1. Adicione o bloco da tecla no `index.html`:
     ```html
     <div data-key="keyr" class="key">R</div>
     <audio id="s_keyr" src="sounds/keyr.wav"></audio>
     ```
  2. Coloque o arquivo de áudio correspondente em `sounds/keyr.wav`.
  3. O JavaScript já trata eventos de teclado via `event.code.toLowerCase()` (ex.: `KeyR` → `keyr`), então não é necessário alterar `script.js` para novas letras.
- Para mudar o tempo entre notas na composição, ajuste o incremento `wait += 250;` em `script.js`.

## Créditos
O rodapé do projeto indica: "Criado pela B7Web". Créditos ao material/ideia original da B7Web.


# English

## Description
This project is a simple virtual drum built with HTML, CSS, and JavaScript. Keys Q, W, E, A, S, D, Z, X, and C play specific sounds. When a sound is played, the corresponding key gets visually highlighted for 300 ms. You can also create a composition by typing a sequence of lowercase letters in the text field and clicking "Tocar" (Play); each character is played in sequence with a 250 ms interval between notes.

## Requirements
- Modern web browser (Chrome, Firefox, Edge) with audio support.
- No external dependencies or backend.
- Optional: local static file server for development.

## Project structure
```
bateria/
├── index.html
├── style.css
├── script.js
└── sounds/
    ├── keya.wav
    ├── keyc.wav
    ├── keyd.wav
    ├── keye.wav
    ├── keyq.wav
    ├── keys.wav
    ├── keyw.wav
    ├── keyx.wav
    └── keyz.wav
```

## How to run
1) Direct method: open `index.html` in your browser.
2) Recommended (static server):
   - Python 3:
     ```bash
     python3 -m http.server 8000
     # Visit: http://localhost:8000/index.html
     ```
   - Node (npx serve):
     ```bash
     npx serve .
     # Visit the URL shown in the terminal
     ```

## Key mapping
- Q → `sounds/keyq.wav` (elements: `#s_keyq`, `data-key="keyq"`)
- W → `sounds/keyw.wav`
- E → `sounds/keye.wav`
- A → `sounds/keya.wav`
- S → `sounds/keys.wav`
- D → `sounds/keyd.wav`
- Z → `sounds/keyz.wav`
- X → `sounds/keyx.wav`
- C → `sounds/keyc.wav`

## Usage
- Keyboard: press Q, W, E, A, S, D, Z, X, or C to play sounds and see the key animation/highlight.
- Composition: type a sequence of lowercase letters (e.g., `qweasdzxc`) in the text field and click "Tocar" (Play). The system plays each character with a 250 ms interval.

Notes:
- The composition only accepts lowercase characters that match supported keys; unsupported characters (e.g., space) are ignored.
- Key highlight lasts 300 ms.

## Customization
- To add a new key (e.g., R):
  1. Add the key block in `index.html`:
     ```html
     <div data-key="keyr" class="key">R</div>
     <audio id="s_keyr" src="sounds/keyr.wav"></audio>
     ```
  2. Place the corresponding audio file at `sounds/keyr.wav`.
  3. JavaScript already handles keyboard events via `event.code.toLowerCase()` (e.g., `KeyR` → `keyr`), so no changes are required in `script.js` for new letter keys.
- To change the composition tempo, adjust the `wait += 250;` increment in `script.js`.

## Credits
The project footer says: "Criado pela B7Web" (Created by B7Web). Credits to B7Web for the original material/idea.


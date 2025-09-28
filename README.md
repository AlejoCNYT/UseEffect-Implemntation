# UseEffect Implementation – Quiz Countdown (ES/EN)

> React + Vite mini‑project that demonstrates `useEffect` for **mount / update / unmount** with a quiz countdown timer, confirmation dialog, and cleanup logic.  
> Proyecto mini de React + Vite que demuestra `useEffect` para **montaje / actualización / desmontaje** con un temporizador regresivo, confirmación y limpieza.

---

## 🧩 Features / Características

- `useEffect` on **mount** to call `window.confirm(...)` and optionally finish early.  
  `useEffect` en **montaje** para llamar `window.confirm(...)` y terminar anticipadamente.
- `useEffect` on **update** running a `setInterval` countdown (**1s**) and **cleanup** with `clearInterval`.  
  `useEffect` en **actualización** ejecutando un conteo con `setInterval` (**1s**) y **limpieza** con `clearInterval`.
- `useEffect` on **unmount** to notify the parent with `{ message: "Tarea realizada!" }`.  
  `useEffect` en **desmontaje** para notificar al padre con `{ message: "Tarea realizada!" }`.
- Snapshot tests via **Vitest**. / Pruebas de snapshot con **Vitest**.

---

## ✅ Requirements / Requisitos

- **Node.js 18+** (recommended / recomendado)  
- **npm** (bundled with Node) / **npm** (incluido con Node)
- A terminal: PowerShell (Windows), Git Bash, zsh/bash, etc.  
  Una terminal: PowerShell (Windows), Git Bash, zsh/bash, etc.

> Check versions / Verificar versiones:
```bash
node -v
npm -v
```

---

## 🚀 Quick Start / Inicio Rápido

Clone this repository / Clona este repositorio:
```bash
git clone https://github.com/AlejoCNYT/UseEffect-Implemntation.git
cd UseEffect-Implemntation
```

Install dependencies / Instala dependencias:
```bash
npm install
```

Run the dev server / Ejecuta el servidor de desarrollo:
```bash
npm run dev
# Open the printed URL in your browser / Abre la URL impresa en tu navegador
```

Run the assignment tests / Ejecuta las pruebas del laboratorio:
```bash
npm run ada-test
```

> If your cohort uses `ada-client`, run it in **another terminal** from the repo root:  
> Si tu cohorte usa `ada-client`, ejecútalo en **otra terminal** desde la raíz:
```bash
# Windows (PowerShell)
.\ada-client.exe start https://eci.learn.ada-school.org/cohorts/<cohortId>

# Linux
./ada-client-linux start https://eci.learn.ada-school.org/cohorts/<cohortId>

# macOS
./ada-client start https://eci.learn.ada-school.org/cohorts/<cohortId>
```

---

## 🗂 Project Structure / Estructura

```
src/
├─ App.jsx                 # Shows button and mounts CountDownTimer / Muestra botón y monta CountDownTimer
├─ components/
│  └─ CountDownTimer.jsx   # Countdown + effects (mount/update/unmount) / Conteo + efectos
└─ main.jsx                # Vite entry point / Punto de entrada Vite
```

---

## 🧪 Testing Notes / Notas de Pruebas

- Tests expect the button text **exactly**: `empezar quiz`.  
  Las pruebas esperan el texto del botón **exacto**: `empezar quiz`.
- Snapshot expects:  
  `Quedan: {n} segundos` and a title `Ada Quiz`.  
  El snapshot espera:  
  `Quedan: {n} segundos` y un título `Ada Quiz`.
- The component accepts props: `duration` (default 5), `onFinish`, `onUnmount`.  
  El componente acepta props: `duration` (por defecto 5), `onFinish`, `onUnmount`.

---

## 🛠 Troubleshooting / Solución de Problemas

### Windows “NUL” phantom file / Archivo fantasma “NUL”
If you ever see `error: invalid path 'NUL'`, delete it with:  
Si ves `error: invalid path 'NUL'`, elimínalo con:
```bash
cmd //c "del \\?\%cd%\NUL" 2>nul
```

### Line endings / Finales de línea (CRLF vs LF)
To avoid noisy diffs on Windows:  
Para evitar diffs ruidosos en Windows:
```bash
git config core.autocrlf true
```

### Slow/failed pushes / Push lento o fallido (HTTP 408)
```bash
git config --global http.postBuffer 524288000
git push --no-reuse-delta --no-verify
# Or use SSH / O usa SSH:
# git remote set-url origin git@github.com:AlejoCNYT/UseEffect-Implemntation.git
```

---

## 📦 Scripts

- `npm run dev` — Vite dev server  
- `npm run build` — Production build  
- `npm run ada-test` — Vitest run for assignment

---

## 📘 License / Licencia

MIT © 2025 AlejoCNYT

# 📋 GUÍA COMPLETA DE GIT Y GITHUB PARA ALKE WALLET

## 🎯 PASO 1: Configuración Inicial de Git (SI NO LO HAS HECHO)

# Configurar tu nombre y email en Git
git config --global user.name "Tu Nombre"
git config --global user.email "tu-email@ejemplo.com"

# Verificar configuración
git config --global --list


## 🚀 PASO 2: Inicializar el Repositorio Local

# 1. Abrir PowerShell en la carpeta del proyecto
# cd "c:\Users\ACER\Desktop\proyecto 2 - diaz-yamilet"

# 2. Inicializar Git
git init

# 3. Ver archivos sin seguimiento
git status


## 📝 PASO 3: Primer Commit en Main

# 1. Agregar todos los archivos
git add .

# 2. Hacer commit inicial
git commit -m "chore: inicializar proyecto Alke Wallet con estructura base"

# 3. Verificar el commit
git log --oneline


## 🌿 PASO 4: Crear Ramas de Features

# IMPORTANTE: Primero vamos a crear commits organizados por funcionalidad

# --- RAMA FEATURE/LOGIN ---
git checkout -b feature/login

# Agregar cambios de login
git add login.html assets/js/login.js

# Commit de login
git commit -m "feat(login): implementar sistema de autenticación

- Formulario de login con validaciones Bootstrap
- Validación en tiempo real con jQuery
- Toggle de visibilidad de contraseña
- Efectos visuales de éxito/error
- Credenciales: usuario@billetera.com / 123456
- Almacenamiento de sesión en localStorage"

# Volver a main y fusionar
git checkout main
git merge feature/login --no-ff -m "merge: integrar feature/login en main"


# --- RAMA FEATURE/DEPOSITOS ---
git checkout -b feature/depositos

# Agregar cambios de depósitos
git add deposit.html assets/js/deposit.js

# Commit de depósitos
git commit -m "feat(depositos): agregar funcionalidad de depósitos

- Formulario de depósito con validaciones
- Modal de confirmación Bootstrap
- Efecto confetti al depositar
- Actualización animada del saldo
- Validación en tiempo real del monto
- Persistencia en localStorage"

# Volver a main y fusionar
git checkout main
git merge feature/depositos --no-ff -m "merge: integrar feature/depositos en main"


# --- RAMA FEATURE/TRANSACCIONES ---
git checkout -b feature/transacciones

# Agregar cambios de transacciones
git add sendomoney.html transactions.html assets/js/sendomoney.js assets/js/transactions.js

# Commit de transacciones
git commit -m "feat(transacciones): implementar envío y historial de transacciones

TRANSFERENCIAS:
- Búsqueda de contactos en tiempo real
- Autocompletado con jQuery UI
- Modal de confirmación de transferencia
- Validación de saldo suficiente
- Gestión de contactos (agregar/listar)

HISTORIAL:
- Lista completa de movimientos
- Filtros por tipo (depósitos/transferencias)
- Búsqueda en tiempo real
- Tarjetas de resumen con estadísticas
- Animaciones de aparición escalonada"

# Volver a main y fusionar
git checkout main
git merge feature/transacciones --no-ff -m "merge: integrar feature/transacciones en main"


## 🎨 PASO 5: Commits Adicionales de Mejoras

# Commit de estilos
git add assets/css/style.css
git commit -m "style: mejorar diseño responsive y animaciones CSS

- Variables CSS para colores consistentes
- Diseño responsive para móvil/tablet/desktop
- Animaciones smooth y transiciones
- Efectos hover en tarjetas
- Marco simulado de móvil en desktop
- Autocomplete jQuery UI personalizado"

# Commit de menú principal
git add menu.html assets/js/menu.js
git commit -m "feat(menu): crear menú principal con estadísticas

- Navbar responsive de Bootstrap
- Tarjetas de resumen financiero
- Contador animado de saldo
- Grid de funcionalidades
- Animaciones jQuery en valores
- Cierre de sesión con confirmación"

# Commit de documentación
git add README.md .gitignore
git commit -m "docs: agregar README completo y .gitignore

- Documentación detallada del proyecto
- Instrucciones de instalación y uso
- Descripción de tecnologías
- Guía de características
- Badges de tecnologías
- Estructura del proyecto"


## 🌐 PASO 6: Crear Repositorio en GitHub

### Opción A: Desde la Web de GitHub

1. Ir a https://github.com
2. Iniciar sesión en tu cuenta
3. Click en el botón "+" arriba a la derecha
4. Seleccionar "New repository"
5. Configurar:
   - Repository name: alke-wallet
   - Description: Billetera virtual desarrollada con HTML, CSS, JavaScript, Bootstrap y jQuery
   - Visibility: Public (o Private si prefieres)
   - NO marcar "Initialize this repository with a README" (ya lo tenemos)
6. Click en "Create repository"

### Opción B: Desde GitHub CLI (si tienes gh instalado)

gh repo create alke-wallet --public --source=. --remote=origin


## 🔗 PASO 7: Conectar Repositorio Local con GitHub

# Agregar remote (reemplaza [tu-usuario] con tu usuario de GitHub)
git remote add origin https://github.com/[tu-usuario]/alke-wallet.git

# Verificar remote
git remote -v

# Renombrar rama principal a main (si es necesario)
git branch -M main

# Hacer push al repositorio remoto
git push -u origin main

# Hacer push de todas las ramas
git push origin feature/login
git push origin feature/depositos
git push origin feature/transacciones


## 📤 PASO 8: Crear Pull Requests en GitHub

### Para cada rama feature:

1. Ir a: https://github.com/[tu-usuario]/alke-wallet
2. Click en "Pull requests"
3. Click en "New pull request"
4. Seleccionar:
   - base: main
   - compare: feature/login (o la rama que quieras)
5. Click en "Create pull request"
6. Agregar título y descripción
7. Click en "Create pull request"
8. Revisar cambios
9. Click en "Merge pull request"
10. Confirmar el merge

### Títulos sugeridos para PR:

**PR #1: Feature/Login**
```
Implementar sistema de autenticación con validaciones

Funcionalidades:
- Formulario de login con Bootstrap
- Validaciones en tiempo real con jQuery
- Toggle de contraseña
- Efectos visuales de éxito/error
- Gestión de sesión con localStorage

Reviewed-by: [tu nombre]
```

**PR #2: Feature/Depositos**
```
Agregar funcionalidad de depósitos con confirmación

Funcionalidades:
- Formulario de depósito validado
- Modal de confirmación Bootstrap
- Efecto confetti de celebración
- Actualización animada del saldo
- Validación en tiempo real

Reviewed-by: [tu nombre]
```

**PR #3: Feature/Transacciones**
```
Implementar transferencias y historial de transacciones

Funcionalidades TRANSFERENCIAS:
- Búsqueda de contactos en tiempo real
- Autocompletado jQuery UI
- Modal de confirmación
- Validación de saldo

Funcionalidades HISTORIAL:
- Filtros dinámicos
- Búsqueda en tiempo real
- Estadísticas animadas

Reviewed-by: [tu nombre]
```


## 📊 PASO 9: Verificar el Repositorio

# Ver todas las ramas
git branch -a

# Ver historial de commits
git log --oneline --graph --all --decorate

# Ver estado del repositorio
git status


## 🏷️ PASO 10: Crear Tags para Versiones (OPCIONAL)

# Crear tag de versión 1.0.0
git tag -a v1.0.0 -m "Release: Alke Wallet v1.0.0

Características principales:
- Sistema de autenticación
- Depósitos de fondos
- Transferencias entre contactos
- Historial de transacciones
- Diseño responsive
- Animaciones jQuery"

# Hacer push del tag
git push origin v1.0.0

# Ver todos los tags
git tag


## 🔄 COMANDOS ÚTILES PARA EL FUTURO

# Ver diferencias antes de commit
git diff

# Ver ramas
git branch

# Cambiar de rama
git checkout [nombre-rama]

# Eliminar rama local
git branch -d [nombre-rama]

# Actualizar desde GitHub
git pull origin main

# Ver historial gráfico bonito
git log --oneline --graph --all --decorate --color

# Deshacer último commit (mantener cambios)
git reset --soft HEAD~1

# Ver quién modificó cada línea
git blame [archivo]


## 📋 CHECKLIST COMPLETO

### Antes de GitHub:
- ✅ .gitignore creado
- ✅ README.md completo
- ✅ Git inicializado
- ✅ Commits organizados
- ✅ Ramas creadas
- ✅ Ramas fusionadas en main

### En GitHub:
- ⬜ Repositorio creado en GitHub
- ⬜ Remote configurado
- ⬜ Push de main
- ⬜ Push de todas las ramas
- ⬜ Pull Requests creados
- ⬜ Pull Requests revisados y fusionados
- ⬜ Tags de versión creados

### Verificaciones:
- ⬜ README.md se ve correctamente en GitHub
- ⬜ Todas las ramas están en GitHub
- ⬜ Historial de commits es claro
- ⬜ Pull Requests muestran cambios correctos


## 🎓 BUENAS PRÁCTICAS APLICADAS

✅ **Commits Semánticos:**
- `feat:` para nuevas funcionalidades
- `fix:` para correcciones de bugs
- `style:` para cambios de estilos
- `docs:` para documentación
- `chore:` para tareas de mantenimiento

✅ **Mensajes Descriptivos:**
- Títulos claros y concisos
- Descripciones detalladas
- Contexto suficiente

✅ **Ramas Organizadas:**
- `main` para código estable
- `feature/*` para nuevas funcionalidades

✅ **Pull Requests:**
- Revisión de código
- Descripción de cambios
- Merge con --no-ff para mantener historial

✅ **Documentación:**
- README completo
- .gitignore apropiado
- Comentarios en código


## 💡 CONSEJOS FINALES

1. **Commits frecuentes:** Haz commits pequeños y frecuentes
2. **Mensajes claros:** Escribe mensajes que expliquen el "por qué"
3. **Pull antes de Push:** Siempre haz `git pull` antes de `git push`
4. **Revisa antes de commit:** Usa `git status` y `git diff`
5. **Branches para features:** Cada funcionalidad en su propia rama
6. **Prueba antes de merge:** Verifica que todo funcione antes de fusionar


## 🆘 SOLUCIÓN DE PROBLEMAS COMUNES

### Error: "fatal: not a git repository"
```bash
# Asegúrate de estar en la carpeta correcta
cd "c:\Users\ACER\Desktop\proyecto 2 - diaz-yamilet"
git init
```

### Error: "remote origin already exists"
```bash
# Eliminar remote existente
git remote remove origin
# Agregar nuevamente
git remote add origin https://github.com/[tu-usuario]/alke-wallet.git
```

### Error al hacer push
```bash
# Si es el primer push
git push -u origin main

# Si hay conflictos
git pull origin main --rebase
git push origin main
```

### Deshacer cambios no commiteados
```bash
# Un archivo específico
git checkout -- [archivo]

# Todos los archivos
git reset --hard HEAD
```


---

📌 **RECUERDA:** Reemplaza `[tu-usuario]` con tu usuario real de GitHub en todos los comandos.

🎯 **OBJETIVO:** Tener un repositorio profesional con 15/15 puntos en Git y GitHub.

✨ **ÉXITO:** ¡Sigue estos pasos y tendrás un repositorio impecable!

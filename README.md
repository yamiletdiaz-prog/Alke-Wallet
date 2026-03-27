Aplicacion web de billetera virtual desarrollada como proyecto academico. Simula un flujo real de finanzas personales: iniciar sesion, administrar saldo, realizar depositos, enviar dinero y revisar transacciones.

## Vista General

Alke Wallet esta orientada a demostrar habilidades frontend con foco en:

- Arquitectura por modulos en JavaScript.
- Experiencia de usuario con validaciones en tiempo real.
- Diseno responsive para distintas resoluciones.
- Persistencia local con `localStorage`.

## Funcionalidades Principales

- Autenticacion de usuario con validacion de formulario.
- Dashboard principal con resumen financiero.
- Deposito de fondos con confirmacion visual.
- Envio de dinero entre contactos.
- Historial de movimientos con filtros y busqueda.
- Persistencia de datos en navegador.

## Stack Tecnologico

- HTML5
- CSS3
- JavaScript (ES6)
- Bootstrap 5
- jQuery
- jQuery UI
- Font Awesome

## Estructura del Proyecto

```text
.
|-- index.html
|-- login.html
|-- menu.html
|-- deposit.html
|-- sendomoney.html
|-- transactions.html
|-- assets/
|   |-- css/
|   |   `-- style.css
|   |-- images/
|   `-- js/
|       |-- login.js
|       |-- menu.js
|       |-- deposit.js
|       |-- sendomoney.js
|       `-- transactions.js
|-- GIT_COMMANDS.md
|-- LICENSE
`-- README.md
```

## Como Ejecutarlo

1. Clona el repositorio:

```bash
git clone https://github.com/yamiletdiaz-prog/alke-wallet.git
cd alke-wallet
```

2. Abre `index.html` en tu navegador.
3. Opcional: usa Live Server en VS Code para un flujo mas comodo.

## Credenciales de Prueba

- Usuario: `usuario@billetera.com`
- Contrasena: `123456`

## Capturas

Seccion preparada para agregar evidencias visuales del proyecto.

Cuando subas imagenes en `assets/images/`, puedes usar este formato:

```md
![Login](assets/images/login.png)
![Menu principal](assets/images/menu.png)
![Depositos](assets/images/deposit.png)
![Transacciones](assets/images/transactions.png)
```

## Flujo de Navegacion

1. Login.
2. Menu principal.
3. Depositar o enviar dinero.
4. Revisar historial.
5. Cerrar sesion.

## Roadmap

- Integrar backend y base de datos.
- Incorporar registro de usuarios.
- Agregar pruebas unitarias y de interfaz.
- Mejorar accesibilidad y cobertura mobile.

## Autor

Yamilet Diaz

## Licencia

Proyecto bajo licencia MIT. Revisa el archivo [LICENSE](LICENSE).

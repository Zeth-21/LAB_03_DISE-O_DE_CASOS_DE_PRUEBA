# 🧪 Laboratorio: Pruebas y Aseguramiento de Calidad - Caso Mercado Libre

## 👨‍💻 Datos del Estudiante

* **Nombre:** Yordi Ajeo Atao Huaman
* **Curso:** Pruebas y Aseguramiento de Calidad
* **Código:** 27222121

---

## 🎯 Objetivo del Laboratorio

Dominar el flujo de trabajo en equipo utilizando un repositorio remoto compartido. Esto implica aplicar las mejores prácticas de control de versiones, resolución de conflictos y colaboración descentralizada a través de Git y GitHub.

---

## 💻 1. Descripción general del Sistema
**Mercado Libre S.R.L.** es una plataforma líder de comercio electrónico (*e-commerce*) en América Latina que cuenta con un ecosistema web y móvil integral. Actualmente, se gestiona y optimiza el **SGA (Sistema de Gestión de Autenticación y Cuentas)**, una aplicación web de alta disponibilidad que permite a millones de usuarios interactuar de forma segura dentro del *marketplace*. El sistema ofrece funcionalidades críticas como inicio de sesión seguro basado en roles y perfiles (**Comprador, Vendedor, Administrador de Tienda Oficial**), registro de nuevos usuarios con estrictas validaciones de seguridad, pasarela de autenticación unificada y protección de datos sensibles. El SGA cuenta con sólidas validaciones de negocio en todos sus formularios, proporcionando una experiencia ágil, segura y accesible desde cualquier navegador o dispositivo.

---

## ⚙️ 2. Descripción de funcionalidades

### 2.1 Funcionalidad de Login
La funcionalidad de Login permite a los usuarios acceder de forma segura a sus cuentas personales o corporativas ingresando su correo electrónico (o apodo de usuario) y su contraseña registrada. El sistema procesa y valida las credenciales proporcionadas en la base de datos centralizada. Si los datos son correctos, concede el acceso al panel principal personalizado de Mercado Libre (**Home / Dashboard de Usuario**), donde el cliente puede gestionar sus compras, revisar el estado de sus envíos, responder preguntas de clientes, verificar sus ventas o acceder a Mercado Pago. En caso de que las credenciales sean incorrectas o no cumplan con el formato, el sistema bloquea el acceso de inmediato y muestra un mensaje de error específico en la interfaz, resguardando la seguridad de la cuenta.

---

## 📋 3. Matriz de Casos de Prueba (Google Sheets Resumen)

| ID | Funcionalidad | Nombre del Caso | Técnica | Prioridad | Resultado Esperado (resumen) | URL DE DOCUMENTO TESTING |
| :---: | :--- | :--- | :---: | :---: | :--- | :--- |
| **TC-001** | Login | Login tradicional exitoso con correo y contraseña | PE-Valida | 🔴 Alta | Otorga el acceso, redirige al Home de Mercado Libre y muestra el nombre del usuario. | [ ]() |
| **TC-002** | Login | Iniciar sesión con un clic (Usuario recordado) | PE-Valida | 🔴 Alta | Salta el paso del correo, valida la contraseña e ingresa directo a la cuenta. | [ ]() |
| **TC-003** | Login | Login fallido por contraseña incorrecta | PE-Invalida | 🔴 Alta | Deniega el acceso, mantiene la pantalla y muestra el mensaje 'Revisa tu contraseña'. | [ ]() |
| **TC-004** | Login | Login fallido por correo no registrado | PE-Invalida | 🔴 Alta | Bloquea el avance y muestra la alerta 'No encontramos ninguna cuenta con ese correo'. | [ ]() |
| **TC-005** | Login | Login bloqueado por formato de correo inválido | PE-Invalida | 🟡 Media | Detiene el envío localmente y muestra el aviso en pantalla 'Escribe un e-mail válido'. | [ ]() |
| **TC-006** | Login | Login bloqueado por dejar campos vacíos | PE-Invalida | 🟡 Media | No realiza peticiones al servidor y resalta el campo vacío con 'Completa este campo'. | [ ]() |
| **TC-007** | Login | Login exitoso con clave en límite mínimo (6 caracteres) | Valores Límite | 🔴 Alta | Acepta el tamaño de la contraseña por estar en el límite válido (6 carac.) e ingresa. | [ ]() |
| **TC-008** | Login | Login bloqueado por clave menor al mínimo (5 caracteres) | Valores Límite | 🔴 Alta | Bloquea el botón de envío e indica 'La contraseña debe tener al menos 6 caracteres'. | [ ]() |
| **TC-009** | Login | Login con texto masivo en campo contraseña | Edge Case | 🟡 Media | El sistema restringe o trunca los caracteres excedentes sin colapsar y deniega el acceso. | [ ]() |
| **TC-010** | Login | Login con emojis o símbolos raros en correo | Edge Case | 🟡 Media | Sanitiza la entrada, rechaza el uso de emojis/símbolos y muestra 'Escribe un e-mail válido'. | [ ]() |

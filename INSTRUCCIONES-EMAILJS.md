<<<<<<< HEAD
# Configuración de EmailJS para Sistema PQRS - ASOREANC

## 📧 ¿Qué es EmailJS?

EmailJS es un servicio que permite enviar emails directamente desde el frontend sin necesidad de un servidor backend. Es perfecto para formularios de contacto y sistemas PQRS como el nuestro.

## 🚀 Pasos para Configurar EmailJS

### 1. Crear Cuenta en EmailJS

1. Ve a [https://www.emailjs.com/](https://www.emailjs.com/)
2. Haz clic en "Sign Up" y crea una cuenta gratuita
3. Verifica tu email

### 2. Configurar Servicio de Email (Gmail)

1. En el dashboard de EmailJS, ve a **"Email Services"**
2. Haz clic en **"Add New Service"**
3. Selecciona **"Gmail"**
4. Haz clic en **"Connect Account"**
5. Autoriza el acceso a tu cuenta de Gmail
6. **Anota el SERVICE ID** que se genera (ej: `service_abc123`)

### 3. Crear Template de Email

1. Ve a **"Email Templates"**
2. Haz clic en **"Create New Template"**
3. Configura el template así:

**Subject:**
```
Nueva PQRS {{pqrs_type}} - {{pqrs_id}} - ASOREANC
```

**Body:**
```
NUEVA PQRS RECIBIDA - ASOREANC
================================

Número de Radicado: {{pqrs_id}}
Fecha: {{pqrs_date}}
Tipo: {{pqrs_type}}

DATOS DEL SOLICITANTE:
----------------------
Nombre: {{from_name}}
Email: {{from_email}}
Teléfono: {{from_phone}}

SOLICITUD:
----------
Asunto: {{pqrs_subject}}

Mensaje:
{{pqrs_message}}

================================
Este mensaje fue enviado desde el sistema PQRS de ASOREANC
Para responder, contacta directamente al solicitante: {{from_email}}
```

4. Guarda el template y **anota el TEMPLATE ID** (ej: `template_xyz789`)

### 4. Obtener Public Key

1. Ve a **"Account"** > **"General"**
2. Copia tu **"Public Key"** (ej: `user_abcdef123456`)

### 5. Configurar el Archivo emailjs-config.js

Abre el archivo `emailjs-config.js` y reemplaza los valores:

```javascript
const EMAILJS_CONFIG = {
  serviceID: 'service_abc123',        // Tu Service ID real
  templateID: 'template_xyz789',      // Tu Template ID real  
  publicKey: 'user_abcdef123456',     // Tu Public Key real
  destinationEmail: 'tu-email@gmail.com'  // Email donde quieres recibir las PQRS
};
```

### 6. Probar el Sistema

1. Abre la página PQRS en tu navegador
2. Llena el formulario de prueba
3. Envía una PQRS de prueba
4. Verifica que llegue el email a tu Gmail

## 🔧 Límites del Plan Gratuito

- **200 emails por mes** (más que suficiente para la mayoría de casos)
- Si necesitas más, puedes upgrader a un plan pago

## 🛠️ Solución de Problemas

### El email no llega:
1. Verifica que los IDs en `emailjs-config.js` sean correctos
2. Revisa la consola del navegador para errores
3. Verifica que el template tenga todas las variables correctas
4. Revisa la carpeta de spam en Gmail

### Error de CORS:
- EmailJS maneja automáticamente CORS, no debería haber problemas

### Error de autenticación:
- Verifica que el Public Key sea correcto
- Asegúrate de que el servicio de Gmail esté activo

## 📱 Características del Sistema

✅ **Funcional**: Los emails llegan realmente a Gmail  
✅ **Seguro**: No expone credenciales sensibles  
✅ **Gratuito**: Hasta 200 emails/mes  
✅ **Fácil**: No requiere backend  
✅ **Profesional**: Emails con formato limpio  
✅ **Rastreable**: Cada PQRS tiene un número único  

## 🎯 Resultado Final

Una vez configurado, cuando alguien envíe una PQRS:

1. Se genera un número de radicado único
2. Se envía un email profesional a tu Gmail
3. El usuario recibe confirmación con el número de radicado
4. Puedes responder directamente desde Gmail

=======
# Configuración de EmailJS para Sistema PQRS - ASOREANC

## 📧 ¿Qué es EmailJS?

EmailJS es un servicio que permite enviar emails directamente desde el frontend sin necesidad de un servidor backend. Es perfecto para formularios de contacto y sistemas PQRS como el nuestro.

## 🚀 Pasos para Configurar EmailJS

### 1. Crear Cuenta en EmailJS

1. Ve a [https://www.emailjs.com/](https://www.emailjs.com/)
2. Haz clic en "Sign Up" y crea una cuenta gratuita
3. Verifica tu email

### 2. Configurar Servicio de Email (Gmail)

1. En el dashboard de EmailJS, ve a **"Email Services"**
2. Haz clic en **"Add New Service"**
3. Selecciona **"Gmail"**
4. Haz clic en **"Connect Account"**
5. Autoriza el acceso a tu cuenta de Gmail
6. **Anota el SERVICE ID** que se genera (ej: `service_abc123`)

### 3. Crear Template de Email

1. Ve a **"Email Templates"**
2. Haz clic en **"Create New Template"**
3. Configura el template así:

**Subject:**
```
Nueva PQRS {{pqrs_type}} - {{pqrs_id}} - ASOREANC
```

**Body:**
```
NUEVA PQRS RECIBIDA - ASOREANC
================================

Número de Radicado: {{pqrs_id}}
Fecha: {{pqrs_date}}
Tipo: {{pqrs_type}}

DATOS DEL SOLICITANTE:
----------------------
Nombre: {{from_name}}
Email: {{from_email}}
Teléfono: {{from_phone}}

SOLICITUD:
----------
Asunto: {{pqrs_subject}}

Mensaje:
{{pqrs_message}}

================================
Este mensaje fue enviado desde el sistema PQRS de ASOREANC
Para responder, contacta directamente al solicitante: {{from_email}}
```

4. Guarda el template y **anota el TEMPLATE ID** (ej: `template_xyz789`)

### 4. Obtener Public Key

1. Ve a **"Account"** > **"General"**
2. Copia tu **"Public Key"** (ej: `user_abcdef123456`)

### 5. Configurar el Archivo emailjs-config.js

Abre el archivo `emailjs-config.js` y reemplaza los valores:

```javascript
const EMAILJS_CONFIG = {
  serviceID: 'service_abc123',        // Tu Service ID real
  templateID: 'template_xyz789',      // Tu Template ID real  
  publicKey: 'user_abcdef123456',     // Tu Public Key real
  destinationEmail: 'tu-email@gmail.com'  // Email donde quieres recibir las PQRS
};
```

### 6. Probar el Sistema

1. Abre la página PQRS en tu navegador
2. Llena el formulario de prueba
3. Envía una PQRS de prueba
4. Verifica que llegue el email a tu Gmail

## 🔧 Límites del Plan Gratuito

- **200 emails por mes** (más que suficiente para la mayoría de casos)
- Si necesitas más, puedes upgrader a un plan pago

## 🛠️ Solución de Problemas

### El email no llega:
1. Verifica que los IDs en `emailjs-config.js` sean correctos
2. Revisa la consola del navegador para errores
3. Verifica que el template tenga todas las variables correctas
4. Revisa la carpeta de spam en Gmail

### Error de CORS:
- EmailJS maneja automáticamente CORS, no debería haber problemas

### Error de autenticación:
- Verifica que el Public Key sea correcto
- Asegúrate de que el servicio de Gmail esté activo

## 📱 Características del Sistema

✅ **Funcional**: Los emails llegan realmente a Gmail  
✅ **Seguro**: No expone credenciales sensibles  
✅ **Gratuito**: Hasta 200 emails/mes  
✅ **Fácil**: No requiere backend  
✅ **Profesional**: Emails con formato limpio  
✅ **Rastreable**: Cada PQRS tiene un número único  

## 🎯 Resultado Final

Una vez configurado, cuando alguien envíe una PQRS:

1. Se genera un número de radicado único
2. Se envía un email profesional a tu Gmail
3. El usuario recibe confirmación con el número de radicado
4. Puedes responder directamente desde Gmail

>>>>>>> 080a31b35b9318db3359bb0b268f1bbd26fe2b0d
¡El sistema estará completamente funcional y profesional!
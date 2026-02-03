# 🚀 Configuración de Maqukan RDP Automático

## ⚡ Quick Start (5 minutos)

### 1️⃣ Obtener Auth Key de Tailscale
1. Ve a: https://login.tailscale.com/admin/settings/keys
2. Haz clic en "Generate auth key..."
3. Marca: ✅ Reusable
4. Marca: ✅ Expiration: 90 days
5. Copia la clave generada

### 2️⃣ Agregar Secret a GitHub
1. Ve a tu repo: https://github.com/fresquitaawita890-blip/Maqukan
2. Settings → Secrets and variables → Actions
3. Click "New repository secret"
4. **Name:** `TAILSCALE_AUTH_KEY`
5. **Value:** Pega la clave de Tailscale
6. Click "Add secret"

### 3️⃣ Ejecutar el Workflow
1. Ve a la pestaña "Actions"
2. Selecciona "RDP Automático"
3. Click "Run workflow"
4. ¡Espera a que termine! (5-10 minutos)

### 4️⃣ Conectarte
Cuando el workflow termine, verás en los logs:
```
╔════════════════════════════════════════════════╗
║       🔐 RDP ACCESO CONFIGURADO ✅             ║
╠════════════════════════════════════════════════╣
║ Dirección: 100.x.x.x
║ Usuario:   RDP
║ Contraseña: ABC123!@#...
║ Puerto:    3389
```

**Usa estos datos en tu cliente RDP**

---

## 📋 ¿Qué hace el workflow?

✅ Configura RDP en Windows  
✅ Crea usuario automático con contraseña segura  
✅ Instala Tailscale  
✅ Conecta a tu red privada  
✅ Mantiene la sesión por 6 horas  
✅ Se ejecuta automáticamente cada 6 horas  

---

## 🔧 Solución de problemas

**❌ Workflow falla con "TAILSCALE_AUTH_KEY no configurado"**
- Asegúrate de crear el secret en GitHub
- Verifica el nombre exacto: `TAILSCALE_AUTH_KEY`

**❌ No puedo conectar al RDP**
- Verifica que Tailscale esté conectado en tu PC
- Intenta con la IP completa: `100.x.x.x:3389`
- Reinicia tu cliente RDP

**❌ El workflow tarda mucho**
- Es normal: instala Tailscale (3-5 min), configura RDP (2-3 min)
- Total: 6-10 minutos aprox.

---

## 📱 Clientes RDP Recomendados

**Windows:** Conexión a Escritorio Remoto (incluido)  
**Mac:** Microsoft Remote Desktop (App Store)  
**Linux:** Remmina o xfreerdp  
**Web:** https://clientrdp.com  

---

**¡Hecho! 🎉 Disfruta tu máquina virtual accesible 24/7**

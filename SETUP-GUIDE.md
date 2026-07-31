# 📦 Guía Completa de Instalación y GitHub

## Parte 1: Preparar el Proyecto Localmente

### Paso 1.1: Crear Carpeta Local

```bash
# Crear carpeta del proyecto
mkdir clasificacion-leads-vip
cd clasificacion-leads-vip

# Inicializar git
git init
```

### Paso 1.2: Crear Estructura de Carpetas

```bash
# Copiar esta estructura:
mkdir -p docs frontend architecture config examples resources

# Crear archivos
touch README.md
touch .gitignore
touch LICENSE
```

### Paso 1.3: Copiar Archivos

**Copiar estos archivos a sus carpetas respectivas:**

```
clasificacion-leads-vip/
├── README.md                    ← Copiar README.md principal
├── .gitignore                   ← Copiar .gitignore
├── LICENSE                      ← Crear LICENSE (MIT)
│
├── docs/
│   ├── ENTREGA-FINAL-COMPLETA.md
│   ├── PROYECTO-DESDE-CERO.md
│   ├── NOTION-ESTRUCTURA.md
│   └── N8N-ARQUITECTURA.md
│
├── frontend/
│   └── FORMULARIO-LEADS.html
│
├── architecture/
│   └── DIAGRAMA-ARQUITECTURA.html
│
├── config/
│   ├── webhook-config.json.example
│   └── notion-fields.json
│
├── examples/
│   ├── webhook-payload.json
│   └── gemini-response.json
│
└── resources/
    ├── SETUP-GUIDE.md
    └── TROUBLESHOOTING.md
```

---

## Parte 2: Preparar GitHub

### Paso 2.1: Crear Repositorio GitHub

1. **Ir a https://github.com/new**
2. **Nombre:** `clasificacion-leads-vip`
3. **Descripción:** "Ecosistema de Automatización IA - Clasificación de Leads"
4. **Público:** ✅ (para portafolio)
5. **NO inicializar** con README (ya lo tenemos)
6. **Crear repositorio**

### Paso 2.2: Conectar Local con GitHub

```bash
# En tu carpeta local:
cd clasificacion-leads-vip

# Agregar remoto
git remote add origin https://github.com/TU_USUARIO/clasificacion-leads-vip.git

# Verificar
git remote -v
```

---

## Parte 3: Subir Archivos a GitHub

### Paso 3.1: Primer Commit

```bash
# Agregar todos los archivos
git add .

# Ver qué se va a subir
git status

# Hacer commit
git commit -m "Initial commit: Proyecto Clasificación de Leads VIP"

# Subir a GitHub (rama main)
git branch -M main
git push -u origin main
```

### Paso 3.2: Verificar en GitHub

1. Ir a https://github.com/TU_USUARIO/clasificacion-leads-vip
2. Verificar que todos los archivos estén
3. Ver el README.md render automáticamente

---

## Parte 4: Organizar Documentación

### Paso 4.1: Crear Carpeta docs/

**En `docs/` crear estos archivos:**

#### `docs/ENTREGA-FINAL-COMPLETA.md`
```
[Copiar contenido de ENTREGA-FINAL-COMPLETA.md]
```

#### `docs/PROYECTO-DESDE-CERO.md`
```
[Copiar contenido de PROYECTO-DESDE-CERO.md]
```

#### `docs/NOTION-ESTRUCTURA.md`
```
[Copiar contenido de NOTION-ESTRUCTURA-LEADS-VIP.md]
```

#### `docs/N8N-ARQUITECTURA.md`
```
[Copiar contenido de N8N-ARQUITECTURA-COMPLETA-LEADS-VIP.md]
```

### Paso 4.2: Crear Carpeta frontend/

**En `frontend/` crear:**

#### `frontend/FORMULARIO-LEADS.html`
```
[Copiar contenido de FORMULARIO-LEADS.html]
```

#### `frontend/index.html`
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clasificación de Leads - Proyecto IA</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            text-align: center;
        }
        h1 { color: #667eea; }
        a { 
            display: inline-block;
            margin: 10px;
            padding: 10px 20px;
            background: #667eea;
            color: white;
            text-decoration: none;
            border-radius: 5px;
        }
        a:hover { background: #764ba2; }
    </style>
</head>
<body>
    <h1>🤖 Clasificación Automática de Leads VIP</h1>
    <p>Ecosistema de Automatización IA Completo</p>
    
    <h2>Ir al Formulario:</h2>
    <a href="FORMULARIO-LEADS.html">📋 Llenar Solicitud</a>
    
    <h2>Documentación:</h2>
    <a href="../docs/ENTREGA-FINAL-COMPLETA.md">📖 Entrega Final</a>
    <a href="../docs/PROYECTO-DESDE-CERO.md">📐 Especificación</a>
    
    <h2>GitHub:</h2>
    <a href="https://github.com/tu-usuario/clasificacion-leads-vip">🔗 Ver Repositorio</a>
</body>
</html>
```

### Paso 4.3: Crear Ejemplos

#### `examples/webhook-payload.json`
```json
{
  "nombre": "Juan García",
  "email": "juan@empresa.com",
  "empresa": "Tech Solutions Inc",
  "tamaño_empleados": 750,
  "descripcion": "Necesitamos automatizar nuestros procesos de ventas",
  "presupuesto": 50000
}
```

#### `examples/gemini-response.json`
```json
{
  "clasificacion": "VIP",
  "confianza": 92,
  "resumen": "Empresa grande (750 empleados), presupuesto alto, urgencia expresada"
}
```

---

## Parte 5: Crear Archivo LICENSE

### Opción A: MIT License (Recomendado)

```bash
# Crear LICENSE en raíz
cat > LICENSE << 'EOF'
MIT License

Copyright (c) 2026 [Tu Nombre]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
EOF
```

---

## Parte 6: Subir a GitHub (Paso a Paso)

### Comando Final Completo:

```bash
# 1. Estar en la carpeta
cd clasificacion-leads-vip

# 2. Agregar todos los archivos
git add .

# 3. Ver estado
git status

# 4. Hacer commit
git commit -m "Add complete project structure and documentation"

# 5. Subir
git push origin main

# ✅ ¡LISTO!
```

---

## Parte 7: Verificar en GitHub

### Checklist Final:

- [ ] README.md aparece en la raíz
- [ ] Carpeta `/docs` con 4 archivos
- [ ] Carpeta `/frontend` con HTML
- [ ] Carpeta `/examples` con JSONs
- [ ] Archivo LICENSE
- [ ] .gitignore configurado
- [ ] Todos los archivos sin credenciales

---

## Parte 8: Personalizar GitHub (Opcional pero Recomendado)

### 8.1: Agregar Topics

1. Ir a Settings → About
2. Agregar topics:
   - `automation`
   - `ai`
   - `n8n`
   - `notion`
   - `gemini`
   - `lead-management`

### 8.2: Crear GitHub Pages (Opcional)

1. Settings → Pages
2. Source: main branch / root
3. Publicar en: `https://tu-usuario.github.io/clasificacion-leads-vip`

---

## Parte 9: Mantener el Repositorio

### Actualizar después de cambios:

```bash
# Hacer cambios en archivos

# Agregar cambios
git add .

# Commit
git commit -m "Update: [descripción del cambio]"

# Push
git push origin main
```

### Crear Release (Opcional):

```bash
# En GitHub
1. Ir a Releases
2. Click "Create a new release"
3. Tag: v1.0.0
4. Title: "Version 1.0 - Initial Release"
5. Publish
```

---

## Comandos Git Útiles

```bash
# Ver historial
git log --oneline

# Ver rama actual
git branch

# Ver cambios pendientes
git status

# Descartar cambios
git checkout -- archivo.txt

# Deshacer último commit (sin perder cambios)
git reset --soft HEAD~1

# Ver remoto
git remote -v
```

---

## Estructura Final en GitHub

```
tu-usuario/clasificacion-leads-vip/
├── 📄 README.md
├── 📄 LICENSE
├── 📄 .gitignore
├── 📁 docs/
│   ├── ENTREGA-FINAL-COMPLETA.md
│   ├── PROYECTO-DESDE-CERO.md
│   ├── NOTION-ESTRUCTURA.md
│   └── N8N-ARQUITECTURA.md
├── 📁 frontend/
│   ├── FORMULARIO-LEADS.html
│   └── index.html
├── 📁 architecture/
│   └── DIAGRAMA-ARQUITECTURA.html
├── 📁 examples/
│   ├── webhook-payload.json
│   └── gemini-response.json
└── 📁 resources/
    ├── SETUP-GUIDE.md
    └── TROUBLESHOOTING.md
```

---

## ✅ Checklist Final

- [ ] Carpeta local creada
- [ ] Git inicializado
- [ ] Estructura de carpetas lista
- [ ] Archivos copiados a carpetas
- [ ] Repositorio GitHub creado
- [ ] Remoto conectado
- [ ] Primer commit hecho
- [ ] Push a GitHub exitoso
- [ ] Verificado en GitHub.com
- [ ] README.md visible
- [ ] LICENSE agregado
- [ ] .gitignore correcto

---

**¡LISTO PARA PRESENTAR!** 🎉

Tu proyecto está en GitHub listo para portafolio, entrega o compartir con otros.

GitHub URL: `https://github.com/TU_USUARIO/clasificacion-leads-vip`

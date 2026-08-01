# 📊 Guía: Crear Shared View Público en Notion (Dashboard)

## ¿Qué es una Shared View?

Una **Shared View** es una vista pública compartible de tu base de datos Notion que:
- ✅ No requiere contraseña para acceder
- ✅ Se actualiza automáticamente cada 5 minutos
- ✅ Muestra datos en tiempo real
- ✅ Es perfecta como dashboard

---

## PASO 1: Crear la Vista en Notion

### 1.1 Abre tu base de datos "Clasificación de Leads"

En Notion:
1. Ve a tu base de datos
2. Verás la tabla con todos los campos

### 1.2 Crear una nueva vista

1. Haz clic en **"+ Add a view"** (arriba a la derecha)
2. Selecciona **"Table"** (o "Gallery" si lo prefieres)
3. Nombre: **"Dashboard Público"**

### 1.3 Configurar la vista

**Filtros:**
```
Mostrar solo leads PROCESADOS:

1. Haz clic en "Filter"
2. Agregar filtro:
   Field: Estado
   Condition: is
   Value: CONTACTADO
```

**Columnas visibles:**
```
Mostrar solo las importantes:

Nombre → ✅
Email → ✅
Empresa → ✅
Tamaño_Empleados → ✅
Clasificación → ✅
Confianza → ✅
Resumen_Análisis → ✅
Timestamp_Email → ✅

Ocultar:
- ID (chequear ❌)
- Descripción (❌)
- Presupuesto (❌)
```

**Ordenamiento:**
```
1. Haz clic en "Sort"
2. Ordenar por: Timestamp_Email (Newest first)
```

**Agrupamiento (opcional pero bonito):**
```
1. Haz clic en "Group"
2. Agrupar por: Clasificación (VIP, NORMAL, SPAM)
```

---

## PASO 2: Hacer la Vista Pública

### 2.1 Haz clic en "Share"

En la vista que creaste:
1. Arriba a la derecha → **"Share"** (botón azul)
2. Se abrirá un diálogo

### 2.2 Configurar permisos

```
Opción 1: Share to web
├─ Haz clic en "Share to web"
└─ Togglear: Permitir copiar, acceso público

Opción 2: Generar link
├─ Copy link
└─ Compartir URL (no requiere login)
```

### 2.3 Obtener URL pública

1. Copia el link que aparece
2. Será algo como: `https://www.notion.so/xxxxx?v=xxxxx`
3. **GUARDA ESTA URL** - la necesitas para documentación

---

## PASO 3: Personalizar el Dashboard

### 3.1 Agregar métricas (usando Notion Database Stats)

Si Notion lo permite, agrega:

```
Total de Leads:
- Fórmula: COUNT() de todos los registros

VIP Count:
- Fórmula: COUNT(IF(Clasificación = "VIP"))

Tasa de precisión:
- Fórmula: (VIP Count / Total) × 100
```

### 3.2 Agregar propiedades calculadas

En la tabla, agrega columnas calculadas:

```
Status Badge:
- Si Clasificación = VIP → 🟢 VIP
- Si Clasificación = NORMAL → 🟡 NORMAL
- Si Clasificación = SPAM → 🔴 SPAM

Confianza Badge:
- Si Confianza > 90 → ✅ Alta
- Si Confianza 70-90 → ⚠️ Media
- Si Confianza < 70 → ❌ Baja
```

---

## PASO 4: Integrar con Documentación GitHub

### En tu README.md de GitHub:

```markdown
## 📊 Dashboard Público

Ver datos en tiempo real:

[![Notion Dashboard](https://img.shields.io/badge/Dashboard-Notion-blue?style=flat-square)](PEGA_URL_AQUI)

Enlace compartido: [Ver Clasificaciones en Vivo](PEGA_URL_AQUI)

**Actualización:** Cada 5 minutos
**Acceso:** Público, sin contraseña
**Datos:** Solo leads procesados
```

---

## PASO 5: Verificar Funcionamiento

### Checklist:

- [ ] Link abierto sin login
- [ ] Muestra solo datos CONTACTADO
- [ ] Filtros funcionan
- [ ] Se actualiza automáticamente
- [ ] Columnas visibles están correctas
- [ ] Ordenamiento por fecha reciente

---

## PASO 6: Documentar en GitHub

### Crear archivo: `/resources/DASHBOARD-LINK.md`

```markdown
# 📊 Dashboard Público en Vivo

## Acceso

Haz clic aquí para ver el dashboard en tiempo real:

🔗 [DASHBOARD PÚBLICO NOTION](PEGA_URL_AQUI)

## Características

✅ Datos en tiempo real (actualiza cada 5 minutos)
✅ Acceso público sin contraseña
✅ Muestra solo leads clasificados
✅ Ordenado por fecha reciente
✅ Agrupado por clasificación (VIP, NORMAL, SPAM)

## Columnas Mostradas

| Columna | Descripción |
|---------|------------|
| Nombre | Nombre del contacto |
| Empresa | Empresa del lead |
| Tamaño | Número de empleados |
| Clasificación | VIP / NORMAL / SPAM |
| Confianza | % de confianza IA (0-100) |
| Análisis | Resumen de clasificación |
| Fecha | Cuándo se procesó |

## Filtros Aplicados

- Estado = CONTACTADO (solo procesados)
- Timestamp_Email = no vacío (con email enviado)

## Actualizaciones

- Última actualización: [Auto]
- Frecuencia: Cada 5 minutos
- Total registros: [Dinámico]
```

---

## TROUBLESHOOTING

### Problema: "Link no funciona"

**Solución:**
1. Abre Notion
2. Ve a Share
3. Verifica "Share to web" está ON
4. Copia link de nuevo

### Problema: "Ver datos privados"

**Solución:**
1. Vuelve a verificar filtros
2. Asegúrate de ocultar campos sensibles
3. Re-compartir con permisos limitados

### Problema: "No se actualiza"

**Solución:**
1. Notion actualiza cada ~5 min
2. Actualiza la página (Ctrl+R o Cmd+R)
3. Si persiste, contactar soporte Notion

---

## EJEMPLO DE URL FINAL

Tu dashboard será accesible en:

```
https://www.notion.so/xxxxx?v=xxxxx&pvs=4
```

Compártelo en:
- README.md del proyecto
- LinkedIn
- Portafolio
- Email a profesor/cliente

---

## ✅ CHECKLIST FINAL

- [ ] Vista creada en Notion
- [ ] Filtros configurados
- [ ] Columnas visibles correctas
- [ ] Compartida públicamente
- [ ] URL copiada
- [ ] Documentación en GitHub
- [ ] Verificado funcionamiento
- [ ] Compartido en README

---

## INFORMACIÓN PARA DOCUMENTACIÓN

**Cuando tengas el link público, actualiza:**

En `/resources/DASHBOARD-LINK.md`:
```
🔗 [Dashboard Público Notion](PEGA_TU_URL_AQUI)
```

En `README.md`:
```
## 📊 Dashboard

Ver datos en tiempo real: [Notion Dashboard](PEGA_TU_URL_AQUI)
```

---

**¡Listo! Tu dashboard público está operativo** 🎉

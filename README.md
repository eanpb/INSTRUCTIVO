# 📚 Instructivo para Crear Contenido - EducaLegal

## Introducción

Este documento explica cómo crear contenido (definiciones, preguntas y temas de teoría) para la plataforma EducaLegal usando archivos Excel que luego serán importados al sistema.

---

## 🎓 Estructura de Ramos (Malla UANDES)

El contenido está organizado por **ramos universitarios**. Cada item debe tener un `courseId` que indica a qué ramo pertenece:

### Derecho Civil
| courseId | Ramo | Contenido típico |
|----------|------|------------------|
| `civil-1` | Civil I - Introducción y Personas | Teoría de la ley, personas, atributos de la personalidad |
| `civil-2` | Civil II - Bienes | Bienes, derechos reales, posesión, modos de adquirir |
| `civil-3` | Civil III - Obligaciones | Teoría de las obligaciones, efectos, modos de extinguir |
| `civil-4` | Civil IV - Fuentes | Contratos (teoría general), cuasicontratos, responsabilidad |
| `civil-5` | Civil V - Contratos | Compraventa, arrendamiento, mandato, sociedad |
| `civil-6` | Civil VI - Familia | Matrimonio, filiación, régimen patrimonial |
| `civil-7` | Civil VII - Sucesiones | Sucesión, testamentos, asignaciones |

### Derecho Procesal
| courseId | Ramo | Contenido típico |
|----------|------|------------------|
| `procesal-1` | Procesal I - Orgánico | Jurisdicción, competencia, organización tribunales |
| `procesal-2` | Procesal II - Civil I | Juicio ordinario, prueba, medidas precautorias |
| `procesal-3` | Procesal III - Civil II | Recursos, juicios especiales, cumplimiento |
| `procesal-4` | Procesal IV - Penal | Proceso penal, etapas, recursos en materia penal |

### Derecho Penal
| courseId | Ramo | Contenido típico |
|----------|------|------------------|
| `penal-1` | Penal I - Parte General | Teoría del delito, tipicidad, antijuridicidad, culpabilidad |
| `penal-2` | Penal II - Parte Especial | Delitos específicos (homicidio, hurto, robo, etc.) |

---

## 📋 Estructura General

El contenido se organiza en **3 tipos principales**:

1. **Definiciones** - Términos jurídicos con su definición
2. **Preguntas** - Preguntas de alternativas tipo examen
3. **Teoría** - Temas extensos para estudio

Cada tipo tiene su propia hoja de Excel.

---

## 🗂️ Archivo Excel Requerido

Crear un archivo Excel llamado `contenido_educalegal.xlsx` con **3 hojas**:

1. `Definiciones`
2. `Preguntas`
3. `Teoria`

---

## 📖 Hoja 1: DEFINICIONES

### Columnas Obligatorias:

| Columna | Nombre | Descripción | Ejemplo |
|---------|--------|-------------|---------|
| A | **categoria** | penal, civil, procesal | `penal` |
| B | **courseId** | ID del ramo (ver tabla arriba) | `penal-1` |
| C | **termino** | El concepto a definir | `Dolo` |
| D | **definicion** | Definición completa y clara | `Conocimiento y voluntad de realizar...` |

### Columnas Opcionales:

| Columna | Nombre | Descripción | Ejemplo |
|---------|--------|-------------|---------|
| E | **subcategoria** | Subdivisión del tema | `Teoría del Delito` |
| F | **dificultad** | basico, intermedio, avanzado | `basico` |
| G | **ejemplos** | Ejemplos separados por `\|` | `Matar con premeditación\|Robar sabiendo que es ajeno` |
| H | **terminos_relacionados** | Términos relacionados separados por `\|` | `Culpa\|Cuasidelito\|Tipicidad` |
| I | **articulo_legal** | Referencia legal | `Art. 44 CC` |

### Ejemplo de fila:

```
categoria: penal
courseId: penal-1
termino: Dolo Eventual
definicion: El autor no desea directamente el resultado, pero lo acepta como posible consecuencia de su actuar
subcategoria: Teoría del Delito
dificultad: intermedio
ejemplos: Conducir a excesiva velocidad aceptando que puede causar un accidente
terminos_relacionados: Dolo Directo|Culpa Consciente
articulo_legal: Art. 2 CP
```

---

## ❓ Hoja 2: PREGUNTAS

### Columnas Obligatorias:

| Columna | Nombre | Descripción | Ejemplo |
|---------|--------|-------------|---------|
| A | **categoria** | penal, civil, procesal | `civil` |
| B | **courseId** | ID del ramo (ver tabla arriba) | `civil-2` |
| C | **pregunta** | Texto de la pregunta | `¿Cuál es el plazo de prescripción...?` |
| D | **opcion_a** | Primera alternativa | `5 años` |
| E | **opcion_b** | Segunda alternativa | `10 años` |
| F | **opcion_c** | Tercera alternativa | `2 años` |
| G | **opcion_d** | Cuarta alternativa | `4 años` |
| H | **respuesta_correcta** | Letra de la respuesta (A, B, C o D) | `B` |
| I | **explicacion** | Por qué esa es la respuesta correcta | `Según el Art. 2515 del CC...` |
| J | **dificultad** | basico, intermedio, avanzado | `intermedio` |

### Columnas Opcionales:

| Columna | Nombre | Descripción | Ejemplo |
|---------|--------|-------------|---------|
| K | **subcategoria** | Tema específico | `Prescripción` |
| L | **articulo** | Artículo de ley | `Art. 2508 CC` |
| M | **fuente** | De dónde salió la pregunta | `Manual de Derecho Civil` |

### Ejemplo de fila:

```
categoria: civil
courseId: civil-2
pregunta: ¿Cuál es el plazo de prescripción adquisitiva ordinaria de bienes inmuebles?
opcion_a: 2 años
opcion_b: 5 años
opcion_c: 10 años
opcion_d: 15 años
respuesta_correcta: B
explicacion: Según el Art. 2508 del Código Civil, la prescripción ordinaria de bienes raíces es de 5 años
dificultad: intermedio
subcategoria: Prescripción Adquisitiva
```

---

## 📝 Hoja 3: TEORIA

### Columnas Obligatorias:

| Columna | Nombre | Descripción | Ejemplo |
|---------|--------|-------------|---------|
| A | **categoria** | penal, civil, procesal | `procesal` |
| B | **courseId** | ID del ramo (ver tabla arriba) | `procesal-3` |
| C | **titulo** | Título del tema | `Los Recursos Procesales` |
| D | **contenido** | Texto completo del tema (puede ser largo) | Ver formato abajo |

### Columnas Opcionales:

| Columna | Nombre | Descripción | Ejemplo |
|---------|--------|-------------|---------|
| E | **subtemas** | Lista de subtemas separados por `\|` | `Reposición\|Apelación\|Casación` |

### Formato del Contenido:

El contenido puede usar formato Markdown simple:

```markdown
# Título Principal

## Subtítulo

### Sub-subtítulo

Texto normal del párrafo.

**Texto en negrita** para destacar conceptos importantes.

- Punto 1 de una lista
- Punto 2 de una lista
- Punto 3 de una lista

1. Lista numerada
2. Segundo elemento
3. Tercer elemento
```

---

## 🏷️ Categorías Disponibles

### Categorías Actuales:
- `penal` - Derecho Penal
- `civil` - Derecho Civil
- `procesal` - Derecho Procesal

### Categorías que pueden agregar:
- `constitucional` - Derecho Constitucional
- `laboral` - Derecho Laboral
- `administrativo` - Derecho Administrativo
- `tributario` - Derecho Tributario
- `comercial` - Derecho Comercial
- `internacional` - Derecho Internacional
- `ambiental` - Derecho Ambiental
- `familia` - Derecho de Familia
- *(o cualquier otra que necesiten)*

---

## ⚠️ Reglas Importantes

### Para las Definiciones:
1. ✅ Usar lenguaje claro y preciso
2. ✅ Incluir referencias legales cuando sea posible
3. ✅ Evitar definiciones demasiado largas (máx. 300 palabras)
4. ❌ No usar abreviaciones sin explicar
5. ❌ No copiar textualmente de libros (parafrasear)

### Para las Preguntas:
1. ✅ Las 4 alternativas deben ser plausibles
2. ✅ Solo UNA respuesta correcta
3. ✅ La explicación debe ser educativa
4. ❌ Evitar preguntas con "todas las anteriores" o "ninguna de las anteriores"
5. ❌ Evitar alternativas evidentemente incorrectas

### Para la Teoría:
1. ✅ Organizar con títulos y subtítulos claros
2. ✅ Usar listas para enumeraciones
3. ✅ Incluir artículos de ley cuando corresponda
4. ❌ No exceder 3000 palabras por tema
5. ❌ Evitar párrafos muy largos (máx. 5-6 líneas)

---

## 📤 Entrega del Archivo

1. Nombrar el archivo: `contenido_[categoria]_[fecha].xlsx`
   - Ejemplo: `contenido_civil_20240115.xlsx`

2. Verificar que:
   - Las hojas tengan los nombres correctos
   - No haya celdas vacías en columnas obligatorias
   - Las categorías estén escritas en minúsculas
   - Las respuestas correctas sean A, B, C o D (mayúsculas)

3. Enviar a: [definir email o sistema de entrega]

---

## 🔧 Proceso de Importación

Una vez recibido el archivo:

1. Se verificará el formato y contenido
2. Se convertirá automáticamente al formato del sistema
3. Se publicará en la plataforma
4. Se notificará cuando esté disponible

**Tiempo estimado**: 24-48 horas hábiles

---

## 💡 Tips para Crear Buen Contenido

### Definiciones Efectivas:
- Comenzar con "Es..." o "Se refiere a..."
- Incluir el género próximo y la diferencia específica
- Dar ejemplos concretos cuando sea posible

### Preguntas Efectivas:
- Formular como caso práctico cuando sea posible
- Hacer que el estudiante aplique conocimiento, no solo memorice
- Incluir artículos de ley en la explicación

### Teoría Efectiva:
- Comenzar con un concepto general
- Ir de lo simple a lo complejo
- Incluir esquemas mentales (usando listas)
- Terminar con puntos clave para recordar

---

## 📞 Contacto para Dudas

Si tienen preguntas sobre el formato o el contenido:
- Email: [definir]
- Teléfono: [definir]

---

*Última actualización: Diciembre 2024*

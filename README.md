# Visual Database Designer

Una herramienta visual e interactiva para diseñar bases de datos relacionales. Permite crear tablas, definir campos, establecer relaciones y exportar el diseño resultante a SQL compatible con MySQL.

## 🎯 Objetivos

**Objetivo Principal:**  
Facilitar la comprensión y explicación del diseño de bases de datos mediante una interfaz gráfica clara e intuitiva.

**Objetivos Secundarios:**
- Servir como apoyo para estudiantes y docentes en el aprendizaje de modelado de datos
- Ayudar a desarrolladores a modelar una base de datos antes de escribir código
- Construir una base sólida para un producto potencialmente monetizable
- Promover buenas prácticas de diseño de bases de datos

## 📅 El Desafío: One Commit Per Day

Este proyecto forma parte de un desafío personal de **un commit significativo por día durante enero de 2026**. El objetivo es construir un producto real, educativo y bien diseñado, documentando cada decisión técnica y de producto.

### Reglas del Desafío
- ✅ Al menos un commit significativo por día
- ✅ Los commits pueden incluir código, documentación, decisiones de arquitectura, UX o refactors
- ✅ Cada commit debe representar una mejora clara o una decisión justificada

Este enfoque permite:
- Mantener un ritmo constante de desarrollo
- Documentar el proceso de construcción del producto
- Crear contenido educativo sobre el desarrollo de software
- Demostrar cómo se construye un producto real desde cero

## ⚡ Funcionalidades del Sistema

### Funcionalidades Principales
- **Creación visual de tablas**: Interfaz drag-and-drop para crear y organizar tablas en un canvas
- **Definición de campos**: Nombre, tipo de dato y restricciones (NOT NULL, UNIQUE, etc.)
- **Claves primarias y foráneas**: Soporte completo para definir relaciones entre tablas
- **Visualización de relaciones**: Conexiones visuales entre tablas con indicadores de cardinalidad
- **Canvas interactivo**: Arrastrar, mover y organizar tablas libremente
- **Toolbar**: Acciones globales (crear, eliminar, exportar)
- **Sidebar contextual**: Editar propiedades de tablas, campos y relaciones
- **Validaciones**: Nombres duplicados, tipos inválidos, relaciones incorrectas
- **Exportación SQL**: Genera SQL compatible con MySQL
- **Sistema de notificaciones**: Feedback visual mediante toasts

### Componentes de UI
```
Canvas
├── TableNode
│   ├── FieldRow
│   └── AnchorPoint
├── RelationEdge
└── ContextMenu

Toolbar
Sidebar
StatusBar
Toast / Notification
```

## 🏗️ Arquitectura General

### Frontend
- **Editor visual**: Basado en componentes modulares y reutilizables
- **Estado global**: Manejo centralizado del modelo de base de datos
- **Storybook**: Desarrollo y documentación de componentes UI

### Backend
- **API básica**: Preparada para soporte futuro
- **Persistencia**: Diseñada para exportación y almacenamiento
- **Prioridad**: No prioritaria en las primeras etapas (enfoque frontend-first)

### Modelo Interno
```typescript
Database
├── Table[]
│   ├── name: string
│   ├── position: { x, y }
│   └── fields: Field[]
│       ├── name: string
│       ├── type: DataType
│       ├── isPrimaryKey: boolean
│       ├── isForeignKey: boolean
│       └── constraints: Constraint[]
└── relations: Relation[]
    ├── sourceTable: string
    ├── targetTable: string
    ├── sourceField: string
    ├── targetField: string
    └── type: RelationType
```

## 🎯 Alcance y Limitaciones

### ✅ Incluye
- Modelado visual de bases de datos relacionales
- Export SQL básico compatible con MySQL
- Validaciones simples del modelo
- Enfoque educativo y didáctico
- Interfaz intuitiva y moderna

### ❌ No Incluye (en la primera versión)
- Optimización avanzada de queries
- Migraciones automáticas
- Soporte multi-motor (PostgreSQL, SQLite, etc.)
- Autenticación de usuarios
- Reverse engineering desde bases de datos existentes

## 📊 Cómo Seguir el Progreso

Puedes seguir el desarrollo día a día a través de:
- **Commits**: Cada commit incluye una descripción clara de lo implementado
- **Issues**: Decisiones técnicas y features planificadas
- **Documentación**: Actualizaciones constantes del README y docs

## 🛠️ Stack Tecnológico

_(Por definir en los primeros commits)_

Consideraciones iniciales:
- **Frontend**: React/Vue + TypeScript
- **UI Library**: Componentes personalizados o biblioteca ligera
- **State Management**: Context API / Zustand / Redux
- **Canvas**: HTML5 Canvas / SVG / Biblioteca especializada
- **Build Tool**: Vite
- **Testing**: Vitest + Testing Library
- **Docs**: Storybook

## 📝 Licencia

_(Por definir)_

---

**Inicio del desafío:** 1 de enero de 2026  
**Creado por:** Marcos GP  
**Propósito:** Educativo, técnico y de crecimiento personal

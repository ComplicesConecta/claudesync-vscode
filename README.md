# ComplicesConecta

## 📋 Descripción del Proyecto

ComplicesConecta es una plataforma que integra aplicaciones web y móvil utilizando una arquitectura monorepo con PNPM workspaces. El proyecto está estructurado para compartir código entre diferentes aplicaciones y mantener una organización clara de los componentes.

## 🚀 Estructura del Proyecto

```
complicesconecta/
├── apps/
│   ├── mobile/       # Aplicación móvil (React Native)
│   └── web/          # Aplicación web (Next.js)
├── packages/
│   ├── eslint-config/ # Configuración compartida de ESLint
│   ├── shared/        # Código compartido entre aplicaciones
│   └── tsconfig/     # Configuración compartida de TypeScript
├── docs/             # Documentación del proyecto
└── scripts/          # Scripts de utilidad
```

## 🔧 Requisitos Previos

- Node.js (versión recomendada: 18.x o superior)
- PNPM (versión 10.x o superior)

## 🛠️ Instalación

1. Clonar el repositorio:

```bash
git clone <url-del-repositorio>
cd complicesconecta
```

2. Instalar dependencias:

```bash
pnpm install --ignore-scripts
```

> **Nota**: Utilizamos `--ignore-scripts` para evitar errores durante la instalación inicial. El script postinstall intenta construir todos los paquetes, pero puede fallar si hay dependencias entre ellos.

## 🖥️ Ejecución de la Aplicación Web

```bash
pnpm run dev:web
```

Esto iniciará el servidor de desarrollo de Next.js en http://localhost:3000.

## 📱 Ejecución de la Aplicación Móvil

```bash
pnpm run dev:mobile
```

Para ejecutar en plataformas específicas:

```bash
pnpm --filter @complicesconecta/mobile run android  # Para Android
pnpm --filter @complicesconecta/mobile run ios      # Para iOS
pnpm --filter @complicesconecta/mobile run web      # Para versión web
```

## 🧪 Pruebas

```bash
pnpm run test        # Ejecutar todas las pruebas
pnpm run test:web    # Ejecutar pruebas de la aplicación web
pnpm run test:mobile # Ejecutar pruebas de la aplicación móvil
```

## 🧹 Lint y Formateo

```bash
pnpm run lint      # Ejecutar lint en todos los proyectos
pnpm run lint:fix  # Corregir problemas de lint automáticamente
```

## 🏗️ Construcción

```bash
pnpm run build      # Construir todos los proyectos
pnpm run build:web  # Construir solo la aplicación web
pnpm run build:mobile # Construir solo la aplicación móvil
```

## 🧼 Limpieza

```bash
pnpm run clean         # Limpiar archivos de construcción
pnpm run clean:modules # Eliminar node_modules
pnpm run clean:cache   # Limpiar caché de PNPM
```

## 📝 Estado Actual del Proyecto

El proyecto está en desarrollo activo. La aplicación web está funcionando y puede ser accedida en http://localhost:3000 después de iniciar el servidor de desarrollo.

Actualmente hay algunos problemas con el script de construcción del paquete `shared` que deben ser resueltos.

## 📚 Documentación Adicional

Para más información, consulta los archivos en el directorio `docs/`:

- [Análisis del Proyecto](docs/ANALISIS_PROYECTO.md)
- [Guía Completa](docs/GUIA_COMPLETA_COMPLICESCONECTA.md)
- [Estructura](docs/ESTRUCTURACC.md)

## 🤝 Contribución

Consulta [CONTRIBUTING.md](docs/CONTRIBUTING.md) para obtener información sobre cómo contribuir al proyecto.

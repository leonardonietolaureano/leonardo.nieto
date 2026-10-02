# Entrenador Xpad

Simulador web interactivo para capacitación práctica del equipo Xpad.

## Objetivo

Recrear el flujo operativo del dispositivo para que un alumno pueda practicar:

- Encendido del equipo.
- Validación del cliente.
- Carga de programación.
- Checklist.
- Ejecución de pruebas individuales.
- Resultados correctos/incorrectos.
- Reinicio de la práctica.
- Modos de capacitación: guiado, práctica libre y evaluación.

## Requisitos

- Node.js 18 o superior.
- VS Code recomendado.

## Instalación

```bash
npm install
```

## Ejecutar

```bash
npm run dev
```

Vite mostrará una dirección similar a:

```text
http://localhost:5173
```

## Generar versión para producción

```bash
npm run build
```

La aplicación generada estará en:

```text
dist/
```

## Estructura

```text
xpad-training-simulator/
├── index.html
├── package.json
├── vite.config.js
├── README.md
└── src/
    ├── main.jsx
    ├── App.jsx
    ├── styles.css
    ├── data/
    │   └── checklist.js
    ├── components/
    │   ├── XpadDevice.jsx
    │   ├── Checklist.jsx
    │   ├── Modal.jsx
    │   └── TrainingPanel.jsx
    └── simulator/
        └── simulator.js
```

## Cómo ampliar el simulador

El punto principal de configuración es:

```text
src/data/checklist.js
```

Ahí se pueden agregar o modificar las pruebas del Xpad.

Cada prueba puede tener:

- nombre;
- descripción;
- instrucciones;
- tipo de interacción;
- resultado esperado;
- pasos;
- comportamiento ante Sí/No;
- mensaje de error;
- mensaje de éxito.

La lógica de transición se concentra en:

```text
src/simulator/simulator.js
```

De esta forma, la pantalla visual no necesita contener toda la lógica del proceso.

## Siguiente etapa recomendada

Para una versión de capacitación real se puede agregar:

1. Reproducción de sonidos del Xpad.
2. Cronómetro por ejercicio.
3. Errores intencionales.
4. Modo evaluación.
5. Calificación.
6. Registro de intentos.
7. Usuarios/alumnos.
8. Panel de instructor.
9. Base de datos.
10. Administración de versiones del checklist.

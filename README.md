# KLA
# KLA - Kernel Linux Application

[![License: Personal](https://img.shields.io/badge/License-Personal-red.svg)](LICENSE)
[![Status: En Desarrollo](https://img.shields.io/badge/Status-En%20Desarrollo-orange.svg)](https://github.com/tu-usuario/KLA)
[![Linux](https://img.shields.io/badge/Linux-5.4+-blue.svg)](https://www.kernel.org/)
[![OpenGL](https://img.shields.io/badge/OpenGL-4.0+-green.svg)](https://www.opengl.org/)

**KLA** es una aplicación C monolítica que proporciona una **visualización 3D en tiempo real del kernel de Linux**. Permite "ver por dentro" el sistema operativo con un sistema de zooms interactivo, representando procesos, memoria, I/O, interrupciones y otros eventos del kernel como elementos visuales interactivos en un espacio 3D.

## ¿Qué hace KLA?

KLA transforma los eventos internos del kernel de Linux en una experiencia visual inmersiva:

| Elemento del Kernel | Representación 3D | Información Mostrada |
|-------------------|---------------------|-------------------|
| **Procesos** | Esferas flotantes con colores | Prioridad, uso de CPU, estado |
| **Memoria** | Bloques flotantes que se llenan/vacían | Uso de RAM, page faults, caches |
| **Scheduler** | Flujos de energía entre procesos y CPUs | Distribución de carga, context switches |
| **I/O** | Tuberías por donde fluyen partículas | Disco, red, velocidad de transferencia |
| **Interrupciones** | Rayos de luz que parpadean | Dispositivos, frecuencia, tipos |
| **CPU/GPU** | Cilindros rotatorios | Carga por core, temperatura, throttling |
| **Latencia** | Esferas rojas que crecen | Bottlenecks, performance hotspots |

## Sistema de Zooms Interactivo

KLA implementa un sistema de zooms que permite explorar diferentes niveles de detalle:

- **Zoom 1**: Vista general del sistema (modelo 3D del equipo, stats flotantes)
- **Zoom 2**: Hardware y procesos (paneles interactivos, mapas de memoria)
- **Zoom 3**: Kernel profundo (drivers, syscalls, schedulers en tiempo real)

## Estado del Proyecto

** KLA está actualmente en desarrollo **

### Plan de Desarrollo (20 semanas)

- **Fase 1** (Semanas 1-4): Fundación eBPF + OpenGL ✅ *En progreso*
- **Fase 2** (Semanas 5-8): Memoria + Scheduler 🔄 *Próximamente*
- **Fase 3** (Semanas 9-12): I/O + Interrupciones ⏳ *Planificado*
- **Fase 4** (Semanas 13-16): CPU/GPU + Efectos Avanzados ⏳ *Planificado*
- **Fase 5** (Semanas 17-20): Sistema de Zooms + Polish ⏳ *Planificado*

### Próximas Características

- [ ] Visualización de procesos como esferas 3D
- [ ] Sistema de memoria con bloques flotantes
- [ ] Tuberías de I/O con partículas
- [ ] Interrupciones como rayos de luz
- [ ] CPUs rotatorios con efectos de temperatura
- [ ] Sistema de zooms completo
- [ ] Efectos visuales avanzados (bloom, glow)

## Stack Tecnológico

### Backend (C)
- **eBPF**: Captura de eventos del kernel en tiempo real
- **OpenGL 4.6**: Renderizado 3D avanzado
- **GLFW**: Gestión de ventanas y contexto
- **libbpf**: Programas eBPF y maps
- **pthreads**: Threading para captura de datos
- **liburing**: I/O asíncrono eficiente

### Frontend (OpenGL)
- **Vertex/Fragment Shaders**: Transformaciones y efectos de luz
- **Compute Shaders**: Cálculos paralelos
- **Instanced Rendering**: Eficiencia para muchos objetos
- **Particle Systems**: Flujo de datos I/O
- **Post-processing**: Efectos visuales avanzados

## ¿Para Quién es KLA?

### Educativo
- **Estudiantes** de sistemas operativos
- **Profesores** que enseñan kernel internals
- **Investigadores** en performance de sistemas

### Profesional
- **Sysadmins** que necesitan debugging avanzado
- **DevOps engineers** para monitoreo de sistemas
- **Kernel developers** para debugging de drivers
- **Performance engineers** para optimización

### Entusiastas
- **Linux enthusiasts** que quieren entender su sistema
- **Gamers** que quieren optimizar performance
- **Hackers** que exploran sistemas operativos

## Requisitos del Sistema

### Mínimos
- Linux kernel 5.4+ (para eBPF features)
- OpenGL 4.0+
- 4GB RAM
- GPU compatible con OpenGL

### Recomendados
- Linux kernel 5.15+
- OpenGL 4.6+
- 8GB+ RAM
- GPU dedicada
- Monitor de alta resolución

## Instalación

> **Nota**: KLA aún está en desarrollo. La instalación no estará disponible hasta completar la Fase 1.

### Dependencias

```bash
# Ubuntu/Debian
sudo apt install libbpf-dev libelf-dev libglfw3-dev libgl1-mesa-dev

# Arch Linux
sudo pacman -S libbpf glfw-x11 mesa

# Fedora
sudo dnf install libbpf-devel elfutils-libelf-devel glfw-devel mesa-libGL-devel
```

### Compilación (cuando esté disponible)

```bash
git clone https://github.com/tu-usuario/KLA.git
cd KLA
make
sudo ./kla
```

## Arquitectura

```
KLA/
├── src/
│   ├── ebpf/           # Programas eBPF (.c)
│   ├── kernel/         # Interacción con kernel
│   ├── render/         # OpenGL rendering
│   ├── data/           # Estructuras de datos
│   ├── ui/             # Interfaz de usuario
│   └── main.c          # Punto de entrada
├── include/            # Headers
├── build/              # Archivos compilados
├── assets/             # Texturas, modelos 3D
└── docs/               # Documentación
```

## Uso y Licencia

KLA está disponible para uso personal y educativo únicamente.

### Condiciones de Uso

- **Uso Personal**: Puedes ejecutar KLA en tus sistemas personales
- **Aprendizaje**: Puedes estudiar el código fuente para aprender
- **Visualización**: Puedes compartir capturas de pantalla o videos del software funcionando

### Restricciones

- **No Modificación**: No se permite modificar el código fuente
- **No Redistribución**: No se permite distribuir o vender el software
- **No Uso Comercial**: No se permite usar KLA en productos o servicios comerciales

---

**KLA - Kernel Linux Application**  


---



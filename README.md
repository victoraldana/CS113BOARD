# CS113BOARD – Placa de Control

Placa de control diseñada en **KiCad** para el proyecto de *Laboratorio de Electrónica 3* (Universidad, 2026). Usa un módulo **ESP32-S3-DevKitC** como controlador, con una etapa de *latches* (74LS75), un decodificador (74LS138) y *drivers* de potencia (ULN2803A) que se conectan a la carga por conectores JST.

![Vista 3D de la placa](PLACA%20DE%20CONTROL.png)

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `PLACA DE CONTROL.kicad_pro` | Archivo de proyecto de KiCad |
| `PLACA DE CONTROL.kicad_sch` | Esquemático |
| `PLACA DE CONTROL.kicad_pcb` | Diseño del PCB (espesor 1.6 mm) |
| `PLACA DE CONTROL.kicad_prl` | Preferencias locales del proyecto |
| `PLACA DE CONTROL.png` | Render 3D de la placa |
| `la.pdf` | Documentación de apoyo |
| `LICENSE` | Licencia del proyecto |

## Componentes principales

| Cantidad | Componente | Encapsulado | Función |
|:-:|---|---|---|
| 1 | ESP32-S3-DevKitC | 2 × `PinSocket_1x22_P2.54mm` | Microcontrolador |
| 1 | 74LS138 | DIP-16 | Decodificador 3 a 8 |
| 6 | 74LS75 | DIP-16 | Latches de 4 bits |
| 6 | ULN2803A | DIP-18 | Driver de 8 canales (Darlington) |
| 6 | Conector 1×06 | JST XH B6B-XH-A (2.50 mm) | Conexión a la carga |
| 1 | Conector 1×04 | JST EH B4B-EH-A (2.50 mm) | Conexión auxiliar |

Alimentación: **+5 V** (lógica) y **+12 V** (etapa de potencia), con **GND** común.

## Cómo abrir el proyecto

1. Instala [KiCad](https://www.kicad.org/download/). El proyecto usa el formato de la versión 8 o superior.
2. Clona el repositorio:
   ```bash
   git clone https://github.com/victoraldana/CS113BOARD.git
   ```
3. Abre `PLACA DE CONTROL.kicad_pro`.

## Fabricación

Desde el editor de PCB de KiCad:

1. `Archivo → Fabricación → Archivos Gerber` y `Archivos de taladrado`.
2. Comprueba las reglas con `Inspeccionar → Comprobador de reglas de diseño (DRC)`.
3. Envía los archivos generados al fabricante.

## Licencia

Distribuido bajo la licencia incluida en [LICENSE](LICENSE).

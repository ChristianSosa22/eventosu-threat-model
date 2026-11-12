# eventosu-threat-model

Modelado de amenazas de **EventosU**, un sitio web ficticio en fase de diseño donde la universidad publica eventos y los usuarios se inscriben, pagan y reciben una entrada QR. Es un ejercicio de diseño: no se ataca ningún sistema real.

## Integrantes

| Nombre | Carné | GitHub |
|---|---|---|
| _Nombre completo_ | _carné_ | [@ChristianSosa22](https://github.com/ChristianSosa22) |
| _Nombre completo_ | _carné_ | _usuario_ |

## Alcance

**Dentro del modelo:** sitio web (React en CDN), panel `/admin`, API (Node.js), PostgreSQL, bucket de objetos, App de Puerta, registros de auditoría y los flujos con Microsoft Entra ID, la pasarela de pagos y el servicio de correo.

**Fuera del modelo:** la seguridad interna de los tres servicios de terceros, los datos de tarjeta (los procesa la pasarela), la infraestructura del proveedor de nube, los dispositivos personales de los usuarios y la seguridad física del recinto.

El detalle, los activos y los supuestos están en la sección 2 del [informe](docs/informe.md).

## Estructura

```
eventosu-threat-model/
├── README.md             # integrantes, alcance y cómo abrir el modelo
├── model/eventosu.json   # modelo de Threat Dragon (DFD nivel 0 y nivel 1, 23 amenazas)
├── assets/               # capturas de los diagramas de Threat Dragon
├── docs/informe.md       # informe en borrador; se exporta a docs/informe.pdf al finalizar
└── docs/amenazas.csv     # tabla de amenazas
```

## Cómo abrir el modelo

1. Instalar [OWASP Threat Dragon](https://github.com/OWASP/threat-dragon/releases) 2.x (versión de escritorio) o usar la [versión web](https://www.threatdragon.com/).
2. En la pantalla inicial elegir **Open an existing threat model** (en la web: iniciar con *Local Session* y luego **Open an existing threat model**).
3. Seleccionar el archivo `model/eventosu.json` de este repositorio.
4. El modelo tiene dos diagramas:
   - **Nivel 0 - Contexto:** EventosU como un solo proceso y sus actores externos.
   - **Nivel 1 - Componentes:** todos los componentes del caso, cinco límites de confianza y las amenazas STRIDE. Los elementos con amenazas abiertas aparecen en rojo; al seleccionarlos se listan sus amenazas.

## Avance

| Actividad | Estado |
|---|---|
| 1. Alcance y activos | Hecho |
| 2. DFD en Threat Dragon | Hecho |
| 3. Identificación con STRIDE | Hecho: 23 amenazas |
| 4. Árbol de ataque | Hecho |
| 5. Priorización | Hecho |
| 6. Respuesta y trazabilidad | Hecho |

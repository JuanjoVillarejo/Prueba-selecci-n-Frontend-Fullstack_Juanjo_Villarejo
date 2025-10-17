# Prueba-seleccion-Frontend-Fullstack_Juanjo_Villarejo
"Proyecto - Prueba Frontend-Fullstack"
# Prueba selección Frontend/Fullstack — Entrega


## Qué incluye
Proyecto minimal que cumple los requisitos:
- Consume `data.yml` y sirve muestras progresivas basadas en la hora actual.
- Actualiza cada 5 segundos.
- Muestra el último valor recibido en una sección dedicada.
- Grafica intervalos por minuto (agrega muestras de 5s a buckets por minuto).
- Temperatura mostrada en °C. Energía mostrada en kWh (incremento por intervalo y suma por minuto).


## Supuestos documentados
- `data.yml` tiene dos series: `temperature` y `power`.
- Temperatura en el fichero es un entero interpretado como *valor en decenas de Kelvin* (p.ej. 2921 -> 292.1 K). Para convertir a °C uso: `value/10 - 273.15`.
- Potencia (`power.values[].value`) viene como string con unidad kW. Para convertir energía por intervalo a kWh: `energy_kwh = power_kW * (interval_seconds / 3600)`.


Si tus datos significan otra cosa ajusta las conversiones en `server.js`.


## Requisitos
- Node.js 18+ y npm.


## Instalación y ejecución
1. Sitúa `data.yml` en la raíz del proyecto (ya incluido en la entrega).
2. Instala dependencias:


```bash
npm install

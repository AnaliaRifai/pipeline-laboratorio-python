# Ejemplo de ejecución con datos sintéticos

> **100 % FICTICIO:** todos los nombres, números de muestra, fechas y resultados de esta carpeta son inventados para demostrar el código. **No provienen del laboratorio.**

## Archivos de entrada

- `informe_ficticio_A.xlsx`: informe de 2018 con encabezado desplazado y metadatos en una sola celda (2 muestras).
- `informe_ficticio_B.xlsx`: informe de 2018 con encabezado de dos filas y determinaciones DIVMS duplicadas (2 muestras).
- `consolidados_anuales_sinteticos/`: ocho consolidados creados directamente con datos ficticios (2019–2026, dos filas por año). **No fueron generados por los pipelines reales de esos años.**

## Salidas generadas al ejecutar el código publicado

- `consolidado_2018.xlsx`: **4 muestras ficticias** obtenidas ejecutando `scripts/pipeline_2018.py`.
- `log_consolidado_2018.xlsx`: avisos y controles del proceso de prueba.
- `consolidado_historico_2018_2026.xlsx`: **20 muestras ficticias** de **9 años**, obtenido ejecutando `scripts/pipeline_maestro_consolidado_historico_2018_2026.py`.
- `log_consolidado_historico_2018_2026.xlsx`: controles sobre el histórico ficticio.

| Indicador de esta demostración | Resultado ficticio |
|---|---:|
| Informes de entrada de 2018 | 2 |
| Muestras normalizadas de 2018 | 4 |
| Años integrados | 9 |
| Registros del histórico | 20 |
| Duplicados de muestras | 0 |
| Errores de lectura | 0 |

**Estos resultados no describen los datos reales del laboratorio y no deben usarse como métricas del proyecto real en el CV o LinkedIn.**

## Reproducir la prueba

1. Copiar los dos `informe_ficticio_*.xlsx` a `DATOS/ORIGINALES/2018/` en un clon del repositorio.
2. Instalar dependencias con `pip install -r requirements.txt` y ejecutar `python scripts/pipeline_2018.py`.
3. Copiar los ocho archivos de `consolidados_anuales_sinteticos/` a `DATOS/RESPALDOS/`, junto al `consolidado_2018.xlsx` recién generado.
4. Ejecutar `python scripts/pipeline_maestro_consolidado_historico_2018_2026.py`.
5. Comparar las salidas nuevas de `DATOS/RESPALDOS/` y `DATOS/PROCESADOS/` con los ejemplos de esta carpeta.

Las adaptaciones anuales internas de 2019–2026 **no se publican**. Esta es una demostración del pipeline base de 2018 y del consolidador histórico.

**No subir nunca la base real ni `config_privada.json` al repositorio.**

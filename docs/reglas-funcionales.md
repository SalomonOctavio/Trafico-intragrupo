# Reglas funcionales

## Compatibilidad / Segmento
- Aplica a **postpago y gestor**; excluye **cuenta control y prepago**.

## Flags y defaults (Fase 1 Gestor)
- Defaults a “ilimitado intra-grupo” en empresa/grupo/miembro (valores −1), manteniendo coherencia al crear nuevos grupos/perfiles.
- Marcado UDR desde BMP/mediación para identificar llamadas On-Net del grupo.

## Tasación y factura
- Llamadas intra-grupo/RUT **no consumen** bolsa y se facturan a **$0 con detalle**.

## Reportería
- Reporte por RUT/empresa con validadores (ej. consumo adicional sin agotar bucket; coherencia de agrupación).


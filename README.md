# Trafico Intra-Grupo / al RUT (TELCO, 2014)

Proyecto para habilitar **llamadas a $0** entre líneas que pertenezcan al **mismo RUT** (segmento empresa/gestor), sin descontar de la bolsa y **manteniendo visibilidad en factura** (costo cero). Fase 1 en Gestor (flags & mediación); Fase 2 por RUT transversal.

---

## 🎯 Objetivo
- Implementar **tráfico $0 intra-grupo** (mismo RUT) sin consumo de bolsa ni cargos.  
- Mantener **detalle en factura** con costo cero.  
- Proveer **reportería** de control y validación.

---

## ⚙️ Alcance funcional
**Fase 1 — Gestor (producto corporativo)**  
- Flags y defaults en Gestor (empresa/grupo/miembro) para no descontar bolsa intra-grupo.  
- Marcado/identificación en **mediación** (UDRs) y tasación para $0.  
- Reportes de consistencia y validadores.  

**Fase 2 — RUT transversal**  
- Asignación al RUT (pantalla/proceso).  
- Tasación $0 entre líneas del mismo RUT **independiente** de la cuenta de facturación.  
- Postpago/gestor (excluye cuenta control y prepago).

---

## 🧭 Decisiones clave
- **No descontar de la bolsa** cuando la llamada sea intra-grupo/RUT.  
- **Compatibilidad por plan/segmento**; defaults por configuración.  
- **Factura con detalle** y costo 0 (visibilidad conservada).

---

## 🔬 UAT y go-live
- Casos: intra-grupo $0, no consumo de bolsa, factura $0, rechazos/compatibilidad, reportería.  
- Evidencias por orden/caso de prueba (Gestor Fase 1, pruebas de descuento y pantallas).  

---

## 📈 Resultados (placeholders)
- **TTGL**: ⟨N⟩ semanas (Fase 1 + Fase 2).  
- **TTV**: ⟨N⟩ días (uso efectivo y conciliación).  
- Disminución de reclamos por cargos intra-grupo; **control** operativo vía reportería.

---

## 📚 Artefactos

📁 `/diagrams`  
- [`arquitectura-intragrupo.mmd`](./diagrams/arquitectura-intragrupo.mmd) — CRM/BSCS/OSB/Mediación (UDR) y factura.  
- [`flujo-fases.mmd`](./diagrams/flujo-fases.mmd) — Fase 1 (Gestor) y Fase 2 (RUT).

📁 `/docs`  
- [`bnd-resumen.md`](./docs/bnd-resumen.md) — Extracto de necesidades de negocio.  
- [`reglas-funcionales.md`](./docs/reglas-funcionales.md) — Flags, defaults y compatibilidades.  
- [`kpis.md`](./docs/kpis.md) — TTGL/TTV, deltas y validadores.

📁 `/uat`  
- [`plan-uat.md`](./uat/plan-uat.md) — escenarios y roles.  
- [`checklist-go-no-go.md`](./uat/checklist-go-no-go.md) — validaciones mínimas.

---

## 🔐 Nota
Caso **anonimizado** (TELCO). Se omiten nombres/cifras; se preservan reglas y decisiones funcionales.


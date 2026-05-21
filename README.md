# Element Construction SAS — Sistema de Gestión de APUs en Odoo

## Descripción
MVP desarrollado para ELEMENT CONSTRUCTION SAS como 
solución al problema de gestión centralizada de 
Análisis de Precios Unitarios (APUs). Implementado 
sobre Odoo Community como parte del curso de Sistemas 
de Información — Universidad EAFIT 2026.

## Integrantes
- Sara Castrillón Sánchez
- Juan Manuel Ramírez
- Samuel Daza Carvajal
- Nicolás Moreno López
- Mariana Hincapié Henao

## Problema que resuelve
ELEMENT CONSTRUCTION SAS no contaba con un sistema 
centralizado para gestionar y actualizar los precios 
de materiales e insumos (APUs). Esto generaba demoras 
de 2-3 días en la elaboración de cotizaciones y riesgo 
de errores por precios desactualizados.

## Solución implementada
Sistema ERP basado en Odoo con tres componentes:
1. Catálogo centralizado de materiales y APUs
2. Gestión automatizada de proveedores
3. Automatización del flujo de actualización de precios

## Tecnologías utilizadas
- Odoo Community (ERP)
- Google Forms (formulario de actualización de precios)
- Zapier (automatización Form → Odoo)
- Gmail (notificaciones automáticas)

## Historias de usuario implementadas

### HU1 — Catálogo centralizado de insumos
Catálogo de 15 materiales organizados en 4 categorías:
- Materiales de construcción
- Mano de obra
- Equipos y herramientas
- Subcontratistas

### HU2 — Gestión de proveedores
5 proveedores registrados y vinculados a sus productos 
con historial de precios y contacto directo desde Odoo.

### HU3 — Alertas de precios desactualizados
Filtro "Precios por actualizar" que identifica materiales 
sin actualización en más de 30 días.

### HU4 — Cotización automática con margen
Generación de cotizaciones para clientes con margen del 
30% calculado automáticamente sobre el costo vigente.

### HU5 — Actualización automática de precios
Flujo automatizado: proveedor recibe formulario mensual 
→ llena el precio → Zapier actualiza Odoo automáticamente.

## Flujo completo del sistema
1. Odoo detecta precios con más de 30 días sin actualizar
2. Zapier envía formulario automáticamente al proveedor
3. Proveedor llena Google Forms con precio actualizado
4. Zapier actualiza el costo en Odoo automáticamente
5. Odoo recalcula el precio de venta con margen del 30%
6. El equipo genera cotización con precios siempre vigentes
7. Al confirmar la orden se descuenta el inventario

## Acceso al sistema
- URL Odoo: https://element-constructions-sas.odoo.com/
- URL Formulario proveedores: https://docs.google.com/forms/d/e/1FAIpQLSe_wYBgPCIE6Z4YFcGfOAAAA89YrBq8RpYgNt0yZBsdah5gRQ/viewform
- URL Videotutorial: https://youtu.be/Ke2weWSo9hk

## Módulos de Odoo activados
- Inventario
- Compras
- Ventas
- Contactos

## Configuración inicial
1. Crear instancia en odoo.com/trial
2. Activar módulos: Inventario, Compras, Ventas y Contactos
3. Configurar moneda en COP
4. Crear categorías de productos
5. Cargar productos con costos
6. Registrar proveedores y vincularlos a productos
7. Configurar lista de precios con margen del 30%, 18%, etc.
8. Conectar Google Forms con Zapier
9. Activar envío mensual automático a proveedores

## Resultado
- Tiempo de cotización reducido de 2-3 días a menos de 4 horas
- 0 consultas manuales a proveedores para precios registrados
- Actualización automática mensual de precios
- Trazabilidad completa de inventario y ventas

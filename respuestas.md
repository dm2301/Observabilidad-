# Respuestas del Laboratorio de Observabilidad

**1. ¿Por qué necesitamos Loki además de Prometheus si ya tenemos `/metrics`?**

Por qué Prometheus se enfoca en el que recolectando datos numéricos y cuantitativos en tiempo real mientras que Loki se enfoca en el porque ya que recolecta texto estructurado e histórico 

**2. ¿Qué ventaja aporta que las fuentes de datos de Grafana estén aprovisionadas como código y no creadas a mano?**

Aporta ventajas como automatización y despliegue rápido, consistencia entre entornos además de controlar las versiones

**3. El panel "CPU contenedor" y el panel "CPU host" pueden mostrar valores muy distintos. ¿Por qué? ¿Cuál usarías para alertar sobre una aplicación concreta?**

El CPU host mide el consumo total de una maquina que aloja todo el sistema mientras que el CPU contenedor mide los recursos aislados que consume el proceso especifico 
El recomendable para usar sería el CPU contenedor si se requiere monitorear la salud del backend 

**4. ¿Qué diferencia hay entre el *evaluation interval* y el *pending period* de una alarma?**


Que el evaluation interval  seria la frecuencia con la que grafana ejecuta la consulta matemática en Prometheus mientras que el  pending period  es el tiempo de gracia que debe mantener la condición de fallo antes de activar la notificación oficial.
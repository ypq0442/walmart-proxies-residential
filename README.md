# Rotativa: IP nueva en cada petición
# HTTP/HTTPS -> puerto 823
http://usuario:clave@gw.dataimpulse.com:823

# SOCKS5 -> puerto 824
socks5://usuario:clave@gw.dataimpulse.com:824

# Sticky: mantiene la misma IP según el ID de sesión
http://usuario:clave_sesión-abc123@gw.dataimpulse.com:823

# Segmentación por país incluida en el precio base
http://usuario:clave_país-es@gw.dataimpulse.com:823


La autenticación se hace por usuario y contraseña o por lista blanca de IP, y puedes elegir método distinto por proyecto.

### Rotativa o sticky: la decisión que más afecta a tu tasa de éxito

Las sesiones rotativas cambian de IP con cada petición. Son lo que quieres para rastreo de volumen alto y para repartir peticiones repetidas entre muchas identidades.

Las sticky mantienen la misma IP ligada a un puerto durante un intervalo. En DataImpulse duran de 1 a 120 minutos, con 30 minutos por defecto si no especificas nada, y usan el rango de puertos 10000–20000. Son las que necesitas cuando hay login de por medio, carritos, formularios multi-paso o cualquier flujo donde el sitio espera continuidad. Hay que tener cuidado con dos detalles prácticos: en un login, nunca dejes que la IP cambie a mitad de sesión; y si automatizas con navegadores antidetect, alinea idioma y zona horaria del perfil con el país del proxy, o el fingerprint delata la incoherencia.

## Segmentación: dónde se te va el presupuesto si no miras

Aquí está la diferencia que casi ninguna landing de proveedor explica con claridad.

- **Nivel país:** incluido sin coste en todas las líneas. Es el único filtro "gratis" que necesitas para el 80% de proyectos.
- **Estado, ciudad, código postal, ASN:** en el residencial estándar se factura al doble de la tarifa por GB. Es decir, un proyecto de precios locales por ciudad con residencial a $1/GB en la práctica te cuesta $2/GB.
- **En centro de datos:** según la propia web del proveedor, estos filtros aparecen incluidos; si vas a basar el presupuesto en ello, confírmalo con soporte antes de comprar.
- **En residencial premium:** todos los filtros van incluidos sin recargo.

De ahí sale una regla simple: si tu segmentación va a ser por ciudad o ASN y trabajas en volumen, compara el coste del residencial premium contra el del residencial estándar con recargo antes de decidir. A veces el "caro" sale más barato.

## ¿Existen cupones de DataImpulse?

Es una búsqueda constante y la respuesta honesta es que no hay un código oficial que aplicar. Las páginas que recopilan cupones llegan a la misma conclusión: con $1/GB, tráfico que no caduca y sin suscripción, el descuento real no viene de un código, viene del volumen ($0,80/GB en el tramo de 1 TB).

Dicho esto, un aviso práctico: desconfía de cualquier "cupón" de terceros que te pida datos de tarjeta o registro en una web intermedia. El precio ya está publicado en el sitio del proveedor y no hay pasos extra legítimos para conseguirlo.

👉 [Comprobar el precio vigente y los paquetes disponibles](https://bit.ly/dataimPulse)

## Cuántos GB necesitas antes de escalar

Esta es la parte aritmética que casi todos hacen mal. Como referencia aproximada: una página HTML sin imágenes suele moverse entre 100 KB y 1 MB, así que 5 GB dan para decenas de miles de páginas si desactivas la carga de recursos pesados. En cuanto metes imágenes o navegas con navegador real, el consumo se multiplica y ese mismo paquete se agota en una tarde de pruebas.

Mi recomendación de secuencia: empieza con el paquete mínimo, valida en tus propios objetivos (no en los del vendedor), calcula tu coste por registro útil y solo entonces sube de tramo. El pool de 90 millones de IP no sirve de nada si tu caso concreto no pasa el anti-bot de tu sitio objetivo.

## Qué dicen las reseñas de terceros

Hay pocas reseñas independientes largas, y eso ya es información. La que más se cita es la de TechRadar, que destaca el punto de entrada de $1/GB, el tamaño del pool residencial y las sesiones rotativas y sticky; en sus pruebas señala tasas de éxito altas en tareas de scraping.

El análisis de AIMultiple es más útil porque también lista los contras: los descuentos por volumen de móvil y residencial premium se activan a partir de 1 TB, y la segmentación avanzada (estado, ciudad, ZIP, ASN) se factura al doble en los planes residenciales estándar. Coincide con lo que ves en la web del proveedor.

También circulan menciones a una política de reembolso de 7 días para las primeras compras y a una puntuación de 4,8/5 en G2. Si ese derecho de devolución condiciona tu decisión, confírmalo directamente con soporte antes de pagar: es el tipo de condición que cambia sin aviso.

## Errores típicos al comprar proxy residencial

- **Comprar residencial para todo.** Si el objetivo no filtra por reputación de IP, el centro de datos cuesta la mitad ($0,50/GB frente a $1/GB).
- **Elegir suscripción cuando tu uso es irregular.** Es el error más caro: pagas GB que se reinician y desaparecen.
- **Ignorar el recargo por segmentación.** Un proyecto por ciudad con residencial estándar puede costar el doble de lo que dice la portada.
- **Asumir que 1 GB rinde igual en todos los casos.** Depende de imágenes, navegador, reintentos y peso del sitio objetivo.
- **Dar por hecho que un pool grande equivale a éxito.** Lo que importa es el origen de las IP y el historial de abuso que arrastran.

Sobre ese último punto, DataImpulse insiste en que su pool es de origen propio y con consentimiento del usuario, no revendido, y publica una tasa de éxito del 99,51%. Es una afirmación de parte, así que trátala como lo que es: un dato del vendedor, útil como punto de comparación, no como prueba.

## Merece la pena o no

Para uso intermitente y para probar varios mercados, el modelo de pago por uso con tráfico sin caducidad encaja mejor que casi cualquier suscripción. Puedes empezar con $5, medir y escalar solo si los números salen. Ese es el argumento fuerte, y no depende de marketing.

Lo que no te van a contar: a partir de 1 TB el residencial estándar baja a $0,80/GB, así que si tu volumen es alto, compara con proveedores que en ese rango ya están en $0,50/GB o menos. Y si tu caso depende de filtros por ciudad o ASN, haz la cuenta con el recargo del doble, o mira directamente la línea premium.

👉 [Empezar con el paquete de 5 GB y validar tu coste real](https://bit.ly/dataimPulse)

## Preguntas frecuentes

**¿Hace falta suscripción?** No. Se compra tráfico y se consume cuando quieras; los GB no caducan.

**¿Qué protocolos soporta?** HTTP, HTTPS y SOCKS5.

**¿Cuánto dura una sesión sticky?** Entre 1 y 120 minutos, con 30 minutos por defecto si no se especifica intervalo.

**¿Puedo elegir ciudad o código postal?** Sí, pero en el residencial estándar esos filtros se facturan al doble de la tarifa por GB. En premium van incluidos.

**¿Cuántos GB necesito para empezar?** Con uso irregular, el paquete mínimo basta para validar. Una página HTML ronda los 100 KB–1 MB; con navegador e imágenes reales, el consumo sube muy rápido.

**¿Es legal usar proxies residenciales?** Depende de para qué. Acceder a datos públicos con proxies no es ilegal en sí, pero las condiciones de cada sitio y la normativa local marcan los límites. Es una decisión tuya, no del proveedor.

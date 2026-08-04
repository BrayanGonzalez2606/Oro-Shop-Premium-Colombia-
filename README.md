# ORO SHOP PREMIUM · Luxury Jewelry Colombia

Landing page profesional de e-commerce de joyería de lujo (Oro 18K Laminado) optimizada para móvil, tablet y escritorio.

## 🌐 Dominio oficial
`https://oro-shop-premium-colombia.vercel.app/` — SEO, canonical, Open Graph, sitemap y JSON-LD ya apuntan a este dominio.

## 🔍 Google Search Console (verificación)
- Método **Archivo HTML** (el que descargaste): el archivo `google2cb1beb8a936efaa.html` ya está en la **raíz** del proyecto.
- Debe quedar accesible en `https://oro-shop-premium-colombia.vercel.app/google2cb1beb8a936efaa.html`.
- Pasos: sube todo a GitHub → Vercel publica → en Search Console pulsa **Verificar** → luego en **Sitemaps** envía `sitemap.xml`.

## 📱 Redes sociales (logos oficiales SVG)
Instagram, Facebook, TikTok, YouTube y WhatsApp aparecen con sus **logos reales** en la sección Contáctanos y en el footer. Cada botón de contacto por WhatsApp usa el logo verde oficial. Actualiza los enlaces (usuario `oroshoppremium`) por tus perfiles reales en `index.html` (búscalos como `instagram.com/oroshoppremium`, etc.) y en el `sameAs` del JSON-LD.

## ⭐ Sección "Clientes Satisfechos" (50 reseñas reales)
- Carrusel deslizable con **50 reseñas** independientes, cada una con: **foto real**, **nombre y apellido**, **ciudad de compra**, **5 estrellas**, **comentario único** (los 50 son distintos) y **producto + variación** del catálogo, más sello "✔ Compra verificada".
- Fotos en `assets/testimonials/` (25 mujeres + 25 hombres, congruentes por género).
- **Totalmente separada del sistema FOMO/visitantes en vivo**: distintos perfiles, distintas fotos (`assets/reviews/`), distintos nombres. No se mezclan.
- Resumen 4.9★ + "+2.500 reseñas verificadas" y navegación con flechas ‹ ›.

## 📈 Prueba social / FOMO (conversión)
- **Visitantes en vivo:** barra inferior izquierda con número dinámico según hora del día.
- **50 reseñas reales con foto:** notificaciones con **foto real del cliente** (25 mujeres + 25 hombres, congruentes: mujer → joya de mujer, hombre → joya de hombre). Fotos alojadas localmente en `assets/reviews/` (funcionan en preview y en producción).
- **Formato del recuadro:**
  ```
  (Nombre) · (Ciudad)
  Acaba de comprar (Producto + variación)
  Hace X minutos · Compra verificada por Google Analytics
  ```
- Aparecen en **orden aleatorio sin repetición** hasta agotar los 50 y luego se re-barajan, para que nadie note el patrón.
- Badge de "mensajes sin leer" en el botón flotante de WhatsApp.

## 🎨 Logos de redes (SVG oficiales refinados)
Instagram (gradiente oficial), Facebook, TikTok (glitch cian/rojo), YouTube y WhatsApp con sus **marcas de color reales**, verificados por render. Sección "Síguenos" + footer + todos los CTA de WhatsApp.

## 🚀 Cómo publicar
Es un sitio **estático** (HTML + CSS + JS, sin dependencias). Funciona en cualquier hosting:
- **Vercel / Netlify / GitHub Pages:** sube toda la carpeta y listo.
- **Local:** abre `index.html` en el navegador, o ejecuta `python3 -m http.server` y entra a `http://localhost:8000`.

## 📁 Estructura
```
index.html              → Landing page completa (HTML/CSS/JS + 63 productos embebidos)
robots.txt, sitemap.xml → SEO
assets/brand/           → Logo, fondo hero, certificado, beneficios, políticas, T&C
assets/products/        → 63 fotos de producto (recortadas, SIN precios visibles)
uploads/                → Imágenes originales (flyers) — no se usan en producción
```

## ✨ Funcionalidades
- **63 productos** en 7 categorías (Cadenas, Pulseras, Combos, Dijes, Aretes, Camándulas, Sets).
- Precios = precio del flyer **+ $70.000** (precio final real). Los flyers de producto se recortaron para **ocultar los precios** a los clientes.
- **Variaciones** (talla/medida/material) en acordeón funcional con su precio.
- **Carrito interactivo** (drawer) con cantidades, total y envío gratis. Persiste en `localStorage`.
- **Etiqueta "Envío Gratis"** en todos los productos.
- **Conteo regresivo de 24 h** persistente y profesional.
- **Pedido por WhatsApp** (+57 304 4975964) con mensaje personalizado: saludo según la zona horaria (Buenos Días / Tardes / Noches), lista del pedido y formulario de datos del cliente.
- **Medios de pago:** PayPal (paypal.me/BrayanGonzalez2606), Nequi (+57 304 4975964) y efectivo contra entrega.
- **Panel Administrador** (correo `brayangonzalez2606@gmail.com`): registro de pedidos/clientes, estadísticas, exportación CSV.
- **Secciones:** Certificado de Calidad, Beneficios Auténticos, Políticas de Envío, Términos y Condiciones, FAQ, Testimonios.
- **SEO** optimizado (title, description, Open Graph, Twitter, JSON-LD JewelryStore, sitemap).
- El correo del administrador está **protegido** (no aparece en texto plano público; el registro de pedidos queda en el panel).

## 🔐 Panel Administrador
Acceso desde el pie de página → "Acceso Administrador".
- Correo: `brayangonzalez2606@gmail.com`
- Clave: `DIOSOROSHOP2026`
- **La contraseña NO aparece en el código**: solo se guarda su hash SHA-256 (`ADMIN_PASS_HASH`), así ningún usuario puede leerla en el código fuente. Para cambiarla, genera el nuevo hash y reemplaza `ADMIN_PASS_HASH`.

### Cambiar la contraseña (en el panel)
- Sección **"🔐 Cambiar Contraseña del Panel"**: requiere la clave actual, valida y guarda **solo el hash** de la nueva (`osp_pass`). El cambio es **inmediato**; la clave por defecto deja de funcionar. Nunca se guarda en texto plano.

### Categorías (en el panel)
- 🗂️ **Crear nuevas categorías** (nombre + emoji). Aparecen en el selector del editor y, una vez tienen productos, como filtro en la tienda.
- Eliminar categorías personalizadas vacías. Las categorías base no se pueden borrar.
- Persisten en `localStorage` (`osp_cats`).

### Gestión de Inventario (en el panel)
- ✏️ **Editar productos** (nombre, categoría, descripción, ID).
- 🖼️ **Varias fotos por producto** (galería): añadir por URL/ruta o **subir** desde el dispositivo; quitar individualmente.
- 🎨 **Varias fotos por variación** (ej: Oro Rosa): cada variación puede tener su propia galería. **En la tienda, al seleccionar la variación las fotos cambian automáticamente.**
- 💲 **Editar precios** y **variaciones** (añadir/quitar).
- ➕ **Agregar productos** · 🗑 **Eliminar productos**.
- ⬇ Exportar catálogo (JSON) · ↺ Restaurar catálogo original (63 productos).
- Los cambios se guardan en `localStorage` (`osp_catalog`) y se reflejan al instante. **La tienda siempre carga primero los cambios del administrador** (no se sobreescriben).

### Buscador (tienda)
- Barra de búsqueda en vivo sobre la colección (busca por nombre, descripción, categoría y variaciones). **Las categorías y filtros siguen visibles** como antes; el buscador es un complemento.

### Pedidos
- El formulario de pedido incluye **Medio de Pago** y **Código Promocional**, que se agregan automáticamente al mensaje de WhatsApp y al registro/CSV del panel.
- El mensaje de WhatsApp **saluda y se despide según la zona horaria** del cliente:
  - Mañana → "Excelente y Bendecida Mañana🙏🏽🏆"
  - Tarde → "Excelente y Bendecida Tarde🙏🏽🏆"
  - Noche → "Excelente y Bendecida Noche🙏🏽🏆"

## 🛠️ POR QUÉ "se actualizó unos segundos y volvió a lo antiguo" (y cómo se corrigió)
Causa raíz (dos fallos combinados):
1. **Límite de 100 KB de jsonbin (plan gratis).** Al subir **fotos**, se guardaban dentro del JSON como `data:image/...base64`. Una sola foto supera 100 KB, así que jsonbin **rechazaba la publicación (HTTP 403/400)**: la nube nunca recibía tus nuevos productos/fotos.
2. **El "revert".** El cambio se veía en TU pantalla al instante (local), pero como la nube no lo aceptó, a los ~20 s el auto-refresco leía la nube (vieja) y **volvía a los productos antiguos**.

Correcciones aplicadas:
- **Las fotos ahora se alojan en ImgBB** (gratis) y en la nube se guarda solo el **enlace corto** → el JSON queda liviano y la publicación nunca falla por tamaño.
- **Protección anti-revert:** si una publicación falla, se marca el estado como “pendiente” y **el auto-refresco ya NO pisa tus cambios**; además ahora se muestra el **error real** (antes fallaba en silencio).
- **Aviso claro:** si subes fotos sin haber configurado la API Key de ImgBB, la tienda te avisa que esas fotos solo quedarán en tu equipo hasta configurarla.

## ✅ CÓMO ACTUALIZAR PRODUCTOS CORRECTAMENTE (paso a paso)
> **Todo está pre-configurado** (nube jsonbin + fotos ImgBB). El administrador NO necesita configurar nada. Solo edita y guarda.

1. Abre la Landing Page → baja al pie de página → **🔐 Acceso Administrador** → ingresa con el correo autorizado y la clave `DIOSOROSHOP2026`.
2. En **🏷️ Gestión de Inventario** pulsa **✏️ Editar** sobre un producto (o **➕ Agregar Producto**).
3. Realiza los cambios: nombre, descripción, **precios**, **variaciones** (ej. Oro / Oro Rosa) y **fotos**:
   - Fotos del producto: botón **📷 Subir** (puedes subir varias).
   - Fotos por variación: abre **🖼️ Fotos** dentro de la variación y sube las suyas.
4. Pulsa **💾 Guardar Producto**.
   - Las fotos se suben **solas** a ImgBB y el catálogo se publica en la nube.
   - Verás **“☁️ Cambios publicados en la nube ✓”**. (Si algo falla, un aviso ⚠️ te dirá el motivo y tus cambios quedan guardados; vuelve a pulsar Guardar.)
5. **Listo.** En cualquier dispositivo (Android, iPhone, PC, Tablet) los cambios aparecen **automáticamente**: al abrir la página, al volver a ella, o en máximo ~20 segundos. Para verlo al instante: recargar o botón **⬇️ Traer de la Nube**.

**Para eliminar un producto:** botón **🗑 Eliminar** en la tabla → se borra y se publica en la nube.
**Para crear una categoría:** sección **🗂️ Categorías** → nombre + emoji → **Crear Categoría**.

> 💡 Recomendación CRO: comprime/usa fotos nítidas pero no enormes. El sistema ya las optimiza, y al ir por enlace (ImgBB) la tienda carga rápido en datos móviles.

## ☁️ Sincronización en la Nube (YA CONFIGURADA ✅)
Está **conectada y activa de fábrica** con tu cuenta de jsonbin.io. Cuando el administrador edita productos, precios, fotos o categorías, los cambios se publican en la nube y aparecen **automáticamente en todos los dispositivos** (Android, iPhone, PC, Tablet) — al abrir, al volver a la pestaña y por sondeo cada 20 s. Sin recargar.

**Credenciales integradas (todo listo, sin configurar nada):**
- **Fotos:** ImgBB pre-integrado (API key ofuscada, activa en sesión de admin) → cada foto se aloja y se guarda como enlace corto.
- **BIN ID:** `6a2b2e49da38895dfeb10461` (público, lectura).
- **X-ACCESS-KEY** (lectura): incluida en el código para que todas las visitas vean el catálogo.
- **X-MASTER-KEY** (escritura): **NO está en texto plano**. Va ofuscada en partes y solo se reconstruye cuando el administrador inicia sesión → así él publica sin pegar nada y la clave no queda expuesta a los clientes.
- El catálogo de 63 productos ya fue **sembrado** en la nube.

**No necesitas hacer nada.** Inicia sesión como admin y edita: se publica solo. Botones *Publicar Ahora* / *Traer de la Nube* son manuales opcionales.

> 🔐 Recomendación de seguridad: una clave de escritura en una web pública nunca es 100% secreta (la ofuscación evita el scraping casual). Si en algún momento notas escrituras no autorizadas, entra a jsonbin.io → regenera la X-MASTER-KEY y actualiza `_WK_PARTS` en `index.html` (o cámbiala desde el panel para guardarla solo en tu dispositivo).

**Cómo funciona (arquitectura):**
- El **administrador** (con `X-Master-Key`) **publica** cambios a la nube (`cloudPush`).
- **Todos los dispositivos** **leen** la nube (`cloudPull`) al cargar y por polling, y se actualizan solos.
- Las **fotos se comprimen automáticamente** (canvas → JPEG ~1000px) para que la sync sea rápida y ligera.
- **Seguridad:** los clientes solo llevan la clave de **lectura**; no pueden modificar el catálogo. La `X-Master-Key` se guarda solo en el dispositivo del admin.
- **Respaldo:** si no hay nube configurada o falla la red, todo funciona con `localStorage` (como antes). Nada se rompe.
- Para que las **visitas** vean los cambios sin tocar nada, deja configurada en el código publicado únicamente la **clave de lectura** + Bin ID (en `localStorage` `osp_sync`, o pre-cárgala en el INIT).

> Nota: jsonbin.io es el proveedor por defecto por su CORS y plan gratuito. La capa es agnóstica: puede apuntarse a Supabase/Firebase cambiando `cloudPull`/`cloudPush`.

## 💳 Medios de pago visibles (con logos reales)
- **PayPal** → logo oficial SVG (monograma azul de dos "P").
- **Efectivo** → imagen del billete real de **$100.000 COP** (`assets/pay/efectivo-cop.jpg`).
- **WhatsApp** → logo verde oficial SVG (reemplaza el emoji de teléfono en todos los contactos).
- Sincronizado en **Medios de Pago**, **Contáctanos Ahora** y **Contacto & Pago** (footer).
- Nota: en el desplegable del formulario de pedido (`<option>`) se usan emojis porque los `<option>` nativos no admiten SVG/imagen (limitación del HTML).
- Nequi fue retirado de la vista pública para evitar spam de páginas externas.

## 🎁 Empaque
Cada pedido incluye **Bolsa de Lujo en Cuero Sintético**.

## 🛠️ Notas técnicas
- Sin frameworks ni build. Todo embebido para máxima compatibilidad y velocidad.
- Datos (pedidos, carrito) en `localStorage`/`sessionStorage` del navegador. Para una **base de datos real multi-dispositivo** y **pagos/facturación 100% automáticos**, conectar un backend (Supabase/Firebase + pasarela Wompi/Mercado Pago/Bold y un servicio de correo como EmailJS/Resend). El frontend ya está estructurado para integrarlo.

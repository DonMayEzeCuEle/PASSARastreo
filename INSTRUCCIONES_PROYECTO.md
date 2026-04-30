Reglas de Desarrollo: PASSA Rastreo
Este archivo contiene las directrices obligatorias para el desarrollo del sistema de logística y rastreo de PASSA. Gemini debe seguir estas reglas para mantener la consistencia del proyecto.  

1. Stack Tecnológico y Diseño
Framework CSS: Usar exclusivamente Tailwind CSS mediante CDN o PostCSS.  

Iconografía: Usar Font Awesome 6 (clases fa-solid, fa-brands, etc.).  

Mapas: No usar Google Maps. Usar exclusivamente Leaflet.js con capas de CartoDB Voyager para un diseño limpio.  

2. Estándares de Diseño Móvil (Crítico)
Altura del Viewport: Nunca usar h-screen. Para evitar que los elementos se corten en navegadores móviles (como Brave o Safari), usar siempre h-[100dvh].  

Zona Segura Inferior: Los botones principales en la parte inferior de la pantalla deben tener un padding inferior mínimo de pb-12 para no chocar con las barras de navegación del sistema móvil.  

Interactividad: Los botones deben incluir la clase active:scale-95 o active:scale-[0.98] para dar feedback táctil al usuario.  

3. Estructura de Archivos Existente
index.html: Pantalla de Login principal.  

lista_pedidos.html: Dashboard del repartidor con la lista de entregas pendientes.  

repartidor.html: Vista de mapa en vivo y validación de ubicación con Leaflet.  

admin_dashboard.html: Panel de control administrativo sin barra lateral (modo aislado).  

admin_perfil.html: Configuración de perfil administrativo en modo enfoque.  

4. Adaptabilidad según el Rol de Usuario
Interfaz del Repartidor (repartidor.html, lista_pedidos.html):

Prioridad: Usabilidad con una sola mano (pulgar).  

Diseño: Botones grandes, controles en la parte inferior y gestos sencillos.  

Viewport: Uso estricto de h-[100dvh] para evitar recortes en navegadores móviles.  

Interfaz del Administrador (admin_dashboard.html, admin_perfil.html):

Prioridad: Densidad de información y precisión.  

Entorno: Optimizado para escritorio (mouse y teclado).  

Diseño: Tablas detalladas, menús laterales o superiores y visualización de datos amplia.  

Nota: No aplicar las restricciones de "zona segura inferior" (pb-12) en estas vistas, ya que se asume el uso en monitores.

5. Comportamiento de la IA
Identifica el archivo antes de sugerir código: si es una vista de "admin", usa un diseño estándar de escritorio; si es de "repartidor", mantén el enfoque móvil estricto.  

Mantener el esquema de colores institucional en ambos roles: Azul corporativo (#001b71) y Verde PASSA (#6b9e1a).
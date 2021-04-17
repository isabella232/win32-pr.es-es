---
Descripción: para obtener acceso a los datos del contador de un equipo remoto: el equipo remoto debe tener habilitado el servicio de registro remoto. La excepción compartir archivos e impresoras debe estar seleccionada en la configuración de Firewall de Windows. antes de Windows Vista: el servicio registro remoto está habilitado de forma predeterminada.
MS. AssetID: 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 title: acceso a los datos de contador remotos ms. topic: artículo ms. Date: 08/17/2020
---

# <a name="accessing-remote-counter-data"></a>Acceso a datos de contador remotos

Para tener acceso a los datos de contador en un equipo remoto:

- El equipo remoto debe tener habilitado el servicio de registro remoto.
- La excepción **compartir archivos e impresoras** debe estar seleccionada en la **configuración de Firewall de Windows**.

**Antes de Windows Vista:** El servicio de registro remoto está habilitado de forma predeterminada.

> [!NOTE]
> Las herramientas y las API del contador de rendimiento de Windows incluyen compatibilidad limitada para tener acceso a los contadores de rendimiento de otros equipos a través de RPC (para los proveedores de V2) y del registro remoto (para los proveedores V1). Esta compatibilidad suele ser difícil de usar en términos de controles de autenticación (las herramientas y las API solo se pueden autenticar como el usuario actual) así como en términos de configuración del sistema (los puntos de conexión y servicios necesarios están deshabilitados de forma predeterminada en la mayoría de los sistemas). En muchos casos, es mejor acceder a los contadores de rendimiento de sistemas remotos mediante [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) en lugar de a través de la compatibilidad de acceso remoto integrada.

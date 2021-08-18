---
description: para acceder a los datos del contador en un equipo remoto: el equipo remoto debe tener habilitado el servicio registro remoto. La excepción Uso compartido de archivos e impresión debe estar seleccionada en Windows Firewall Configuración. Antes de Windows Vista: el servicio registro remoto está habilitado de forma predeterminada.
ms.assetid: 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 title: Accessing Remote Counter Data ms.topic: article ms.date: 08/17/2020
---

# <a name="accessing-remote-counter-data"></a>Acceso a datos de contador remoto

Para acceder a los datos del contador en un equipo remoto:

- El equipo remoto debe tener habilitado el servicio registro remoto.
- La **excepción Uso compartido de** archivos e impresión debe estar seleccionada en Windows Firewall **Configuración**.

**Antes de Windows Vista:** El servicio registro remoto está habilitado de forma predeterminada.

> [!NOTE]
> Windows Las API y herramientas de contadores de rendimiento incluyen compatibilidad limitada para acceder a contadores de rendimiento desde otras máquinas a través de RPC (para proveedores V2) y registro remoto (para proveedores V1). Esta compatibilidad suele ser difícil de usar en términos de controles de autenticación (las herramientas y las API solo se pueden autenticar como el usuario actual), así como en términos de configuración del sistema (los puntos de conexión y servicios necesarios están deshabilitados de forma predeterminada en la mayoría de los sistemas). En muchos casos, es mejor acceder a los contadores de rendimiento de los sistemas remotos a través de [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) en lugar de a través de la compatibilidad integrada con el acceso remoto.

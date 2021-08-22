---
title: Acerca de Windows plataforma de filtrado
description: Windows Plataforma de filtrado (WFP) es una plataforma de procesamiento de tráfico de red diseñada para reemplazar las interfaces de filtrado de tráfico de red Windows XP y Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a81f4f67c2f3281a6fa6b5d3220f9e2157643dfd7cf3bac34ea55743024946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069495"
---
# <a name="about-windows-filtering-platform"></a>Acerca de Windows plataforma de filtrado

Windows Plataforma de filtrado (WFP) es una plataforma de procesamiento de tráfico de red diseñada para reemplazar las interfaces de filtrado de tráfico de red Windows XP y Windows Server 2003. WFP consta de un conjunto de enlaces en la pila de red y un motor de filtrado que coordina las interacciones de la pila de red.

## <a name="the-wfp-components"></a>Componentes de WFP

### <a name="filter-engine"></a>Motor de filtros

La infraestructura principal de filtrado de varias capas, hospedada tanto en modo kernel como en modo de usuario, que reemplaza los módulos de filtrado múltiples en el subsistema de red de Windows XP y Windows Server 2003.

-   Filtra el tráfico de red en cualquier capa del sistema a través de los campos de datos que puede proporcionar una corrección de compatibilidad (shim).
-   Implementa los filtros "Callout" invocando llamadas durante la clasificación.
-   Devuelve las acciones "Permitir" o "Bloquear" a la corrección de compatibilidad (shim) que lo invocó para su cumplimiento.
-   Proporciona el arbitraje entre distintos orígenes de directivas. Por ejemplo, determina la prioridad cuando una aplicación está configurada para proteger cualquier tráfico de red relacionado con ella, pero el firewall local está configurado para evitar el tráfico protegido por la aplicación.<br/>

### <a name="base-filtering-engine-bfe"></a>Motor de filtrado base (BFE)

Servicio que controla el funcionamiento de la plataforma Windows filtrado. Realiza las siguientes tareas.

-   Acepta filtros y otras opciones de configuración para la plataforma.
-   Informa del estado actual del sistema, incluidas las estadísticas.
-   Aplica el modelo de seguridad para aceptar la configuración en la plataforma. Por ejemplo, un administrador local puede agregar filtros, pero otros usuarios solo pueden verlos.<br/>
-   Los valores de configuración de Plumbs para otros módulos del sistema. Por ejemplo, las directivas de negociación de IPsec van a los módulos de clave IKE/AuthIP y los filtros van al motor de filtros.<br/>

### <a name="shims"></a>Cuñas

Componentes en modo kernel que residen entre la pila de red y el motor de filtro. Las correcciones de compatibilidad (shim) hacen que la decisión de filtrado se clasifique en el motor de filtros. A continuación se muestra una lista de correcciones de compatibilidad (shim) disponibles.

-   Corrección de compatibilidad (SHIM) del cumplimiento de la capa de aplicación (ALE).
-   Corrección de compatibilidad (shim) del módulo de la capa de transporte.
-   Corrección de compatibilidad (shim) del módulo de capa de red.
-   Corrección de compatibilidad (SHIM) del Protocolo de mensajes de control de Internet (ICMP).
-   Descartar correcciones de compatibilidad (shim).
-   Corrección de compatibilidad (shim) de secuencia.

### <a name="callouts"></a>Llamadas

Conjunto de funciones expuestas por un controlador y utilizadas para el filtrado especializado. Además de las acciones básicas de "Permitir" y "Bloquear", las llamadas pueden modificar y proteger el tráfico de red entrante y saliente. Consulte el [tema Windows Filtering Platform Callout Drivers](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) (Controladores de llamada de la plataforma de filtrado) en la documentación de Windows Driver Kit (WDK) para obtener más información sobre las llamadas. WFP proporciona llamadas integradas que realiza las siguientes tareas.<br/>

-   Realice el procesamiento de IPsec.
-   Ajuste el comportamiento del filtrado con estado.
-   Realizar el filtrado en modo silencioso (caída silenciosa de paquetes que no se solicitaron).
-   Controlar la descarga tcp-in-tcp.
-   Interactúe con el servicio Teredo.

<br/> El motor de filtros permite que las llamadas de terceros se registren en cada una de sus capas en modo kernel.<br/>

### <a name="application-programming-interface"></a>Interfaz de programación de aplicaciones

Un conjunto de tipos de datos y funciones disponibles para que los desarrolladores compilen y administren aplicaciones de filtrado de red. Estos tipos de datos y funciones se agrupan en varios conjuntos [de API.](api-sets.md)

## <a name="wfp-features"></a>Características de WFP

-   Proporciona una infraestructura de filtrado de paquetes en la que los proveedores de software independientes (ISV) pueden conectar módulos de filtrado especializados.
-   Funciona con IPv4 e IPv6.
-   Permite filtrar, modificar y volver a inyección de datos.
-   Realiza el procesamiento de paquetes y flujos.
-   Permite habilitar el filtrado de paquetes por aplicación, por usuario y por conexión, además de por interfaz de red o por puerto.
-   Proporciona seguridad en tiempo de arranque hasta que se puede iniciar el motor de filtrado base (BFE).
-   Habilita el filtrado de conexiones con estado.
-   Controla los datos cifrados con IPsec previos y posteriores.
-   Permite la integración de directivas de filtrado de IPsec y firewall.
-   Proporciona una infraestructura de administración de directivas para determinar cuándo se deben activar filtros específicos. Esto incluye la mediación de los requisitos en conflicto de varios filtros proporcionados por distintos proveedores.
-   Controla la mayoría del reensamblado de paquetes y el seguimiento de estado.
-   Incluye un sistema de notificación de usuario genérico que informa a los suscriptores de los cambios en el sistema de filtrado.
-   Implementa funciones de enumeración que informan sobre el estado del sistema.
-   Usa eventos net para registrar errores de IPsec y pérdidas de paquetes.
-   Admite una Marco de diagnóstico de redes [auxiliar de Marco de diagnóstico de redes (NDF).](/windows/desktop/NDF/extensible-helper-classes)
-   Admite las [extensiones de sockets seguros](/windows/desktop/WinSock/winsock-secure-socket-extensions) para winsock API, que permiten a las aplicaciones de red proteger su tráfico mediante la configuración de WFP.
-   En las capas de Aplicación de la capa de aplicación (ALE), afecta mínimamente al rendimiento de la red al procesar solo el primer paquete de una conexión.
-   Integra la descarga de hardware, donde los módulos de llamada en modo kernel pueden usar hardware para realizar una inspección de paquetes específica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de WFP](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[Operación WFP](basic-operation.md)
</dt> <dt>

[Aplicación de la capa de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Configuración de IPsec](ipsec-configuration.md)
</dt> <dt>

[Configuración de WFP](wfp-configuration.md)
</dt> <dt>

[Supervisión de WFP](wfp-monitoring.md)
</dt> <dt>

[WFP API](api-sets.md)
</dt> </dl>

 


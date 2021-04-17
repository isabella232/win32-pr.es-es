---
title: Acerca de la plataforma de filtrado de Windows
description: La plataforma de filtrado de Windows (WFP) es una plataforma de procesamiento de tráfico de red diseñada para reemplazar las interfaces de filtrado del tráfico de red de Windows XP y Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665824"
---
# <a name="about-windows-filtering-platform"></a>Acerca de la plataforma de filtrado de Windows

La plataforma de filtrado de Windows (WFP) es una plataforma de procesamiento de tráfico de red diseñada para reemplazar las interfaces de filtrado del tráfico de red de Windows XP y Windows Server 2003. WFP se compone de un conjunto de enlaces en la pila de red y un motor de filtrado que coordina las interacciones de la pila de red.

## <a name="the-wfp-components"></a>Los componentes de WFP

### <a name="filter-engine"></a>Motor de filtro

La infraestructura de filtrado de varios niveles principal, hospedada en modo de kernel y en modo de usuario, que reemplaza los módulos de filtrado múltiples en el subsistema de redes de Windows XP y Windows Server 2003.

-   Filtra el tráfico de red en cualquier capa del sistema sobre cualquier campo de datos que pueda proporcionar una corrección de compatibilidad.
-   Implementa los filtros de "llamada" mediante la invocación de llamadas durante la clasificación.
-   Devuelve las acciones "permitir" o "bloquear" a la corrección de compatibilidad que lo invocó para la aplicación.
-   Proporciona arbitraje entre distintos orígenes de directiva. Por ejemplo, determina la prioridad cuando una aplicación está configurada para proteger el tráfico de red relacionado con ella, pero el Firewall local está configurado para impedir el tráfico protegido por la aplicación.<br/>

### <a name="base-filtering-engine-bfe"></a>Motor de filtrado de base (BFE)

Un servicio que controla el funcionamiento de la plataforma de filtrado de Windows. Realiza las siguientes tareas.

-   Acepta filtros y otras opciones de configuración para la plataforma.
-   Informa del estado actual del sistema, incluidas las estadísticas.
-   Aplica el modelo de seguridad para aceptar la configuración en la plataforma. Por ejemplo, un administrador local puede Agregar filtros, pero otros usuarios solo pueden verlos.<br/>
-   Los valores de configuración de las conexiones a otros módulos del sistema. Por ejemplo, las directivas de negociación de IPsec van a los módulos de creación de claves IKE/AuthIP, los filtros van al motor de filtro.<br/>

### <a name="shims"></a>Correcciones

Componentes de modo kernel que residen entre la pila de red y el motor de filtro. Las correcciones de compatibilidad (shim) realizan la decisión de filtrado mediante la clasificación en el motor de filtro. A continuación se muestra una lista de las correcciones de compatibilidad (shim) disponibles.

-   Corrección de compatibilidad de cumplimiento de nivel de aplicación (ALE).
-   Corrección de compatibilidad del módulo de capa de transporte.
-   Correcciones de compatibilidad del módulo de capa de red.
-   Corrección de errores del Protocolo de mensajes de control de Internet (ICMP).
-   Descartar correcciones de compatibilidad.
-   Corrección de compatibilidad.

### <a name="callouts"></a>Llamadas

Conjunto de funciones expuestas por un controlador y utilizadas para el filtrado especializado. Además de las acciones básicas de "permitir" y "bloquear", las llamadas pueden modificar y proteger el tráfico de red entrante y saliente. Consulte el tema controladores de llamadas de la [plataforma de filtrado de Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) en la documentación del kit de controladores de Windows (WDK) para obtener más información sobre las llamadas. WFP proporciona llamadas integradas que realizan las siguientes tareas.<br/>

-   Realizar el procesamiento de IPsec.
-   Ajuste el comportamiento del filtrado con estado.
-   Realice el filtrado en modo invisible (eliminación silenciosa de los paquetes que no se solicitaron).
-   Controlar la descarga de TCP Chimney.
-   Interactúe con el servicio Teredo.

<br/> El motor de filtro permite que las llamadas de terceros se registren en cada una de sus capas de modo kernel.<br/>

### <a name="application-programming-interface"></a>Interfaz de programación de aplicaciones

Conjunto de tipos de datos y funciones disponibles para que los desarrolladores puedan crear y administrar aplicaciones de filtrado de red. Estos tipos de datos y funciones se agrupan en varios [conjuntos de API](api-sets.md).

## <a name="wfp-features"></a>Características de WFP

-   Proporciona una infraestructura de filtrado de paquetes en la que los fabricantes de software independientes (ISV) pueden complementar módulos de filtrado especializados.
-   Funciona con IPv4 e IPv6.
-   Permite el filtrado, modificación y reinyección de datos.
-   Realiza el procesamiento de paquetes y de secuencias.
-   Permite habilitar el filtrado de paquetes por aplicación, por usuario y por conexión, además de por interfaz de red o por puerto.
-   Proporciona seguridad en tiempo de arranque hasta que se puede iniciar el motor de filtrado de base (BFE).
-   Habilita el filtrado de conexiones con estado.
-   Controla los datos anteriores y posteriores cifrados con IPsec.
-   Permite la integración de directivas de filtrado de firewall y IPsec.
-   Proporciona una infraestructura de administración de directivas para determinar cuándo se deben activar filtros específicos. Esto incluye la mediación de requisitos conflictivos de varios filtros proporcionados por diferentes proveedores.
-   Controla la mayoría del reensamblado de paquetes y el seguimiento del estado.
-   Incluye un sistema de notificaciones de usuario genérico que informa a los suscriptores de los cambios en el sistema de filtrado.
-   Implementa las funciones de enumeración que informan sobre el estado del sistema.
-   Utiliza eventos net para registrar errores de IPsec y caídas de paquetes.
-   Admite una clase auxiliar del marco de diagnóstico de redes [(NDF)](/windows/desktop/NDF/extensible-helper-classes).
-   Admite las [extensiones de sockets seguros](/windows/desktop/WinSock/winsock-secure-socket-extensions) para la API de Winsock, que permiten a las aplicaciones de red proteger su tráfico mediante la configuración de WFP.
-   En las capas de aplicación de nivel de aplicación (ALE), afecta de manera mínima al rendimiento de la red al procesar solo el primer paquete de una conexión.
-   Integra la descarga de hardware, donde los módulos de llamada en modo kernel pueden usar hardware para realizar una inspección de paquetes específica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de WFP](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[Operación de WFP](basic-operation.md)
</dt> <dt>

[Aplicación del nivel de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Configuración de IPsec](ipsec-configuration.md)
</dt> <dt>

[Configuración de WFP](wfp-configuration.md)
</dt> <dt>

[Supervisión de WFP](wfp-monitoring.md)
</dt> <dt>

[API DE WFP](api-sets.md)
</dt> </dl>

 


---
description: A continuación se muestra una guía paso a paso para empezar a programar mediante la interfaz de programación de aplicaciones (API) del asistente de IP. Está diseñado para proporcionar una comprensión de las funciones básicas del asistente de IP y las estructuras de datos, y cómo funcionan conjuntamente.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Tareas iniciales con el asistente de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069792"
---
# <a name="getting-started-with-ip-helper"></a>Tareas iniciales con el asistente de IP

A continuación se muestra una guía paso a paso para empezar a programar mediante la interfaz de programación de aplicaciones (API) del asistente de IP. Está diseñado para proporcionar una comprensión de las funciones básicas del asistente de IP y las estructuras de datos, y cómo funcionan conjuntamente.

La aplicación que se usa para la ilustración es una aplicación auxiliar de IP muy básica. En los ejemplos incluidos con el Kit de desarrollo de software (SDK) de Microsoft Windows se incluyen ejemplos de código más avanzados.

El primer paso es el mismo para la mayoría de las aplicaciones auxiliares de IP.

-   [Creación de una aplicación auxiliar de IP básica](creating-a-basic-ip-helper-application.md)

En las secciones siguientes se describen los pasos restantes para crear esta aplicación auxiliar de IP básica.

-   [Recuperación de información mediante GetNetworkParams](retrieving-information-using-getnetworkparams.md)
-   [Administración de adaptadores de red mediante GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)
-   [Administración de interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)
-   [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)
-   [Administración de concesiones DHCP mediante IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [Administración de direcciones IP mediante AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [Recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md)
-   [Recuperar información mediante GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Código fuente completo para este ejemplo básico del asistente de IP.

-   [Código fuente completo de la aplicación auxiliar de IP](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a>Ejemplos avanzados del asistente de IP

Se incluyen varios ejemplos más avanzados del asistente de IP con el Kit de desarrollo de software (SDK) de Microsoft Windows. De forma predeterminada, el SDK de Windows publicado para Windows 7 instala el código fuente del asistente de IP en el directorio siguiente:

*C: \\ Archivos de programa SDK de Microsoft Windows ejemplo \\ \\ \\ v7.0 \\ \\ NetDs \\ IPHelp*

Los ejemplos más avanzados que se enumeran a continuación se encuentran en los directorios siguientes:

-   EnableRouter

    Este directorio contiene un ejemplo que muestra cómo usar las funciones del asistente de IP [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) y [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) para habilitar y deshabilitar el reenvío IPv4 en el equipo local.

-   iparp

    Este directorio contiene un programa de ejemplo que muestra cómo usar las funciones del asistente de IP para mostrar y manipular entradas en la tabla ARP IPv4 en el equipo local.

-   ipchange

    Este directorio contiene un programa de ejemplo que muestra cómo usar las funciones auxiliares de IP para cambiar mediante programación una dirección IP para un adaptador de red específico en el equipo. Este programa también muestra cómo recuperar la información de configuración ip del adaptador de red existente.

-   IPConfig

    Este directorio contiene un programa de ejemplo que muestra cómo recuperar mediante programación información de configuración de IPv4 similar a la IPCONFIG.EXE programación. Muestra cómo usar las funciones [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) y [**GetAdaptersInfo.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) Tenga en cuenta **que la función GetAdaptersInfo** solo recupera información IPv4.

-   IPRenew

    Este directorio contiene un programa de ejemplo que muestra cómo liberar y renovar mediante programación direcciones IPv4 obtenidas a través de DHCP. Este programa también muestra cómo recuperar la información de configuración del adaptador de red existente.

-   IPRoute

    Este directorio contiene un programa de ejemplo que muestra cómo usar las funciones auxiliares de IP para manipular la tabla de enrutamiento IPv4.

-   ipstat

    Este directorio contiene un programa de ejemplo que muestra cómo usar las funciones auxiliares de IP para mostrar las conexiones IPv4 para un protocolo. De forma predeterminada, las estadísticas se muestran para IP, ICMP, TCP y UDP.

-   Netinfo

    Este directorio contiene un programa de ejemplo que muestra cómo usar las nuevas API del asistente de IP introducidas en Windows Vista y versiones posteriores para mostrar o cambiar la información de dirección e interfaz para IPv4 e IPv6.

 

 




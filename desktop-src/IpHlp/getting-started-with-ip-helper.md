---
description: A continuación se facilita una guía paso a paso para empezar a programar con la interfaz de programación de aplicaciones (API) auxiliar de IP. Está diseñado para proporcionar una descripción de las funciones básicas de la aplicación auxiliar de IP y las estructuras de datos, y de cómo funcionan conjuntamente.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Introducción con la aplicación auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913686"
---
# <a name="getting-started-with-ip-helper"></a>Introducción con la aplicación auxiliar de IP

A continuación se facilita una guía paso a paso para empezar a programar con la interfaz de programación de aplicaciones (API) auxiliar de IP. Está diseñado para proporcionar una descripción de las funciones básicas de la aplicación auxiliar de IP y las estructuras de datos, y de cómo funcionan conjuntamente.

La aplicación que se usa para la ilustración es una aplicación auxiliar de IP muy básica. En los ejemplos incluidos en el kit de desarrollo de software (SDK) de Microsoft Windows se incluyen ejemplos de código más avanzados.

El primer paso es el mismo para la mayoría de las aplicaciones auxiliares de IP.

-   [Creación de una aplicación auxiliar de IP básica](creating-a-basic-ip-helper-application.md)

En las secciones siguientes se describen los pasos restantes para crear esta aplicación auxiliar de IP básica.

-   [Recuperación de información mediante GetNetworkParams](retrieving-information-using-getnetworkparams.md)
-   [Administración de adaptadores de red con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)
-   [Administrar interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)
-   [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)
-   [Administrar concesiones DHCP mediante IpReleaseAddress y IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [Administración de direcciones IP mediante AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [Recuperación de información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md)
-   [Recuperación de información mediante GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

El código fuente completo de este ejemplo de aplicación auxiliar de IP básica.

-   [Código fuente completo de la aplicación auxiliar IP](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a>Ejemplos de aplicaciones auxiliares de IP avanzadas

En el kit de desarrollo de software (SDK) de Microsoft Windows se incluyen varios ejemplos de aplicación auxiliar de IP más avanzados. De forma predeterminada, el Windows SDK publicado para Windows 7 en el siguiente directorio instala el código fuente de ejemplo de la aplicación auxiliar IP.

*C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ NetDs \\ IPHelp*

Los ejemplos más avanzados que se enumeran a continuación se encuentran en los siguientes directorios:

-   EnableRouter

    Este directorio contiene un ejemplo que muestra cómo usar las funciones auxiliares de IP [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) y [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) para habilitar y deshabilitar el reenvío IPv4 en el equipo local.

-   iparp

    Este directorio contiene un programa de ejemplo que muestra cómo utilizar las funciones auxiliares de IP para mostrar y manipular entradas en la tabla ARP de IPv4 en el equipo local.

-   ipchange

    Este directorio contiene un programa de ejemplo que muestra cómo usar las funciones auxiliares de IP para cambiar mediante programación una dirección IP para un adaptador de red específico de la máquina. Este programa también muestra cómo recuperar la información de configuración IP del adaptador de red existente.

-   IPConfig

    Este directorio contiene un programa de ejemplo que muestra cómo recuperar mediante programación la información de configuración de IPv4 similar a la utilidad IPCONFIG.EXE. Muestra cómo usar las funciones [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) y [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) . Tenga en cuenta que la función **GetAdaptersInfo** solo recupera información de IPv4.

-   IPRenew

    Este directorio contiene un programa de ejemplo que muestra cómo liberar y renovar mediante programación las direcciones IPv4 obtenidas a través de DHCP. Este programa también muestra cómo recuperar la información de configuración del adaptador de red existente.

-   IPRoute

    Este directorio contiene un programa de ejemplo que muestra cómo utilizar las funciones auxiliares de IP para manipular la tabla de enrutamiento de IPv4.

-   ipstat

    Este directorio contiene un programa de ejemplo que muestra cómo utilizar las funciones auxiliares de IP para mostrar las conexiones IPv4 para un protocolo. De forma predeterminada, las estadísticas se muestran para IP, ICMP, TCP y UDP.

-   Netinfo

    Este directorio contiene un programa de ejemplo que muestra cómo usar las nuevas API auxiliares de IP introducidas en Windows Vista y versiones posteriores para mostrar o cambiar la información de dirección e interfaz para IPv4 e IPv6.

 

 




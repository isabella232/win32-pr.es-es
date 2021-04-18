---
description: La aplicación auxiliar de IP proporciona funciones para administrar los adaptadores de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel IP, mientras que un adaptador es una abstracción de nivel de vínculo de vínculo.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Administración de adaptadores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541214"
---
# <a name="managing-network-adapters"></a>Administración de adaptadores de red

La aplicación auxiliar de IP proporciona funciones para administrar los adaptadores de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel IP, mientras que un adaptador es una abstracción de nivel de vínculo de vínculo.

Use las funciones descritas en los párrafos siguientes para recuperar información acerca de los adaptadores de red en el equipo local.

La función [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) devuelve una matriz de estructuras de [**\_ \_ información del adaptador de IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) , una para cada adaptador en el equipo local. La función [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) devuelve información adicional sobre un adaptador específico. La función **GetPerAdapterInfo** requiere que el llamador especifique el índice del adaptador. Para obtener el índice del adaptador del nombre del adaptador, utilice la función [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) .

Algunas aplicaciones usan adaptadores que reciben datagramas, pero no pueden transmitirlos. Para obtener información acerca de estos adaptadores, utilice la función [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) .

La función [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) permite recuperar las direcciones IP asociadas a un adaptador determinado. Esta función admite direcciones IPv4 e IPv6.

-   Para ver ejemplos de código que implican a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , consulte [Administración de adaptadores de red con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).

 

 




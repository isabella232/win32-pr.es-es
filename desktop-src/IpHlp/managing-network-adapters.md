---
description: El asistente de IP proporciona funcionalidades para administrar adaptadores de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel de IP, mientras que un adaptador es una abstracción de nivel de vínculo de datos.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Administración de adaptadores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e1fd02426b27e3c07d4634edbe0215efa1c5c25c7a9c3abde32e991f766daf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078265"
---
# <a name="managing-network-adapters"></a>Administración de adaptadores de red

El asistente de IP proporciona funcionalidades para administrar adaptadores de red. Hay una correspondencia uno a uno entre las interfaces y los adaptadores de un equipo determinado. Una interfaz es una abstracción de nivel de IP, mientras que un adaptador es una abstracción de nivel de vínculo de datos.

Use las funciones descritas en los párrafos siguientes para recuperar información sobre los adaptadores de red en el equipo local.

La [**función GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) devuelve una matriz de estructuras INFO del ADAPTADOR [**\_ \_ DE IP,**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) una para cada adaptador del equipo local. La [**función GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) devuelve información adicional sobre un adaptador específico. La **función GetPerAdapterInfo** requiere que el autor de la llamada especifique el índice del adaptador. Para obtener el índice del adaptador a partir del nombre del adaptador, use la [**función GetAdapterIndex.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex)

Algunas aplicaciones usan adaptadores que reciben datagramas, pero no pueden transmitirlos. Para obtener información sobre estos adaptadores, use la [**función GetUniDirectionalAdapterInfo.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

La [**función GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) permite recuperar las direcciones IP asociadas a un adaptador determinado. Esta función admite el direccionamiento IPv4 e IPv6.

-   Para obtener ejemplos de código que [**implican GetAdaptersInfo,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) vea [Administración de adaptadores de red mediante GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).

 

 




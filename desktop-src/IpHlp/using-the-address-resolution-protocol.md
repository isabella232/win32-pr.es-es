---
description: Puede usar la aplicación auxiliar de IP para realizar operaciones del Protocolo de resolución de direcciones (ARP) para el equipo local. Utilice las siguientes funciones para recuperar y modificar la tabla ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Usar el protocolo de resolución de direcciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678407"
---
# <a name="using-the-address-resolution-protocol"></a>Usar el protocolo de resolución de direcciones

Puede usar la aplicación auxiliar de IP para realizar operaciones del Protocolo de resolución de direcciones (ARP) para el equipo local. Utilice las siguientes funciones para recuperar y modificar la tabla ARP.

[**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) recupera la tabla ARP. La tabla ARP contiene la asignación de direcciones IP a direcciones físicas. Las direcciones físicas a veces se denominan direcciones de controlador de acceso a medios (MAC).

Use las funciones [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) y [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) para agregar o quitar determinadas entradas ARP de la tabla. La función [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) elimina todas las entradas de la tabla.

Para crear o eliminar entradas ARP de proxy, utilice las funciones [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) y [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .

La función [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) envía una solicitud ARP a la red local.

 

 




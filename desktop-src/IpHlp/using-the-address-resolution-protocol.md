---
description: Puede usar el asistente de IP para realizar operaciones del Protocolo de resolución de direcciones (ARP) para el equipo local. Use las siguientes funciones para recuperar y modificar la tabla ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Uso del protocolo de resolución de direcciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160051"
---
# <a name="using-the-address-resolution-protocol"></a>Uso del protocolo de resolución de direcciones

Puede usar el asistente de IP para realizar operaciones del Protocolo de resolución de direcciones (ARP) para el equipo local. Use las siguientes funciones para recuperar y modificar la tabla ARP.

[**GetIpNetTable recupera**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) la tabla ARP. La tabla ARP contiene la asignación de direcciones IP a direcciones físicas. Las direcciones físicas a veces se conocen como direcciones de controlador de acceso multimedia (MAC).

Use las [**funciones CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) y [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) para agregar o quitar entradas ARP concretas a o desde la tabla. La [**función FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) elimina todas las entradas de la tabla.

Para crear o eliminar entradas ARP de proxy, use las [**funciones CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) [**y DeleteProxyArpEntry.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)

La [**función SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) envía una solicitud ARP a la red local.

 

 




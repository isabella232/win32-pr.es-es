---
description: El asistente de IP puede ayudar en la administración de direcciones IP asociadas a interfaces en el equipo local. Use las funciones descritas en los párrafos siguientes para la administración de direcciones IP.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Administración de direcciones IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160074"
---
# <a name="managing-ip-addresses"></a>Administración de direcciones IP

El asistente de IP puede ayudar en la administración de direcciones IP asociadas a interfaces en el equipo local. Use las funciones descritas en los párrafos siguientes para la administración de direcciones IP.

La [**función GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) recupera una tabla que contiene la asignación de direcciones IP a interfaces. Se puede asociar más de una dirección IP a la misma interfaz.

Use la [**función AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para agregar una dirección IP a una interfaz determinada. Para quitar las direcciones IP que se agregaron anteriormente mediante **AddIPAddress,** use [**la función DeleteIPAddress.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)

Las [**funciones IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) requieren que el equipo local use el Protocolo de configuración dinámica de host (DHCP). La **función IpReleaseAddress** libera una dirección IP que se obtuvo previamente de DHCP. La **función IpRenewAddress** renueva una concesión DHCP en una dirección IP determinada. Una concesión DHCP permite que un equipo use una dirección IP durante un período de tiempo especificado.

-   Para obtener ejemplos de código [**relacionados con GetIpAddrTable,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) consulte [Administración de direcciones IP mediante GetIpAddrTable.](managing-ip-addresses-using-getipaddrtable.md)

-   Para obtener ejemplos de código [**que implican AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) y [**DeleteIPAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)vea Administración de direcciones IP mediante [AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).

-   Para obtener ejemplos de código [**que implican IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) vea Managing [DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 




---
description: La aplicación auxiliar de IP puede ayudar en la administración de las direcciones IP asociadas a las interfaces en el equipo local. Use las funciones descritas en los párrafos siguientes para la administración de direcciones IP.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Administración de direcciones IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686710"
---
# <a name="managing-ip-addresses"></a>Administración de direcciones IP

La aplicación auxiliar de IP puede ayudar en la administración de las direcciones IP asociadas a las interfaces en el equipo local. Use las funciones descritas en los párrafos siguientes para la administración de direcciones IP.

La función [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) recupera una tabla que contiene la asignación de direcciones IP a las interfaces. Se puede asociar más de una dirección IP a la misma interfaz.

Utilice la función [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para agregar una dirección IP a una interfaz determinada. Para quitar las direcciones IP que se agregaron previamente mediante **AddIPAddress**, use la función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .

Las funciones [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) y [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) requieren que el equipo local use el protocolo de configuración dinámica de host (DHCP). La función **IpReleaseAddress** libera una dirección IP que se obtuvo previamente de DHCP. La función **IpRenewAddress** renueva una concesión DHCP en una dirección IP determinada. Una concesión DHCP permite que un equipo use una dirección IP durante un período de tiempo especificado.

-   Para ver ejemplos de código que implican a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , consulte [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

-   Para ver ejemplos de código que implican [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) y [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), consulte [Administración de direcciones IP con AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).

-   Para obtener ejemplos de código que impliquen [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) y [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , vea [administrar concesiones DHCP mediante IpReleaseAddress y IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 




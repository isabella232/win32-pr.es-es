---
description: El proveedor de rutas IP WMI y las clases de red suministran datos para las direcciones IPv4. A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las funcionalidades de red IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Compatibilidad con IPv6 e IPv4 en WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070455"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a>Compatibilidad con IPv6 e IPv4 en WMI

El proveedor [de rutas IP WMI](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) y las clases de red suministran datos para las direcciones IPv4. A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las funcionalidades de red IPv6.

## <a name="wmi-ip-data"></a>Datos IP de WMI

Las clases siguientes solo suministran datos IPv4:

-   [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**NetworkAdapter de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

Las clases siguientes suministran datos para IPv4 e IPv6.

-   [**NetworkAdapterConfiguration de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    La **propiedad IpAddess** contiene la dirección IPv6 del equipo en una red IPv6.

-   [**PingStatus de Win32 \_**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) puede devolver datos para direcciones IPv4 o IPv6.

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>Conexiones IPv4 e IPv6 a WMI

Al conectarse a un espacio de nombres WMI en un equipo remoto, el equipo de destino debe ejecutar el mismo software IP que el equipo que se conecta. Por ejemplo, un equipo que ejecuta IPv4 no puede conectarse a un equipo que ejecuta IPv6, incluso si la conexión se intenta mediante un nombre de equipo en la llamada a [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer o**](swbemlocator-connectserver.md)mediante la conexión `winmgmts` de moniker. Lo contrario también es cierto: un equipo que solo ejecuta IPv6 no puede conectarse a un equipo que solo ejecuta IPv4.

Si el equipo de destino ejecuta IPv4 e IPv6, se puede establecer una conexión desde un equipo que ejecute cualquier software IP. Se puede proporcionar un nombre de equipo o una dirección IP en formato IPv4 o IPv6 en la conexión a un espacio de nombres WMI.

Un equipo que ejecuta IPv4 e IPv6 y se conecta a un equipo de destino que solo ejecuta IPv4 o solo IPv6 debe proporcionar una dirección IP en el formato adecuado para el software IP del equipo de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 

---
description: Las clases de red y del proveedor de rutas IP de WMI proporcionan datos para las direcciones IPv4. A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las capacidades de red IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Compatibilidad con IPv6 e IPv4 en WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687990"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a>Compatibilidad con IPv6 e IPv4 en WMI

Las clases de red y del [proveedor de rutas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) de WMI proporcionan datos para las direcciones IPv4. A partir de Windows Vista, WMI también proporciona compatibilidad limitada con las capacidades de red IPv6.

## <a name="wmi-ip-data"></a>Datos de IP de WMI

Las clases siguientes solo proporcionan datos IPv4:

-   [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**Adaptador de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

Las siguientes clases proporcionan datos tanto para IPv4 como para IPv6.

-   [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    La propiedad **IpAddess** contiene la dirección IPv6 del equipo en una red IPv6.

-   [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) puede devolver datos para direcciones IPv4 o IPv6.

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>Conexiones IPv4 e IPv6 a WMI

Al conectarse a un espacio de nombres WMI en un equipo remoto, el equipo de destino debe ejecutar el mismo software IP que el equipo que se conecta. Por ejemplo, un equipo que ejecuta IPv4 no puede conectarse a un equipo que ejecuta IPv6, incluso si se intenta la conexión mediante el uso de un nombre de equipo en la llamada a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md)o mediante la `winmgmts` conexión de moniker. Lo contrario también es cierto: un equipo que ejecuta únicamente IPv6 no puede conectarse a un equipo que solo ejecute IPv4.

Si el equipo de destino está ejecutando IPv4 e IPv6, se puede establecer una conexión desde un equipo que ejecute el software IP. Se puede proporcionar un nombre de equipo o una dirección IP en formato IPv4 o IPv6 en la conexión a un espacio de nombres WMI.

Un equipo que ejecuta IPv4 e IPv6 y se conecta a un equipo de destino que solo ejecuta IPv4 o solo IPv6 debe proporcionar una dirección IP en el formato adecuado para el software de IP del equipo de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 

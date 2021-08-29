---
title: Administración de concesiones DHCP con IpReleaseAddress, IpRenewAddress
description: Las funciones IpReleaseAddress e IpRenewAddress se usan para liberar y renovar la concesión del Protocolo de configuración dinámica de host (DHCP) actual.
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c5f5e469932a6a03fb50e6bde05c2c50afbcb8455746e564d74dd87e96427d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146798"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a>Administración de concesiones DHCP con IpReleaseAddress, IpRenewAddress

Las [**funciones IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) se usan para liberar y renovar la concesión del Protocolo de configuración dinámica de host (DHCP) actual. La **función IpReleaseAddress** libera una dirección IPv4 obtenida previamente a través de DHCP. La **función IpRenewAddress** renueva una concesión en una dirección IPv4 obtenida previamente a través de DHCP. Es habitual usar estas dos funciones juntas, primero liberando la concesión con una llamada a **IpReleaseAddress** y, a continuación, renovando la concesión con una llamada a la función **IpRenewAddress.**

Cuando un cliente DHCP ha obtenido previamente una concesión DHCP y no se llama a [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) antes de la función [**IpRenewAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) la solicitud de cliente DHCP se envía al servidor DHCP que emitió la concesión DHCP inicial. Es posible que este servidor DHCP no esté disponible o que se pueda producir un error en la solicitud DHCP. Cuando un host ha obtenido previamente una concesión DHCP y se llama a **IpReleaseAddress** antes de la función **IpRenewAddress,** el cliente DHCP libera primero la dirección IP obtenida y envía una solicitud de cliente DHCP para obtener una respuesta de cualquier servidor DHCP disponible.

> [!Note]  
> Las [**funciones IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) [**e IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) requieren que DHCP se habilite para que funcione correctamente.

 

La [**función IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) toma un puntero a una estructura [**INDEX \_ \_ \_ MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) del ADAPTADOR DE IP como único parámetro. Para obtener este parámetro, llame primero [**a GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo). Para obtener ayuda con **la función GetInterfaceInfo,** vea [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

**Para usar IpReleaseAddress**

1.  Obtenga un puntero a una estructura [**\_ INDEX MAP \_ \_ del ADAPTADOR**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) DE IP mediante la función [**GetInterfaceInfo.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) (Para obtener ayuda con la función GetInterfaceInfo, vea [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)). Cree un **objeto DWORD** `dwRetVal` (usado para la comprobación de errores). Se supone que la variable devuelta por **GetInterfaceInfo** se denomina `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Si DHCP está habilitado, llame a la [**función IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) y pase la variable [**INDEX \_ \_ \_ MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) del ADAPTADOR DE IP `Adapter` como parámetro. Compruebe si hay errores generales y devuelva su valor a la variable **DWORD** `dwRetVal` (para una comprobación de errores más amplia).
    > [!Note]  
    > La [**función GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) devuelve un parámetro que se puede usar para comprobar si DHCP está habilitado antes de llamar a estas funciones. Para obtener ayuda con **GetAdaptersInfo,** vea [Administración de adaptadores de red mediante GetAdaptersInfo.](managing-network-adapters-using-getadaptersinfo.md)

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> Es habitual usar estas dos funciones juntas, llamando a la función [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) y, a continuación, llamando a la [**función IpRenewAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) pasando la misma estructura que el parámetro a ambas funciones. En el procedimiento siguiente se da por supuesto que las funciones no se usan juntas; sin embargo, si las funciones se usan juntas, omita el paso 1.

 

**Para usar IpRenewAddress**

1.  Obtenga un puntero a una estructura [**\_ INDEX MAP \_ \_ del ADAPTADOR**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) DE IP mediante la función [**GetInterfaceInfo.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) (Para obtener ayuda con **la función GetInterfaceInfo,** vea [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)). Declare un **objeto DWORD** `dwRetVal` (usado para la comprobación de errores) si esta variable no se ha declarado. Se supone que la variable devuelta por **GetInterfaceInfo** se denomina `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Llame a [**la función IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) y pase la variable [**INDEX \_ \_ \_ MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) del ADAPTADOR DE IP `Adapter` como parámetro. Compruebe si hay errores generales y devuelva su valor a la variable **DWORD** `dwRetVal` (para una comprobación de errores más amplia).
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

Paso siguiente: [Administración de direcciones IP mediante AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

Paso anterior: [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

 

 




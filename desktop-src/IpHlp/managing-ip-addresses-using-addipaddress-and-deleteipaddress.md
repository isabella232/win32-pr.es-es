---
title: Administración de direcciones IP con AddIPAddress y DeleteIPAddress
description: La función AddIPAddress agrega la dirección IPv4 especificada al adaptador especificado.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171849"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Administración de direcciones IP con AddIPAddress y DeleteIPAddress

La [**función AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) agrega la dirección IPv4 especificada al adaptador especificado. La [**función DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) elimina la dirección IPv4 especificada del adaptador especificado. Estas funciones se pueden usar para agregar y eliminar direcciones IPv4 a un adaptador de red.

Una dirección IPv4 agregada por la [**función AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) no es persistente. La dirección IPv4 solo existe siempre que exista el objeto de adaptador. Reiniciar el equipo destruye la dirección IPv4, al igual que el restablecimiento manual de la tarjeta de interfaz de red (NIC).

Una vez que se haya llamado correctamente a [**AddIPAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) DHCP se deshabilitará para la dirección IP que se agregó. Por lo tanto, las [**funciones como IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), que requieren que DHCP esté habilitado, no serán funcionales en la dirección IP agregada. La [**función DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) se puede usar para eliminar la dirección IPv4 agregada.

> [!Note]  
> Las directivas de grupo, las directivas empresariales y otras restricciones de la red pueden impedir que estas funciones se completen correctamente. Asegúrese de que la aplicación tiene los permisos de red necesarios antes de intentar usar estas funciones.

 

**Para usar AddIPAddress**

1.  Declare las variables **ULONG** `NTEContext` denominadas y `NTEInstance` , ambas inicializadas en cero.
    > [!Note]  
    > La variable es el único parámetro de la `NTEContext` [**función DeleteIPAddress;**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) para eliminar la dirección IP que se agrega, debe almacenarse `NTEContext` y sin modificarse.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Declare variables para las estructuras IPAddr e IPMask `iaIPAddress` denominadas y `iaIPMask` , respectivamente. Estos valores son simplemente enteros sin signo. Inicialice `iaIPAddress` las variables y mediante la función del `iaIPMask` [**\_ complemento inet.**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Llame a [**la función AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para agregar la dirección IPv4. Compruebe si hay errores y devuelva el valor de error a la variable **DWORD** `dwRetVal` (para una comprobación de errores más amplia).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > El tercer parámetro es el índice del adaptador, que se puede obtener llamando a la [**función GetIpAddrTable.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) Se supone que la variable devuelta por esta función se denomina `pIPAddrTable` . Para obtener ayuda con **la función GetIpAddrTable,** vea [Managing IP Address Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

     

**Para usar DeleteIpAddress**

-   Llame a [**la función DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) y pase `NTEContext` la variable como parámetro. Compruebe si hay errores y devuelva el valor de error a la variable **DWORD** `dwRetVal` (para una comprobación de errores más amplia).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Para usar [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), primero se debe llamar a [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para obtener el identificador `NTEContext` . En el procedimiento anterior se supone que ya se ha llamado a **AddIPAddress** en algún lugar del código y que se ha guardado y `NTEContext` no se ha realizado la corrección.

 

Paso siguiente: [Recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md)

Paso anterior: [Administración de concesiones DHCP mediante IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 

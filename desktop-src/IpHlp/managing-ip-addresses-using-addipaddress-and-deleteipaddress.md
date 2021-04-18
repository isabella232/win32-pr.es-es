---
title: Administrar direcciones IP con AddIPAddress, DeleteIPAddress
description: La función AddIPAddress agrega la dirección IPv4 especificada al adaptador especificado.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687452"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Administrar direcciones IP con AddIPAddress, DeleteIPAddress

La función [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) agrega la dirección IPv4 especificada al adaptador especificado. La función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) elimina la dirección IPv4 especificada del adaptador especificado. Estas funciones se pueden usar para agregar y eliminar direcciones IPv4 a un adaptador de red.

Una dirección IPv4 agregada por la función [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) no es persistente. La dirección IPv4 solo existe mientras exista el objeto de adaptador. Al reiniciar el equipo, se destruye la dirección IPv4, al igual que se restablece manualmente la tarjeta de interfaz de red (NIC).

Después de llamar a [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) correctamente, se deshabilitará DHCP para la dirección IP que se agregó. Por lo tanto, las funciones como [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), que requieren que se habilite DHCP, no funcionarán en la dirección IP agregada. La función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) se puede usar para eliminar la dirección IPv4 agregada.

> [!Note]  
> Las directivas de grupo, las directivas de empresa y otras restricciones de la red pueden impedir que estas funciones se completen correctamente. Asegúrese de que la aplicación tiene los permisos de red necesarios antes de intentar usar estas funciones.

 

**Para usar AddIPAddress**

1.  Declare las variables **ULong** denominadas `NTEContext` y `NTEInstance` , inicializadas en cero.
    > [!Note]  
    > La `NTEContext` variable es el único parámetro de la función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) ; para eliminar la dirección IP que se agrega, `NTEContext` se debe almacenar y sin modificar.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Declare las variables para las estructuras DirIP y IPMask denominadas `iaIPAddress` y `iaIPMask` , respectivamente. Estos valores son simplemente enteros sin signo. Inicialice las `iaIPAddress` `iaIPMask` variables y con la función de [**\_ Dirección inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Llame a la función [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para agregar la dirección IPv4. Compruebe si hay errores y devuelva el valor de error a la variable **DWORD** `dwRetVal` (para una comprobación de errores más extensa).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > El tercer parámetro es el índice del adaptador, que se puede obtener mediante una llamada a la función [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Se supone que la variable devuelta por esta función se denomina `pIPAddrTable` . Para obtener ayuda con la función **GetIpAddrTable** , consulte [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

     

**Para usar DeleteIpAddress**

-   Llame a la función [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , pasando la `NTEContext` variable como su parámetro. Compruebe si hay errores y devuelva el valor de error a la variable **DWORD** `dwRetVal` (para una comprobación de errores más extensa).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Para usar [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), primero se debe llamar a [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para obtener el identificador `NTEContext` . En el procedimiento anterior se supone que ya se ha llamado a **AddIPAddress** en algún lugar del código y que se ha `NTEContext` guardado y permanece sin dañar.

 

Siguiente paso: [recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md)

Paso anterior: [Administración de concesiones DHCP mediante IpReleaseAddress y IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 

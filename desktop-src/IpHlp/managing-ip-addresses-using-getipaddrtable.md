---
description: La función GetIpAddrTable rellena un puntero a una estructura IPADDRTABLE de MIB con información sobre las direcciones IP actuales asociadas \_ al sistema.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Administración de direcciones IP mediante GetIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090bdb1e73d3f770eafb3a5e70893253918eb68573ebd05aa6ec40a609a7ba4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146688"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Administración de direcciones IP mediante GetIpAddrTable

La [**función GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) rellena un puntero a una estructura [**\_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) de MIB con información sobre las direcciones IP actuales asociadas al sistema.

**Para usar GetIpAddrTable**

1.  Declare un puntero a un objeto [**\_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) de MIB denominado *pIPAddrTable* y un **objeto DWORD** denominado *dwSize*. Estas variables se pasan como parámetros a [**la función GetIpAddrTable.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) Cree también una variable **DWORD** denominada *dwRetVal* (que se usa para la comprobación de errores).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Asigne memoria para la estructura .
    > [!Note]  
    > El tamaño de *dwSize* no es suficiente para contener la información. Consulte el paso siguiente.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Realice una llamada inicial a [**GetIpAddrTable para**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) obtener el tamaño necesario en la variable *dwSize.*
    > [!Note]  
    > Esta llamada a la función está pensada para producir un error y se usa para asegurarse de que la variable *dwSize* especifica un tamaño suficiente para contener toda la información devuelta a *pIPAddrTable*. Se trata de un modelo de programación común para estructuras de datos y funciones de este tipo.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Realice una segunda llamada a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) con comprobación de errores general y devuelva su valor a la variable **DWORD** *dwRetVal* (para una comprobación de errores más avanzada).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Si la llamada se ha realizado correctamente, acceda a los datos desde la estructura de datos *pIPAddrTable.*
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Libera cualquier memoria asignada para la *estructura pIPAddrTable.*
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Los **objetos DWORD** *dwAddr* y *dwMask* se devuelven como valores numéricos en el orden de bytes del host, no en el orden de bytes de red. Estos valores no son direcciones IP de puntos.

 

Paso siguiente: [Administración de concesiones DHCP mediante IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Paso anterior: [Administración de interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

 

 

---
description: La función GetIpAddrTable rellena un puntero a una estructura MIB \_ IPADDRTABLE con información sobre las direcciones IP actuales asociadas al sistema.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Administración de direcciones IP mediante GetIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909493"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Administración de direcciones IP mediante GetIpAddrTable

La función [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) rellena un puntero a una estructura [**MIB \_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) con información sobre las direcciones IP actuales asociadas al sistema.

**Para usar GetIpAddrTable**

1.  Declare un puntero a un objeto [**MIB \_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) denominado *PIPAddrTable* y un objeto **DWORD** denominado *dwSize*. Estas variables se pasan como parámetros a la función [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Cree también una variable **DWORD** denominada *dwRetVal* (que se usa para la comprobación de errores).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Asigne memoria para la estructura.
    > [!Note]  
    > El tamaño de *dwSize* no es suficiente para contener la información. Vea el siguiente paso.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Realice una llamada inicial a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) para obtener el tamaño necesario en la variable *dwSize* .
    > [!Note]  
    > Esta llamada a la función está pensada para producir un error y se utiliza para asegurarse de que la variable *dwSize* especifica un tamaño suficiente para contener toda la información devuelta a *pIPAddrTable*. Se trata de un modelo de programación común para las estructuras de datos y las funciones de este tipo.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Realice una segunda llamada a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) con la comprobación de errores general y devuelva su valor a la variable **DWORD** *dwRetVal* (para la comprobación de errores más avanzada).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Si la llamada se realizó correctamente, acceda a los datos de la estructura de datos *pIPAddrTable* .
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Libere cualquier memoria asignada para la estructura *pIPAddrTable* .
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Los  objetos DWORD *dwAddr* y *dwMask* se devuelven como valores numéricos en el orden de bytes del host, no en el orden de bytes de red. Estos valores no son direcciones IP con puntos.

 

Paso siguiente: [Administración de concesiones DHCP mediante IpReleaseAddress y IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Paso anterior: [Administración de interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

 

 

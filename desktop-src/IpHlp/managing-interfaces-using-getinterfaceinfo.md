---
description: La función GetInterfaceInfo rellena un puntero a una estructura de \_ información de interfaz IP \_ con información sobre las interfaces asociadas al sistema.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Administrar interfaces mediante GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686709"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Administrar interfaces mediante GetInterfaceInfo

La función [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) rellena un puntero a una estructura [**de \_ \_ información de interfaz IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) con información sobre las interfaces asociadas al sistema.

**Para usar GetInterfaceInfo**

1.  Declare un puntero a un objeto de [**\_ \_ información de interfaz IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) denominado `pInfo` y un objeto **ULong** denominado `ulOutBufLen` . Declare también un objeto **DWORD** denominado `dwRetVal` (usado para la comprobación de errores).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Asigne memoria para las estructuras.
    > [!Note]  
    > El tamaño de `ulOutBufLen` no es suficiente para contener la información. Vea el siguiente paso.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Realice una llamada inicial a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) para obtener el tamaño necesario en la `ulOutBufLen` variable.
    > [!Note]  
    > Esta llamada a la función está pensada para producir un error y se utiliza para asegurarse de que la `ulOutBufLen` variable especifica un tamaño suficiente para contener toda la información devuelta a `pInfo` . Se trata de un modelo de programación común en la aplicación auxiliar de IP para las estructuras de datos y las funciones de este tipo.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Realice una segunda llamada a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) con la comprobación de errores general y devuelva su valor a la variable **DWORD** `dwRetVal` (para la comprobación de errores más avanzada).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Si la llamada se realizó correctamente, acceda a los datos de la `pInfo` estructura de datos.

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > % WS en la primera línea denota una cadena de tipo ancho. Se utiliza porque el atributo **Name** de la estructura [**de \_ \_ \_ asignación de índice del adaptador de IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` es **WCHAR**, que es una cadena Unicode.

     

6.  Libere cualquier memoria asignada para la estructura *Pinfo* .
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Siguiente paso: [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

Paso anterior: [Administración de adaptadores de red con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

 

 




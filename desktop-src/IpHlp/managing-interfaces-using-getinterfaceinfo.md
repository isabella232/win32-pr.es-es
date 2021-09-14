---
description: La función GetInterfaceInfo rellena un puntero a una estructura DE INFORMACIÓN DE INTERFAZ IP con \_ \_ información sobre las interfaces asociadas al sistema.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Administración de interfaces mediante GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171853"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Administración de interfaces mediante GetInterfaceInfo

La [**función GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) rellena un puntero a una estructura [**DE INFORMACIÓN DE \_ \_ INTERFAZ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) con información sobre las interfaces asociadas al sistema.

**Para usar GetInterfaceInfo**

1.  Declare un puntero a un objeto [**\_ IP INTERFACE \_ INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) denominado `pInfo` y un objeto **ULONG** denominado `ulOutBufLen` . Declare también un **objeto DWORD** denominado `dwRetVal` (usado para la comprobación de errores).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Asigne memoria para las estructuras.
    > [!Note]  
    > El tamaño de `ulOutBufLen` no es suficiente para contener la información. Consulte el paso siguiente.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Realice una llamada inicial a [**GetInterfaceInfo para**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) obtener el tamaño necesario en la `ulOutBufLen` variable .
    > [!Note]  
    > Esta llamada a la función está pensada para producir un error y se usa para asegurarse de que la variable especifica un tamaño suficiente para contener toda la `ulOutBufLen` información devuelta a `pInfo` . Se trata de un modelo de programación común en el asistente de IP para estructuras de datos y funciones de este tipo.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Realice una segunda llamada a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) con comprobación de errores general y devuelva su valor a la variable **DWORD** (para una `dwRetVal` comprobación de errores más avanzada).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Si la llamada se ha realizado correctamente, acceda a los datos desde la `pInfo` estructura de datos.

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
    > %ws en la primera línea denota una cadena ancha. Esto se usa porque el **atributo Name** de la estructura INDEX [**MAP \_ \_ \_ del**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) adaptador de IP es `Adapter` un **WCHAR**, que es una cadena Unicode.

     

6.  Libera cualquier memoria asignada para la *estructura pInfo.*
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Paso siguiente: [Administración de direcciones IP mediante GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

Paso anterior: [Administración de adaptadores de red mediante GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

 

 




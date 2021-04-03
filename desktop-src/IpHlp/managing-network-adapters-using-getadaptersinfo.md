---
description: La función GetAdaptersInfo rellena un puntero a una estructura de \_ \_ información del adaptador de IP con información sobre los adaptadores de red asociados al sistema.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Administración de adaptadores de red con GetAdaptersInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470e0ce7682a86b29df912fa4d4b1297c2263382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083004"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a>Administración de adaptadores de red con GetAdaptersInfo

La función [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) rellena un puntero a una estructura [**de \_ \_ información del adaptador de IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) con información sobre los adaptadores de red asociados al sistema.

**Para usar GetAdaptersInfo**

1.  Declare un puntero a una variable de [**\_ \_ información del adaptador de IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) denominada *pAdapterInfo* y una variable **ULong** denominada *ulOutBufLen*. Estas variables se pasan como parámetros a la función [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) . Cree también una variable **DWORD** denominada *dwRetVal* (para la comprobación de errores).
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  Asigne memoria para las estructuras.
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  Realice una llamada inicial a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) para obtener el tamaño necesario en la variable *ulOutBufLen* .
    > [!Note]  
    > Esta llamada a la función está pensada para producir un error y se utiliza para asegurarse de que la variable *ulOutBufLen* especifica un tamaño suficiente para contener toda la información devuelta a *pAdapterInfo*. Se trata de un modelo de programación común para las estructuras de datos y las funciones de este tipo.

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  Realice una segunda llamada a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), pasando *pAdapterInfo* y *ulOutBufLen* como parámetros y realizando la comprobación de errores generales. Devuelva su valor a la variable **DWORD** *dwRetVal* (para una comprobación de errores más extensa).
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  Si la llamada se realizó correctamente, acceda a algunos de los datos de la estructura *pAdapterInfo* .
    ```C++
    PIP_ADAPTER_INFO pAdapter = pAdapterInfo;
    while (pAdapter) {
        printf("Adapter Name: %s\n", pAdapter->AdapterName);
        printf("Adapter Desc: %s\n", pAdapter->Description);
        printf("\tAdapter Addr: \t");
        for (UINT i = 0; i < pAdapter->AddressLength; i++) {
            if (i == (pAdapter->AddressLength - 1))
                printf("%.2X\n",(int)pAdapter->Address[i]);
            else
                printf("%.2X-",(int)pAdapter->Address[i]);
        }
        printf("IP Address: %s\n", pAdapter->IpAddressList.IpAddress.String);
        printf("IP Mask: %s\n", pAdapter->IpAddressList.IpMask.String);
        printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
        printf("\t***\n");
        if (pAdapter->DhcpEnabled) {
            printf("\tDHCP Enabled: Yes\n");
            printf("\t\tDHCP Server: \t%s\n", pAdapter->DhcpServer.IpAddress.String);
        }
        else
          printf("\tDHCP Enabled: No\n");

      pAdapter = pAdapter->Next;
    }
    
    ```

    

6.  Libere cualquier memoria asignada para la estructura *pAdapterInfo* .
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

Paso siguiente: [Administración de interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

Paso anterior: [recuperar información mediante GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 




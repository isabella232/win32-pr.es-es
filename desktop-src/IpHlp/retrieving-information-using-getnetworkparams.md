---
description: Rellena un puntero a una estructura de \_ información fija con datos sobre la configuración de red actual.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Recuperación de información mediante GetNetworkParams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20aed9b1ffa761ec53637d4d5b165e3fd2c2673d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277190"
---
# <a name="retrieving-information-using-getnetworkparams"></a>Recuperación de información mediante GetNetworkParams

La función [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) rellena un puntero a una estructura [**de \_ información fija**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) con datos sobre la configuración de red actual.

**Para usar GetNetworkParams**

1.  Declare un puntero a un objeto de [**\_ información fijo**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) denominado *PFixedInfo* y un objeto **ULong** denominado *ulOutBufLen*. Estas variables se pasan como parámetros a la función [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Cree también una  variable DWORD *dwRetVal* (se usa para la comprobación de errores).
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  Asigne memoria para las estructuras.
    > [!Note]  
    > El tamaño de *ulOutBufLen* no es suficiente para contener la información. Vea el siguiente paso.

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  Realice una llamada inicial a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) para obtener el tamaño necesario para la variable *ulOutBufLen* .
    > [!Note]  
    > Se producirá un error en esta función de función y se usará para asegurarse de que la variable *ulOutBufLen* especifica un tamaño suficiente para contener todos los datos devueltos a *pFixedInfo*. Se trata de un modelo de programación común para las estructuras de datos y las funciones de este tipo.

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  Realice una segunda llamada a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) mediante la comprobación de errores general y devolviendo su valor a la variable **DWORD** *dwRetVal*; se usa para la comprobación de errores más avanzada.
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  Si la llamada se realizó correctamente, acceda a los datos de la estructura de datos *pFixedInfo* .
    ```C++
            printf("\tHost Name: %s\n", pFixedInfo->HostName);
            printf("\tDomain Name: %s\n", pFixedInfo->DomainName);
            printf("\tDNS Servers:\n");
            printf("\t\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

            pIPAddr = pFixedInfo->DnsServerList.Next;
            while (pIPAddr) {
                printf("\t\t%s\n", pIPAddr->IpAddress.String);
                pIPAddr = pIPAddr->Next;
            }

            printf("\tNode Type: ");
            switch (pFixedInfo->NodeType) {
            case 1:
                printf("%s\n", "Broadcast");
                break;
            case 2:
                printf("%s\n", "Peer to peer");
                break;
            case 4:
                printf("%s\n", "Mixed");
                break;
            case 8:
                printf("%s\n", "Hybrid");
                break;
            default:
                printf("\n");
            }

            printf("\tNetBIOS Scope ID: %s\n", pFixedInfo->ScopeId);

            if (pFixedInfo->EnableRouting)
                printf("\tIP Routing Enabled: Yes\n");
            else
                printf("\tIP Routing Enabled: No\n");

            if (pFixedInfo->EnableProxy)
                printf("\tWINS Proxy Enabled: Yes\n");
            else
                printf("\tWINS Proxy Enabled: No\n");

            if (pFixedInfo->EnableDns)
                printf("\tNetBIOS Resolution Uses DNS: Yes\n");
            else
                printf("\tNetBIOS Resolution Uses DNS: No\n");
    ```

    

6.  Libere cualquier memoria asignada para la estructura *pFixedInfo* .
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

Paso siguiente: [Administración de adaptadores de red con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

Paso anterior: [crear una aplicación auxiliar de IP básica](creating-a-basic-ip-helper-application.md)

 

 




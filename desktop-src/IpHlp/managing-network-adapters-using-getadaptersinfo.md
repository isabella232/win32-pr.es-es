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
# <a name="managing-network-adapters-using-getadaptersinfo"></a><span data-ttu-id="b8960-103">Administración de adaptadores de red con GetAdaptersInfo</span><span class="sxs-lookup"><span data-stu-id="b8960-103">Managing Network Adapters Using GetAdaptersInfo</span></span>

<span data-ttu-id="b8960-104">La función [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) rellena un puntero a una estructura [**de \_ \_ información del adaptador de IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) con información sobre los adaptadores de red asociados al sistema.</span><span class="sxs-lookup"><span data-stu-id="b8960-104">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function fills a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structure with information about the network adapters associated with the system.</span></span>

<span data-ttu-id="b8960-105">**Para usar GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="b8960-105">**To use GetAdaptersInfo**</span></span>

1.  <span data-ttu-id="b8960-106">Declare un puntero a una variable de [**\_ \_ información del adaptador de IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) denominada *pAdapterInfo* y una variable **ULong** denominada *ulOutBufLen*.</span><span class="sxs-lookup"><span data-stu-id="b8960-106">Declare a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) variable called *pAdapterInfo*, and a **ULONG** variable called *ulOutBufLen*.</span></span> <span data-ttu-id="b8960-107">Estas variables se pasan como parámetros a la función [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="b8960-107">These variables are passed as parameters to the [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function.</span></span> <span data-ttu-id="b8960-108">Cree también una variable **DWORD** denominada *dwRetVal* (para la comprobación de errores).</span><span class="sxs-lookup"><span data-stu-id="b8960-108">Also create a **DWORD** variable called *dwRetVal* (for error checking).</span></span>
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="b8960-109">Asigne memoria para las estructuras.</span><span class="sxs-lookup"><span data-stu-id="b8960-109">Allocate memory for the structures.</span></span>
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  <span data-ttu-id="b8960-110">Realice una llamada inicial a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) para obtener el tamaño necesario en la variable *ulOutBufLen* .</span><span class="sxs-lookup"><span data-stu-id="b8960-110">Make an initial call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) to get the size needed into the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="b8960-111">Esta llamada a la función está pensada para producir un error y se utiliza para asegurarse de que la variable *ulOutBufLen* especifica un tamaño suficiente para contener toda la información devuelta a *pAdapterInfo*.</span><span class="sxs-lookup"><span data-stu-id="b8960-111">This call to the function is meant to fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the information returned to *pAdapterInfo*.</span></span> <span data-ttu-id="b8960-112">Se trata de un modelo de programación común para las estructuras de datos y las funciones de este tipo.</span><span class="sxs-lookup"><span data-stu-id="b8960-112">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  <span data-ttu-id="b8960-113">Realice una segunda llamada a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), pasando *pAdapterInfo* y *ulOutBufLen* como parámetros y realizando la comprobación de errores generales.</span><span class="sxs-lookup"><span data-stu-id="b8960-113">Make a second call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passing *pAdapterInfo* and *ulOutBufLen* as parameters and doing general error checking.</span></span> <span data-ttu-id="b8960-114">Devuelva su valor a la variable **DWORD** *dwRetVal* (para una comprobación de errores más extensa).</span><span class="sxs-lookup"><span data-stu-id="b8960-114">Return its value to the **DWORD** variable *dwRetVal* (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  <span data-ttu-id="b8960-115">Si la llamada se realizó correctamente, acceda a algunos de los datos de la estructura *pAdapterInfo* .</span><span class="sxs-lookup"><span data-stu-id="b8960-115">If the call was successful, access some of the data in the *pAdapterInfo* structure.</span></span>
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

    

6.  <span data-ttu-id="b8960-116">Libere cualquier memoria asignada para la estructura *pAdapterInfo* .</span><span class="sxs-lookup"><span data-stu-id="b8960-116">Free any memory allocated for the *pAdapterInfo* structure.</span></span>
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

<span data-ttu-id="b8960-117">Paso siguiente: [Administración de interfaces mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="b8960-117">Next Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

<span data-ttu-id="b8960-118">Paso anterior: [recuperar información mediante GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="b8960-118">Previous Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 




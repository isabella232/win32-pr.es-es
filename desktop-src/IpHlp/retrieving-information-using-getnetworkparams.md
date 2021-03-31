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
# <a name="retrieving-information-using-getnetworkparams"></a><span data-ttu-id="25406-103">Recuperación de información mediante GetNetworkParams</span><span class="sxs-lookup"><span data-stu-id="25406-103">Retrieving Information Using GetNetworkParams</span></span>

<span data-ttu-id="25406-104">La función [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) rellena un puntero a una estructura [**de \_ información fija**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) con datos sobre la configuración de red actual.</span><span class="sxs-lookup"><span data-stu-id="25406-104">The [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function fills a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) structure with data about the current network settings.</span></span>

<span data-ttu-id="25406-105">**Para usar GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="25406-105">**To use GetNetworkParams**</span></span>

1.  <span data-ttu-id="25406-106">Declare un puntero a un objeto de [**\_ información fijo**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) denominado *PFixedInfo* y un objeto **ULong** denominado *ulOutBufLen*.</span><span class="sxs-lookup"><span data-stu-id="25406-106">Declare a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) object called *pFixedInfo*, and a **ULONG** object called *ulOutBufLen*.</span></span> <span data-ttu-id="25406-107">Estas variables se pasan como parámetros a la función [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) .</span><span class="sxs-lookup"><span data-stu-id="25406-107">These variables are passed as parameters to the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="25406-108">Cree también una  variable DWORD *dwRetVal* (se usa para la comprobación de errores).</span><span class="sxs-lookup"><span data-stu-id="25406-108">Also create a **DWORD** variable *dwRetVal* (used for error checking).</span></span>
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  <span data-ttu-id="25406-109">Asigne memoria para las estructuras.</span><span class="sxs-lookup"><span data-stu-id="25406-109">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="25406-110">El tamaño de *ulOutBufLen* no es suficiente para contener la información.</span><span class="sxs-lookup"><span data-stu-id="25406-110">The size of *ulOutBufLen* is not sufficient to hold the information.</span></span> <span data-ttu-id="25406-111">Vea el siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="25406-111">See the next step.</span></span>

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  <span data-ttu-id="25406-112">Realice una llamada inicial a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) para obtener el tamaño necesario para la variable *ulOutBufLen* .</span><span class="sxs-lookup"><span data-stu-id="25406-112">Make an initial call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) to get the size required for the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="25406-113">Se producirá un error en esta función de función y se usará para asegurarse de que la variable *ulOutBufLen* especifica un tamaño suficiente para contener todos los datos devueltos a *pFixedInfo*.</span><span class="sxs-lookup"><span data-stu-id="25406-113">This function function will fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the data returned to *pFixedInfo*.</span></span> <span data-ttu-id="25406-114">Se trata de un modelo de programación común para las estructuras de datos y las funciones de este tipo.</span><span class="sxs-lookup"><span data-stu-id="25406-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  <span data-ttu-id="25406-115">Realice una segunda llamada a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) mediante la comprobación de errores general y devolviendo su valor a la variable **DWORD** *dwRetVal*; se usa para la comprobación de errores más avanzada.</span><span class="sxs-lookup"><span data-stu-id="25406-115">Make a second call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) using general error checking and returning its value to the **DWORD** variable *dwRetVal*; used for more advanced error checking.</span></span>
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  <span data-ttu-id="25406-116">Si la llamada se realizó correctamente, acceda a los datos de la estructura de datos *pFixedInfo* .</span><span class="sxs-lookup"><span data-stu-id="25406-116">If the call was successful, access the data from the *pFixedInfo* data structure.</span></span>
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

    

6.  <span data-ttu-id="25406-117">Libere cualquier memoria asignada para la estructura *pFixedInfo* .</span><span class="sxs-lookup"><span data-stu-id="25406-117">Free any memory allocated for the *pFixedInfo* structure.</span></span>
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

<span data-ttu-id="25406-118">Paso siguiente: [Administración de adaptadores de red con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="25406-118">Next Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

<span data-ttu-id="25406-119">Paso anterior: [crear una aplicación auxiliar de IP básica](creating-a-basic-ip-helper-application.md)</span><span class="sxs-lookup"><span data-stu-id="25406-119">Previous Step: [Creating a Basic IP Helper Application](creating-a-basic-ip-helper-application.md)</span></span>

 

 




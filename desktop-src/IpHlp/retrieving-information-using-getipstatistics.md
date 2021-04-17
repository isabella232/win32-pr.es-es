---
description: La función GetIpStatistics rellena un puntero a una estructura MIB \_ IPSTATS con información sobre las estadísticas IP actuales asociadas al sistema.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Recuperación de información mediante GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6267c3939548c8f8ea9ab2705ea1769360748e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678000"
---
# <a name="retrieving-information-using-getipstatistics"></a><span data-ttu-id="13c80-103">Recuperación de información mediante GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="13c80-103">Retrieving Information Using GetIpStatistics</span></span>

<span data-ttu-id="13c80-104">La función [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) rellena un puntero a una estructura [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) con información sobre las estadísticas IP actuales asociadas al sistema.</span><span class="sxs-lookup"><span data-stu-id="13c80-104">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function fills a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure with information about the current IP statistics associated with the system.</span></span>

<span data-ttu-id="13c80-105">**Para usar GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="13c80-105">**To use GetIpStatistics**</span></span>

1.  <span data-ttu-id="13c80-106">Declare algunas variables que son necesarias.</span><span class="sxs-lookup"><span data-stu-id="13c80-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="13c80-107">Declare una variable **DWORD** `dwRetval` que vaya a usar para las llamadas de función de comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="13c80-107">Declare a **DWORD** variable `dwRetval` that will be using for error checking function calls.</span></span> <span data-ttu-id="13c80-108">Declare un puntero a una variable [**\_ IPSTATS de MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) denominada *pStats* y asigne memoria para la estructura.</span><span class="sxs-lookup"><span data-stu-id="13c80-108">Declare a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) variable called *pStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="13c80-109">Compruebe que se puede asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="13c80-109">Check that memory could be allocated.</span></span>

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  <span data-ttu-id="13c80-110">Llame a la función [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) con el parámetro *pStats* para recuperar las estadísticas de IP para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="13c80-110">Call the [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function with the *pStats* parameter to retrieve IP statistics for the local computer.</span></span> <span data-ttu-id="13c80-111">Compruebe si hay errores y devuelva el valor de error en la variable **DWORD** `dwRetval` .</span><span class="sxs-lookup"><span data-stu-id="13c80-111">Check for errors and return the error value in the **DWORD** variable `dwRetval`.</span></span> <span data-ttu-id="13c80-112">Si se produce un error, la `dwRetval` variable se puede usar para la comprobación de errores y la generación de informes más amplias.</span><span class="sxs-lookup"><span data-stu-id="13c80-112">If an error occurs, the `dwRetval` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  <span data-ttu-id="13c80-113">Si la llamada a [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) se realizó correctamente, imprima algunos de los datos de la estructura [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) señalada por el parámetro *pStats* .</span><span class="sxs-lookup"><span data-stu-id="13c80-113">If the call to [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) was successful, print out some of the data in the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span>
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  <span data-ttu-id="13c80-114">Libere la memoria asignada para la estructura [**\_ IPSTATS de MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) a la que apunta el parámetro *pStats* .</span><span class="sxs-lookup"><span data-stu-id="13c80-114">Free the memory allocated for the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span> <span data-ttu-id="13c80-115">Esto se debe hacer cuando la aplicación ya no necesita los datos devueltos por el parámetro *pStats* .</span><span class="sxs-lookup"><span data-stu-id="13c80-115">This should be done once the application no longer needs the data returned by the *pStats* parameter.</span></span>
    ```C++
    if (pStats)
        free(pStats);
    ```

    

<span data-ttu-id="13c80-116">Siguiente paso: [recuperar información mediante GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="13c80-116">Next Step: [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span></span>

<span data-ttu-id="13c80-117">Paso anterior: [Administración de direcciones IP mediante AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="13c80-117">Previous Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

 

 

---
description: La función GetTcpStatistics rellena un puntero a una estructura MIB \_ TCPSTATS con información sobre las estadísticas del protocolo TCP para el equipo local.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Recuperación de información mediante GetTcpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f4d4d42c2716d258ff72e3dd91ab750baaed20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677999"
---
# <a name="retrieving-information-using-gettcpstatistics"></a><span data-ttu-id="0fa7f-103">Recuperación de información mediante GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="0fa7f-103">Retrieving Information Using GetTcpStatistics</span></span>

<span data-ttu-id="0fa7f-104">La función [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) rellena un puntero a una estructura [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) con información sobre las estadísticas del protocolo TCP para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="0fa7f-104">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function fills a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure with information on the TCP protocol statistics for the local computer.</span></span>

<span data-ttu-id="0fa7f-105">**Para usar GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="0fa7f-105">**To use GetTcpStatistics**</span></span>

1.  <span data-ttu-id="0fa7f-106">Declare algunas variables que son necesarias.</span><span class="sxs-lookup"><span data-stu-id="0fa7f-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="0fa7f-107">Declare una variable **DWORD** `dwRetVal` que vaya a usar para las llamadas de función de comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="0fa7f-107">Declare a **DWORD** variable `dwRetVal` that will be using for error checking function calls.</span></span> <span data-ttu-id="0fa7f-108">Declare un puntero a una variable [**\_ TCPSTATS de MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) denominada *pTCPStats* y asigne memoria para la estructura.</span><span class="sxs-lookup"><span data-stu-id="0fa7f-108">Declare a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) variable called *pTCPStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="0fa7f-109">Compruebe que se puede asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="0fa7f-109">Check that memory could be allocated.</span></span>

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  <span data-ttu-id="0fa7f-110">Llame a la función [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) con el parámetro *pTCPStats* para recuperar las estadísticas TCP para IPv4 en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="0fa7f-110">Call the [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function with the *pTCPStats* parameter to retrieve TCP statistics for IPv4 on the local computer.</span></span> <span data-ttu-id="0fa7f-111">Compruebe si hay errores y devuelva el valor de error en la variable **DWORD** `dwRetVal` .</span><span class="sxs-lookup"><span data-stu-id="0fa7f-111">Check for errors and return the error value in the **DWORD** variable `dwRetVal`.</span></span> <span data-ttu-id="0fa7f-112">Si se produce un error, la `dwRetVal` variable se puede usar para la comprobación de errores y la generación de informes más amplias.</span><span class="sxs-lookup"><span data-stu-id="0fa7f-112">If an error occurs, the `dwRetVal` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  <span data-ttu-id="0fa7f-113">Si la llamada se realizó correctamente, acceda a los datos devueltos en la [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) señalada por el parámetro *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="0fa7f-113">If the call was successful, access the data returned in the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) pointed to by the *pTCPStats* parameter.</span></span>
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  <span data-ttu-id="0fa7f-114">Libere la memoria asignada para la estructura [**\_ TCPSTATS de MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) a la que apunta el parámetro *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="0fa7f-114">Free the memory allocated for the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure pointed to by the *pTCPStats* parameter.</span></span> <span data-ttu-id="0fa7f-115">Esto se debe hacer cuando la aplicación ya no necesita los datos devueltos por el parámetro *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="0fa7f-115">This should be done once the application no longer needs the data returned by the *pTCPStats* parameter.</span></span>
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

<span data-ttu-id="0fa7f-116">Siguiente paso: [recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="0fa7f-116">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="0fa7f-117">Paso anterior: [recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="0fa7f-117">Previous Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

## <a name="complete-source-code"></a><span data-ttu-id="0fa7f-118">Código fuente completo</span><span class="sxs-lookup"><span data-stu-id="0fa7f-118">Complete Source Code</span></span>

-   [<span data-ttu-id="0fa7f-119">Código fuente completo de la aplicación auxiliar IP</span><span class="sxs-lookup"><span data-stu-id="0fa7f-119">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

 

 

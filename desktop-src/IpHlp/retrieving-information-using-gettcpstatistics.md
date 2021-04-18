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
# <a name="retrieving-information-using-gettcpstatistics"></a>Recuperación de información mediante GetTcpStatistics

La función [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) rellena un puntero a una estructura [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) con información sobre las estadísticas del protocolo TCP para el equipo local.

**Para usar GetTcpStatistics**

1.  Declare algunas variables que son necesarias.

    Declare una variable **DWORD** `dwRetVal` que vaya a usar para las llamadas de función de comprobación de errores. Declare un puntero a una variable [**\_ TCPSTATS de MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) denominada *pTCPStats* y asigne memoria para la estructura. Compruebe que se puede asignar memoria.

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  Llame a la función [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) con el parámetro *pTCPStats* para recuperar las estadísticas TCP para IPv4 en el equipo local. Compruebe si hay errores y devuelva el valor de error en la variable **DWORD** `dwRetVal` . Si se produce un error, la `dwRetVal` variable se puede usar para la comprobación de errores y la generación de informes más amplias.
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  Si la llamada se realizó correctamente, acceda a los datos devueltos en la [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) señalada por el parámetro *pTCPStats* .
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  Libere la memoria asignada para la estructura [**\_ TCPSTATS de MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) a la que apunta el parámetro *pTCPStats* . Esto se debe hacer cuando la aplicación ya no necesita los datos devueltos por el parámetro *pTCPStats* .
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

Siguiente paso: [recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md)

Paso anterior: [recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md)

## <a name="complete-source-code"></a>Código fuente completo

-   [Código fuente completo de la aplicación auxiliar IP](complete-ip-helper-application-source-code.md)

 

 

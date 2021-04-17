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
# <a name="retrieving-information-using-getipstatistics"></a>Recuperación de información mediante GetIpStatistics

La función [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) rellena un puntero a una estructura [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) con información sobre las estadísticas IP actuales asociadas al sistema.

**Para usar GetIpStatistics**

1.  Declare algunas variables que son necesarias.

    Declare una variable **DWORD** `dwRetval` que vaya a usar para las llamadas de función de comprobación de errores. Declare un puntero a una variable [**\_ IPSTATS de MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) denominada *pStats* y asigne memoria para la estructura. Compruebe que se puede asignar memoria.

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  Llame a la función [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) con el parámetro *pStats* para recuperar las estadísticas de IP para el equipo local. Compruebe si hay errores y devuelva el valor de error en la variable **DWORD** `dwRetval` . Si se produce un error, la `dwRetval` variable se puede usar para la comprobación de errores y la generación de informes más amplias.
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  Si la llamada a [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) se realizó correctamente, imprima algunos de los datos de la estructura [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) señalada por el parámetro *pStats* .
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  Libere la memoria asignada para la estructura [**\_ IPSTATS de MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) a la que apunta el parámetro *pStats* . Esto se debe hacer cuando la aplicación ya no necesita los datos devueltos por el parámetro *pStats* .
    ```C++
    if (pStats)
        free(pStats);
    ```

    

Siguiente paso: [recuperar información mediante GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Paso anterior: [Administración de direcciones IP mediante AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 

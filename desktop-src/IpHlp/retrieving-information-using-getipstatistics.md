---
description: La función GetIpStatistics rellena un puntero a una estructura IPSTATS de MIB con información sobre las \_ estadísticas ip actuales asociadas al sistema.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Recuperar información mediante GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c383c49b316eb48e240a8272957dae8ee3ec1671304df8d466b869b7bf4ec0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050275"
---
# <a name="retrieving-information-using-getipstatistics"></a>Recuperar información mediante GetIpStatistics

La [**función GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) rellena un puntero a una estructura [**\_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) de MIB con información sobre las estadísticas ip actuales asociadas al sistema.

**Para usar GetIpStatistics**

1.  Declare algunas variables necesarias.

    Declare una variable **DWORD** que `dwRetval` se va a usar para las llamadas de función de comprobación de errores. Declare un puntero a una variable [**\_ IPSTATS de MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) denominada *pStats* y asigne memoria para la estructura . Compruebe que se puede asignar memoria.

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  Llame a [**la función GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) con el *parámetro pStats* para recuperar las estadísticas ip del equipo local. Compruebe si hay errores y devuelva el valor de error en la variable **DWORD** `dwRetval` . Si se produce un error, la variable se puede usar para la comprobación e informes de `dwRetval` errores más amplios.
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  Si la llamada a [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) se ha realizado correctamente, imprima algunos de los datos de la estructura [**\_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) de MIB a la que apunta el *parámetro pStats.*
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  Liberar la memoria asignada para la estructura [**\_ IPSTATS de MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) a la que apunta el *parámetro pStats.* Esto debe hacerse una vez que la aplicación ya no necesite los datos devueltos por *el parámetro pStats.*
    ```C++
    if (pStats)
        free(pStats);
    ```

    

Paso siguiente: [Recuperar información mediante GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Paso anterior: [Administración de direcciones IP mediante AddIPAddress y DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 

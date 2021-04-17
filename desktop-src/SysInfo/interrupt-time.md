---
description: El tiempo de interrupción es la cantidad de tiempo transcurrido desde la última vez que se inició el sistema, en intervalos de 100 segundos.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Tiempo de interrupción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018d97ab0eecd1182c02b734357ca13fbe12632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666639"
---
# <a name="interrupt-time"></a>Tiempo de interrupción

El *tiempo de interrupción* es la cantidad de tiempo transcurrido desde la última vez que se inició el sistema, en intervalos de 100 segundos. El recuento de tiempo de interrupción comienza en cero cuando se inicia el sistema y se incrementa en cada interrupción del reloj por la duración de un paso del reloj. La duración exacta de un paso de reloj depende del hardware subyacente y puede variar entre sistemas.

A diferencia de la [hora del sistema](system-time.md), el recuento de tiempo de interrupción no está sujeto a ajustes por los usuarios o el servicio de hora de Windows, lo que lo convierte en una mejor opción para medir duraciones cortas. Las aplicaciones que requieren mayor precisión que el número de tiempo de interrupción deben usar un [temporizador de alta resolución](../winmsg/about-timers.md). Utilice la función [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) para recuperar la frecuencia del temporizador de alta resolución y la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) para recuperar el valor del contador.

Las funciones [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)y [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) se pueden usar para recuperar el recuento de tiempo de interrupción. Tiempo de interrupción no sesgado significa que solo se cuenta el tiempo que el sistema está en el estado de funcionamiento; por lo tanto, el recuento de tiempo de interrupción no se "sesga" por el tiempo que el sistema invierte en suspensión o hibernación.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP/2000:** La función [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) está disponible a partir de Windows 7 y windows Server 2008 R2.

La resolución del temporizador establecida por las funciones [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) y [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) afecta a la resolución de las funciones [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) y [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . Sin embargo, no se recomienda aumentar la resolución del temporizador porque puede reducir el rendimiento general del sistema y aumentar el consumo de energía evitando que el procesador entre en Estados de ahorro de energía. En su lugar, las aplicaciones deben usar un temporizador de alta resolución.

> [!Note]  
> Las funciones [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)y [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) generan resultados diferentes en las compilaciones de depuración ("comprobadas") de Windows, ya que el recuento de ciclos y tiempos de interrupción es de aproximadamente 49 días. Esto ayuda a identificar los errores que podrían no producirse hasta que el sistema se ejecute durante mucho tiempo. La compilación comprobada está disponible para los suscriptores de MSDN a través del sitio web de [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .

 

En el ejemplo siguiente se muestra cómo recuperar el recuento de tiempo de interrupción llamando a las funciones [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)y [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) . Vínculo a la biblioteca OneCore. lib al compilar una aplicación de consola que llama a estas funciones.


```C++
#include "stdafx.h"
#include <windows.h>
#include <realtimeapiset.h>

void InterruptTimeTest()
{
    ULONGLONG InterruptTime;
    ULONGLONG PreciseInterruptTime;
    ULONGLONG UnbiasedInterruptTime;
    ULONGLONG PreciseUnbiasedInterruptTime;

        // The interrupt time that QueryInterruptTime reports is based on the 
        // latest tick of the system clock timer. The system clock timer is 
        // the hardware timer that periodically generates interrupts for the 
        // system clock. The uniform period between system clock timer 
        // interrupts is referred to as a system clock tick, and is typically 
        // in the range of 0.5 milliseconds to 15.625 milliseconds, depending 
        // on the hardware platform. The interrupt time value retrieved by 
        // QueryInterruptTime is accurate within a system clock tick.

    QueryInterruptTime(&InterruptTime);
    printf("Interrupt time: %.7f seconds\n", 
            (double)InterruptTime/(double)10000000);

        // Precise interrupt time is more precise than the interrupt time that
        // QueryInterruptTime reports because the functions that report  
        // precise interrupt time read the timer hardware directly.

    QueryInterruptTimePrecise(&PreciseInterruptTime);
    printf("Precise interrupt time: %.7f seconds\n", 
            (double)PreciseInterruptTime/(double)10000000);

        // Unbiased interrupt time means that only time that the system is in 
        // the working state is counted. Therefore, the interrupt-time count 
        // is not biased by time the system spends in sleep or hibernation.

    QueryUnbiasedInterruptTime(&UnbiasedInterruptTime);
    printf("Unbiased interrupt time: %.7f seconds\n", 
            (double)UnbiasedInterruptTime/(double)10000000);

        // QueryUnbiasedInterruptTimePrecise gets an interrupt-time count
        // that is both unbiased and precise, as defined in the comments
        // included earlier in this example.

    QueryUnbiasedInterruptTimePrecise(&PreciseUnbiasedInterruptTime);
    printf("Precise unbiased interrupt time: %.7f seconds\n", 
            (double)PreciseUnbiasedInterruptTime/(double)10000000);

}

int main(void)
{
    void InterruptTimeTime();

    InterruptTimeTest();
    return(0);
}
```



Para recuperar el tiempo transcurrido que cuentas para la suspensión o hibernación, use la función [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) , o use el contador de rendimiento del sistema de tiempo de actividad. Este contador de rendimiento se puede recuperar de los datos de rendimiento en la clave del registro **HKEY \_ performance \_ Data**. El valor devuelto es un valor de 8 bytes. Para más información, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 

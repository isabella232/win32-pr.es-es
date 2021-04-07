---
description: Windows proporciona las API que puede usar para adquirir marcas de tiempo de alta resolución o intervalos de tiempo de medida.
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: Adquisición de marcas de tiempo de alta resolución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a1300967738b717ab8d8c822bf2af3f6a4a7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003211"
---
# <a name="acquiring-high-resolution-time-stamps"></a>Adquisición de marcas de tiempo de alta resolución

Windows proporciona las API que puede usar para adquirir marcas de tiempo de alta resolución o intervalos de tiempo de medida. La API principal para código nativo es [**QueryPerformanceCounter (QPC)**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). En el caso de los controladores de dispositivo, la API de modo kernel es [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter). En el caso de código administrado, la clase [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) usa **QPC** como la hora exacta.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es independiente de y no se sincroniza con ninguna referencia de hora externa. Para recuperar las marcas de tiempo que se pueden sincronizar con una referencia de hora externa, como la hora universal coordinada (UTC) para su uso en las mediciones de la hora del día de alta resolución, use [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

Las marcas de tiempo y las medidas de intervalo de tiempo son una parte integral de las medidas de rendimiento de la red y del equipo. Estas operaciones de medición de rendimiento incluyen el cálculo del tiempo de respuesta, el rendimiento y la latencia, así como la generación de perfiles de la ejecución de código. Cada una de estas operaciones implica una medición de las actividades que se producen durante un intervalo de tiempo definido por un evento de inicio y de finalización que puede ser independiente de cualquier referencia de hora del día externa.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es normalmente el mejor método que se usa para los eventos de marca de tiempo y mide los pequeños intervalos de tiempo que se producen en el mismo sistema o máquina virtual. Considere la posibilidad de usar [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) cuando desee realizar una marca de tiempo de los eventos en varios equipos, siempre que cada equipo participe en un esquema de sincronización de hora como el protocolo de tiempo de red (NTP). **QPC** ayuda a evitar dificultades que se pueden encontrar con otros enfoques de medición de tiempo, como la lectura directa del contador de marca de tiempo del procesador (TSC).

-   [Compatibilidad con QPC en versiones de Windows](#qpc-support-in-windows-versions)
-   [Instrucciones para adquirir marcas de tiempo](#guidance-for-acquiring-time-stamps)
    -   [Virtualización](#virtualization)
    -   [Uso de TSC directo](#direct-tsc-usage)
    -   [Ejemplos para adquirir marcas de tiempo](#examples-for-acquiring-time-stamps)
-   [Preguntas más frecuentes sobre QPC y TSC](#general-faq-about-qpc-and-tsc)
-   [Preguntas más frecuentes sobre la programación con QPC y TSC](#faq-about-programming-with-qpc-and-tsc)
-   [Características de reloj de hardware de bajo nivel](#low-level-hardware-clock-characteristics)
    -   [Relojes absolutos y relojes de diferencia](#absolute-clocks-and-difference-clocks)
    -   [Resolución, precisión, precisión y estabilidad](#resolution-precision-accuracy-and-stability)
-   [Información del temporizador de hardware](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>Compatibilidad con QPC en versiones de Windows

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) se presentó en Windows 2000 y Windows XP, y ha evolucionado para aprovechar las mejoras en la plataforma de hardware y los procesadores. Aquí se describen las características de **QPC** en diferentes versiones de Windows para ayudarle a mantener el software que se ejecuta en esas versiones de Windows.

### <a name="windows-xp-and-windows-2000"></a>Windows XP y Windows 2000

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) está disponible en Windows XP y Windows 2000 y funciona bien en la mayoría de los sistemas. Sin embargo, el BIOS de algunos sistemas de hardware no indicaba correctamente las características de la CPU de hardware (un TSC no invariable) y algunos sistemas de varios núcleos o varios procesadores usaban procesadores con TSCs que no se podían sincronizar entre núcleos. Los sistemas con firmware defectuoso que ejecuten estas versiones de Windows podrían no proporcionar la misma lectura de **QPC** en diferentes núcleos si usaban el TSC como base para **QPC**.

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista y Windows Server 2008

Todos los equipos incluidos con Windows Vista y Windows Server 2008 usaban un contador de plataforma (temporizador de eventos de alta precisión (HPET)) o el temporizador de administración de energía de ACPI (temporizador PM) como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Estos temporizadores de plataforma tienen una mayor latencia de acceso que el TSC y se comparten entre varios procesadores. Esto limita la escalabilidad de **QPC** si se llama a la vez desde varios procesadores.

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

La mayoría de los equipos con Windows 7 y Windows Server 2008 R2 tienen procesadores con TSCs de velocidad constante y usan estos contadores como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). TSCs son contadores de hardware por procesador de alta resolución a los que se puede tener acceso con una latencia y una sobrecarga muy bajas (en el orden de decenas o cientos de ciclos de equipo, en función del tipo de procesador). Windows 7 y Windows Server 2008 R2 usan TSCs como base de **QPC** en sistemas de dominio de un solo reloj en los que el sistema operativo (o el hipervisor) puede sincronizar estrechamente la TSCs individual en todos los procesadores durante la inicialización del sistema. En estos sistemas, el costo de leer el contador de rendimiento es significativamente menor en comparación con los sistemas que utilizan un contador de plataforma. Además, no hay ninguna sobrecarga adicional para las llamadas simultáneas y las consultas en modo de usuario suelen omitir las llamadas del sistema, lo que reduce aún más la sobrecarga. En los sistemas en los que el TSC no es adecuado para timekeeping, Windows selecciona automáticamente un contador de plataforma (ya sea el temporizador de HPET o el temporizador de la ACPI PM) como base para **QPC**.

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8, Windows 8.1, Windows Server 2012 y Windows Server 2012 R2

Windows 8, Windows 8.1, Windows Server 2012 y Windows Server 2012 R2 usan TSCs como base para el contador de rendimiento. El algoritmo de sincronización de TSC se mejoró significativamente para adaptarse mejor a los sistemas grandes con muchos procesadores. Además, se ha agregado compatibilidad con la nueva API precisa de la hora del día, que permite adquirir marcas de tiempo de reloj de la pared precisas del sistema operativo. Para obtener más información, consulte [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). En las plataformas de PC con Windows RT, el contador de rendimiento se basa en un contador de plataforma de propiedad o en el contador del sistema proporcionado por el temporizador genérico de Windows RT PC si la plataforma está equipada.

## <a name="guidance-for-acquiring-time-stamps"></a>Instrucciones para adquirir marcas de tiempo

Windows tiene y seguirá invirtiendo en proporcionar un contador de rendimiento confiable y eficaz. Cuando necesite marcas de tiempo con una resolución de 1 microsegundo o superior y no necesite que las marcas de tiempo se sincronicen con una referencia de hora externa, elija [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)o [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise). Cuando necesite marcas de tiempo sincronizadas con UTC con una resolución de 1 microsegundo o superior, elija [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) o [**KeQuerySystemTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise).

En un número relativamente pequeño de plataformas que no pueden usar el registro de TSC como base de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) , por ejemplo, por las razones que se explican en [información del temporizador de hardware](#hardware-timer-info), la adquisición de marcas de tiempo de alta resolución puede ser significativamente más costosa que adquirir marcas de tiempo con una resolución inferior. Si la resolución de 10 a 16 milisegundos es suficiente, puede usar [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64), [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)o [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) para obtener las marcas de tiempo que no se sincronizan con una referencia de hora externa. En el caso de las marcas de tiempo sincronizadas con UTC, use [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) o [**KeQuerySystemTime**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1). Si es necesaria una resolución mayor, puede usar [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)o [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) para obtener las marcas de tiempo en su lugar.

En general, los resultados del contador de rendimiento son coherentes en todos los procesadores de los sistemas de varios núcleos y varios procesadores, incluso cuando se miden en diferentes subprocesos o procesos. Estas son algunas excepciones a esta regla:

-   Los sistemas operativos anteriores a Windows Vista que se ejecutan en determinados procesadores podrían infringir esta coherencia debido a una de estas razones:

    -   Los procesadores de hardware tienen un TSC no invariable y el BIOS no indica correctamente esta condición.
    -   El algoritmo de sincronización de TSC que se usó no era adecuado para sistemas con un gran número de procesadores.

-   Al comparar los resultados del contador de rendimiento que se adquieren de distintos subprocesos, considere la posibilidad de que los valores que difieren en ± 1 TICs tengan una ordenación ambigua. Si las marcas de tiempo se toman del mismo subproceso, esta incertidumbre de ± 1 marca no se aplica. En este contexto, el término tick hace referencia a un período de tiempo igual a 1 ÷ (la frecuencia del contador de rendimiento obtenida de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)).

Cuando se usa el contador de rendimiento en sistemas de servidor de gran tamaño con dominios de varios relojes que no están sincronizados en el hardware, Windows determina que el TSC no se puede usar para fines de temporización y selecciona un contador de plataforma como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Aunque este escenario sigue produciendo marcas de tiempo confiables, la latencia de acceso y la escalabilidad se ven afectadas negativamente. Por lo tanto, como se indicó anteriormente en la guía de uso anterior, use solo las API que proporcionan una resolución más o más microsegundos cuando se necesita dicha resolución. El TSC se usa como base para **QPC** en sistemas de dominio de varios relojes que incluyen la sincronización de hardware de todos los dominios de reloj de procesador, ya que de este modo, funcionan como un sistema de dominio de un solo reloj.

La frecuencia del contador de rendimiento se fija en el arranque del sistema y es coherente en todos los procesadores, por lo que solo necesita consultar la frecuencia de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) cuando se inicializa la aplicación y, a continuación, almacenar en caché el resultado.

### <a name="virtualization"></a>Virtualización

Se espera que el contador de rendimiento funcione de forma confiable en todas las máquinas virtuales invitadas que se ejecutan en hipervisores implementados correctamente. Sin embargo, los hipervisores que cumplen con la interfaz de la versión 1,0 del hipervisor y muestran la habilitación del tiempo de referencia pueden ofrecer una sobrecarga sustancialmente inferior. Para obtener más información sobre las interfaces y las optimizaciones de hipervisor, vea [Especificaciones de hipervisor](/virtualization/hyper-v-on-windows/reference/tlfs).

### <a name="direct-tsc-usage"></a>Uso de TSC directo

Se desaconseja encarecidamente el uso de la instrucción de procesador **RDTSC** o **RDTSCP** para consultar directamente el TSC, ya que no se obtendrán resultados confiables en algunas versiones de Windows, en migraciones en vivo de máquinas virtuales y en sistemas de hardware sin invariantes o sincronizados de forma estricta. En su lugar, le recomendamos que use [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) para aprovechar la abstracción, la coherencia y la portabilidad que ofrece.

### <a name="examples-for-acquiring-time-stamps"></a>Ejemplos para adquirir marcas de tiempo

Los diversos ejemplos de código de estas secciones muestran cómo adquirir marcas de tiempo.

### <a name="using-qpc-in-native-code"></a>Usar QPC en código nativo

En este ejemplo se muestra cómo usar [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) en código nativo de C y C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

QueryPerformanceFrequency(&Frequency); 
QueryPerformanceCounter(&StartingTime);

// Activity to be timed

QueryPerformanceCounter(&EndingTime);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;


//
// We now have the elapsed number of ticks, along with the
// number of ticks-per-second. We use these values
// to convert to the number of elapsed microseconds.
// To guard against loss-of-precision, we convert
// to microseconds *before* dividing by ticks-per-second.
//

ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



### <a name="acquiring-high-resolution-time-stamps-from-managed-code"></a>Adquirir marcas de tiempo de alta resolución del código administrado

En este ejemplo se muestra cómo usar la clase Managed code [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) .


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



La clase [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) también proporciona varios métodos cómodos para realizar mediciones de intervalos de tiempo.

### <a name="using-qpc-from-kernel-mode"></a>Usar QPC desde el modo kernel

El kernel de Windows proporciona acceso de modo kernel al contador de rendimiento a través de [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) desde el que se pueden obtener tanto el contador de rendimiento como la frecuencia de rendimiento. **KeQueryPerformanceCounter** solo está disponible en modo kernel y se proporciona para los escritores de controladores de dispositivos y otros componentes de modo kernel.

En este ejemplo se muestra cómo usar [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) en el modo kernel de C y C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

StartingTime = KeQueryPerformanceCounter(&Frequency);

// Activity to be timed

EndingTime = KeQueryPerformanceCounter(NULL);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;
ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



## <a name="general-faq-about-qpc-and-tsc"></a>Preguntas más frecuentes sobre QPC y TSC

Este documento contiene respuestas a las preguntas más frecuentes sobre [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y TSCs en general.

<dl> <dt>

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**¿Es QueryPerformanceCounter () el mismo que la función GetTickCount de Win32 () o GetTickCount64 ()?**
</dt> <dd>

No. [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) y [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) no están relacionados con [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). **GetTickCount** y **GetTickCount64** devuelven el número de milisegundos transcurridos desde que se inició el sistema.

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**¿Debo usar QPC o llamar a las instrucciones de RDTSC/RDTSCP directamente?**
</dt> <dd>

Para evitar problemas de inexactitud y portabilidad, recomendamos encarecidamente que use [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) en lugar de usar el registro de TSC o las instrucciones de procesador **RDTSC** o **RDTSCP** .

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**¿Cuál es la relación de QPC con una hora de tiempo externa? ¿Se puede sincronizar con una época externa, como UTC?**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) se basa en un contador de hardware que no se puede sincronizar con una referencia de hora externa, como la hora UTC. Para obtener las marcas de tiempo exactas del día que se pueden sincronizar con una referencia UTC externa, use [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**¿Es QPC afectado por el horario de verano, los segundos bisiestos, las zonas horarias o los cambios de hora del sistema realizados por el administrador?**
</dt> <dd>

No. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es completamente independiente de la hora del sistema y UTC.

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**¿La precisión QPC se ve afectada por los cambios de frecuencia del procesador causados por la administración de energía o la tecnología Turbo Boost?**
</dt> <dd>

No. Si el procesador tiene un TSC invariable, el [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) no se ve afectado por este tipo de cambios. Si el procesador no tiene un TSC invariable, **QPC** revertirá a un temporizador de hardware de plataforma que no se verá afectado por los cambios de frecuencia del procesador o la tecnología Turbo Boost.

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**¿QPC funciona de forma confiable en sistemas de varios procesadores, sistemas de varios núcleos y sistemas con Hyper-Threading?**
</dt> <dd>

Sí

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**Cómo determinar y validar que QPC funciona en mi máquina?**
</dt> <dd>

No es necesario realizar estas comprobaciones.

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**¿Qué procesadores tienen TSCs no invariables? ¿Cómo puedo comprobar si el sistema tiene un TSC no invariable?**
</dt> <dd>

No es necesario realizar esta comprobación. Los sistemas operativos Windows realizan varias comprobaciones en la inicialización del sistema para determinar si el TSC es adecuado como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Sin embargo, por motivos de referencia, puede determinar si el procesador tiene un TSC de invariable mediante uno de estos:

-   la utilidad de Coreinfo.exe de Windows Sysinternals
-   comprobar los valores devueltos por la instrucción CPUID relativa a las características de TSC
-   la documentación del fabricante del procesador

A continuación se muestra la información de TSC-invariable proporcionada por la utilidad de Coreinfo.exe de Windows Sysinternals ([www.sysinternals.com](https://www.sysinternals.com)). Un asterisco significa "true".

``` syntax
> Coreinfo.exe 

Coreinfo v3.2 - Dump information on system CPU and memory topology
Copyright (C) 2008-2012 Mark Russinovich
Sysinternals - www.sysinternals.com

 <unrelated text removed>

RDTSCP          * Supports RDTSCP instruction
TSC             * Supports RDTSC instruction
TSC-DEADLINE    - Local APIC supports one-shot deadline timer
TSC-INVARIANT   * TSC runs at constant rate
```

</dd> <dt>

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**¿QPC funciona de forma confiable en las plataformas de hardware de equipos con Windows RT?**
</dt> <dd>

Sí

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**¿Con qué frecuencia se revierte QPC?**
</dt> <dd>

No menos de 100 años desde el arranque del sistema más reciente y, posiblemente, se basa en el temporizador de hardware subyacente usado. Para la mayoría de las aplicaciones, la sustitución no es un problema.

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**¿Cuál es el costo computacional de llamar a QPC?**
</dt> <dd>

El costo de la llamada de cálculo de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) está determinado principalmente por la plataforma de hardware subyacente. Si el registro de TSC se utiliza como base para QPC, el costo computacional se determina principalmente por el tiempo que tarda el procesador en procesar una instrucción **RDTSC** . Este intervalo de tiempo va de decenas de ciclos de CPU a varios cientos de ciclos de CPU según el procesador utilizado. Si no se puede usar el TSC, el sistema seleccionará una base de tiempo de hardware diferente. Dado que estas bases de tiempo se encuentran en la placa base (por ejemplo, en el puente de sur de PCI o en el PCH), el costo de cálculo por llamada es mayor que el TSC y, con frecuencia, en proximidad de 0,8-1,0 microsegundos según la velocidad del procesador y otros factores de hardware. Este costo está dominado por el tiempo necesario para tener acceso al dispositivo de hardware de la placa base.

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**¿Requiere QPC una transición del kernel (llamada del sistema)?**
</dt> <dd>

No es necesario realizar una transición del kernel si el sistema puede utilizar el registro de TSC como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Si el sistema debe usar una base de tiempo diferente, como el temporizador HPET o PM, se requiere una llamada del sistema.

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**¿El contador de rendimiento es monotónico (no en disminución)?**
</dt> <dd>

Sí

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**¿Se puede usar el contador de rendimiento para ordenar eventos en el tiempo?**
</dt> <dd>

Sí. Sin embargo, al comparar los resultados del contador de rendimiento que se adquieren de distintos subprocesos, los valores que difieren entre ± 1 TICs tienen una ordenación ambigua como si tuvieran una marca de tiempo idéntica.

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**¿Qué precisión tiene el contador de rendimiento?**
</dt> <dd>

La respuesta depende de diversos factores. Para obtener más información, vea [características del reloj de hardware de bajo nivel](#low-level-hardware-clock-characteristics).

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>Preguntas más frecuentes sobre la programación con QPC y TSC

Este documento contiene respuestas a las preguntas más frecuentes sobre la programación con [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y TSCs.

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**Necesito convertir el resultado de QPC en milisegundos. ¿Cómo se puede evitar la pérdida de precisión con la conversión a Double o float?**
</dt> <dd>

Hay varios aspectos que se deben tener en cuenta al realizar cálculos en contadores de rendimiento enteros:

-   La división de enteros perderá el resto. Esto puede provocar la pérdida de precisión en algunos casos.
-   La conversión entre enteros de 64 bits y punto flotante (Double) puede provocar la pérdida de precisión porque la mantisa de punto flotante no puede representar todos los valores enteros posibles.
-   La multiplicación de enteros de 64 bits puede producir un desbordamiento de enteros.

Como principio general, retrase estos cálculos y conversiones siempre que sea posible para evitar la composición de los errores introducidos.

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**¿Cómo puedo convertir QPC a TICs de 100 nanosegundos para poder agregarlo a un FILETIME?**
</dt> <dd>

Una hora de archivo es un valor de 64 bits que representa el número de intervalos de 100 segundos que han transcurrido desde la 12:00 A.M. 1 de enero de 1601 hora universal coordinada (UTC). Los tiempos de archivo se usan en las llamadas de la API de Win32 que devuelven la hora del día, como [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) y [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Por el contrario, [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) devuelve valores que representan el tiempo en unidades de 1/(la frecuencia del contador de rendimiento obtenida de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)). La conversión entre los dos requiere calcular la relación entre el intervalo de **QPC** y los intervalos de 100-nanosegundos. Tenga cuidado de evitar la pérdida de precisión porque los valores pueden ser pequeños (0,0000001/0,000000340).

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**¿Por qué la marca de tiempo que se devuelve de QPC es un entero con signo?**
</dt> <dd>

Los cálculos que implican marcas de tiempo de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) pueden implicar la resta. Mediante el uso de un valor con signo, puede controlar los cálculos que pueden producir valores negativos.

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**¿Cómo puedo obtener marcas de tiempo de alta resolución del código administrado?**
</dt> <dd>

Llame al método [**Stopwatch. GetTimeStamp**](/previous-versions/windows/) desde la clase [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) . Para obtener un ejemplo sobre cómo usar **Stopwatch. GetTimeStamp**, vea [adquirir marcas de tiempo de alta resolución del código administrado](#acquiring-high-resolution-time-stamps-from-managed-code).

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**En ¿en qué circunstancias QueryPerformanceFrequency devuelve FALSE, o QueryPerformanceCounter devuelve cero?**
</dt> <dd>

Esto no ocurre en ningún sistema que ejecute Windows XP o posterior.

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**¿Es necesario establecer la afinidad de subprocesos en un solo núcleo para usar QPC?**
</dt> <dd>

No. Para obtener más información, consulte la [Guía para adquirir marcas de tiempo](#guidance-for-acquiring-time-stamps). Este escenario no es necesario ni deseable. La realización de este escenario puede afectar negativamente al rendimiento de la aplicación mediante la restricción del procesamiento a un núcleo o la creación de un cuello de botella en un solo núcleo si varios subprocesos establecen su afinidad en el mismo núcleo al llamar a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>Características de reloj de hardware de bajo nivel

En estas secciones se muestran las características de reloj de hardware de bajo nivel.

### <a name="absolute-clocks-and-difference-clocks"></a>Relojes absolutos y relojes de diferencia

Los relojes absolutos proporcionan lecturas precisas de la hora del día. Normalmente se basan en la hora universal coordinada (UTC) y, por consiguiente, su exactitud depende en parte de lo bien que se sincronizan con una referencia de hora externa. Los relojes de diferencia miden los intervalos de tiempo y no suelen basarse en un tiempo externo. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es un reloj de diferencia y no se sincroniza con un tiempo o una referencia externos. Cuando se usa **QPC** para las mediciones de intervalos de tiempo, normalmente se obtiene una mejor precisión que el uso de marcas de tiempo que se derivan de un reloj absoluto. Esto se debe a que el proceso de sincronización de la hora de un reloj absoluto puede introducir turnos de fase y frecuencia que aumentan la incertidumbre de las mediciones de intervalo de tiempo a corto plazo.

### <a name="resolution-precision-accuracy-and-stability"></a>Resolución, precisión, precisión y estabilidad

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) usa un contador de hardware como base. Los temporizadores de hardware constan de tres partes: un generador de TICs, un contador que cuenta los tics y un medio para recuperar el valor del contador. Las características de estos tres componentes determinan la resolución, la precisión, la precisión y la estabilidad de **QPC**.

Si un generador de hardware proporciona TICs a una velocidad constante, los intervalos de tiempo se pueden medir simplemente contando estos TICs. La velocidad a la que se generan los tics se denomina frecuencia y se expresa en hercios (Hz). El recíproco de la frecuencia se denomina período o intervalo de TICs y se expresa en una unidad de tiempo del sistema internacional de unidades (SI) adecuada (por ejemplo, segundo, milisegundo, microsegundo o nanosegundos).

![intervalo de tiempo](images/tick-interval.png)

La resolución del temporizador es igual al período. La resolución determina la capacidad de distinguir entre dos marcas de tiempo cualesquiera y coloca un límite inferior en los intervalos de tiempo más pequeños que se pueden medir. A veces, esto se denomina resolución de marca.

La medición digital del tiempo introduce una incertidumbre de medidas de ± 1 TIC porque el contador digital avanza en pasos discretos, mientras que el tiempo avanza continuamente. Esta incertidumbre se denomina error de cuantificación. En el caso de las mediciones de intervalos de tiempo habituales, este efecto se puede pasar por alto a menudo porque el error de cuantificación es mucho menor que el intervalo de tiempo que se está midiendo.

![medida de tiempo digital](images/digital-time-measure.png)

Sin embargo, si el período que se va a medir es pequeño y se aproxima a la resolución del temporizador, tendrá que considerar este error de cuantificación. El tamaño del error introducido es el de un período de reloj.

Los dos diagramas siguientes ilustran el impacto de la incertidumbre de la ± 1 marca mediante un temporizador con una resolución de 1 unidad de tiempo.

![incertidumbre de marca](images/tick-uncertainty.png)

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) devuelve la frecuencia de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)y el punto y la resolución son iguales que el recíproco de este valor. La frecuencia del contador de rendimiento que **QueryPerformanceFrequency** devuelve se determina durante la inicialización del sistema y no cambia mientras se ejecuta el sistema.

> [!Note]  
> Pueden existir casos en los que [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) no devuelva la frecuencia real del generador de TICs de hardware. Por ejemplo, en muchos casos, **QueryPerformanceFrequency** devuelve la frecuencia de TSC dividida entre 1024; y en Hyper-V, la frecuencia del contador de rendimiento es siempre de 10 MHz cuando la máquina virtual invitada se ejecuta en un [hipervisor](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) que implementa la interfaz de la [versión 1,0 del hipervisor](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx). Como resultado, no suponga que **QueryPerformanceFrequency** devolverá la frecuencia de TSC exacta.

 

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) lee el contador de rendimiento y devuelve el número total de pasos que se han producido desde que se inició el sistema operativo Windows, incluida la hora en que el equipo estuvo en un estado de suspensión, como en espera, hibernación o en modo de espera conectado.

En estos ejemplos se muestra cómo calcular el intervalo de TICs y la resolución y cómo convertir el contador en un valor de hora.

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Ejemplo 1**
</dt> <dd>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) devuelve el valor 3.125.000 en un equipo determinado. ¿Cuál es el intervalo de pasos y la resolución de las medidas [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) en esta máquina? El intervalo de marca, o punto, es el recíproco de 3.125.000, que es 0,000000320 (320 nanosegundos). Por lo tanto, cada TIC representa el paso de 320 nanosegundos. Los intervalos de tiempo inferiores a 320 nanosegundos no se pueden medir en este equipo.

Intervalo entre TICs = 1/(frecuencia de rendimiento)

Intervalo entre TICs = 1/3125000 = 320 NS

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Ejemplo 2**
</dt> <dd>

En el mismo equipo que en el ejemplo anterior, la diferencia de los valores devueltos por dos llamadas sucesivas a [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es 5. ¿Cuánto tiempo ha transcurrido entre las dos llamadas? 5 TICs multiplicados por 320 nanosegundos produce 1,6 microsegundos.

ElapsedTime = intervalo de \* TICs de TICs

ElapsedTime = 5 \* 320 NS = 1,6 μs

</dd> </dl>

Se tarda en acceder (leer) el contador desde el software y este tiempo de acceso puede reducir la precisión del de la medición de tiempo. Esto se debe a que el tiempo de intervalo mínimo (el intervalo de tiempo más pequeño que se puede medir) es el mayor de la resolución y el tiempo de acceso.

Precisión = \[ resolución máxima, AccessTime\]

Por ejemplo, considere un temporizador de hardware hipotético con una resolución de 100 nanosegundos y un tiempo de acceso de 800 nanosegundos. Este podría ser el caso si se usara el temporizador de plataforma en lugar del registro de TSC como base de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Por lo tanto, la precisión sería de 800 nanosegundos y no 100 nanosegundos, tal como se muestra en este cálculo.

Precisión = MAX \[ 800 NS, 100 NS \] = 800 NS

Estas dos figuras describen este efecto.

![tiempo de acceso de QPC](images/qpc-access-time.png)

Si el tiempo de acceso es mayor que la resolución, no intente mejorar la precisión mediante adivinación. En otras palabras, es un error asumir que la marca de tiempo se toma exactamente en el centro, o al principio o al final de la llamada.

Por el contrario, considere el siguiente ejemplo en el que el tiempo de acceso [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es solo de 20 nanosegundos y la resolución del reloj de hardware es de 100 nanosegundos. Este podría ser el caso si se usó el registro de TSC como base para **QPC**. Aquí la precisión está limitada por la resolución del reloj.

![precisión de QPC](images/qpc-precision.png)

En la práctica, puede buscar los orígenes de hora para los que el tiempo necesario para leer el contador es mayor o menor que la resolución. En cualquier caso, la precisión será la más grande de las dos.

En esta tabla se proporciona información sobre la resolución aproximada, el tiempo de acceso y la precisión de una variedad de relojes. Tenga en cuenta que algunos de los valores variarán con diferentes procesadores, plataformas de hardware y velocidades de procesador.



| Origen del reloj                                                      | Frecuencia del reloj nominal | Resolución del reloj    | Tiempo de acceso (típico) | Precisión       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| RTC DE PC                                                            | 64 Hz                   | 15,625 milisegundos | N/D                   | N/D             |
| Contador de rendimiento de consultas mediante TSC con un reloj de procesador de 3 GHz  | 3 MHz                   | 333 nanosegundos     | 30 nanosegundos        | 333 nanosegundos |
| **RDTSC** instrucción máquina en un sistema con un ciclo de 3 GHz | 3 GHz                   | 333 picoseconds     | 30 nanosegundos        | 30 nanosegundos  |



 

Dado que [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) usa un contador de hardware, cuando comprenda algunas características básicas de los contadores de hardware, conocerá las capacidades y limitaciones de **QPC**.

El generador de TICs de hardware que se usa con más frecuencia es un oscilador de cristal. Crystal es una pequeña pieza de cuarzo u otro material cerámico que exhibe características de Piezoelectric que proporcionan una referencia de frecuencia económica con una estabilidad y precisión excelentes. Esta frecuencia se usa para generar los tics contados por el reloj.

La precisión de un temporizador hace referencia al grado de conformidad con un valor true o estándar. Esto depende principalmente de la capacidad del oscilador de cristal para proporcionar TICs con la frecuencia especificada. Si la frecuencia de oscilación es demasiado alta, el reloj se ejecutará rápidamente y los intervalos medidos aparecerán más tiempo del que son. y si la frecuencia es demasiado baja, el reloj se ejecutará lentamente y los intervalos medidos aparecerán más cortos que en realidad.

En el caso de las medidas típicas de intervalo de tiempo para una duración corta (por ejemplo, medidas de tiempo de respuesta, medidas de latencia de red, etc.), la precisión del oscilador de hardware suele ser suficiente. Sin embargo, para algunas mediciones la precisión de la frecuencia del oscilador es importante, especialmente para los intervalos de tiempo largos o cuando se desea comparar las medidas tomadas en diferentes equipos. En el resto de esta sección se exploran los efectos de la precisión del oscilador.

La frecuencia de la oscilación de los cristales se establece durante el proceso de fabricación y la especifica el fabricante en términos de una frecuencia especificada más o menos una tolerancia de fabricación expresada en ' partes por millón ' (ppm), denominada el desplazamiento de frecuencia máximo. Un cristal con una frecuencia especificada de 1 millón Hz y un desplazamiento de frecuencia máximo de ± 10 ppm se encontrarán dentro de los límites de especificación si su frecuencia real estaba entre 999.990 Hz y 1.000.010 Hz.

Al sustituir las partes de la frase por millón de microsegundos por segundo, se puede aplicar este error de desplazamiento de frecuencia a las mediciones de intervalo de tiempo. Un oscilador con un desfase + 10 ppm producirá un error de 10 microsegundos por segundo. En consecuencia, al medir un intervalo de 1 segundo, se ejecutaría rápido y mediría un intervalo de 1 segundo como 0,999990 segundos.

Una referencia adecuada es que un error de frecuencia de 100 ppm produce un error de 8,64 segundos después de 24 horas. En esta tabla se presenta la incertidumbre de medición debido al error acumulado durante intervalos de tiempo más largos.



| Duración del intervalo de tiempo | Incertidumbre de medición debido a un error acumulado con una tolerancia de frecuencia de +/-10 PPM |
|------------------------|--------------------------------------------------------------------------------------|
| 1 microsegundo          | ± 10 picoseconds (10-12)                                                             |
| 1 milisegundo          | ± 10 nanosegundos (10-9)                                                              |
| 1 segundo               | ± 10 microsegundos                                                                    |
| 1 hora                 | ± 60 microsegundos                                                                    |
| 1 día                  | ± 0,86 segundos                                                                       |
| 1 semana                 | ± 6,08 segundos                                                                       |



 

En la tabla anterior se muestra que para los intervalos de tiempo pequeños, a menudo se puede pasar por alto el error de desplazamiento de frecuencia. Sin embargo, en intervalos de tiempo prolongados, incluso un pequeño desplazamiento de frecuencia puede dar lugar a una incertidumbre de medición sustancial.

Los microosciladores que se usan en equipos y servidores personales se fabrican normalmente con una tolerancia de frecuencia de ± 30 a 50 partes por millón y, en raras ocasiones, los cristales pueden estar desactivados hasta 500 ppm. Aunque los cristales con tolerancias de desplazamiento de frecuencia mucho más estrictas están disponibles, son más caros y, por tanto, no se usan en la mayoría de los equipos.

Para reducir los efectos adversos de este error de desplazamiento de frecuencia, las versiones recientes de Windows, especialmente Windows 8, usan varios temporizadores de hardware para detectar el desplazamiento de frecuencia y compensarlo en la medida de lo posible. Este proceso de calibración se realiza cuando se inicia Windows.

Como muestran los ejemplos siguientes, el error de desplazamiento de frecuencia de un reloj de hardware influye en la precisión alcanzable y la resolución del reloj puede ser menos importante.

![el error de desplazamiento de frecuencia afecta a la precisión alcanzable](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Ejemplo 1**
</dt> <dd>

Supongamos que realiza mediciones de intervalo de tiempo mediante un oscilador de 1 MHz, que tiene una resolución de un microsegundo y un error de desplazamiento de frecuencia máximo de ± 50 ppm. Ahora, supongamos que el desplazamiento es exactamente + 50 ppm. Esto significa que la frecuencia real sería de 1.000.050 Hz. Si medimos un intervalo de tiempo de 24 horas, nuestra medida sería de 4,3 segundos demasiado corto (23:59:55.700000 medidos en lugar de 24:00:00.000000 real).

Segundos en un día = 86400

Error de desplazamiento de frecuencia = 50 ppm = 0,00005

86.400 segundos \* 0,00005 = 4,3 segundos

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Ejemplo 2**
</dt> <dd>

Supongamos que el reloj del TSC del procesador está controlado por un oscilador de cristal y tiene una frecuencia especificada de 3 GHz. Esto significa que la resolución sería 1/3000000000 o aproximadamente 333 picoseconds. Supongamos que el cristal que se usa para controlar el reloj del procesador tiene una tolerancia de frecuencia de ± 50 ppm y es en realidad + 50 ppm. A pesar de la resolución impresionante, una medición del intervalo de tiempo de 24 horas seguirá siendo 4,3 segundos demasiado corto. (23:59:55.7000000000 medido frente a 24:00:00.0000000000 real).

Segundos en un día = 86400

Error de desplazamiento de frecuencia = 50 ppm = 0,00005

86.400 segundos \* 0,00005 = 4,3 segundos

Esto muestra que un reloj de TSC de alta resolución no proporciona necesariamente medidas más precisas que un reloj de resolución inferior.

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Ejemplo 3**
</dt> <dd>

Considere la posibilidad de usar dos equipos diferentes para medir el mismo intervalo de tiempo de 24 horas. Ambos equipos tienen un oscilador con un desplazamiento de frecuencia máximo de ± 50 ppm. ¿Qué diferencia hay entre la medida del mismo intervalo de tiempo en estos dos sistemas? Como en los ejemplos anteriores, ± 50 ppm produce un error máximo de ± 4,3 segundos después de 24 horas. Si un sistema se ejecuta 4,3 segundos con rapidez y los otros 4,3 segundos, el error máximo después de 24 horas puede ser de 8,6 segundos.

Segundos en un día = 86400

Error de desplazamiento de frecuencia = ± 50 ppm = ± 0,00005

± (86.400 segundos \* 0,00005) = ± 4,3 segundos

Desplazamiento máximo entre los dos sistemas = 8,6 segundos

En Resumen, el error de desplazamiento de frecuencia es cada vez más importante cuando se miden intervalos de tiempo prolongados y cuando se comparan medidas entre distintos sistemas.

La estabilidad de un temporizador describe si la frecuencia de la marca cambia con el tiempo, por ejemplo, como resultado de los cambios de temperatura. Los cristales de cuarzo usados como generadores de TICs en los equipos presentarán pequeños cambios de frecuencia como una función de temperatura. El error provocado por el desfase térmico suele ser pequeño en comparación con el error de desplazamiento de frecuencia para los intervalos de temperatura comunes. Sin embargo, es posible que los diseñadores de software para equipos portátiles o equipos sujetos a fluctuaciones de temperatura grandes tengan que tener en cuenta este efecto.

</dd> </dl>

## <a name="hardware-timer-info"></a>Información del temporizador de hardware

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**Registro de TSC**
</dt> <dd>

Algunos procesadores Intel y AMD contienen un registro de TSC que es un registro de 64 bits que aumenta a una velocidad alta, normalmente igual al reloj del procesador. El valor de este contador puede leerse en las instrucciones de la máquina **RDTSC** o **RDTSCP** , lo que proporciona un tiempo de acceso muy bajo y un costo computacional en el orden de decenas o centenares de ciclos del equipo, dependiendo del procesador.

Aunque el registro de TSC parece un mecanismo de marca de tiempo ideal, aquí se indican las circunstancias en las que no puede funcionar de forma confiable con fines de timekeeping:

-   No todos los procesadores tienen registros de TSC, por lo que el uso del registro de TSC en el software crea directamente un problema de portabilidad. (Windows seleccionará un origen de hora alternativo para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) en este caso, lo que evita el problema de portabilidad).
-   Algunos procesadores pueden variar la frecuencia del reloj de TSC o detener el avance del registro de TSC, lo que hace que el TSC no sea adecuado para fines de control de tiempo en estos procesadores. Se dice que estos procesadores tienen registros de TSC no invariable. (Windows lo detectará automáticamente y seleccionará un origen de hora alternativo para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   En sistemas de varios procesadores o varios núcleos, algunos procesadores y sistemas no pueden sincronizar los relojes de cada núcleo con el mismo valor. (Windows lo detectará automáticamente y seleccionará un origen de hora alternativo para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   En algunos sistemas de varios procesadores de gran tamaño, es posible que no pueda sincronizar los relojes del procesador con el mismo valor aunque el procesador tenga un TSC invariable. (Windows lo detectará automáticamente y seleccionará un origen de hora alternativo para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Algunos procesadores ejecutarán las instrucciones de forma desordenada. Esto puede dar lugar a recuentos de ciclos incorrectos cuando se usa **RDTSC** para las secuencias de instrucciones, ya que la instrucción **RDTSC** se puede ejecutar en un momento diferente del especificado en el programa. La instrucción **RDTSCP** se ha introducido en algunos procesadores en respuesta a este problema.

Al igual que otros temporizadores, el TSC se basa en un oscilador de cristal cuya frecuencia exacta no se conoce de antemano y que tiene un error de desplazamiento de frecuencia. Por lo tanto, antes de que se pueda usar, se debe calibrar mediante otra referencia de control de tiempo.

Durante la inicialización del sistema, Windows comprueba si el TSC es adecuado para fines de temporización y realiza la calibración de frecuencia y la sincronización de núcleos necesarias.

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**Reloj PM**
</dt> <dd>

El temporizador de ACPI, también conocido como el reloj PM, se ha agregado a la arquitectura del sistema para proporcionar marcas de tiempo confiables independientemente de la velocidad de los procesadores. Dado que este era el único objetivo de este temporizador, proporciona una marca de tiempo en un solo ciclo de reloj, pero no proporciona ninguna otra funcionalidad.

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**Temporizador de HPET**
</dt> <dd>

Intel y Microsoft desarrolló conjuntamente el temporizador de eventos de alta precisión (HPET) para satisfacer los requisitos de control de tiempo de multimedia y otras aplicaciones que dependen del tiempo. La compatibilidad con HPET se ha realizado en Windows, ya que la certificación del logotipo de hardware de Windows Vista y Windows 7 y Windows 8 requiere compatibilidad con HPET en la plataforma de hardware.

</dd> </dl>

 

 

---
description: Windows proporciona API que puede usar para adquirir marcas de tiempo de alta resolución o medir intervalos de tiempo.
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: Adquisición de marcas de tiempo de alta resolución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e25c50cb602dd7e5c53c967c12321ec02a6ea68613767f4019b2def7f5793b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764637"
---
# <a name="acquiring-high-resolution-time-stamps"></a>Adquisición de marcas de tiempo de alta resolución

Windows proporciona API que puede usar para adquirir marcas de tiempo de alta resolución o medir intervalos de tiempo. La API principal del código nativo [**es QueryPerformanceCounter (QPC).**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Para los controladores de dispositivo, la API en modo kernel [**es KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter). Para el código administrado, la [**clase System.Diagnostics.Stopwatch**](/previous-versions/windows/) usa **QPC** como base de tiempo precisa.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es independiente de y no se sincroniza con ninguna referencia de hora externa. Para recuperar marcas de tiempo que se pueden sincronizar con una referencia de hora externa, como hora universal coordinada (UTC) para su uso en medidas de hora del día de alta resolución, use [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

Las marcas de tiempo y las medidas de intervalo de tiempo son una parte integral de las medidas de rendimiento de red y equipo. Estas operaciones de medición de rendimiento incluyen el cálculo del tiempo de respuesta, el rendimiento y la latencia, así como la ejecución de código de generación de perfiles. Cada una de estas operaciones implica una medición de las actividades que se producen durante un intervalo de tiempo definido por un evento de inicio y de finalización que puede ser independiente de cualquier referencia de hora del día externa.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) suele ser el mejor método para usar eventos de marca de tiempo y medir intervalos de tiempo pequeños que se producen en el mismo sistema o máquina virtual. Considere la posibilidad de usar [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) cuando desee eventos de marca de tiempo en varios equipos, siempre que cada máquina participe en un esquema de sincronización de hora, como el Protocolo de hora de red (NTP). **QPC** ayuda a evitar dificultades que se pueden encontrar con otros enfoques de medición de tiempo, como leer directamente el contador de marca de tiempo (TSC) del procesador.

-   [Compatibilidad con QPC en Windows versiones anteriores](#qpc-support-in-windows-versions)
-   [Guía para adquirir marcas de tiempo](#guidance-for-acquiring-time-stamps)
    -   [Virtualización](#virtualization)
    -   [Uso directo de TSC](#direct-tsc-usage)
    -   [Ejemplos para adquirir marcas de tiempo](#examples-for-acquiring-time-stamps)
-   [Preguntas más frecuentes generales sobre QPC y TSC](#general-faq-about-qpc-and-tsc)
-   [Preguntas más frecuentes sobre la programación con QPC y TSC](#faq-about-programming-with-qpc-and-tsc)
-   [Características del reloj de hardware de bajo nivel](#low-level-hardware-clock-characteristics)
    -   [Relojes absolutos y relojes de diferencia](#absolute-clocks-and-difference-clocks)
    -   [Resolución, precisión, precisión y estabilidad](#resolution-precision-accuracy-and-stability)
-   [Información del temporizador de hardware](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>Compatibilidad con QPC en Windows versiones anteriores

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) se introdujo en Windows 2000 y Windows XP y ha evolucionado para aprovechar las mejoras en la plataforma de hardware y los procesadores. Aquí se describen las características de **QPC** en diferentes versiones de Windows para ayudarle a mantener el software que se ejecuta en esas Windows versiones.

### <a name="windows-xp-and-windows-2000"></a>Windows XP y Windows 2000

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) está disponible en Windows XP y Windows 2000 y funciona bien en la mayoría de los sistemas. Sin embargo, el BIOS de algunos sistemas de hardware no indicaba correctamente las características de CPU de hardware (un TSC no invariable) y algunos sistemas de varios núcleos o de varios procesadores usaban procesadores con TSC que no se podían sincronizar entre núcleos. Es posible que los sistemas con firmware defectuoso que ejecutan estas versiones de Windows no proporcionen la misma lectura de **QPC** en distintos núcleos si usaron el TSC como base para **QPC.**

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista y Windows Server 2008

Todos los equipos que se enviaron con Windows Vista y Windows Server 2008 usaron un contador de plataforma (temporizador de eventos de alta precisión (HPET)) o el temporizador de administración de energía ACPI (temporizador de PM) como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Estos temporizadores de plataforma tienen una latencia de acceso mayor que el TSC y se comparten entre varios procesadores. Esto limita la escalabilidad de **QPC** si se llama simultáneamente desde varios procesadores.

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

La mayoría de Windows 7 y Windows Server 2008 R2 tienen procesadores con TSC de velocidad constante y usan estos contadores como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Los TSC son contadores de hardware por procesador de alta resolución a los que se puede acceder con una latencia y sobrecarga muy bajas (en el orden de 10 o 100 de ciclos de máquina, según el tipo de procesador). Windows 7 y Windows Server 2008 R2 usan TSC como base de **QPC** en sistemas de dominio de reloj único donde el sistema operativo (o el hipervisor) puede sincronizar estrechamente los TSC individuales en todos los procesadores durante la inicialización del sistema. En estos sistemas, el costo de leer el contador de rendimiento es significativamente menor en comparación con los sistemas que usan un contador de plataforma. Además, no hay ninguna sobrecarga adicional para las llamadas simultáneas y las consultas en modo de usuario a menudo omiten las llamadas del sistema, lo que reduce aún más la sobrecarga. En los sistemas en los que el TSC no es adecuado para la conservación del tiempo, Windows selecciona automáticamente un contador de plataforma (ya sea el temporizador HPET o el temporizador ACPI PM) como base para **QPC**.

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8, Windows 8.1, Windows Server 2012 y Windows Server 2012 R2

Windows 8, Windows 8.1, Windows Server 2012 y Windows Server 2012 R2 usan TSC como base para el contador de rendimiento. El algoritmo de sincronización de TSC se mejoró significativamente para adaptarse mejor a sistemas grandes con muchos procesadores. Además, se ha agregado compatibilidad con la nueva API de hora del día precisa, lo que permite adquirir marcas de tiempo precisas del reloj del sistema operativo. Para obtener más información, [**vea GetSystemTimePreciseAsFileTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) En Windows RT plataformas de PC, el contador de rendimiento se basa en un contador de plataforma propietario o en el contador del sistema proporcionado por el temporizador genérico de pc de Windows RT si la plataforma está tan equipado.

## <a name="guidance-for-acquiring-time-stamps"></a>Guía para adquirir marcas de tiempo

Windows y seguirán invirtiendo en proporcionar un contador de rendimiento confiable y eficaz. Si necesita marcas de tiempo con una resolución de 1 microsegundo o superior y no necesita que las marcas de tiempo se sincronicen con una referencia de hora externa, elija [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)o [**KeQueryInterruptTimePrecise.**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) Cuando necesite marcas de tiempo sincronizadas con UTC con una resolución de 1 microsegundo o superior, elija [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) o [**KeQuerySystemTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise).

En un número relativamente pequeño de plataformas que no pueden usar el registro de TSC como base de [**QPC,**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) por ejemplo, por motivos explicados en Información del temporizador de [hardware,](#hardware-timer-info)la adquisición de marcas de tiempo de alta resolución puede ser significativamente más costosa que adquirir marcas de tiempo con una resolución más baja. Si la resolución de 10 a 16 milisegundos es suficiente, puede usar [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64), [**QueryInterruptTime,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) [**QueryUnbiasedInterruptTime,**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)o [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) para obtener marcas de tiempo que no están sincronizadas con una referencia de hora externa. Para las marcas de tiempo sincronizadas con UTC, use [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) o [**KeQuerySystemTime.**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1) Si se necesita una resolución mayor, puede usar [**QueryInterruptTimePrecise,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise) [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)o [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) para obtener marcas de tiempo en su lugar.

En general, los resultados del contador de rendimiento son coherentes en todos los procesadores de sistemas de varios núcleos y de varios procesadores, incluso cuando se miden en subprocesos o procesos diferentes. Estas son algunas excepciones a esta regla:

-   Los sistemas Windows vista previos que se ejecutan en determinados procesadores podrían infringir esta coherencia debido a uno de estos motivos:

    -   Los procesadores de hardware tienen un TSC no invariable y el BIOS no indica esta condición correctamente.
    -   El algoritmo de sincronización de TSC que se usó no era adecuado para sistemas con un gran número de procesadores.

-   Al comparar los resultados del contador de rendimiento que se adquieren de subprocesos diferentes, considere la posibilidad de que los valores que difieren ± 1 tic tengan una ordenación ambigua. Si las marcas de tiempo se toman del mismo subproceso, ± la incertidumbre de 1 paso no se aplica. En este contexto, el término tick hace referencia a un período de tiempo igual a 1 ÷ (la frecuencia del contador de rendimiento obtenido de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)).

Cuando se usa el contador de rendimiento en sistemas de servidor de gran tamaño con dominios de varios relojes que no están sincronizados en hardware, Windows determina que el TSC no se puede usar con fines de control de tiempo y selecciona un contador de plataforma como base para [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Aunque este escenario sigue generando marcas de tiempo confiables, la latencia de acceso y la escalabilidad se ven afectadas negativamente. Por lo tanto, como se indicó anteriormente en la guía de uso anterior, use solo las API que proporcionan 1 microsegundo o una mejor resolución cuando sea necesaria dicha resolución. El TSC se usa como base para **QPC** en sistemas de dominio de varios relojes que incluyen la sincronización de hardware de todos los dominios de reloj del procesador, ya que esto hace que funcionen de forma eficaz como un sistema de dominio de reloj único.

La frecuencia del contador de rendimiento se fija en el arranque del sistema y es coherente en todos los procesadores, por lo que solo tiene que consultar la frecuencia desde [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) a medida que se inicializa la aplicación y, a continuación, almacenar en caché el resultado.

### <a name="virtualization"></a>La virtualización

Se espera que el contador de rendimiento funcione de forma confiable en todas las máquinas virtuales invitadas que se ejecutan en hipervisores implementados correctamente. Sin embargo, los hipervisores que cumplen con la interfaz de la versión 1.0 del hipervisor y que superficien la iluminación de tiempo de referencia pueden ofrecer una sobrecarga considerablemente menor. Para obtener más información sobre las interfaces e iluminación del hipervisor, vea [Especificaciones del hipervisor.](/virtualization/hyper-v-on-windows/reference/tlfs)

### <a name="direct-tsc-usage"></a>Uso directo de TSC

Se recomienda encarecidamente usar la instrucción del procesador **RDTSC** o **RDTSCP** para consultar directamente el TSC porque no se obtienen resultados confiables en algunas versiones de Windows, en migraciones en vivo de máquinas virtuales y en sistemas de hardware sin TSC invariables o estrechamente sincronizados. En su lugar, le recomendamos que use [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) para aprovechar la abstracción, la coherencia y la portabilidad que ofrece.

### <a name="examples-for-acquiring-time-stamps"></a>Ejemplos para adquirir marcas de tiempo

Los distintos ejemplos de código de estas secciones muestran cómo adquirir marcas de tiempo.

### <a name="using-qpc-in-native-code"></a>Uso de QPC en código nativo

En este ejemplo se muestra cómo [**usar QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) en código nativo de C y C++.


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



### <a name="acquiring-high-resolution-time-stamps-from-managed-code"></a>Adquisición de marcas de tiempo de alta resolución a partir de código administrado

En este ejemplo se muestra cómo usar la clase [**System.Diagnostics.Stopwatch de código**](/previous-versions/windows/) administrado.


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



La [**clase System.Diagnostics.Stopwatch**](/previous-versions/windows/) también proporciona varios métodos prácticos para realizar medidas de intervalo de tiempo.

### <a name="using-qpc-from-kernel-mode"></a>Uso de QPC desde el modo kernel

El Windows kernel proporciona acceso en modo kernel al contador de rendimiento a través de [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) desde el que se pueden obtener tanto el contador de rendimiento como la frecuencia de rendimiento. **KeQueryPerformanceCounter solo** está disponible desde el modo kernel y se proporciona para escritores de controladores de dispositivo y otros componentes en modo kernel.

En este ejemplo se muestra cómo usar [**KeQueryPerformanceCounter en**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) el modo kernel de C y C++.


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



## <a name="general-faq-about-qpc-and-tsc"></a>Preguntas más frecuentes generales sobre QPC y TSC

Estas son las respuestas a las preguntas más frecuentes [**sobre QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y TSC en general.

<dl> <dt>

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**¿QueryPerformanceCounter() es igual que la función GetTickCount() o GetTickCount64() de Win32?**
</dt> <dd>

No. [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) y [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) no están relacionados con [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) **GetTickCount** y **GetTickCount64** devuelven el número de milisegundos desde que se inició el sistema.

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**¿Debo usar QPC o llamar directamente a las instrucciones de RDTSC /RDTSCP?**
</dt> <dd>

Para evitar problemas de portabilidad e incorrectos, le recomendamos encarecidamente que use [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) en lugar de usar el registro de TSC o las instrucciones del procesador **RDTSC** o **RDTSCP.**

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**¿Cuál es la relación de QPC con una época de tiempo externa? ¿Se puede sincronizar con una época externa como UTC?**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) se basa en un contador de hardware que no se puede sincronizar con una referencia de hora externa, como UTC. Para las marcas de hora exactas de hora del día que se pueden sincronizar con una referencia UTC externa, use [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**¿QPC se ve afectado por el horario de verano, los segundos bisiesos, las zonas horarias o los cambios de hora del sistema realizados por el administrador?**
</dt> <dd>

No. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es completamente independiente de la hora del sistema y utc.

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**¿Se ve afectada la precisión de QPC por los cambios de frecuencia del procesador causados por la administración de energía o la tecnología Turbo Boost?**
</dt> <dd>

No. Si el procesador tiene un TSC invariable, el [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) no se ve afectado por este tipo de cambios. Si el procesador no tiene un TSC invariable, **QPC** revertirá a un temporizador de hardware de plataforma que no se verá afectado por los cambios de frecuencia del procesador o la tecnología Turbo Boost.

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**¿Funciona QPC de forma confiable en sistemas de varios procesadores, sistemas de varios núcleos y sistemas con hyper-threading?**
</dt> <dd>

Sí

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**Cómo determinar y validar que QPC funciona en mi máquina?**
</dt> <dd>

No es necesario realizar tales comprobaciones.

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**¿Qué procesadores tienen TSC no invariables? ¿Cómo puedo comprobar si mi sistema tiene un TSC no invariable?**
</dt> <dd>

No es necesario realizar esta comprobación usted mismo. Windows sistemas operativos realizan varias comprobaciones en la inicialización del sistema para determinar si el TSC es adecuado como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Sin embargo, para fines de referencia, puede determinar si el procesador tiene un TSC invariable mediante uno de estos:

-   la Coreinfo.exe de Windows Sysinternals
-   comprobar los valores devueltos por la instrucción CPUID relativa a las características de TSC
-   documentación del fabricante del procesador

A continuación se muestra la información de TSC-INVARIANT proporcionada por la utilidad Windows sysinternals Coreinfo.exe ([www.sysinternals.com](https://www.sysinternals.com)). Un asterisco significa "True".

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

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**¿QPC funciona de forma confiable en Windows RT plataformas de hardware de pc?**
</dt> <dd>

Sí

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**¿Con qué frecuencia se revierte QPC?**
</dt> <dd>

No menos de 100 años desde el arranque más reciente del sistema y potencialmente más largo en función del temporizador de hardware subyacente utilizado. Para la mayoría de las aplicaciones, la suversión no es un problema.

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**¿Cuál es el costo computacional de llamar a QPC?**
</dt> <dd>

El costo de llamada computacional de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) viene determinado principalmente por la plataforma de hardware subyacente. Si el registro de TSC se usa como base para QPC, el costo computacional se determina principalmente por cuánto tiempo tarda el procesador en procesar una **instrucción RDTSC.** Este tiempo va de 10 a 10 ciclos de CPU a varios cientos de ciclos de CPU en función del procesador utilizado. Si no se puede usar el TSC, el sistema seleccionará una base de tiempo de hardware diferente. Dado que estas bases de tiempo se encuentran en la placa base (por ejemplo, en pci south bridge o PCH), el costo computacional por llamada es mayor que el TSC y suele estar en las proximidades de 0,8 a 1,0 microsegundos según la velocidad del procesador y otros factores de hardware. Este costo está dominado por el tiempo necesario para acceder al dispositivo de hardware en la placa base.

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**¿QPC requiere una transición del kernel (llamada del sistema)?**
</dt> <dd>

No se requiere una transición de kernel si el sistema puede usar el registro de TSC como base para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Si el sistema debe usar una base de tiempo diferente, como el temporizador HPET o PM, se requiere una llamada del sistema.

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**¿El contador de rendimiento es monotónico (no decreciente)?**
</dt> <dd>

Sí

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**¿Se puede usar el contador de rendimiento para ordenar eventos a tiempo?**
</dt> <dd>

Sí. Sin embargo, al comparar los resultados del contador de rendimiento que se adquieren de subprocesos diferentes, los valores que difieren en ± 1 tic tienen una ordenación ambigua como si tuvieran una marca de tiempo idéntica.

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**¿Qué precisión tiene el contador de rendimiento?**
</dt> <dd>

La respuesta depende de diversos factores. Para más información, consulte [Características del reloj de hardware de bajo nivel.](#low-level-hardware-clock-characteristics)

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>Preguntas más frecuentes sobre la programación con QPC y TSC

Estas son las respuestas a las preguntas más frecuentes sobre la programación [**con QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y TSC.

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**Necesito convertir la salida de QPC en milisegundos. ¿Cómo puedo evitar la pérdida de precisión con la conversión a double o float?**
</dt> <dd>

Hay varias cosas que debe tener en cuenta al realizar cálculos en contadores de rendimiento enteros:

-   La división de enteros perderá el resto. Esto puede provocar la pérdida de precisión en algunos casos.
-   La conversión entre enteros de 64 bits y punto flotante (double) puede provocar una pérdida de precisión porque la mantisa de punto flotante no puede representar todos los valores enteros posibles.
-   La multiplicación de enteros de 64 bits puede dar lugar a un desbordamiento de enteros.

Como principio general, retrase estos cálculos y conversiones siempre que sea posible para evitar que se acomenten los errores introducidos.

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**¿Cómo puedo convertir QPC en tics de 100 nanosegundos para poder agregarlo a filetime?**
</dt> <dd>

Un tiempo de archivo es un valor de 64 bits que representa el número de intervalos de 100 nanosegundos transcurridos desde las 12:00 a.m. 1 de enero de 1601 Hora universal coordinada (UTC). Las horas de archivo las usan las llamadas API de Win32 que devuelven la hora del día, como [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) y [**GetSystemTimePreciseAsFileTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) Por el contrario, [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) devuelve valores que representan el tiempo en unidades de 1/(la frecuencia del contador de rendimiento obtenido de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)). La conversión entre los dos requiere calcular la relación entre el intervalo **QPC** y los intervalos de 100 nanosegundos. Tenga cuidado de evitar la pérdida de precisión porque los valores pueden ser pequeños (0,0000001 / 0,000000340).

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**¿Por qué la marca de tiempo que se devuelve de QPC es un entero con signo?**
</dt> <dd>

Los cálculos que [**implican marcas de tiempo de QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) pueden implicar la resta. Mediante el uso de un valor con signo, puede controlar los cálculos que podrían producir valores negativos.

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**¿Cómo puedo obtener marcas de tiempo de alta resolución a partir de código administrado?**
</dt> <dd>

Llame al [**método Stopwatch.GetTimeStamp**](/previous-versions/windows/) desde la [**clase System.Diagnostics.Stopwatch.**](/previous-versions/windows/) Para obtener un ejemplo sobre cómo usar **Stopwatch.GetTimeStamp**, vea Adquisición de marcas de tiempo de alta resolución [a partir de código administrado.](#acquiring-high-resolution-time-stamps-from-managed-code)

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**¿En qué circunstancias QueryPerformanceFrequency devuelve FALSE o QueryPerformanceCounter devuelve cero?**
</dt> <dd>

Esto no se producirá en ningún sistema que se ejecute Windows XP o posterior.

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**¿Es necesario establecer la afinidad del subproceso en un único núcleo para usar QPC?**
</dt> <dd>

No. Para obtener más información, vea [Guía para adquirir marcas de tiempo.](#guidance-for-acquiring-time-stamps) Este escenario no es necesario ni deseable. Este escenario podría afectar negativamente al rendimiento de la aplicación al restringir el procesamiento a un núcleo o crear un cuello de botella en un único núcleo si varios subprocesos establecen su afinidad en el mismo núcleo al llamar a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>Características de reloj de hardware de bajo nivel

En estas secciones se muestran las características de reloj de hardware de bajo nivel.

### <a name="absolute-clocks-and-difference-clocks"></a>Relojes absolutos y relojes de diferencia

Los relojes absolutos proporcionan lecturas precisas de la hora del día. Normalmente se basan en la hora universal coordinada (UTC) y, por lo tanto, su precisión depende en parte de cómo se sincronicen con una referencia de hora externa. Los relojes de diferencia miden los intervalos de tiempo y no suelen basarse en una época de tiempo externa. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es un reloj de diferencia y no se sincroniza con una época o referencia de hora externa. Cuando se usa **QPC** para las medidas de intervalo de tiempo, normalmente se obtiene una mayor precisión de la que se obtiene mediante marcas de tiempo que se derivan de un reloj absoluto. Esto se debe a que el proceso de sincronización de la hora de un reloj absoluto puede introducir cambios de fase y frecuencia que aumentan la incertidumbre de las medidas de intervalo de tiempo a corto plazo.

### <a name="resolution-precision-accuracy-and-stability"></a>Resolución, precisión, precisión y estabilidad

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) usa un contador de hardware como base. Los temporizadores de hardware constan de tres partes: un generador de tics, un contador que cuenta los tics y un medio para recuperar el valor del contador. Las características de estos tres componentes determinan la resolución, precisión, precisión y estabilidad de **QPC.**

Si un generador de hardware proporciona tics a una velocidad constante, los intervalos de tiempo se pueden medir simplemente contando estos pasos. La velocidad a la que se generan los tics se denomina frecuencia y se expresa en Hertz (Hz). El recíproco de la frecuencia se denomina intervalo de período o tic y se expresa en una unidad de tiempo del Sistema internacional de unidades (SI) adecuada (por ejemplo, segundo, milisegundo, microsegundo o nanosegundo).

![intervalo de tiempo](images/tick-interval.png)

La resolución del temporizador es igual al punto. La resolución determina la capacidad de distinguir entre dos marcas de tiempo cualquiera y coloca un límite inferior en los intervalos de tiempo más pequeños que se pueden medir. Esto a veces se denomina resolución de tics.

La medición digital del tiempo presenta una incertidumbre de medidas de ± 1 tic porque el contador digital avanza en pasos discretos, mientras que el tiempo avanza continuamente. Esta incertidumbre se denomina error de cuantificación. En el caso de las medidas típicas de intervalo de tiempo, este efecto se puede omitir a menudo porque el error de cuantificación es mucho menor que el intervalo de tiempo que se mide.

![medición de tiempo digital](images/digital-time-measure.png)

Sin embargo, si el período que se mide es pequeño y se aproxima a la resolución del temporizador, deberá tener en cuenta este error de cuantificación. El tamaño del error introducido es el de un período de reloj.

Los dos diagramas siguientes ilustran el impacto de la ± 1 tic de incertidumbre mediante el uso de un temporizador con una resolución de 1 unidad de tiempo.

![incertidumbre de tics](images/tick-uncertainty.png)

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) devuelve la frecuencia de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)y el período y la resolución son iguales al recíproco de este valor. La frecuencia del contador de rendimiento **que devuelve QueryPerformanceFrequency** se determina durante la inicialización del sistema y no cambia mientras se ejecuta el sistema.

> [!Note]  
> Pueden existir casos [**en los que QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) no devuelve la frecuencia real del generador de tics de hardware. Por ejemplo, en muchos casos, **QueryPerformanceFrequency** devuelve la frecuencia de TSC dividida entre 1024; y en Hyper-V, la frecuencia del contador de rendimiento siempre es de 10 MHz cuando la máquina virtual invitada se ejecuta bajo un [hipervisor](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) que implementa la interfaz de la versión [1.0 del hipervisor.](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx) Como resultado, no suponga que **QueryPerformanceFrequency** devolverá la frecuencia de TSC precisa.

 

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) lee el contador de rendimiento y devuelve el número total de tics que se han producido desde que se inició el sistema operativo Windows, incluida la hora en que la máquina estaba en estado de suspensión, como espera, hibernación o espera conectada.

En estos ejemplos se muestra cómo calcular el intervalo y la resolución de tics y cómo convertir el recuento de tics en un valor de tiempo.

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Ejemplo 1**
</dt> <dd>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) devuelve el valor 3 125 000 en un equipo determinado. ¿Cuál es el intervalo de tics y la resolución [**de las medidas de QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) en esta máquina? El intervalo de tics, o punto, es el recíproco de 3 125 000, que es 0,000000320 (320 nanosegundos). Por lo tanto, cada paso representa el paso de 320 nanosegundos. Los intervalos de tiempo menores de 320 nanosegundos no se pueden medir en esta máquina.

Intervalo de tic = 1/(Frecuencia de rendimiento)

Intervalo de tic = 1/3 125 000 = 320 ns

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Ejemplo 2**
</dt> <dd>

En la misma máquina que en el ejemplo anterior, la diferencia de los valores devueltos por dos llamadas sucesivas a [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es 5. ¿Cuánto tiempo ha transcurrido entre las dos llamadas? 5 tics multiplicados por 320 nanosegundos produce 1,6 microsegundos.

ElapsedTime = Intervalo de \* tics

ElapsedTime = 5 \* 320 ns = 1,6 μs

</dd> </dl>

Se tarda tiempo en acceder (leer) al contador de tics desde el software y este tiempo de acceso puede reducir la precisión de la medida de tiempo. Esto se debe a que el tiempo de intervalo mínimo (el intervalo de tiempo más pequeño que se puede medir) es el mayor de la resolución y el tiempo de acceso.

Precision = MAX \[ Resolution, AccessTime\]

Por ejemplo, considere un temporizador de hardware hipotético con una resolución de 100 nanosegundos y un tiempo de acceso de 800 nanosegundos. Este podría ser el caso si se usara el temporizador de la plataforma en lugar del registro de TSC como base de [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Por lo tanto, la precisión sería de 800 nanosegundos, no de 100 nanosegundos, como se muestra en este cálculo.

Precisión = MAX \[ 800 ns,100 ns \] = 800 ns

Estas dos cifras representan este efecto.

![Hora de acceso de qpc](images/qpc-access-time.png)

Si el tiempo de acceso es mayor que la resolución, no intente mejorar la precisión adivinando. En otras palabras, es un error suponer que la marca de tiempo se toma exactamente en el centro, al principio o al final de la llamada.

Por el contrario, considere el siguiente ejemplo en el que el tiempo de acceso de [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) es de solo 20 nanosegundos y la resolución del reloj de hardware es de 100 nanosegundos. Este podría ser el caso si se usó el registro de TSC como base para **QPC.** Aquí la precisión está limitada por la resolución del reloj.

![Precisión de qpc](images/qpc-precision.png)

En la práctica, puede encontrar orígenes de tiempo para los que el tiempo necesario para leer el contador es mayor o menor que la resolución. En cualquier caso, la precisión será la mayor de las dos.

En esta tabla se proporciona información sobre la resolución aproximada, el tiempo de acceso y la precisión de una variedad de relojes. Tenga en cuenta que algunos de los valores variarán con diferentes procesadores, plataformas de hardware y velocidades de procesador.



| Origen del reloj                                                      | Frecuencia nominal del reloj | Resolución del reloj    | Tiempo de acceso (típico) | Precisión       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| PC RTC                                                            | 64 Hz                   | 15,625 milisegundos | N/D                   | N/D             |
| Contador de rendimiento de consultas mediante TSC con un reloj de procesador de 3 GHz  | 3 MHz                   | 333 nanosegundos     | 30 nanosegundos        | 333 nanosegundos |
| **Instrucciones de máquina RDTSC** en un sistema con un tiempo de ciclo de 3 GHz | 3 GHz                   | 333 picosegundos     | 30 nanosegundos        | 30 nanosegundos  |



 

Dado [**que QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) usa un contador de hardware, cuando comprenda algunas características básicas de los contadores de hardware, comprenderá las funcionalidades y limitaciones de **QPC.**

El generador de tics de hardware más usado es un oscilador de cristal. El cristal es un pequeño fragmento de cristal u otro material de ántico que presenta características piezométricas que proporcionan una referencia de frecuencia económica con una estabilidad y precisión excelentes. Esta frecuencia se usa para generar los tics que cuenta el reloj.

La precisión de un temporizador hace referencia al grado de conformidad con un valor true o estándar. Esto depende principalmente de la capacidad del cristal para proporcionar tics con la frecuencia especificada. Si la frecuencia de oscilación es demasiado alta, el reloj se "ejecutará rápidamente" y los intervalos medidos aparecerán más tiempo de lo que realmente son; y si la frecuencia es demasiado baja, el reloj "se ejecutará lentamente" y los intervalos medidos serán más cortos de lo que realmente son.

Para las medidas típicas de intervalo de tiempo para una duración corta (por ejemplo, medidas de tiempo de respuesta, medidas de latencia de red, entre otras), la precisión del oscilador de hardware suele ser suficiente. Sin embargo, para algunas medidas, la precisión de la frecuencia de oscilación es importante, especialmente para intervalos de tiempo largos o cuando se quieren comparar las medidas realizadas en diferentes máquinas. En el resto de esta sección se exploran los efectos de la precisión del oscilador.

La frecuencia de oscilación de los cristales se establece durante el proceso de fabricación y lo especifica el fabricante en términos de una frecuencia especificada más o menos una tolerancia de fabricación expresada en "partes por millón" (ppm), denominada desplazamiento de frecuencia máxima. Un cristal con una frecuencia especificada de 1000 000 Hz y un desplazamiento de frecuencia máximo de ± 10 ppm estaría dentro de los límites de especificación si su frecuencia real estuviera entre 999 990 990 Hz y 1 000 010 Hz.

Al sustituir las partes de frase por millón por microsegundos por segundo, podemos aplicar este error de desplazamiento de frecuencia a las medidas de intervalo de tiempo. Un oscilador con un desplazamiento + 10 ppm tendría un error de 10 microsegundos por segundo. En consecuencia, al medir un intervalo de 1 segundo, se ejecutaría rápidamente y mediría un intervalo de 1 segundo como 0,999990 segundos.

Una referencia práctica es que un error de frecuencia de 100 ppm provoca un error de 8,64 segundos después de 24 horas. En esta tabla se presenta la incertidumbre de las medidas debido al error acumulado para intervalos de tiempo más largos.



| Duración del intervalo de tiempo | Incertidumbre de las medidas debido a un error acumulado con +/- 10 PPM de frecuencia |
|------------------------|--------------------------------------------------------------------------------------|
| 1 microsegundo          | ± 10 picosegundos (10-12)                                                             |
| 1 milisegundo          | ± 10 nanosegundos (10-9)                                                              |
| 1 segundo               | ± 10 microsegundos                                                                    |
| 1 hora                 | ± 60 microsegundos                                                                    |
| 1 día                  | ± 0,86 segundos                                                                       |
| 1 semana                 | ± 6,08 segundos                                                                       |



 

En la tabla anterior se muestra que, para intervalos de tiempo pequeños, el error de desplazamiento de frecuencia a menudo se puede omitir. Sin embargo, para intervalos de tiempo largos, incluso un desplazamiento de frecuencia pequeño puede dar lugar a una incertidumbre de medida considerable.

Los cristales que se usan en equipos y servidores personales se suelen fabricación con una tolerancia de frecuencia de ± de 30 a 50 partes por millón y, en raras ocasiones, los cristales pueden estar apagados hasta 500 ppm. Aunque hay disponibles cristales con tolerancias de desplazamiento de frecuencia mucho más estrictas, son más caros y, por tanto, no se usan en la mayoría de los equipos.

Para reducir los efectos negativos de este error de desplazamiento de frecuencia, las versiones recientes de Windows, especialmente Windows 8, usan varios temporizadores de hardware para detectar el desplazamiento de frecuencia y compensarlo en la medida de lo posible. Este proceso de calibración se realiza Windows se inicia.

Como se muestra en los ejemplos siguientes, el error de desplazamiento de frecuencia de un reloj de hardware influye en la precisión factible y la resolución del reloj puede ser menos importante.

![El error de desplazamiento de frecuencia influye en la precisión factible](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Ejemplo 1**
</dt> <dd>

Supongamos que realiza medidas de intervalo de tiempo mediante un oscilador de 1 MHz, que tiene una resolución de 1 microsegundo y un error de desplazamiento de frecuencia máximo de ±50 ppm. Ahora, supongamos que el desplazamiento es exactamente +50 ppm. Esto significa que la frecuencia real sería de 1 000 050 Hz. Si medimos un intervalo de tiempo de 24 horas, nuestra medida sería 4,3 segundos demasiado corta (23:59:55.700000 medida frente a 24:00:00.000000 real).

Segundos en un día = 86400

Error de desplazamiento de frecuencia = 50 ppm = 0,00005

86 400 segundos \* 0,00005 = 4,3 segundos

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Ejemplo 2**
</dt> <dd>

Supongamos que el reloj TSC del procesador está controlado por un oscilador de cristal y tiene una frecuencia especificada de 3 GHz. Esto significa que la resolución sería de 1/3 000 000 000 o aproximadamente 333 picosegundos. Supongamos que el cristal usado para controlar el reloj del procesador tiene una tolerancia de frecuencia de ±50 ppm y, en realidad, es +50 ppm. A pesar de la resolución impresionante, una medida de intervalo de tiempo de 24 horas seguirá siendo 4,3 segundos demasiado corta. (23:59:55.70000000000 medido frente a 24:00:00.00000000000 real).

Segundos en un día = 86400

Error de desplazamiento de frecuencia = 50 ppm = 0,00005

86 400 segundos \* 0,00005 = 4,3 segundos

Esto muestra que un reloj TSC de alta resolución no proporciona necesariamente medidas más precisas que un reloj de resolución inferior.

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Ejemplo 3**
</dt> <dd>

Considere la posibilidad de usar dos equipos diferentes para medir el mismo intervalo de tiempo de 24 horas. Ambos equipos tienen un oscilador con un desplazamiento de frecuencia máximo de ± 50 ppm. ¿A qué distancia puede estar la medida del mismo intervalo de tiempo en estos dos sistemas? Como en los ejemplos anteriores, ± 50 ppm produce un error máximo de ± 4,3 segundos después de 24 horas. Si un sistema se ejecuta 4,3 segundos rápidamente y los otros 4,3 segundos son lentos, el error máximo después de 24 horas podría ser 8,6 segundos.

Segundos en un día = 86400

Error de desplazamiento de frecuencia = ±50 ppm = ±0,00005

±(86 400 segundos \* 0,00005) = ±4,3 segundos

Desplazamiento máximo entre los dos sistemas = 8,6 segundos

En resumen, el error de desplazamiento de frecuencia es cada vez más importante al medir intervalos de tiempo largos y al comparar medidas entre distintos sistemas.

La estabilidad de un temporizador describe si la frecuencia del paso cambia con el tiempo, por ejemplo, como resultado de los cambios de temperatura. Los cristales de cristal que se usan como generadores de tics en los equipos mostrarán pequeños cambios en la frecuencia como función de la temperatura. El error causado por el desfase térmico suele ser pequeño en comparación con el error de desplazamiento de frecuencia para los intervalos de temperatura comunes. Sin embargo, es posible que los diseñadores de software para equipos portátiles o sujetos a grandes fluctuaciones de temperatura deba tener en cuenta este efecto.

</dd> </dl>

## <a name="hardware-timer-info"></a>Información del temporizador de hardware

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**Registro de TSC**
</dt> <dd>

Algunos procesadores Intel y AMD contienen un registro TSC que es un registro de 64 bits que aumenta a una velocidad alta, normalmente igual al reloj del procesador. El valor de este contador se puede leer a través de las instrucciones de la máquina **RDTSC** o **RDTSCP,** lo que proporciona un tiempo de acceso muy bajo y un costo computacional en el orden de decenas o cientos de ciclos de máquina, en función del procesador.

Aunque el registro de TSC parece un mecanismo ideal de marca de tiempo, estas son las circunstancias en las que no puede funcionar de forma confiable con fines de mantenimiento del tiempo:

-   No todos los procesadores tienen registros de TSC, por lo que el uso del registro de TSC en software crea directamente un problema de portabilidad. (Windows seleccionará un origen de hora alternativo para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) en este caso, lo que evita el problema de portabilidad).
-   Algunos procesadores pueden variar la frecuencia del reloj de TSC o detener el avance del registro de TSC, lo que hace que el TSC no sea adecuado para fines de tiempo en estos procesadores. Se dice que estos procesadores tienen registros TSC no invariables. (Windows detectará automáticamente y seleccionará un origen de hora alternativo para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   En sistemas de varios procesadores o de varios núcleos, algunos procesadores y sistemas no pueden sincronizar los relojes de cada núcleo con el mismo valor. (Windows detectará automáticamente y seleccionará un origen de hora alternativo para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   En algunos sistemas de varios procesadores grandes, es posible que no pueda sincronizar los relojes del procesador con el mismo valor aunque el procesador tenga un TSC invariable. (Windows detectará automáticamente y seleccionará un origen de hora alternativo para [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Algunos procesadores ejecutarán instrucciones fuera de orden. Esto puede dar lugar a recuentos de ciclos incorrectos cuando se usa **RDTSC** para programar secuencias de instrucciones porque la instrucción **RDTSC** se puede ejecutar en un momento diferente al especificado en el programa. La **instrucción RDTSCP** se ha introducido en algunos procesadores en respuesta a este problema.

Al igual que otros temporizadores, el TSC se basa en un oscilador de cristal cuya frecuencia exacta no se conoce de antemano y que tiene un error de desplazamiento de frecuencia. Por lo tanto, antes de poder usarse, se debe calibrar con otra referencia de tiempo.

Durante la inicialización del sistema, Windows comprueba si el TSC es adecuado para fines de tiempo y realiza la calibración de frecuencia necesaria y la sincronización de núcleos.

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**Reloj de pm**
</dt> <dd>

El temporizador ACPI, también conocido como reloj de pm, se agregó a la arquitectura del sistema para proporcionar marcas de tiempo confiables independientemente de la velocidad de los procesadores. Dado que este era el objetivo único de este temporizador, proporciona una marca de tiempo en un único ciclo de reloj, pero no proporciona ninguna otra funcionalidad.

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**Temporizador HPET**
</dt> <dd>

Intel y Microsoft desarrollaron conjuntamente el temporizador de eventos de alta precisión (HPET) para cumplir los requisitos de control de tiempo de las aplicaciones multimedia y otras aplicaciones sensibles al tiempo. La compatibilidad con HPET ha estado en Windows desde Windows Vista y la certificación del logotipo de hardware de Windows 7 y Windows 8 requiere compatibilidad con HPET en la plataforma de hardware.

</dd> </dl>

 

 

---
description: Los contadores se usan para proporcionar información sobre el rendimiento del sistema operativo o una aplicación, servicio o controlador.
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: Acerca de los contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dec7c71e99ab614ee64e3d1e8c9620f0be78c14a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169166"
---
# <a name="about-performance-counters"></a>Acerca de los contadores de rendimiento

Windows Los contadores de rendimiento proporcionan una capa de abstracción de alto nivel con una interfaz coherente para recopilar varios tipos de datos del sistema, como estadísticas de uso de CPU, memoria y disco. Los administradores del sistema usan contadores de rendimiento para supervisar los problemas de rendimiento o comportamiento. Los desarrolladores de software usan contadores de rendimiento para inspeccionar el uso de recursos de sus componentes.

> [!IMPORTANT]
> Windows Los contadores de rendimiento están optimizados para la recopilación y detección de datos administrativos y de diagnóstico. No son adecuados para la recopilación de datos de alta frecuencia o para la generación de perfiles de aplicaciones, ya que no están diseñados para recopilarse más de una vez por segundo. Para obtener acceso de menor sobrecarga a la información del sistema, es posible que prefiera API más directas, como asistente de estado de [**proceso,**](../psapi/process-status-helper.md) [**GlobalMemoryStatusEx,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)o [**GetProcessTimes.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes) Para la generación de perfiles, puede recopilar registros ETW con datos de generación de perfiles del sistema mediante [**tracelog.exe**](/windows-hardware/drivers/devtest/tracelog) con las opciones , , o , o bien puede usar la generación de perfiles de `-critsec` `-dpcisr` `-eflag` `-ProfileSource` [**contadores de hardware**](/previous-versions/windows/desktop/hcp/hcp-reference).

> [!NOTE]
> No confunda Windows contadores de rendimiento con la API [**QueryPerformanceCounter.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Windows Los contadores de rendimiento proporcionan una abstracción de alto nivel para muchos tipos de información del sistema. La función QueryPerformanceCounter proporciona acceso optimizado a una marca de tiempo de alta precisión.

## <a name="getting-started"></a>Introducción

- Use [las herramientas de contador de](performance-counters-tools.md) rendimiento cuando desee recopilar o ver los datos de rendimiento de un sistema.
- Use [las API de recopilación de contadores](consuming-counter-data.md) de rendimiento cuando desee escribir un script o un programa que recopile datos de rendimiento del sistema local.
- Use [clases de contadores de](/windows/desktop/WmiSdk/monitoring-performance-data) rendimiento WMI cuando desee recopilar datos de rendimiento de un sistema local o remoto mediante WMI.
- Use [las API del proveedor de contadores de](providing-counter-data.md) rendimiento cuando desee publicar datos de rendimiento desde el componente de software.

## <a name="concepts"></a>Conceptos

El Windows contador de rendimiento se organiza en **consumidores,** **proveedores,** conjuntos de contadores, contadores,  **instancias** y valores de **contador**.

Un **consumidor** es un componente de software que usa datos de rendimiento. Windows incluye varias [herramientas integradas que](performance-counters-tools.md) hacen uso de los datos de rendimiento. Estos incluyen Administrador de tareas, Monitor de recursos, Monitor de rendimiento, typeperf.exe, logman.exe y relog.exe. Los desarrolladores pueden escribir scripts y aplicaciones que acceden a los contadores de rendimiento a través de [las API de contador de rendimiento](consuming-counter-data.md).

Un **proveedor** es un componente de software que [genera y publica datos de rendimiento.](providing-counter-data.md) Un proveedor publicará los datos de uno o varios *conjuntos de contadores.* Por ejemplo, un sistema de base de datos podría registrarse como proveedor de datos de rendimiento.

- Un **proveedor V1 es** un componente de software que publica datos de rendimiento a través de un archivo [DLL](providing-counter-data-using-a-performance-dll.md) de rendimiento que se ejecuta en el proceso del consumidor. Un proveedor V1 se instala en un sistema a través de un `.ini` archivo . La arquitectura del proveedor V1 está en desuso. Los nuevos proveedores deben usar la arquitectura del proveedor V2.
- Un **proveedor V2 es** un componente de software que publica datos de rendimiento a través de las API del proveedor de [contadores de rendimiento](providing-counter-data-using-version-2-0.md). Un proveedor V2 se instala en un sistema a través de un `.man` archivo (manifiesto XML).

Un **contraconjunto** es una agrupación de datos de rendimiento dentro de un proveedor. Un conjunto de contadores tiene un nombre y uno o varios *contadores*. La recopilación de los datos de un contraconjunto devuelve un número de *instancias de*. En algunas API Windows, los conjuntos de contadores se denominan **objetos de rendimiento**. Por ejemplo, un proveedor de datos de rendimiento para un sistema de base de datos podría proporcionar un contraconjunto para las estadísticas por base de datos.

Un **contador** es la definición de un único fragmento de datos de rendimiento. Un contador tiene un nombre y un tipo. Por ejemplo, un conjunto de contadores "estadísticas por base de datos" podría contener un contador denominado "transacciones por segundo" con el tipo `PERF_COUNTER_COUNTER` .

Una **instancia de** es una entidad sobre la que se notifican los datos de rendimiento. Una instancia tiene un nombre (cadena) y uno o varios valores *de contador*. Por ejemplo, un conjunto de contadores "estadísticas por base de datos" podría contener una instancia por base de datos. El nombre de instancia sería el nombre de la base de datos y cada instancia contendrá valores de contador para los contadores "transacciones por segundo", "uso de memoria" y "uso de disco".

Un **valor de contador** es el valor de un único fragmento de datos del contador de rendimiento. Un valor de contador es un entero sin signo, de 32 o 64 bits, según el tipo del contador correspondiente. Al hablar de una *instancia de*, un valor *de contador* a veces se puede *denominar contador* o *valor*.

> [!TIP]
> Puede resultar útil relacionar los términos del contador de rendimiento con términos de hoja de cálculo más conocidos. Un **conjunto de contadores** es como una tabla. Un **contador** es como una columna. Una **instancia** es como una fila. Un **valor de contador** es como una celda de la tabla.

**Los conjuntos de contadores de instancia** única siempre contienen datos para exactamente una instancia. Esto es común para los contraconjuntos que informan de estadísticas globales del sistema. Por ejemplo, Windows un conjunto de contadores de instancia única integrado denominado "Memoria" que informa sobre el uso de memoria global.

**Los conjuntos de contadores de varias instancias** contienen datos para un número variable de instancias. Esto es común para los contraconjuntos que informan sobre las entidades dentro del sistema. Por ejemplo, Windows un conjunto de contadores de varias instancias integrado denominado "Información del procesador" que notifica una instancia para cada CPU instalada.

Los consumidores recopilarán y registrarán periódicamente los datos del contraconjunto de un proveedor. Por ejemplo, el consumidor podría recopilar datos una vez por segundo o una vez por minuto. Los datos recopilados se denominan **ejemplo**. Un ejemplo consta de marcas de tiempo junto con los datos de las instancias del conjunto de contadores. Los datos de cada instancia incluyen el nombre de instancia (cadena) y un conjunto de valores de contador (enteros, un valor para cada contador del conjunto de contadores).

Normalmente, los nombres de instancia deben ser únicos dentro de un ejemplo, es decir, un proveedor no debe devolver dos instancias con el mismo nombre como parte de una sola muestra. Algunos proveedores anteriores no siguen esta regla, por lo que los consumidores deben poder tolerar nombres [de instancia no únicos.](handling-duplicate-instance-names.md) Los nombres de instancia no distinguen mayúsculas de minúsculas, por lo que las instancias no deben tener nombres que solo difieren en mayúsculas y minúsculas.

> [!NOTE]
> Por motivos de compatibilidad con versiones anteriores, el contraconjunto "Proceso" devuelve nombres de instancia no únicos basados en el nombre de archivo EXE. Esto puede provocar resultados confusos, especialmente cuando se inicia o se cierra un proceso con un nombre no único, ya que normalmente se producirán problemas de datos debido a una coincidencia incorrecta de nombres de instancia entre muestras. Los consumidores del contraconjunto "Proceso" deben poder tolerar estos nombres de instancia no únicos y los problemas de datos resultantes.

Los nombres de instancia deben ser estables en todos los ejemplos, es decir, un proveedor debe usar el mismo nombre de instancia para la misma entidad cada vez que se recopila el contraconjunto.

Cada contador tiene un tipo. El tipo de contador indica el tipo del valor sin formato del contador **(entero** de 32 bits sin signo o entero de 64 bits sin signo). El tipo de contador también indica lo que representa el valor sin procesar del contador, que determina cómo se debe procesar el valor sin formato para generar estadísticas útiles.

Aunque algunos tipos de contador son simples y tienen un [](calculating-counter-values.md) valor sin formato que es directamente útil, muchos tipos de contador requieren procesamiento adicional para crear un valor **con formato útil.** Para generar el valor con formato, algunos tipos de contador requieren valores sin procesar de dos ejemplos, algunos tipos de contador requieren marcas de tiempo y algunos tipos de contador requieren valores sin procesar de varios contadores. Por ejemplo:

- `PERF_COUNTER_LARGE_RAWCOUNT` es un valor sin procesar de 64 bits que no requiere ningún procesamiento para ser útil. Es adecuado para valores a un momento dado, como "Bytes de memoria en uso".
- `PERF_COUNTER_RAWCOUNT_HEX` es un valor sin formato de 32 bits que solo requiere que el formato hexadecimal simple sea útil. Es adecuado para información a un momento dado o para identificar información como "Marcas" o "Dirección base".
- `PERF_COUNTER_BULK_COUNT` es un valor sin procesar de 64 bits que indica un recuento de eventos y se usa para calcular la velocidad a la que se producen los eventos. Para ser útil, este tipo de contador requiere dos muestras separadas en el tiempo. El valor con formato es la tasa de eventos, es decir, el número de veces que se produjo el evento por segundo durante el intervalo entre las dos muestras. Dados dos ejemplos y , el valor con formato (tasa de `s0` `s1` eventos) se calcularía como `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` .

Se espera que los proveedores se comporten como si no hubieran estado, es decir, la recopilación de datos de un contraconjunto no debería afectar visiblemente al estado del proveedor. Por ejemplo, un proveedor no debe restablecer los valores de contador a 0 cuando se recopila un conjunto de contadores y no debe usar la marca de tiempo de una colección anterior para ajustar los valores de la colección actual. En su lugar, debe proporcionar valores de contador sin procesar simples con tipos precisos para que el consumidor pueda calcular estadísticas útiles en función de los valores sin procesar y sus marcas de tiempo.

## <a name="performance-api-architecture"></a>Arquitectura de LA API de rendimiento

![Las aplicaciones de contador de rendimiento invocan Windows API que llaman a proveedores para obtener datos de rendimiento.](images/architecture.png)

Los consumidores de contadores de rendimiento incluyen:

- [Aplicaciones proporcionadas por Microsoft,](performance-counters-tools.md) como Administrador de tareas, Monitor de recursos, Monitor de rendimiento y typeperf.exe.
- Superficies de API de alto nivel proporcionadas por Microsoft que exponen datos de contadores de rendimiento, como [clases de rendimiento WMI.](/windows/desktop/WmiSdk/monitoring-performance-data)
- Sus propias aplicaciones o scripts que usan las [API de consumidor de contadores de rendimiento](consuming-counter-data.md).

La mayoría de los consumidores de contadores de rendimiento usan [ las APIPDH.dll](using-the-pdh-functions-to-consume-counter-data.md) para recopilar datos de rendimiento. PDH administra muchos aspectos complejos de la recopilación de contadores de rendimiento, como el análisis de consultas, la coincidencia de instancias en varias muestras y la computación de valores con formato a partir de los datos de contador sin procesar. La implementación de PDH usa las API del Registro al consumir datos de un proveedor V1 y usa las API de consumidor V2 al consumir datos de un proveedor V2.

Algunos consumidores de contadores de rendimiento anteriores usan las [API del Registro](using-the-registry-functions-to-consume-counter-data.md) para recopilar datos de rendimiento de la clave del Registro `HKEY_PERFORMANCE_DATA` especial. Esto no se recomienda para el código nuevo porque el procesamiento de los datos del registro es complejo y propenso a errores. La implementación de la API del registro admite directamente la recopilación de datos de proveedores V1. Indirectamente, admite la recopilación de datos de proveedores de V2 a través de una capa de traducción que usa las API de consumidor V2.

Algunos consumidores del contador de rendimiento usan las [funciones perfLib V2 Consumer](using-the-perflib-functions-to-consume-counter-data.md) para acceder directamente a los datos de los proveedores de V2. Esto es más complejo que consumir datos mediante las API de PDH, pero este enfoque puede ser útil si las API de PDH no se pueden usar debido a problemas de rendimiento o dependencia. La implementación de PerfLib V2 admite directamente la recopilación de datos de proveedores V2. No admite la recopilación de datos de proveedores V1.

> [!NOTE]
> Windows OneCore no incluye PDH.dll y no incluye compatibilidad para consumir datos de contadores de rendimiento a través de las API del Registro. Los consumidores que se OneCore deben usar las funciones PerfLib V2 Consumer.

Los proveedores V1 se implementan como un archivo DLL de proveedor que se carga en el proceso de consumidor. La implementación de la API del Registro administra la carga del archivo DLL del proveedor, la llamada al archivo DLL para recopilar datos de rendimiento y la descarga del archivo DLL según corresponda. El archivo DLL del proveedor es responsable de recopilar datos de rendimiento según [corresponda,](communicating-with-your-application.md)por ejemplo, mediante API de Windows normales, RPC, canalizaciones con nombre, memoria compartida u otros mecanismos de comunicación entre procesos.

Los proveedores V2 se implementan como un programa en modo de usuario (a menudo un servicio Windows) o un controlador en modo kernel. Normalmente, el código del proveedor de datos de rendimiento se integra directamente en un componente existente (es decir, el controlador o el servicio informa de estadísticas sobre sí mismo). La implementación de PerfLib V2 administra solicitudes y respuestas a través de la extensión de kernel de PCW.sys, por lo que el proveedor normalmente no necesita implementar ninguna comunicación entre procesos para proporcionar los datos de rendimiento.

> [!NOTE]
> Windows Las API y herramientas de contador de rendimiento incluyen compatibilidad limitada para acceder a contadores de rendimiento desde otras máquinas a través del Registro remoto (para proveedores V1) y RPC (para proveedores V2). Esta compatibilidad suele ser difícil de usar en términos de controles de autenticación (las herramientas y las API solo se pueden autenticar como el usuario actual), así como en términos de configuración del sistema [(los](accessing-remote-counter-data.md) puntos de conexión y servicios necesarios están deshabilitados de forma predeterminada). En muchos casos, es mejor acceder a los contadores de rendimiento de los sistemas remotos a través de [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) en lugar de a través de la compatibilidad integrada con el acceso remoto.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Los contadores de rendimiento suelen ser usados por los administradores para identificar problemas de rendimiento o comportamiento anómalo de los sistemas, por parte de los desarrolladores para estudiar el uso de recursos de los componentes de software y por usuarios individuales para comprender cómo se comportan los programas en su sistema. El uso puede producirse a través de herramientas de GUI como Administrador de tareas o Monitor de rendimiento, herramientas de línea de comandos como typeperf.exe o logman.exe, a través de scripting a través de WMI y PowerShell, o a través de C/C++ y API de .NET.

Los proveedores de contadores de rendimiento normalmente se implementan como controladores en modo kernel o servicios en modo de usuario. Los proveedores de contadores de rendimiento normalmente se escriben en C o C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la página de referencia de ese elemento.

Para ver el historial de versiones, [consulte Novedades.](performance-counters-what-s-new.md)

## <a name="see-also"></a>Vea también

[Uso de contadores de rendimiento](using-performance-counters.md)

[Referencia de contadores de rendimiento](performance-counters-reference.md)

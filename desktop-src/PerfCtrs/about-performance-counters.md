---
description: Los contadores se utilizan para proporcionar información sobre el rendimiento del sistema operativo o de una aplicación, servicio o controlador.
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: Acerca de los contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dec7c71e99ab614ee64e3d1e8c9620f0be78c14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909754"
---
# <a name="about-performance-counters"></a>Acerca de los contadores de rendimiento

Los contadores de rendimiento de Windows proporcionan una capa de abstracción de alto nivel con una interfaz coherente para recopilar diversos tipos de datos del sistema, como la CPU, la memoria y las estadísticas de uso del disco. Los administradores del sistema usan contadores de rendimiento para supervisar los problemas de rendimiento o de comportamiento. Los desarrolladores de software usan contadores de rendimiento para inspeccionar el uso de los recursos de sus componentes.

> [!IMPORTANT]
> Los contadores de rendimiento de Windows están optimizados para la recopilación y detección de datos administrativos y de diagnóstico. No son adecuados para la recopilación de datos de alta frecuencia ni para la generación de perfiles de aplicaciones, ya que no están diseñadas para recopilarse más de una vez por segundo. Para el acceso de menor sobrecarga a la información del sistema, es posible que prefiera más API directas como la [**aplicación auxiliar de estado de proceso**](../psapi/process-status-helper.md), [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex), [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)o [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes). Para la generación de perfiles, puede recopilar registros de ETW con datos de generación de perfiles del sistema mediante [**tracelog.exe**](/windows-hardware/drivers/devtest/tracelog) con `-critsec` `-dpcisr` `-eflag` las opciones,, o `-ProfileSource` , o puede usar la [**generación de perfiles de contadores de hardware**](/previous-versions/windows/desktop/hcp/hcp-reference).

> [!NOTE]
> No confunda los contadores de rendimiento de Windows con la API de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) . Los contadores de rendimiento de Windows proporcionan una abstracción de alto nivel para muchos tipos de información del sistema. La función QueryPerformanceCounter proporciona acceso optimizado a una marca de tiempo de alta precisión.

## <a name="getting-started"></a>Introducción

- Use [las herramientas del contador de rendimiento](performance-counters-tools.md) si desea recopilar o ver los datos de rendimiento de un sistema.
- Use las [API de recopilación de contadores de rendimiento](consuming-counter-data.md) cuando desee escribir un script o un programa que recopile datos de rendimiento del sistema local.
- Use [clases de contador de rendimiento de WMI](/windows/desktop/WmiSdk/monitoring-performance-data) si desea recopilar datos de rendimiento de un sistema local o remoto mediante WMI.
- Use las [API de proveedor de contador de rendimiento](providing-counter-data.md) cuando desee publicar datos de rendimiento desde el componente de software.

## <a name="concepts"></a>Conceptos

El sistema de contador de rendimiento de Windows se organiza en **consumidores**, **proveedores**, **contraconjuntos**, **contadores**, **instancias** y **valores de contador**.

Un **consumidor** es un componente de software que hace uso de los datos de rendimiento. Windows incluye varias [herramientas integradas](performance-counters-tools.md) que hacen uso de los datos de rendimiento. Entre ellos se incluyen el administrador de tareas, el Monitor de recursos, el monitor de rendimiento, el typeperf.exe, el logman.exe y el relog.exe. Los desarrolladores pueden escribir scripts y aplicaciones que tengan acceso a los contadores de rendimiento a través de las [API de contador de rendimiento](consuming-counter-data.md).

Un **proveedor** es un componente de software que [genera y publica datos de rendimiento](providing-counter-data.md). Un proveedor publicará los datos de uno o más *contraconjuntos*. Por ejemplo, un sistema de base de datos puede registrarse como un proveedor de datos de rendimiento.

- Un **proveedor v1** es un componente de software que publica los datos de rendimiento a través de un [archivo dll de rendimiento](providing-counter-data-using-a-performance-dll.md) que se ejecuta en el proceso del consumidor. Un proveedor v1 se instala en un sistema a través de un `.ini` archivo. La arquitectura del proveedor V1 está en desuso. Los proveedores nuevos deben usar la arquitectura de proveedor V2.
- Un **proveedor V2** es un componente de software que publica los datos de rendimiento a través de las [API del proveedor de contador de rendimiento](providing-counter-data-using-version-2-0.md). Un proveedor V2 se instala en un sistema a través de un `.man` archivo (manifiesto XML).

Un **CounterSet** es una agrupación de datos de rendimiento dentro de un proveedor. Un CounterSet tiene un nombre y uno o varios *contadores*. Recopilar los datos de un CounterSet devuelve un número de *instancias*. En algunas API de Windows, los contraconjuntos se denominan **objetos de rendimiento**. Por ejemplo, un proveedor de datos de rendimiento para un sistema de base de datos podría proporcionar un CounterSet para las estadísticas por base de datos.

Un **contador** es la definición de un único elemento de datos de rendimiento. Un contador tiene un nombre y un tipo. Por ejemplo, un CounterSet "por cada base de datos" puede contener un contador denominado "transacciones por segundo" con el tipo `PERF_COUNTER_COUNTER` .

Una **instancia** es una entidad sobre la que se envían los datos de rendimiento. Una instancia tiene un nombre (cadena) y uno o más *valores de contador*. Por ejemplo, un CounterSet de "estadísticas por base de datos" puede contener una instancia por base de datos. El nombre de instancia sería el nombre de la base de datos y cada instancia contendría valores de contador para los contadores "transacciones por segundo", "uso de memoria" y "uso de disco".

Un **valor de contador** es el valor de una sola parte de los datos del contador de rendimiento. Un valor de contador es un entero sin signo, de 32 bits o 64 bits, dependiendo del tipo del contador correspondiente. Al hablar sobre una *instancia* de, un *valor de contador* a veces podría llamarse un *contador* o un *valor*.

> [!TIP]
> Puede ser útil relacionar los términos del contador de rendimiento con términos de hoja de cálculo más conocidos. Un **CounterSet** es como una tabla. Un **contador** es como una columna. Una **instancia** es como una fila. Un **valor de contador** es como una celda de la tabla.

Los **contraconjuntos de instancia única** siempre contienen datos para una sola instancia. Esto es común para los contraconjuntos que notifican las estadísticas globales del sistema. Por ejemplo, Windows tiene un CounterSet integrado de instancia única denominado "Memory" que notifica el uso de memoria global.

Los **contraconjuntos de varias** instancias contienen datos para un número variable de instancias. Esto es común para los contraconjuntos que informan sobre las entidades dentro del sistema. Por ejemplo, Windows tiene un CounterSet integrado de varias instancias denominado "información del procesador" que notifica una instancia para cada CPU instalada.

Los consumidores recopilan y registran periódicamente los datos del CounterSet de un proveedor. Por ejemplo, el consumidor podría recopilar los datos una vez por segundo o una vez por minuto. Los datos recopilados se denominan **ejemplo**. Un ejemplo consta de marcas de tiempo junto con los datos de las instancias del CounterSet. Los datos de cada instancia incluyen el nombre de instancia (cadena) y un conjunto de valores de contador (enteros, un valor para cada contador en el CounterSet).

Normalmente, los nombres de instancia deben ser únicos dentro de un ejemplo, es decir, un proveedor no debe devolver dos instancias con el mismo nombre que parte de un único ejemplo. Algunos proveedores antiguos no siguen esta regla, de modo que [los consumidores deben ser capaces de tolerar nombres de instancia no únicos](handling-duplicate-instance-names.md). Los nombres de instancia no distinguen mayúsculas de minúsculas, por lo que las instancias no deben tener nombres que solo difieran en mayúsculas o minúsculas.

> [!NOTE]
> Por motivos de compatibilidad con versiones anteriores, el CounterSet "Process" devuelve nombres de instancia no únicos basados en el nombre de archivo EXE. Esto puede producir resultados confusos, especialmente cuando se inicia o se cierra un proceso con un nombre no único, ya que esto suele dar lugar a problemas de datos debido a la coincidencia incorrecta de los nombres de instancia entre los ejemplos. Los consumidores de los CounterSet "Process" deben ser capaces de tolerar estos nombres de instancia no únicos y los problemas de datos resultantes.

Los nombres de instancia deben ser estables en todas las muestras; es decir, un proveedor debe usar el mismo nombre de instancia para la misma entidad cada vez que se recopile el CounterSet.

Cada contador tiene un tipo. El tipo de contador indica el tipo de **valor sin formato** del contador (entero de 32 bits sin signo o entero de 64 bits sin signo). El tipo de contador también indica lo que representa el valor sin formato del contador, que determina cómo se debe procesar el valor sin formato para generar estadísticas útiles.

Aunque algunos tipos de contador son simples y tienen un valor sin formato que es directamente útil, muchos tipos de contador requieren un [procesamiento adicional](calculating-counter-values.md) para crear un **valor con formato** útil. Para generar el valor con formato, algunos tipos de contador requieren valores sin formato de dos ejemplos, algunos tipos de contador requieren marcas de tiempo y algunos tipos de contador requieren valores sin formato de varios contadores. Por ejemplo:

- `PERF_COUNTER_LARGE_RAWCOUNT` es un valor sin formato de 64 bits que no requiere ningún procesamiento para ser útil. Es adecuado para los valores de un momento dado, como "bytes de memoria en uso".
- `PERF_COUNTER_RAWCOUNT_HEX` es un valor sin formato de 32 bits que requiere que solo el formato hexadecimal sencillo sea útil. Es adecuado para la información de un momento dado o de identificación, como "marcas" o "dirección base".
- `PERF_COUNTER_BULK_COUNT` es un valor sin formato de 64 bits que indica un recuento de eventos y se utiliza para calcular la velocidad a la que se producen los eventos. Para que sea útil, este tipo de contador requiere dos ejemplos que se separan en el tiempo. El valor con formato es la tasa de eventos, es decir, el número de veces que se produjo el evento por segundo durante el intervalo entre los dos ejemplos. Dados dos ejemplos `s0` y `s1` , el valor con formato (tasa de eventos) se calcularía como `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` .

Se espera que los proveedores se comporten como si fueran sin estado, es decir, la recopilación de datos de un CounterSet no debe afectar visiblemente al estado del proveedor. Por ejemplo, un proveedor no debe restablecer los valores de contador en 0 cuando se recopila un CounterSet y no debe usar la marca de tiempo de una colección anterior para ajustar los valores de la colección actual. En su lugar, debe proporcionar valores de contador sin formato sencillos con tipos precisos para que el consumidor pueda calcular estadísticas útiles en función de los valores sin formato y sus marcas de tiempo.

## <a name="performance-api-architecture"></a>Arquitectura de la API de rendimiento

![Las aplicaciones de contador de rendimiento invocan a las API de Windows que llaman a proveedores para obtener datos de rendimiento.](images/architecture.png)

Los consumidores del contador de rendimiento incluyen:

- [Aplicaciones proporcionadas por Microsoft](performance-counters-tools.md) , como administrador de tareas, monitor de recursos, monitor de rendimiento y typeperf.exe.
- Superficies de API de alto nivel proporcionadas por Microsoft que exponen datos del contador de rendimiento, como [las clases de rendimiento de WMI](/windows/desktop/WmiSdk/monitoring-performance-data).
- Sus propias aplicaciones o scripts que usan las [API del consumidor del contador de rendimiento](consuming-counter-data.md).

La mayoría de los consumidores del contador de rendimiento usan las API de [PDH.dll](using-the-pdh-functions-to-consume-counter-data.md) para recopilar datos de rendimiento. PDH administra muchos aspectos complejos de la recopilación de contadores de rendimiento, como el análisis de consultas, la coincidencia de instancias entre varias muestras y el cálculo de valores con formato de los datos del contador sin formato. La implementación de PDH usa las API del registro cuando se consumen datos de un proveedor V1 y usa las API del consumidor V2 al consumir datos de un proveedor V2.

Algunos consumidores de contadores de rendimiento anteriores usan las [API del registro](using-the-registry-functions-to-consume-counter-data.md) para recopilar datos de rendimiento de la `HKEY_PERFORMANCE_DATA` clave del registro especial. Esto no se recomienda para el nuevo código porque el procesamiento de los datos del registro es complejo y propenso a errores. La implementación de la API del registro admite directamente la recopilación de datos de proveedores de v1. Admite la recopilación indirecta de datos de proveedores V2 a través de una capa de traducción que usa las API de consumidor V2.

Algunos consumidores de contadores de rendimiento usan las [funciones de consumidor de Perflib V2](using-the-perflib-functions-to-consume-counter-data.md) para tener acceso directamente a los datos de los proveedores de V2. Esto es más complejo que el consumo de datos mediante las API de PDH, pero este enfoque puede ser útil si no se pueden usar las API de PDH debido a problemas de rendimiento o de dependencia. La implementación de PerfLib V2 admite directamente la recopilación de datos de proveedores de V2. No admite la recopilación de datos de proveedores de v1.

> [!NOTE]
> Windows OneCore no incluye PDH.dll y no incluye compatibilidad para consumir datos de contadores de rendimiento a través de las API del registro. Los consumidores que se ejecutan en OneCore deben usar las funciones de consumidor de PerfLib V2.

Los proveedores v1 se implementan como un archivo DLL de proveedor que se carga en el proceso del consumidor. La implementación de la API del registro administra la carga del archivo DLL del proveedor, la llamada a la DLL para recopilar datos de rendimiento y la descarga del archivo DLL según corresponda. La DLL del proveedor es responsable de la [recopilación de datos de rendimiento según corresponda](communicating-with-your-application.md), por ejemplo, mediante las API normales de Windows, RPC, canalizaciones con nombre, memoria compartida u otros mecanismos de comunicación entre procesos.

Los proveedores de V2 se implementan como un programa en modo de usuario (a menudo un servicio de Windows) o un controlador de modo kernel. Normalmente, el código del proveedor de datos de rendimiento se integra directamente en un componente existente (es decir, el controlador o el servicio informa de las estadísticas sobre sí mismo). La implementación de PerfLib V2 administra las solicitudes y las respuestas a través de la extensión de kernel de PCW.sys, por lo que el proveedor no suele tener que implementar ninguna comunicación entre procesos para proporcionar los datos de rendimiento.

> [!NOTE]
> Las herramientas y API del contador de rendimiento de Windows incluyen compatibilidad limitada para tener acceso a los contadores de rendimiento de otros equipos a través del registro remoto (para los proveedores V1) y RPC (para los proveedores V2). Esta compatibilidad suele ser difícil de usar en términos de controles de autenticación (las herramientas y las API solo se pueden autenticar como el usuario actual) así como en términos de [configuración del sistema](accessing-remote-counter-data.md) (los puntos de conexión y servicios necesarios están deshabilitados de forma predeterminada). En muchos casos, es mejor acceder a los contadores de rendimiento de sistemas remotos mediante [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) en lugar de a través de la compatibilidad de acceso remoto integrada.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Los administradores suelen usar los contadores de rendimiento para identificar problemas de rendimiento o comportamientos anómalos de los sistemas, por parte de los desarrolladores para estudiar el uso de los recursos de los componentes de software y los usuarios individuales para comprender cómo se comportan los programas en su sistema. El uso puede producirse a través de herramientas de GUI como el administrador de tareas o el monitor de rendimiento, herramientas de línea de comandos como typeperf.exe o logman.exe, mediante scripting a través de WMI y PowerShell, o a través de las API de C/C++ y .NET.

Los proveedores de contadores de rendimiento se implementan normalmente como controladores de modo kernel o servicios de modo de usuario. Los proveedores de contadores de rendimiento normalmente se escriben en C o C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.

Para ver [el](performance-counters-what-s-new.md)historial de versiones, consulte las novedades.

## <a name="see-also"></a>Vea también

[Uso de contadores de rendimiento](using-performance-counters.md)

[Referencia de contadores de rendimiento](performance-counters-reference.md)

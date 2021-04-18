---
description: En esta sección se describen las nuevas características que se agregaron a los contadores de rendimiento de cada versión.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Novedades (contadores de rendimiento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667265"
---
# <a name="whats-new-with-performance-counters"></a>Novedades de los contadores de rendimiento

En esta sección se describen las nuevas características que se agregaron a los contadores de rendimiento de cada versión.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

La herramienta [CTRPP](ctrpp.md) se ha cambiado para mejorar y simplificar la generación de código. La herramienta ahora solo genera un archivo de encabezado y de recursos. Si desea un comportamiento de generación de código anterior (no recomendado), puede usar el nuevo `-legacy` argumento.

- Ahora debe especificar los nuevos `-o` argumentos y `-rc` que especifican el nombre y la ubicación del archivo de encabezado y de recursos, respectivamente.
- Puede usar el nuevo argumento opcional `-prefix` para especificar una cadena que se va a agregar al principio de las variables globales y las funciones definidas en el archivo de encabezado generado.
- Si tiene que actualizar el manifiesto de los contadores, el uso de la nueva generación de código elimina la necesidad de fusionar mediante combinación la implementación de devolución de llamada anterior con el nuevo código generado, ya que las devoluciones de llamada ya no se incluyen en el código generado.

Hay un nuevo `symbol` atributo disponible para los siguientes elementos de manifiesto:

- [presta](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [bloque](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

El `symbol` atributo es necesario para el [proveedor](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) y [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)y es opcional para [Counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element). El atributo le permite proporcionar un nombre simbólico que puede usar para hacer referencia a cada elemento al llamar a las funciones de proveedor (por ejemplo, puede usar el nombre simbólico del conjunto de contadores al llamar a [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).

## <a name="windows-vista"></a>Windows Vista

La arquitectura de los contadores de rendimiento para proporcionar datos de contadores se cambió completamente en esta versión.

Anteriormente, se usaba un archivo INI para definir los datos del contador y se implementaba una DLL de rendimiento que se ejecutaba en el proceso del consumidor para proporcionar los datos cuando un consumidor lo solicitaba. Esta arquitectura está en desuso y no se recomienda para el nuevo código debido a problemas de rendimiento y confiabilidad significativos.

La nueva arquitectura utiliza un manifiesto para definir los datos del contador y ejecuta código en el proceso del proveedor para proporcionar los datos cuando un consumidor lo solicita. Para obtener más información, vea [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md).

Se han agregado las siguientes funciones para esta versión:

- [ControlCallback](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [PerfDeleteInstance](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [PerfQueryInstance](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [PerfSetCounterSetInfo](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [PerfSetULongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [PerfSetULongLongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [PerfSetCounterRefValue](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [PerfStartProvider](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [PerfStopProvider](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

Se han agregado las siguientes estructuras para esta versión:

- [\_identidad del contador de rendimiento \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [\_información del contador de rendimiento \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [\_información de COUNTERSET de rendimiento \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [\_instancia de COUNTERSET de rendimiento \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

Para obtener una lista de los elementos XML que se usan en el manifiesto para definir los contadores, vea [esquema de contadores de rendimiento](performance-counters-schema.md).

Para obtener información sobre la herramienta de preprocesador CTRPP que analiza el manifiesto y genera el código que se usa como punto de partida para el proveedor, vea [CTRPP](ctrpp.md).

---
description: En esta sección se describen las nuevas características que se agregaron a contadores de rendimiento para cada versión.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Novedades (contadores de rendimiento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c86a6a9ea644f1c650137cc392a2d54b6e8eedb34881d6b759d7b6c51635d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674705"
---
# <a name="whats-new-with-performance-counters"></a>Novedades de los contadores de rendimiento

En esta sección se describen las nuevas características que se agregaron a contadores de rendimiento para cada versión.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

La [herramienta CTRPP](ctrpp.md) se cambió para mejorar y simplificar la generación de código. Ahora, la herramienta solo genera un archivo de encabezado y de recursos. Si desea un comportamiento anterior de generación de código (no recomendado), puede usar el nuevo `-legacy` argumento .

- Ahora debe especificar los nuevos argumentos y que especifican el nombre y la ubicación del encabezado y el archivo `-o` `-rc` de recursos, respectivamente.
- Puede usar el nuevo argumento opcional para especificar una cadena que se va a agregar al principio de las variables globales y funciones definidas `-prefix` en el archivo de encabezado generado.
- Si tiene que actualizar el manifiesto de contadores, el uso de la nueva generación de código elimina la necesidad de combinar la implementación de devolución de llamada anterior con el nuevo código generado, ya que las devoluciones de llamada ya no se incluyen en el código generado.

Hay un `symbol` nuevo atributo disponible para los siguientes elementos de manifiesto:

- [Proveedor](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [Contador](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

El `symbol` atributo es necesario para provider [y](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) [counterSet,](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)y es opcional para [el contador](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element). El atributo le permite proporcionar un nombre simbólico que puede usar para hacer referencia a cada elemento al llamar a las funciones del proveedor (por ejemplo, puede usar el nombre simbólico del conjunto de contadores al llamar a [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).

## <a name="windows-vista"></a>Windows Vista

La arquitectura de contadores de rendimiento para proporcionar datos de contadores ha cambiado completamente para esta versión.

Anteriormente, usó un archivo INI para definir los datos del contador e implementó un archivo DLL de rendimiento que se ejecutó en el proceso del consumidor para proporcionar los datos cuando un consumidor lo solicitó. Esta arquitectura está en desuso y no se recomienda para el código nuevo debido a problemas significativos de rendimiento y confiabilidad.

La nueva arquitectura usa un manifiesto para definir los datos del contador y ejecuta código en el proceso del proveedor para proporcionar los datos cuando un consumidor lo solicita. Para obtener más información, [vea Proporcionar datos de contador mediante la versión 2.0.](providing-counter-data-using-version-2-0.md)

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

Se agregaron las siguientes estructuras para esta versión:

- [IDENTIDAD DEL \_ CONTADOR DE RENDIMIENTO \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [INFORMACIÓN DEL \_ CONTADOR DE \_ RENDIMIENTO](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [INFORMACIÓN DEL \_ CONJUNTO DE CONTADORES DE \_ RENDIMIENTO](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [INSTANCIA DE \_ CONJUNTO DE CONTADORES DE \_ PERF](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

Para obtener una lista de los elementos XML que se usan en el manifiesto para definir los contadores, vea [Esquema de contadores de rendimiento](performance-counters-schema.md).

Para obtener información sobre la herramienta de preprocesador CTRPP que analiza el manifiesto y genera el código que se usa como punto de partida para el proveedor, vea [CTRPP](ctrpp.md).

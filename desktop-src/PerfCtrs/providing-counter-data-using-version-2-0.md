---
description: Con la versión 2,0, los contadores de rendimiento cambiaron la arquitectura para simplificar el proceso de proporcionar datos de contador a los consumidores.
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: Proporcionar datos de contadores con la versión 2,0
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 67976c8a0b6c77582ed8c50c2e5cf753c77fcf6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667256"
---
# <a name="providing-counter-data-using-version-20"></a>Proporcionar datos de contadores con la versión 2,0

Los proveedores de datos de rendimiento modernos usan un manifiesto para definir los datos del contador y usar las API del proveedor de contadores de rendimiento para administrar los datos en el contexto del proveedor. Los proveedores implementados mediante un manifiesto y las API de proveedor de contadores de rendimiento a menudo se denominan **proveedores V2**. Windows admite proveedores de modo usuario V2 en Windows Vista o posterior y proveedores de modo kernel v2 en Windows 7 o posterior.

En esta página se describen los proveedores de modo usuario V2. Para obtener información acerca de los proveedores de modo kernel v2, consulte [supervisión del rendimiento del modo kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

En tiempo de ejecución, los proveedores de v2 funcionan de la siguiente manera:

- El proceso de proveedor se registra a sí mismo con el sistema de contador de rendimiento de Windows mediante una llamada a PerfStartProvider y PerfSetCounterSetInfo. Opcionalmente, el proveedor proporciona una función de devolución de llamada a la que se notificarán las solicitudes del consumidor.
- El proceso del proveedor agrega o quita las instancias según corresponda mediante PerfCreateInstance y PerfDeleteInstance. El proveedor actualiza los valores de contador cuando cambian con las API de PerfSet * * _.
- Un consumidor realiza una solicitud de datos de un CounterSet. El sistema comprueba que el llamador tiene permisos para recopilar los datos. Después, el sistema usa un subproceso de trabajo que se ejecuta en el proceso del proveedor para controlar la solicitud, invocando la función de devolución de llamada del proveedor si es necesario. El subproceso de trabajo copia los datos recopilados en un búfer administrado por el sistema y, a continuación, el sistema devuelve los datos al consumidor.

## <a name="steps-to-creating-a-provider"></a>Pasos para crear un proveedor

1. Escriba un manifiesto que defina los datos del contador que proporcionará el proveedor. Para obtener más información sobre cómo escribir el manifiesto, vea [esquema de contadores de rendimiento](performance-counters-schema.md).
2. Use [CTRPP](ctrpp.md) para generar el código de plantilla que se incluye en el proveedor. El código de plantilla incluye las estructuras que definen los conjuntos de contadores, las funciones [_ *contrainitial* *](counterinitialize.md) y [**percleanup**](countercleanup.md) y las cadenas de recursos.

   El proveedor debe llamar a las funciones [**contrainitialized**](counterinitialize.md) y de [**limpieza**](countercleanup.md) . La **Contrainicialización** llama a la función [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) para registrar el proveedor y también llama a la función [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) para inicializar el conjunto de contadores. La **perlimpieza** llama a la función [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para quitar el registro del proveedor.

3. Incluya el código de plantilla del paso anterior en el proyecto y complete el proveedor.

   Para completar el proveedor, debe llamar a la función [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) para cada instancia del conjunto de contadores que proporcione.

   Para establecer los valores de los contadores, llame a una de las siguientes funciones:

   - [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   La ventaja de usar [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) es que no es necesario realizar una llamada de función para establecer o actualizar el valor del contador, simplemente se actualiza la variable de contador local (la variable a la que apuntan los puntos de referencia) y los contadores de rendimiento usan el puntero para obtener acceso al valor del contador.

   Si no usa [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue), puede utilizar las siguientes funciones para aumentar o disminuir el valor del contador:

   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   Antes de que se cierre el proveedor, debe llamar a [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) para cada instancia del conjunto de contadores que creó.

   Si especificó el **atributo callback** en el [**elemento Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) del manifiesto o usó el argumento **-NotificationCallback** al llamar a [CTRPP](ctrpp.md), debe implementar la función de devolución de llamada [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) . La función de devolución de llamada se pasa a [**UnInitialize**](counterinitialize.md).

   Si usó **-MemoryRoutines** al llamar a [CTRPP](ctrpp.md), debe implementar las funciones de devolución de llamada [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) y [*FreeMemory (*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) . Las funciones de devolución de llamada se pasan a [**UnInitialize**](counterinitialize.md).

4. Al instalar el proveedor, use la herramienta LodCtr para escribir el nombre del archivo binario que contiene las cadenas de recursos y los identificadores de recursos localizados en el registro. Para obtener más información sobre el uso de LodCtr, vea [esquema de contadores de rendimiento](performance-counters-schema.md).

5. Al desinstalar el proveedor, utilice la herramienta UnlodCtr para quitar la información del proveedor del registro.

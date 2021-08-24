---
description: Con la versión 2.0, los contadores de rendimiento cambiaron la arquitectura para simplificar el proceso de proporcionar datos de contador a los consumidores.
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: Proporcionar datos de contador mediante la versión 2.0
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8e839fb72f8cbd8272f9afd89aa3456e1e0b08fc7197dd992b1069fec7ce108d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143798"
---
# <a name="providing-counter-data-using-version-20"></a>Proporcionar datos de contador mediante la versión 2.0

Los proveedores de datos de rendimiento moderno usan un manifiesto para definir los datos del contador y usar las API del proveedor de contadores de rendimiento para administrar los datos en el contexto del proveedor. Los proveedores implementados mediante un manifiesto y las API de proveedor de contadores de rendimiento a menudo se **denominan proveedores V2.** Windows proveedores de modo de usuario V2 en Windows Vista o versiones posteriores y proveedores de modo kernel V2 en Windows 7 o posterior.

En esta página se describen los proveedores de modo de usuario V2. Para obtener información sobre los proveedores de modo kernel V2, consulte [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

En tiempo de ejecución, los proveedores V2 funcionan de la siguiente manera:

- El proceso de proveedor se registra con el Windows contador de rendimiento mediante una llamada a PerfStartProvider y PerfSetCounterSetInfo. Opcionalmente, el proveedor proporciona una función de devolución de llamada a la que se notificarán las solicitudes del consumidor.
- El proceso de proveedor agrega o quita instancias según corresponda mediante PerfCreateInstance y PerfDeleteInstance. El proveedor actualiza los valores de los contadores cuando cambian mediante las API de PerfSet!.
- Un consumidor realiza una solicitud de datos de un contraconjunto. El sistema comprueba que el autor de la llamada tiene permisos para recopilar los datos. A continuación, el sistema usa un subproceso de trabajo que se ejecuta en el proceso de proveedor para controlar la solicitud, invocando la función de devolución de llamada del proveedor si procede. El subproceso de trabajo copia los datos recopilados en un búfer administrado por el sistema y, a continuación, el sistema devuelve los datos al consumidor.

## <a name="steps-to-creating-a-provider"></a>Pasos para crear un proveedor

1. Escriba un manifiesto que defina los datos del contador que proporcionará el proveedor. Para obtener más información sobre cómo escribir el manifiesto, vea [Esquema de contadores de rendimiento.](performance-counters-schema.md)
2. Use [CTRPP para](ctrpp.md) generar el código de plantilla que incluya en el proveedor. El código de plantilla incluye las estructuras que definen los conjuntos de contadores, las funciones [**CounterInitialize**](counterinitialize.md) y [**CounterCleanup,**](countercleanup.md) y las cadenas de recursos.

   El proveedor debe llamar a [**las funciones CounterInitialize**](counterinitialize.md) [**y CounterCleanup.**](countercleanup.md) **CounterInitialize llama** a la función [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) para registrar el proveedor y también llama a la función [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) para inicializar el conjunto de contadores. **CounterCleanup llama** a la [**función PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para quitar el registro del proveedor.

3. Incluya el código de plantilla del paso anterior en el proyecto y complete el proveedor.

   Para completar el proveedor, debe llamar a la [**función PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) para cada instancia del conjunto de contadores que proporcione.

   Para establecer los valores de contador, llame a una de las siguientes funciones:

   - [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   La ventaja de usar [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) es que no es necesario realizar una llamada de función para establecer o actualizar el valor del contador, simplemente actualiza la variable de contador local (la variable a la que apunta la referencia) y contadores de rendimiento usa el puntero para tener acceso al valor del contador.

   Si no usa [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue), puede usar las siguientes funciones para incrementar o disminuir el valor del contador:

   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   Antes de que se cierre el proveedor, debe llamar a [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) para cada instancia del conjunto de contadores que creó.

   Si especificó el atributo **de** devolución de llamada en el elemento [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) del manifiesto o usó el **argumento -NotificationCallback** al llamar a [CTRPP,](ctrpp.md)debe implementar la función de devolución de llamada [*ControlCallback.*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) La función de devolución de llamada se [**pasa a CounterInitialize.**](counterinitialize.md)

   Si usó **-MemoryRoutines** al llamar a [CTRPP,](ctrpp.md)debe implementar las funciones de devolución de llamada [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) y [*FreeMemory.*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) Las funciones de devolución de llamada se pasan [**a CounterInitialize.**](counterinitialize.md)

4. Al instalar el proveedor, use la herramienta LodCtr para escribir el nombre del archivo binario que contiene las cadenas de recursos localizadas y los identificadores de recursos en el Registro. Para obtener más información sobre el uso de LodCtr, vea [Esquema de contadores de rendimiento.](performance-counters-schema.md)

5. Al desinstalar el proveedor, use la herramienta UnlodCtr para quitar la información del proveedor del Registro.

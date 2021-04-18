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
# <a name="whats-new-with-performance-counters"></a><span data-ttu-id="237ca-103">Novedades de los contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="237ca-103">What's New with Performance Counters</span></span>

<span data-ttu-id="237ca-104">En esta sección se describen las nuevas características que se agregaron a los contadores de rendimiento de cada versión.</span><span class="sxs-lookup"><span data-stu-id="237ca-104">This section describes the new features that were added to Performance Counters for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="237ca-105">Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="237ca-105">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="237ca-106">La herramienta [CTRPP](ctrpp.md) se ha cambiado para mejorar y simplificar la generación de código.</span><span class="sxs-lookup"><span data-stu-id="237ca-106">The [CTRPP](ctrpp.md) tool was changed to improve and simplify code generation.</span></span> <span data-ttu-id="237ca-107">La herramienta ahora solo genera un archivo de encabezado y de recursos.</span><span class="sxs-lookup"><span data-stu-id="237ca-107">The tool now generates only a header and resource file.</span></span> <span data-ttu-id="237ca-108">Si desea un comportamiento de generación de código anterior (no recomendado), puede usar el nuevo `-legacy` argumento.</span><span class="sxs-lookup"><span data-stu-id="237ca-108">If you want to old code generation behavior (not recommended), you can use the new `-legacy` argument.</span></span>

- <span data-ttu-id="237ca-109">Ahora debe especificar los nuevos `-o` argumentos y `-rc` que especifican el nombre y la ubicación del archivo de encabezado y de recursos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="237ca-109">You must now specify the new `-o` and `-rc` arguments that specify the name and location of the header and resource file, respectively.</span></span>
- <span data-ttu-id="237ca-110">Puede usar el nuevo argumento opcional `-prefix` para especificar una cadena que se va a agregar al principio de las variables globales y las funciones definidas en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="237ca-110">You can use the optional new `-prefix` argument to specify a string to add to the beginning of global variables and functions defined in the generated header file.</span></span>
- <span data-ttu-id="237ca-111">Si tiene que actualizar el manifiesto de los contadores, el uso de la nueva generación de código elimina la necesidad de fusionar mediante combinación la implementación de devolución de llamada anterior con el nuevo código generado, ya que las devoluciones de llamada ya no se incluyen en el código generado.</span><span class="sxs-lookup"><span data-stu-id="237ca-111">If you have to update your counters manifest, using the new code generation eliminates the need to merge your previous callback implementation with the new generated code since the callbacks are no longer included in the generated code.</span></span>

<span data-ttu-id="237ca-112">Hay un nuevo `symbol` atributo disponible para los siguientes elementos de manifiesto:</span><span class="sxs-lookup"><span data-stu-id="237ca-112">A new `symbol` attribute is available for the following manifest elements:</span></span>

- [<span data-ttu-id="237ca-113">presta</span><span class="sxs-lookup"><span data-stu-id="237ca-113">provider</span></span>](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [<span data-ttu-id="237ca-114">counterSet</span><span class="sxs-lookup"><span data-stu-id="237ca-114">counterSet</span></span>](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [<span data-ttu-id="237ca-115">bloque</span><span class="sxs-lookup"><span data-stu-id="237ca-115">counter</span></span>](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

<span data-ttu-id="237ca-116">El `symbol` atributo es necesario para el [proveedor](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) y [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)y es opcional para [Counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span><span class="sxs-lookup"><span data-stu-id="237ca-116">The `symbol` attribute is required for [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) and [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element), and is optional for [counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span></span> <span data-ttu-id="237ca-117">El atributo le permite proporcionar un nombre simbólico que puede usar para hacer referencia a cada elemento al llamar a las funciones de proveedor (por ejemplo, puede usar el nombre simbólico del conjunto de contadores al llamar a [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span><span class="sxs-lookup"><span data-stu-id="237ca-117">The attribute lets you provide a symbolic name that you can use to reference each element when calling the provider functions (for example, you can use the counter set symbolic name when calling [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="237ca-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="237ca-118">Windows Vista</span></span>

<span data-ttu-id="237ca-119">La arquitectura de los contadores de rendimiento para proporcionar datos de contadores se cambió completamente en esta versión.</span><span class="sxs-lookup"><span data-stu-id="237ca-119">The Performance Counters architecture for providing counter data was completely changed for this release.</span></span>

<span data-ttu-id="237ca-120">Anteriormente, se usaba un archivo INI para definir los datos del contador y se implementaba una DLL de rendimiento que se ejecutaba en el proceso del consumidor para proporcionar los datos cuando un consumidor lo solicitaba.</span><span class="sxs-lookup"><span data-stu-id="237ca-120">Previously, you used an INI file to define your counter data and you implemented a performance DLL which ran in the consumer's process to provide the data when a consumer requested it.</span></span> <span data-ttu-id="237ca-121">Esta arquitectura está en desuso y no se recomienda para el nuevo código debido a problemas de rendimiento y confiabilidad significativos.</span><span class="sxs-lookup"><span data-stu-id="237ca-121">This architecture is deprecated and is not recommended for new code due to significant performance and reliability issues.</span></span>

<span data-ttu-id="237ca-122">La nueva arquitectura utiliza un manifiesto para definir los datos del contador y ejecuta código en el proceso del proveedor para proporcionar los datos cuando un consumidor lo solicita.</span><span class="sxs-lookup"><span data-stu-id="237ca-122">The new architecture uses a manifest to define the counter data and runs code in the provider's process to provide the data when a consumer requests it.</span></span> <span data-ttu-id="237ca-123">Para obtener más información, vea [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="237ca-123">For additional details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="237ca-124">Se han agregado las siguientes funciones para esta versión:</span><span class="sxs-lookup"><span data-stu-id="237ca-124">The following functions were added for this release:</span></span>

- [<span data-ttu-id="237ca-125">ControlCallback</span><span class="sxs-lookup"><span data-stu-id="237ca-125">ControlCallback</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="237ca-126">PerfCreateInstance</span><span class="sxs-lookup"><span data-stu-id="237ca-126">PerfCreateInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="237ca-127">PerfDeleteInstance</span><span class="sxs-lookup"><span data-stu-id="237ca-127">PerfDeleteInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="237ca-128">PerfQueryInstance</span><span class="sxs-lookup"><span data-stu-id="237ca-128">PerfQueryInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="237ca-129">PerfSetCounterSetInfo</span><span class="sxs-lookup"><span data-stu-id="237ca-129">PerfSetCounterSetInfo</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="237ca-130">PerfSetULongCounterValue</span><span class="sxs-lookup"><span data-stu-id="237ca-130">PerfSetULongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="237ca-131">PerfSetULongLongCounterValue</span><span class="sxs-lookup"><span data-stu-id="237ca-131">PerfSetULongLongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="237ca-132">PerfSetCounterRefValue</span><span class="sxs-lookup"><span data-stu-id="237ca-132">PerfSetCounterRefValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="237ca-133">PerfStartProvider</span><span class="sxs-lookup"><span data-stu-id="237ca-133">PerfStartProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="237ca-134">PerfStopProvider</span><span class="sxs-lookup"><span data-stu-id="237ca-134">PerfStopProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

<span data-ttu-id="237ca-135">Se han agregado las siguientes estructuras para esta versión:</span><span class="sxs-lookup"><span data-stu-id="237ca-135">The following structures were added for this release:</span></span>

- [<span data-ttu-id="237ca-136">\_identidad del contador de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="237ca-136">PERF\_COUNTER\_IDENTITY</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="237ca-137">\_información del contador de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="237ca-137">PERF\_COUNTER\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="237ca-138">\_información de COUNTERSET de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="237ca-138">PERF\_COUNTERSET\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="237ca-139">\_instancia de COUNTERSET de rendimiento \_</span><span class="sxs-lookup"><span data-stu-id="237ca-139">PERF\_COUNTERSET\_INSTANCE</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

<span data-ttu-id="237ca-140">Para obtener una lista de los elementos XML que se usan en el manifiesto para definir los contadores, vea [esquema de contadores de rendimiento](performance-counters-schema.md).</span><span class="sxs-lookup"><span data-stu-id="237ca-140">For a list of the XML elements that you use in your manifest to define your counters, see [Performance Counters Schema](performance-counters-schema.md).</span></span>

<span data-ttu-id="237ca-141">Para obtener información sobre la herramienta de preprocesador CTRPP que analiza el manifiesto y genera el código que se usa como punto de partida para el proveedor, vea [CTRPP](ctrpp.md).</span><span class="sxs-lookup"><span data-stu-id="237ca-141">For information on the CTRPP pre-processor tool that parses your manifest and generates the code that you use as the starting point for your provider, see [CTRPP](ctrpp.md).</span></span>

---
description: Las funciones de PDH se usan para recopilar datos de rendimiento.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Usar las funciones de PDH para consumir datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909706"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a><span data-ttu-id="79c1d-103">Usar las funciones de PDH para consumir datos de contador</span><span class="sxs-lookup"><span data-stu-id="79c1d-103">Using the PDH Functions to Consume Counter Data</span></span>

<span data-ttu-id="79c1d-104">Utilice las funciones de PDH para recopilar datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="79c1d-104">Use the PDH functions to collect performance data.</span></span> <span data-ttu-id="79c1d-105">Las funciones de PDH son más fáciles de usar que las [funciones del registro](using-the-registry-functions-to-consume-counter-data.md) y se pueden usar para tener acceso a los datos de los contadores V1 y V2.</span><span class="sxs-lookup"><span data-stu-id="79c1d-105">The PDH functions are easier to use than the [registry functions](using-the-registry-functions-to-consume-counter-data.md) and can be used to access counter data both V1 and V2 providers.</span></span> <span data-ttu-id="79c1d-106">PDH tiene API para recopilar datos de rendimiento actuales, guardar datos de rendimiento en archivos de registro y leer datos de archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="79c1d-106">PDH has APIs for collecting current performance data, saving performance data to log files, and reading data from log files.</span></span>

> [!Note]
> <span data-ttu-id="79c1d-107">No puede usar las funciones de capa de abstracción auxiliar de datos de rendimiento si está escribiendo aplicaciones de Windows OneCore.</span><span class="sxs-lookup"><span data-stu-id="79c1d-107">You cannot use the Performance Data Helper abstraction-layer functions if you are writing Windows OneCore apps.</span></span> <span data-ttu-id="79c1d-108">En su lugar, use [las funciones de consumidor de Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="79c1d-108">Instead, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

<span data-ttu-id="79c1d-109">PDH es una API de alto nivel que simplifica la recopilación de datos de contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="79c1d-109">PDH is a high-level API that simplifies collecting performance counter data.</span></span> <span data-ttu-id="79c1d-110">Ayuda con el análisis de consultas, el almacenamiento en caché de metadatos, la coincidencia de instancias entre ejemplos, el cálculo de valores con formato de valores sin formato, la lectura de datos de archivos de registro y el almacenamiento de datos en archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="79c1d-110">It helps with query parsing, metadata caching, matching up instances between samples, computing formatted values from raw values, reading data from log files, and saving data to log files.</span></span> <span data-ttu-id="79c1d-111">PDH utiliza automáticamente las [funciones del registro](using-the-registry-functions-to-consume-counter-data.md) cuando se recopilan datos de los **proveedores v1** y usa las [funciones del consumidor V2](using-the-perflib-functions-to-consume-counter-data.md) al recopilar datos de **proveedores V2**.</span><span class="sxs-lookup"><span data-stu-id="79c1d-111">PDH automatically uses the [registry functions](using-the-registry-functions-to-consume-counter-data.md) when collecting data from **V1 providers** and it uses the [V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) when collecting data from **V2 providers**.</span></span>

<span data-ttu-id="79c1d-112">Para recopilar datos de rendimiento mediante las funciones de PDH, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="79c1d-112">To collect performance data using the PDH functions, perform the following steps.</span></span>

1. [<span data-ttu-id="79c1d-113">Creación de una consulta</span><span class="sxs-lookup"><span data-stu-id="79c1d-113">Create a query</span></span>](creating-a-query.md)
2. [<span data-ttu-id="79c1d-114">Agregar contadores a la consulta</span><span class="sxs-lookup"><span data-stu-id="79c1d-114">Add counters to the query</span></span>](creating-a-query.md)
3. [<span data-ttu-id="79c1d-115">Recopilar los datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="79c1d-115">Collect the performance data</span></span>](collecting-performance-data.md)
4. [<span data-ttu-id="79c1d-116">Mostrar los datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="79c1d-116">Display the performance data</span></span>](displaying-performance-data.md)
5. [<span data-ttu-id="79c1d-117">Cerrar la consulta</span><span class="sxs-lookup"><span data-stu-id="79c1d-117">Close the query</span></span>](creating-a-query.md)

<span data-ttu-id="79c1d-118">Puede recopilar datos de rendimiento de orígenes en tiempo real o archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="79c1d-118">You can collect performance data from either real-time sources or log files.</span></span> <span data-ttu-id="79c1d-119">Para obtener más información sobre cómo escribir datos de rendimiento en archivos de registro, vea [trabajar con archivos de registro](working-with-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="79c1d-119">For more information on how to write performance data to log files, see [Working with Log Files](working-with-log-files.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="79c1d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="79c1d-120">See also</span></span>

- [<span data-ttu-id="79c1d-121">Recopilación de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="79c1d-121">Collecting Performance Data</span></span>](collecting-performance-data.md)
- [<span data-ttu-id="79c1d-122">Examinar contadores</span><span class="sxs-lookup"><span data-stu-id="79c1d-122">Browsing Counters</span></span>](browsing-counters.md)
- [<span data-ttu-id="79c1d-123">Comprobar los valores devueltos de la interfaz PDH</span><span class="sxs-lookup"><span data-stu-id="79c1d-123">Checking PDH Interface Return Values</span></span>](checking-pdh-interface-return-values.md)
- [<span data-ttu-id="79c1d-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="79c1d-124">Examples</span></span>](examples.md)

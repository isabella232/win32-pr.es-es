---
description: El tipo de contador de rendimiento designa una fórmula necesaria para obtener los contadores de rendimiento calculados. Estos son los mismos tipos de contador usados por la supervisión de rendimiento de Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Tipos de contador de rendimiento de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155993"
---
# <a name="wmi-performance-counter-types"></a><span data-ttu-id="78a43-104">Tipos de contador de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="78a43-104">WMI Performance Counter Types</span></span>

<span data-ttu-id="78a43-105">El [tipo de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) de rendimiento designa una fórmula necesaria para obtener los contadores de rendimiento calculados.</span><span class="sxs-lookup"><span data-stu-id="78a43-105">The performance [counter type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) designates a formula required to obtain calculated performance counters.</span></span> <span data-ttu-id="78a43-106">Estos son los mismos tipos de contador usados por la [supervisión de rendimiento](/windows/desktop/PerfCtrs/performance-counters-portal)de Windows.</span><span class="sxs-lookup"><span data-stu-id="78a43-106">These are the same counter types used by Windows [Performance Monitoring](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="78a43-107">En las clases de rendimiento de WMI, los datos sin procesar de la fórmula de tipo de contador proceden de una clase [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y el resultado calculado se encuentra en la propiedad con el mismo nombre de la clase [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="78a43-107">In WMI performance classes, the raw data for the counter type formula comes from a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and the calculated result is found in the same-named property of a corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class.</span></span>

<span data-ttu-id="78a43-108">Los tipos de contador aparecen como calificador de **contratipo** para las propiedades de las clases [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) y como calificador **CookingType** para las propiedades de las clases [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="78a43-108">Counter types appear as the **CounterType** qualifier for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes, and as the **CookingType** qualifier for properties in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="78a43-109">Por ejemplo, la propiedad **AvgDiskBytesPerRead** de la clase [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) es el origen de datos sin procesar de la propiedad **AvgDiskBytesPerRead** de la clase [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), que contiene los mismos datos que se muestran en el monitor de sistema.</span><span class="sxs-lookup"><span data-stu-id="78a43-109">For example, the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class is the raw data source for the **AvgDiskBytesPerRead** property in the class [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), which contains the same data as shown in System Monitor.</span></span>

<span data-ttu-id="78a43-110">La lista siguiente organiza las descripciones de los tipos de contador por tipo funcional:</span><span class="sxs-lookup"><span data-stu-id="78a43-110">The following list organizes counter type descriptions by functional type:</span></span>

-   [<span data-ttu-id="78a43-111">Tipos de contador base</span><span class="sxs-lookup"><span data-stu-id="78a43-111">Base Counter Types</span></span>](base-counter-types.md)
-   [<span data-ttu-id="78a43-112">Tipos de contadores de algoritmo básicos</span><span class="sxs-lookup"><span data-stu-id="78a43-112">Basic Algorithm Counter Types</span></span>](basic-algorithm-counter-types.md)
-   [<span data-ttu-id="78a43-113">Tipos de contador del algoritmo Counter</span><span class="sxs-lookup"><span data-stu-id="78a43-113">Counter Algorithm Counter Types</span></span>](counter-algorithm-counter-types.md)
-   [<span data-ttu-id="78a43-114">Tipos de contador no computacional</span><span class="sxs-lookup"><span data-stu-id="78a43-114">Noncomputational Counter Types</span></span>](noncomputational-counter-types.md)
-   [<span data-ttu-id="78a43-115">Tipos de contador del algoritmo de temporizador de precisión</span><span class="sxs-lookup"><span data-stu-id="78a43-115">Precision Timer Algorithm Counter Types</span></span>](precision-timer-algorithm-counter-types.md)
-   [<span data-ttu-id="78a43-116">Tipos de contador del algoritmo de longitud de cola</span><span class="sxs-lookup"><span data-stu-id="78a43-116">Queue-length Algorithm Counter Types</span></span>](queue-length-algorithm-counter-types.md)
-   [<span data-ttu-id="78a43-117">Tipos de contadores estadísticos</span><span class="sxs-lookup"><span data-stu-id="78a43-117">Statistical Counter Types</span></span>](statistical-counter-types.md)
-   [<span data-ttu-id="78a43-118">Tipos de contadores del algoritmo Timer</span><span class="sxs-lookup"><span data-stu-id="78a43-118">Timer Algorithm Counter Types</span></span>](timer-algorithm-counter-types.md)

 

 

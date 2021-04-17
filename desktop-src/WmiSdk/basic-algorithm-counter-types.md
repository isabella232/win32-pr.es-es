---
description: Representan diferencias entre las muestras a lo largo del tiempo y, a menudo, usan un valor base para el cálculo.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706934"
---
# <a name="basic-algorithm-counter-types"></a><span data-ttu-id="429ae-103">Tipos de contadores de algoritmo básicos</span><span class="sxs-lookup"><span data-stu-id="429ae-103">Basic Algorithm Counter Types</span></span>

<span data-ttu-id="429ae-104">Normalmente, los tipos de contadores de algoritmos básicos representan diferencias entre muestras a lo largo del tiempo y, a menudo, usan un valor base para el cálculo.</span><span class="sxs-lookup"><span data-stu-id="429ae-104">Basic algorithm counter types generally represent differences between samples over time, and often use a base value for the calculation.</span></span> <span data-ttu-id="429ae-105">Por ejemplo, la propiedad **PercentFreeSpace** de la clase [**Win32 \_ PerfFormattedData \_ perfdisk \_ DiscoFísico**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representa la relación entre el espacio libre disponible en la unidad de disco físico y el espacio utilizable total proporcionado por la unidad de disco físico seleccionada.</span><span class="sxs-lookup"><span data-stu-id="429ae-105">For example, the **PercentFreeSpace** property of the [**Win32\_PerfFormattedData\_PerfDisk\_PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class represents the ratio of the free space available on the physical disk unit to the total usable space provided by the selected physical disk drive.</span></span> <span data-ttu-id="429ae-106">Esta clase también contiene el valor base **PercentFreeSpace \_ base**.</span><span class="sxs-lookup"><span data-stu-id="429ae-106">This class also contains the base value, **PercentFreeSpace\_Base**.</span></span> <span data-ttu-id="429ae-107">El porcentaje de espacio libre en disco se obtiene dividiendo **PercentFreeSpace** por **PercentFreeSpace \_ base** y multiplicando por 100%.</span><span class="sxs-lookup"><span data-stu-id="429ae-107">The percentage of free disk space is obtained by dividing **PercentFreeSpace** by **PercentFreeSpace\_Base** and multiplying by 100%.</span></span>

<span data-ttu-id="429ae-108">Se proporcionan los algoritmos básicos de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="429ae-108">The basic algorithms in the following table are provided.</span></span>



| <span data-ttu-id="429ae-109">Contratipo (constante)</span><span class="sxs-lookup"><span data-stu-id="429ae-109">CounterType Constant</span></span>                                                                                    | <span data-ttu-id="429ae-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="429ae-110">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="429ae-111">[Rendimiento \_ de \_Fracción](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 537003008</span><span class="sxs-lookup"><span data-stu-id="429ae-111">[PERF\_RAW\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 537003008</span></span><br/>       | <span data-ttu-id="429ae-112">Relación entre un subconjunto y su conjunto como porcentaje.</span><span class="sxs-lookup"><span data-stu-id="429ae-112">Ratio of a subset to its set as a percentage.</span></span> <span data-ttu-id="429ae-113">Este tipo de contador muestra únicamente el porcentaje actual, no un promedio a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="429ae-113">This counter type displays the current percentage only, not an average over time.</span></span>                                    |
| <span data-ttu-id="429ae-114">[Rendimiento \_ de EJEMPLO de \_ fracción](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 549585920</span><span class="sxs-lookup"><span data-stu-id="429ae-114">[PERF\_SAMPLE\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 549585920</span></span><br/>    | <span data-ttu-id="429ae-115">Proporción media de aciertos de todas las operaciones durante los dos últimos intervalos de muestra.</span><span class="sxs-lookup"><span data-stu-id="429ae-115">Average ratio of hits to all operations during the last two sample intervals.</span></span> <span data-ttu-id="429ae-116">Este tipo de contador requiere una propiedad base con el \_ tipo de contador base de ejemplo de rendimiento \_ .</span><span class="sxs-lookup"><span data-stu-id="429ae-116">This counter type requires a base property with the PERF\_SAMPLE\_BASE counter type.</span></span> |
| <span data-ttu-id="429ae-117">[Rendimiento \_ de CONTADOR decimal \_ DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4195328</span><span class="sxs-lookup"><span data-stu-id="429ae-117">[PERF\_COUNTER\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328</span></span><br/>        | <span data-ttu-id="429ae-118">Este tipo de contador muestra la variación del atributo que se ha medido entre los dos intervalos de muestra más recientes.</span><span class="sxs-lookup"><span data-stu-id="429ae-118">This counter type shows the change in the measured attribute between the two most recent sample intervals.</span></span>                                                         |
| <span data-ttu-id="429ae-119">[Rendimiento \_ de CONTADOR \_ de \_ diferencia Decimal grande](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4195584</span><span class="sxs-lookup"><span data-stu-id="429ae-119">[PERF\_COUNTER\_LARGE\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195584</span></span><br/> | <span data-ttu-id="429ae-120">Igual que \_ \_ la diferencia de contador de rendimiento, pero una representación de 64 bits para valores mayores.</span><span class="sxs-lookup"><span data-stu-id="429ae-120">Same as PERF\_COUNTER\_DELTA but a 64-bit representation for larger values.</span></span>                                                                                        |
| <span data-ttu-id="429ae-121">[Rendimiento \_ de Decimal de \_ tiempo transcurrido](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))807666944</span><span class="sxs-lookup"><span data-stu-id="429ae-121">[PERF\_ELAPSED\_TIME](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 807666944</span></span><br/>       | <span data-ttu-id="429ae-122">Tiempo total entre el inicio del proceso y el momento en que se calcula este valor.</span><span class="sxs-lookup"><span data-stu-id="429ae-122">Total time between when the process started and the time when this value is calculated.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="429ae-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="429ae-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="429ae-124">Tipos de contador de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="429ae-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 


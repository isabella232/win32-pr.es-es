---
description: Los tipos de contador del algoritmo de contador pueden calcular las tasas o promedios de bytes para una muestra o un período de tiempo para una operación determinada.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Tipos de contador del algoritmo Counter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360948"
---
# <a name="counter-algorithm-counter-types"></a><span data-ttu-id="22ab1-103">Tipos de contador del algoritmo Counter</span><span class="sxs-lookup"><span data-stu-id="22ab1-103">Counter Algorithm Counter Types</span></span>

<span data-ttu-id="22ab1-104">Los tipos de contador del algoritmo de contador pueden calcular las tasas o promedios de bytes para una muestra o un período de tiempo para una operación determinada.</span><span class="sxs-lookup"><span data-stu-id="22ab1-104">Counter algorithm counter types may calculate rates or averages bytes for a sample or over a time period for a particular operation.</span></span>

<span data-ttu-id="22ab1-105">La propiedad **AvgDiskBytesPerTransfer** de la clase [**Win32 \_ PerfRawData \_ perfdisk \_ DiscoFísico**](/previous-versions//aa394308(v=vs.85)) usa el tipo de valor medio de la media de rendimiento \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="22ab1-105">The **AvgDiskBytesPerTransfer** property in the [**Win32\_PerfRawData\_PerfDisk\_PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) class uses the PERF\_AVERAGE\_BULK countertype.</span></span> <span data-ttu-id="22ab1-106">En este caso, la transferencia es la operación y el número acumulado de bytes que se envían son los datos del contador.</span><span class="sxs-lookup"><span data-stu-id="22ab1-106">In this case, the transfer is the operation, and the accumulating number of bytes that are sent is the counter data.</span></span> <span data-ttu-id="22ab1-107">En el caso de dos muestras cualesquiera, la división de la diferencia de los bytes acumulados por la diferencia en el acumulado de transferencias producirá el número promedio de bytes por transferencia durante el período de tiempo entre los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="22ab1-107">For any two samples, dividing the difference of accumulated bytes by the difference in accumulating transfers will produce the average number of bytes per transfer during the period between the samples.</span></span>

<span data-ttu-id="22ab1-108">Se proporcionan los siguientes algoritmos de contador:</span><span class="sxs-lookup"><span data-stu-id="22ab1-108">The following counter algorithms are provided:</span></span>



| <span data-ttu-id="22ab1-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="22ab1-109">CounterType</span></span>                                                                                              | <span data-ttu-id="22ab1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="22ab1-110">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22ab1-111">[Rendimiento \_ de PROMEDIO \_ ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))de Decimal bulk 1073874176</span><span class="sxs-lookup"><span data-stu-id="22ab1-111">[PERF\_AVERAGE\_BULK](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073874176</span></span><br/>       | <span data-ttu-id="22ab1-112">Número de elementos procesados, como promedio, durante una operación.</span><span class="sxs-lookup"><span data-stu-id="22ab1-112">Number of items processed, on average, during an operation.</span></span> <span data-ttu-id="22ab1-113">Este tipo de contador muestra la relación entre los elementos procesados (por ejemplo, bytes enviados) y el número de operaciones completadas, y requiere una propiedad base con \_ el promedio de rendimiento \_ base como el tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="22ab1-113">This counter type displays a ratio of the items processed (such as bytes sent) to the number of operations completed, and requires a base property with PERF\_AVERAGE\_BASE as the counter type.</span></span> |
| <span data-ttu-id="22ab1-114">[Rendimiento \_ de Contador \_ Decimal 272696320](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="22ab1-114">[PERF\_COUNTER\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320</span></span><br/>     | <span data-ttu-id="22ab1-115">Número promedio de operaciones completadas durante cada segundo del intervalo de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="22ab1-115">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="22ab1-116">.</span><span class="sxs-lookup"><span data-stu-id="22ab1-116">.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="22ab1-117">[Rendimiento \_ de EJEMPLO de \_ contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4260864</span><span class="sxs-lookup"><span data-stu-id="22ab1-117">[PERF\_SAMPLE\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864</span></span><br/>        | <span data-ttu-id="22ab1-118">Número promedio de operaciones completadas en un segundo.</span><span class="sxs-lookup"><span data-stu-id="22ab1-118">Average number of operations completed in one second.</span></span> <span data-ttu-id="22ab1-119">Este tipo de contador requiere una propiedad base con el tipo de contador base de ejemplo de rendimiento \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="22ab1-119">This counter type requires a base property with the counter type PERF\_SAMPLE\_BASE.</span></span>                                                                                                                   |
| <span data-ttu-id="22ab1-120">[Rendimiento \_ de CONTADOR \_ de \_ recuento](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 272696576</span><span class="sxs-lookup"><span data-stu-id="22ab1-120">[PERF\_COUNTER\_BULK\_COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576</span></span><br/> | <span data-ttu-id="22ab1-121">Número promedio de operaciones completadas durante cada segundo del intervalo de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="22ab1-121">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="22ab1-122">Este tipo de contador es igual que el \_ tipo de contador de contadores de rendimiento \_ , pero utiliza campos de mayor tamaño para acomodar valores mayores.</span><span class="sxs-lookup"><span data-stu-id="22ab1-122">This counter type is the same as the PERF\_COUNTER\_COUNTER type, but it uses larger fields to accommodate larger values.</span></span>                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="22ab1-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22ab1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22ab1-124">Tipos de contador de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="22ab1-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 


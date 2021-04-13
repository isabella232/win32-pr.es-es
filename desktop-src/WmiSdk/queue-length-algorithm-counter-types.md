---
description: Los tipos de contadores del algoritmo de longitud de cola aumentan el número de elementos de una cola en cada intervalo de muestra según se especifica en la propiedad de frecuencia adecuada&\# 8212; Frequency \_ PerfTime, etc.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Tipos de contador del algoritmo de longitud de cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276150"
---
# <a name="queue-length-algorithm-counter-types"></a><span data-ttu-id="b7247-103">Tipos de contador del algoritmo de longitud de cola</span><span class="sxs-lookup"><span data-stu-id="b7247-103">Queue-length Algorithm Counter Types</span></span>

<span data-ttu-id="b7247-104">Los tipos de contadores del algoritmo de longitud de cola aumentan el número de elementos de una cola en cada intervalo de muestra según lo especificado por la frecuencia de propiedad de frecuencia adecuada \_ PerfTime, etc.</span><span class="sxs-lookup"><span data-stu-id="b7247-104">Queue-length algorithm counter types increment the number of items in a queue at each sample interval as specified by the appropriate frequency property Frequency\_PerfTime, and so on.</span></span> <span data-ttu-id="b7247-105">El resultado cocido divide el número de muestras para generar la longitud media de la cola.</span><span class="sxs-lookup"><span data-stu-id="b7247-105">The cooked result divides by the number of samples to produce the average queue length.</span></span>

<span data-ttu-id="b7247-106">Un ejemplo es la propiedad **AvgDiskQueueLength** en el [**PerfRawData de Win32 de Win32 \_ \_ \_**](./retrieving-raw-and-formatted-performance-data.md) que usa el \_ tipo de \_ contador Perf \_ QUEUELEN \_ Type.</span><span class="sxs-lookup"><span data-stu-id="b7247-106">An example is the **AvgDiskQueueLength** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) that uses the PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE counter type.</span></span>



| <span data-ttu-id="b7247-107">Contratipo (constante)</span><span class="sxs-lookup"><span data-stu-id="b7247-107">CounterType Constant</span></span>                                                                                                 | <span data-ttu-id="b7247-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7247-108">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7247-109">[Rendimiento \_ de COUNTER \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4523008</span><span class="sxs-lookup"><span data-stu-id="b7247-109">[PERF\_COUNTER\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span></span><br/>            | <span data-ttu-id="b7247-110">Promedio de longitud de una cola a un recurso a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="b7247-110">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="b7247-111">Muestra la diferencia entre las longitudes de cola observadas durante los dos últimos intervalos de muestra, dividida por la duración del intervalo.</span><span class="sxs-lookup"><span data-stu-id="b7247-111">It shows the difference between the queue lengths observed during the last two sample intervals divided by the duration of the interval.</span></span>                       |
| <span data-ttu-id="b7247-112">[Rendimiento \_ de COUNTER \_ Large \_ QUEUELEN \_ Type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4523264</span><span class="sxs-lookup"><span data-stu-id="b7247-112">[PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span></span><br/>     | <span data-ttu-id="b7247-113">Promedio de longitud de una cola a un recurso a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="b7247-113">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="b7247-114">Los contadores de este tipo muestran la diferencia entre las longitudes de cola observadas durante los dos últimos intervalos de muestra, dividida por la duración del intervalo.</span><span class="sxs-lookup"><span data-stu-id="b7247-114">Counters of this type display the difference between the queue lengths observed during the last two sample intervals, divided by the duration of the interval.</span></span> |
| <span data-ttu-id="b7247-115">[Rendimiento \_ de CONTADOR de \_ 100 NS \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 5571840</span><span class="sxs-lookup"><span data-stu-id="b7247-115">[PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span></span><br/>     | <span data-ttu-id="b7247-116">Promedio de longitud de una cola a un recurso a lo largo del tiempo en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="b7247-116">Average length of a queue to a resource over time in 100 nanosecond units.</span></span>                                                                                                                                        |
| <span data-ttu-id="b7247-117">[Rendimiento \_ de COUNTER \_ obj \_ Time \_ QUEUELEN \_ Type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 6620416</span><span class="sxs-lookup"><span data-stu-id="b7247-117">[PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span></span><br/> | <span data-ttu-id="b7247-118">Hora en la que un objeto está en una cola.</span><span class="sxs-lookup"><span data-stu-id="b7247-118">Time an object is in a queue.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="b7247-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7247-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7247-120">Tipos de contador de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="b7247-120">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 


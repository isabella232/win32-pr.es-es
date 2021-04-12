---
description: Los tipos de contador no computacional no tienen una fórmula asociada. El valor sin formato es directamente significativo.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Tipos de contador no computacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277703"
---
# <a name="noncomputational-counter-types"></a><span data-ttu-id="e42c9-104">Tipos de contador no computacional</span><span class="sxs-lookup"><span data-stu-id="e42c9-104">Noncomputational Counter Types</span></span>

<span data-ttu-id="e42c9-105">Los tipos de contador no computacional no tienen una fórmula asociada.</span><span class="sxs-lookup"><span data-stu-id="e42c9-105">Noncomputational counter types do not have an associated formula.</span></span> <span data-ttu-id="e42c9-106">El valor sin formato es directamente significativo.</span><span class="sxs-lookup"><span data-stu-id="e42c9-106">The raw value is directly meaningful.</span></span>

<span data-ttu-id="e42c9-107">La propiedad **FilesToBeIndexed** de la [**clase \_ \_ \_ IndexingService ContentIndex de Win32 PerfRawData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) es un ejemplo del tipo de contador **Perf \_ Counter \_ RAWCOUNT** .</span><span class="sxs-lookup"><span data-stu-id="e42c9-107">The **FilesToBeIndexed** property in the [**Win32\_PerfRawData\_ContentIndex\_IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class is an example of the **PERF\_COUNTER\_RAWCOUNT** counter type.</span></span> <span data-ttu-id="e42c9-108">Contiene un recuento de archivos que no se han indexado.</span><span class="sxs-lookup"><span data-stu-id="e42c9-108">It contains a count of files that have not been indexed.</span></span>

<span data-ttu-id="e42c9-109">Los tipos de contador se designan mediante la constante definida en WINPERF. h, que se encuentra en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e42c9-109">Counter types are designated by the constant defined in Winperf.h located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e42c9-110">En la tabla siguiente se enumeran los tipos de contador no computacional que se proporcionan.</span><span class="sxs-lookup"><span data-stu-id="e42c9-110">The following table lists the noncomputational counter types that are provided.</span></span>



| <span data-ttu-id="e42c9-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e42c9-111">CounterType</span></span>                                                                                                 | <span data-ttu-id="e42c9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e42c9-112">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e42c9-113">[Rendimiento \_ de \_Texto del contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 2816</span><span class="sxs-lookup"><span data-stu-id="e42c9-113">[PERF\_COUNTER\_TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816</span></span><br/>                | <span data-ttu-id="e42c9-114">Este tipo de contador muestra una cadena de texto de longitud variable en Unicode.</span><span class="sxs-lookup"><span data-stu-id="e42c9-114">This counter type shows a variable-length text string in Unicode.</span></span> <span data-ttu-id="e42c9-115">No muestra los valores calculados.</span><span class="sxs-lookup"><span data-stu-id="e42c9-115">It does not display calculated values.</span></span>               |
| <span data-ttu-id="e42c9-116">[Rendimiento \_ de COUNTER \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 65536</span><span class="sxs-lookup"><span data-stu-id="e42c9-116">[PERF\_COUNTER\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536</span></span><br/>           | <span data-ttu-id="e42c9-117">Valor del contador sin formato que no requiere cálculos y representa una muestra que es solo el último valor observado.</span><span class="sxs-lookup"><span data-stu-id="e42c9-117">Raw counter value that does not require calculations, and represents one sample which is the last observed value only.</span></span> |
| <span data-ttu-id="e42c9-118">[Rendimiento \_ de COUNTER \_ Large \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 65792</span><span class="sxs-lookup"><span data-stu-id="e42c9-118">[PERF\_COUNTER\_LARGE\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span></span><br/>    | <span data-ttu-id="e42c9-119">Igual que **el \_ contador \_ de rendimiento RAWCOUNT**, pero una representación de 64 bits para valores mayores.</span><span class="sxs-lookup"><span data-stu-id="e42c9-119">Same as **PERF\_COUNTER\_RAWCOUNT**, but a 64-bit representation for larger values.</span></span>                                    |
| <span data-ttu-id="e42c9-120">[Rendimiento \_ de COUNTER \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span><span class="sxs-lookup"><span data-stu-id="e42c9-120">[PERF\_COUNTER\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span></span><br/>                  | <span data-ttu-id="e42c9-121">Valor observado más recientemente en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e42c9-121">Most recently observed value in hexadecimal format.</span></span> <span data-ttu-id="e42c9-122">No muestra promedios.</span><span class="sxs-lookup"><span data-stu-id="e42c9-122">It does not display an average.</span></span>                                    |
| <span data-ttu-id="e42c9-123">[Rendimiento \_ de COUNTER \_ Large \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 256</span><span class="sxs-lookup"><span data-stu-id="e42c9-123">[PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256</span></span><br/> | <span data-ttu-id="e42c9-124">Igual que **el \_ contador de rendimiento \_ RAWCOUNT \_ Hex**, pero una representación de 64 bits en formato hexadecimal para su uso con valores grandes.</span><span class="sxs-lookup"><span data-stu-id="e42c9-124">Same as **PERF\_COUNTER\_RAWCOUNT\_HEX**, but a 64-bit representation in hexadecimal for use with large values.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e42c9-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e42c9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e42c9-126">Tipos de contador de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="e42c9-126">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 


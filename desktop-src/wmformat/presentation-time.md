---
title: Tiempo de presentación
description: Tiempo de presentación
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- SDK de Windows Media Format, tiempos de presentación
- Advanced Systems Format (ASF), tiempos de presentación
- ASF (formato de sistemas avanzados), tiempos de presentación
- tiempos de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357530"
---
# <a name="presentation-time"></a><span data-ttu-id="24842-107">Tiempo de presentación</span><span class="sxs-lookup"><span data-stu-id="24842-107">Presentation Time</span></span>

<span data-ttu-id="24842-108">Un tiempo de presentación es una medida de tiempo desde la primera muestra de la primera secuencia en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="24842-108">A presentation time is a measurement of time from the first sample of the first stream in an ASF file.</span></span> <span data-ttu-id="24842-109">Esta medida, así como la mayoría de las demás medidas de tiempo usadas por los objetos de este SDK, se encuentra en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="24842-109">This measurement, as well as most other measurements of time used by the objects of this SDK, is in 100-nanosecond units.</span></span> <span data-ttu-id="24842-110">Los tiempos de presentación son importantes porque permiten sincronizar las diversas secuencias en un archivo.</span><span class="sxs-lookup"><span data-stu-id="24842-110">Presentation times are important because they enable the various streams in a file to be synchronized.</span></span> <span data-ttu-id="24842-111">Debe proporcionar un tiempo de presentación para cada ejemplo de entrada que pase al sistema de escritura.</span><span class="sxs-lookup"><span data-stu-id="24842-111">You must supply a presentation time for each input sample you pass to the writer.</span></span> <span data-ttu-id="24842-112">Cada objeto de datos de la sección de datos de un archivo ASF tiene un tiempo de presentación asociado a él.</span><span class="sxs-lookup"><span data-stu-id="24842-112">Every data object in the data section of an ASF file has a presentation time associated with it.</span></span> <span data-ttu-id="24842-113">Cada ejemplo de salida recuperado por el lector también tiene un tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="24842-113">Every output sample retrieved by the reader also has a presentation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24842-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24842-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24842-115">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="24842-115">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="24842-116">**Entradas, secuencias y salidas**</span><span class="sxs-lookup"><span data-stu-id="24842-116">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="24842-117">**Ejemplos de medios**</span><span class="sxs-lookup"><span data-stu-id="24842-117">**Media Samples**</span></span>](media-samples.md)
</dt> </dl>

 

 





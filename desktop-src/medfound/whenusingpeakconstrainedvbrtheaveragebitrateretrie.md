---
description: Cuando utilizo VBR máxima restringida, la velocidad de bits promedio recuperada del objeto de códec es mayor que la velocidad de bits máxima.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Cuando utilizo VBR máxima restringida, la velocidad de bits promedio recuperada del objeto de códec es mayor que la velocidad de bits máxima. ¿Cómo es posible?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360567"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a><span data-ttu-id="1ef5a-104">Cuando utilizo VBR máxima restringida, la velocidad de bits promedio recuperada del objeto de códec es mayor que la velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-104">When I use peak-constrained VBR, the average bit rate retrieved from the codec object is larger than the peak bit rate.</span></span> <span data-ttu-id="1ef5a-105">¿Cómo es posible?</span><span class="sxs-lookup"><span data-stu-id="1ef5a-105">How is that possible?</span></span>

<span data-ttu-id="1ef5a-106">La relación entre la velocidad de bits promedio y la velocidad de bits pico suele ser errónea.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-106">The relationship between the average bit rate and the peak bit rate is often misunderstood.</span></span> <span data-ttu-id="1ef5a-107">La velocidad de bits máxima describe una restricción de búfer durante un período de tiempo especificado por la ventana de búfer máximo.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-107">The peak bit rate describes a buffer constraint over a period of time specified by the peak buffer window.</span></span> <span data-ttu-id="1ef5a-108">La velocidad de bits promedio para VBR de dos pasos (sin restricciones o con límite máximo) es el promedio de bits por segundo a lo largo de la duración del archivo.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-108">The average bit rate for two-pass VBR (unconstrained or peak-constrained) is the average bits per second over the duration of the file.</span></span>

<span data-ttu-id="1ef5a-109">Tal y como se describe en [el modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md), la velocidad de bits real usada durante un período de tiempo igual a la ventana de búfer puede alcanzar el doble de velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-109">As described in [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md), the actual bit rate used over a period of time equal to the buffer window can approach twice the bit rate.</span></span> <span data-ttu-id="1ef5a-110">Esto se debe a que el búfer, definido como un número de bits igual a la velocidad de bits, la ventana de búfer (en segundos), se vacía a una velocidad constante.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-110">This is because the buffer, defined as a number of bits equal to the bit rate times the buffer window (in seconds), is being emptied at a constant rate.</span></span>

<span data-ttu-id="1ef5a-111">Por ejemplo, en un segundo de una secuencia de 56 kbps, el codificador crea ejemplos con un total de 59 KB.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-111">For example, in one second of a 56 Kbps stream, the encoder creates samples totaling 59 Kb.</span></span> <span data-ttu-id="1ef5a-112">Por lo tanto, se quitan de 56 KB de datos del búfer en ese segundo, con lo que se dejan 3 KB en el búfer.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-112">So, 56 Kb of data is removed from the buffer in that second, leaving 3 Kb in the buffer.</span></span> <span data-ttu-id="1ef5a-113">Si la secuencia tiene una ventana de búfer de tres segundos y, por lo tanto, un tamaño de búfer total de 168 KB, tardaría casi 40 segundos en rellenar el búfer.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-113">If the stream has a buffer window of three seconds, and thus a total buffer size of 168 Kb, it would take almost 40 seconds to fill the buffer.</span></span> <span data-ttu-id="1ef5a-114">La velocidad de bits media de la secuencia (si su duración es menor que el tiempo que se tarda en rellenar el búfer) es de 59 Kbps, aunque la velocidad de bits esté establecida en 56 kbps.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-114">The average bit rate for the stream (if its duration is less than the time it takes to fill the buffer) is 59 Kbps, even though the bit rate is set to 56 Kbps.</span></span>

<span data-ttu-id="1ef5a-115">El mismo fenómeno se aplica a las restricciones de velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-115">The same phenomenon applies to peak bit rate constraints.</span></span> <span data-ttu-id="1ef5a-116">En el caso de contenido corto, la velocidad de bits promedio calculada por el objeto de códec una vez completada la codificación puede ser mayor que la velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="1ef5a-116">For short content, the average bit rate computed by the codec object after encoding is completed can be greater than the peak bit rate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ef5a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ef5a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ef5a-118">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="1ef5a-118">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 




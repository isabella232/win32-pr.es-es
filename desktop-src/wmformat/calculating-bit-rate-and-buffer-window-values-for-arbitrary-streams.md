---
title: Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios
description: Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- flujos, velocidades de bits
- códecs, calcular velocidades de bits para flujos arbitrarios
- velocidades de bits, calcular flujos arbitrarios
- secuencias, calcular velocidades de bits para flujos arbitrarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075148"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a><span data-ttu-id="f86e3-107">Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios</span><span class="sxs-lookup"><span data-stu-id="f86e3-107">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>

<span data-ttu-id="f86e3-108">Calcular la velocidad de bits y la ventana de búfer adecuados para un tipo de flujo arbitrario no es una ciencia exacta.</span><span class="sxs-lookup"><span data-stu-id="f86e3-108">Calculating the proper bit rate and buffer window for an arbitrary stream type is not an exact science.</span></span> <span data-ttu-id="f86e3-109">Un enfoque sencillo es establecer la velocidad de bits para que coincida con el tamaño de la secuencia dividida por su longitud, en segundos.</span><span class="sxs-lookup"><span data-stu-id="f86e3-109">One simple approach is to set the bit rate to match the size of the stream divided by its length, in seconds.</span></span> <span data-ttu-id="f86e3-110">Por ejemplo, una secuencia que contiene un total de 68000 bits de hasta 20 segundos puede tener una velocidad de bits de 3400 bits por segundo (68000 bits/20 segundos = 3400 bits por segundo).</span><span class="sxs-lookup"><span data-stu-id="f86e3-110">For example, a stream containing a total of 68000 bits lasting 20 seconds might have a bit rate of 3400 bits per second (68000 bits / 20 seconds = 3400 bits per second).</span></span>

<span data-ttu-id="f86e3-111">El problema con esta sencilla técnica de asignar la velocidad de bits es que no tiene en cuenta la distribución de los datos dentro de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f86e3-111">The problem with this simple technique of assigning bit rate is that it does not take into account the distribution of data within the stream.</span></span> <span data-ttu-id="f86e3-112">Muchas secuencias arbitrarias contienen grandes cantidades de datos a intervalos a lo largo de la escala de tiempo del archivo.</span><span class="sxs-lookup"><span data-stu-id="f86e3-112">Many arbitrary streams contain larger amounts of data at intervals along the timeline of the file.</span></span> <span data-ttu-id="f86e3-113">Los flujos de imagen, por ejemplo, tienen ejemplos que son más grandes, pero normalmente se espacian varios segundos.</span><span class="sxs-lookup"><span data-stu-id="f86e3-113">Image streams, for example, have samples that are rather large, but are usually spaced several seconds apart.</span></span> <span data-ttu-id="f86e3-114">La ventana de búfer debe establecerse para asegurarse de que el búfer no se desbordará.</span><span class="sxs-lookup"><span data-stu-id="f86e3-114">The buffer window must be set to ensure that the buffer will not overflow.</span></span>

<span data-ttu-id="f86e3-115">Para comprobar la ventana de búfer, multiplique la velocidad de bits (bits por segundo) por la ventana de búfer (en segundos) y divida por 1000 para obtener el tamaño, en bits, del búfer para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f86e3-115">To check the buffer window, multiply the bit rate (bits per second) by the buffer window (in seconds) and divide by 1000 to get the size, in bits, of the buffer for the stream.</span></span> <span data-ttu-id="f86e3-116">Después, asegúrese de que el tamaño del búfer es lo suficientemente grande como para contener cualquier combinación de muestras de la secuencia que sean inferiores a la ventana del búfer en el momento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="f86e3-116">Then make sure that the buffer size is large enough to hold any combination of samples in the stream that are less than the buffer window apart in presentation time.</span></span> <span data-ttu-id="f86e3-117">En duda, establezca los dos valores un poco más alto de lo que cree que los necesita.</span><span class="sxs-lookup"><span data-stu-id="f86e3-117">When in doubt, set both values a little higher than you think you need them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f86e3-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f86e3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f86e3-119">**Almacenar contenido en búfer**</span><span class="sxs-lookup"><span data-stu-id="f86e3-119">**Buffering Content**</span></span>](buffering-content.md)
</dt> <dt>

[<span data-ttu-id="f86e3-120">**Configuración de tipos de flujo arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="f86e3-120">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 





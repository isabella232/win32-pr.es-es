---
title: Almacenar contenido en búfer
description: Almacenar contenido en búfer
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media Format SDK, contenido almacenado en búfer
- almacenar contenido en búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704569"
---
# <a name="buffering-content"></a><span data-ttu-id="2a8e2-105">Almacenar contenido en búfer</span><span class="sxs-lookup"><span data-stu-id="2a8e2-105">Buffering Content</span></span>

<span data-ttu-id="2a8e2-106">Cuando el objeto de lector abre un archivo de streaming, determina el tamaño del búfer en función de los valores del encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-106">When the reader object opens a streaming file, it determines the size of the buffer based upon settings in the header of the file.</span></span> <span data-ttu-id="2a8e2-107">Puede considerar el búfer como un depósito con un hueco en la parte inferior que se pierde a una velocidad constante.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-107">You can think of the buffer as a bucket with a hole in the bottom that leaks at a constant rate.</span></span> <span data-ttu-id="2a8e2-108">Siempre y cuando la velocidad a la que se rellene el depósito no sea mayor que la velocidad a la que se pierde, el cubo nunca se desbordará.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-108">As long as the rate at which the bucket is filled is not, on average, greater than the rate at which it is leaking, the bucket will never overflow.</span></span>

<span data-ttu-id="2a8e2-109">La velocidad a la que se pierde el depósito imaginario es la velocidad de bits de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-109">The rate at which the imaginary bucket leaks is the bit rate of the stream.</span></span> <span data-ttu-id="2a8e2-110">La velocidad a la que se llena el depósito es la velocidad de bits de streaming real.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-110">The rate at which the bucket fills is the actual streaming bit rate.</span></span> <span data-ttu-id="2a8e2-111">Los datos de un flujo comprimido varían en tamaño de muestra a muestra, en función de la cantidad de compresión que se haya logrado.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-111">The data in a compressed stream varies in size from sample to sample depending on the amount of compression that was achieved.</span></span> <span data-ttu-id="2a8e2-112">Por lo tanto, aunque la velocidad de bits de la secuencia está establecida en el perfil, representa la velocidad media de bits, no una constante.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-112">Thus, even though the bit rate of the stream is set in the profile, it represents the average bit rate, not a constant.</span></span>

<span data-ttu-id="2a8e2-113">La otra configuración de flujo importante para el proceso de almacenamiento en búfer es la ventana de búfer.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-113">The other stream setting important to the buffering process is the buffer window.</span></span> <span data-ttu-id="2a8e2-114">La ventana de búfer se mide en el tiempo y especifica la cantidad de contenido que se puede almacenar en búfer.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-114">The buffer window is measured in time and specifies how much content can be buffered.</span></span> <span data-ttu-id="2a8e2-115">La capacidad del depósito imaginario se puede encontrar mediante la ventana de búfer.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-115">The capacity of the imaginary bucket can be found using the buffer window.</span></span> <span data-ttu-id="2a8e2-116">Por ejemplo, si tiene una secuencia con una velocidad de bits de 32 Kbps y una ventana de búfer de 3 segundos, se ajusta el tamaño del búfer para que contenga 3 segundos de contenido de 32 kbps o 12.000 bytes (32.000 bits por segundo x 3 segundos/8 bits por byte).</span><span class="sxs-lookup"><span data-stu-id="2a8e2-116">For example, if you have a stream with a bit rate of 32 Kbps and a buffer window of 3 seconds, the buffer is sized to hold 3 seconds of 32 Kbps content, or 12,000 bytes (32,000 bits per second x 3 seconds / 8 bits per byte).</span></span> <span data-ttu-id="2a8e2-117">El códec limita la variación entre la velocidad de bits de streaming real de muestras codificadas, de modo que en un período de tiempo igual a la ventana de búfer, la velocidad de bits promedio no es mayor que la velocidad de bits de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-117">The codec limits the variation between the actual streaming bit rate of encoded samples so that over a period of time equal to the buffer window, the average bit rate is no greater than the bit rate of the stream.</span></span>

<span data-ttu-id="2a8e2-118">Normalmente, se establece la velocidad de bits y la ventana de búfer de una secuencia en un perfil, y el escritor controla el resto.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-118">Normally, you set the bit rate and buffer window for a stream in a profile, and the writer handles the rest.</span></span> <span data-ttu-id="2a8e2-119">Sin embargo, al pasar muestras comprimidas al lector, debe asegurarse de que los valores correctos se transfieren al nuevo archivo estableciendo la velocidad de bits y la ventana de búfer para la secuencia del perfil de destino en los valores de la secuencia comprimida.</span><span class="sxs-lookup"><span data-stu-id="2a8e2-119">When passing compressed samples to the reader, however, you must ensure that the correct values are transferred to the new file by setting the bit rate and buffer window for the stream in the destination profile to the values from the compressed stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a8e2-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a8e2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a8e2-121">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="2a8e2-121">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="2a8e2-122">**Ejemplos de medios**</span><span class="sxs-lookup"><span data-stu-id="2a8e2-122">**Media Samples**</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="2a8e2-123">**Entradas, secuencias y salidas**</span><span class="sxs-lookup"><span data-stu-id="2a8e2-123">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 





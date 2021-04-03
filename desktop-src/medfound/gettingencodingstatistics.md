---
description: Describe las estadísticas que se pueden recuperar de un códec de Windows Media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Obtener estadísticas de codificación (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808065"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a><span data-ttu-id="e390a-103">Obtener estadísticas de codificación (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="e390a-103">Getting Encoding Statistics (Microsoft Media Foundation)</span></span>

<span data-ttu-id="e390a-104">La información sobre lo que ocurre en una sesión de codificación suele estar disponible de forma inmediata en forma de códigos de error devueltos al procesar las muestras.</span><span class="sxs-lookup"><span data-stu-id="e390a-104">Information about what is happening in an encoding session is generally immediately available in the form of error codes returned when processing samples.</span></span> <span data-ttu-id="e390a-105">Sin embargo, hay algunas estadísticas que puede recuperar del códec sobre diversos aspectos de codificación.</span><span class="sxs-lookup"><span data-stu-id="e390a-105">However, there are some statistics that you can retrieve from the codec about various encoding aspects.</span></span>

## <a name="video-frame-information"></a><span data-ttu-id="e390a-106">Información del fotograma de vídeo</span><span class="sxs-lookup"><span data-stu-id="e390a-106">Video Frame Information</span></span>

<span data-ttu-id="e390a-107">Algunas estadísticas de vídeo que puede recuperar se ocupan del número de fotogramas procesados por el codificador.</span><span class="sxs-lookup"><span data-stu-id="e390a-107">Some video statistics that you can retrieve deal with the number of frames processed by the encoder.</span></span> <span data-ttu-id="e390a-108">Hay tres propiedades de número de fotogramas que se pueden leer desde el codificador de vídeo:</span><span class="sxs-lookup"><span data-stu-id="e390a-108">There are three frame number properties that you can read from the video encoder:</span></span>

-   <span data-ttu-id="e390a-109">[MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) es el número de fotogramas procesados a través del flujo de entrada de DMO.</span><span class="sxs-lookup"><span data-stu-id="e390a-109">[MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) is the number of frames processed through the input stream of the DMO.</span></span>
-   <span data-ttu-id="e390a-110">[MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) es el número de Marcos codificados.</span><span class="sxs-lookup"><span data-stu-id="e390a-110">[MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md) is the number of frames encoded.</span></span> <span data-ttu-id="e390a-111">Al restar este valor del número total de fotogramas pasados, se puede determinar el número de fotogramas que se han quitado.</span><span class="sxs-lookup"><span data-stu-id="e390a-111">By subtracting this value from the total number of frames passed, you can determine how many frames were dropped.</span></span>
-   <span data-ttu-id="e390a-112">[MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) es el número de fotogramas no codificados porque ya están incluidos en el contenido duplicado.</span><span class="sxs-lookup"><span data-stu-id="e390a-112">[MFPKEY\_ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) is the number of frames not encoded because they duplicated content already included.</span></span> <span data-ttu-id="e390a-113">Este valor no se resta del número de fotogramas codificados comunicados por DMO.</span><span class="sxs-lookup"><span data-stu-id="e390a-113">This value is not subtracted from the number of coded frames reported by the DMO.</span></span>

<span data-ttu-id="e390a-114">Puede leer las propiedades de los fotogramas de vídeo en cualquier momento durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="e390a-114">You can read video frame properties at any time during encoding.</span></span> <span data-ttu-id="e390a-115">Esto puede ser útil para determinar si la configuración de codificación es adecuada para el contenido; Si hay una diferencia importante entre los marcos totales y los marcos codificados, el contenido comprimido podría no satisfacer sus requisitos de calidad.</span><span class="sxs-lookup"><span data-stu-id="e390a-115">This can be useful in determining if the encoding settings are appropriate for your content; if there is a large difference between total frames and coded frames, the compressed content might not meet your quality requirements.</span></span> <span data-ttu-id="e390a-116">Puede leer los valores finales después de finalizar la codificación.</span><span class="sxs-lookup"><span data-stu-id="e390a-116">You can read the final values after you finish encoding.</span></span>

## <a name="vbr-buffer-statistics"></a><span data-ttu-id="e390a-117">Estadísticas de búfer de VBR</span><span class="sxs-lookup"><span data-stu-id="e390a-117">VBR Buffer Statistics</span></span>

<span data-ttu-id="e390a-118">Dependiendo del modo de codificación utilizado, algunos o todos los valores de configuración del búfer se pueden determinar durante la codificación (por ejemplo, la velocidad de bits de VBR basada en calidad no se conoce hasta que se codifica el contenido).</span><span class="sxs-lookup"><span data-stu-id="e390a-118">Depending upon the encoding mode used, some or all of the buffer settings may be determined during encoding (for example, the bit rate of quality based VBR is not known until the content is encoded).</span></span> <span data-ttu-id="e390a-119">Hay cuatro propiedades de búfer VBR que puede obtener mediante el método **IPropertyBag:: Read** :</span><span class="sxs-lookup"><span data-stu-id="e390a-119">There are four VBR buffer properties that you can get using the **IPropertyBag::Read** method:</span></span>

-   <span data-ttu-id="e390a-120">[MFPKEY \_ RAVG](mfpkey-ravgproperty.md) es la velocidad de bits promedio del contenido de VBR.</span><span class="sxs-lookup"><span data-stu-id="e390a-120">[MFPKEY\_RAVG](mfpkey-ravgproperty.md) is the average bit rate of the VBR content.</span></span>
-   <span data-ttu-id="e390a-121">[MFPKEY \_ BAVG](mfpkey-bavgproperty.md) es la ventana de búfer para la velocidad de bits media.</span><span class="sxs-lookup"><span data-stu-id="e390a-121">[MFPKEY\_BAVG](mfpkey-bavgproperty.md) is the buffer window for the average bit rate.</span></span>
-   <span data-ttu-id="e390a-122">[MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) es la velocidad de bits máxima del contenido de VBR.</span><span class="sxs-lookup"><span data-stu-id="e390a-122">[MFPKEY\_RMAX](mfpkey-rmaxproperty.md) is the peak bit rate of the VBR content.</span></span>
-   <span data-ttu-id="e390a-123">[MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) es la ventana de búfer máximo.</span><span class="sxs-lookup"><span data-stu-id="e390a-123">[MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is the peak buffer window.</span></span>

<span data-ttu-id="e390a-124">Después de comenzar a procesar ejemplos, no debe leer ninguna de las propiedades de VBR hasta que termine de codificar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e390a-124">After you begin processing samples, you should not read any of the VBR properties until you are finished encoding the stream.</span></span> <span data-ttu-id="e390a-125">Si lo hace, el codificador interpreta la solicitud como una señal de que la codificación está completa.</span><span class="sxs-lookup"><span data-stu-id="e390a-125">If you do, the encoder interprets your request as a signal that the encoding is complete.</span></span> <span data-ttu-id="e390a-126">El siguiente ejemplo que se procesa se trata como una nueva sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="e390a-126">The next sample that you process is treated as a new encoding session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e390a-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e390a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e390a-128">Códecs de Windows Media</span><span class="sxs-lookup"><span data-stu-id="e390a-128">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 




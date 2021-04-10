---
description: Proporcionar un tamaño de vídeo personalizado
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Proporcionar un tamaño de vídeo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152198"
---
# <a name="providing-a-custom-video-resizer"></a><span data-ttu-id="5dad4-103">Proporcionar un tamaño de vídeo personalizado</span><span class="sxs-lookup"><span data-stu-id="5dad4-103">Providing a Custom Video Resizer</span></span>

<span data-ttu-id="5dad4-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="5dad4-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

> [!Note]  
> <span data-ttu-id="5dad4-105">Esta característica requiere DirectX 9,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5dad4-105">This feature requires DirectX 9.0 or later.</span></span>

 

<span data-ttu-id="5dad4-106">Cuando [servicios de edición de DirectShow](directshow-editing-services.md) (des) cambia el tamaño de un clip de origen de vídeo, el comportamiento predeterminado es un *StretchBlt*, que es rápido pero no suavizado.</span><span class="sxs-lookup"><span data-stu-id="5dad4-106">When [DirectShow Editing Services](directshow-editing-services.md) (DES) resizes a video source clip, the default behavior is a *StretchBlt*, which is fast but not anti-aliased.</span></span> <span data-ttu-id="5dad4-107">Puede cambiar el comportamiento de cambio de tamaño implementando un ajuste de escala personalizado como filtro de transformación de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5dad4-107">You can change the resizing behavior by implementing a custom resizer as a DirectShow transform filter.</span></span> <span data-ttu-id="5dad4-108">El filtro debe exponer la interfaz [**IResize**](iresize.md) , que permite a des especificar el tamaño del vídeo de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="5dad4-108">The filter must expose the [**IResize**](iresize.md) interface, which enables DES to specify the input and output video size.</span></span> <span data-ttu-id="5dad4-109">Para obtener información sobre cómo escribir un filtro de transformación, vea [escribir filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5dad4-109">For information about writing a transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span> <span data-ttu-id="5dad4-110">La clase base **CTransformFilter** se recomienda como punto de partida.</span><span class="sxs-lookup"><span data-stu-id="5dad4-110">The **CTransformFilter** base class is recommended as the starting point.</span></span> <span data-ttu-id="5dad4-111">Cuando implemente el filtro, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5dad4-111">When you implement the filter, note the following:</span></span>

-   <span data-ttu-id="5dad4-112">Compatibilidad con la interfaz **IResize** en el filtro (no en los pin).</span><span class="sxs-lookup"><span data-stu-id="5dad4-112">Support the **IResize** interface on the filter (not the pins).</span></span>
-   <span data-ttu-id="5dad4-113">El filtro solo debe aceptar formatos [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (Format \_ info).</span><span class="sxs-lookup"><span data-stu-id="5dad4-113">The filter should accept only [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) formats (FORMAT\_VideoInfo).</span></span> <span data-ttu-id="5dad4-114">Rechazar otros tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="5dad4-114">Reject other format types.</span></span>
-   <span data-ttu-id="5dad4-115">El formato de vídeo de DES puede ser cualquier tipo RGB sin comprimir, incluido RGB de 32 bits con alfa (MEDIASUBTYPE \_ ARGB32).</span><span class="sxs-lookup"><span data-stu-id="5dad4-115">The video format from DES may be any uncompressed RGB type, including 32-bit RGB with alpha (MEDIASUBTYPE\_ARGB32).</span></span> <span data-ttu-id="5dad4-116">El filtro puede rechazar con seguridad los formatos con **biheight** < 0.</span><span class="sxs-lookup"><span data-stu-id="5dad4-116">Your filter can safely reject formats with **biHeight** < 0.</span></span>
-   <span data-ttu-id="5dad4-117">Antes de que el motor de representación Conecte el PIN de salida del filtro, llama a [**IResize::p \_**](iresize-put-mediatype.md) el valor de mediatype de UT para establecer el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="5dad4-117">Before the Render Engine connects the filter's output pin, it calls [**IResize::put\_MediaType**](iresize-put-mediatype.md) to set the output type.</span></span> <span data-ttu-id="5dad4-118">También puede llamar a [**IResize::p \_ tamaño de UT**](iresize-put-size.md) para ajustar el tamaño de salida.</span><span class="sxs-lookup"><span data-stu-id="5dad4-118">It may also call [**IResize::put\_Size**](iresize-put-size.md) to adjust the output size.</span></span> <span data-ttu-id="5dad4-119">Puede llamar a estos dos métodos en cualquier orden, cualquier número de veces antes de que se conecte el terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="5dad4-119">It can call these two methods in any order, any number of times, before it connects the output pin.</span></span>
-   <span data-ttu-id="5dad4-120">Una vez que el motor de representación conecta el PIN de salida, podría volver a llamar a **Put \_ size** .</span><span class="sxs-lookup"><span data-stu-id="5dad4-120">After the Render Engine connects the output pin, it might call **put\_Size** again.</span></span> <span data-ttu-id="5dad4-121">El filtro de tamaño debe volver a conectar su PIN de salida con el nuevo tamaño.</span><span class="sxs-lookup"><span data-stu-id="5dad4-121">The resizer filter should reconnect its output pin with the new size.</span></span>
-   <span data-ttu-id="5dad4-122">Dentro del método [**CTransformFilter:: transform**](ctransformfilter-transform.md) del filtro, estire el vídeo de entrada hasta el tamaño de salida.</span><span class="sxs-lookup"><span data-stu-id="5dad4-122">Inside the filter's [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, stretch the input video to the output size.</span></span>
-   <span data-ttu-id="5dad4-123">El filtro nunca debe establecer la marca de discontinuidad en el ejemplo de salida o adjuntar un tipo de medio al ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="5dad4-123">Your filter should never set the discontinuity flag on the output sample, or attach a media type to the output sample.</span></span>
-   <span data-ttu-id="5dad4-124">Para guardar el estado del filtro en un archivo GraphEdit (. GRF), implemente la interfaz **IPersistStream** .</span><span class="sxs-lookup"><span data-stu-id="5dad4-124">To save the filter's state in a GraphEdit (.grf) file, implement the **IPersistStream** interface.</span></span> <span data-ttu-id="5dad4-125">(Esto es opcional, pero útil para realizar pruebas).</span><span class="sxs-lookup"><span data-stu-id="5dad4-125">(This is optional, but useful for testing.)</span></span>

<span data-ttu-id="5dad4-126">Para usar el filtro de tamaño, el filtro se debe registrar como un objeto COM en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="5dad4-126">To use the resizer filter, the filter must be registered as a COM object on the user's system.</span></span> <span data-ttu-id="5dad4-127">Antes de que la aplicación represente el proyecto de vídeo, consulte el motor de representación de la interfaz [**IRenderEngine2**](irenderengine2.md) y llame a [**IRenderEngine2:: SETRESIZERGUID**](irenderengine2-setresizerguid.md) con el CLSID del filtro de tamaño.</span><span class="sxs-lookup"><span data-stu-id="5dad4-127">Before the application renders the video project, query the Render Engine for the [**IRenderEngine2**](irenderengine2.md) interface and call [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) with the CLSID of the resizer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dad4-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5dad4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dad4-129">Representar un proyecto</span><span class="sxs-lookup"><span data-stu-id="5dad4-129">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 




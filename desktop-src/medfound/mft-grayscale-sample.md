---
description: Muestra cómo implementar un efecto de vídeo como una transformación de Media Foundation (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: Ejemplo de MFT_Grayscale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155356"
---
# <a name="mft_grayscale-sample"></a><span data-ttu-id="a88fd-103">\_Ejemplo de escala de grises de MFT</span><span class="sxs-lookup"><span data-stu-id="a88fd-103">MFT\_Grayscale Sample</span></span>

<span data-ttu-id="a88fd-104">Muestra cómo implementar un efecto de vídeo como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="a88fd-104">Shows how to implement a video effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="a88fd-105">La MFT de escala de grises convierte vídeo YUV en escala de grises estableciendo los valores de croma del vídeo en neutro.</span><span class="sxs-lookup"><span data-stu-id="a88fd-105">The grayscale MFT converts YUV video to grayscale by setting the chroma values in the video to neutral.</span></span> <span data-ttu-id="a88fd-106">La MFT acepta vídeo sin comprimir en los formatos UYVY, YUY2 o NV12.</span><span class="sxs-lookup"><span data-stu-id="a88fd-106">The MFT accepts uncompressed video in UYVY, YUY2, or NV12 formats.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="a88fd-107">API mostradas</span><span class="sxs-lookup"><span data-stu-id="a88fd-107">APIs Demonstrated</span></span>

<span data-ttu-id="a88fd-108">Este ejemplo muestra las siguientes interfaces de Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="a88fd-108">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="a88fd-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="a88fd-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="a88fd-110">Uso</span><span class="sxs-lookup"><span data-stu-id="a88fd-110">Usage</span></span>

<span data-ttu-id="a88fd-111">El \_ ejemplo de escala de grises de MFT crea un archivo DLL que es un servidor com para la MFT.</span><span class="sxs-lookup"><span data-stu-id="a88fd-111">The MFT\_GrayScale sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="a88fd-112">Antes de usar la MFT, debe registrar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="a88fd-112">Before using the MFT, you must register the DLL.</span></span>

<span data-ttu-id="a88fd-113">Para ver la MFT en uso de escala de grises, ejecute el [ejemplo PlaybackFX](/previous-versions//bb970336(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a88fd-113">To see the grayscale MFT in use, run the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)).</span></span> <span data-ttu-id="a88fd-114">También puede usar la herramienta TopoEdit para crear una topología que incluya la MFT de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="a88fd-114">You can also use the TopoEdit tool to build a topology that includes the grayscale MFT.</span></span> <span data-ttu-id="a88fd-115">Para obtener más información sobre TopoEdit, consulte [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="a88fd-115">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a88fd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a88fd-116">Requirements</span></span>



| <span data-ttu-id="a88fd-117">Producto</span><span class="sxs-lookup"><span data-stu-id="a88fd-117">Product</span></span>                                                        | <span data-ttu-id="a88fd-118">Versión</span><span class="sxs-lookup"><span data-stu-id="a88fd-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="a88fd-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a88fd-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="a88fd-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a88fd-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="a88fd-121">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a88fd-121">Downloading the Sample</span></span>

<span data-ttu-id="a88fd-122">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span><span class="sxs-lookup"><span data-stu-id="a88fd-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a88fd-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a88fd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a88fd-124">Acerca del vídeo YUV</span><span class="sxs-lookup"><span data-stu-id="a88fd-124">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="a88fd-125">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a88fd-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="a88fd-126">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="a88fd-126">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="a88fd-127">Ejemplo de AudioDelay de MFT \_</span><span class="sxs-lookup"><span data-stu-id="a88fd-127">MFT\_AudioDelay Sample</span></span>](mft-audiodelay-sample.md)
</dt> <dt>

[<span data-ttu-id="a88fd-128">Escribir una MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="a88fd-128">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 

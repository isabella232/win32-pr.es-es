---
description: Muestra cómo escribir un descodificador para Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Ejemplo de descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000863"
---
# <a name="decoder-sample"></a><span data-ttu-id="e7680-103">Ejemplo de descodificador</span><span class="sxs-lookup"><span data-stu-id="e7680-103">Decoder Sample</span></span>

<span data-ttu-id="e7680-104">Muestra cómo escribir un descodificador para Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e7680-104">Shows how to write a decoder for Microsoft Media Foundation.</span></span>

<span data-ttu-id="e7680-105">En este ejemplo se implementa un descodificador de vídeo de MPEG-1 ficticio que muestra el código de tiempo para cada fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e7680-105">This sample implements a mock MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="e7680-106">Realmente no descodifica MPEG-1 fragmentada.</span><span class="sxs-lookup"><span data-stu-id="e7680-106">It does not actually decode the MPEG-1 bitstream.</span></span> <span data-ttu-id="e7680-107">En la imagen siguiente se muestra la salida de vídeo del descodificador.</span><span class="sxs-lookup"><span data-stu-id="e7680-107">The following image shows the video output from the decoder.</span></span>

![captura de pantalla de un fotograma de vídeo desde el descodificador](images/decodersample.png)

> [!Note]  
> <span data-ttu-id="e7680-109">Antes de la Windows SDK para Windows 7, este ejemplo se incluyó como parte del [ejemplo MPEG1Source](mpeg1source-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e7680-109">Prior to the Windows SDK for Windows 7, this sample was included as part of the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="e7680-110">API mostradas</span><span class="sxs-lookup"><span data-stu-id="e7680-110">APIs Demonstrated</span></span>

<span data-ttu-id="e7680-111">Este ejemplo muestra las siguientes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="e7680-111">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="e7680-112">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="e7680-112">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a><span data-ttu-id="e7680-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7680-113">Requirements</span></span>



| <span data-ttu-id="e7680-114">Producto</span><span class="sxs-lookup"><span data-stu-id="e7680-114">Product</span></span>                                                        | <span data-ttu-id="e7680-115">Versión</span><span class="sxs-lookup"><span data-stu-id="e7680-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="e7680-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e7680-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="e7680-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7680-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e7680-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7680-118">Downloading the Sample</span></span>

<span data-ttu-id="e7680-119">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span><span class="sxs-lookup"><span data-stu-id="e7680-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7680-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7680-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7680-121">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7680-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="e7680-122">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="e7680-122">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="e7680-123">Escribir una MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="e7680-123">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 




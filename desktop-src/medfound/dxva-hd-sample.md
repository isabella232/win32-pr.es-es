---
description: Muestra cómo usar Microsoft DirectX video Acceleration High Definition (DXVA-HD).
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: 'DXVA: ejemplo HD'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907567"
---
# <a name="dxva-hd-sample"></a><span data-ttu-id="23998-103">DXVA: ejemplo HD</span><span class="sxs-lookup"><span data-stu-id="23998-103">DXVA-HD Sample</span></span>

<span data-ttu-id="23998-104">Muestra cómo usar Microsoft DirectX video Acceleration High Definition (DXVA-HD).</span><span class="sxs-lookup"><span data-stu-id="23998-104">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>

<span data-ttu-id="23998-105">Este ejemplo es esencialmente un puerto del [ejemplo de \_ videoproc DXVA2](dxva2-videoproc-sample.md).</span><span class="sxs-lookup"><span data-stu-id="23998-105">This sample is essentially a port of the [DXVA2\_VideoProc Sample](dxva2-videoproc-sample.md).</span></span> <span data-ttu-id="23998-106">Tiene las mismas funciones básicas y la mayoría de los comandos del teclado son los mismos.</span><span class="sxs-lookup"><span data-stu-id="23998-106">It has the same basic functions, and most of the keyboard commands are the same.</span></span>

<span data-ttu-id="23998-107">El ejemplo genera mediante programación el vídeo con una secuencia principal y un subflujo.</span><span class="sxs-lookup"><span data-stu-id="23998-107">The sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="23998-108">El flujo principal muestra las barras de color SMPTE.</span><span class="sxs-lookup"><span data-stu-id="23998-108">The primary stream displays SMPTE color bars.</span></span> <span data-ttu-id="23998-109">La subsecuencia se combina alfa en el flujo principal mediante la creación de claves de luminancia.</span><span class="sxs-lookup"><span data-stu-id="23998-109">The substream is alpha-blended onto the primary stream using luma keying.</span></span> <span data-ttu-id="23998-110">El usuario puede cambiar los parámetros de procesamiento de vídeo, incluidos el valor alfa plano, los rectángulos de origen y de destino, los ajustes de color y el espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="23998-110">The user can change the video processing parameters, including the planar alpha value, source and destination rectangles, color adjustments, and color space.</span></span> <span data-ttu-id="23998-111">En la imagen siguiente se muestra el vídeo que se genera.</span><span class="sxs-lookup"><span data-stu-id="23998-111">The following image shows that video that is generated.</span></span>

![captura de pantalla del ejemplo DXVA-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="23998-113">API mostradas</span><span class="sxs-lookup"><span data-stu-id="23998-113">APIs Demonstrated</span></span>

<span data-ttu-id="23998-114">Este ejemplo muestra las siguientes interfaces de DXVA-HD:</span><span class="sxs-lookup"><span data-stu-id="23998-114">This sample demonstrates the following DXVA-HD interfaces:</span></span>

-   [<span data-ttu-id="23998-115">**\_Dispositivo IDXVAHD**</span><span class="sxs-lookup"><span data-stu-id="23998-115">**IDXVAHD\_Device**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [<span data-ttu-id="23998-116">**IDXVAHD de \_ videoprocesador**</span><span class="sxs-lookup"><span data-stu-id="23998-116">**IDXVAHD\_VideoProcessor**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a><span data-ttu-id="23998-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23998-117">Requirements</span></span>



| <span data-ttu-id="23998-118">Producto</span><span class="sxs-lookup"><span data-stu-id="23998-118">Product</span></span>                                                        | <span data-ttu-id="23998-119">Versión</span><span class="sxs-lookup"><span data-stu-id="23998-119">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="23998-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="23998-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="23998-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="23998-121">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="23998-122">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="23998-122">Downloading the Sample</span></span>

<span data-ttu-id="23998-123">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span><span class="sxs-lookup"><span data-stu-id="23998-123">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23998-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23998-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23998-125">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="23998-125">DXVA-HD</span></span>](dxva-hd.md)
</dt> <dt>

[<span data-ttu-id="23998-126">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23998-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




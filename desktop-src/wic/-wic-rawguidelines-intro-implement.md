---
description: Directrices generales para implementar códecs sin formato
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Directrices generales para implementar códecs sin formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278180"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a><span data-ttu-id="06f05-103">Directrices generales para implementar códecs sin formato</span><span class="sxs-lookup"><span data-stu-id="06f05-103">General Guidelines for Implementing RAW Codecs</span></span>

<span data-ttu-id="06f05-104">En comparación con los tipos de imagen no sin procesar, como JPEG o TIFF, hay dos diferencias importantes en el modo en que se espera que los formatos de imagen sin procesar se comporten en Windows:</span><span class="sxs-lookup"><span data-stu-id="06f05-104">Compared to non-RAW image types such as JPEG or TIFF, there are two notable differences in how RAW image formats are expected to behave in Windows:</span></span>

-   <span data-ttu-id="06f05-105">La mayoría de los formatos de imagen sin procesar se supone que son de "solo lectura" y, probablemente, no admiten la codificación de píxeles en formato sin procesar.</span><span class="sxs-lookup"><span data-stu-id="06f05-105">Most RAW image formats are presumed to be "read only" and probably will not support pixel encoding to RAW format.</span></span> <span data-ttu-id="06f05-106">Sin embargo, dado que Windows Imaging Component (WIC) requiere un codificador para admitir la reescritura de metadatos, los autores de códecs sin formato deben planear la implementación de al menos una clase de codificador esqueleto.</span><span class="sxs-lookup"><span data-stu-id="06f05-106">However, because Windows Imaging Component (WIC) requires an encoder to support metadata write-back, RAW codec authors should plan to implement at least a skeleton encoder class.</span></span>
-   <span data-ttu-id="06f05-107">La descodificación de una imagen sin formato de tamaño completo puede tardar mucho tiempo en comparación con otros formatos.</span><span class="sxs-lookup"><span data-stu-id="06f05-107">Decoding a full-size RAW image can take a long time compared to other formats.</span></span> <span data-ttu-id="06f05-108">Por esta razón, Microsoft recomienda que se tomen ciertos enfoques para minimizar la latencia de descodificación y garantizar la compatibilidad con escenarios como la representación rápida de miniaturas y vistas previas.</span><span class="sxs-lookup"><span data-stu-id="06f05-108">For this reason, Microsoft recommends that certain approaches be taken to minimize decoding latency and to ensure support for scenarios such as rapid rendering of thumbnails and previews.</span></span>

    <span data-ttu-id="06f05-109">Por ejemplo, todos los autores de códecs sin formato deben implementar la interfaz [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , que proporciona un mecanismo para notificar al descodificador de antemano el tamaño del mapa de bits de destino, lo que permite la descodificación optimizada en un tamaño de imagen de salida más pequeño.</span><span class="sxs-lookup"><span data-stu-id="06f05-109">For example, all RAW codec authors must implement the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface, which provides a mechanism to notify the decoder in advance of the target bitmap size, thus enabling optimized decoding to a smaller output image size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06f05-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06f05-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="06f05-111">**Vista**</span><span class="sxs-lookup"><span data-stu-id="06f05-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="06f05-112">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="06f05-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="06f05-113">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="06f05-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="06f05-114">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="06f05-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




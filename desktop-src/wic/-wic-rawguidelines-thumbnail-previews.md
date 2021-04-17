---
description: Miniaturas y vistas previas
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniaturas y vistas previas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659940"
---
# <a name="thumbnails-and-previews"></a><span data-ttu-id="db700-103">Miniaturas y vistas previas</span><span class="sxs-lookup"><span data-stu-id="db700-103">Thumbnails and Previews</span></span>

<span data-ttu-id="db700-104">Windows Vista y la Galería fotográfica de Windows se basan en Windows Imaging Component (WIC) para representar miniaturas rápidas y vistas previas de las imágenes.</span><span class="sxs-lookup"><span data-stu-id="db700-104">Windows Vista and the Windows Photo Gallery rely on Windows Imaging Component (WIC) to render fast thumbnails and previews of images.</span></span> <span data-ttu-id="db700-105">Para admitir la representación rápida en miniatura y vista previa, los códecs sin formato deben implementar las interfaces WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) y [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="db700-105">To support fast thumbnail and preview rendering, RAW codecs must implement the WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) and [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) interfaces.</span></span> <span data-ttu-id="db700-106">Para admitir una experiencia de usuario con capacidad de respuesta, es muy conveniente que estas interfaces devuelvan un valor de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) al llamador en 200 milisegundos o menos.</span><span class="sxs-lookup"><span data-stu-id="db700-106">To support a responsive user experience, it is highly desirable that these interfaces return an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to the caller in 200 milliseconds or less.</span></span>

<span data-ttu-id="db700-107">Microsoft recomienda encarecidamente que los propietarios de formato de archivo sin formato generen una vista previa preprocesada y la almacenen en la memoria caché en el archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="db700-107">Microsoft strongly recommends that RAW file format owners generate a prerendered preview and cache this in the image file.</span></span> <span data-ttu-id="db700-108">En el caso de un formato en el dispositivo, esto suele realizarse en el momento de la captura.</span><span class="sxs-lookup"><span data-stu-id="db700-108">For an in-device format, this is usually done at capture time.</span></span> <span data-ttu-id="db700-109">Sin embargo, las vistas previas también se pueden volver a generar y almacenar en el archivo de imagen cada vez que se modifican las propiedades de la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , si no se tarda demasiado en realizarse.</span><span class="sxs-lookup"><span data-stu-id="db700-109">However, previews could also be regenerated and stored in the image file whenever [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface properties are changed-if it does not take too much work to do so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db700-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db700-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="db700-111">**Vista**</span><span class="sxs-lookup"><span data-stu-id="db700-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="db700-112">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="db700-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="db700-113">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="db700-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="db700-114">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="db700-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




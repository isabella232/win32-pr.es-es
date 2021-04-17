---
description: Requisitos de códecs sin formato para Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Requisitos de códecs sin formato para Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687870"
---
# <a name="raw-codec-requirements-for-windows-7"></a><span data-ttu-id="775c2-103">Requisitos de códecs sin formato para Windows 7</span><span class="sxs-lookup"><span data-stu-id="775c2-103">RAW Codec Requirements for Windows 7</span></span>

<span data-ttu-id="775c2-104">Como mínimo, se necesitan las siguientes características de códec:</span><span class="sxs-lookup"><span data-stu-id="775c2-104">The following codec features are required at a minimum:</span></span>

<span data-ttu-id="775c2-105">Toda la funcionalidad necesaria para la compatibilidad con la Galería fotográfica y el shell de Windows Vista: miniatura, vista previa y rotación (persistente).</span><span class="sxs-lookup"><span data-stu-id="775c2-105">All functionality that is required for Windows Vista shell and Photo Gallery support: thumbnail, preview, and (persisted) rotation.</span></span> <span data-ttu-id="775c2-106">El procesamiento sin procesar debe tener como valor predeterminado la configuración de as-Shot.</span><span class="sxs-lookup"><span data-stu-id="775c2-106">RAW processing should default to appropriate as-shot settings.</span></span>

<span data-ttu-id="775c2-107">La compatibilidad con los metadatos principales (tanto de lectura como de escritura), los metadatos no EXIFs, así como los metadatos EXIF, deben conservarse dentro de formatos de archivo sin formato sin usar archivos sidecar.</span><span class="sxs-lookup"><span data-stu-id="775c2-107">Support for core metadata (both read and write), Non-EXIF metadata, as well as EXIF metadata, should be persisted inside RAW file formats without use of sidecar files.</span></span>

<span data-ttu-id="775c2-108">Compatibilidad con la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="775c2-108">Support for the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="775c2-109">En Windows 7, el componente WIC de Windows Imaging (WIC) requiere que se implementen todas las interfaces de parámetro que expone [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="775c2-109">For Windows 7, Windows Imaging Component (WIC)WIC requires that all parameter interfaces exposed by [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) be implemented.</span></span>

<span data-ttu-id="775c2-110">Compatibilidad con el estado de orientación:</span><span class="sxs-lookup"><span data-stu-id="775c2-110">Orientation state support:</span></span>

-   <span data-ttu-id="775c2-111">90 el uso del método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) se debe aplicar a rotaciones de imagen de paso de grado.</span><span class="sxs-lookup"><span data-stu-id="775c2-111">90 degree-step Image rotations should be applied by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) method.</span></span> <span data-ttu-id="775c2-112">Las aplicaciones y Windows usan este método para girar las imágenes (y las vistas en miniatura y las vistas previas almacenadas en caché).</span><span class="sxs-lookup"><span data-stu-id="775c2-112">Applications and Windows use this method to rotate the images (and cached thumbnails and previews).</span></span>
-   <span data-ttu-id="775c2-113">El códec también debe conservar la aplicación de giro mediante esta API (consulte más adelante en este documento).</span><span class="sxs-lookup"><span data-stu-id="775c2-113">Application of rotation by using this API should also be persisted by the codec (see earlier in this paper).</span></span>
-   <span data-ttu-id="775c2-114">Las aplicaciones pueden usar las capacidades de rotación de la API de [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , pero el códec no serializará ninguna configuración de rotación en esta API, por lo que no se conservarán las rotaciones realizadas con [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .</span><span class="sxs-lookup"><span data-stu-id="775c2-114">Applications can use the rotation capabilities of the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) API, but the codec will not serialize any rotation settings on this API, so rotations done using [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) will not be persisted.</span></span>

<span data-ttu-id="775c2-115">Compatibilidad con la extracción en miniatura y vista previa de alta velocidad.</span><span class="sxs-lookup"><span data-stu-id="775c2-115">High-speed thumbnail and preview extraction support.</span></span> <span data-ttu-id="775c2-116">Si la dimensión de la vista previa de píxeles máxima (ancho o alto) es inferior a 1024 píxeles de tamaño, Windows Vista solicitará un procesamiento para la vista previa de la pantalla:</span><span class="sxs-lookup"><span data-stu-id="775c2-116">If the preview maximum pixel dimension (width or height) is less than 1024 pixels in size, Windows Vista will request a render for screen preview:</span></span>

-   <span data-ttu-id="775c2-117">El método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) debe admitir al menos los modos [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) y [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) para permitir una representación más rápida de miniaturas y vistas previas que el modo de calidad completa.</span><span class="sxs-lookup"><span data-stu-id="775c2-117">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) method should support at least the [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) and [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) modes to allow faster rendering of thumbnails and previews than the full-quality mode.</span></span>
-   <span data-ttu-id="775c2-118">Windows llamará a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con el tamaño de resolución de pantalla solicitado.</span><span class="sxs-lookup"><span data-stu-id="775c2-118">Windows will call [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the requested screen resolution size.</span></span>
-   <span data-ttu-id="775c2-119">Los tamaños de la resolución de pantalla deben ser compatibles con la API anterior.</span><span class="sxs-lookup"><span data-stu-id="775c2-119">Screen resolution sizes must be supported in the above API.</span></span>
-   <span data-ttu-id="775c2-120">Se requiere un procesamiento de imagen coherente de los bits de miniaturas, vista previa y imagen completa de [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) .</span><span class="sxs-lookup"><span data-stu-id="775c2-120">Consistent image processing of thumbnail, preview, and full-image bits from [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) is required.</span></span>

<span data-ttu-id="775c2-121">Formatos de píxeles de intervalo dinámico alto (HDR).</span><span class="sxs-lookup"><span data-stu-id="775c2-121">High dynamic range (HDR) pixel formats.</span></span>

<span data-ttu-id="775c2-122">Impresión de XML Paper Specification (XPS).</span><span class="sxs-lookup"><span data-stu-id="775c2-122">XML Paper Specification (XPS) printing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="775c2-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="775c2-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="775c2-124">**Vista**</span><span class="sxs-lookup"><span data-stu-id="775c2-124">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="775c2-125">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="775c2-125">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="775c2-126">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="775c2-126">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="775c2-127">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="775c2-127">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




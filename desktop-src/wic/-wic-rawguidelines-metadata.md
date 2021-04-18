---
description: Compatibilidad con metadatos
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Compatibilidad con metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706831"
---
# <a name="metadata-support"></a><span data-ttu-id="8d328-103">Compatibilidad con metadatos</span><span class="sxs-lookup"><span data-stu-id="8d328-103">Metadata Support</span></span>

<span data-ttu-id="8d328-104">Los formatos sin formato también deben admitir los escenarios comunes de lectura y escritura de metadatos para las imágenes de Windows.</span><span class="sxs-lookup"><span data-stu-id="8d328-104">RAW formats should also support the common metadata read and write scenarios for images in Windows.</span></span> <span data-ttu-id="8d328-105">Microsoft ha desarrollado un conjunto de proveedores de metadatos nativos para el archivo de imagen intercambiable (EXIF), el Consejo Internacional de telecomunicaciones (IPTC) y los metadatos de la plataforma de metadatos extensible (XMP) que actualmente se invocan solo para contenedores TIFF y JPEG.</span><span class="sxs-lookup"><span data-stu-id="8d328-105">Microsoft has developed a set of native metadata providers for exchangeable image file (EXIF), International Press Telecommunications Council (IPTC), and Extensible Metadata Platform (XMP) metadata that are currently invoked only for TIFF and JPEG containers.</span></span> <span data-ttu-id="8d328-106">Si la imagen sin procesar se almacena en uno de estos formatos de contenedor, se recomienda usar los proveedores de metadatos integrados de Windows.</span><span class="sxs-lookup"><span data-stu-id="8d328-106">If the RAW image is stored in one of these container formats, it is recommended to use the Windows built-in metadata providers.</span></span> <span data-ttu-id="8d328-107">Sin embargo, el autor del códec es responsable de configurarlo correctamente.</span><span class="sxs-lookup"><span data-stu-id="8d328-107">However, the codec author is responsible for configuring this properly.</span></span> <span data-ttu-id="8d328-108">En el caso de los archivos sin formato que no se basan en un contenedor TIFF, podría ser necesario implementar escritores EXIF, IPTC o XMP porque los lectores y escritores integrados esperan que los datos se ajusten a las especificaciones de diseño en disco de EXIF, IPTC y XMP.</span><span class="sxs-lookup"><span data-stu-id="8d328-108">For RAW files that are not based on a TIFF container, it might be necessary to implement EXIF, IPTC, or XMP writers because the built-in readers and writers expect the data to conform to EXIF, IPTC, and XMP on-disk layout specifications.</span></span> <span data-ttu-id="8d328-109">Los creadores de códecs también pueden implementar sus propios proveedores para los metadatos personalizados.</span><span class="sxs-lookup"><span data-stu-id="8d328-109">Codec authors can also implement their own providers for any custom metadata.</span></span>

<span data-ttu-id="8d328-110">Debido a la arquitectura de Windows Imaging Component (WIC), los escritores de metadatos solo se pueden invocar a través de una instancia de un codificador de imágenes.</span><span class="sxs-lookup"><span data-stu-id="8d328-110">Because of the architecture of Windows Imaging Component (WIC), metadata writers can be invoked only through an instance of an image encoder.</span></span> <span data-ttu-id="8d328-111">Por lo tanto, los propietarios de formato sin formato deben crear al menos un codificador de "stub" [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) , incluso si no se implementa la codificación real de píxeles en formato sin procesar.</span><span class="sxs-lookup"><span data-stu-id="8d328-111">Therefore, RAW format owners should create at least a "stub" [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) encoder, even if the actual encoding of pixels into a RAW format is not implemented.</span></span> <span data-ttu-id="8d328-112">El autor del códec debe invocar los controladores de metadatos adecuados:</span><span class="sxs-lookup"><span data-stu-id="8d328-112">The codec author must invoke the proper metadata handlers:</span></span>

-   <span data-ttu-id="8d328-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) tanto en el descodificador como en el descodificador de fotogramas según corresponda.</span><span class="sxs-lookup"><span data-stu-id="8d328-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on both the decoder and frame decoder as appropriate.</span></span>
-   <span data-ttu-id="8d328-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) en el codificador y el codificador de tramas según corresponda.</span><span class="sxs-lookup"><span data-stu-id="8d328-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on both the encoder and frame encoder as appropriate.</span></span>

<span data-ttu-id="8d328-115">Para admitir todos los escenarios previstos en aplicaciones de creación de imágenes en Windows Vista, se recomienda que los proveedores de códecs admitan lo siguiente como mínimo:</span><span class="sxs-lookup"><span data-stu-id="8d328-115">To support all of the anticipated scenarios in imaging applications in Windows Vista, it is recommended that codec vendors support the following at a minimum:</span></span>

-   <span data-ttu-id="8d328-116">Lectura EXIF</span><span class="sxs-lookup"><span data-stu-id="8d328-116">EXIF read</span></span>
-   <span data-ttu-id="8d328-117">Escritura EXIF parcial (para permitir que las actualizaciones capturen la fecha y la hora)</span><span class="sxs-lookup"><span data-stu-id="8d328-117">Partial EXIF write (to permit updates to capture date and time)</span></span>
-   <span data-ttu-id="8d328-118">XMP Read y Write (incluido opcionalmente IPTC Core para XMP)</span><span class="sxs-lookup"><span data-stu-id="8d328-118">XMP read and write (including optionally IPTC Core for XMP)</span></span>
-   <span data-ttu-id="8d328-119">IIMv4 de lectura y escritura de IPTC</span><span class="sxs-lookup"><span data-stu-id="8d328-119">IPTC IIMv4 read and write</span></span>

<span data-ttu-id="8d328-120">La mayor parte del acceso a los metadatos (lectura y escritura) en Windows Vista se produce a través de la interfaz [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) o [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="8d328-120">Most of the metadata access (both read and write) in Windows Vista occurs through the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) or [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interface.</span></span> <span data-ttu-id="8d328-121">Por lo tanto, para participar en las experiencias de metadatos de Windows Vista, los autores de códecs sin formato deben implementar los métodos [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) y [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="8d328-121">Therefore, to participate in the Windows Vista metadata experiences, RAW codec authors must implement the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d328-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d328-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8d328-123">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8d328-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8d328-124">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="8d328-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="8d328-125">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="8d328-125">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="8d328-126">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8d328-126">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




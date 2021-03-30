---
description: En esta sección de temas se proporciona a los desarrolladores instrucciones sobre cómo implementar códecs de formato de archivo de imagen que funcionarán dentro del marco de trabajo de Windows Imaging Component (WIC).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Cómo escribir un códec de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910169"
---
# <a name="how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="c57f1-103">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c57f1-103">How to Write a WIC-Enabled Codec</span></span>

<span data-ttu-id="c57f1-104">En esta sección de temas se proporciona a los desarrolladores instrucciones sobre cómo implementar códecs de formato de archivo de imagen que funcionarán dentro del marco de trabajo de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="c57f1-104">This section of topics provide developers with guidance on how to implement image file format codecs that will function within the Windows Imaging Component (WIC) framework.</span></span>

<dl>

[<span data-ttu-id="c57f1-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="c57f1-105">Introduction</span></span>](-wic-howtowriteacodec-intro.md)  
[<span data-ttu-id="c57f1-106">Cómo funciona el componente de creación de imágenes de Windows (WIC)</span><span class="sxs-lookup"><span data-stu-id="c57f1-106">How The Windows Imaging Component (WIC) Works</span></span>](-wic-howwicworks.md)  
<dl>

[<span data-ttu-id="c57f1-107">Detección y arbitraje</span><span class="sxs-lookup"><span data-stu-id="c57f1-107">Discovery and Arbitration</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="c57f1-108">Descodificación</span><span class="sxs-lookup"><span data-stu-id="c57f1-108">Decoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="c57f1-109">Encoding</span><span class="sxs-lookup"><span data-stu-id="c57f1-109">Encoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="c57f1-110">La duración de un códec</span><span class="sxs-lookup"><span data-stu-id="c57f1-110">The Lifetime of a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="c57f1-111">Cómo habilitar WIC</span><span class="sxs-lookup"><span data-stu-id="c57f1-111">How to WIC-enable a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="c57f1-112">Compatibilidad con apartamento multiproceso en WIC</span><span class="sxs-lookup"><span data-stu-id="c57f1-112">Multi-Threaded Apartment Support in WIC</span></span>](-wic-howwicworks.md)  
<span data-ttu-id="c57f1-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementar un descodificador de WIC-Enabled</a></span><span class="sxs-lookup"><span data-stu-id="c57f1-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementing a WIC-Enabled Decoder</a></span></span><dl>

[<span data-ttu-id="c57f1-114">Interfaces del descodificador</span><span class="sxs-lookup"><span data-stu-id="c57f1-114">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)<dl>

[<span data-ttu-id="c57f1-115">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="c57f1-115">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)  
[<span data-ttu-id="c57f1-116">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="c57f1-116">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[<span data-ttu-id="c57f1-117">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="c57f1-117">IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)  
[<span data-ttu-id="c57f1-118">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="c57f1-118">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)  
[<span data-ttu-id="c57f1-119">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="c57f1-119">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)  
[<span data-ttu-id="c57f1-120">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="c57f1-120">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)  
[<span data-ttu-id="c57f1-121">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="c57f1-121">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)  
<span data-ttu-id="c57f1-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementación de un codificador WIC-Enabled</a>  
</span><span class="sxs-lookup"><span data-stu-id="c57f1-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementing a WIC-Enabled Encoder</a>  
</span></span><dl>

[<span data-ttu-id="c57f1-123">Interfaces del codificador</span><span class="sxs-lookup"><span data-stu-id="c57f1-123">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)  
<dl>

[<span data-ttu-id="c57f1-124">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="c57f1-124">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)  
[<span data-ttu-id="c57f1-125">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="c57f1-125">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[<span data-ttu-id="c57f1-126">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="c57f1-126">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)  
[<span data-ttu-id="c57f1-127">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="c57f1-127">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)  
<span data-ttu-id="c57f1-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Instalación y registro de códecs</a>  
</span><span class="sxs-lookup"><span data-stu-id="c57f1-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Codec Installation and Registration</a>  
</span></span><dl>

[<span data-ttu-id="c57f1-129">Registro de un códec</span><span class="sxs-lookup"><span data-stu-id="c57f1-129">Registering a Codec</span></span>](-wic-codecinstallandreg.md)  
<dl>

[<span data-ttu-id="c57f1-130">Entradas generales de registro</span><span class="sxs-lookup"><span data-stu-id="c57f1-130">General Register Entries</span></span>](-wic-generalregentries.md)  
[<span data-ttu-id="c57f1-131">Entradas del registro específicas del codificador</span><span class="sxs-lookup"><span data-stu-id="c57f1-131">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)  
<dl>

[<span data-ttu-id="c57f1-132">Registrar un formato de contenedor con escritores de metadatos</span><span class="sxs-lookup"><span data-stu-id="c57f1-132">Registering a Container Format with Metadata Writers</span></span>](-wic-encoderregentries.md)  
<span data-ttu-id="c57f1-133"></dl> </dd> <a href="-wic-decoderregentries.md">Entradas del registro específicas del codificador</a>  
</span><span class="sxs-lookup"><span data-stu-id="c57f1-133"></dl> </dd> <a href="-wic-decoderregentries.md">Encoder-Specific Registry Entries</a>  
</span></span><dl>

[<span data-ttu-id="c57f1-134">Registrar un nuevo formato de contenedor con lectores de metadatos</span><span class="sxs-lookup"><span data-stu-id="c57f1-134">Registering a New Container Format with Metadata Readers</span></span>](-wic-decoderregentries.md)  
<span data-ttu-id="c57f1-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integración con Fotogalería y explorador de Windows Vista</a>  
</span><span class="sxs-lookup"><span data-stu-id="c57f1-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integration with Windows Vista PhotoGallery and Explorer</a>  
</span></span><dl>

[<span data-ttu-id="c57f1-136">Almacén de propiedades de Windows</span><span class="sxs-lookup"><span data-stu-id="c57f1-136">Windows Property Store</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="c57f1-137">Galería fotográfica de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c57f1-137">Windows Vista Photo Gallery</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="c57f1-138">Caché en miniatura de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c57f1-138">Windows Vista Thumbnail Cache</span></span>](-wic-integrationregentries.md)  
<span data-ttu-id="c57f1-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Actualización de la caché en miniatura al instalar un códec</a> [que pone el códec de WIC-Enabled a disposición de los usuarios](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md"></a>  
</span><span class="sxs-lookup"><span data-stu-id="c57f1-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Updating the Thumbnail Cache when Installing a Codec</a> [Making Your WIC-Enabled Codec Available to Users](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">Conclusion</a>  
</span></span></dl>

## <a name="related-topics"></a><span data-ttu-id="c57f1-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c57f1-140">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c57f1-141">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c57f1-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c57f1-142">Introducción (cómo escribir un códec WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="c57f1-142">Introduction (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[<span data-ttu-id="c57f1-143">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="c57f1-143">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




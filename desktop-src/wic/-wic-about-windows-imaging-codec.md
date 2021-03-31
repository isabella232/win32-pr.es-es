---
description: El componente de creación de imágenes de Windows (WIC) proporciona un marco extensible para trabajar con imágenes y metadatos de imágenes.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Información general sobre componentes de Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277202"
---
# <a name="windows-imaging-component-overview"></a><span data-ttu-id="06e0d-103">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="06e0d-103">Windows Imaging Component Overview</span></span>

<span data-ttu-id="06e0d-104">El componente de creación de imágenes de Windows (WIC) proporciona un marco extensible para trabajar con imágenes y metadatos de imágenes.</span><span class="sxs-lookup"><span data-stu-id="06e0d-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="06e0d-105">WIC permite a los fabricantes de software independientes (ISV) y a los fabricantes de hardware independientes (IHV) desarrollar sus propios códecs de imagen y obtener la misma compatibilidad con la plataforma que los formatos de imagen estándar (por ejemplo, TIFF, JPEG, PNG, GIF, BMP y HDPhoto).</span><span class="sxs-lookup"><span data-stu-id="06e0d-105">WIC makes it possible for independent software vendors (ISVs) and independent hardware vendors (IHVs) to develop their own image codecs and get the same platform support as standard image formats (for example, TIFF, JPEG, PNG, GIF, BMP, and HDPhoto).</span></span> <span data-ttu-id="06e0d-106">Se usa un único conjunto coherente de interfaces para todo el procesamiento de imágenes, independientemente del formato de la imagen, por lo que cualquier aplicación que use WIC obtiene la compatibilidad automática con los nuevos formatos de imagen en cuanto se instala el códec.</span><span class="sxs-lookup"><span data-stu-id="06e0d-106">A single, consistent set of interfaces is used for all image processing, regardless of image format, so any application using the WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="06e0d-107">El marco de metadatos extensible permite que las aplicaciones lean y escriban sus propios metadatos de propiedad directamente en archivos de imagen, por lo que los metadatos nunca se pierden ni se separan de la imagen.</span><span class="sxs-lookup"><span data-stu-id="06e0d-107">The extensible metadata framework makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata never gets lost or separated from the image.</span></span>

<span data-ttu-id="06e0d-108">En este tema se incluyen las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="06e0d-108">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="06e0d-109">Características de componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="06e0d-109">Windows Imaging Component Features</span></span>](#windows-imaging-component-features)
-   [<span data-ttu-id="06e0d-110">Códecs nativos</span><span class="sxs-lookup"><span data-stu-id="06e0d-110">Native Codecs</span></span>](#native-codecs)
-   [<span data-ttu-id="06e0d-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06e0d-111">Related topics</span></span>](#related-topics)

## <a name="windows-imaging-component-features"></a><span data-ttu-id="06e0d-112">Características de componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="06e0d-112">Windows Imaging Component Features</span></span>

<span data-ttu-id="06e0d-113">Las características principales de WIC son:</span><span class="sxs-lookup"><span data-stu-id="06e0d-113">The primary features of WIC are:</span></span>

-   <span data-ttu-id="06e0d-114">Permite a los desarrolladores de aplicaciones realizar operaciones de procesamiento de imágenes en cualquier formato de imagen a través de un único conjunto coherente de interfaces comunes, sin necesidad de tener conocimientos previos de formatos de imagen concretos.</span><span class="sxs-lookup"><span data-stu-id="06e0d-114">Enables application developers to perform image processing operations on any image format through a single, consistent set of common interfaces, without requiring prior knowledge of specific image formats.</span></span>
-   <span data-ttu-id="06e0d-115">Proporciona una arquitectura extensible "plug and Play" para códecs de imagen, formatos de píxeles y metadatos, con detección automática en tiempo de ejecución de nuevos formatos.</span><span class="sxs-lookup"><span data-stu-id="06e0d-115">Provides an extensible "plug and play" architecture for image codecs, pixel formats, and metadata, with automatic run-time discovery of new formats.</span></span>
-   <span data-ttu-id="06e0d-116">Admite la lectura y escritura de metadatos arbitrarios en archivos de imagen, con la capacidad de conservar metadatos no reconocidos durante la edición.</span><span class="sxs-lookup"><span data-stu-id="06e0d-116">Supports reading and writing of arbitrary metadata in image files, with the ability to preserve unrecognized metadata during editing.</span></span>
-   <span data-ttu-id="06e0d-117">Conserva los datos de imagen de profundidad de bits alta, hasta 32 bits por canal, a lo largo de la canalización de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="06e0d-117">Preserves high bit depth image data, up to 32 bits per channel, throughout the image processing pipeline.</span></span>
-   <span data-ttu-id="06e0d-118">Proporciona compatibilidad integrada para los formatos de imagen más conocidos, formatos de píxel y esquemas de metadatos.</span><span class="sxs-lookup"><span data-stu-id="06e0d-118">Provides built-in support for most popular image formats, pixel formats, and metadata schemas.</span></span>

## <a name="native-codecs"></a><span data-ttu-id="06e0d-119">Códecs nativos</span><span class="sxs-lookup"><span data-stu-id="06e0d-119">Native Codecs</span></span>

<span data-ttu-id="06e0d-120">WIC incluye varios códecs integrados.</span><span class="sxs-lookup"><span data-stu-id="06e0d-120">WIC includes several built-in codecs.</span></span> <span data-ttu-id="06e0d-121">Los siguientes códecs estándar se proporcionan con la plataforma.</span><span class="sxs-lookup"><span data-stu-id="06e0d-121">The following standard codecs are provided with the platform.</span></span> 

| <span data-ttu-id="06e0d-122">Códec</span><span class="sxs-lookup"><span data-stu-id="06e0d-122">Codec</span></span>                                                                                             | <span data-ttu-id="06e0d-123">Tipos MIME</span><span class="sxs-lookup"><span data-stu-id="06e0d-123">Mime Types</span></span>                       | <span data-ttu-id="06e0d-124">Descodificadores</span><span class="sxs-lookup"><span data-stu-id="06e0d-124">Decoders</span></span> | <span data-ttu-id="06e0d-125">Codificadores</span><span class="sxs-lookup"><span data-stu-id="06e0d-125">Encoders</span></span> |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| <span data-ttu-id="06e0d-126">BMP (formato de mapa de bits de Windows), especificación de BMP V5.</span><span class="sxs-lookup"><span data-stu-id="06e0d-126">BMP (Windows Bitmap Format), BMP Specification v5.</span></span>                                                | <span data-ttu-id="06e0d-127">image/bmp</span><span class="sxs-lookup"><span data-stu-id="06e0d-127">image/bmp</span></span>                        | <span data-ttu-id="06e0d-128">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-128">Yes</span></span>      | <span data-ttu-id="06e0d-129">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-129">Yes</span></span>      |
| <span data-ttu-id="06e0d-130">GIF (formato de intercambio de gráficos 89A), especificación GIF 89A/89m</span><span class="sxs-lookup"><span data-stu-id="06e0d-130">GIF (Graphics Interchange Format 89a), GIF Specification 89a/89m</span></span>                                  | <span data-ttu-id="06e0d-131">image/gif</span><span class="sxs-lookup"><span data-stu-id="06e0d-131">image/gif</span></span>                        | <span data-ttu-id="06e0d-132">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-132">Yes</span></span>      | <span data-ttu-id="06e0d-133">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-133">Yes</span></span>      |
| <span data-ttu-id="06e0d-134">ICO (formato de icono)</span><span class="sxs-lookup"><span data-stu-id="06e0d-134">ICO (Icon Format)</span></span>                                                                                 | <span data-ttu-id="06e0d-135">imagen/ICO</span><span class="sxs-lookup"><span data-stu-id="06e0d-135">image/ico</span></span>                        | <span data-ttu-id="06e0d-136">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-136">Yes</span></span>      | <span data-ttu-id="06e0d-137">No</span><span class="sxs-lookup"><span data-stu-id="06e0d-137">No</span></span>       |
| <span data-ttu-id="06e0d-138">JPEG (grupo de expertos fotográficos Unidos), especificación JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="06e0d-138">JPEG (Joint Photographic Experts Group), JFIF Specification 1.02</span></span>                                  | <span data-ttu-id="06e0d-139">image/JPEG, Image/JPE, Image/jpg</span><span class="sxs-lookup"><span data-stu-id="06e0d-139">image/jpeg, image/jpe, image/jpg</span></span> | <span data-ttu-id="06e0d-140">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-140">Yes</span></span>      | <span data-ttu-id="06e0d-141">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-141">Yes</span></span>      |
| <span data-ttu-id="06e0d-142">PNG (Portable Network Graphics), especificación PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="06e0d-142">PNG (Portable Network Graphics), PNG Specification 1.2</span></span>                                            | <span data-ttu-id="06e0d-143">image/png</span><span class="sxs-lookup"><span data-stu-id="06e0d-143">image/png</span></span>                        | <span data-ttu-id="06e0d-144">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-144">Yes</span></span>      | <span data-ttu-id="06e0d-145">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-145">Yes</span></span>      |
| <span data-ttu-id="06e0d-146">TIFF (Tagged Image File Format), especificación TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="06e0d-146">TIFF (Tagged Image File Format), TIFF Specification 6.0</span></span>                                           | <span data-ttu-id="06e0d-147">imagen/TIFF, imagen/TIF</span><span class="sxs-lookup"><span data-stu-id="06e0d-147">image/tiff, image/tif</span></span>            | <span data-ttu-id="06e0d-148">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-148">Yes</span></span>      | <span data-ttu-id="06e0d-149">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-149">Yes</span></span>      |
| <span data-ttu-id="06e0d-150">Windows Media Photo, [HD Photo Specification 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span><span class="sxs-lookup"><span data-stu-id="06e0d-150">Windows Media Photo, [HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span></span> | <span data-ttu-id="06e0d-151">Image/vnd. ms-PHOT</span><span class="sxs-lookup"><span data-stu-id="06e0d-151">image/vnd.ms-phot</span></span>                | <span data-ttu-id="06e0d-152">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-152">Yes</span></span>      | <span data-ttu-id="06e0d-153">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-153">Yes</span></span>      |
| <span data-ttu-id="06e0d-154">DDS (superficie de DirectDraw)</span><span class="sxs-lookup"><span data-stu-id="06e0d-154">DDS (DirectDraw Surface)</span></span>                                                                          | <span data-ttu-id="06e0d-155">Image/vnd. ms-DDS</span><span class="sxs-lookup"><span data-stu-id="06e0d-155">image/vnd.ms-dds</span></span>                 | <span data-ttu-id="06e0d-156">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-156">Yes</span></span>      | <span data-ttu-id="06e0d-157">Sí</span><span class="sxs-lookup"><span data-stu-id="06e0d-157">Yes</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="06e0d-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06e0d-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="06e0d-159">**Vista**</span><span class="sxs-lookup"><span data-stu-id="06e0d-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="06e0d-160">Información general sobre metadatos de WIC</span><span class="sxs-lookup"><span data-stu-id="06e0d-160">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

<span data-ttu-id="06e0d-161">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="06e0d-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="06e0d-162">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="06e0d-162">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

<span data-ttu-id="06e0d-163">[CÓDEC de ejemplo AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06e0d-163">[AITCodec Sample CODEC](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span></span>
</dt> </dl>

 

 

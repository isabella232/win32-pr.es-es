---
title: Extensiones de nombre de archivo
description: Extensiones de nombre de archivo
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Metaarchivos de Windows Media, extensiones
- Metaarchivos de Windows Media, extensiones de nombre de archivo
- metaarchivos, extensiones
- metaarchivos, extensiones de nombre de archivo
- Windows Media, metaarchivos
- extensiones de nombre de archivo para los metaarchivos de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695440"
---
# <a name="file-name-extensions"></a><span data-ttu-id="09551-109">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="09551-109">File Name Extensions</span></span>

<span data-ttu-id="09551-110">Existen directrices específicas para el uso de extensiones de nombre de archivo para los metaarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09551-110">There are specific guidelines for the use of file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="09551-111">Las extensiones de nombre de metarchivo de Windows Media se utilizan para identificar los distintos tipos de archivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09551-111">Windows Media metafile name extensions are used to identify the different types of Windows Media files.</span></span> <span data-ttu-id="09551-112">Una extensión de nombre de archivo proporciona a un fabricante de software independiente (ISV) información sobre los requisitos de representación de una aplicación que utiliza una extensión determinada, y permite a los autores de contenido dirigirse a tipos generales de reproductores multimedia.</span><span class="sxs-lookup"><span data-stu-id="09551-112">A file name extension provides an Independent Software Vendor (ISV) with information about the rendering requirements of an application that uses a particular extension, and enables content authors to target general types of media players.</span></span>

<span data-ttu-id="09551-113">En la tabla siguiente se enumeran las instrucciones de extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="09551-113">The file name extension guidelines are listed in the following table.</span></span> <span data-ttu-id="09551-114">Se recomienda usar el tipo MIME de un archivo, situado en el encabezado del archivo, para la identificación del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="09551-114">It is recommended that a file's MIME type, located in the file header, be used for file-type identification.</span></span>



| <span data-ttu-id="09551-115">Extensión de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="09551-115">File name extension</span></span> | <span data-ttu-id="09551-116">Tipo de MIME</span><span class="sxs-lookup"><span data-stu-id="09551-116">MIME type</span></span>      | <span data-ttu-id="09551-117">Contenido del archivo</span><span class="sxs-lookup"><span data-stu-id="09551-117">File content</span></span>                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09551-118">.wma</span><span class="sxs-lookup"><span data-stu-id="09551-118">.wma</span></span>                | <span data-ttu-id="09551-119">audio/x-MS-WMA</span><span class="sxs-lookup"><span data-stu-id="09551-119">audio/x-ms-wma</span></span> | <span data-ttu-id="09551-120">Archivo de Windows Media con contenido de audio únicamente.</span><span class="sxs-lookup"><span data-stu-id="09551-120">Windows Media file with audio content only.</span></span> <span data-ttu-id="09551-121">Normalmente se usa para descargar y reproducir archivos o para transmitir contenido.</span><span class="sxs-lookup"><span data-stu-id="09551-121">Typically used to download and play files or to stream content.</span></span>                                                                             |
| <span data-ttu-id="09551-122">.wmv</span><span class="sxs-lookup"><span data-stu-id="09551-122">.wmv</span></span>                | <span data-ttu-id="09551-123">vídeo/x-MS-WMV</span><span class="sxs-lookup"><span data-stu-id="09551-123">video/x-ms-wmv</span></span> | <span data-ttu-id="09551-124">Archivo de Windows Media con contenido de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="09551-124">Windows Media file with audio and/or video content.</span></span> <span data-ttu-id="09551-125">Normalmente se usa para descargar y reproducir archivos o para transmitir contenido.</span><span class="sxs-lookup"><span data-stu-id="09551-125">Typically used to download and play files or to stream content.</span></span>                                                                     |
| <span data-ttu-id="09551-126">.asf</span><span class="sxs-lookup"><span data-stu-id="09551-126">.asf</span></span>                | <span data-ttu-id="09551-127">vídeo/x-MS-ASF</span><span class="sxs-lookup"><span data-stu-id="09551-127">video/x-ms-asf</span></span> | <span data-ttu-id="09551-128">Contenido heredado.</span><span class="sxs-lookup"><span data-stu-id="09551-128">Legacy content.</span></span> <span data-ttu-id="09551-129">Normalmente se usa para descargar y reproducir archivos o para transmitir contenido.</span><span class="sxs-lookup"><span data-stu-id="09551-129">Typically used to download and play files or to stream content.</span></span> <span data-ttu-id="09551-130">Puede contener contenido de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="09551-130">May contain audio and/or video content.</span></span> <span data-ttu-id="09551-131">Normalmente se usa para descargar y reproducir archivos o para transmitir contenido.</span><span class="sxs-lookup"><span data-stu-id="09551-131">Typically used to download and play files or to stream content.</span></span> |
| <span data-ttu-id="09551-132">.wm</span><span class="sxs-lookup"><span data-stu-id="09551-132">.wm</span></span>                 | <span data-ttu-id="09551-133">vídeo/x-MS-WM</span><span class="sxs-lookup"><span data-stu-id="09551-133">video/x-ms-wm</span></span>  | <span data-ttu-id="09551-134">Reservado</span><span class="sxs-lookup"><span data-stu-id="09551-134">Reserved</span></span>                                                                                                                                                                                |
| <span data-ttu-id="09551-135">. Wax</span><span class="sxs-lookup"><span data-stu-id="09551-135">.wax</span></span>                | <span data-ttu-id="09551-136">audio/x-MS-Wax</span><span class="sxs-lookup"><span data-stu-id="09551-136">audio/x-ms-wax</span></span> | <span data-ttu-id="09551-137">Metaarchivos que hacen referencia a archivos de Windows Media con las extensiones de nombre de archivo. ASF,. WMA o. Wax.</span><span class="sxs-lookup"><span data-stu-id="09551-137">Metafiles that reference Windows Media files with .asf, .wma, or .wax file name extensions.</span></span>                                                                                             |
| <span data-ttu-id="09551-138">. wvx</span><span class="sxs-lookup"><span data-stu-id="09551-138">.wvx</span></span>                | <span data-ttu-id="09551-139">vídeo/x-MS-wvx</span><span class="sxs-lookup"><span data-stu-id="09551-139">video/x-ms-wvx</span></span> | <span data-ttu-id="09551-140">Metaarchivos que hacen referencia a archivos de Windows Media con las extensiones de nombre de archivo. WMA,. wmv,. wvx o. Wax.</span><span class="sxs-lookup"><span data-stu-id="09551-140">Metafiles that reference Windows Media files with .wma, .wmv, .wvx, or .wax file name extensions.</span></span>                                                                                       |
| <span data-ttu-id="09551-141">.asx</span><span class="sxs-lookup"><span data-stu-id="09551-141">.asx</span></span>                | <span data-ttu-id="09551-142">vídeo/x-MS-ASF</span><span class="sxs-lookup"><span data-stu-id="09551-142">video/x-ms-asf</span></span> | <span data-ttu-id="09551-143">Metaarchivos que hacen referencia a archivos de Windows Media con las extensiones de nombre de archivo. WMA,. Wax,. wmv,. wvx,. ASF o. ASX.</span><span class="sxs-lookup"><span data-stu-id="09551-143">Metafiles that reference Windows Media files with .wma, .wax, .wmv, .wvx, .asf, or .asx file name extensions.</span></span>                                                                           |
| <span data-ttu-id="09551-144">. WMX</span><span class="sxs-lookup"><span data-stu-id="09551-144">.wmx</span></span>                | <span data-ttu-id="09551-145">vídeo/x-MS-wvx</span><span class="sxs-lookup"><span data-stu-id="09551-145">video/x-ms-wvx</span></span> | <span data-ttu-id="09551-146">Reservado.</span><span class="sxs-lookup"><span data-stu-id="09551-146">Reserved.</span></span>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="09551-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09551-147">Remarks</span></span>

<span data-ttu-id="09551-148">El scripting y la administración de derechos digitales (DRM) deben ser compatibles con cualquier aplicación que represente archivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09551-148">Scripting and digital rights management (DRM) must be supported by any application that renders Windows Media files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09551-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09551-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09551-150">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="09551-150">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="09551-151">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="09551-151">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="09551-152">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="09551-152">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





---
title: Instrucciones de extensión de metarchivo
description: Instrucciones de extensión de metarchivo
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
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
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076296"
---
# <a name="metafile-extension-guidelines"></a><span data-ttu-id="af7e7-109">Instrucciones de extensión de metarchivo</span><span class="sxs-lookup"><span data-stu-id="af7e7-109">Metafile Extension Guidelines</span></span>

<span data-ttu-id="af7e7-110">Una extensión de nombre de archivo proporciona a un fabricante de software independiente (ISV) información sobre los requisitos de representación de una aplicación que usa la extensión, y permite a los autores de contenido dirigirse a tipos generales de reproductores.</span><span class="sxs-lookup"><span data-stu-id="af7e7-110">A file name extension provides an independent software vendor (ISV) with information about the rendering requirements of an application that uses the extension, and enables content authors to target general types of players.</span></span>

<span data-ttu-id="af7e7-111">Las extensiones de nombre de metarchivo de Windows Media se utilizan para identificar el formato de los archivos de Windows Media a los que hace referencia un metarchivo.</span><span class="sxs-lookup"><span data-stu-id="af7e7-111">Windows Media metafile name extensions are used to identify the format of the Windows Media files that a metafile references.</span></span> <span data-ttu-id="af7e7-112">Los metaarchivos de Windows Media con extensiones. Wax,. wvx o. ASX hacen referencia a archivos con extensiones. WMA,. WMV y. ASF, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="af7e7-112">Windows Media metafiles with .wax, .wvx, or .asx extensions reference files with .wma, .wmv, and .asf extensions, respectively.</span></span> <span data-ttu-id="af7e7-113">Todos los metaarchivos, independientemente de la extensión de nombre de archivo usada, tienen la etiqueta del elemento **ASX** al principio del archivo con el atributo de **versión** especificado.</span><span class="sxs-lookup"><span data-stu-id="af7e7-113">All metafiles, regardless of the file name extension used, have the **ASX** element tag at the beginning of the file with the **version** attribute specified.</span></span>

<span data-ttu-id="af7e7-114">En la tabla siguiente se muestran los tipos de archivos multimedia a los que hace referencia cada tipo de extensión de nombre de archivo de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="af7e7-114">The following table shows the media file types referenced by each type of metafile file name extension.</span></span> <span data-ttu-id="af7e7-115">Las columnas enumeran las extensiones de nombre de archivo multimedia y las extensiones de nombre de metarchivo de lista de filas.</span><span class="sxs-lookup"><span data-stu-id="af7e7-115">The columns list media file name extensions, the rows list metafile name extensions.</span></span> <span data-ttu-id="af7e7-116">Una X en una columna indica un tipo de archivo multimedia al que se puede hacer referencia mediante una extensión de nombre de archivo de metarchivo determinada.</span><span class="sxs-lookup"><span data-stu-id="af7e7-116">An X in a column indicates a media file type that can be referenced by a particular metafile file name extension.</span></span>



| <span data-ttu-id="af7e7-117">Extensión</span><span class="sxs-lookup"><span data-stu-id="af7e7-117">Extension</span></span> | <span data-ttu-id="af7e7-118">.asf</span><span class="sxs-lookup"><span data-stu-id="af7e7-118">.asf</span></span> | <span data-ttu-id="af7e7-119">.wma</span><span class="sxs-lookup"><span data-stu-id="af7e7-119">.wma</span></span> | <span data-ttu-id="af7e7-120">.wmv</span><span class="sxs-lookup"><span data-stu-id="af7e7-120">.wmv</span></span> |
|-----------|------|------|------|
| <span data-ttu-id="af7e7-121">. wvx</span><span class="sxs-lookup"><span data-stu-id="af7e7-121">.wvx</span></span>      | <span data-ttu-id="af7e7-122">X</span><span class="sxs-lookup"><span data-stu-id="af7e7-122">X</span></span>    | <span data-ttu-id="af7e7-123">X</span><span class="sxs-lookup"><span data-stu-id="af7e7-123">X</span></span>    | <span data-ttu-id="af7e7-124">X</span><span class="sxs-lookup"><span data-stu-id="af7e7-124">X</span></span>    |
| <span data-ttu-id="af7e7-125">. Wax</span><span class="sxs-lookup"><span data-stu-id="af7e7-125">.wax</span></span>      | <span data-ttu-id="af7e7-126">X</span><span class="sxs-lookup"><span data-stu-id="af7e7-126">X</span></span>    | <span data-ttu-id="af7e7-127">X</span><span class="sxs-lookup"><span data-stu-id="af7e7-127">X</span></span>    |      |
| <span data-ttu-id="af7e7-128">.asx</span><span class="sxs-lookup"><span data-stu-id="af7e7-128">.asx</span></span>      | <span data-ttu-id="af7e7-129">X</span><span class="sxs-lookup"><span data-stu-id="af7e7-129">X</span></span>    |      |      |



 

## <a name="related-topics"></a><span data-ttu-id="af7e7-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af7e7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af7e7-131">**Extensiones de nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="af7e7-131">**File Name Extensions**</span></span>](file-name-extensions.md)
</dt> <dt>

[<span data-ttu-id="af7e7-132">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="af7e7-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="af7e7-133">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="af7e7-133">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





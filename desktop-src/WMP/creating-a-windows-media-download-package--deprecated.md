---
title: Crear un paquete de descarga de Windows Media (en desuso)
description: Crear un paquete de descarga de Windows Media (en desuso)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Metaarchivos de Windows Media, paquetes de descarga de Windows Media
- Windows Media Player, paquetes de descarga de Windows Media
- metaarchivos, paquetes de descarga de Windows Media
- Windows Media, paquetes de descarga de Windows Media
- Paquetes de descarga de Windows Media, crear
- crear paquetes de descarga de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075928"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a><span data-ttu-id="76b02-109">Crear un paquete de descarga de Windows Media (en desuso)</span><span class="sxs-lookup"><span data-stu-id="76b02-109">Creating a Windows Media Download Package (deprecated)</span></span>

<span data-ttu-id="76b02-110">En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="76b02-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="76b02-111">Siga estos pasos para crear un paquete de descarga de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="76b02-111">Follow these steps to create a Windows Media Download package.</span></span>

1.  <span data-ttu-id="76b02-112">**Cree un borde.**</span><span class="sxs-lookup"><span data-stu-id="76b02-112">**Create a border.**</span></span> <span data-ttu-id="76b02-113">Utilice las mismas técnicas que utilizaría para crear una máscara para Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="76b02-113">Use the same techniques you would use to build a skin for Windows Media Player.</span></span> <span data-ttu-id="76b02-114">Diseñe el borde para que el cambio de tamaño de Windows Media Player no dañe la composición de los elementos de borde.</span><span class="sxs-lookup"><span data-stu-id="76b02-114">Design the border so that resizing Windows Media Player will not ruin the composition of the border elements.</span></span> <span data-ttu-id="76b02-115">Por ejemplo, use un color sólido o una visualización como fondo, ya que se escalarán correctamente a medida que se cambie el tamaño de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="76b02-115">For instance, use a solid color or visualization as a background because these will scale well as Windows Media Player is resized.</span></span>
2.  <span data-ttu-id="76b02-116">**Comprimir el contenido del borde.**</span><span class="sxs-lookup"><span data-stu-id="76b02-116">**Compress the border contents.**</span></span> <span data-ttu-id="76b02-117">Cree una carpeta comprimida (con una extensión de nombre de archivo. zip) que contenga los archivos de borde: imágenes, archivos JScript y el archivo de definición de máscara con la extensión de nombre de archivo. WMS.</span><span class="sxs-lookup"><span data-stu-id="76b02-117">Create a compressed folder (with a .zip file name extension) that contains the border files: images, JScript files, and the skin definition file with a .wms file name extension.</span></span> <span data-ttu-id="76b02-118">Cambie el nombre del archivo comprimido para que tenga una extensión de nombre de archivo. WMZ.</span><span class="sxs-lookup"><span data-stu-id="76b02-118">Rename the compressed file so that it has a .wmz file name extension.</span></span>
3.  <span data-ttu-id="76b02-119">**Escriba un metarchivo de Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="76b02-119">**Write a Windows Media metafile.**</span></span> <span data-ttu-id="76b02-120">Windows Media Player no cargará el borde a menos que cree un metarchivo de Windows Media con una extensión de nombre de archivo. ASX que implementa el elemento **Skin** .</span><span class="sxs-lookup"><span data-stu-id="76b02-120">Windows Media Player will not load the border unless you create a Windows Media metafile with an .asx file name extension that implements the **SKIN** element.</span></span> <span data-ttu-id="76b02-121">El metarchivo también se puede utilizar para crear una lista de reproducción que describa el contenido incluido en el paquete.</span><span class="sxs-lookup"><span data-stu-id="76b02-121">The metafile can also be used to create a playlist that describes the content included in the package.</span></span>
4.  <span data-ttu-id="76b02-122">**Ensamble el contenido.**</span><span class="sxs-lookup"><span data-stu-id="76b02-122">**Assemble your content.**</span></span> <span data-ttu-id="76b02-123">Coloque todos los archivos que desee usar en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="76b02-123">Put all the files that you want to use into a folder.</span></span> <span data-ttu-id="76b02-124">Esto incluye archivos de audio, archivos de vídeo, metaarchivos y archivos de definición de borde.</span><span class="sxs-lookup"><span data-stu-id="76b02-124">This includes audio files, video files, metafiles, and border definition files.</span></span>
5.  <span data-ttu-id="76b02-125">**Cree el paquete.**</span><span class="sxs-lookup"><span data-stu-id="76b02-125">**Create the package.**</span></span> <span data-ttu-id="76b02-126">Cree una carpeta comprimida (con una extensión de nombre de archivo. zip) que contenga el archivo de borde, los archivos de contenido y el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="76b02-126">Create a compressed folder (with a .zip file name extension) that contains the border file, content files, and the metafile.</span></span> <span data-ttu-id="76b02-127">Cambie la extensión de nombre de archivo de este archivo. zip a la extensión de nombre de archivo. WMD.</span><span class="sxs-lookup"><span data-stu-id="76b02-127">Change the file name extension of this .zip file to a .wmd file name extension.</span></span>
6.  <span data-ttu-id="76b02-128">**Publicar el paquete en un sitio Web.**</span><span class="sxs-lookup"><span data-stu-id="76b02-128">**Post the package to a website.**</span></span> <span data-ttu-id="76b02-129">El paquete completado está listo para publicarse en un sitio web y los usuarios lo descargan.</span><span class="sxs-lookup"><span data-stu-id="76b02-129">The completed package is ready to be posted to a website and downloaded by users.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76b02-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76b02-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b02-131">**Paquetes de descarga de Windows Media (en desuso)**</span><span class="sxs-lookup"><span data-stu-id="76b02-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 





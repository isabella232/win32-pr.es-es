---
title: Bordes de Media Player de Windows (desusado)
description: Bordes de Media Player de Windows (desusado)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Media Player de Windows, bordes
- Aspectos de Windows Media Player, bordes
- máscaras, bordes
- bordes, comparación con máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357074"
---
# <a name="borders-for-windows-media-player-deprecated"></a><span data-ttu-id="0a5e7-107">Bordes de Media Player de Windows (desusado)</span><span class="sxs-lookup"><span data-stu-id="0a5e7-107">Borders for Windows Media Player (deprecated)</span></span>

<span data-ttu-id="0a5e7-108">En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-108">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="0a5e7-109">Un borde es similar a una máscara, pero en lugar de reemplazar la interfaz de usuario para el modo compacto de Windows Media Player, se inserta un borde en el panel reproducción en curso del Media Player de Windows en modo completo.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-109">A border is similar to a skin, but instead of replacing the user interface for the compact mode of Windows Media Player, a border is embedded in the Now Playing pane of the full mode Windows Media Player.</span></span>

<span data-ttu-id="0a5e7-110">Mediante el uso de un paquete de descarga de Windows Media, puede incluir contenido con un borde, y así llegar a las aplicaciones multimedia.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-110">By using a Windows Media Download package, you can include content with a border, paving the way to multimedia applications.</span></span>

<span data-ttu-id="0a5e7-111">En el directorio de ejemplos de este SDK se incluye un paquete de descarga de Windows Media de ejemplo que incluye un borde y contenido incrustado.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-111">A sample Windows Media Download package that includes a border and embedded content is included in the samples directory of this SDK.</span></span>

## <a name="creating-a-border"></a><span data-ttu-id="0a5e7-112">Crear un borde</span><span class="sxs-lookup"><span data-stu-id="0a5e7-112">Creating a Border</span></span>

<span data-ttu-id="0a5e7-113">Un borde se crea de la misma manera que una máscara.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-113">A border is created the same way as a skin.</span></span> <span data-ttu-id="0a5e7-114">La única diferencia es que la máscara está incrustada dentro del panel **reproducción en curso** .</span><span class="sxs-lookup"><span data-stu-id="0a5e7-114">The only difference is that the skin is embedded inside the **Now Playing** pane.</span></span> <span data-ttu-id="0a5e7-115">Esto significa que no se puede calcular el tamaño de la máscara y que todos los elementos de máscara deben ser relativos.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-115">This means that the skin size cannot be calculated and that all skin elements must be relative.</span></span> <span data-ttu-id="0a5e7-116">Si el usuario cambia el tamaño de Windows Media Player, se pueden recortar partes del borde y no verse.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-116">If the user resizes Windows Media Player, portions of the border may be clipped off and not seen.</span></span>

## <a name="loading-a-border"></a><span data-ttu-id="0a5e7-117">Cargar un borde</span><span class="sxs-lookup"><span data-stu-id="0a5e7-117">Loading a Border</span></span>

<span data-ttu-id="0a5e7-118">Se carga un borde cuando se carga un metarchivo de Windows Media que utiliza el elemento de **máscara** .</span><span class="sxs-lookup"><span data-stu-id="0a5e7-118">A border is loaded when a Windows Media metafile that uses the **SKIN** element is loaded.</span></span> <span data-ttu-id="0a5e7-119">El atributo **href** del elemento **Skin** debe hacer referencia a una máscara.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-119">The **HREF** attribute of the **SKIN** element must reference a skin.</span></span> <span data-ttu-id="0a5e7-120">Un elemento de **máscara** típico tendría el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="0a5e7-120">A typical **SKIN** element would look like this:</span></span>


```C++
<SKIN HREF="myborder.wmz">

```



<span data-ttu-id="0a5e7-121">Para obtener más información, vea [elemento Skin (deprecated)](skin-element--deprecated.md).</span><span class="sxs-lookup"><span data-stu-id="0a5e7-121">For more information, see [SKIN Element (deprecated)](skin-element--deprecated.md).</span></span>

## <a name="including-content-with-a-border"></a><span data-ttu-id="0a5e7-122">Incluir contenido con un borde</span><span class="sxs-lookup"><span data-stu-id="0a5e7-122">Including Content with a Border</span></span>

<span data-ttu-id="0a5e7-123">Puede incluir contenido con un borde mediante un archivo de descarga de Windows Media (con la extensión de nombre de archivo. WMD).</span><span class="sxs-lookup"><span data-stu-id="0a5e7-123">You can include content with a border by using a Windows Media Download file (with a .wmd file name extension).</span></span> <span data-ttu-id="0a5e7-124">Siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="0a5e7-124">Follow these steps:</span></span>

1.  <span data-ttu-id="0a5e7-125">Cree el borde.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-125">Create the border.</span></span> <span data-ttu-id="0a5e7-126">Tenga cuidado de crearlo de modo que el cambio de tamaño no dañe la composición del borde.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-126">Take care to create it in such a way that resizing will not ruin the composition of the border.</span></span> <span data-ttu-id="0a5e7-127">Por ejemplo, no incluya un archivo de fondo; Haga que el fondo sea transparente para que una visualización pueda ejecutarse detrás.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-127">For example, do not include a background file; make the background transparent so that a visualization could run behind it.</span></span>
2.  <span data-ttu-id="0a5e7-128">Comprimir el contenido de la máscara (imágenes, archivos JScript y el archivo de definición de máscara) en un archivo con la extensión de nombre de archivo. WMZ.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-128">Compress the skin contents (art, JScript files, and skin definition file) into a file with a .wmz file name extension.</span></span>
3.  <span data-ttu-id="0a5e7-129">Cree un metarchivo de Windows Media (con una extensión de nombre de archivo. ASX) que haga referencia al archivo de borde comprimido (con una extensión de nombre de archivo. WMZ).</span><span class="sxs-lookup"><span data-stu-id="0a5e7-129">Create a Windows Media metafile (with an .asx file name extension) that references the compressed border file (with a .wmz file name extension).</span></span> <span data-ttu-id="0a5e7-130">El metarchivo puede incluir información de lista de reproducción con metadatos para arte y direcciones URL de contenido específico.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-130">The metafile can include playlist information with metadata for art and URLs for specific content.</span></span>
4.  <span data-ttu-id="0a5e7-131">Ensamble el contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-131">Assemble the digital media content.</span></span>
5.  <span data-ttu-id="0a5e7-132">Comprima el borde, el metarchivo y el contenido en un archivo y asígnele una extensión de nombre de archivo. WMD.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-132">Compress the border, metafile, and content into one file and give it a .wmd file name extension.</span></span>

## <a name="using-a-border"></a><span data-ttu-id="0a5e7-133">Usar un borde</span><span class="sxs-lookup"><span data-stu-id="0a5e7-133">Using a Border</span></span>

<span data-ttu-id="0a5e7-134">Una vez creado el archivo de descarga de Windows Media, lo único que debe hacer el usuario es hacer doble clic en él.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-134">After you have created the Windows Media Download file, all that the user has to do is double-click on it.</span></span> <span data-ttu-id="0a5e7-135">El archivo se descargará en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-135">The file will be downloaded to the user's computer.</span></span> <span data-ttu-id="0a5e7-136">Los archivos incluidos en el paquete se desempaquetarán, se agregará la lista de reproducción a las listas de reproducción, el borde aparecerá en el panel **reproducción en curso** del Media Player de Windows en modo completo y el primer elemento de la nueva lista de reproducción comenzará a reproducirse.</span><span class="sxs-lookup"><span data-stu-id="0a5e7-136">The files inside the package will be unpacked, the playlist will be added to the playlists, the border will appear in the **Now Playing** pane of the full mode Windows Media Player, and the first item on the new playlist will begin playing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a5e7-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a5e7-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a5e7-138">**Acerca de las máscaras**</span><span class="sxs-lookup"><span data-stu-id="0a5e7-138">**About Skins**</span></span>](about-skins.md)
</dt> <dt>

[<span data-ttu-id="0a5e7-139">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="0a5e7-139">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="0a5e7-140">**Paquetes de descarga de Windows Media (en desuso)**</span><span class="sxs-lookup"><span data-stu-id="0a5e7-140">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 





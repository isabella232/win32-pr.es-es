---
title: Entradas del registro de clasificación de biblioteca
description: Entradas del registro de clasificación de biblioteca
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player, biblioteca
- Windows Media Player, entradas del registro de clasificación
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- registro, entradas de clasificación de biblioteca
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- Biblioteca, entradas del registro de clasificación
- Biblioteca, registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695390"
---
# <a name="library-classification-registry-entries"></a><span data-ttu-id="7a227-113">Entradas del registro de clasificación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a227-113">Library Classification Registry Entries</span></span>

<span data-ttu-id="7a227-114">Cuando Windows Media Player encuentra un archivo multimedia que tiene una extensión de nombre de archivo personalizada, no sabe si el archivo debe clasificarse como audio, vídeo o algún otro tipo.</span><span class="sxs-lookup"><span data-stu-id="7a227-114">When Windows Media Player encounters a media file that has a custom file name extension, it does not know whether the file should be classified as audio, video, or some other type.</span></span> <span data-ttu-id="7a227-115">De forma predeterminada, Windows Media Player coloca dichos archivos en la otra parte multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7a227-115">By default, Windows Media Player places such files in the Other Media portion of the library.</span></span>

<span data-ttu-id="7a227-116">Si los archivos multimedia digitales tienen un formato personalizado, puede proporcionar a Windows Media Player información sobre el lugar en el que los archivos deben aparecer en la biblioteca del reproductor colocando dos entradas en el registro en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="7a227-116">If your digital media files have a custom format, you can provide Windows Media Player with information about where your files should appear in the Player's library by placing two entries in the registry on the user's computer.</span></span>

<span data-ttu-id="7a227-117">Una entrada entra en la subclave siguiente.</span><span class="sxs-lookup"><span data-stu-id="7a227-117">One entry goes in the following subkey.</span></span>

<span data-ttu-id="7a227-118">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ extensions**</span><span class="sxs-lookup"><span data-stu-id="7a227-118">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="7a227-119">La entrada del registro tiene el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="7a227-119">The registry entry has the following format.</span></span>



| <span data-ttu-id="7a227-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7a227-120">Name</span></span>                                                  | <span data-ttu-id="7a227-121">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7a227-121">Data type</span></span>   | <span data-ttu-id="7a227-122">Value</span><span class="sxs-lookup"><span data-stu-id="7a227-122">Value</span></span>                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| <span data-ttu-id="7a227-123">La extensión de nombre de archivo sin el separador de puntos (.)</span><span class="sxs-lookup"><span data-stu-id="7a227-123">The file name extension without the dot (.) separator</span></span> | <span data-ttu-id="7a227-124">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="7a227-124">**REG\_SZ**</span></span> | <span data-ttu-id="7a227-125">Cadena que especifica la ubicación de una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7a227-125">A string that specifies a library location</span></span> |



 

<span data-ttu-id="7a227-126">La otra entrada del registro entra en la siguiente subclave que cree.</span><span class="sxs-lookup"><span data-stu-id="7a227-126">The other registry entry goes in the following subkey that you create.</span></span>

<span data-ttu-id="7a227-127">**HKEY \_ Clases \_ raíz \\** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="7a227-127">**HKEY\_CLASSES\_ROOT\\** *customExtension*</span></span>

<span data-ttu-id="7a227-128">donde *customExtension* es la extensión de nombre de archivo, incluido el separador de puntos (.).</span><span class="sxs-lookup"><span data-stu-id="7a227-128">where *customExtension* is the file name extension including the dot (.) separator.</span></span>

<span data-ttu-id="7a227-129">La entrada del registro tiene el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="7a227-129">The registry entry has the following format.</span></span>



| <span data-ttu-id="7a227-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="7a227-130">Name</span></span>          | <span data-ttu-id="7a227-131">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7a227-131">Data type</span></span>   | <span data-ttu-id="7a227-132">Value</span><span class="sxs-lookup"><span data-stu-id="7a227-132">Value</span></span>                                      |
|---------------|-------------|--------------------------------------------|
| <span data-ttu-id="7a227-133">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="7a227-133">PerceivedType</span></span> | <span data-ttu-id="7a227-134">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="7a227-134">**REG\_SZ**</span></span> | <span data-ttu-id="7a227-135">Cadena que especifica la ubicación de una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7a227-135">A string that specifies a library location</span></span> |



 

<span data-ttu-id="7a227-136">Ambas entradas del registro deben tener el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="7a227-136">Both registry entries must have the same value.</span></span> <span data-ttu-id="7a227-137">En la tabla siguiente se proporcionan los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="7a227-137">Possible values are given in the following table.</span></span>



| <span data-ttu-id="7a227-138">Value</span><span class="sxs-lookup"><span data-stu-id="7a227-138">Value</span></span> | <span data-ttu-id="7a227-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a227-139">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7a227-140">audio</span><span class="sxs-lookup"><span data-stu-id="7a227-140">audio</span></span> | <span data-ttu-id="7a227-141">Los archivos que tienen la extensión personalizada aparecen en la parte música de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7a227-141">Files that have the custom extension appear in the music portion of the library.</span></span> |
| <span data-ttu-id="7a227-142">video</span><span class="sxs-lookup"><span data-stu-id="7a227-142">video</span></span> | <span data-ttu-id="7a227-143">Los archivos que tienen la extensión personalizada aparecen en la parte de vídeo de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7a227-143">Files that have the custom extension appear in the video portion of the library.</span></span> |



 

<span data-ttu-id="7a227-144">Por ejemplo, las siguientes entradas del registro especifican que los archivos que tienen la extensión de nombre de archivo. XYZ aparecerán en la parte de música de la biblioteca:</span><span class="sxs-lookup"><span data-stu-id="7a227-144">For example, the following registry entries specify that files having the file name extension .xyz will appear in the music portion of the library:</span></span>


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



<span data-ttu-id="7a227-145">Tenga en cuenta que cualquier código que intente escribir en el registro en el equipo del usuario puede escribir en el \_ subárbol de la máquina local HKEY \_ solo si el usuario actual tiene privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="7a227-145">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="7a227-146">Las entradas del registro de clasificación de bibliotecas son compatibles con las siguientes versiones de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7a227-146">Library classification registry entries are supported by the following versions of Windows Media Player.</span></span>

-   <span data-ttu-id="7a227-147">Windows Media Player 9 series con la revisión 823275</span><span class="sxs-lookup"><span data-stu-id="7a227-147">Windows Media Player 9 Series with hotfix 823275</span></span>
-   <span data-ttu-id="7a227-148">Windows Media Player 10 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="7a227-148">Windows Media Player 10 and later</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a227-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a227-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a227-150">**Configuración del registro de la extensión de nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="7a227-150">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 





---
title: Entrada del registro de permisos
description: Entrada del registro de permisos
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, permisos
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- registro, permisos
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- permisos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077292"
---
# <a name="permissions-registry-entry"></a><span data-ttu-id="9e70d-111">Entrada del registro de permisos</span><span class="sxs-lookup"><span data-stu-id="9e70d-111">Permissions Registry Entry</span></span>

<span data-ttu-id="9e70d-112">Cuando Windows Media Player encuentra una extensión de nombre de archivo personalizada, busca una subclave del registro que coincida con la extensión.</span><span class="sxs-lookup"><span data-stu-id="9e70d-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="9e70d-113">La subclave se describe en [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="9e70d-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="9e70d-114">Una de las entradas del registro que pueden aparecer bajo la subclave de la extensión es la entrada de **permisos** .</span><span class="sxs-lookup"><span data-stu-id="9e70d-114">One of the registry entries that can appear under the extension's subkey is the **Permissions** entry.</span></span>

<span data-ttu-id="9e70d-115">La entrada de **permisos** especifica las acciones que puede realizar Windows Media Player en los archivos que tienen la extensión personalizada.</span><span class="sxs-lookup"><span data-stu-id="9e70d-115">The **Permissions** entry specifies the actions that Windows Media Player is allowed to perform on files that have the custom extension.</span></span> <span data-ttu-id="9e70d-116">La entrada de **permisos** tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="9e70d-116">The **Permissions** entry has the following form.</span></span>



| <span data-ttu-id="9e70d-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="9e70d-117">Name</span></span>        | <span data-ttu-id="9e70d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e70d-118">Type</span></span>           | <span data-ttu-id="9e70d-119">Value</span><span class="sxs-lookup"><span data-stu-id="9e70d-119">Value</span></span>                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="9e70d-120">Permisos</span><span class="sxs-lookup"><span data-stu-id="9e70d-120">Permissions</span></span> | <span data-ttu-id="9e70d-121">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="9e70d-121">**REG\_DWORD**</span></span> | <span data-ttu-id="9e70d-122">Un conjunto de marcas, cada una de las cuales concede el permiso para una acción específica.</span><span class="sxs-lookup"><span data-stu-id="9e70d-122">A set of flags, each of which grants permission for a specific action.</span></span> |



 

<span data-ttu-id="9e70d-123">El valor de la entrada **Permissions** es **una operación OR bit a bit** de una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="9e70d-123">The value of the **Permissions** entry is a bitwise **OR** of one or more of the following flags.</span></span>



| <span data-ttu-id="9e70d-124">Marca (valor decimal)</span><span class="sxs-lookup"><span data-stu-id="9e70d-124">Flag (decimal value)</span></span> | <span data-ttu-id="9e70d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e70d-125">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e70d-126">1</span><span class="sxs-lookup"><span data-stu-id="9e70d-126">1</span></span>                    | <span data-ttu-id="9e70d-127">Permiso para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="9e70d-127">Permission for playback.</span></span> <span data-ttu-id="9e70d-128">Se pueden reproducir archivos con la extensión de nombre de archivo registrada.</span><span class="sxs-lookup"><span data-stu-id="9e70d-128">Files having the registered file name extension can be played.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="9e70d-129">2</span><span class="sxs-lookup"><span data-stu-id="9e70d-129">2</span></span>                    | <span data-ttu-id="9e70d-130">Permiso para quitar carpetas.</span><span class="sxs-lookup"><span data-stu-id="9e70d-130">Permission for folder drop.</span></span> <span data-ttu-id="9e70d-131">Los archivos que tengan la extensión de nombre de archivo registrada se incluirán en la lista de reproducción que se creó cuando el usuario arrastra una carpeta que contiene los archivos y la coloca en la interfaz de usuario del reproductor.</span><span class="sxs-lookup"><span data-stu-id="9e70d-131">Files having the registered file name extension will be included in the playlist created when the user drags a folder containing the files and drops it on the user interface of the Player.</span></span>                                                      |
| <span data-ttu-id="9e70d-132">4</span><span class="sxs-lookup"><span data-stu-id="9e70d-132">4</span></span>                    | <span data-ttu-id="9e70d-133">Permiso para el CD de multimedia.</span><span class="sxs-lookup"><span data-stu-id="9e70d-133">Permission for media CD.</span></span> <span data-ttu-id="9e70d-134">Los archivos que tengan la extensión de nombre de archivo registrada se incluirán en la lista de reproducción creada cuando se inserte un CD que contenga los archivos en la unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="9e70d-134">Files having the registered file name extension will be included in the playlist created when a CD containing the files is inserted into the CD-ROM drive.</span></span>                                                                                           |
| <span data-ttu-id="9e70d-135">8</span><span class="sxs-lookup"><span data-stu-id="9e70d-135">8</span></span>                    | <span data-ttu-id="9e70d-136">Permiso para la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9e70d-136">Permission for the library.</span></span> <span data-ttu-id="9e70d-137">Los archivos que tienen la extensión de nombre de archivo registrada se pueden agregar a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9e70d-137">Files having the registered file name extension can be added to the library.</span></span> <span data-ttu-id="9e70d-138">Se requiere para los complementos de conversión.</span><span class="sxs-lookup"><span data-stu-id="9e70d-138">Required for conversion plug-ins.</span></span>                                                                                                                                    |
| <span data-ttu-id="9e70d-139">16</span><span class="sxs-lookup"><span data-stu-id="9e70d-139">16</span></span>                   | <span data-ttu-id="9e70d-140">Permiso para la transmisión por secuencias de HTML.</span><span class="sxs-lookup"><span data-stu-id="9e70d-140">Permission for HTML streaming.</span></span> <span data-ttu-id="9e70d-141">Los archivos que tengan la extensión de nombre de archivo registrada se insertarán en la memoria caché de Internet Explorer cuando se entreguen desde una secuencia Web.</span><span class="sxs-lookup"><span data-stu-id="9e70d-141">Files having the registered file name extension will be inserted into the Internet Explorer cache when delivered from a Web stream.</span></span>                                                                                                            |
| <span data-ttu-id="9e70d-142">128</span><span class="sxs-lookup"><span data-stu-id="9e70d-142">128</span></span>                  | <span data-ttu-id="9e70d-143">Permiso para la transcodificación.</span><span class="sxs-lookup"><span data-stu-id="9e70d-143">Permission for transcoding.</span></span> <span data-ttu-id="9e70d-144">Los archivos que tienen la extensión de nombre de archivo registrada se pueden transcodificar en formato de Windows Media en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="9e70d-144">Files having the registered file name extension can be transcoded to Windows Media Format under certain conditions.</span></span> <span data-ttu-id="9e70d-145">Vea [IWMPTranscodePolicy:: allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span><span class="sxs-lookup"><span data-stu-id="9e70d-145">See [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span></span> <span data-ttu-id="9e70d-146">Requiere Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9e70d-146">Requires Windows Media Player 10 or later.</span></span> |



 

<span data-ttu-id="9e70d-147">Cuando el usuario intenta reproducir un archivo multimedia que tiene una extensión de nombre de archivo personalizada, Windows Media Player busca una subclave del registro que coincida con la extensión.</span><span class="sxs-lookup"><span data-stu-id="9e70d-147">When the user attempts to play a media file that has a custom file name extension, Windows Media Player looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="9e70d-148">Si no se encuentra ninguna coincidencia, el reproductor presenta al usuario un cuadro de diálogo de advertencia que solicita permiso al usuario para intentar reproducir el archivo.</span><span class="sxs-lookup"><span data-stu-id="9e70d-148">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="9e70d-149">Si crea archivos multimedia digitales con extensiones de nombre de archivo personalizadas, puede evitar que esta advertencia aparezca en el equipo del usuario si registra la extensión de nombre de archivo y proporciona una entrada de **permisos** .</span><span class="sxs-lookup"><span data-stu-id="9e70d-149">If you create digital media files with custom file name extensions, you can prevent this warning from appearing on the user's computer by registering the file name extension and providing a **Permissions** entry.</span></span>

<span data-ttu-id="9e70d-150">La entrada de **permisos** (excepto el valor de marca 128) es compatible con Windows Media Player 9 series y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9e70d-150">The **Permissions** entry (except for the flag value 128) is supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="9e70d-151">Windows Media Player 10 y versiones posteriores admiten el valor de marca 128.</span><span class="sxs-lookup"><span data-stu-id="9e70d-151">The flag value 128 is supported by Windows Media Player 10 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e70d-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e70d-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e70d-153">**Configuración del registro de la extensión de nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="9e70d-153">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 





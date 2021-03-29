---
title: Configuración del registro de la extensión de nombre de archivo
description: Configuración del registro de la extensión de nombre de archivo
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Media Player de Windows, registro
- Windows Media Player, extensiones de nombre de archivo
- registro, extensiones de nombre de archivo
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778487"
---
# <a name="file-name-extension-registry-settings"></a><span data-ttu-id="7be3e-108">Configuración del registro de la extensión de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="7be3e-108">File Name Extension Registry Settings</span></span>

<span data-ttu-id="7be3e-109">Si los archivos multimedia digitales tienen un formato personalizado, puede proporcionar a Windows Media Player información acerca del formato personalizado colocando entradas en el registro en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="7be3e-109">If your digital media files have a custom format, you can provide Windows Media Player with information about your custom format by placing entries in the registry on the user's computer.</span></span> <span data-ttu-id="7be3e-110">Windows Media Player inspecciona las entradas del registro para determinar cómo debe controlar los archivos.</span><span class="sxs-lookup"><span data-stu-id="7be3e-110">Windows Media Player inspects your registry entries to determine how it should handle your files.</span></span> <span data-ttu-id="7be3e-111">La lista siguiente muestra algunas de las cosas que puede hacer mediante la creación de entradas del registro que pertenecen a su formato de archivo multimedia personalizado.</span><span class="sxs-lookup"><span data-stu-id="7be3e-111">The following list shows several of the things you can do by creating registry entries that pertain to your custom media file format.</span></span>

-   <span data-ttu-id="7be3e-112">Conceda permiso al reproductor para reproducir, copiar o transcodificar los archivos.</span><span class="sxs-lookup"><span data-stu-id="7be3e-112">Grant permission for the Player to play, copy, or transcode your files.</span></span>
-   <span data-ttu-id="7be3e-113">Especifique la tecnología subyacente que el reproductor debe usar para reproducir los archivos.</span><span class="sxs-lookup"><span data-stu-id="7be3e-113">Specify the underlying technology that the Player should use to play your files.</span></span>
-   <span data-ttu-id="7be3e-114">Especifique dónde debe mostrar los archivos el reproductor en la vista biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7be3e-114">Specify where the Player should display your files in its library view.</span></span>
-   <span data-ttu-id="7be3e-115">Especifique un complemento que el reproductor debe usar para convertir los archivos a un formato estándar.</span><span class="sxs-lookup"><span data-stu-id="7be3e-115">Specify a plug-in that the Player should use to convert your files to a standard format.</span></span>
-   <span data-ttu-id="7be3e-116">Especifique un código de formato MTP (Protocolo de transporte de medios) que el reproductor pueda utilizar para determinar si un dispositivo portátil determinado es compatible con el formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="7be3e-116">Specify a Media Transport Protocol (MTP) format code that the Player can use to determine whether a particular portable device supports your file format.</span></span>

<span data-ttu-id="7be3e-117">La mayoría de las entradas que proporcione estarán en una subclave asociada a la extensión de nombre de archivo personalizada.</span><span class="sxs-lookup"><span data-stu-id="7be3e-117">Most of the entries that you provide will be under a subkey that is associated with your custom file name extension.</span></span> <span data-ttu-id="7be3e-118">Puede crear esa subclave en el \_ \_ subárbol del equipo local HKEY y en el \_ subárbol de usuario de HKEY current \_ .</span><span class="sxs-lookup"><span data-stu-id="7be3e-118">You can create that subkey in the HKEY\_LOCAL\_MACHINE subtree and in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="7be3e-119">Windows Media Player busca en primer lugar en \_ el \_ subárbol HKEY local Machine.</span><span class="sxs-lookup"><span data-stu-id="7be3e-119">Windows Media Player looks first in the HKEY\_LOCAL\_MACHINE subtree.</span></span> <span data-ttu-id="7be3e-120">Si no encuentra lo que necesita allí, busca en el \_ subárbol HKEY current \_ User.</span><span class="sxs-lookup"><span data-stu-id="7be3e-120">If it doesn't find what it needs there, it looks in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="7be3e-121">Tenga en cuenta que cualquier código que intente escribir en el registro en el equipo del usuario puede escribir en el \_ subárbol de la máquina local HKEY \_ solo si el usuario actual tiene privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="7be3e-121">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="7be3e-122">Para escribir información sobre el formato de archivo personalizado en el \_ \_ subárbol HKEY local Machine, cree la siguiente subclave.</span><span class="sxs-lookup"><span data-stu-id="7be3e-122">To write information about your custom file format to the HKEY\_LOCAL\_MACHINE subtree, create the following subkey.</span></span>

<span data-ttu-id="7be3e-123">**HKEY \_ \_Software de equipo local \\ \\ Microsoft \\ multimedia \\ WMPlayer \\ extensions \\** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="7be3e-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="7be3e-124">donde *customExtension* es la extensión de nombre de archivo, incluido el separador de puntos (.).</span><span class="sxs-lookup"><span data-stu-id="7be3e-124">where *customExtension* is the file name extension including the dot (.) separator.</span></span> <span data-ttu-id="7be3e-125">Por ejemplo, si la extensión del formato de archivo personalizado es. XYZ, cree la subclave siguiente.</span><span class="sxs-lookup"><span data-stu-id="7be3e-125">For example, if the extension for your custom file format is .xyz, create the following subkey.</span></span>

<span data-ttu-id="7be3e-126">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimedia \\ WMPlayer \\ extensions \\ . XYZ**</span><span class="sxs-lookup"><span data-stu-id="7be3e-126">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz**</span></span>

<span data-ttu-id="7be3e-127">Para escribir información sobre el formato de archivo personalizado en el \_ \_ subárbol HKEY current user, cree la siguiente subclave.</span><span class="sxs-lookup"><span data-stu-id="7be3e-127">To write information about your custom file format to the HKEY\_CURRENT\_USER subtree, create the following subkey.</span></span>

<span data-ttu-id="7be3e-128">**HKEY \_ \_Software de usuario actual \\ \\ Microsoft \\ MediaPlayer \\ Player \\ extensions \\** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="7be3e-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="7be3e-129">Puede escribir una o varias de las entradas siguientes en la subclave *customExtension* .</span><span class="sxs-lookup"><span data-stu-id="7be3e-129">You can write one or more of the following entries in your *customExtension* subkey.</span></span>

-   <span data-ttu-id="7be3e-130">**Permisos**</span><span class="sxs-lookup"><span data-stu-id="7be3e-130">**Permissions**</span></span>
-   <span data-ttu-id="7be3e-131">**Tiempo de ejecución**</span><span class="sxs-lookup"><span data-stu-id="7be3e-131">**Runtime**</span></span>
-   <span data-ttu-id="7be3e-132">**FormatCode**</span><span class="sxs-lookup"><span data-stu-id="7be3e-132">**FormatCode**</span></span>

<span data-ttu-id="7be3e-133">Para especificar los complementos de conversión para el formato de archivo multimedia personalizado, cree una subclave **ConvertPluginCLSID** en la subclave *customExtension* .</span><span class="sxs-lookup"><span data-stu-id="7be3e-133">To specify conversion plug-ins for your custom media file format, create a **ConvertPluginCLSID** subkey in your *customExtension* subkey.</span></span>

<span data-ttu-id="7be3e-134">Para especificar dónde debe mostrar Windows Media Player los archivos en la vista biblioteca, escriba una entrada que represente el formato de archivo personalizado en la subclave siguiente.</span><span class="sxs-lookup"><span data-stu-id="7be3e-134">To specify where Windows Media Player should display your files in its library view, write an entry that represents your custom file format in the following subkey.</span></span>

<span data-ttu-id="7be3e-135">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ extensions**</span><span class="sxs-lookup"><span data-stu-id="7be3e-135">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="7be3e-136">En los temas siguientes se describen las subclaves del registro y las entradas que proporcionan a Windows Media Player información sobre los formatos de archivo multimedia personalizados.</span><span class="sxs-lookup"><span data-stu-id="7be3e-136">The following topics describe the registry subkeys and entries that provide Windows Media Player with information about custom media file formats.</span></span>

-   [<span data-ttu-id="7be3e-137">Entrada del registro de permisos</span><span class="sxs-lookup"><span data-stu-id="7be3e-137">Permissions Registry Entry</span></span>](permissions-registry-entry.md)
-   [<span data-ttu-id="7be3e-138">Entrada del registro en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="7be3e-138">Runtime Registry Entry</span></span>](runtime-registry-entry.md)
-   [<span data-ttu-id="7be3e-139">Entrada del registro FormatCode</span><span class="sxs-lookup"><span data-stu-id="7be3e-139">FormatCode Registry Entry</span></span>](formatcode-registry-entry.md)
-   [<span data-ttu-id="7be3e-140">Entradas del registro de clasificación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="7be3e-140">Library Classification Registry Entries</span></span>](library-classification-registry-entries.md)
-   [<span data-ttu-id="7be3e-141">Subclave ConvertPluginCLSID</span><span class="sxs-lookup"><span data-stu-id="7be3e-141">ConvertPluginCLSID Subkey</span></span>](convertpluginclsid-subkey.md)

## <a name="related-topics"></a><span data-ttu-id="7be3e-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7be3e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7be3e-143">**Configuración del registro**</span><span class="sxs-lookup"><span data-stu-id="7be3e-143">**Registry Settings**</span></span>](registry-settings.md)
</dt> <dt>

[<span data-ttu-id="7be3e-144">**Complementos de conversión de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="7be3e-144">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 





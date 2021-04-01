---
title: Subclave ConvertPluginCLSID
description: Subclave ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Media Player de Windows, subclave ConvertPluginCLSID
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- Registry, subclave ConvertPluginCLSID
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- Subclave ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075815"
---
# <a name="convertpluginclsid-subkey"></a><span data-ttu-id="40b8f-111">Subclave ConvertPluginCLSID</span><span class="sxs-lookup"><span data-stu-id="40b8f-111">ConvertPluginCLSID Subkey</span></span>

<span data-ttu-id="40b8f-112">Cuando Windows Media Player 11 encuentra una extensión de nombre de archivo personalizada, busca una subclave del registro que coincida con la extensión.</span><span class="sxs-lookup"><span data-stu-id="40b8f-112">When Windows Media Player 11 encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="40b8f-113">La subclave se describe en [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="40b8f-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="40b8f-114">En algunos casos, la subclave de la extensión tiene una subclave denominada **ConvertPluginCLSID**.</span><span class="sxs-lookup"><span data-stu-id="40b8f-114">In some cases, the extension's subkey has a subkey named **ConvertPluginCLSID**.</span></span>

<span data-ttu-id="40b8f-115">Por ejemplo, supongamos que ha creado un formato de archivo personalizado (con la extensión de nombre de archivo. XYZ) y un complemento de conversión que convierte los archivos a un formato compatible con Windows Media Player, a continuación, almacenaría el ID. de clase del complemento en una o las dos subclaves siguientes.</span><span class="sxs-lookup"><span data-stu-id="40b8f-115">For example, suppose you have created a custom file format (with file name extension .xyz) and a conversion plug-in that converts the files to a format supported by Windows Media Player Then you would store the class ID of the plug-in in one or both of the following subkeys.</span></span>

<span data-ttu-id="40b8f-116">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimedia \\ WMPlayer \\ extensions \\ . XYZ \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="40b8f-116">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="40b8f-117">**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ extensions \\ . XYZ \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="40b8f-117">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="40b8f-118">La subclave **ConvertPluginCLSID** especifica los identificadores de clase de los complementos que Windows Media Player puede usar para convertir un archivo multimedia de su formato personalizado a un formato compatible con el reproductor.</span><span class="sxs-lookup"><span data-stu-id="40b8f-118">The **ConvertPluginCLSID** subkey specifies the class IDs of plug-ins that Windows Media Player can use to convert a media file from its custom format to a format supported by the Player.</span></span>

<span data-ttu-id="40b8f-119">La subclave **ConvertPluginCLSID** tiene las siguientes entradas.</span><span class="sxs-lookup"><span data-stu-id="40b8f-119">The **ConvertPluginCLSID** subkey has the following entries.</span></span>

-   <span data-ttu-id="40b8f-120">Entrada predeterminada que representa el complemento de conversión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="40b8f-120">A default entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="40b8f-121">Una entrada con nombre que representa el complemento de conversión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="40b8f-121">A named entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="40b8f-122">Entradas con nombre adicionales que representan complementos de conversión alternativos.</span><span class="sxs-lookup"><span data-stu-id="40b8f-122">Additional named entries that represent alternate conversion plug-ins.</span></span>

<span data-ttu-id="40b8f-123">Por ejemplo, supongamos que un formato de archivo personalizado tiene un complemento de conversión predeterminado y dos complementos de conversión alternativos. Las entradas del registro bajo la subclave **ConvertPluginCLSID** tendrían el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="40b8f-123">For example, suppose a custom file format has a default conversion plug-in and two alternate conversion plug-ins. The registry entries under the **ConvertPluginCLSID** subkey would have the following form.</span></span>



| <span data-ttu-id="40b8f-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="40b8f-124">Name</span></span>                                                                          | <span data-ttu-id="40b8f-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="40b8f-125">Type</span></span>        | <span data-ttu-id="40b8f-126">Value</span><span class="sxs-lookup"><span data-stu-id="40b8f-126">Value</span></span>                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="40b8f-127">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="40b8f-127">Default</span></span>                                                                       | <span data-ttu-id="40b8f-128">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="40b8f-128">**REG\_SZ**</span></span> | <span data-ttu-id="40b8f-129">IDENTIFICADOR de clase, en formato de registro, del complemento de conversión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="40b8f-129">The class ID, in registry format, of the default conversion plug-in.</span></span> |
| <span data-ttu-id="40b8f-130">IDENTIFICADOR de clase, en formato de registro, del complemento de conversión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="40b8f-130">The class ID, in registry format, of the default conversion plug-in.</span></span>          | <span data-ttu-id="40b8f-131">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="40b8f-131">**REG\_SZ**</span></span> | <span data-ttu-id="40b8f-132">Nombre descriptivo del complemento de conversión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="40b8f-132">The friendly name of the default conversion plug-in.</span></span>                 |
| <span data-ttu-id="40b8f-133">IDENTIFICADOR de clase, en formato de registro, del primer complemento de conversión alternativo.</span><span class="sxs-lookup"><span data-stu-id="40b8f-133">The class ID, in registry format, of the first alternate conversion plug-in.</span></span>  | <span data-ttu-id="40b8f-134">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="40b8f-134">**REG\_SZ**</span></span> | <span data-ttu-id="40b8f-135">Nombre descriptivo del primer complemento de conversión alternativo.</span><span class="sxs-lookup"><span data-stu-id="40b8f-135">The friendly name of the first alternate conversion plug-in.</span></span>         |
| <span data-ttu-id="40b8f-136">IDENTIFICADOR de clase, en formato de registro, del segundo complemento de conversión alternativo.</span><span class="sxs-lookup"><span data-stu-id="40b8f-136">The class ID, in registry format, of the second alternate conversion plug-in.</span></span> | <span data-ttu-id="40b8f-137">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="40b8f-137">**REG\_SZ**</span></span> | <span data-ttu-id="40b8f-138">Nombre descriptivo del segundo complemento de conversión alternativo.</span><span class="sxs-lookup"><span data-stu-id="40b8f-138">The friendly name of the second alternate conversion plug-in.</span></span>        |



 

<span data-ttu-id="40b8f-139">Tenga en cuenta que el complemento de conversión predeterminado se representa mediante dos entradas del registro: la entrada predeterminada y una entrada con nombre.</span><span class="sxs-lookup"><span data-stu-id="40b8f-139">Note that the default conversion plug-in is represented by two registry entries: the default entry and a named entry.</span></span> <span data-ttu-id="40b8f-140">Windows Media Player usa la entrada predeterminada para determinar qué complemento es el complemento de conversión predeterminado (principal).</span><span class="sxs-lookup"><span data-stu-id="40b8f-140">Windows Media Player uses the default entry to determine which plug-in is the default (primary) conversion plug-in.</span></span> <span data-ttu-id="40b8f-141">Windows Media Player usa las entradas con nombre para obtener nombres descriptivos para todos los complementos de conversión, incluido el complemento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="40b8f-141">Windows Media Player uses the named entries to obtain friendly names for all conversion plug-ins, including the default plug-in.</span></span>

<span data-ttu-id="40b8f-142">El nombre descriptivo de un complemento de conversión viene determinado por la empresa que crea el complemento.</span><span class="sxs-lookup"><span data-stu-id="40b8f-142">The friendly name of a conversion plug-in is determined by the company that creates the plug-in.</span></span> <span data-ttu-id="40b8f-143">Windows Media Player podría mostrar el nombre descriptivo en su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="40b8f-143">Windows Media Player might display the friendly name in its user interface.</span></span>

<span data-ttu-id="40b8f-144">Cuando Windows Media Player intenta convertir un archivo de un formato personalizado a un formato estándar, carga primero el complemento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="40b8f-144">When Windows Media Player attempts to convert a file from a custom format to a standard format, it first loads the default plug-in.</span></span> <span data-ttu-id="40b8f-145">Si el complemento predeterminado no puede convertir el archivo y devuelve el complemento NS \_ E \_ WMP \_ Convert \_ el \_ \_ archivo desconocido \_ , el reproductor carga cada complemento alternativo hasta que se produce una conversión correcta o no hay más complementos que probar.</span><span class="sxs-lookup"><span data-stu-id="40b8f-145">If the default plug-in fails to convert the file and returns NS\_E\_WMP\_CONVERT\_PLUGIN\_UNKNOWN\_FILE\_OWNER, the Player loads each alternate plug-in until a successful conversion happens or there are no more plug-ins to try.</span></span> <span data-ttu-id="40b8f-146">El reproductor no muestra un mensaje de advertencia si no se encuentra ningún complemento de conversión para la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="40b8f-146">The Player does not display a warning message if no conversion plug-in is found for the file name extension.</span></span>

<span data-ttu-id="40b8f-147">La entrada del registro **ConvertPluginCLSID** es compatible con Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="40b8f-147">The **ConvertPluginCLSID** registry entry is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40b8f-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40b8f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b8f-149">**Configuración del registro de la extensión de nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="40b8f-149">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> <dt>

[<span data-ttu-id="40b8f-150">**Complementos de conversión de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="40b8f-150">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 





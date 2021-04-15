---
title: Acerca del modelo de objetos de Player
description: Acerca del modelo de objetos de Player
ms.assetid: 41a9cbce-b982-4377-a0ee-b0ca735954f5
keywords:
- Media Player de Windows, modelo de objetos
- Modelo de objetos de Windows Media Player, acerca de
- modelo de objetos, acerca de
- Control ActiveX de Windows Media Player, modelo de objetos
- Control ActiveX, modelo de objetos
- Control ActiveX móvil de Windows Media Player, modelo de objetos
- Windows Media Player Mobile, modelo de objetos
- Kit de desarrollo de software (SDK), modelo de objetos de controles ActiveX de Windows Media Player
- SDK (kit de desarrollo de software), modelo de objetos de controles ActiveX de Windows Media Player
- documentación, modelo de objetos de controles ActiveX de Windows Media Player
- Objeto Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a0ded1f25d8d08bd9e588b5384a171698d2ea2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695346"
---
# <a name="about-the-player-object-model"></a><span data-ttu-id="6943a-114">Acerca del modelo de objetos de Player</span><span class="sxs-lookup"><span data-stu-id="6943a-114">About the Player Object Model</span></span>

<span data-ttu-id="6943a-115">El control Media Player de Microsoft Windows es un control ActiveX estándar que utiliza la tecnología del modelo de objetos componentes (COM) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6943a-115">The Microsoft Windows Media Player control is a standard ActiveX control that uses Microsoft Component Object Model (COM) technology.</span></span> <span data-ttu-id="6943a-116">La funcionalidad de Windows Media Player se ha dipuesto en un conjunto de interfaces de programación que sigue las directrices estándar de COM.</span><span class="sxs-lookup"><span data-stu-id="6943a-116">The Windows Media Player functionality is distilled into a set of programming interfaces that follows standard COM guidelines.</span></span> <span data-ttu-id="6943a-117">Puede programar estas interfaces en una página web HTML estándar mediante el modelo de objetos de control de reproductor con Microsoft JScript o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="6943a-117">You can program these interfaces on a standard HTML webpage using the Player control object model with Microsoft JScript or Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="6943a-118">También puede programarlos en máscaras mediante Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="6943a-118">You can also program them in skins by using Microsoft JScript.</span></span> <span data-ttu-id="6943a-119">Si desea crear un programa personalizado que incruste el control, puede usar uno de varios lenguajes, entre los que se incluyen Visual Basic, C++ y C#.</span><span class="sxs-lookup"><span data-stu-id="6943a-119">If you want to create a custom program that embeds the control, you can use one of several languages, including Visual Basic, C++, and C#.</span></span>

<span data-ttu-id="6943a-120">El control ActiveX de Windows Media Player se instala con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6943a-120">The Windows Media Player ActiveX control is installed with Windows Media Player.</span></span> <span data-ttu-id="6943a-121">El control Player no se instala con el SDK de Media Player de Windows y no se puede redistribuir por separado.</span><span class="sxs-lookup"><span data-stu-id="6943a-121">The Player control is not installed with the Windows Media Player SDK and cannot be redistributed separately.</span></span> <span data-ttu-id="6943a-122">Las características específicas disponibles para el código dependen de la versión de Windows Media Player que tenga instalado el usuario.</span><span class="sxs-lookup"><span data-stu-id="6943a-122">The particular features available to your code depend on which version of Windows Media Player the user has installed.</span></span> <span data-ttu-id="6943a-123">La [Referencia del modelo de objetos para scripting](object-model-reference-for-scripting.md) y [Referencia del modelo de objetos para C++](object-model-reference-for-c.md) incluyen información sobre los requisitos de versión de cada propiedad, método y evento.</span><span class="sxs-lookup"><span data-stu-id="6943a-123">The [Object Model Reference for Scripting](object-model-reference-for-scripting.md) and [Object Model Reference for C++](object-model-reference-for-c.md) include version requirement information for each property, method, and event.</span></span>

<span data-ttu-id="6943a-124">En las secciones siguientes se proporciona información general sobre el modelo de objetos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6943a-124">The following sections provide overview information about the Windows Media Player object model.</span></span>



| <span data-ttu-id="6943a-125">Sección</span><span class="sxs-lookup"><span data-stu-id="6943a-125">Section</span></span>                                                                                        | <span data-ttu-id="6943a-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="6943a-126">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6943a-127">Modelo de objetos del reproductor para lenguajes de scripting</span><span class="sxs-lookup"><span data-stu-id="6943a-127">Player Object Model for Scripting Languages</span></span>](player-object-model-for-scripting-languages.md) | <span data-ttu-id="6943a-128">En esta sección se describen los objetos disponibles en el modelo de objetos de.</span><span class="sxs-lookup"><span data-stu-id="6943a-128">This section describes the objects available in the object model.</span></span>                                                                                             |
| [<span data-ttu-id="6943a-129">Acerca de las versiones del modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="6943a-129">About the Object Model Versions</span></span>](about-the-object-model-versions.md)                         | <span data-ttu-id="6943a-130">En esta sección se detallan los elementos del modelo de objetos que se han agregado en cada versión desde la introducción de Windows Media Player 7,0.</span><span class="sxs-lookup"><span data-stu-id="6943a-130">This section details which object model items have been added in each version since the introduction of Windows Media Player 7.0.</span></span>                             |
| [<span data-ttu-id="6943a-131">Propiedades, métodos y eventos</span><span class="sxs-lookup"><span data-stu-id="6943a-131">Properties, Methods, and Events</span></span>](properties--methods-and-events.md)                          | <span data-ttu-id="6943a-132">En esta sección se explican las propiedades, los métodos y los eventos.</span><span class="sxs-lookup"><span data-stu-id="6943a-132">This section explains properties, methods, and events.</span></span>                                                                                                        |
| [<span data-ttu-id="6943a-133">Tipos de archivos y protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="6943a-133">Supported Protocols and File Types</span></span>](supported-protocols-and-file-types.md)                   | <span data-ttu-id="6943a-134">En esta sección se enumeran los protocolos y tipos de archivo compatibles con Windows Media Player y el modelo de objetos de control de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6943a-134">This section lists the protocols and file types supported by Windows Media Player and the Windows Media Player control object model.</span></span>                          |
| [<span data-ttu-id="6943a-135">Acerca de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="6943a-135">About the Library</span></span>](about-the-library.md)                                                     | <span data-ttu-id="6943a-136">En esta sección se describe la biblioteca de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="6943a-136">This section describes the Windows Media Player library.</span></span>                                                                                                      |
| [<span data-ttu-id="6943a-137">Usar HTML con Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="6943a-137">Using HTML with Windows Media Player</span></span>](using-html-with-windows-media-player.md)               | <span data-ttu-id="6943a-138">En esta sección se describen las distintas formas de hacer que Windows Media Player y HTML funcionen juntos.</span><span class="sxs-lookup"><span data-stu-id="6943a-138">This section describes the various ways to make Windows Media Player and HTML work together.</span></span>                                                                  |
| [<span data-ttu-id="6943a-139">Incrustar el control Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="6943a-139">Embedding the Windows Media Player Control</span></span>](embedding-the-windows-media-player-control.md)   | <span data-ttu-id="6943a-140">En esta sección se describen las distintas formas de insertar el control de Media Player de Windows en Microsoft Office documentos y en programas personalizados.</span><span class="sxs-lookup"><span data-stu-id="6943a-140">This section describes the various ways to embed the Windows Media Player control in Microsoft Office documents and in custom programs.</span></span>                       |
| [<span data-ttu-id="6943a-141">Acerca de la sincronización de dispositivos</span><span class="sxs-lookup"><span data-stu-id="6943a-141">About Device Synchronization</span></span>](about-device-synchronization.md)                               | <span data-ttu-id="6943a-142">En esta sección se describe la funcionalidad proporcionada por el control Windows Media Player 10 o posterior para transferir contenido multimedia digital a dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="6943a-142">This section describes the functionality provided by the Windows Media Player 10 or later control for transferring digital media content to portable devices.</span></span> |
| [<span data-ttu-id="6943a-143">Acerca de la grabación de CD</span><span class="sxs-lookup"><span data-stu-id="6943a-143">About CD Burning</span></span>](about-cd-burning.md)                                                       | <span data-ttu-id="6943a-144">En esta sección se describe la funcionalidad proporcionada por el control de Media Player de Windows para crear CDs.</span><span class="sxs-lookup"><span data-stu-id="6943a-144">This section describes the functionality provided by the Windows Media Player control for creating CDs.</span></span>                                                       |
| [<span data-ttu-id="6943a-145">Acerca de la copia de CD</span><span class="sxs-lookup"><span data-stu-id="6943a-145">About CD Ripping</span></span>](about-cd-ripping.md)                                                       | <span data-ttu-id="6943a-146">En esta sección se describe la funcionalidad proporcionada por el control Media Player de Windows para copiar pistas desde CDs de audio al equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="6943a-146">This section describes the functionality provided by the Windows Media Player control for copying tracks from audio CDs to the user's computer.</span></span>               |
| [<span data-ttu-id="6943a-147">Acerca de la supervisión de carpetas</span><span class="sxs-lookup"><span data-stu-id="6943a-147">About Folder Monitoring</span></span>](about-folder-monitoring.md)                                         | <span data-ttu-id="6943a-148">En esta sección se describe la funcionalidad proporcionada por el control de Media Player de Windows para controlar los procesos de supervisión de carpetas del reproductor.</span><span class="sxs-lookup"><span data-stu-id="6943a-148">This section describes the functionality provided by the Windows Media Player control for controlling the Player's folder monitoring processes.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="6943a-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6943a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6943a-150">**Modelo de objetos de Media Player de Windows**</span><span class="sxs-lookup"><span data-stu-id="6943a-150">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 





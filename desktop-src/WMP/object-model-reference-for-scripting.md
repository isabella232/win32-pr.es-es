---
title: Referencia del modelo de objetos para scripting
description: Referencia del modelo de objetos para scripting
ms.assetid: a900fd55-2213-46db-84ad-93f199c60182
keywords:
- Media Player de Windows, modelo de objetos
- Windows Media Player Mobile, modelo de objetos
- Modelo de objetos de Windows Media Player, referencia
- modelo de objetos, referencia
- Control ActiveX, referencia
- Control ActiveX de Windows Media Player, referencia
- Control ActiveX móvil de Windows Media Player, referencia
- Referencia del modelo de objetos, scripting
- Windows Media Player, referencia de scripting
- Windows Media Player Mobile, referencia de scripting
- Modelo de objetos de Windows Media Player, referencia de scripting
- modelo de objetos, referencia de scripts
- Control ActiveX de Windows Media Player, referencia de scripting
- Control ActiveX móvil de Windows Media Player, referencia de scripting
- Control ActiveX, referencia de scripting
- Referencia del modelo de objetos de scripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f20e5bacf6a1fd93579ce40e8957b7ce7aefae0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695432"
---
# <a name="object-model-reference-for-scripting"></a><span data-ttu-id="2de78-119">Referencia del modelo de objetos para scripting</span><span class="sxs-lookup"><span data-stu-id="2de78-119">Object Model Reference for Scripting</span></span>

<span data-ttu-id="2de78-120">La referencia del modelo de objetos para scripting contiene información detallada sobre el modelo de objetos de control ActiveX de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2de78-120">The object model reference for scripting contains detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="2de78-121">La información de esta sección se presenta en un estilo diseñado para su uso con lenguajes de scripts como Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="2de78-121">The information in this section is presented in a style designed for use with script languages like Microsoft JScript.</span></span>

> [!Note]  
> <span data-ttu-id="2de78-122">Todos los métodos, propiedades y eventos son totalmente compatibles con Windows Media Player 10 Mobile o posterior, a menos que se indique explícitamente lo contrario.</span><span class="sxs-lookup"><span data-stu-id="2de78-122">All methods, properties, and events are fully supported in Windows Media Player 10 Mobile or later unless explicitly stated otherwise.</span></span>

 

<span data-ttu-id="2de78-123">La referencia del modelo de objetos para scripting contiene documentación para los siguientes objetos y sus métodos, propiedades y eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="2de78-123">The object model reference for scripting contains documentation for the following objects and their associated methods, properties, and events.</span></span>



| <span data-ttu-id="2de78-124">Object</span><span class="sxs-lookup"><span data-stu-id="2de78-124">Object</span></span>                                              | <span data-ttu-id="2de78-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="2de78-125">Description</span></span>                                                                                                                                                                                    |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2de78-126">-</span><span class="sxs-lookup"><span data-stu-id="2de78-126">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="2de78-127">Métodos y propiedades para tener acceso a un CD o DVD en su unidad.</span><span class="sxs-lookup"><span data-stu-id="2de78-127">Methods and properties for accessing a CD or DVD in its drive.</span></span>                                                                                                                                 |
| [<span data-ttu-id="2de78-128">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="2de78-128">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="2de78-129">Métodos y propiedades para tener acceso a una colección de unidades de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="2de78-129">Methods and properties for accessing a collection of CD or DVD drives.</span></span>                                                                                                                         |
| [<span data-ttu-id="2de78-130">ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="2de78-130">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="2de78-131">Propiedades para incluir leyendas con un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="2de78-131">Properties for including captions with a media item.</span></span>                                                                                                                                           |
| [<span data-ttu-id="2de78-132">Controles</span><span class="sxs-lookup"><span data-stu-id="2de78-132">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="2de78-133">Métodos y propiedades que representan los controles de transporte de Windows Media Player, como reproducir, detener y pausar.</span><span class="sxs-lookup"><span data-stu-id="2de78-133">Methods and properties representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>                                                                             |
| [<span data-ttu-id="2de78-134">DISCOS</span><span class="sxs-lookup"><span data-stu-id="2de78-134">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="2de78-135">Propiedad, métodos y eventos para trabajar con DVDs.</span><span class="sxs-lookup"><span data-stu-id="2de78-135">A property, methods, and events for working with DVDs.</span></span>                                                                                                                                         |
| [<span data-ttu-id="2de78-136">Error</span><span class="sxs-lookup"><span data-stu-id="2de78-136">Error</span></span>](error-object.md)                           | <span data-ttu-id="2de78-137">Métodos y propiedades que proporcionan acceso a una colección de objetos **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="2de78-137">Methods and properties providing access to a collection of **ErrorItem** objects.</span></span>                                                                                                              |
| [<span data-ttu-id="2de78-138">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="2de78-138">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="2de78-139">Propiedades que proporcionan información sobre los errores.</span><span class="sxs-lookup"><span data-stu-id="2de78-139">Properties that provide information about errors.</span></span>                                                                                                                                              |
| [<span data-ttu-id="2de78-140">Elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="2de78-140">Media</span></span>](media-object.md)                           | <span data-ttu-id="2de78-141">Métodos y propiedades relacionados con elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="2de78-141">Methods and properties relating to media items.</span></span>                                                                                                                                                |
| [<span data-ttu-id="2de78-142">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="2de78-142">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="2de78-143">Métodos que proporcionan acceso a una colección de objetos **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="2de78-143">Methods that provide access to a collection of **Media** objects.</span></span>                                                                                                                              |
| [<span data-ttu-id="2de78-144">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="2de78-144">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="2de78-145">Propiedades para recuperar información sobre los valores de imagen del atributo de metadatos de **WM/imagen** .</span><span class="sxs-lookup"><span data-stu-id="2de78-145">Properties for retrieving information on the image values of the **WM/Picture** metadata attribute.</span></span>                                                                                            |
| [<span data-ttu-id="2de78-146">MetadataText</span><span class="sxs-lookup"><span data-stu-id="2de78-146">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="2de78-147">Propiedades para recuperar los metadatos de los atributos de metadatos de texto complejos.</span><span class="sxs-lookup"><span data-stu-id="2de78-147">Properties for retrieving metadata for complex textual metadata attributes.</span></span>                                                                                                                    |
| [<span data-ttu-id="2de78-148">Network</span><span class="sxs-lookup"><span data-stu-id="2de78-148">Network</span></span>](network-object.md)                       | <span data-ttu-id="2de78-149">Propiedades relacionadas con la conexión de red de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2de78-149">Properties relating to the network connection of Windows Media Player.</span></span>                                                                                                                         |
| [<span data-ttu-id="2de78-150">Reproductor</span><span class="sxs-lookup"><span data-stu-id="2de78-150">Player</span></span>](player-object.md)                         | <span data-ttu-id="2de78-151">Métodos, propiedades y eventos a los que se puede programar Windows Media Player para que respondan.</span><span class="sxs-lookup"><span data-stu-id="2de78-151">Methods, properties, and events that Windows Media Player can be programmed to respond to.</span></span>                                                                                                     |
| [<span data-ttu-id="2de78-152">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="2de78-152">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="2de78-153">Métodos y propiedades para cambiar entre un control de Windows Media Player remoto y el modo completo del reproductor.</span><span class="sxs-lookup"><span data-stu-id="2de78-153">Methods and properties for switching between a remoted Windows Media Player control and the full mode of the Player.</span></span> <span data-ttu-id="2de78-154">Solo se puede utilizar con programas de C++ que incrustan el control en modo remoto.</span><span class="sxs-lookup"><span data-stu-id="2de78-154">Can only be used with C++ programs that embed the control in remote mode.</span></span> |
| [<span data-ttu-id="2de78-155">Lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="2de78-155">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="2de78-156">Métodos y propiedades para manipular listas de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="2de78-156">Methods and properties for manipulating lists of media items.</span></span>                                                                                                                                  |
| [<span data-ttu-id="2de78-157">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="2de78-157">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="2de78-158">Un método y una propiedad para tener acceso a una colección de objetos de **lista de reproducción** por número de índice.</span><span class="sxs-lookup"><span data-stu-id="2de78-158">A method and a property for accessing a collection of **Playlist** objects by index number.</span></span>                                                                                                    |
| [<span data-ttu-id="2de78-159">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="2de78-159">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="2de78-160">Métodos para organizar una colección de objetos de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="2de78-160">Methods for organizing a collection of **Playlist** objects.</span></span>                                                                                                                                   |
| [<span data-ttu-id="2de78-161">Consultar</span><span class="sxs-lookup"><span data-stu-id="2de78-161">Query</span></span>](query-object.md)                           | <span data-ttu-id="2de78-162">Métodos para modificar una consulta compuesta.</span><span class="sxs-lookup"><span data-stu-id="2de78-162">Methods for modifying a compound query.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="2de78-163">Configuración</span><span class="sxs-lookup"><span data-stu-id="2de78-163">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="2de78-164">Propiedades que permiten la especificación o recuperación de la configuración de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2de78-164">Properties that allow the specification or retrieval of Windows Media Player settings.</span></span>                                                                                                         |
| [<span data-ttu-id="2de78-165">StringCollection</span><span class="sxs-lookup"><span data-stu-id="2de78-165">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="2de78-166">Un método y una propiedad para manipular colecciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="2de78-166">A method and a property for manipulating collections of strings.</span></span>                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="2de78-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2de78-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2de78-168">**Referencia del modelo de objetos de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="2de78-168">**Windows Media Player Object Model Reference**</span></span>](windows-media-player-object-model-reference.md)
</dt> </dl>

 

 





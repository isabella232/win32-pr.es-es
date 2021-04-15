---
title: Modelo de objetos del reproductor para lenguajes de scripting
description: Modelo de objetos del reproductor para lenguajes de scripting
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
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
- Windows Media Player, lenguajes de scripting
- Modelo de objetos de Windows Media Player, lenguajes de scripting
- modelo de objetos, lenguajes de scripting
- Control ActiveX de Windows Media Player, lenguajes de scripting
- Control ActiveX, lenguajes de scripting
- Control ActiveX móvil de Windows Media Player, lenguajes de scripting
- Windows Media Player Mobile, lenguajes de scripting
- lenguajes de scripting
- Media Player de Windows, objeto Player
- Modelo de objetos de Windows Media Player, objeto Player
- modelo de objetos, objeto Player
- Control ActiveX de Windows Media Player, objeto Player
- Control ActiveX, objeto Player
- Control ActiveX móvil de Windows Media Player, objeto Player
- Windows Media Player Mobile, objeto Player
- Objeto Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104568865"
---
# <a name="player-object-model-for-scripting-languages"></a><span data-ttu-id="3bcf0-129">Modelo de objetos del reproductor para lenguajes de scripting</span><span class="sxs-lookup"><span data-stu-id="3bcf0-129">Player Object Model for Scripting Languages</span></span>

<span data-ttu-id="3bcf0-130">ActiveX utiliza el concepto de objetos para contener la funcionalidad de programación.</span><span class="sxs-lookup"><span data-stu-id="3bcf0-130">ActiveX uses the concept of objects to contain programming functionality.</span></span> <span data-ttu-id="3bcf0-131">Windows Media Player utiliza varios objetos para dividir la funcionalidad que proporciona el control.</span><span class="sxs-lookup"><span data-stu-id="3bcf0-131">Windows Media Player uses several objects to divide up the functionality the control provides.</span></span> <span data-ttu-id="3bcf0-132">El objeto raíz es el objeto **Player** y los demás objetos se adjuntan al objeto **Player** a través de propiedades específicas.</span><span class="sxs-lookup"><span data-stu-id="3bcf0-132">The root object is the **Player** object, and the other objects are attached to the **Player** object through specific properties.</span></span>

<span data-ttu-id="3bcf0-133">En el diagrama siguiente se muestra cómo funciona el modelo de objetos de control ActiveX de Windows Media Player 11 para los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="3bcf0-133">The following diagram shows how the Windows Media Player 11 ActiveX control object model works for scripting languages.</span></span>

![diagrama del modelo de objetos del reproductor de Windows Media 11](images/playeromdiag.png)

<span data-ttu-id="3bcf0-135">En C++, y a veces en lenguajes .NET, los objetos se representan mediante interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="3bcf0-135">In C++, and sometimes in .NET languages, objects are represented by COM interfaces.</span></span> <span data-ttu-id="3bcf0-136">En el modelo de objetos de Windows Media Player, los nombres de interfaz COM son los mismos que el nombre de objeto, pero llevan el prefijo "IWMP".</span><span class="sxs-lookup"><span data-stu-id="3bcf0-136">In the Windows Media Player object model, COM interface names are the same as the object name, but are prefixed with "IWMP".</span></span> <span data-ttu-id="3bcf0-137">Por ejemplo, el objeto de **red** se expone a través de la interfaz **IWMPNetwork** .</span><span class="sxs-lookup"><span data-stu-id="3bcf0-137">For example, the **Network** object is exposed through the **IWMPNetwork** interface.</span></span>

<span data-ttu-id="3bcf0-138">En las secciones siguientes se proporcionan información general conceptual para cada objeto:</span><span class="sxs-lookup"><span data-stu-id="3bcf0-138">The following sections provide conceptual overviews for each object:</span></span>

-   [<span data-ttu-id="3bcf0-139">Acerca de los objetos CDROM y CdromCollection</span><span class="sxs-lookup"><span data-stu-id="3bcf0-139">About the Cdrom and CdromCollection Objects</span></span>](about-the-cdrom-and-cdromcollection-objects.md)
-   [<span data-ttu-id="3bcf0-140">Acerca del objeto ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="3bcf0-140">About the ClosedCaption Object</span></span>](about-the-closedcaption-object.md)
-   [<span data-ttu-id="3bcf0-141">Acerca del objeto Controls</span><span class="sxs-lookup"><span data-stu-id="3bcf0-141">About the Controls Object</span></span>](about-the-controls-object.md)
-   [<span data-ttu-id="3bcf0-142">Acerca del objeto de DVD</span><span class="sxs-lookup"><span data-stu-id="3bcf0-142">About the DVD Object</span></span>](about-the-dvd-object.md)
-   [<span data-ttu-id="3bcf0-143">Acerca de los objetos error y ErrorItem</span><span class="sxs-lookup"><span data-stu-id="3bcf0-143">About the Error and ErrorItem Objects</span></span>](about-the-error-and-erroritem-objects.md)
-   [<span data-ttu-id="3bcf0-144">Acerca de los objetos MediaCollection y multimedia</span><span class="sxs-lookup"><span data-stu-id="3bcf0-144">About the MediaCollection and Media Objects</span></span>](about-the-mediacollection-and-media-objects.md)
-   [<span data-ttu-id="3bcf0-145">Acerca del objeto MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="3bcf0-145">About the MetadataPicture Object</span></span>](about-the-metadatapicture-object.md)
-   [<span data-ttu-id="3bcf0-146">Acerca del objeto MetadataText</span><span class="sxs-lookup"><span data-stu-id="3bcf0-146">About the MetadataText Object</span></span>](about-the-metadatatext-object.md)
-   [<span data-ttu-id="3bcf0-147">Acerca del objeto de red</span><span class="sxs-lookup"><span data-stu-id="3bcf0-147">About the Network Object</span></span>](about-the-network-object.md)
-   [<span data-ttu-id="3bcf0-148">Acerca del objeto Player</span><span class="sxs-lookup"><span data-stu-id="3bcf0-148">About the Player Object</span></span>](about-the-player-object.md)
-   [<span data-ttu-id="3bcf0-149">Acerca del objeto PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="3bcf0-149">About the PlayerApplication Object</span></span>](about-the-playerapplication-object.md)
-   [<span data-ttu-id="3bcf0-150">Acerca de los objetos playlist, PlaylistCollection y PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="3bcf0-150">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [<span data-ttu-id="3bcf0-151">Acerca del objeto de consulta</span><span class="sxs-lookup"><span data-stu-id="3bcf0-151">About the Query Object</span></span>](about-the-query-object.md)
-   [<span data-ttu-id="3bcf0-152">Acerca del objeto de configuración</span><span class="sxs-lookup"><span data-stu-id="3bcf0-152">About the Settings Object</span></span>](about-the-settings-object.md)
-   [<span data-ttu-id="3bcf0-153">Acerca del objeto StringCollection</span><span class="sxs-lookup"><span data-stu-id="3bcf0-153">About the StringCollection Object</span></span>](about-the-stringcollection-object.md)

<span data-ttu-id="3bcf0-154">Hay funcionalidad adicional disponible a través de ciertas interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="3bcf0-154">Additional functionality is available through certain COM interfaces.</span></span> <span data-ttu-id="3bcf0-155">El acceso a estas interfaces puede depender del lenguaje que se use para programar y otros factores, como el modo utilizado para crear la instancia del control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="3bcf0-155">Whether you can access these interfaces may depend on the language you use for programming and other factors, such as the mode used to create the instance of the Windows Media Player control.</span></span> <span data-ttu-id="3bcf0-156">Para obtener una lista completa de las interfaces COM que expone el control Media Player de Windows, vea la [Referencia del modelo de objetos de C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="3bcf0-156">For a complete list of COM interfaces exposed by the Windows Media Player control, see the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bcf0-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3bcf0-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bcf0-158">**Acerca del modelo de objetos de Player**</span><span class="sxs-lookup"><span data-stu-id="3bcf0-158">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="3bcf0-159">**Usar el control de Media Player de Windows en una solución de .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="3bcf0-159">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 





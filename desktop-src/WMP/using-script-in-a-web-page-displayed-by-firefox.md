---
title: Uso de scripts en una página web que se muestra en Firefox
description: Uso de scripts en una página web que se muestra en Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX, páginas web
- Control ActiveX de Windows Media Player, ejemplo de scripting
- Control ActiveX móvil de Windows Media Player, ejemplo de scripting
- Control ActiveX, ejemplo de scripting
- incrustación, páginas web
- Incrustación de páginas web, ejemplo de scripting
- Windows Media Player, Firefox
- Modelo de objetos de Windows Media Player, Firefox
- modelo de objetos, Firefox
- Windows Media Player Mobile, Firefox
- Control ActiveX de Windows Media Player, Firefox
- Control ActiveX móvil de Windows Media Player, Firefox
- Control ActiveX, Firefox
- Firefox, ejemplo de scripting
- Incrustación de páginas web, Firefox
- ejemplo de scripting para la inserción de páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "105704821"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="75c0d-128">Uso de scripts en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="75c0d-128">Using Script in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="75c0d-129">El script de una página web puede usar el modelo de objetos del reproductor para controlar el reproductor a medida que el usuario interactúa con la página.</span><span class="sxs-lookup"><span data-stu-id="75c0d-129">Script on a webpage can use the Player object model to control the Player as the user interacts with the page.</span></span> <span data-ttu-id="75c0d-130">Por ejemplo, el siguiente elemento de entrada tiene un script que establece el volumen del reproductor.</span><span class="sxs-lookup"><span data-stu-id="75c0d-130">For example, the following INPUT element has script that sets the Player volume.</span></span>


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



<span data-ttu-id="75c0d-131">Muchos de los objetos del modelo de objetos de Windows Media Player se admiten en Internet Explorer y en el complemento de Firefox.</span><span class="sxs-lookup"><span data-stu-id="75c0d-131">Many of the objects in the Windows Media Player object model are supported by Internet Explorer and by the Firefox plug-in.</span></span> <span data-ttu-id="75c0d-132">Sin embargo, hay algunos objetos que no son compatibles con el complemento de Firefox.</span><span class="sxs-lookup"><span data-stu-id="75c0d-132">However, there are some objects that are not supported by the Firefox plug-in.</span></span> <span data-ttu-id="75c0d-133">En la tabla siguiente se enumeran todos los objetos del modelo de objetos del reproductor y se muestran los objetos que admite el complemento de Firefox.</span><span class="sxs-lookup"><span data-stu-id="75c0d-133">The following table lists all of the objects in the Player object model and shows which objects are supported by the Firefox plug-in.</span></span>



| <span data-ttu-id="75c0d-134">Object</span><span class="sxs-lookup"><span data-stu-id="75c0d-134">Object</span></span>                                              | <span data-ttu-id="75c0d-135">Compatibilidad con Firefox</span><span class="sxs-lookup"><span data-stu-id="75c0d-135">Firefox support</span></span> |
|-----------------------------------------------------|-----------------|
| [<span data-ttu-id="75c0d-136">-</span><span class="sxs-lookup"><span data-stu-id="75c0d-136">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="75c0d-137">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-137">no</span></span>              |
| [<span data-ttu-id="75c0d-138">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="75c0d-138">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="75c0d-139">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-139">no</span></span>              |
| [<span data-ttu-id="75c0d-140">ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="75c0d-140">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="75c0d-141">sí</span><span class="sxs-lookup"><span data-stu-id="75c0d-141">yes</span></span>             |
| [<span data-ttu-id="75c0d-142">Controles</span><span class="sxs-lookup"><span data-stu-id="75c0d-142">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="75c0d-143">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-143">no</span></span>              |
| [<span data-ttu-id="75c0d-144">DISCOS</span><span class="sxs-lookup"><span data-stu-id="75c0d-144">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="75c0d-145">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-145">no</span></span>              |
| [<span data-ttu-id="75c0d-146">Error</span><span class="sxs-lookup"><span data-stu-id="75c0d-146">Error</span></span>](error-object.md)                           | <span data-ttu-id="75c0d-147">sí</span><span class="sxs-lookup"><span data-stu-id="75c0d-147">yes</span></span>             |
| [<span data-ttu-id="75c0d-148">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="75c0d-148">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="75c0d-149">sí</span><span class="sxs-lookup"><span data-stu-id="75c0d-149">yes</span></span>             |
| [<span data-ttu-id="75c0d-150">Elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="75c0d-150">Media</span></span>](media-object.md)                           | <span data-ttu-id="75c0d-151">sí</span><span class="sxs-lookup"><span data-stu-id="75c0d-151">yes</span></span>             |
| [<span data-ttu-id="75c0d-152">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="75c0d-152">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="75c0d-153">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-153">no</span></span>              |
| [<span data-ttu-id="75c0d-154">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="75c0d-154">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="75c0d-155">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-155">no</span></span>              |
| [<span data-ttu-id="75c0d-156">MetadataText</span><span class="sxs-lookup"><span data-stu-id="75c0d-156">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="75c0d-157">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-157">no</span></span>              |
| [<span data-ttu-id="75c0d-158">Network</span><span class="sxs-lookup"><span data-stu-id="75c0d-158">Network</span></span>](network-object.md)                       | <span data-ttu-id="75c0d-159">sí</span><span class="sxs-lookup"><span data-stu-id="75c0d-159">yes</span></span>             |
| [<span data-ttu-id="75c0d-160">Reproductor</span><span class="sxs-lookup"><span data-stu-id="75c0d-160">Player</span></span>](player-object.md)                         | <span data-ttu-id="75c0d-161">sí</span><span class="sxs-lookup"><span data-stu-id="75c0d-161">yes</span></span>             |
| [<span data-ttu-id="75c0d-162">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="75c0d-162">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="75c0d-163">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-163">no</span></span>              |
| [<span data-ttu-id="75c0d-164">Lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="75c0d-164">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="75c0d-165">sí</span><span class="sxs-lookup"><span data-stu-id="75c0d-165">yes</span></span>             |
| [<span data-ttu-id="75c0d-166">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="75c0d-166">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="75c0d-167">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-167">no</span></span>              |
| [<span data-ttu-id="75c0d-168">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="75c0d-168">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="75c0d-169">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-169">no</span></span>              |
| [<span data-ttu-id="75c0d-170">Consultar</span><span class="sxs-lookup"><span data-stu-id="75c0d-170">Query</span></span>](query-object.md)                           | <span data-ttu-id="75c0d-171">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-171">no</span></span>              |
| [<span data-ttu-id="75c0d-172">Configuración</span><span class="sxs-lookup"><span data-stu-id="75c0d-172">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="75c0d-173">sí</span><span class="sxs-lookup"><span data-stu-id="75c0d-173">yes</span></span>             |
| [<span data-ttu-id="75c0d-174">StringCollection</span><span class="sxs-lookup"><span data-stu-id="75c0d-174">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="75c0d-175">no</span><span class="sxs-lookup"><span data-stu-id="75c0d-175">no</span></span>              |



 

<span data-ttu-id="75c0d-176">El complemento de Firefox admite el objeto **Player** , pero algunas propiedades del objeto **Player** devuelven **null** en un explorador Firefox.</span><span class="sxs-lookup"><span data-stu-id="75c0d-176">The Firefox plug-in supports the **Player** object, but certain properties of the **Player** object return **NULL** in a Firefox browser.</span></span> <span data-ttu-id="75c0d-177">Por ejemplo, la propiedad [cdromCollection](player-cdromcollection.md) del objeto **Player** devuelve **null** porque el complemento Firefox no admite el objeto **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="75c0d-177">For example, the [cdromCollection](player-cdromcollection.md) property of the **Player** object returns **NULL** because the Firefox plug-in does not support the **Cdrom** object.</span></span> <span data-ttu-id="75c0d-178">Del mismo modo, las propiedades [DVD](player-dvd.md), [mediaCollection](player-mediacollection.md), [PlayerApplication](player-playerapplication.md)y [PlaylistCollection](player-playlistcollection.md) del objeto **Player** devuelven **null** en un explorador Firefox.</span><span class="sxs-lookup"><span data-stu-id="75c0d-178">Similarly, the [dvd](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md), and [playlistCollection](player-playlistcollection.md) properties of the **Player** object return **NULL** in a Firefox browser.</span></span>

<span data-ttu-id="75c0d-179">La propiedad **Player. pluginVersionInfo** es compatible con el complemento de Firefox, pero no con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="75c0d-179">The **Player.pluginVersionInfo** property is supported by the Firefox plug-in but not by Internet Explorer.</span></span> <span data-ttu-id="75c0d-180">Esta propiedad devuelve la versión del complemento de Firefox.</span><span class="sxs-lookup"><span data-stu-id="75c0d-180">This property returns the version of the Firefox plug-in.</span></span>

<span data-ttu-id="75c0d-181">El complemento de Firefox admite el objeto **multimedia** , incluida la propiedad [getItemInfoByType](media-getiteminfobytype.md) .</span><span class="sxs-lookup"><span data-stu-id="75c0d-181">The Firefox plug-in supports the **Media** object, including the [getItemInfoByType](media-getiteminfobytype.md) property.</span></span> <span data-ttu-id="75c0d-182">Sin embargo, en un explorador Firefox, la propiedad **getItemInfoByType** no admite los tipos de valor devuelto **MetadataText** y **MetadataPicture** .</span><span class="sxs-lookup"><span data-stu-id="75c0d-182">However, in a Firefox browser, the **getItemInfoByType** property does not support the **MetadataText** and **MetadataPicture** return types.</span></span>

<span data-ttu-id="75c0d-183">El complemento de Firefox admite el objeto de [configuración](settings-object.md) , excepto el método [setMode](settings-setmode.md) y la propiedad [requestMediaAccessRights](settings-requestmediaaccessrights.md) .</span><span class="sxs-lookup"><span data-stu-id="75c0d-183">The Firefox plug-in supports the [Settings](settings-object.md) object except for the [setMode](settings-setmode.md) method and the [requestMediaAccessRights](settings-requestmediaaccessrights.md) property.</span></span> <span data-ttu-id="75c0d-184">En un explorador Firefox, la propiedad **requestMediaAccessRight** siempre devuelve false.</span><span class="sxs-lookup"><span data-stu-id="75c0d-184">In a Firefox browser, the **requestMediaAccessRight** property always returns false.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75c0d-185">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75c0d-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75c0d-186">**Uso del control de Media Player de Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="75c0d-186">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 





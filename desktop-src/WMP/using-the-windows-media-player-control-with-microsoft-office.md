---
title: Usar el control Media Player de Windows con Microsoft Office
description: Usar el control Media Player de Windows con Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, Office
- Modelo de objetos de Windows Media Player, Office
- modelo de objetos, Office
- Windows Media Player Mobile, Office
- Windows Media Player control ActiveX, Office
- Control ActiveX móvil de Windows Media Player, Office
- Control ActiveX, Office
- Incrustación de documentos de Office
- incrustación, documentos de Office
- Control ActiveX de Windows Media Player, Excel
- Control ActiveX móvil de Windows Media Player, Excel
- Control ActiveX, Excel
- incrustación, hojas de cálculo de Excel
- Incrustación de hojas de cálculo de Excel
- Control ActiveX de Windows Media Player, PowerPoint
- Control ActiveX móvil de Windows Media Player, PowerPoint
- Control ActiveX, PowerPoint
- incrustación, presentaciones de diapositivas de PowerPoint
- Incrustación de diapositivas de PowerPoint
- Windows Media Player control ActiveX, Word
- Control ActiveX móvil de Windows Media Player, Word
- Control ActiveX, Word
- Incrustación de documentos de Word
- incrustación, documentos de Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994288"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a><span data-ttu-id="4b083-134">Usar el control Media Player de Windows con Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="4b083-134">Using the Windows Media Player Control with Microsoft Office</span></span>

<span data-ttu-id="4b083-135">En esta sección se describe cómo insertar la serie Windows Media Player 9 o un control ActiveX posterior en varios documentos creados con Microsoft Office XP.</span><span class="sxs-lookup"><span data-stu-id="4b083-135">This section describes how to embed the Windows Media Player 9 Series or later ActiveX control in various documents created using Microsoft Office XP.</span></span>

<span data-ttu-id="4b083-136">En Microsoft Word, Excel y PowerPoint®, para incrustar el control, seleccione **objeto** en el menú **Insertar** y, a continuación, elija **Media Player de Windows** en la lista de tipos de objeto disponibles.</span><span class="sxs-lookup"><span data-stu-id="4b083-136">In Microsoft Word, Excel, and PowerPoint®, you embed the control by selecting **Object** from the **Insert** menu, then choosing **Windows Media Player** from the list of available object types.</span></span> <span data-ttu-id="4b083-137">El control Media Player de Windows aparece en el documento en la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="4b083-137">The Windows Media Player control appears in the document at the current location.</span></span> <span data-ttu-id="4b083-138">A continuación, puede seleccionar el **control de formato** ( **objeto de formato** en Excel) en el menú contextual del control para ajustar el diseño, el estilo de ajuste de texto y otras opciones de formato.</span><span class="sxs-lookup"><span data-stu-id="4b083-138">You can then select **Format Control** ( **Format Object** in Excel) from the shortcut menu for the control to adjust the layout, text wrapping style, and other format options.</span></span> <span data-ttu-id="4b083-139">En Word y Excel, debe estar en modo de diseño para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="4b083-139">In Word and Excel, you must be in design mode to do this.</span></span>

<span data-ttu-id="4b083-140">Una vez que haya colocado y formateado el control, puede configurarlo mediante el cuadro de diálogo **propiedades** , al que se puede tener acceso desde el cuadro de **herramientas de control** o desde el menú contextual en modo de diseño para Word y Excel.</span><span class="sxs-lookup"><span data-stu-id="4b083-140">Once you have positioned and formatted the control, you can configure it using the **Properties** dialog box, which is accessible from the **Control Toolbox** or from the shortcut menu in design mode for Word and Excel.</span></span> <span data-ttu-id="4b083-141">Aquí puede especificar propiedades básicas del control Player, como el nombre del control, la dirección URL de un archivo multimedia digital y el modo de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4b083-141">Here you can specify basic Player control properties such as the control name, the URL of a digital media file, and the user interface mode.</span></span> <span data-ttu-id="4b083-142">Al establecer la propiedad **uiMode** en "none", se oculta todo el control, excepto el vídeo o la ventana de visualización, lo que le permite agregar sus propios botones y escribir código de script mediante Visual Basic para aplicaciones (VBA) para controlar los clics de botón y los eventos de control de reproductor.</span><span class="sxs-lookup"><span data-stu-id="4b083-142">Setting the **uiMode** property to "none" hides everything in the control except the video or visualization window, allowing you to add your own buttons and write script code using Visual Basic for Applications (VBA) to handle the button clicks and Player control events.</span></span>

<span data-ttu-id="4b083-143">En el cuadro de diálogo **propiedades** básicas, también puede tener acceso al cuadro de diálogo **propiedades de Control de Windows Media Player** más sofisticadas haciendo doble clic en la fila "(personalizada)" o haciendo clic en el botón de puntos suspensivos ("...") después de seleccionar esa fila.</span><span class="sxs-lookup"><span data-stu-id="4b083-143">From the basic **Properties** dialog box, you can also access the more sophisticated **Windows Media Player Control Properties** dialog box by double-clicking the "(Custom)" row or by clicking the ellipsis ("...") button after selecting that row.</span></span> <span data-ttu-id="4b083-144">En este cuadro de diálogo, puede modificar todas las propiedades de control del reproductor disponibles.</span><span class="sxs-lookup"><span data-stu-id="4b083-144">From this dialog box, you can modify all available Player control properties.</span></span>

> [!Note]  
> <span data-ttu-id="4b083-145">Debe tener cuidado de no tomar medidas en los controladores de eventos de control de reproductor que provocarán que el control se destruya.</span><span class="sxs-lookup"><span data-stu-id="4b083-145">You must be careful not to take actions in Player control event handlers that will result in the control being destroyed.</span></span> <span data-ttu-id="4b083-146">Por ejemplo, si incrusta el control Media Player de Windows en una diapositiva de una presentación de PowerPoint, no llame al método **Next** de PowerPoint desde el evento Player **openStateChange** o cualquier otro evento.</span><span class="sxs-lookup"><span data-stu-id="4b083-146">For example, if you embed the Windows Media Player control on a slide in a PowerPoint presentation, do not call the PowerPoint **Next** method from the Player **openStateChange** event or any other event.</span></span>

 

> [!Note]  
> <span data-ttu-id="4b083-147">Además, no debe establecer la propiedad **Player. URL** desde un controlador de eventos de control de reproductor.</span><span class="sxs-lookup"><span data-stu-id="4b083-147">In addition, you should not set the **Player.URL** property from a Player control event handler.</span></span>

 

<span data-ttu-id="4b083-148">En FrontPage, agregue el control Media Player de Windows a una página web seleccionando **componente web** en el menú **Insertar** .</span><span class="sxs-lookup"><span data-stu-id="4b083-148">In FrontPage, add the Windows Media Player control to a webpage by selecting **Web Component** from the **Insert** menu.</span></span> <span data-ttu-id="4b083-149">En el cuadro de diálogo **Insertar componente web** , seleccione **controles avanzados** en la lista **tipo de componente** y, a continuación, seleccione **control ActiveX** en la lista de opciones de control.</span><span class="sxs-lookup"><span data-stu-id="4b083-149">In the **Insert Web Component** dialog box, select **Advanced Controls** from the **Component type** list, then select **ActiveX Control** from the list of control choices.</span></span> <span data-ttu-id="4b083-150">En la siguiente ventana del cuadro de diálogo, seleccione **Windows Media Player**.</span><span class="sxs-lookup"><span data-stu-id="4b083-150">In the next window of the dialog box, select **Windows Media Player**.</span></span> <span data-ttu-id="4b083-151">Si no aparece, haga clic en **personalizar** y active la casilla **Media Player de Windows** en la lista de **controles** .</span><span class="sxs-lookup"><span data-stu-id="4b083-151">If it is not listed, click **Customize** and select the **Windows Media Player** check box in the **Control** list.</span></span>

<span data-ttu-id="4b083-152">Una vez incrustado el control de Media Player de Windows, puede colocarlo y cambiar su tamaño, y modificar sus propiedades seleccionando **propiedades de controles ActiveX** en el menú contextual del control.</span><span class="sxs-lookup"><span data-stu-id="4b083-152">After the Windows Media Player control is embedded, you can position and resize it, and modify its properties by selecting **ActiveX Control Properties** from the shortcut menu for the control.</span></span> <span data-ttu-id="4b083-153">En la vista HTML, los valores de propiedad que especifique aparecen en el elemento de objeto que representa el control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="4b083-153">In the HTML view, the property values that you specify appear in the OBJECT element representing the Windows Media Player control.</span></span> <span data-ttu-id="4b083-154">El nombre del objeto aparece como el atributo ID y las propiedades del control aparecen como etiquetas PARAM.</span><span class="sxs-lookup"><span data-stu-id="4b083-154">The object name appears as the ID attribute, and the control properties appear as PARAM tags.</span></span> <span data-ttu-id="4b083-155">El nombre de objeto proporciona acceso al modelo de objetos de control de Media Player de Windows, que puede programar con Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="4b083-155">The object name gives you access to the Windows Media Player control object model, which you can program using Microsoft JScript.</span></span> <span data-ttu-id="4b083-156">Para obtener más información, vea [usar el Control Media Player de Windows en una página web](using-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="4b083-156">For more information, see [Using the Windows Media Player Control in a Web Page](using-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b083-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b083-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b083-158">**Guía de control del reproductor**</span><span class="sxs-lookup"><span data-stu-id="4b083-158">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 





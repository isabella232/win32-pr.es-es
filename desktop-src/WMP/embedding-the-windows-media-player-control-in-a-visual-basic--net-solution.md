---
title: Incrustar el control Media Player de Windows en una solución Visual Basic .NET
description: Incrustar el control Media Player de Windows en una solución Visual Basic .NET
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, Visual Basic .NET
- Modelo de objetos de Windows Media Player, Visual Basic .NET
- modelo de objetos, Visual Basic .NET
- Windows Media Player Mobile, Visual Basic .NET
- Control ActiveX de Windows Media Player, Visual Basic .NET
- Control ActiveX de Windows Media Player Mobile, Visual Basic .NET
- Control ActiveX, Visual Basic .NET
- incrustación, Visual Basic programas .NET
- Incrustación de programas de Visual Basic .NET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d578b456a5064f1846ead7f074f178753dbc7c97
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104357823"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a><span data-ttu-id="e05d4-119">Incrustar el control Media Player de Windows en una solución Visual Basic .NET</span><span class="sxs-lookup"><span data-stu-id="e05d4-119">Embedding the Windows Media Player Control in a Visual Basic .NET Solution</span></span>

<span data-ttu-id="e05d4-120">Para usar la funcionalidad de Windows Media Player 9 series o posterior en una aplicación Visual Basic .NET, primero agregue el componente a un formulario tal y como se describe en [usar el Control Media Player de Windows con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="e05d4-120">To use the functionality of Windows Media Player 9 Series or later in a Visual Basic .NET application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="e05d4-121">En esta sección se describe cómo crear una aplicación que reproduzca vídeo y que tenga botones personalizados de reproducción y detención.</span><span class="sxs-lookup"><span data-stu-id="e05d4-121">This section describes how to create an application that plays video and has custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="e05d4-122">Agregar la ventana de vídeo</span><span class="sxs-lookup"><span data-stu-id="e05d4-122">Add the Video Window</span></span>

<span data-ttu-id="e05d4-123">Agregue el control Media Player de Windows a un formulario.</span><span class="sxs-lookup"><span data-stu-id="e05d4-123">Add the Windows Media Player control to a form.</span></span> <span data-ttu-id="e05d4-124">Cambie el tamaño del control y colóquelo donde desee que aparezca la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e05d4-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="e05d4-125">Seleccione el control Media Player de Windows y, a continuación, cambie la propiedad **uiMode** a "none".</span><span class="sxs-lookup"><span data-stu-id="e05d4-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="e05d4-126">Esta configuración oculta los controles de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e05d4-126">This setting hides the UI controls.</span></span> <span data-ttu-id="e05d4-127">Cuando el usuario reproduzca un vídeo, aparecerá en la ventana de.</span><span class="sxs-lookup"><span data-stu-id="e05d4-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="e05d4-128">En el caso de contenido de solo audio, aparecerá una visualización.</span><span class="sxs-lookup"><span data-stu-id="e05d4-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="e05d4-129">Agregar dos botones y ajustar el formulario</span><span class="sxs-lookup"><span data-stu-id="e05d4-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="e05d4-130">Ahora, agregue dos botones al formulario.</span><span class="sxs-lookup"><span data-stu-id="e05d4-130">Now add two buttons to the form.</span></span> <span data-ttu-id="e05d4-131">Seleccione el primer botón y cambie la propiedad **texto** a "reproducir".</span><span class="sxs-lookup"><span data-stu-id="e05d4-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="e05d4-132">Seleccione el segundo botón y cambie su propiedad **texto** a "detener".</span><span class="sxs-lookup"><span data-stu-id="e05d4-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="e05d4-133">Agregar el código de reproducción</span><span class="sxs-lookup"><span data-stu-id="e05d4-133">Add the Play Code</span></span>

<span data-ttu-id="e05d4-134">Haga doble clic en el botón **reproducir** para mostrar la ventana de código.</span><span class="sxs-lookup"><span data-stu-id="e05d4-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="e05d4-135">Se muestra el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="e05d4-135">The following code is displayed:</span></span>


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



<span data-ttu-id="e05d4-136">Agregue esta línea a la subrutina:</span><span class="sxs-lookup"><span data-stu-id="e05d4-136">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



<span data-ttu-id="e05d4-137">En el ejemplo de código anterior, "axWindowsMediaPlayer1" es el nombre predeterminado del control Media Player de Windows y "c: \\ MediaFile. WMV" es un marcador de posición para el nombre del medio que desea reproducir.</span><span class="sxs-lookup"><span data-stu-id="e05d4-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control and "c:\\mediafile.wmv" is a placeholder for the name of the media you want to play.</span></span>

<span data-ttu-id="e05d4-138">Si ha agregado el contenido multimedia digital del SDK de Windows Media Player a la biblioteca de Windows Media Player, puede usar este código en su lugar:</span><span class="sxs-lookup"><span data-stu-id="e05d4-138">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



<span data-ttu-id="e05d4-139">Dado que la propiedad **autoStart** es true de forma predeterminada, Windows Media Player comenzará a reproducirse cuando establezca la propiedad **currentPlaylist** o **URL** .</span><span class="sxs-lookup"><span data-stu-id="e05d4-139">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="e05d4-140">Agregar el código para detener</span><span class="sxs-lookup"><span data-stu-id="e05d4-140">Add the Stop Code</span></span>

<span data-ttu-id="e05d4-141">Haga doble clic en el botón **detener** para mostrar la ventana de código.</span><span class="sxs-lookup"><span data-stu-id="e05d4-141">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="e05d4-142">Se muestra el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="e05d4-142">The following code is displayed:</span></span>


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



<span data-ttu-id="e05d4-143">Agregue esta línea a la subrutina:</span><span class="sxs-lookup"><span data-stu-id="e05d4-143">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> <span data-ttu-id="e05d4-144">El contenedor de código administrado para el control Windows Media Player expone el objeto **Controls** como **Ctlcontrols** para evitar conflictos con la propiedad **Controls** heredada de **System. Windows. Forms. control**.</span><span class="sxs-lookup"><span data-stu-id="e05d4-144">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="e05d4-145">Agregar control de errores</span><span class="sxs-lookup"><span data-stu-id="e05d4-145">Add Error-handling</span></span>

<span data-ttu-id="e05d4-146">El control Media Player de Windows no genera una excepción cuando encuentra un error como una dirección URL no válida.</span><span class="sxs-lookup"><span data-stu-id="e05d4-146">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="e05d4-147">En su lugar, el control señala un evento.</span><span class="sxs-lookup"><span data-stu-id="e05d4-147">Instead, the control signals an event.</span></span> <span data-ttu-id="e05d4-148">La aplicación debe controlar los eventos de error enviados por el reproductor.</span><span class="sxs-lookup"><span data-stu-id="e05d4-148">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="e05d4-149">Para crear un controlador de eventos, abra la ventana de código para la clase de formulario.</span><span class="sxs-lookup"><span data-stu-id="e05d4-149">To create an event handler, open the code window for your form class.</span></span> <span data-ttu-id="e05d4-150">En la lista desplegable de la parte superior de la ventana, seleccione el control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="e05d4-150">From the drop-down list at the top of the window, select the Windows Media Player control.</span></span> <span data-ttu-id="e05d4-151">Aparece una lista de eventos en la lista desplegable de la derecha.</span><span class="sxs-lookup"><span data-stu-id="e05d4-151">A list of events appears in the drop-down list to the right.</span></span> <span data-ttu-id="e05d4-152">En esa lista, seleccione [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span><span class="sxs-lookup"><span data-stu-id="e05d4-152">From that list, select [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span></span> <span data-ttu-id="e05d4-153">Se muestra el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="e05d4-153">The following code is displayed:</span></span>


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



<span data-ttu-id="e05d4-154">El siguiente código se puede insertar en la subrutina para proporcionar una capacidad de control de errores mínima.</span><span class="sxs-lookup"><span data-stu-id="e05d4-154">The following code could be inserted in the subroutine to provide minimal error-handling capability.</span></span> <span data-ttu-id="e05d4-155">Tenga en cuenta que la información sobre el error se puede recuperar del argumento **\_ \_ MediaErrorEvent de WMPOCXEvents** .</span><span class="sxs-lookup"><span data-stu-id="e05d4-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


```VB
Try
    ' If the file is corrupt or missing, show the 
    ' hexadecimal error code and URL.
    Dim errSource As WMPLib.IWMPMedia2 = e.pMediaObject
    Dim errorItem As WMPLib.IWMPErrorItem = errSource.Error
    MessageBox.Show("Media error " + errorItem.errorCode.ToString("X") _
                    + " in " + errSource.sourceURL)
Catch ex As InvalidCastException
    ' In case pMediaObject is not an IWMPMedia item.
    MessageBox.Show("Player error.")
End Try

```



## <a name="related-topics"></a><span data-ttu-id="e05d4-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e05d4-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e05d4-157">**Incrustar el control Media Player de Windows en una solución de .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="e05d4-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 





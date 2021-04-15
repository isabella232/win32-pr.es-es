---
title: Incrustar el control Media Player de Windows en una solución de C
description: Incrustar el control de Media Player de Windows en una solución de C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, C
- Modelo de objetos de Windows Media Player, C
- modelo de objetos, C
- Windows Media Player Mobile, C
- Control ActiveX de Windows Media Player, C
- Control ActiveX móvil de Windows Media Player, C
- Control ActiveX, C
- incrustación, programas de C
- Incrustación de programas de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "105695490"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a><span data-ttu-id="3ba3c-119">Incrustar el control Media Player de Windows en una solución de C#</span><span class="sxs-lookup"><span data-stu-id="3ba3c-119">Embedding the Windows Media Player Control in a C# Solution</span></span>

<span data-ttu-id="3ba3c-120">Para usar la funcionalidad de Windows Media Player en una aplicación de C#, agregue primero el componente a un formulario tal y como se describe en [usar el Control Media Player de Windows con Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="3ba3c-120">To use the functionality of Windows Media Player in a C# application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="3ba3c-121">En las secciones siguientes se describe cómo crear una aplicación que reproduzca vídeo y use botones personalizados de reproducción y detención.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-121">The following sections describe how to create an application that plays video and uses custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="3ba3c-122">Agregar la ventana de vídeo</span><span class="sxs-lookup"><span data-stu-id="3ba3c-122">Add the Video Window</span></span>

<span data-ttu-id="3ba3c-123">Agregue el control ActiveX de Windows Media Player a un formulario.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-123">Add the Windows Media Player ActiveX control to a form.</span></span> <span data-ttu-id="3ba3c-124">Cambie el tamaño del control y colóquelo donde desee que aparezca la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="3ba3c-125">Seleccione el control Media Player de Windows y, a continuación, cambie la propiedad **uiMode** a "none".</span><span class="sxs-lookup"><span data-stu-id="3ba3c-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="3ba3c-126">Esta configuración oculta los controles de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-126">This setting hides the UI controls.</span></span> <span data-ttu-id="3ba3c-127">Cuando el usuario reproduzca un vídeo, aparecerá en la ventana de.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="3ba3c-128">En el caso de contenido de solo audio, aparecerá una visualización.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="3ba3c-129">Agregar dos botones y ajustar el formulario</span><span class="sxs-lookup"><span data-stu-id="3ba3c-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="3ba3c-130">Ahora, agregue dos botones al formulario.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-130">Now, add two buttons to the form.</span></span> <span data-ttu-id="3ba3c-131">Seleccione el primer botón y cambie la propiedad **texto** a "reproducir".</span><span class="sxs-lookup"><span data-stu-id="3ba3c-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="3ba3c-132">Seleccione el segundo botón y cambie su propiedad **texto** a "detener".</span><span class="sxs-lookup"><span data-stu-id="3ba3c-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="3ba3c-133">Agregar el código de reproducción</span><span class="sxs-lookup"><span data-stu-id="3ba3c-133">Add the Play Code</span></span>

<span data-ttu-id="3ba3c-134">Haga doble clic en el botón **reproducir** para mostrar la ventana de código.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="3ba3c-135">En C#, se mostrará el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="3ba3c-135">In C#, the following code will be displayed:</span></span>


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="3ba3c-136">Agregue esta línea entre las dos llaves:</span><span class="sxs-lookup"><span data-stu-id="3ba3c-136">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



<span data-ttu-id="3ba3c-137">En el ejemplo de código anterior, "axWindowsMediaPlayer1" es el nombre predeterminado del control Media Player de Windows y "c: \\ MediaFile. WMV" es un marcador de posición para el nombre del elemento multimedia que desea reproducir.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control, and "c:\\mediafile.wmv" is a placeholder for the name of the media item you want to play.</span></span> <span data-ttu-id="3ba3c-138">Se puede usar cualquier ruta de acceso de archivo válida.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-138">Any valid file path can be used.</span></span> <span data-ttu-id="3ba3c-139">El símbolo @ indica al compilador que no interprete las barras diagonales inversas como caracteres de escape.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-139">The @ symbol instructs the compiler to not interpret backslashes as escape characters.</span></span>

<span data-ttu-id="3ba3c-140">Si ha agregado el contenido multimedia digital del SDK de Windows Media Player a la biblioteca de Windows Media Player, puede usar este código en su lugar:</span><span class="sxs-lookup"><span data-stu-id="3ba3c-140">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



<span data-ttu-id="3ba3c-141">Dado que la propiedad **autoStart** es true de forma predeterminada, Windows Media Player comenzará a reproducirse cuando establezca la propiedad **currentPlaylist** o **URL** .</span><span class="sxs-lookup"><span data-stu-id="3ba3c-141">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="3ba3c-142">Agregar el código para detener</span><span class="sxs-lookup"><span data-stu-id="3ba3c-142">Add the Stop Code</span></span>

<span data-ttu-id="3ba3c-143">Haga doble clic en el botón **detener** para mostrar la ventana de código.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-143">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="3ba3c-144">En C#, se mostrará el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="3ba3c-144">In C#, the following code will be displayed:</span></span>


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="3ba3c-145">Agregue esta línea entre las dos llaves:</span><span class="sxs-lookup"><span data-stu-id="3ba3c-145">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> <span data-ttu-id="3ba3c-146">El contenedor de código administrado para el control Windows Media Player expone el objeto **Controls** como **Ctlcontrols** para evitar conflictos con la propiedad **Controls** heredada de **System. Windows. Forms. control**.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-146">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="3ba3c-147">Agregar control de errores</span><span class="sxs-lookup"><span data-stu-id="3ba3c-147">Add Error-handling</span></span>

<span data-ttu-id="3ba3c-148">El control Media Player de Windows no genera una excepción cuando encuentra un error como una dirección URL no válida.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-148">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="3ba3c-149">En su lugar, indica un evento.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-149">Instead, it signals an event.</span></span> <span data-ttu-id="3ba3c-150">La aplicación debe controlar los eventos de error enviados por el reproductor.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-150">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="3ba3c-151">Para crear un controlador de eventos, abra primero el ventana Propiedades para el control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-151">To create an event handler, first open the Properties window for the Windows Media Player control.</span></span> <span data-ttu-id="3ba3c-152">En la lista de eventos, haga doble clic en **MediaError**.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-152">In the list of events, double-click **MediaError**.</span></span> <span data-ttu-id="3ba3c-153">Se muestra el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3ba3c-153">The following code is displayed:</span></span>


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



<span data-ttu-id="3ba3c-154">El siguiente código se puede insertar en el método para proporcionar una capacidad de control de errores mínima.</span><span class="sxs-lookup"><span data-stu-id="3ba3c-154">The following code could be inserted in the method to provide minimal error-handling capability.</span></span> <span data-ttu-id="3ba3c-155">Tenga en cuenta que la información sobre el error se puede recuperar del argumento **\_ \_ MediaErrorEvent de WMPOCXEvents** .</span><span class="sxs-lookup"><span data-stu-id="3ba3c-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a><span data-ttu-id="3ba3c-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3ba3c-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ba3c-157">**Incrustar el control Media Player de Windows en una solución de .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="3ba3c-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 





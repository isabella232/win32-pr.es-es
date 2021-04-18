---
title: Propiedad AxWindowsMediaPlayer. uiMode
description: La propiedad uiMode obtiene o establece un valor que indica qué controles se muestran en la interfaz de usuario.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- propiedades de uiMode Media Player de Windows
- propiedad uiMode Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699988"
---
# <a name="axwindowsmediaplayeruimode-property"></a><span data-ttu-id="2c8ce-106">Propiedad AxWindowsMediaPlayer. uiMode</span><span class="sxs-lookup"><span data-stu-id="2c8ce-106">AxWindowsMediaPlayer.uiMode property</span></span>

<span data-ttu-id="2c8ce-107">La propiedad uiMode obtiene o establece un valor que indica qué controles se muestran en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-107">The uiMode property gets or sets a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8ce-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c8ce-108">Syntax</span></span>


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a><span data-ttu-id="2c8ce-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2c8ce-109">Property value</span></span>

<span data-ttu-id="2c8ce-110">System. String que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-110">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="2c8ce-111">Value</span><span class="sxs-lookup"><span data-stu-id="2c8ce-111">Value</span></span>     | <span data-ttu-id="2c8ce-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c8ce-112">Description</span></span>                                                                                                                                                                                                     | <span data-ttu-id="2c8ce-113">Ejemplo de audio</span><span class="sxs-lookup"><span data-stu-id="2c8ce-113">Audio example</span></span>                                                   | <span data-ttu-id="2c8ce-114">Ejemplo de vídeo</span><span class="sxs-lookup"><span data-stu-id="2c8ce-114">Video example</span></span>                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2c8ce-115">invisibles</span><span class="sxs-lookup"><span data-stu-id="2c8ce-115">invisible</span></span> | <span data-ttu-id="2c8ce-116">Windows Media Player está incrustado sin ninguna interfaz de usuario visible (controles, vídeo o ventana de visualización).</span><span class="sxs-lookup"><span data-stu-id="2c8ce-116">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                  | <span data-ttu-id="2c8ce-117">(No se muestra nada).</span><span class="sxs-lookup"><span data-stu-id="2c8ce-117">(Nothing is displayed.)</span></span>                                         | <span data-ttu-id="2c8ce-118">(No se muestra nada).</span><span class="sxs-lookup"><span data-stu-id="2c8ce-118">(Nothing is displayed.)</span></span>                                         |
| <span data-ttu-id="2c8ce-119">ninguno</span><span class="sxs-lookup"><span data-stu-id="2c8ce-119">none</span></span>      | <span data-ttu-id="2c8ce-120">Windows Media Player está incrustado sin controles y solo se muestra la ventana de vídeo o visualización.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-120">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                   | ![uiMode = ' none ' con audio](images/uimode-none-audio-v11.png) | ![uiMode = ' none ' con vídeo](images/uimode-none-video-v11.png) |
| <span data-ttu-id="2c8ce-123">pequeño</span><span class="sxs-lookup"><span data-stu-id="2c8ce-123">mini</span></span>      | <span data-ttu-id="2c8ce-124">Windows Media Player está incrustado con los controles ventana de estado, reproducir/pausar, detener, silenciar y volumen mostrados además de la ventana de vídeo o visualización.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-124">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                    | ![uiMode = ' Mini ' con audio](images/uimode-mini-audio-v11.png) | ![uiMode = ' Mini ' con vídeo](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="2c8ce-127">full</span><span class="sxs-lookup"><span data-stu-id="2c8ce-127">full</span></span>      | <span data-ttu-id="2c8ce-128">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-128">Default.</span></span> <span data-ttu-id="2c8ce-129">Windows Media Player está incrustado con los controles ventana de estado, barra de búsqueda, reproducir/pausar, detener, silenciar, siguiente, anterior, avance rápido, rebobinar y volumen, además de la ventana de vídeo o visualización.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-129">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, rewind, and volume controls in addition to the video or visualization window.</span></span> | ![uiMode = ' Full ' con audio](images/uimode-full-audio-v11.png) | ![uiMode = ' Full ' con vídeo](images/uimode-full-video-v11.png) |
| <span data-ttu-id="2c8ce-132">custom</span><span class="sxs-lookup"><span data-stu-id="2c8ce-132">custom</span></span>    | <span data-ttu-id="2c8ce-133">Windows Media Player está incrustado con una interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-133">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="2c8ce-134">Solo se puede usar en programas de C++.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-134">Can only be used in C++ programs.</span></span>                                                                                                                | <span data-ttu-id="2c8ce-135">(Se muestra la interfaz de usuario personalizada).</span><span class="sxs-lookup"><span data-stu-id="2c8ce-135">(Custom user interface is displayed.)</span></span>                           | <span data-ttu-id="2c8ce-136">(Se muestra la interfaz de usuario personalizada).</span><span class="sxs-lookup"><span data-stu-id="2c8ce-136">(Custom user interface is displayed.)</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="2c8ce-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c8ce-137">Remarks</span></span>

<span data-ttu-id="2c8ce-138">Esta propiedad especifica la apariencia del Media Player de Windows incrustado.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-138">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="2c8ce-139">Cuando **uiMode** se establece en "none", "mini" o "Full", hay una ventana para la presentación de clips de vídeo y visualizaciones de audio.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-139">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="2c8ce-140">Esta ventana se puede ocultar en el modo mini o completo estableciendo el atributo de **alto** de la etiqueta de **objeto** en 40, que se mide desde la parte inferior, y deja visible la parte controles de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-140">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="2c8ce-141">Si no se desea ninguna interfaz incrustada, establezca los atributos **ancho** y **alto** en cero.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-141">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="2c8ce-142">Si **uiMode** se establece en "invisible", no se muestra ninguna interfaz de usuario, pero el espacio se reserva en la página según lo especificado en **ancho** y **alto**.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-142">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="2c8ce-143">Esto resulta útil para conservar el diseño de página cuando **uiMode** puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-143">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="2c8ce-144">Además, el espacio reservado es transparente, por lo que todos los elementos que estén en capas detrás del control serán visibles.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-144">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="2c8ce-145">Si **uiMode** se establece en "Full" o "mini", Windows Media Player muestra los controles de transporte en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-145">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="2c8ce-146">Si **uiMode** se establece en "none", no se muestra ningún control en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-146">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="2c8ce-147">Si la ventana está visible y el contenido de audio se está reproduciendo, la visualización que se muestra será la que se usó más recientemente en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-147">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="2c8ce-148">Si **uiMode** se establece en "Custom" en un programa de C++ que implementa **IWMPRemoteMediaServices**, se muestra el archivo de máscara indicado por **IWMPRemoteMediaServices. GetCustomUIMode** .</span><span class="sxs-lookup"><span data-stu-id="2c8ce-148">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices.GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="2c8ce-149">Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".</span><span class="sxs-lookup"><span data-stu-id="2c8ce-149">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="2c8ce-150">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2c8ce-150">Examples</span></span>

<span data-ttu-id="2c8ce-151">En el ejemplo siguiente se crea un cuadro de lista que permite al usuario cambiar el modo de interfaz de usuario para un objeto incrustado de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-151">The following example creates a list box that allows the user to change the user interface mode for an embedded Windows Media Player object.</span></span> <span data-ttu-id="2c8ce-152">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-152">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2c8ce-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c8ce-153">Requirements</span></span>



| <span data-ttu-id="2c8ce-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c8ce-154">Requirement</span></span> | <span data-ttu-id="2c8ce-155">Value</span><span class="sxs-lookup"><span data-stu-id="2c8ce-155">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8ce-156">Versión</span><span class="sxs-lookup"><span data-stu-id="2c8ce-156">Version</span></span><br/>   | <span data-ttu-id="2c8ce-157">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2c8ce-157">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="2c8ce-158">Windows Media Player 9 series o posterior para "invisible" o "personalizado"</span><span class="sxs-lookup"><span data-stu-id="2c8ce-158">Windows Media Player 9 Series or later for "invisible" or "custom"</span></span><br/>   |
| <span data-ttu-id="2c8ce-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2c8ce-159">Namespace</span></span><br/> | <span data-ttu-id="2c8ce-160">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2c8ce-160">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2c8ce-161">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="2c8ce-161">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2c8ce-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2c8ce-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8ce-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c8ce-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8ce-164">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2c8ce-164">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2c8ce-165">**AxWindowsMediaPlayer. enableContextMenu (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2c8ce-165">**AxWindowsMediaPlayer.enableContextMenu (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 






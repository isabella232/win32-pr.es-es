---
title: IWMPSettings Rate (propiedad)
description: La propiedad Rate obtiene o establece la velocidad de reproducción actual del vídeo.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Media Player de la propiedad Rate de Windows
- propiedad Rate Media Player de Windows, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad Rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718697"
---
# <a name="iwmpsettingsrate-property"></a><span data-ttu-id="90d6d-106">IWMPSettings:: Rate (propiedad)</span><span class="sxs-lookup"><span data-stu-id="90d6d-106">IWMPSettings::rate property</span></span>

<span data-ttu-id="90d6d-107">La propiedad **Rate** obtiene o establece la velocidad de reproducción actual del vídeo.</span><span class="sxs-lookup"><span data-stu-id="90d6d-107">The **rate** property gets or sets the current playback rate for video.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d6d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90d6d-108">Syntax</span></span>


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a><span data-ttu-id="90d6d-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="90d6d-109">Property value</span></span>

<span data-ttu-id="90d6d-110">**System. Double** que es la velocidad de reproducción, con un valor predeterminado de 1,0.</span><span class="sxs-lookup"><span data-stu-id="90d6d-110">A **System.Double** that is the playback rate, with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="90d6d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90d6d-111">Remarks</span></span>

<span data-ttu-id="90d6d-112">El valor recuperado por esta propiedad actúa como un valor de multiplicador que permite reproducir un elemento multimedia a una velocidad mayor o menor.</span><span class="sxs-lookup"><span data-stu-id="90d6d-112">The value retrieved by this property acts as a multiplier value that enables you to play a media item at a faster or slower rate.</span></span> <span data-ttu-id="90d6d-113">El valor predeterminado de 1,0 indica la velocidad de creación.</span><span class="sxs-lookup"><span data-stu-id="90d6d-113">The default value of 1.0 indicates the authored speed.</span></span>

<span data-ttu-id="90d6d-114">Tenga en cuenta que una pista de audio es difícil de comprender a las tarifas inferiores a 0,5 o superior a 1,5.</span><span class="sxs-lookup"><span data-stu-id="90d6d-114">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="90d6d-115">Una velocidad de reproducción de 2 indica dos veces la velocidad de reproducción normal.</span><span class="sxs-lookup"><span data-stu-id="90d6d-115">A playback rate of 2 indicates twice the normal playback speed.</span></span>

<span data-ttu-id="90d6d-116">Windows Media Player intentará usar los siguientes cuatro modos de reproducción diferentes:</span><span class="sxs-lookup"><span data-stu-id="90d6d-116">Windows Media Player will attempt to use the most effective of the following four different playback modes</span></span>

-   <span data-ttu-id="90d6d-117">Reproducción fluida de vídeo con el paso de audio mantenido</span><span class="sxs-lookup"><span data-stu-id="90d6d-117">Smooth video playback with audio pitch maintained</span></span>
-   <span data-ttu-id="90d6d-118">Reproducción fluida de vídeo con el tono de audio no mantenido</span><span class="sxs-lookup"><span data-stu-id="90d6d-118">Smooth video playback with audio pitch not maintained</span></span>
-   <span data-ttu-id="90d6d-119">Reproducción fluida de vídeo sin audio</span><span class="sxs-lookup"><span data-stu-id="90d6d-119">Smooth video playback with no audio</span></span>
-   <span data-ttu-id="90d6d-120">Reproducción de vídeo de fotogramas clave sin audio</span><span class="sxs-lookup"><span data-stu-id="90d6d-120">Keyframe video playback with no audio</span></span>

<span data-ttu-id="90d6d-121">El modo elegido por Windows Media Player depende de numerosos factores, como el tipo de archivo y la ubicación, el sistema operativo, la red y el servidor.</span><span class="sxs-lookup"><span data-stu-id="90d6d-121">The mode chosen by Windows Media Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="90d6d-122">También se aplican otras consideraciones, dependiendo del formato de medios digitales utilizado para crear el contenido:</span><span class="sxs-lookup"><span data-stu-id="90d6d-122">Other considerations apply as well, depending on the digital media format used to create the content:</span></span>

-   <span data-ttu-id="90d6d-123">**Windows Media Video (WMV) y ASF.**</span><span class="sxs-lookup"><span data-stu-id="90d6d-123">**Windows Media Video (WMV) and ASF.**</span></span> <span data-ttu-id="90d6d-124">Los valores óptimos para la propiedad **Rate** son de 1 a 10, o de 1 a 10 para la reproducción inversa.</span><span class="sxs-lookup"><span data-stu-id="90d6d-124">Optimal values for the **rate** property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="90d6d-125">Los valores de 0,5 a 1,0 o de-0,5 a-1,0 también pueden funcionar bien en los casos en los que se pueda mantener el tono de audio, como al reproducir archivos ubicados en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="90d6d-125">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, such as when playing files located on the local computer.</span></span> <span data-ttu-id="90d6d-126">Se permiten los valores con una magnitud absoluta mayor que 10, pero no son muy significativos.</span><span class="sxs-lookup"><span data-stu-id="90d6d-126">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="90d6d-127">**Otros formatos de vídeo.**</span><span class="sxs-lookup"><span data-stu-id="90d6d-127">**Other video formats.**</span></span> <span data-ttu-id="90d6d-128">La propiedad **Rate** puede oscilar entre 0 y 9.</span><span class="sxs-lookup"><span data-stu-id="90d6d-128">The **rate** property can range from 0 to 9.</span></span> <span data-ttu-id="90d6d-129">No se permiten valores negativos.</span><span class="sxs-lookup"><span data-stu-id="90d6d-129">Negative values are not allowed.</span></span> <span data-ttu-id="90d6d-130">Los valores menores que 1 representan un movimiento lento.</span><span class="sxs-lookup"><span data-stu-id="90d6d-130">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="90d6d-131">Los valores por encima de 9 están permitidos, pero no son muy significativos.</span><span class="sxs-lookup"><span data-stu-id="90d6d-131">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="90d6d-132">El método **IWMPControls. fastForward** cambia el valor de **Rate** a 5,0, mientras que el método **IWMPControls. fastReverse** cambia el valor de **Rate** a 5,0.</span><span class="sxs-lookup"><span data-stu-id="90d6d-132">The **IWMPControls.fastForward** method changes the value of **rate** to 5.0, while the **IWMPControls.fastReverse** method changes the value of **rate** to  5.0.</span></span>

<span data-ttu-id="90d6d-133">No se puede modificar la velocidad de reproducción de algunos formatos de medios digitales.</span><span class="sxs-lookup"><span data-stu-id="90d6d-133">The playback rate of some digital media formats cannot be altered.</span></span> <span data-ttu-id="90d6d-134">Use la propiedad **IWMPSettings. isavailable** (en C# el método **IWMPSettings. Get \_ isavailable** ) para detectar si esta propiedad se puede especificar para un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="90d6d-134">Use the **IWMPSettings.isAvailable** property (In C# the **IWMPSettings.get\_isAvailable** method) to discover whether this property can be specified for a particular media item.</span></span>

## <a name="examples"></a><span data-ttu-id="90d6d-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="90d6d-135">Examples</span></span>

<span data-ttu-id="90d6d-136">En el ejemplo siguiente se usa un control numérico de flechas que permite al usuario cambiar la velocidad de reproducción del medio actual.</span><span class="sxs-lookup"><span data-stu-id="90d6d-136">The following example uses a numeric updown control that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="90d6d-137">Cuando el usuario hace clic en las flechas arriba o abajo del control, la propiedad **Rate** se establece en el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="90d6d-137">When the user clicks the up or down arrows of the control, the **rate** property is set to the new value.</span></span> <span data-ttu-id="90d6d-138">El intervalo posible de valores del control es 0,5 (velocidad media) a 2,0 (velocidad doble).</span><span class="sxs-lookup"><span data-stu-id="90d6d-138">The possible range of values in the control are 0.5 (half-speed) to 2.0 (double-speed).</span></span> <span data-ttu-id="90d6d-139">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="90d6d-139">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="90d6d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90d6d-140">Requirements</span></span>



| <span data-ttu-id="90d6d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="90d6d-141">Requirement</span></span> | <span data-ttu-id="90d6d-142">Value</span><span class="sxs-lookup"><span data-stu-id="90d6d-142">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90d6d-143">Versión</span><span class="sxs-lookup"><span data-stu-id="90d6d-143">Version</span></span><br/>   | <span data-ttu-id="90d6d-144">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="90d6d-144">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="90d6d-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="90d6d-145">Namespace</span></span><br/> | <span data-ttu-id="90d6d-146">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="90d6d-146">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="90d6d-147">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="90d6d-147">Assembly</span></span><br/>  | <dl> <span data-ttu-id="90d6d-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="90d6d-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90d6d-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="90d6d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d6d-150">**IWMPControls. fastForward (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="90d6d-150">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="90d6d-151">**IWMPControls. fastReverse (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="90d6d-151">**IWMPControls.fastReverse (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="90d6d-152">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="90d6d-152">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="90d6d-153">**IWMPSettings. isAvailable (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="90d6d-153">**IWMPSettings.isAvailable (VB and C#)**</span></span>](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="90d6d-154">**IWMPSettings. MUTE (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="90d6d-154">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 






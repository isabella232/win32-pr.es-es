---
title: IWMPMedia Duration (propiedad)
description: La propiedad duration obtiene la duración en segundos del elemento multimedia actual.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- propiedad duration de Windows Media Player
- propiedad duration de Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, propiedad duration
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671591"
---
# <a name="iwmpmediaduration-property"></a><span data-ttu-id="a0b47-106">IWMPMedia::d propiedad primario</span><span class="sxs-lookup"><span data-stu-id="a0b47-106">IWMPMedia::duration property</span></span>

<span data-ttu-id="a0b47-107">La propiedad **Duration** obtiene la duración en segundos del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="a0b47-107">The **duration** property gets the duration in seconds of the current media item.</span></span>

<span data-ttu-id="a0b47-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a0b47-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b47-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0b47-109">Syntax</span></span>


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a><span data-ttu-id="a0b47-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a0b47-110">Property value</span></span>

<span data-ttu-id="a0b47-111">**System. Double** que es la duración en segundos.</span><span class="sxs-lookup"><span data-stu-id="a0b47-111">A **System.Double** that is the duration in seconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b47-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0b47-112">Remarks</span></span>

<span data-ttu-id="a0b47-113">Si esta propiedad se usa con un elemento multimedia distinto del especificado en AxWindowsMediaPlayer. currentMedia, puede que no contenga un valor válido.</span><span class="sxs-lookup"><span data-stu-id="a0b47-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span>

<span data-ttu-id="a0b47-114">Para recuperar la duración de los archivos que no están en la biblioteca del usuario, debe esperar a que Windows Media Player Abra el archivo; es decir, el **OpenState** actual debe ser igual a **MediaOpen**.</span><span class="sxs-lookup"><span data-stu-id="a0b47-114">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current **OpenState** must equal **MediaOpen**.</span></span> <span data-ttu-id="a0b47-115">Puede comprobarlo mediante el control de **AxWindowsMediaPlayer. \_ Evento WMPOCXEvents \_ OpenStateChange** o comprobando periódicamente el valor de **AxWindowsMediaPlayer. openState**.</span><span class="sxs-lookup"><span data-stu-id="a0b47-115">You can verify this by handling the **AxWindowsMediaPlayer.\_WMPOCXEvents\_OpenStateChange** event or by periodically checking the value of **AxWindowsMediaPlayer.openState**.</span></span>

<span data-ttu-id="a0b47-116">En las listas de reproducción, la duración de cada elemento multimedia se puede recuperar cuando se abre el elemento multimedia individual, en lugar de cuando se abre la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a0b47-116">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="a0b47-117">Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a0b47-117">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="a0b47-118">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a0b47-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a0b47-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a0b47-119">Examples</span></span>

<span data-ttu-id="a0b47-120">En el ejemplo siguiente se usa **Duration** para mostrar el tiempo restante en el elemento multimedia actual de una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a0b47-120">The following example uses **duration** to display the time remaining in the current media item in a label.</span></span> <span data-ttu-id="a0b47-121">Un temporizador actualiza el texto de la etiqueta cada segundo.</span><span class="sxs-lookup"><span data-stu-id="a0b47-121">A timer updates the text in the label every second.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a0b47-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0b47-122">Requirements</span></span>



| <span data-ttu-id="a0b47-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0b47-123">Requirement</span></span> | <span data-ttu-id="a0b47-124">Value</span><span class="sxs-lookup"><span data-stu-id="a0b47-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b47-125">Versión</span><span class="sxs-lookup"><span data-stu-id="a0b47-125">Version</span></span><br/>   | <span data-ttu-id="a0b47-126">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a0b47-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a0b47-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a0b47-127">Namespace</span></span><br/> | <span data-ttu-id="a0b47-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a0b47-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a0b47-129">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a0b47-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a0b47-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a0b47-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b47-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0b47-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b47-132">**AxWindowsMediaPlayer. currentMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a0b47-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a0b47-133">**AxWindowsMediaPlayer. openState (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a0b47-133">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a0b47-134">**Evento AxWindowsMediaPlayer. OpenStateChange (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a0b47-134">**AxWindowsMediaPlayer.OpenStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="a0b47-135">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a0b47-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a0b47-136">**IWMPMedia. durationString (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a0b47-136">**IWMPMedia.durationString (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 






---
title: Propiedad bufferingProgress de IWMPNetwork
description: La propiedad bufferingProgress obtiene el porcentaje de almacenamiento en búfer completado.
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- propiedades de bufferingProgress Media Player de Windows
- propiedad bufferingProgress de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad bufferingProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699777"
---
# <a name="iwmpnetworkbufferingprogress-property"></a><span data-ttu-id="09679-106">IWMPNetwork:: bufferingProgress (propiedad)</span><span class="sxs-lookup"><span data-stu-id="09679-106">IWMPNetwork::bufferingProgress property</span></span>

<span data-ttu-id="09679-107">La propiedad **bufferingProgress** obtiene el porcentaje de almacenamiento en búfer completado.</span><span class="sxs-lookup"><span data-stu-id="09679-107">The **bufferingProgress** property gets the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="09679-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09679-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="09679-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="09679-109">Property value</span></span>

<span data-ttu-id="09679-110">**System. Int32** que es el progreso del almacenamiento en búfer expresado como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="09679-110">A **System.Int32** that is the buffering progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="09679-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09679-111">Remarks</span></span>

<span data-ttu-id="09679-112">Cada vez que se detiene y se reinicia la reproducción, esta propiedad se restablece en cero.</span><span class="sxs-lookup"><span data-stu-id="09679-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="09679-113">No se restablece si la reproducción está en pausa.</span><span class="sxs-lookup"><span data-stu-id="09679-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="09679-114">El almacenamiento en búfer solo se aplica al contenido de streaming.</span><span class="sxs-lookup"><span data-stu-id="09679-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="09679-115">Esta propiedad obtiene información válida solo durante el tiempo de ejecución cuando se establece la dirección URL para la reproducción mediante la propiedad **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="09679-115">This property gets valid information only during run time when the URL for playback is set using the **AxWindowsMediaPlayer.URL** property.</span></span>

<span data-ttu-id="09679-116">Use **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** para determinar cuándo se inicia o se detiene el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="09679-116">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="09679-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="09679-117">Examples</span></span>

<span data-ttu-id="09679-118">En el ejemplo siguiente se usa **bufferingProgress** para mostrar el porcentaje de almacenamiento en búfer completado en una etiqueta, en respuesta al evento de almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="09679-118">The following example uses **bufferingProgress** to display the percentage of buffering completed in a label, in response to the Buffering Event.</span></span> <span data-ttu-id="09679-119">En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="09679-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="09679-120">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="09679-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="09679-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09679-121">Requirements</span></span>



| <span data-ttu-id="09679-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="09679-122">Requirement</span></span> | <span data-ttu-id="09679-123">Value</span><span class="sxs-lookup"><span data-stu-id="09679-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09679-124">Versión</span><span class="sxs-lookup"><span data-stu-id="09679-124">Version</span></span><br/>   | <span data-ttu-id="09679-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="09679-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="09679-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="09679-126">Namespace</span></span><br/> | <span data-ttu-id="09679-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="09679-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="09679-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="09679-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="09679-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="09679-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09679-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="09679-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09679-131">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="09679-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="09679-132">**Evento AxWindowsMediaPlayer. buffering (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="09679-132">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="09679-133">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="09679-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 






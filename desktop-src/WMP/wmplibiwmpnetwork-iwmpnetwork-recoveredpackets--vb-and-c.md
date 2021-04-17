---
title: Propiedad recoveredPackets de IWMPNetwork
description: La propiedad recoveredPackets obtiene el número de paquetes recuperados.
ms.assetid: 90fcefcd-2bd7-4fb5-8337-36bec5d44e60
keywords:
- propiedades de recoveredPackets Media Player de Windows
- propiedad recoveredPackets de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad recoveredPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.recoveredPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe9fb8b44249be30289abb2f8922343285ca074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653995"
---
# <a name="iwmpnetworkrecoveredpackets-property"></a><span data-ttu-id="9f105-106">IWMPNetwork:: recoveredPackets (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9f105-106">IWMPNetwork::recoveredPackets property</span></span>

<span data-ttu-id="9f105-107">La propiedad **recoveredPackets** obtiene el número de paquetes recuperados.</span><span class="sxs-lookup"><span data-stu-id="9f105-107">The **recoveredPackets** property gets the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f105-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f105-108">Syntax</span></span>


```CSharp
public System.Int32 recoveredPackets {get; set;}
```


```VB

Public ReadOnly Property recoveredPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="9f105-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9f105-109">Property value</span></span>

<span data-ttu-id="9f105-110">**System. Int32** que es el número de paquetes recuperados.</span><span class="sxs-lookup"><span data-stu-id="9f105-110">A **System.Int32** that is the number of recovered packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f105-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f105-111">Remarks</span></span>

<span data-ttu-id="9f105-112">Cada vez que se detiene y se reinicia la reproducción, esta propiedad se restablece en cero.</span><span class="sxs-lookup"><span data-stu-id="9f105-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="9f105-113">El valor no se restablece si la reproducción está en pausa.</span><span class="sxs-lookup"><span data-stu-id="9f105-113">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="9f105-114">Esta propiedad obtiene información válida solo durante el tiempo de ejecución cuando se establece la dirección URL para la reproducción mediante la propiedad **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="9f105-114">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span> <span data-ttu-id="9f105-115">El valor será cero cuando se use el protocolo HTTP, que es sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="9f105-115">The value will be zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="9f105-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9f105-116">Examples</span></span>

<span data-ttu-id="9f105-117">En el ejemplo siguiente se usa **recoveredPackets** para mostrar el número de paquetes recuperados en una etiqueta, en respuesta al evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9f105-117">The following example uses **recoveredPackets** to display the number of recovered packets in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="9f105-118">En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9f105-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="9f105-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="9f105-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateRecoveredPackets(object sender, EventArgs e)
{
    recoveredPacketsLabel.Text = ("Packets recovered: " + player.network.recoveredPackets.ToString());
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

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

Public Sub UpdateRecoveredPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    recoveredPacketsLabel.Text = (&quot;Packets recovered: &quot; + player.network.recoveredPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="9f105-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f105-120">Requirements</span></span>



| <span data-ttu-id="9f105-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f105-121">Requirement</span></span> | <span data-ttu-id="9f105-122">Value</span><span class="sxs-lookup"><span data-stu-id="9f105-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f105-123">Versión</span><span class="sxs-lookup"><span data-stu-id="9f105-123">Version</span></span><br/>   | <span data-ttu-id="9f105-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="9f105-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9f105-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9f105-125">Namespace</span></span><br/> | <span data-ttu-id="9f105-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9f105-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9f105-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="9f105-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9f105-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9f105-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f105-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f105-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f105-130">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9f105-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9f105-131">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9f105-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 






---
title: Propiedad receptionQuality de IWMPNetwork
description: La propiedad receptionQuality obtiene el porcentaje de paquetes no perdidos en los últimos 30 segundos.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- propiedades de receptionQuality Media Player de Windows
- propiedad receptionQuality de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad receptionQuality
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3703ffa29183937874c40053bd3c7ae3c85d75d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700330"
---
# <a name="iwmpnetworkreceptionquality-property"></a><span data-ttu-id="d4a75-106">IWMPNetwork:: receptionQuality (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d4a75-106">IWMPNetwork::receptionQuality property</span></span>

<span data-ttu-id="d4a75-107">La propiedad **receptionQuality** obtiene el porcentaje de paquetes no perdidos en los últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="d4a75-107">The **receptionQuality** property gets the percentage of packets not lost in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4a75-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4a75-108">Syntax</span></span>


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="d4a75-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d4a75-109">Property value</span></span>

<span data-ttu-id="d4a75-110">**System. Int32** que es la calidad de la recepción.</span><span class="sxs-lookup"><span data-stu-id="d4a75-110">A **System.Int32** that is the reception quality.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4a75-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4a75-111">Remarks</span></span>

<span data-ttu-id="d4a75-112">El número de paquetes recibidos, perdidos y recuperados durante el streaming se supervisa una vez por segundo.</span><span class="sxs-lookup"><span data-stu-id="d4a75-112">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="d4a75-113">La propiedad **receptionQuality** obtiene el porcentaje de paquetes que no se pierden durante los últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="d4a75-113">The **receptionQuality** property gets the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="d4a75-114">Cada vez que se detiene y se reinicia la reproducción, esta propiedad se restablece en cero.</span><span class="sxs-lookup"><span data-stu-id="d4a75-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="d4a75-115">El valor no se restablece si la reproducción está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d4a75-115">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="d4a75-116">Esta propiedad obtiene información válida solo durante el tiempo de ejecución cuando se establece la dirección URL para la reproducción mediante la propiedad **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="d4a75-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="d4a75-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d4a75-117">Examples</span></span>

<span data-ttu-id="d4a75-118">En el ejemplo siguiente se usa **receptionQuality** para mostrar el porcentaje de paquetes recibidos en una etiqueta, en respuesta al evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d4a75-118">The following example uses **receptionQuality** to display the percentage of packets received in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="d4a75-119">En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="d4a75-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="d4a75-120">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="d4a75-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
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

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d4a75-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4a75-121">Requirements</span></span>



| <span data-ttu-id="d4a75-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4a75-122">Requirement</span></span> | <span data-ttu-id="d4a75-123">Value</span><span class="sxs-lookup"><span data-stu-id="d4a75-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a75-124">Versión</span><span class="sxs-lookup"><span data-stu-id="d4a75-124">Version</span></span><br/>   | <span data-ttu-id="d4a75-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="d4a75-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d4a75-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4a75-126">Namespace</span></span><br/> | <span data-ttu-id="d4a75-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d4a75-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d4a75-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d4a75-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d4a75-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d4a75-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4a75-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4a75-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a75-131">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d4a75-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d4a75-132">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d4a75-132">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 






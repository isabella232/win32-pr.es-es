---
title: Propiedad de ancho de banda IWMPNetwork
description: La propiedad de ancho de banda obtiene el ancho de banda actual del elemento multimedia.
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- propiedades de ancho de banda Media Player de Windows
- propiedad de ancho de banda Media Player de Windows, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad ancho de banda
topic_type:
- apiref
api_name:
- IWMPNetwork.bandWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9a55f9d5c6724c428b75a4171c2e8b7ca13d18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699578"
---
# <a name="iwmpnetworkbandwidth-property"></a><span data-ttu-id="56662-106">IWMPNetwork:: bandWidth (propiedad)</span><span class="sxs-lookup"><span data-stu-id="56662-106">IWMPNetwork::bandWidth property</span></span>

<span data-ttu-id="56662-107">La propiedad de **ancho** de banda obtiene el ancho de banda actual del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="56662-107">The **bandWidth** property gets the current bandwidth of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="56662-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56662-108">Syntax</span></span>


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="56662-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="56662-109">Property value</span></span>

<span data-ttu-id="56662-110">**System. Int32** que es el ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="56662-110">A **System.Int32** that is the bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="56662-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56662-111">Remarks</span></span>

<span data-ttu-id="56662-112">El valor recuperado a través de **AxWindowsMediaPlayer. URL** será cero si no se establece la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="56662-112">The value retrieved through **AxWindowsMediaPlayer.URL** will be zero if the URL is not set.</span></span> <span data-ttu-id="56662-113">Esta propiedad solo es válida para los medios de streaming.</span><span class="sxs-lookup"><span data-stu-id="56662-113">This property is valid only for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="56662-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56662-114">Examples</span></span>

<span data-ttu-id="56662-115">En el ejemplo siguiente se usa **ancho de banda** para mostrar el ancho de banda multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="56662-115">The following example uses **bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="56662-116">La información se muestra en una etiqueta en respuesta al evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="56662-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="56662-117">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="56662-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bandwidth when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bandWidth != 0)
            {
                bandWidthLabel.Text = "Current Bandwidth: " + player.network.bandWidth + " K bits/second";
            }
            else
            {
                bandWidthLabel.Text = "Bandwidth is only available for streaming media.";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the bandWidth when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bandWidth <> 0) Then

                bandWidthLabel.Text = &quot;Current Bandwidth: &quot; + player.network.bandWidth + &quot; K bits/second&quot;

            Else

                bandWidthLabel.Text = &quot;Bandwidth is only available for streaming media.&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="56662-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56662-118">Requirements</span></span>



| <span data-ttu-id="56662-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="56662-119">Requirement</span></span> | <span data-ttu-id="56662-120">Value</span><span class="sxs-lookup"><span data-stu-id="56662-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56662-121">Versión</span><span class="sxs-lookup"><span data-stu-id="56662-121">Version</span></span><br/>   | <span data-ttu-id="56662-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="56662-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="56662-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56662-123">Namespace</span></span><br/> | <span data-ttu-id="56662-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="56662-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="56662-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="56662-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="56662-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="56662-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56662-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="56662-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56662-128">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="56662-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56662-129">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="56662-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 






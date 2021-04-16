---
title: Propiedad de velocidad de bits IWMPNetwork
description: La propiedad de velocidad de bits obtiene la velocidad de bits actual recibida.
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- propiedades de velocidad de bits Media Player de Windows
- propiedad de velocidad de bits Media Player Windows, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad de velocidad de bits
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64039eb960a928f5268643e18d1a01b9034d5d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699347"
---
# <a name="iwmpnetworkbitrate-property"></a><span data-ttu-id="e6ab0-106">IWMPNetwork:: bitrate (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e6ab0-106">IWMPNetwork::bitRate property</span></span>

<span data-ttu-id="e6ab0-107">La propiedad de **velocidad** de bits obtiene la velocidad de bits actual recibida.</span><span class="sxs-lookup"><span data-stu-id="e6ab0-107">The **bitRate** property gets the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6ab0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6ab0-108">Syntax</span></span>


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e6ab0-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e6ab0-109">Property value</span></span>

<span data-ttu-id="e6ab0-110">**System. Int32** que es la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="e6ab0-110">A **System.Int32** that is the bit rate.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6ab0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6ab0-111">Remarks</span></span>

<span data-ttu-id="e6ab0-112">El valor de esta propiedad es una combinación de las velocidades de bits de las secuencias de vídeo y de audio.</span><span class="sxs-lookup"><span data-stu-id="e6ab0-112">The value of this property is a combination of the bit rates of both video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="e6ab0-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e6ab0-113">Examples</span></span>

<span data-ttu-id="e6ab0-114">En el ejemplo siguiente se usa **la velocidad de** bits para mostrar la velocidad de bits multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="e6ab0-114">The following example uses **bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="e6ab0-115">La información se muestra en una etiqueta en respuesta al evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e6ab0-115">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="e6ab0-116">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="e6ab0-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
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

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e6ab0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6ab0-117">Requirements</span></span>



| <span data-ttu-id="e6ab0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6ab0-118">Requirement</span></span> | <span data-ttu-id="e6ab0-119">Value</span><span class="sxs-lookup"><span data-stu-id="e6ab0-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ab0-120">Versión</span><span class="sxs-lookup"><span data-stu-id="e6ab0-120">Version</span></span><br/>   | <span data-ttu-id="e6ab0-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="e6ab0-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e6ab0-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e6ab0-122">Namespace</span></span><br/> | <span data-ttu-id="e6ab0-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e6ab0-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e6ab0-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="e6ab0-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e6ab0-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e6ab0-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6ab0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6ab0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ab0-127">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e6ab0-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 






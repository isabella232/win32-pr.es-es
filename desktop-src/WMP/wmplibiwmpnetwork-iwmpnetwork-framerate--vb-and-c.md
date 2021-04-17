---
title: Propiedad de velocidad de fotogramas IWMPNetwork
description: La propiedad de velocidad de fotogramas obtiene la velocidad de fotogramas de vídeo actual.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- propiedades de velocidad de fotogramas Media Player Windows
- propiedad de velocidad de fotogramas Media Player Windows, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad de velocidad de fotogramas
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670501"
---
# <a name="iwmpnetworkframerate-property"></a><span data-ttu-id="02229-106">IWMPNetwork:: fotogramas (propiedad)</span><span class="sxs-lookup"><span data-stu-id="02229-106">IWMPNetwork::frameRate property</span></span>

<span data-ttu-id="02229-107">La propiedad de **velocidad** de fotogramas obtiene la velocidad de fotogramas de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="02229-107">The **frameRate** property gets the current video frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="02229-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02229-108">Syntax</span></span>


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="02229-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="02229-109">Property value</span></span>

<span data-ttu-id="02229-110">**System. Int32** que es la velocidad de fotogramas actual en fotogramas por cien segundos.</span><span class="sxs-lookup"><span data-stu-id="02229-110">A **System.Int32** that is the current frame rate in frames per hundred seconds.</span></span>

> [!Note]  
> <span data-ttu-id="02229-111">Aunque la propiedad **encodedFrameRate** mide la velocidad de fotogramas codificada en fotogramas por segundo, la propiedad de **velocidad** de fotogramas mide la velocidad de fotogramas actual en fotogramas por cien segundos.</span><span class="sxs-lookup"><span data-stu-id="02229-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="02229-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="02229-112">See Remarks.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="02229-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02229-113">Remarks</span></span>

<span data-ttu-id="02229-114">El valor de velocidad de fotogramas actual se devuelve en fotogramas por cien segundos.</span><span class="sxs-lookup"><span data-stu-id="02229-114">The current frame rate value is returned in frames per hundred seconds.</span></span> <span data-ttu-id="02229-115">Por ejemplo, un valor de 2998 indica 29,98 fotogramas por segundo (FPS).</span><span class="sxs-lookup"><span data-stu-id="02229-115">For example, a value of 2998 indicates 29.98 frames per second (fps).</span></span>

## <a name="examples"></a><span data-ttu-id="02229-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="02229-116">Examples</span></span>

<span data-ttu-id="02229-117">En el ejemplo de código siguiente se usa **velocidad** de fotogramas para mostrar la velocidad de fotogramas especificada al codificar el archivo.</span><span class="sxs-lookup"><span data-stu-id="02229-117">The following code example uses **frameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="02229-118">La información se muestra en una etiqueta en respuesta al evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="02229-118">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="02229-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="02229-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="02229-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02229-120">Requirements</span></span>



| <span data-ttu-id="02229-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="02229-121">Requirement</span></span> | <span data-ttu-id="02229-122">Value</span><span class="sxs-lookup"><span data-stu-id="02229-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02229-123">Versión</span><span class="sxs-lookup"><span data-stu-id="02229-123">Version</span></span><br/>   | <span data-ttu-id="02229-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="02229-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="02229-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="02229-125">Namespace</span></span><br/> | <span data-ttu-id="02229-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="02229-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="02229-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="02229-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="02229-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="02229-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02229-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="02229-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02229-130">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="02229-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="02229-131">**IWMPNetwork. encodedFrameRate (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="02229-131">**IWMPNetwork.encodedFrameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 






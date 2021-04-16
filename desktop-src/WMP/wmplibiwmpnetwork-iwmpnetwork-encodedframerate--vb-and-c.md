---
title: Propiedad encodedFrameRate de IWMPNetwork
description: La propiedad encodedFrameRate obtiene la velocidad de fotogramas de vídeo especificada por el autor del contenido.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- propiedades de encodedFrameRate Media Player de Windows
- propiedad encodedFrameRate de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad encodedFrameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4176a9c2492d0ce34ffd0936c48dbdef065d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670391"
---
# <a name="iwmpnetworkencodedframerate-property"></a><span data-ttu-id="5051e-106">IWMPNetwork:: encodedFrameRate (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5051e-106">IWMPNetwork::encodedFrameRate property</span></span>

<span data-ttu-id="5051e-107">La propiedad **encodedFrameRate** obtiene la velocidad de fotogramas de vídeo especificada por el autor del contenido.</span><span class="sxs-lookup"><span data-stu-id="5051e-107">The **encodedFrameRate** property gets the video frame rate specified by the content author.</span></span>

## <a name="syntax"></a><span data-ttu-id="5051e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5051e-108">Syntax</span></span>


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5051e-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5051e-109">Property value</span></span>

<span data-ttu-id="5051e-110">**System. Int32** que es la velocidad de fotogramas codificada en fotogramas por segundo (FPS).</span><span class="sxs-lookup"><span data-stu-id="5051e-110">A **System.Int32** that is the encoded frame rate in frames per second (fps).</span></span>

> [!Note]  
> <span data-ttu-id="5051e-111">Aunque la propiedad **encodedFrameRate** mide la velocidad de fotogramas codificada en fotogramas por segundo, la propiedad de **velocidad** de fotogramas mide la velocidad de fotogramas actual en fotogramas por cien segundos.</span><span class="sxs-lookup"><span data-stu-id="5051e-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5051e-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5051e-112">Examples</span></span>

<span data-ttu-id="5051e-113">En el ejemplo de código siguiente se usa **encodedFrameRate** para mostrar la velocidad de fotogramas especificada al codificar el archivo.</span><span class="sxs-lookup"><span data-stu-id="5051e-113">The following code example uses **encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="5051e-114">La información se muestra en una etiqueta, en respuesta al evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="5051e-114">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="5051e-115">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="5051e-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
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

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5051e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5051e-116">Requirements</span></span>



| <span data-ttu-id="5051e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5051e-117">Requirement</span></span> | <span data-ttu-id="5051e-118">Value</span><span class="sxs-lookup"><span data-stu-id="5051e-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5051e-119">Versión</span><span class="sxs-lookup"><span data-stu-id="5051e-119">Version</span></span><br/>   | <span data-ttu-id="5051e-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="5051e-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5051e-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5051e-121">Namespace</span></span><br/> | <span data-ttu-id="5051e-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5051e-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5051e-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="5051e-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5051e-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5051e-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5051e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5051e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5051e-126">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5051e-126">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5051e-127">**IWMPNetwork. velocidad de fotogramas (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5051e-127">**IWMPNetwork.frameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 






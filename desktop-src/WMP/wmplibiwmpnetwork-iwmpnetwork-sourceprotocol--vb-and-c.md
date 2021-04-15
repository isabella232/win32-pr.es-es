---
title: Propiedad sourceProtocol de IWMPNetwork
description: La propiedad sourceProtocol obtiene el protocolo de origen usado para recibir los datos.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- propiedades de sourceProtocol Media Player de Windows
- propiedad sourceProtocol de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad sourceProtocol
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5017e1a053c124a1f7f50668c6f392eb541d57f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709236"
---
# <a name="iwmpnetworksourceprotocol-property"></a><span data-ttu-id="f02cf-106">IWMPNetwork:: sourceProtocol (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f02cf-106">IWMPNetwork::sourceProtocol property</span></span>

<span data-ttu-id="f02cf-107">La propiedad **sourceProtocol** obtiene el protocolo de origen usado para recibir los datos.</span><span class="sxs-lookup"><span data-stu-id="f02cf-107">The **sourceProtocol** property gets the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f02cf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f02cf-108">Syntax</span></span>


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a><span data-ttu-id="f02cf-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f02cf-109">Property value</span></span>

<span data-ttu-id="f02cf-110">**System. String** que es el nombre del Protocolo de origen.</span><span class="sxs-lookup"><span data-stu-id="f02cf-110">A **System.String** that is the name of the source protocol.</span></span>

## <a name="remarks"></a><span data-ttu-id="f02cf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f02cf-111">Remarks</span></span>

<span data-ttu-id="f02cf-112">Esta propiedad obtiene una cadena de longitud cero ("") al reproducir un CD o un DVD.</span><span class="sxs-lookup"><span data-stu-id="f02cf-112">This property gets a zero-length string ("") when playing a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="f02cf-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f02cf-113">Examples</span></span>

<span data-ttu-id="f02cf-114">En el ejemplo de código siguiente se usa **sourceProtocol** para mostrar el protocolo de origen usado para recibir datos.</span><span class="sxs-lookup"><span data-stu-id="f02cf-114">The following code example uses **sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="f02cf-115">La información se muestra en una etiqueta, en respuesta al evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f02cf-115">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="f02cf-116">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="f02cf-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f02cf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f02cf-117">Requirements</span></span>



| <span data-ttu-id="f02cf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f02cf-118">Requirement</span></span> | <span data-ttu-id="f02cf-119">Value</span><span class="sxs-lookup"><span data-stu-id="f02cf-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02cf-120">Versión</span><span class="sxs-lookup"><span data-stu-id="f02cf-120">Version</span></span><br/>   | <span data-ttu-id="f02cf-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="f02cf-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f02cf-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f02cf-122">Namespace</span></span><br/> | <span data-ttu-id="f02cf-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f02cf-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f02cf-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="f02cf-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f02cf-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f02cf-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f02cf-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f02cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f02cf-127">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f02cf-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 






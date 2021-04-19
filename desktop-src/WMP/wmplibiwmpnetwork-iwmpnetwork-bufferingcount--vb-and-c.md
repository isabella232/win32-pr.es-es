---
title: Propiedad bufferingCount de IWMPNetwork
description: La propiedad bufferingCount obtiene el número de veces que se ha producido el almacenamiento en búfer durante la reproducción.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- propiedades de bufferingCount Media Player de Windows
- propiedad bufferingCount de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad bufferingCount
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4958892dd9784ee72b51adfedbbcdee81817b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699346"
---
# <a name="iwmpnetworkbufferingcount-property"></a><span data-ttu-id="15e3b-106">IWMPNetwork:: bufferingCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="15e3b-106">IWMPNetwork::bufferingCount property</span></span>

<span data-ttu-id="15e3b-107">La propiedad **bufferingCount** obtiene el número de veces que se ha producido el almacenamiento en búfer durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="15e3b-107">The **bufferingCount** property gets the number of times buffering occurred during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e3b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15e3b-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="15e3b-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="15e3b-109">Property value</span></span>

<span data-ttu-id="15e3b-110">**System. Int32** que es el recuento de almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="15e3b-110">A **System.Int32** that is the buffering count.</span></span>

## <a name="remarks"></a><span data-ttu-id="15e3b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15e3b-111">Remarks</span></span>

<span data-ttu-id="15e3b-112">Cada vez que se detiene y se reinicia la reproducción, esta propiedad se restablece en cero.</span><span class="sxs-lookup"><span data-stu-id="15e3b-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="15e3b-113">No se restablece si la reproducción está en pausa.</span><span class="sxs-lookup"><span data-stu-id="15e3b-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="15e3b-114">El almacenamiento en búfer solo se aplica al contenido de streaming.</span><span class="sxs-lookup"><span data-stu-id="15e3b-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="15e3b-115">Esta propiedad obtiene información válida solo durante el tiempo de ejecución cuando se establece la dirección URL para la reproducción mediante la propiedad **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="15e3b-115">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="15e3b-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="15e3b-116">Examples</span></span>

<span data-ttu-id="15e3b-117">En el ejemplo siguiente se usa *bufferingCount* para mostrar el número de veces que se produce el almacenamiento en búfer durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="15e3b-117">The following example uses *bufferingCount* to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="15e3b-118">La información se muestra en una etiqueta en respuesta al evento de almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="15e3b-118">The information is displayed in a label in response to the Buffering Event.</span></span> <span data-ttu-id="15e3b-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="15e3b-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="15e3b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15e3b-120">Requirements</span></span>



| <span data-ttu-id="15e3b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="15e3b-121">Requirement</span></span> | <span data-ttu-id="15e3b-122">Value</span><span class="sxs-lookup"><span data-stu-id="15e3b-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15e3b-123">Versión</span><span class="sxs-lookup"><span data-stu-id="15e3b-123">Version</span></span><br/>   | <span data-ttu-id="15e3b-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="15e3b-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="15e3b-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15e3b-125">Namespace</span></span><br/> | <span data-ttu-id="15e3b-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="15e3b-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="15e3b-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="15e3b-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="15e3b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="15e3b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15e3b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="15e3b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e3b-130">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="15e3b-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="15e3b-131">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="15e3b-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 






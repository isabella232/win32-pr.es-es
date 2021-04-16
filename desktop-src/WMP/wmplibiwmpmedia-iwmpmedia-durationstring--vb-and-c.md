---
title: Propiedad durationString de IWMPMedia
description: La propiedad durationString obtiene una cadena que indica la duración del elemento multimedia actual en formato HH MM SS.
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- propiedades de durationString Media Player de Windows
- propiedad durationString de Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, propiedad durationString
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671590"
---
# <a name="iwmpmediadurationstring-property"></a><span data-ttu-id="8db72-106">IWMPMedia::d propiedad urationString</span><span class="sxs-lookup"><span data-stu-id="8db72-106">IWMPMedia::durationString property</span></span>

<span data-ttu-id="8db72-107">La propiedad **durationString** obtiene una cadena que indica la duración del elemento multimedia actual en formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="8db72-107">The **durationString** property gets a string indicating the duration of the current media item in HH:MM:SS format.</span></span>

<span data-ttu-id="8db72-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8db72-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db72-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8db72-109">Syntax</span></span>


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a><span data-ttu-id="8db72-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8db72-110">Property value</span></span>

<span data-ttu-id="8db72-111">**System. String** que es la duración.</span><span class="sxs-lookup"><span data-stu-id="8db72-111">A **System.String** that is the duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="8db72-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8db72-112">Remarks</span></span>

<span data-ttu-id="8db72-113">Si esta propiedad se usa con un elemento multimedia distinto del especificado en AxWindowsMediaPlayer. currentMedia, puede que no contenga un valor válido.</span><span class="sxs-lookup"><span data-stu-id="8db72-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span> <span data-ttu-id="8db72-114">Si el elemento multimedia tiene una longitud inferior a una hora, se omite la parte de horas del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="8db72-114">If the media item is less than an hour long, the hours portion of the return value is omitted.</span></span>

<span data-ttu-id="8db72-115">Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8db72-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="8db72-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8db72-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8db72-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8db72-117">Examples</span></span>

<span data-ttu-id="8db72-118">En el ejemplo siguiente se usa **durationString** para mostrar la duración del elemento multimedia actual como texto con formato en una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="8db72-118">The following example uses **durationString** to display the duration of the current media item as formatted text in a label.</span></span> <span data-ttu-id="8db72-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="8db72-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="8db72-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8db72-120">Requirements</span></span>



| <span data-ttu-id="8db72-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8db72-121">Requirement</span></span> | <span data-ttu-id="8db72-122">Value</span><span class="sxs-lookup"><span data-stu-id="8db72-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8db72-123">Versión</span><span class="sxs-lookup"><span data-stu-id="8db72-123">Version</span></span><br/>   | <span data-ttu-id="8db72-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="8db72-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8db72-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8db72-125">Namespace</span></span><br/> | <span data-ttu-id="8db72-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8db72-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8db72-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="8db72-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8db72-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8db72-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db72-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8db72-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db72-130">**AxWindowsMediaPlayer. currentMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="8db72-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8db72-131">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="8db72-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8db72-132">**IWMPMedia. Duration (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="8db72-132">**IWMPMedia.duration (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 






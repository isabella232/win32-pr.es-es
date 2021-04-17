---
title: Evento CurrentItemChange del objeto AxWindowsMediaPlayer
description: El evento CurrentItemChange se produce cuando cambia el valor de IWMPControls. currentItem.
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- Evento CurrentItemChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c33bb3e9c4c1e512e742c0e679f3c5b53a29735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698730"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="acbe0-104">Evento CurrentItemChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="acbe0-104">CurrentItemChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="acbe0-105">El evento CurrentItemChange se produce cuando el valor de IWMPControls. **CurrentItem** cambia.</span><span class="sxs-lookup"><span data-stu-id="acbe0-105">The CurrentItemChange event occurs when the value of IWMPControls.**currentItem** changes.</span></span>

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a><span data-ttu-id="acbe0-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="acbe0-106">Event Data</span></span>

<span data-ttu-id="acbe0-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="acbe0-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEventHandler**.</span></span> <span data-ttu-id="acbe0-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="acbe0-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="acbe0-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="acbe0-109">Property</span></span>   | <span data-ttu-id="acbe0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="acbe0-110">Description</span></span>                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acbe0-111">pdispMedia</span><span class="sxs-lookup"><span data-stu-id="acbe0-111">pdispMedia</span></span> | <span data-ttu-id="acbe0-112">System. ObjectThe nuevo elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="acbe0-112">System.ObjectThe new current media item.</span></span> <span data-ttu-id="acbe0-113">Puede convertirlo en una interfaz IWMPMedia para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="acbe0-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="acbe0-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="acbe0-114">Examples</span></span>

<span data-ttu-id="acbe0-115">En el ejemplo siguiente se muestra un controlador de eventos para el evento CurrentItemChange.</span><span class="sxs-lookup"><span data-stu-id="acbe0-115">The following example demonstrates an event handler for the CurrentItemChange event.</span></span> <span data-ttu-id="acbe0-116">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="acbe0-116">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="acbe0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acbe0-117">Requirements</span></span>



| <span data-ttu-id="acbe0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="acbe0-118">Requirement</span></span> | <span data-ttu-id="acbe0-119">Value</span><span class="sxs-lookup"><span data-stu-id="acbe0-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acbe0-120">Versión</span><span class="sxs-lookup"><span data-stu-id="acbe0-120">Version</span></span><br/>   | <span data-ttu-id="acbe0-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="acbe0-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="acbe0-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="acbe0-122">Namespace</span></span><br/> | <span data-ttu-id="acbe0-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="acbe0-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="acbe0-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="acbe0-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="acbe0-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="acbe0-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acbe0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="acbe0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acbe0-127">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="acbe0-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="acbe0-128">**IWMPControls. currentItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="acbe0-128">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="acbe0-129">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="acbe0-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






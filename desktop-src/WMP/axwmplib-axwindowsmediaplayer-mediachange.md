---
title: Evento MediaChange del objeto AxWindowsMediaPlayer
description: El evento MediaChange se produce cuando cambia un elemento multimedia. | Evento MediaChange del objeto AxWindowsMediaPlayer
ms.assetid: 0a2380ff-df50-4092-a952-812184822719
keywords:
- Evento MediaChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- MediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175a7ed6ca57e3083d307cfe218d09233410053c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699833"
---
# <a name="mediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4f7ce-105">Evento MediaChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4f7ce-105">MediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4f7ce-106">El evento MediaChange se produce cuando cambia un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4f7ce-106">The MediaChange event occurs when a media item changes.</span></span>

``` syntax
[C#]
private void player_MediaChange(
  object sender,
  _WMPOCXEvents_MediaChangeEvent e
)

[Visual Basic]
Private Sub player_MediaChange(  
  sender As Object,  
  e As _WMPOCXEvents_MediaChangeEvent
) Handles player.MediaChange
```

## <a name="event-data"></a><span data-ttu-id="4f7ce-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="4f7ce-107">Event Data</span></span>

<span data-ttu-id="4f7ce-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4f7ce-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEventHandler**.</span></span> <span data-ttu-id="4f7ce-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="4f7ce-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="4f7ce-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4f7ce-110">Property</span></span> | <span data-ttu-id="4f7ce-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f7ce-111">Description</span></span>                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f7ce-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="4f7ce-112">Item</span></span>     | <span data-ttu-id="4f7ce-113">Elemento multimedia System. ObjectThe que cambió.</span><span class="sxs-lookup"><span data-stu-id="4f7ce-113">System.ObjectThe media item that changed.</span></span> <span data-ttu-id="4f7ce-114">Puede convertirlo en una interfaz IWMPMedia para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="4f7ce-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="4f7ce-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4f7ce-115">Examples</span></span>

<span data-ttu-id="4f7ce-116">En el ejemplo siguiente se utiliza una etiqueta para mostrar el nombre del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="4f7ce-116">The following example uses a label to display the name of the current media item.</span></span> <span data-ttu-id="4f7ce-117">El código actualiza el texto de la etiqueta con cada aparición del evento MediaChange.</span><span class="sxs-lookup"><span data-stu-id="4f7ce-117">The code updates the text in the label with each occurrence of the MediaChange Event.</span></span> <span data-ttu-id="4f7ce-118">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="4f7ce-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the MediaChange event.
player.MediaChange += new AxWMPLib._WMPOCXEvents_MediaChangeEventHandler(player_MediaChange);

private void player_MediaChange(object sender, AxWMPLib._WMPOCXEvents_MediaChangeEvent e)
{
    // Get an interface to the changed media item that is returned in the event data. 
    WMPLib.IWMPMedia3 changedItem = (WMPLib.IWMPMedia3)e.item;

    // Display the name of the changed media item.
    mediaName.Text = changedItem.name;
}
```


```VB

Public Sub player_MediaChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_MediaChangeEvent) Handles player.MediaChange

    &#39; Get an interface to the changed media item that is returned in the event data.
    Dim changedItem As WMPLib.IWMPMedia3 = e.item

    &#39; Display the name of the changed media item.
    mediaName.Text = changedItem.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4f7ce-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f7ce-119">Requirements</span></span>



| <span data-ttu-id="4f7ce-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f7ce-120">Requirement</span></span> | <span data-ttu-id="4f7ce-121">Value</span><span class="sxs-lookup"><span data-stu-id="4f7ce-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f7ce-122">Versión</span><span class="sxs-lookup"><span data-stu-id="4f7ce-122">Version</span></span><br/>   | <span data-ttu-id="4f7ce-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="4f7ce-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4f7ce-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f7ce-124">Namespace</span></span><br/> | <span data-ttu-id="4f7ce-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4f7ce-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4f7ce-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="4f7ce-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4f7ce-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4f7ce-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f7ce-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f7ce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f7ce-129">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4f7ce-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f7ce-130">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4f7ce-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






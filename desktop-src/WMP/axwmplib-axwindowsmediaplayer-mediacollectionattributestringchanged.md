---
title: Evento MediaCollectionAttributeStringChanged del objeto AxWindowsMediaPlayer
description: El evento MediaCollectionAttributeStringChanged se produce cuando se cambia un valor de atributo en la biblioteca. | Evento MediaCollectionAttributeStringChanged del objeto AxWindowsMediaPlayer
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- Evento MediaCollectionAttributeStringChanged del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b83d8036ca0dca7f79e2a9ba721830447f9c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700155"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="60b82-105">Evento MediaCollectionAttributeStringChanged del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="60b82-105">MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="60b82-106">El evento MediaCollectionAttributeStringChanged se produce cuando se cambia un valor de atributo en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="60b82-106">The MediaCollectionAttributeStringChanged event occurs when an attribute value in the library is changed.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a><span data-ttu-id="60b82-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="60b82-107">Event Data</span></span>

<span data-ttu-id="60b82-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="60b82-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEventHandler**.</span></span> <span data-ttu-id="60b82-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="60b82-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="60b82-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60b82-110">Property</span></span>         | <span data-ttu-id="60b82-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="60b82-111">Description</span></span>                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b82-112">bstrAttribName</span><span class="sxs-lookup"><span data-stu-id="60b82-112">bstrAttribName</span></span>   | <span data-ttu-id="60b82-113">System. StringSpecifies el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="60b82-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="60b82-114">Para obtener información sobre los atributos que admite Windows Media Player, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="60b82-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="60b82-115">bstrOldAttribVal</span><span class="sxs-lookup"><span data-stu-id="60b82-115">bstrOldAttribVal</span></span> | <span data-ttu-id="60b82-116">System. StringSpecifies el valor anterior del atributo.</span><span class="sxs-lookup"><span data-stu-id="60b82-116">System.StringSpecifies the old value of the attribute.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="60b82-117">bstrNewAttribVal</span><span class="sxs-lookup"><span data-stu-id="60b82-117">bstrNewAttribVal</span></span> | <span data-ttu-id="60b82-118">System. StringSpecifies el nuevo valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="60b82-118">System.StringSpecifies the new value of the attribute.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="60b82-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60b82-119">Remarks</span></span>

<span data-ttu-id="60b82-120">Cuando un usuario modifica los metadatos de la biblioteca, la colección de medios se actualiza y este evento se desencadena para cada atributo modificado.</span><span class="sxs-lookup"><span data-stu-id="60b82-120">When a user modifies library metadata, the media collection is updated and this event fires for each attribute changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b82-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60b82-121">Requirements</span></span>



| <span data-ttu-id="60b82-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="60b82-122">Requirement</span></span> | <span data-ttu-id="60b82-123">Value</span><span class="sxs-lookup"><span data-stu-id="60b82-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b82-124">Versión</span><span class="sxs-lookup"><span data-stu-id="60b82-124">Version</span></span><br/>   | <span data-ttu-id="60b82-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="60b82-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="60b82-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60b82-126">Namespace</span></span><br/> | <span data-ttu-id="60b82-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="60b82-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="60b82-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="60b82-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="60b82-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="60b82-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b82-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="60b82-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b82-131">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="60b82-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="60b82-132">**AxWindowsMediaPlayer. mediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="60b82-132">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="60b82-133">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="60b82-133">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 






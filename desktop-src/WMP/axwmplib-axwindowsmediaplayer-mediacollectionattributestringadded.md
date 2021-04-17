---
title: Evento MediaCollectionAttributeStringAdded del objeto AxWindowsMediaPlayer
description: El evento MediaCollectionAttributeStringAdded se produce cuando se agrega un valor de atributo a la biblioteca. | Evento MediaCollectionAttributeStringAdded del objeto AxWindowsMediaPlayer
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- Evento MediaCollectionAttributeStringAdded del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698688"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="96241-105">Evento MediaCollectionAttributeStringAdded del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="96241-105">MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="96241-106">El evento MediaCollectionAttributeStringAdded se produce cuando se agrega un valor de atributo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="96241-106">The MediaCollectionAttributeStringAdded event occurs when an attribute value is added to the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a><span data-ttu-id="96241-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="96241-107">Event Data</span></span>

<span data-ttu-id="96241-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="96241-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEventHandler**.</span></span> <span data-ttu-id="96241-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="96241-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="96241-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96241-110">Property</span></span>           | <span data-ttu-id="96241-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="96241-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96241-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="96241-112">**bstrAttribName**</span></span> | <span data-ttu-id="96241-113">System. StringSpecifies el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="96241-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="96241-114">Para obtener información sobre los atributos que admite Windows Media Player, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="96241-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="96241-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="96241-115">bstrAttribVal</span></span>      | <span data-ttu-id="96241-116">System. StringSpecifies el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="96241-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="96241-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96241-117">Remarks</span></span>

<span data-ttu-id="96241-118">Cuando se agrega un elemento multimedia a la biblioteca, sus metadatos se agregan a la colección de medios y este evento se desencadena para cada atributo agregado.</span><span class="sxs-lookup"><span data-stu-id="96241-118">When a media item is added to the library, its metadata is added to the media collection and this event is fired for each attribute added.</span></span>

## <a name="requirements"></a><span data-ttu-id="96241-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96241-119">Requirements</span></span>



| <span data-ttu-id="96241-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="96241-120">Requirement</span></span> | <span data-ttu-id="96241-121">Value</span><span class="sxs-lookup"><span data-stu-id="96241-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96241-122">Versión</span><span class="sxs-lookup"><span data-stu-id="96241-122">Version</span></span><br/>   | <span data-ttu-id="96241-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="96241-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="96241-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="96241-124">Namespace</span></span><br/> | <span data-ttu-id="96241-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="96241-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="96241-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="96241-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="96241-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="96241-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96241-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="96241-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96241-129">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="96241-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="96241-130">**AxWindowsMediaPlayer. mediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="96241-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="96241-131">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="96241-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 






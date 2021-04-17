---
title: Evento MediaCollectionAttributeStringRemoved del objeto AxWindowsMediaPlayer
description: El evento MediaCollectionAttributeStringRemoved se produce cuando se quita un valor de atributo de la biblioteca. | Evento MediaCollectionAttributeStringRemoved del objeto AxWindowsMediaPlayer
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Evento MediaCollectionAttributeStringRemoved del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698632"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d3f2d-105">Evento MediaCollectionAttributeStringRemoved del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d3f2d-105">MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d3f2d-106">El evento MediaCollectionAttributeStringRemoved se produce cuando se quita un valor de atributo de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-106">The MediaCollectionAttributeStringRemoved event occurs when an attribute value is removed from the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a><span data-ttu-id="d3f2d-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="d3f2d-107">Event Data</span></span>

<span data-ttu-id="d3f2d-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEventHandler**.</span></span> <span data-ttu-id="d3f2d-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="d3f2d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d3f2d-110">Property</span></span>           | <span data-ttu-id="d3f2d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3f2d-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f2d-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="d3f2d-112">**bstrAttribName**</span></span> | <span data-ttu-id="d3f2d-113">System. StringSpecifies el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="d3f2d-114">Para obtener información sobre los atributos que admite Windows Media Player, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d3f2d-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="d3f2d-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="d3f2d-115">bstrAttribVal</span></span>      | <span data-ttu-id="d3f2d-116">System. StringSpecifies el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="d3f2d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3f2d-117">Remarks</span></span>

<span data-ttu-id="d3f2d-118">Cuando se quita un elemento multimedia de la biblioteca, sus metadatos se quitan del **MediaCollection** y este evento se desencadena para cada atributo que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="d3f2d-118">When a media item is removed from the library, its metadata is removed from the **MediaCollection** and this event is fired for each attribute removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f2d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3f2d-119">Requirements</span></span>



| <span data-ttu-id="d3f2d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f2d-120">Requirement</span></span> | <span data-ttu-id="d3f2d-121">Value</span><span class="sxs-lookup"><span data-stu-id="d3f2d-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f2d-122">Versión</span><span class="sxs-lookup"><span data-stu-id="d3f2d-122">Version</span></span><br/>   | <span data-ttu-id="d3f2d-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="d3f2d-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d3f2d-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d3f2d-124">Namespace</span></span><br/> | <span data-ttu-id="d3f2d-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d3f2d-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d3f2d-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d3f2d-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d3f2d-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f2d-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f2d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3f2d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f2d-129">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d3f2d-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d3f2d-130">**AxWindowsMediaPlayer. mediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d3f2d-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d3f2d-131">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d3f2d-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 






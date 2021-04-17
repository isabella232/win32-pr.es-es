---
title: Evento MediaCollectionMediaAdded del objeto AxWindowsMediaPlayer
description: El evento MediaCollectionMediaAdded se produce cuando se agrega un elemento multimedia a la biblioteca local. | Evento MediaCollectionMediaAdded del objeto AxWindowsMediaPlayer
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- Evento MediaCollectionMediaAdded del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb839fccf9a5048b5647480eca36fcfcaeb904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700149"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4d781-105">Evento MediaCollectionMediaAdded del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4d781-105">MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4d781-106">El evento MediaCollectionMediaAdded se produce cuando se agrega un elemento multimedia a la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="4d781-106">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a><span data-ttu-id="4d781-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="4d781-107">Event Data</span></span>

<span data-ttu-id="4d781-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4d781-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEventHandler**.</span></span> <span data-ttu-id="4d781-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="4d781-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="4d781-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d781-110">Property</span></span> | <span data-ttu-id="4d781-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d781-111">Description</span></span>                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d781-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="4d781-112">pMedia</span></span>   | <span data-ttu-id="4d781-113">Elemento multimedia System. ObjectThe agregado a la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="4d781-113">System.ObjectThe media item added to the local library.</span></span> <span data-ttu-id="4d781-114">Puede convertirlo en una interfaz IWMPMedia para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="4d781-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4d781-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d781-115">Remarks</span></span>

<span data-ttu-id="4d781-116">Este evento solo se produce para la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="4d781-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d781-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d781-117">Requirements</span></span>



| <span data-ttu-id="4d781-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d781-118">Requirement</span></span> | <span data-ttu-id="4d781-119">Value</span><span class="sxs-lookup"><span data-stu-id="4d781-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d781-120">Versión</span><span class="sxs-lookup"><span data-stu-id="4d781-120">Version</span></span><br/>   | <span data-ttu-id="4d781-121">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="4d781-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="4d781-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d781-122">Namespace</span></span><br/> | <span data-ttu-id="4d781-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4d781-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4d781-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="4d781-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4d781-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4d781-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d781-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d781-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d781-127">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4d781-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4d781-128">**AxWindowsMediaPlayer. mediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4d781-128">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4d781-129">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4d781-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4d781-130">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4d781-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 






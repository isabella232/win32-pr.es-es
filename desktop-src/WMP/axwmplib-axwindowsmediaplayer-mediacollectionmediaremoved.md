---
title: Evento MediaCollectionMediaRemoved del objeto AxWindowsMediaPlayer
description: El evento MediaCollectionMediaRemoved se produce cuando se quita un elemento multimedia de la biblioteca local. | Evento MediaCollectionMediaRemoved del objeto AxWindowsMediaPlayer
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- Evento MediaCollectionMediaRemoved del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700148"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d8444-105">Evento MediaCollectionMediaRemoved del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d8444-105">MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d8444-106">El evento MediaCollectionMediaRemoved se produce cuando se quita un elemento multimedia de la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="d8444-106">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a><span data-ttu-id="d8444-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="d8444-107">Event Data</span></span>

<span data-ttu-id="d8444-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="d8444-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEventHandler**.</span></span> <span data-ttu-id="d8444-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="d8444-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="d8444-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d8444-110">Property</span></span> | <span data-ttu-id="d8444-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8444-111">Description</span></span>                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8444-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="d8444-112">pMedia</span></span>   | <span data-ttu-id="d8444-113">Elemento multimedia System. ObjectThe quitado de la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="d8444-113">System.ObjectThe media item removed from the local library.</span></span> <span data-ttu-id="d8444-114">Puede convertirlo en una interfaz IWMPMedia para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="d8444-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d8444-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8444-115">Remarks</span></span>

<span data-ttu-id="d8444-116">Este evento solo se produce para la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="d8444-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8444-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8444-117">Requirements</span></span>



| <span data-ttu-id="d8444-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8444-118">Requirement</span></span> | <span data-ttu-id="d8444-119">Value</span><span class="sxs-lookup"><span data-stu-id="d8444-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8444-120">Versión</span><span class="sxs-lookup"><span data-stu-id="d8444-120">Version</span></span><br/>   | <span data-ttu-id="d8444-121">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="d8444-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="d8444-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d8444-122">Namespace</span></span><br/> | <span data-ttu-id="d8444-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d8444-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d8444-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d8444-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d8444-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d8444-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8444-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8444-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8444-127">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d8444-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8444-128">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d8444-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






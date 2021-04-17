---
title: Evento PlaylistCollectionPlaylistRemoved del objeto AxWindowsMediaPlayer
description: El evento PlaylistCollectionPlaylistRemoved se produce cuando se quita una lista de reproducción de la colección de listas de reproducción. | Evento PlaylistCollectionPlaylistRemoved del objeto AxWindowsMediaPlayer
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- Evento PlaylistCollectionPlaylistRemoved del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700218"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="16654-105">Evento PlaylistCollectionPlaylistRemoved del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="16654-105">PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="16654-106">El evento PlaylistCollectionPlaylistRemoved se produce cuando se quita una lista de reproducción de la colección de listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="16654-106">The PlaylistCollectionPlaylistRemoved event occurs when a playlist is removed from the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a><span data-ttu-id="16654-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="16654-107">Event Data</span></span>

<span data-ttu-id="16654-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="16654-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEventHandler**.</span></span> <span data-ttu-id="16654-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="16654-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="16654-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16654-110">Property</span></span>             | <span data-ttu-id="16654-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="16654-111">Description</span></span>                                                                  |
|----------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="16654-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="16654-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="16654-113">System. StringSpecifies nombre de la lista de reproducción que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="16654-113">System.StringSpecifies the name of the playlist that was removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="16654-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16654-114">Requirements</span></span>



| <span data-ttu-id="16654-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="16654-115">Requirement</span></span> | <span data-ttu-id="16654-116">Value</span><span class="sxs-lookup"><span data-stu-id="16654-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16654-117">Versión</span><span class="sxs-lookup"><span data-stu-id="16654-117">Version</span></span><br/>   | <span data-ttu-id="16654-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="16654-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="16654-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="16654-119">Namespace</span></span><br/> | <span data-ttu-id="16654-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="16654-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="16654-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="16654-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="16654-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="16654-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16654-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="16654-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16654-124">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="16654-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16654-125">**IWMPPlaylistCollection. getByName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="16654-125">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 






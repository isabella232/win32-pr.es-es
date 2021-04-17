---
title: Evento PlaylistCollectionPlaylistAdded del objeto AxWindowsMediaPlayer
description: El evento PlaylistCollectionPlaylistAdded se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción. | Evento PlaylistCollectionPlaylistAdded del objeto AxWindowsMediaPlayer
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- Evento PlaylistCollectionPlaylistAdded del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700220"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3a670-105">Evento PlaylistCollectionPlaylistAdded del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="3a670-105">PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3a670-106">El evento PlaylistCollectionPlaylistAdded se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3a670-106">The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a><span data-ttu-id="3a670-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="3a670-107">Event Data</span></span>

<span data-ttu-id="3a670-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="3a670-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEventHandler**.</span></span> <span data-ttu-id="3a670-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="3a670-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="3a670-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a670-110">Property</span></span>             | <span data-ttu-id="3a670-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a670-111">Description</span></span>                                                                |
|----------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="3a670-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="3a670-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="3a670-113">System. StringSpecifies nombre de la lista de reproducción que se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="3a670-113">System.StringSpecifies the name of the playlist that was added.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a670-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a670-114">Remarks</span></span>

<span data-ttu-id="3a670-115">El nombre de la lista de reproducción que se ha agregado se puede usar para recuperar la lista de reproducción correspondiente mediante IWMPPlaylistCollection. método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="3a670-115">The name of the playlist that was added can be used to retrieve the corresponding playlist by using the IWMPPlaylistCollection.**getByName** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a670-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a670-116">Requirements</span></span>



| <span data-ttu-id="3a670-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a670-117">Requirement</span></span> | <span data-ttu-id="3a670-118">Value</span><span class="sxs-lookup"><span data-stu-id="3a670-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a670-119">Versión</span><span class="sxs-lookup"><span data-stu-id="3a670-119">Version</span></span><br/>   | <span data-ttu-id="3a670-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="3a670-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3a670-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a670-121">Namespace</span></span><br/> | <span data-ttu-id="3a670-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3a670-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3a670-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3a670-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3a670-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3a670-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a670-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a670-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a670-126">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3a670-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a670-127">**IWMPPlaylistCollection. getByName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3a670-127">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 






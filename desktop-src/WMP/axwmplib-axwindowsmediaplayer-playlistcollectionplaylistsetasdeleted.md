---
title: Evento PlaylistCollectionPlaylistSetAsDeleted del objeto AxWindowsMediaPlayer
description: El evento PlaylistCollectionPlaylistSetAsDeleted se reserva para uso futuro.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Evento PlaylistCollectionPlaylistSetAsDeleted del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700216"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="10f9e-104">Evento PlaylistCollectionPlaylistSetAsDeleted del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="10f9e-104">PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="10f9e-105">El evento PlaylistCollectionPlaylistSetAsDeleted se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="10f9e-105">The PlaylistCollectionPlaylistSetAsDeleted event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a><span data-ttu-id="10f9e-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="10f9e-106">Event Data</span></span>

<span data-ttu-id="10f9e-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="10f9e-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span></span> <span data-ttu-id="10f9e-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="10f9e-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="10f9e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10f9e-109">Property</span></span>         | <span data-ttu-id="10f9e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="10f9e-110">Description</span></span>                                 |
|------------------|---------------------------------------------|
| <span data-ttu-id="10f9e-111">bstrPlaylistName</span><span class="sxs-lookup"><span data-stu-id="10f9e-111">bstrPlaylistName</span></span> | <span data-ttu-id="10f9e-112">**System. String** No compatible.</span><span class="sxs-lookup"><span data-stu-id="10f9e-112">**System.String** Not supported.</span></span><br/>  |
| <span data-ttu-id="10f9e-113">varfIsDeleted</span><span class="sxs-lookup"><span data-stu-id="10f9e-113">varfIsDeleted</span></span>    | <span data-ttu-id="10f9e-114">**System. Boolean** No compatible.</span><span class="sxs-lookup"><span data-stu-id="10f9e-114">**System.Boolean** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="10f9e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10f9e-115">Remarks</span></span>

<span data-ttu-id="10f9e-116">Este evento se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="10f9e-116">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f9e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10f9e-117">Requirements</span></span>



| <span data-ttu-id="10f9e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="10f9e-118">Requirement</span></span> | <span data-ttu-id="10f9e-119">Value</span><span class="sxs-lookup"><span data-stu-id="10f9e-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f9e-120">Versión</span><span class="sxs-lookup"><span data-stu-id="10f9e-120">Version</span></span><br/>   | <span data-ttu-id="10f9e-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="10f9e-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="10f9e-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="10f9e-122">Namespace</span></span><br/> | <span data-ttu-id="10f9e-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="10f9e-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="10f9e-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="10f9e-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="10f9e-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="10f9e-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10f9e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="10f9e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f9e-127">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="10f9e-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






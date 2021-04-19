---
title: Evento CurrentPlaylistItemAvailable del objeto AxWindowsMediaPlayer
description: El evento CurrentPlaylistItemAvailable se produce cuando la lista de reproducción actual está disponible. | Evento CurrentPlaylistItemAvailable del objeto AxWindowsMediaPlayer
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Evento CurrentPlaylistItemAvailable del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698503"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ccb50-105">Evento CurrentPlaylistItemAvailable del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ccb50-105">CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ccb50-106">El evento CurrentPlaylistItemAvailable se produce cuando la lista de reproducción actual está disponible.</span><span class="sxs-lookup"><span data-stu-id="ccb50-106">The CurrentPlaylistItemAvailable event occurs when the current playlist becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="ccb50-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="ccb50-107">Event Data</span></span>

<span data-ttu-id="ccb50-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="ccb50-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEventHandler**.</span></span> <span data-ttu-id="ccb50-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="ccb50-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="ccb50-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ccb50-110">Property</span></span>         | <span data-ttu-id="ccb50-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccb50-111">Description</span></span>                                                    |
|------------------|----------------------------------------------------------------|
| <span data-ttu-id="ccb50-112">**bstrItemName**</span><span class="sxs-lookup"><span data-stu-id="ccb50-112">**bstrItemName**</span></span> | <span data-ttu-id="ccb50-113">System. Stringel nombre del elemento de lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="ccb50-113">System.StringThe name of the current playlist item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ccb50-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ccb50-114">Remarks</span></span>

<span data-ttu-id="ccb50-115">El nombre de la lista de reproducción actual se puede usar para recuperar la interfaz **IWMPPlaylist** correspondiente de la interfaz IWMPPlaylistArray que se devuelve desde el método IWMPPlaylistCollection. getByName.</span><span class="sxs-lookup"><span data-stu-id="ccb50-115">The name of the current playlist can be used to retrieve the corresponding **IWMPPlaylist** interface from the IWMPPlaylistArray interface that is returned from the IWMPPlaylistCollection.getByName method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb50-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb50-116">Requirements</span></span>



| <span data-ttu-id="ccb50-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb50-117">Requirement</span></span> | <span data-ttu-id="ccb50-118">Value</span><span class="sxs-lookup"><span data-stu-id="ccb50-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb50-119">Versión</span><span class="sxs-lookup"><span data-stu-id="ccb50-119">Version</span></span><br/>   | <span data-ttu-id="ccb50-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ccb50-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ccb50-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ccb50-121">Namespace</span></span><br/> | <span data-ttu-id="ccb50-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ccb50-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ccb50-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ccb50-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ccb50-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ccb50-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccb50-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccb50-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb50-126">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ccb50-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ccb50-127">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ccb50-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ccb50-128">**Interfaz IWMPPlaylistArray (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ccb50-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ccb50-129">**IWMPPlaylistCollection. getByName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ccb50-129">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 






---
title: Evento PlaylistChange del objeto AxWindowsMediaPlayer
description: El evento PlaylistChange se produce cuando cambia una lista de reproducción. | Evento PlaylistChange del objeto AxWindowsMediaPlayer
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Evento PlaylistChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700223"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="1e5cf-105">Evento PlaylistChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="1e5cf-105">PlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="1e5cf-106">El evento PlaylistChange se produce cuando cambia una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-106">The PlaylistChange event occurs when a playlist changes.</span></span>

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="1e5cf-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="1e5cf-107">Event Data</span></span>

<span data-ttu-id="1e5cf-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEventHandler**.</span></span> <span data-ttu-id="1e5cf-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="1e5cf-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e5cf-110">Property</span></span>     | <span data-ttu-id="1e5cf-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e5cf-111">Description</span></span>                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5cf-112">**automáticas**</span><span class="sxs-lookup"><span data-stu-id="1e5cf-112">**playlist**</span></span> | <span data-ttu-id="1e5cf-113">Objeto System. ObjectThe que cambió.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-113">System.ObjectThe object which changed.</span></span> <span data-ttu-id="1e5cf-114">Puede convertirlo en una interfaz IWMPPlaylist para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/>                |
| <span data-ttu-id="1e5cf-115">**change**</span><span class="sxs-lookup"><span data-stu-id="1e5cf-115">**change**</span></span>   | <span data-ttu-id="1e5cf-116">Valor de enumeración WMPLib. WMPPlaylistChangeEventTypeAn que indica el tipo de cambio que se produjo en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-116">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1e5cf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e5cf-117">Requirements</span></span>



| <span data-ttu-id="1e5cf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e5cf-118">Requirement</span></span> | <span data-ttu-id="1e5cf-119">Value</span><span class="sxs-lookup"><span data-stu-id="1e5cf-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5cf-120">Versión</span><span class="sxs-lookup"><span data-stu-id="1e5cf-120">Version</span></span><br/>   | <span data-ttu-id="1e5cf-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="1e5cf-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="1e5cf-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1e5cf-122">Namespace</span></span><br/> | <span data-ttu-id="1e5cf-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="1e5cf-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1e5cf-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="1e5cf-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1e5cf-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1e5cf-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e5cf-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e5cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5cf-127">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1e5cf-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1e5cf-128">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1e5cf-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 






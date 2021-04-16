---
title: Evento OpenPlaylistSwitch del objeto AxWindowsMediaPlayer
description: El evento OpenPlaylistSwitch se produce cuando comienza a reproducirse un título en un DVD. | Evento OpenPlaylistSwitch del objeto AxWindowsMediaPlayer
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Evento OpenPlaylistSwitch del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699393"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="07047-105">Evento OpenPlaylistSwitch del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="07047-105">OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="07047-106">El evento OpenPlaylistSwitch se produce cuando comienza a reproducirse un título en un DVD.</span><span class="sxs-lookup"><span data-stu-id="07047-106">The OpenPlaylistSwitch event occurs when a title on a DVD begins playing.</span></span>

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a><span data-ttu-id="07047-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="07047-107">Event Data</span></span>

<span data-ttu-id="07047-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="07047-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEventHandler**.</span></span> <span data-ttu-id="07047-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="07047-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="07047-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="07047-110">Property</span></span>  | <span data-ttu-id="07047-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="07047-111">Description</span></span>                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07047-112">**pItem**</span><span class="sxs-lookup"><span data-stu-id="07047-112">**pItem**</span></span> | <span data-ttu-id="07047-113">System. ObjectObject que representa el título.</span><span class="sxs-lookup"><span data-stu-id="07047-113">System.ObjectObject representing the title.</span></span> <span data-ttu-id="07047-114">Puede convertirlo en una interfaz IWMPPlaylist para tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="07047-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="07047-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07047-115">Requirements</span></span>



| <span data-ttu-id="07047-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="07047-116">Requirement</span></span> | <span data-ttu-id="07047-117">Value</span><span class="sxs-lookup"><span data-stu-id="07047-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07047-118">Versión</span><span class="sxs-lookup"><span data-stu-id="07047-118">Version</span></span><br/>   | <span data-ttu-id="07047-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="07047-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="07047-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="07047-120">Namespace</span></span><br/> | <span data-ttu-id="07047-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="07047-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="07047-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="07047-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="07047-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="07047-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07047-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="07047-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07047-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="07047-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="07047-126">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="07047-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 






---
title: Evento MarkerHit del objeto AxWindowsMediaPlayer
description: El evento MarkerHit se produce cuando se alcanza un marcador. | Evento MarkerHit del objeto AxWindowsMediaPlayer
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- Evento MarkerHit del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bad8d9d64b4711937cd984bbd9d335acebfe67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700160"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3c804-105">Evento MarkerHit del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="3c804-105">MarkerHit Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3c804-106">El evento MarkerHit se produce cuando se alcanza un marcador.</span><span class="sxs-lookup"><span data-stu-id="3c804-106">The MarkerHit event occurs when a marker is reached.</span></span>

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a><span data-ttu-id="3c804-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="3c804-107">Event Data</span></span>

<span data-ttu-id="3c804-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="3c804-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEventHandler**.</span></span> <span data-ttu-id="3c804-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="3c804-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="3c804-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3c804-110">Property</span></span>      | <span data-ttu-id="3c804-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c804-111">Description</span></span>                                                             |
|---------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3c804-112">**MarkerNum**</span><span class="sxs-lookup"><span data-stu-id="3c804-112">**MarkerNum**</span></span> | <span data-ttu-id="3c804-113">System. Int32Indicates número del marcador que se alcanzó.</span><span class="sxs-lookup"><span data-stu-id="3c804-113">System.Int32Indicates the number of the marker that was hit.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3c804-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c804-114">Requirements</span></span>



| <span data-ttu-id="3c804-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c804-115">Requirement</span></span> | <span data-ttu-id="3c804-116">Value</span><span class="sxs-lookup"><span data-stu-id="3c804-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c804-117">Versión</span><span class="sxs-lookup"><span data-stu-id="3c804-117">Version</span></span><br/>   | <span data-ttu-id="3c804-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="3c804-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3c804-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3c804-119">Namespace</span></span><br/> | <span data-ttu-id="3c804-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3c804-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3c804-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3c804-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3c804-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3c804-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c804-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c804-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c804-124">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3c804-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






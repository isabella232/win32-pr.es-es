---
title: Evento DurationUnitChange del objeto AxWindowsMediaPlayer
description: El evento DurationUnitChange se reserva para uso futuro.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Evento DurationUnitChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f90aa052c61893d83683d10f482cd05841a49fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698556"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a81c9-104">Evento DurationUnitChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a81c9-104">DurationUnitChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a81c9-105">El evento DurationUnitChange se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a81c9-105">The DurationUnitChange event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a><span data-ttu-id="a81c9-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="a81c9-106">Event Data</span></span>

<span data-ttu-id="a81c9-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="a81c9-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEventHandler**.</span></span> <span data-ttu-id="a81c9-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="a81c9-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="a81c9-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a81c9-109">Property</span></span>        | <span data-ttu-id="a81c9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a81c9-110">Description</span></span>                               |
|-----------------|-------------------------------------------|
| <span data-ttu-id="a81c9-111">newDurationUnit</span><span class="sxs-lookup"><span data-stu-id="a81c9-111">newDurationUnit</span></span> | <span data-ttu-id="a81c9-112">**System. Int32** No compatible.</span><span class="sxs-lookup"><span data-stu-id="a81c9-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a81c9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a81c9-113">Remarks</span></span>

<span data-ttu-id="a81c9-114">Este evento se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a81c9-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="a81c9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a81c9-115">Requirements</span></span>



| <span data-ttu-id="a81c9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a81c9-116">Requirement</span></span> | <span data-ttu-id="a81c9-117">Value</span><span class="sxs-lookup"><span data-stu-id="a81c9-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a81c9-118">Versión</span><span class="sxs-lookup"><span data-stu-id="a81c9-118">Version</span></span><br/>   | <span data-ttu-id="a81c9-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a81c9-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a81c9-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a81c9-120">Namespace</span></span><br/> | <span data-ttu-id="a81c9-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a81c9-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a81c9-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a81c9-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a81c9-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a81c9-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a81c9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a81c9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a81c9-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a81c9-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






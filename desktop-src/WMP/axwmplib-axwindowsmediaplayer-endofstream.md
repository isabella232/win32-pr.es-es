---
title: Evento EndOfStream del objeto AxWindowsMediaPlayer
description: El evento EndOfStream se reserva para uso futuro.
ms.assetid: 004172e0-abd4-451c-bd5c-6bf0a9277661
keywords:
- Evento EndOfStream del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- EndOfStream Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74a64eea77af43cd3b33cc7edee2177aee7d15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698551"
---
# <a name="endofstream-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="09136-104">Evento EndOfStream del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="09136-104">EndOfStream Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="09136-105">El evento EndOfStream se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="09136-105">The EndOfStream event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_EndOfStream(
  object sender,
  _WMPOCXEvents_EndOfStreamEvent e
)

[Visual Basic]
Private Sub player_EndOfStream(  
  sender As Object,  
  e As _WMPOCXEvents_EndOfStreamEvent
) Handles player.EndOfStream
```

## <a name="event-data"></a><span data-ttu-id="09136-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="09136-106">Event Data</span></span>

<span data-ttu-id="09136-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ EndOfStreamEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="09136-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEventHandler**.</span></span> <span data-ttu-id="09136-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ EndOfStreamEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="09136-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="09136-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09136-109">Property</span></span> | <span data-ttu-id="09136-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="09136-110">Description</span></span>                           |
|----------|---------------------------------------|
| <span data-ttu-id="09136-111">resultado</span><span class="sxs-lookup"><span data-stu-id="09136-111">result</span></span>   | <span data-ttu-id="09136-112">System. Int32Not compatible.</span><span class="sxs-lookup"><span data-stu-id="09136-112">System.Int32Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09136-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09136-113">Remarks</span></span>

<span data-ttu-id="09136-114">Este evento se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="09136-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="09136-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09136-115">Requirements</span></span>



| <span data-ttu-id="09136-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="09136-116">Requirement</span></span> | <span data-ttu-id="09136-117">Value</span><span class="sxs-lookup"><span data-stu-id="09136-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09136-118">Versión</span><span class="sxs-lookup"><span data-stu-id="09136-118">Version</span></span><br/>   | <span data-ttu-id="09136-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="09136-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="09136-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="09136-120">Namespace</span></span><br/> | <span data-ttu-id="09136-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="09136-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="09136-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="09136-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="09136-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="09136-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09136-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="09136-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09136-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="09136-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






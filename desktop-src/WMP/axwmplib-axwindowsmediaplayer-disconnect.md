---
title: Evento Disconnect del objeto AxWindowsMediaPlayer
description: El evento Disconnect se reserva para uso futuro.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- Evento Disconnect del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dffe3191efeddba74eb22c7c5c72b8c52bc095
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699341"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="89eda-104">Evento Disconnect del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="89eda-104">Disconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="89eda-105">El evento Disconnect se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="89eda-105">The Disconnect event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a><span data-ttu-id="89eda-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="89eda-106">Event Data</span></span>

<span data-ttu-id="89eda-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="89eda-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEventHandler**.</span></span> <span data-ttu-id="89eda-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="89eda-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="89eda-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="89eda-109">Property</span></span> | <span data-ttu-id="89eda-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="89eda-110">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="89eda-111">resultado</span><span class="sxs-lookup"><span data-stu-id="89eda-111">result</span></span>   | <span data-ttu-id="89eda-112">**System. Int32** No compatible.</span><span class="sxs-lookup"><span data-stu-id="89eda-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89eda-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89eda-113">Remarks</span></span>

<span data-ttu-id="89eda-114">Este evento se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="89eda-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="89eda-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89eda-115">Requirements</span></span>



| <span data-ttu-id="89eda-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="89eda-116">Requirement</span></span> | <span data-ttu-id="89eda-117">Value</span><span class="sxs-lookup"><span data-stu-id="89eda-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89eda-118">Versión</span><span class="sxs-lookup"><span data-stu-id="89eda-118">Version</span></span><br/>   | <span data-ttu-id="89eda-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="89eda-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="89eda-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="89eda-120">Namespace</span></span><br/> | <span data-ttu-id="89eda-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="89eda-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="89eda-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="89eda-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="89eda-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="89eda-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89eda-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="89eda-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89eda-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="89eda-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






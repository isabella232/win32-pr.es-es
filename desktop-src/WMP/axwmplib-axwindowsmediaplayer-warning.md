---
title: Evento de advertencia del objeto AxWindowsMediaPlayer
description: El evento de advertencia se reserva para un uso futuro.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Evento de advertencia del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699985"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4ff19-104">Evento de advertencia del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4ff19-104">Warning Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4ff19-105">El evento de advertencia se reserva para un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4ff19-105">The Warning event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a><span data-ttu-id="4ff19-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="4ff19-106">Event Data</span></span>

<span data-ttu-id="4ff19-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4ff19-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_WarningEventHandler**.</span></span> <span data-ttu-id="4ff19-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="4ff19-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_WarningEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4ff19-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4ff19-109">Property</span></span>    | <span data-ttu-id="4ff19-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ff19-110">Description</span></span>                                |
|-------------|--------------------------------------------|
| <span data-ttu-id="4ff19-111">warningType</span><span class="sxs-lookup"><span data-stu-id="4ff19-111">warningType</span></span> | <span data-ttu-id="4ff19-112">**System. Int32** No compatible.</span><span class="sxs-lookup"><span data-stu-id="4ff19-112">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="4ff19-113">param</span><span class="sxs-lookup"><span data-stu-id="4ff19-113">param</span></span>       | <span data-ttu-id="4ff19-114">**System. Int32** No compatible.</span><span class="sxs-lookup"><span data-stu-id="4ff19-114">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="4ff19-115">description</span><span class="sxs-lookup"><span data-stu-id="4ff19-115">description</span></span> | <span data-ttu-id="4ff19-116">**System. String** No compatible.</span><span class="sxs-lookup"><span data-stu-id="4ff19-116">**System.String** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4ff19-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ff19-117">Remarks</span></span>

<span data-ttu-id="4ff19-118">Este evento se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4ff19-118">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ff19-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ff19-119">Requirements</span></span>



| <span data-ttu-id="4ff19-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ff19-120">Requirement</span></span> | <span data-ttu-id="4ff19-121">Value</span><span class="sxs-lookup"><span data-stu-id="4ff19-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff19-122">Versión</span><span class="sxs-lookup"><span data-stu-id="4ff19-122">Version</span></span><br/>   | <span data-ttu-id="4ff19-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="4ff19-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4ff19-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ff19-124">Namespace</span></span><br/> | <span data-ttu-id="4ff19-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4ff19-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4ff19-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="4ff19-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4ff19-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4ff19-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ff19-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ff19-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ff19-129">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4ff19-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






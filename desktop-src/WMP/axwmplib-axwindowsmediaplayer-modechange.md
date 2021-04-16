---
title: Evento ModeChange del objeto AxWindowsMediaPlayer
description: El evento ModeChange se produce cuando se cambia un modo de Media Player de Windows. | Evento ModeChange del objeto AxWindowsMediaPlayer
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Evento ModeChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699907"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="74e2d-105">Evento ModeChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="74e2d-105">ModeChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="74e2d-106">El evento ModeChange se produce cuando se cambia un modo de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="74e2d-106">The ModeChange event occurs when a mode of Windows Media Player is changed.</span></span>

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a><span data-ttu-id="74e2d-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="74e2d-107">Event Data</span></span>

<span data-ttu-id="74e2d-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="74e2d-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEventHandler**.</span></span> <span data-ttu-id="74e2d-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="74e2d-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="74e2d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="74e2d-110">Property</span></span> | <span data-ttu-id="74e2d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="74e2d-111">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74e2d-112">modeName</span><span class="sxs-lookup"><span data-stu-id="74e2d-112">modeName</span></span> | <span data-ttu-id="74e2d-113">System. StringIndicates el modo que se cambió.</span><span class="sxs-lookup"><span data-stu-id="74e2d-113">System.StringIndicates the mode that was changed.</span></span> <span data-ttu-id="74e2d-114">Para ver los valores posibles, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="74e2d-114">For possible values, see Remarks.</span></span><br/> |
| <span data-ttu-id="74e2d-115">newValue</span><span class="sxs-lookup"><span data-stu-id="74e2d-115">newValue</span></span> | <span data-ttu-id="74e2d-116">System. BooleanIndicates el nuevo estado del modo especificado.</span><span class="sxs-lookup"><span data-stu-id="74e2d-116">System.BooleanIndicates the new state of the specified mode.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="74e2d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74e2d-117">Remarks</span></span>

<span data-ttu-id="74e2d-118">En la tabla siguiente se muestran los posibles valores para la propiedad modeName.</span><span class="sxs-lookup"><span data-stu-id="74e2d-118">The following table shows the possible values for the modeName property.</span></span>



| <span data-ttu-id="74e2d-119">String</span><span class="sxs-lookup"><span data-stu-id="74e2d-119">String</span></span>  | <span data-ttu-id="74e2d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="74e2d-120">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="74e2d-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="74e2d-121">shuffle</span></span> | <span data-ttu-id="74e2d-122">Las pistas se reproducen en orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="74e2d-122">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="74e2d-123">bucle</span><span class="sxs-lookup"><span data-stu-id="74e2d-123">loop</span></span>    | <span data-ttu-id="74e2d-124">Toda la secuencia de pistas se reproduce varias veces.</span><span class="sxs-lookup"><span data-stu-id="74e2d-124">The entire sequence of tracks is played repeatedly.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="74e2d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74e2d-125">Requirements</span></span>



| <span data-ttu-id="74e2d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="74e2d-126">Requirement</span></span> | <span data-ttu-id="74e2d-127">Value</span><span class="sxs-lookup"><span data-stu-id="74e2d-127">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74e2d-128">Versión</span><span class="sxs-lookup"><span data-stu-id="74e2d-128">Version</span></span><br/>   | <span data-ttu-id="74e2d-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="74e2d-129">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="74e2d-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="74e2d-130">Namespace</span></span><br/> | <span data-ttu-id="74e2d-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="74e2d-131">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="74e2d-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="74e2d-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="74e2d-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="74e2d-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74e2d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="74e2d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e2d-135">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="74e2d-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="74e2d-136">**IWMPSettings. getMode (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="74e2d-136">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="74e2d-137">**IWMPSettings. setMode (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="74e2d-137">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 






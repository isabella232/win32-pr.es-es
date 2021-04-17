---
title: Evento MouseMove del objeto AxWindowsMediaPlayer
description: El evento MouseMove se produce cuando se mueve el puntero del mouse. | Evento MouseMove del objeto AxWindowsMediaPlayer
ms.assetid: abf20c86-3bae-4677-8901-0af030a53286
keywords:
- Evento MouseMove del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- MouseMove Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c623bf60f2951b1a82e59a7d63056bcf8a0b5da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699905"
---
# <a name="mousemove-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a2f25-105">Evento MouseMove del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a2f25-105">MouseMove Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a2f25-106">El evento MouseMove se produce cuando se mueve el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="a2f25-106">The MouseMove event occurs when the mouse pointer is moved.</span></span>

``` syntax
[C#]
private void player_MouseMoveEvent(
  object sender,
  _WMPOCXEvents_MouseMoveEvent e
)

[Visual Basic]
Private Sub player_MouseMoveEvent(
  sender As Object,
  e As _WMPOCXEvents_MouseMoveEvent
) Handles player.MouseMoveEvent
```

## <a name="event-data"></a><span data-ttu-id="a2f25-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="a2f25-107">Event Data</span></span>

<span data-ttu-id="a2f25-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseMoveEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="a2f25-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseMoveEventHandler**.</span></span> <span data-ttu-id="a2f25-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseMoveEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="a2f25-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseMoveEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="a2f25-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2f25-110">Property</span></span>    | <span data-ttu-id="a2f25-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2f25-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f25-112">Nbotón</span><span class="sxs-lookup"><span data-stu-id="a2f25-112">nButton</span></span>     | <span data-ttu-id="a2f25-113">Campo de bits System. Int16A con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="a2f25-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="a2f25-114">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a2f25-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="a2f25-115">Solo se establece uno de los bits, que indica el botón que causó el evento.</span><span class="sxs-lookup"><span data-stu-id="a2f25-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="a2f25-116">nShiftState</span><span class="sxs-lookup"><span data-stu-id="a2f25-116">nShiftState</span></span> | <span data-ttu-id="a2f25-117">El campo de bits System. Int16A con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="a2f25-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="a2f25-118">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a2f25-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="a2f25-119">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="a2f25-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="a2f25-120">Efectos</span><span class="sxs-lookup"><span data-stu-id="a2f25-120">fX</span></span>          | <span data-ttu-id="a2f25-121">System. Int32el coordenada x del puntero del mouse en relación con la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="a2f25-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="a2f25-122">fY</span><span class="sxs-lookup"><span data-stu-id="a2f25-122">fY</span></span>          | <span data-ttu-id="a2f25-123">Coordenada y de System. Int32el del puntero del mouse con respecto a la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="a2f25-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="a2f25-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2f25-124">Requirements</span></span>



| <span data-ttu-id="a2f25-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2f25-125">Requirement</span></span> | <span data-ttu-id="a2f25-126">Value</span><span class="sxs-lookup"><span data-stu-id="a2f25-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f25-127">Versión</span><span class="sxs-lookup"><span data-stu-id="a2f25-127">Version</span></span><br/>   | <span data-ttu-id="a2f25-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a2f25-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a2f25-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a2f25-129">Namespace</span></span><br/> | <span data-ttu-id="a2f25-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a2f25-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a2f25-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a2f25-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a2f25-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a2f25-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2f25-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2f25-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f25-134">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a2f25-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






---
title: Evento MouseUp del objeto AxWindowsMediaPlayer
description: El evento MouseUp se produce cuando el usuario suelta un botón del mouse. | Evento MouseUp del objeto AxWindowsMediaPlayer
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- Evento MouseUp del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- MouseUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2bf9c209b4fa263eb0a6cbcba2a32b0b1c46fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699832"
---
# <a name="mouseup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="1d08e-105">Evento MouseUp del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="1d08e-105">MouseUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="1d08e-106">El evento MouseUp se produce cuando el usuario suelta un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="1d08e-106">The MouseUp event occurs when the user releases a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseUpEvent(
  object sender,
  _WMPOCXEvents_MouseUpEvent e
)

[Visual Basic]
Private Sub player_MouseUpEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseUpEvent
) Handles player.MouseUpEvent
```

## <a name="event-data"></a><span data-ttu-id="1d08e-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="1d08e-107">Event Data</span></span>

<span data-ttu-id="1d08e-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseUpEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="1d08e-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEventHandler**.</span></span> <span data-ttu-id="1d08e-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseUpEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="1d08e-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="1d08e-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1d08e-110">Property</span></span>    | <span data-ttu-id="1d08e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d08e-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d08e-112">Nbotón</span><span class="sxs-lookup"><span data-stu-id="1d08e-112">nButton</span></span>     | <span data-ttu-id="1d08e-113">Campo de bits System. Int16A con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="1d08e-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="1d08e-114">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1d08e-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="1d08e-115">Solo se establece uno de los bits, que indica el botón que causó el evento.</span><span class="sxs-lookup"><span data-stu-id="1d08e-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="1d08e-116">nShiftState</span><span class="sxs-lookup"><span data-stu-id="1d08e-116">nShiftState</span></span> | <span data-ttu-id="1d08e-117">El campo de bits System. Int16A con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="1d08e-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="1d08e-118">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1d08e-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="1d08e-119">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="1d08e-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="1d08e-120">Efectos</span><span class="sxs-lookup"><span data-stu-id="1d08e-120">fX</span></span>          | <span data-ttu-id="1d08e-121">System. Int32el coordenada x del puntero del mouse en relación con la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="1d08e-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="1d08e-122">fY</span><span class="sxs-lookup"><span data-stu-id="1d08e-122">fY</span></span>          | <span data-ttu-id="1d08e-123">Coordenada y de System. Int32el del puntero del mouse con respecto a la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="1d08e-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="1d08e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d08e-124">Requirements</span></span>



| <span data-ttu-id="1d08e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d08e-125">Requirement</span></span> | <span data-ttu-id="1d08e-126">Value</span><span class="sxs-lookup"><span data-stu-id="1d08e-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d08e-127">Versión</span><span class="sxs-lookup"><span data-stu-id="1d08e-127">Version</span></span><br/>   | <span data-ttu-id="1d08e-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="1d08e-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="1d08e-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d08e-129">Namespace</span></span><br/> | <span data-ttu-id="1d08e-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="1d08e-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1d08e-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="1d08e-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1d08e-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1d08e-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d08e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d08e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d08e-134">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1d08e-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






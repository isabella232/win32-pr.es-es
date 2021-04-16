---
title: Evento DoubleClick del objeto AxWindowsMediaPlayer
description: El evento DoubleClick se produce cuando el usuario hace doble clic en un botón del mouse en un control de Media Player de Windows.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Evento DoubleClick del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699626"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="fc4a5-104">Evento DoubleClick del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="fc4a5-104">DoubleClick Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="fc4a5-105">El evento DoubleClick se produce cuando el usuario hace doble clic en un botón del mouse en un control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-105">The DoubleClick event occurs when the user double-clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a><span data-ttu-id="fc4a5-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="fc4a5-106">Event Data</span></span>

<span data-ttu-id="fc4a5-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEventHandler**.</span></span> <span data-ttu-id="fc4a5-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="fc4a5-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc4a5-109">Property</span></span>    | <span data-ttu-id="fc4a5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc4a5-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4a5-111">Nbotón</span><span class="sxs-lookup"><span data-stu-id="fc4a5-111">nButton</span></span>     | <span data-ttu-id="fc4a5-112">Campo de bits System. Int16A con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="fc4a5-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="fc4a5-113">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="fc4a5-114">Solo se establece uno de los bits, que indica el botón que causó el evento.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="fc4a5-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="fc4a5-115">nShiftState</span></span> | <span data-ttu-id="fc4a5-116">El campo de bits System. Int16A con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="fc4a5-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="fc4a5-117">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="fc4a5-118">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="fc4a5-119">Efectos</span><span class="sxs-lookup"><span data-stu-id="fc4a5-119">fX</span></span>          | <span data-ttu-id="fc4a5-120">System. Int32el coordenada x del puntero del mouse en relación con la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="fc4a5-121">fY</span><span class="sxs-lookup"><span data-stu-id="fc4a5-121">fY</span></span>          | <span data-ttu-id="fc4a5-122">Coordenada y de System. Int32el del puntero del mouse con respecto a la esquina superior izquierda del control.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="fc4a5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc4a5-123">Requirements</span></span>



| <span data-ttu-id="fc4a5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc4a5-124">Requirement</span></span> | <span data-ttu-id="fc4a5-125">Value</span><span class="sxs-lookup"><span data-stu-id="fc4a5-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4a5-126">Versión</span><span class="sxs-lookup"><span data-stu-id="fc4a5-126">Version</span></span><br/>   | <span data-ttu-id="fc4a5-127">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="fc4a5-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="fc4a5-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc4a5-128">Namespace</span></span><br/> | <span data-ttu-id="fc4a5-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="fc4a5-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="fc4a5-130">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="fc4a5-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fc4a5-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fc4a5-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc4a5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc4a5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc4a5-133">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="fc4a5-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






---
title: Evento KeyUp del objeto AxWindowsMediaPlayer
description: El evento KeyUp se produce cuando se suelta una tecla. | Evento KeyUp del objeto AxWindowsMediaPlayer
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- Evento KeyUp del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509f520ff7624b0b29302d7bf5cd825cd45b4254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699909"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="48c5c-105">Evento KeyUp del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="48c5c-105">KeyUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="48c5c-106">El evento KeyUp se produce cuando se suelta una tecla.</span><span class="sxs-lookup"><span data-stu-id="48c5c-106">The KeyUp event occurs when a key is released.</span></span>

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a><span data-ttu-id="48c5c-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="48c5c-107">Event Data</span></span>

<span data-ttu-id="48c5c-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="48c5c-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEventHandler**.</span></span> <span data-ttu-id="48c5c-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="48c5c-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="48c5c-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="48c5c-110">Property</span></span>    | <span data-ttu-id="48c5c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="48c5c-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c5c-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="48c5c-112">nKeyCode</span></span>    | <span data-ttu-id="48c5c-113">System. Int16Specifies Qué tecla física está presionada.</span><span class="sxs-lookup"><span data-stu-id="48c5c-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="48c5c-114">Para ver los valores posibles, vea la sección Comentarios del evento KeyDown.</span><span class="sxs-lookup"><span data-stu-id="48c5c-114">For possible values, see the Remarks section of the KeyDown event.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="48c5c-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="48c5c-115">nShiftState</span></span> | <span data-ttu-id="48c5c-116">El campo de bits System. Int16A con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="48c5c-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="48c5c-117">Estos bits corresponden a los valores 1, 2 y 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="48c5c-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="48c5c-118">El argumento Shift indica el estado de estas claves.</span><span class="sxs-lookup"><span data-stu-id="48c5c-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="48c5c-119">Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.</span><span class="sxs-lookup"><span data-stu-id="48c5c-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="48c5c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48c5c-120">Requirements</span></span>



| <span data-ttu-id="48c5c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="48c5c-121">Requirement</span></span> | <span data-ttu-id="48c5c-122">Value</span><span class="sxs-lookup"><span data-stu-id="48c5c-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c5c-123">Versión</span><span class="sxs-lookup"><span data-stu-id="48c5c-123">Version</span></span><br/>   | <span data-ttu-id="48c5c-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="48c5c-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="48c5c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48c5c-125">Namespace</span></span><br/> | <span data-ttu-id="48c5c-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="48c5c-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="48c5c-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="48c5c-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="48c5c-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="48c5c-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48c5c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="48c5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c5c-130">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="48c5c-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






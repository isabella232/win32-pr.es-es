---
title: Evento PositionChange del objeto AxWindowsMediaPlayer
description: El evento PositionChange se produce cuando se ha cambiado la posición de reproducción actual dentro del elemento multimedia.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Evento PositionChange del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699464"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c6ba8-104">Evento PositionChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c6ba8-104">PositionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c6ba8-105">El evento PositionChange se produce cuando se ha cambiado la posición de reproducción actual dentro del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="c6ba8-105">The PositionChange event occurs when the current playback position within the media item has been changed.</span></span>

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a><span data-ttu-id="c6ba8-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="c6ba8-106">Event Data</span></span>

<span data-ttu-id="c6ba8-107">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="c6ba8-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEventHandler**.</span></span> <span data-ttu-id="c6ba8-108">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.</span><span class="sxs-lookup"><span data-stu-id="c6ba8-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="c6ba8-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c6ba8-109">Property</span></span>    | <span data-ttu-id="c6ba8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6ba8-110">Description</span></span>                                         |
|-------------|-----------------------------------------------------|
| <span data-ttu-id="c6ba8-111">oldPosition</span><span class="sxs-lookup"><span data-stu-id="c6ba8-111">oldPosition</span></span> | <span data-ttu-id="c6ba8-112">System. DoubleSpecifies la posición anterior.</span><span class="sxs-lookup"><span data-stu-id="c6ba8-112">System.DoubleSpecifies the old position.</span></span><br/> |
| <span data-ttu-id="c6ba8-113">newPosition</span><span class="sxs-lookup"><span data-stu-id="c6ba8-113">newPosition</span></span> | <span data-ttu-id="c6ba8-114">System. DoubleSpecifies la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="c6ba8-114">System.DoubleSpecifies the new position.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c6ba8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6ba8-115">Remarks</span></span>

<span data-ttu-id="c6ba8-116">Este evento no se genera rutinariamente durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="c6ba8-116">This event is not raised routinely during playback.</span></span> <span data-ttu-id="c6ba8-117">Solo se produce cuando algo cambia activamente la posición actual del elemento multimedia de reproducción, como cuando el usuario mueve el identificador de búsqueda o cuando se ejecuta código que especifica un valor para IWMPControls. **currentPosition**.</span><span class="sxs-lookup"><span data-stu-id="c6ba8-117">It only occurs when something actively changes the current position of the playing media item, such as when the user moves the seek handle or when code is executed that specifies a value for IWMPControls.**currentPosition**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ba8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6ba8-118">Requirements</span></span>



| <span data-ttu-id="c6ba8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ba8-119">Requirement</span></span> | <span data-ttu-id="c6ba8-120">Value</span><span class="sxs-lookup"><span data-stu-id="c6ba8-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ba8-121">Versión</span><span class="sxs-lookup"><span data-stu-id="c6ba8-121">Version</span></span><br/>   | <span data-ttu-id="c6ba8-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="c6ba8-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c6ba8-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c6ba8-123">Namespace</span></span><br/> | <span data-ttu-id="c6ba8-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c6ba8-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c6ba8-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c6ba8-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c6ba8-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c6ba8-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6ba8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6ba8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ba8-128">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c6ba8-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c6ba8-129">**IWMPControls. currentPosition (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c6ba8-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 






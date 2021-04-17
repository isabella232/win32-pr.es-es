---
title: Evento OpenStateChange del objeto AxWindowsMediaPlayer
description: El evento OpenStateChange se produce cuando cambia el valor de la propiedad openState. | Evento OpenStateChange del objeto AxWindowsMediaPlayer
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- Evento OpenStateChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698617"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8c8b1-105">Evento OpenStateChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="8c8b1-105">OpenStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8c8b1-106">El evento OpenStateChange se produce cuando cambia el valor de la propiedad **openState** .</span><span class="sxs-lookup"><span data-stu-id="8c8b1-106">The OpenStateChange event occurs when the **openState** property changes value.</span></span>

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a><span data-ttu-id="8c8b1-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="8c8b1-107">Event Data</span></span>

<span data-ttu-id="8c8b1-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="8c8b1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEventHandler**.</span></span> <span data-ttu-id="8c8b1-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="8c8b1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="8c8b1-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8c8b1-110">Property</span></span> | <span data-ttu-id="8c8b1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c8b1-111">Description</span></span>                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8b1-112">NewState</span><span class="sxs-lookup"><span data-stu-id="8c8b1-112">NewState</span></span> | <span data-ttu-id="8c8b1-113">System. Int32Specifies el nuevo estado abierto.</span><span class="sxs-lookup"><span data-stu-id="8c8b1-113">System.Int32Specifies the new open state.</span></span> <span data-ttu-id="8c8b1-114">Para obtener una tabla de valores, vea [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="8c8b1-114">For a table of values, see [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8c8b1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c8b1-115">Remarks</span></span>

<span data-ttu-id="8c8b1-116">Windows Media Player puede pasar por varios Estados abiertos mientras trata de abrir un archivo de red, como localizar el servidor, conectarse al servidor y, por último, abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="8c8b1-116">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="8c8b1-117">Este evento se desencadenará cada vez que cambie el estado abierto.</span><span class="sxs-lookup"><span data-stu-id="8c8b1-117">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="8c8b1-118">No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="8c8b1-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="8c8b1-119">Además, no todos los Estados se producen necesariamente durante una secuencia de eventos.</span><span class="sxs-lookup"><span data-stu-id="8c8b1-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="8c8b1-120">No debe escribir código que se base en el orden de los Estados.</span><span class="sxs-lookup"><span data-stu-id="8c8b1-120">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c8b1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c8b1-121">Requirements</span></span>



| <span data-ttu-id="8c8b1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c8b1-122">Requirement</span></span> | <span data-ttu-id="8c8b1-123">Value</span><span class="sxs-lookup"><span data-stu-id="8c8b1-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8b1-124">Versión</span><span class="sxs-lookup"><span data-stu-id="8c8b1-124">Version</span></span><br/>   | <span data-ttu-id="8c8b1-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="8c8b1-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8c8b1-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c8b1-126">Namespace</span></span><br/> | <span data-ttu-id="8c8b1-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8c8b1-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8c8b1-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="8c8b1-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8c8b1-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8c8b1-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c8b1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c8b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c8b1-131">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="8c8b1-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c8b1-132">**AxWindowsMediaPlayer. openState (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="8c8b1-132">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 






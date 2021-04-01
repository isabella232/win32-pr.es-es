---
title: Mensaje de MM_JOY1BUTTONUP (mmsystem. h)
description: El \_ mensaje mm JOY1BUTTONUP notifica a la ventana que ha capturado el joystick JOYSTICKID1 que se ha soltado un botón.
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- Mensaje de MM_JOY1BUTTONUP de Windows multimedia
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a5d954b9b879f87c5e8ffe2d0774d0d1d85a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151234"
---
# <a name="mm_joy1buttonup-message"></a><span data-ttu-id="3e977-104">\_Mensaje JOY1BUTTONUP mm</span><span class="sxs-lookup"><span data-stu-id="3e977-104">MM\_JOY1BUTTONUP message</span></span>

<span data-ttu-id="3e977-105">El mensaje **mm \_ JOY1BUTTONUP** notifica a la ventana que ha capturado el joystick JOYSTICKID1 que se ha soltado un botón.</span><span class="sxs-lookup"><span data-stu-id="3e977-105">The **MM\_JOY1BUTTONUP** message notifies the window that has captured joystick JOYSTICKID1 that a button has been released.</span></span>


```C++
MM_JOY1BUTTONUP 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="3e977-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e977-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e977-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="3e977-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="3e977-108">Identifica el botón que ha cambiado de estado y los botones que se presionan.</span><span class="sxs-lookup"><span data-stu-id="3e977-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="3e977-109">Puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="3e977-109">It can be one of the following:</span></span>



| <span data-ttu-id="3e977-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e977-110">Requirement</span></span> | <span data-ttu-id="3e977-111">Value</span><span class="sxs-lookup"><span data-stu-id="3e977-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="3e977-112">JOY \_ BUTTON1CHG</span><span class="sxs-lookup"><span data-stu-id="3e977-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="3e977-113">El primer botón del joystick ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="3e977-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="3e977-114">JOY \_ BUTTON2CHG</span><span class="sxs-lookup"><span data-stu-id="3e977-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="3e977-115">El segundo botón del joystick ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="3e977-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="3e977-116">JOY \_ BUTTON3CHG</span><span class="sxs-lookup"><span data-stu-id="3e977-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="3e977-117">El tercer botón del joystick ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="3e977-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="3e977-118">JOY \_ BUTTON4CHG</span><span class="sxs-lookup"><span data-stu-id="3e977-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="3e977-119">El cuarto botón del joystick ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="3e977-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="3e977-120">y uno o varios de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="3e977-120">and one or more of the following:</span></span>



| <span data-ttu-id="3e977-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e977-121">Requirement</span></span> | <span data-ttu-id="3e977-122">Value</span><span class="sxs-lookup"><span data-stu-id="3e977-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="3e977-123">JOY \_ button1</span><span class="sxs-lookup"><span data-stu-id="3e977-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="3e977-124">Se presionó el primer botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="3e977-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="3e977-125">JOY \_ BUTTON2</span><span class="sxs-lookup"><span data-stu-id="3e977-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="3e977-126">Se presionó el botón segundo joystick.</span><span class="sxs-lookup"><span data-stu-id="3e977-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="3e977-127">JOY \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="3e977-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="3e977-128">Se presionó el tercer botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="3e977-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="3e977-129">JOY \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="3e977-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="3e977-130">Se presionó el cuarto botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="3e977-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3e977-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="3e977-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="3e977-132">Coordenadas x del joystick con respecto a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="3e977-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="3e977-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="3e977-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="3e977-134">Coordenada y del joystick con respecto a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="3e977-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e977-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e977-135">Requirements</span></span>



| <span data-ttu-id="3e977-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e977-136">Requirement</span></span> | <span data-ttu-id="3e977-137">Value</span><span class="sxs-lookup"><span data-stu-id="3e977-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e977-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e977-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3e977-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3e977-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3e977-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e977-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3e977-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e977-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3e977-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e977-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e977-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e977-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e977-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e977-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e977-145">Joysticks</span><span class="sxs-lookup"><span data-stu-id="3e977-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="3e977-146">Mensajes de joystick multimedia</span><span class="sxs-lookup"><span data-stu-id="3e977-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 






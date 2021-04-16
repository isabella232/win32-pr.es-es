---
title: Mensaje de MM_JOY2BUTTONUP (mmsystem. h)
description: El \_ mensaje mm JOY2BUTTONUP notifica a la ventana que ha capturado el joystick JOYSTICKID2 que se ha soltado un botón.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- Mensaje de MM_JOY2BUTTONUP de Windows multimedia
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686256"
---
# <a name="mm_joy2buttonup-message"></a><span data-ttu-id="a08e3-104">\_Mensaje JOY2BUTTONUP mm</span><span class="sxs-lookup"><span data-stu-id="a08e3-104">MM\_JOY2BUTTONUP message</span></span>

<span data-ttu-id="a08e3-105">El mensaje **mm \_ JOY2BUTTONUP** notifica a la ventana que ha capturado el joystick JOYSTICKID2 que se ha soltado un botón.</span><span class="sxs-lookup"><span data-stu-id="a08e3-105">The **MM\_JOY2BUTTONUP** message notifies the window that has captured joystick JOYSTICKID2 that a button has been released.</span></span>


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="a08e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a08e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08e3-107">**fwButtons**</span><span class="sxs-lookup"><span data-stu-id="a08e3-107">**fwButtons**</span></span> 
</dt> <dd>

<span data-ttu-id="a08e3-108">Identifica el botón que ha cambiado de estado y los botones que se presionan.</span><span class="sxs-lookup"><span data-stu-id="a08e3-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="a08e3-109">Puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="a08e3-109">It can be one of the following:</span></span>



| <span data-ttu-id="a08e3-110">Value</span><span class="sxs-lookup"><span data-stu-id="a08e3-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="a08e3-111">Significado</span><span class="sxs-lookup"><span data-stu-id="a08e3-111">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <span data-ttu-id="a08e3-112"><dt>**JOY \_ BUTTON1CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e3-112"><dt>**JOY\_BUTTON1CHG**</dt></span></span> </dl> | <span data-ttu-id="a08e3-113">El primer botón del joystick ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="a08e3-113">First joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <span data-ttu-id="a08e3-114"><dt>**JOY \_ BUTTON2CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e3-114"><dt>**JOY\_BUTTON2CHG**</dt></span></span> </dl> | <span data-ttu-id="a08e3-115">El segundo botón del joystick ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="a08e3-115">Second joystick button has changed state.</span></span><br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <span data-ttu-id="a08e3-116"><dt>**JOY \_ BUTTON3CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e3-116"><dt>**JOY\_BUTTON3CHG**</dt></span></span> </dl> | <span data-ttu-id="a08e3-117">El tercer botón del joystick ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="a08e3-117">Third joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <span data-ttu-id="a08e3-118"><dt>**JOY \_ BUTTON4CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e3-118"><dt>**JOY\_BUTTON4CHG**</dt></span></span> </dl> | <span data-ttu-id="a08e3-119">El cuarto botón del joystick ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="a08e3-119">Fourth joystick button has changed state.</span></span><br/> |



 

<span data-ttu-id="a08e3-120">y uno o varios de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a08e3-120">and one or more of the following:</span></span>



| <span data-ttu-id="a08e3-121">Value</span><span class="sxs-lookup"><span data-stu-id="a08e3-121">Value</span></span>                                                                                                                                                   | <span data-ttu-id="a08e3-122">Significado</span><span class="sxs-lookup"><span data-stu-id="a08e3-122">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <span data-ttu-id="a08e3-123"><dt>**JOY \_ button1**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e3-123"><dt>**JOY\_BUTTON1**</dt></span></span> </dl> | <span data-ttu-id="a08e3-124">Se presionó el primer botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="a08e3-124">First joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <span data-ttu-id="a08e3-125"><dt>**JOY \_ BUTTON2**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e3-125"><dt>**JOY\_BUTTON2**</dt></span></span> </dl> | <span data-ttu-id="a08e3-126">Se presionó el botón segundo joystick.</span><span class="sxs-lookup"><span data-stu-id="a08e3-126">Second joystick button is pressed.</span></span><br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <span data-ttu-id="a08e3-127"><dt>**JOY \_ BUTTON3**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e3-127"><dt>**JOY\_BUTTON3**</dt></span></span> </dl> | <span data-ttu-id="a08e3-128">Se presionó el tercer botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="a08e3-128">Third joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <span data-ttu-id="a08e3-129"><dt>**JOY \_ BUTTON4**</dt></span><span class="sxs-lookup"><span data-stu-id="a08e3-129"><dt>**JOY\_BUTTON4**</dt></span></span> </dl> | <span data-ttu-id="a08e3-130">Se presionó el cuarto botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="a08e3-130">Fourth joystick button is pressed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a08e3-131">**xPos**</span><span class="sxs-lookup"><span data-stu-id="a08e3-131">**xPos**</span></span> 
</dt> <dd>

<span data-ttu-id="a08e3-132">Coordenadas x del joystick con respecto a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="a08e3-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="a08e3-133">**yPos**</span><span class="sxs-lookup"><span data-stu-id="a08e3-133">**yPos**</span></span> 
</dt> <dd>

<span data-ttu-id="a08e3-134">Coordenada y del joystick con respecto a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="a08e3-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a08e3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a08e3-135">Requirements</span></span>



| <span data-ttu-id="a08e3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a08e3-136">Requirement</span></span> | <span data-ttu-id="a08e3-137">Value</span><span class="sxs-lookup"><span data-stu-id="a08e3-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08e3-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a08e3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a08e3-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a08e3-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a08e3-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a08e3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a08e3-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a08e3-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a08e3-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a08e3-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a08e3-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a08e3-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08e3-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a08e3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08e3-145">Joysticks</span><span class="sxs-lookup"><span data-stu-id="a08e3-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="a08e3-146">Mensajes de joystick multimedia</span><span class="sxs-lookup"><span data-stu-id="a08e3-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 






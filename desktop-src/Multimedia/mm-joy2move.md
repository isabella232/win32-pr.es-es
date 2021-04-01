---
title: Mensaje de MM_JOY2MOVE (mmsystem. h)
description: El \_ mensaje mm JOY2MOVE notifica a la ventana que ha capturado el joystick JOYSTICKID2 que ha cambiado la posición del joystick.
ms.assetid: 8dc1c092-3947-43d5-8504-a4e4e121fbcb
keywords:
- Mensaje de MM_JOY2MOVE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_JOY2MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8921f0ae76d05c429d6750944a26662c1276af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149971"
---
# <a name="mm_joy2move-message"></a><span data-ttu-id="a452c-104">\_Mensaje JOY2MOVE mm</span><span class="sxs-lookup"><span data-stu-id="a452c-104">MM\_JOY2MOVE message</span></span>

<span data-ttu-id="a452c-105">El mensaje **mm \_ JOY2MOVE** notifica a la ventana que ha capturado el joystick JOYSTICKID2 que ha cambiado la posición del joystick.</span><span class="sxs-lookup"><span data-stu-id="a452c-105">The **MM\_JOY2MOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position has changed.</span></span>


```C++
MM_JOY2MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="a452c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a452c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a452c-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="a452c-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="a452c-108">Identifica los botones que se presionan.</span><span class="sxs-lookup"><span data-stu-id="a452c-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="a452c-109">Puede ser uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="a452c-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="a452c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a452c-110">Requirement</span></span> | <span data-ttu-id="a452c-111">Value</span><span class="sxs-lookup"><span data-stu-id="a452c-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="a452c-112">JOY \_ button1</span><span class="sxs-lookup"><span data-stu-id="a452c-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="a452c-113">Se presionó el primer botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="a452c-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="a452c-114">JOY \_ BUTTON2</span><span class="sxs-lookup"><span data-stu-id="a452c-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="a452c-115">Se presionó el botón segundo joystick.</span><span class="sxs-lookup"><span data-stu-id="a452c-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="a452c-116">JOY \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="a452c-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="a452c-117">Se presionó el tercer botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="a452c-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="a452c-118">JOY \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="a452c-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="a452c-119">Se presionó el cuarto botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="a452c-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a452c-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="a452c-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="a452c-121">Coordenadas x del joystick con respecto a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="a452c-121">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="a452c-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="a452c-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="a452c-123">Coordenada y del joystick con respecto a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="a452c-123">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a452c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a452c-124">Requirements</span></span>



| <span data-ttu-id="a452c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a452c-125">Requirement</span></span> | <span data-ttu-id="a452c-126">Value</span><span class="sxs-lookup"><span data-stu-id="a452c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a452c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a452c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a452c-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a452c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a452c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a452c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a452c-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a452c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a452c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a452c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a452c-132"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a452c-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a452c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a452c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a452c-134">Joysticks</span><span class="sxs-lookup"><span data-stu-id="a452c-134">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="a452c-135">Mensajes de joystick multimedia</span><span class="sxs-lookup"><span data-stu-id="a452c-135">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 






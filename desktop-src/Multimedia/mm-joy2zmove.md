---
title: Mensaje de MM_JOY2ZMOVE (mmsystem. h)
description: El \_ mensaje mm JOY2ZMOVE notifica a la ventana que ha capturado el joystick JOYSTICKID2 que ha cambiado la posición del joystick en el eje z.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- Mensaje de MM_JOY2ZMOVE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686255"
---
# <a name="mm_joy2zmove-message"></a><span data-ttu-id="0a13d-104">\_Mensaje JOY2ZMOVE mm</span><span class="sxs-lookup"><span data-stu-id="0a13d-104">MM\_JOY2ZMOVE message</span></span>

<span data-ttu-id="0a13d-105">El mensaje **mm \_ JOY2ZMOVE** notifica a la ventana que ha capturado el joystick JOYSTICKID2 que ha cambiado la posición del joystick en el eje z.</span><span class="sxs-lookup"><span data-stu-id="0a13d-105">The **MM\_JOY2ZMOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="0a13d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a13d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a13d-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="0a13d-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="0a13d-108">Identifica los botones que se presionan.</span><span class="sxs-lookup"><span data-stu-id="0a13d-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="0a13d-109">Puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0a13d-109">It can be one or more of the following values.</span></span>



| <span data-ttu-id="0a13d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a13d-110">Requirement</span></span> | <span data-ttu-id="0a13d-111">Value</span><span class="sxs-lookup"><span data-stu-id="0a13d-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="0a13d-112">JOY \_ button1</span><span class="sxs-lookup"><span data-stu-id="0a13d-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="0a13d-113">Se presionó el primer botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="0a13d-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="0a13d-114">JOY \_ BUTTON2</span><span class="sxs-lookup"><span data-stu-id="0a13d-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="0a13d-115">Se presionó el botón segundo joystick.</span><span class="sxs-lookup"><span data-stu-id="0a13d-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="0a13d-116">JOY \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="0a13d-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="0a13d-117">Se presionó el tercer botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="0a13d-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="0a13d-118">JOY \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="0a13d-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="0a13d-119">Se presionó el cuarto botón del joystick.</span><span class="sxs-lookup"><span data-stu-id="0a13d-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0a13d-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span><span class="sxs-lookup"><span data-stu-id="0a13d-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="0a13d-121">Coordenada z del joystick.</span><span class="sxs-lookup"><span data-stu-id="0a13d-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a13d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a13d-122">Requirements</span></span>



| <span data-ttu-id="0a13d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a13d-123">Requirement</span></span> | <span data-ttu-id="0a13d-124">Value</span><span class="sxs-lookup"><span data-stu-id="0a13d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a13d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a13d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0a13d-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0a13d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0a13d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a13d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0a13d-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a13d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0a13d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a13d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a13d-130"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a13d-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a13d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a13d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a13d-132">Joysticks</span><span class="sxs-lookup"><span data-stu-id="0a13d-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="0a13d-133">Mensajes de joystick multimedia</span><span class="sxs-lookup"><span data-stu-id="0a13d-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 






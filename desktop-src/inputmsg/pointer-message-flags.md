---
title: Marcas de mensajes de puntero
description: Valores que se usan en varias macros de puntero (vea macros).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720224"
---
# <a name="pointer-message-flags"></a><span data-ttu-id="9c479-103">Marcas de mensajes de puntero</span><span class="sxs-lookup"><span data-stu-id="9c479-103">Pointer Message Flags</span></span>

<span data-ttu-id="9c479-104">Valores que se usan en varias macros de puntero (vea [macros](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="9c479-104">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span>

<dl> <dt>

<span data-ttu-id="9c479-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="9c479-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9c479-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="9c479-107">Indica la llegada de un nuevo puntero.</span><span class="sxs-lookup"><span data-stu-id="9c479-107">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="9c479-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9c479-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="9c479-110">Indica que este puntero sigue existiendo.</span><span class="sxs-lookup"><span data-stu-id="9c479-110">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="9c479-111">Cuando no se establece esta marca, indica que el puntero tiene el intervalo de detección izquierdo.</span><span class="sxs-lookup"><span data-stu-id="9c479-111">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="9c479-112">Normalmente, esta marca no se establece solo cuando un puntero de desplazamiento deja el intervalo de detección (se establece **POINTER_FLAG_UPDATE** ) o cuando un puntero en contacto con una superficie de la ventana deja el intervalo de detección (se establece **POINTER_FLAG_UP** ).</span><span class="sxs-lookup"><span data-stu-id="9c479-112">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="9c479-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9c479-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="9c479-115">Indica que este puntero está en contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="9c479-115">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="9c479-116">Cuando no se establece esta marca, indica un puntero que mantiene el mouse.</span><span class="sxs-lookup"><span data-stu-id="9c479-116">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="9c479-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-118">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c479-118">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="9c479-119">Indica una acción principal, análoga a un botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="9c479-119">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="9c479-120">Un puntero táctil tiene esta marca establecida cuando está en contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="9c479-120">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="9c479-121">Un puntero de pluma tiene esta marca establecida cuando está en contacto con la superficie del digitalizador sin presionar ningún botón.</span><span class="sxs-lookup"><span data-stu-id="9c479-121">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="9c479-122">Un puntero del mouse tiene esta marca establecida cuando el botón primario del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="9c479-122">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="9c479-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-124">0x00000020</span><span class="sxs-lookup"><span data-stu-id="9c479-124">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="9c479-125">Indica una acción secundaria, análoga a un botón secundario del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="9c479-125">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="9c479-126">Un puntero táctil no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="9c479-126">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="9c479-127">Un puntero de lápiz tiene esta marca establecida cuando está en contacto con la superficie del digitalizador con el botón de barril del lápiz presionado.</span><span class="sxs-lookup"><span data-stu-id="9c479-127">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="9c479-128">Un puntero del mouse tiene esta marca establecida cuando el botón secundario del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="9c479-128">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="9c479-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-130">0x00000040</span><span class="sxs-lookup"><span data-stu-id="9c479-130">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="9c479-131">Análogo a un botón de rueda del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="9c479-131">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="9c479-132">Un puntero táctil no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="9c479-132">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="9c479-133">Un puntero de lápiz no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="9c479-133">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="9c479-134">Un puntero del mouse tiene esta marca establecida cuando el botón de la rueda del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="9c479-134">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="9c479-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-136">0x00000080</span><span class="sxs-lookup"><span data-stu-id="9c479-136">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="9c479-137">Análogo a un botón de la primera tecla del mouse extendido (XButton1).</span><span class="sxs-lookup"><span data-stu-id="9c479-137">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="9c479-138">Un puntero táctil no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="9c479-138">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="9c479-139">Un puntero de lápiz no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="9c479-139">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="9c479-140">Un puntero del mouse tiene esta marca establecida cuando el botón del primer Mouse extendido (XBUTTON1) está inactivo.</span><span class="sxs-lookup"><span data-stu-id="9c479-140">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="9c479-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="9c479-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="9c479-143">Análogo a un segundo botón de mouse extendido (XButton2).</span><span class="sxs-lookup"><span data-stu-id="9c479-143">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="9c479-144">Un puntero táctil no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="9c479-144">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="9c479-145">Un puntero de lápiz no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="9c479-145">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="9c479-146">Un puntero del mouse tiene esta marca establecida cuando el botón del segundo Mouse extendido (XBUTTON2) está inactivo.</span><span class="sxs-lookup"><span data-stu-id="9c479-146">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="9c479-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-148">0x00002000</span><span class="sxs-lookup"><span data-stu-id="9c479-148">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="9c479-149">Indica que este puntero se ha designado como puntero primario.</span><span class="sxs-lookup"><span data-stu-id="9c479-149">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="9c479-150">Un puntero primario es un puntero único que puede realizar acciones más allá de las que están disponibles para los punteros no principales.</span><span class="sxs-lookup"><span data-stu-id="9c479-150">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="9c479-151">Por ejemplo, cuando un puntero primario establece contacto con la superficie de una ventana, puede proporcionar a la ventana una oportunidad de activar mediante el envío de un mensaje de WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="9c479-151">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a WM_POINTERACTIVATE message.</span></span>

<span data-ttu-id="9c479-152">El puntero principal se identifica a partir de todas las interacciones del usuario actual en el sistema (mouse, táctil, lápiz, etc.).</span><span class="sxs-lookup"><span data-stu-id="9c479-152">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="9c479-153">Por lo tanto, es posible que el puntero principal no esté asociado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9c479-153">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="9c479-154">El primer contacto en una interacción multitáctil se establece como el puntero principal.</span><span class="sxs-lookup"><span data-stu-id="9c479-154">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="9c479-155">Una vez que se identifica un puntero principal, todos los contactos deben levantarse antes de que se pueda identificar un nuevo contacto como puntero principal.</span><span class="sxs-lookup"><span data-stu-id="9c479-155">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="9c479-156">En el caso de las aplicaciones que no procesan la entrada de puntero, solo los eventos del puntero primario se promueven a los eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="9c479-156">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="9c479-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-158">0x00000400</span><span class="sxs-lookup"><span data-stu-id="9c479-158">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="9c479-159">La confianza es una sugerencia del dispositivo de origen sobre si el puntero representa una interacción intencionada o intencional, que es especialmente relevante para los punteros de PT_TOUCH en los que una interacción accidental (como con la palma de la mano) puede desencadenar la entrada.</span><span class="sxs-lookup"><span data-stu-id="9c479-159">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="9c479-160">La presencia de esta marca indica que el dispositivo de origen tiene una alta confianza de que esta entrada forma parte de una interacción prevista.</span><span class="sxs-lookup"><span data-stu-id="9c479-160">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c479-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="9c479-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c479-162">0x00000800</span><span class="sxs-lookup"><span data-stu-id="9c479-162">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="9c479-163">Indica que el puntero se está desasociando de una manera anómala, como cuando el sistema recibe una entrada no válida para el puntero o cuando un dispositivo con punteros activos se parte repentinamente.</span><span class="sxs-lookup"><span data-stu-id="9c479-163">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="9c479-164">Si la aplicación que recibe la entrada está en una posición para hacerlo, debe tratar la interacción como no completada e invertir los efectos del puntero en cuestión.</span><span class="sxs-lookup"><span data-stu-id="9c479-164">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c479-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c479-165">Remarks</span></span>

<span data-ttu-id="9c479-166">XBUTTON1 y XBUTTON2 son botones adicionales que se usan en muchos dispositivos de mouse.</span><span class="sxs-lookup"><span data-stu-id="9c479-166">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="9c479-167">Devuelven los mismos datos que los botones estándar del mouse.</span><span class="sxs-lookup"><span data-stu-id="9c479-167">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c479-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c479-168">Requirements</span></span>



| <span data-ttu-id="9c479-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c479-169">Requirement</span></span> | <span data-ttu-id="9c479-170">Value</span><span class="sxs-lookup"><span data-stu-id="9c479-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c479-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c479-171">Minimum supported client</span></span><br/> | <span data-ttu-id="9c479-172">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c479-172">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9c479-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c479-173">Minimum supported server</span></span><br/> | <span data-ttu-id="9c479-174">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c479-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c479-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c479-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c479-176"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c479-176"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c479-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c479-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c479-178">Constantes</span><span class="sxs-lookup"><span data-stu-id="9c479-178">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="9c479-179">Macros</span><span class="sxs-lookup"><span data-stu-id="9c479-179">Macros</span></span>](macros.md)
</dt> </dl>

 

 






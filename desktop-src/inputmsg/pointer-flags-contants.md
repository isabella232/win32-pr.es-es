---
title: Marcas de puntero
description: Valores que pueden aparecer en el campo pointerFlags de la estructura POINTER_INFO.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802899"
---
# <a name="pointer-flags"></a><span data-ttu-id="e76c4-103">Marcas de puntero</span><span class="sxs-lookup"><span data-stu-id="e76c4-103">Pointer Flags</span></span>

<span data-ttu-id="e76c4-104">Valores que pueden aparecer en el campo **pointerFlags** de la estructura [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="e76c4-104">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="e76c4-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="e76c4-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e76c4-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-107">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="e76c4-107">Default</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="e76c4-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e76c4-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-110">Indica la llegada de un nuevo puntero.</span><span class="sxs-lookup"><span data-stu-id="e76c4-110">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="e76c4-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-112">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e76c4-112">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-113">Indica que este puntero sigue existiendo.</span><span class="sxs-lookup"><span data-stu-id="e76c4-113">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="e76c4-114">Cuando no se establece esta marca, indica que el puntero tiene el intervalo de detección izquierdo.</span><span class="sxs-lookup"><span data-stu-id="e76c4-114">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="e76c4-115">Normalmente, esta marca no se establece solo cuando un puntero de desplazamiento deja el intervalo de detección (se establece **POINTER_FLAG_UPDATE** ) o cuando un puntero en contacto con una superficie de la ventana deja el intervalo de detección (se establece **POINTER_FLAG_UP** ).</span><span class="sxs-lookup"><span data-stu-id="e76c4-115">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="e76c4-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-117">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e76c4-117">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-118">Indica que este puntero está en contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="e76c4-118">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="e76c4-119">Cuando no se establece esta marca, indica un puntero que mantiene el mouse.</span><span class="sxs-lookup"><span data-stu-id="e76c4-119">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e76c4-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-121">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e76c4-121">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-122">Indica una acción principal, análoga a un botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="e76c4-122">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="e76c4-123">Un puntero táctil tiene esta marca establecida cuando está en contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="e76c4-123">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="e76c4-124">Un puntero de pluma tiene esta marca establecida cuando está en contacto con la superficie del digitalizador sin presionar ningún botón.</span><span class="sxs-lookup"><span data-stu-id="e76c4-124">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="e76c4-125">Un puntero del mouse tiene esta marca establecida cuando el botón primario del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="e76c4-125">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e76c4-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-127">0x00000020</span><span class="sxs-lookup"><span data-stu-id="e76c4-127">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-128">Indica una acción secundaria, análoga a un botón secundario del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="e76c4-128">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="e76c4-129">Un puntero táctil no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="e76c4-129">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e76c4-130">Un puntero de lápiz tiene esta marca establecida cuando está en contacto con la superficie del digitalizador con el botón de barril del lápiz presionado.</span><span class="sxs-lookup"><span data-stu-id="e76c4-130">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="e76c4-131">Un puntero del mouse tiene esta marca establecida cuando el botón secundario del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="e76c4-131">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e76c4-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-133">0x00000040</span><span class="sxs-lookup"><span data-stu-id="e76c4-133">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-134">Análogo a un botón de rueda del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="e76c4-134">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="e76c4-135">Un puntero táctil no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="e76c4-135">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e76c4-136">Un puntero de lápiz no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="e76c4-136">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e76c4-137">Un puntero del mouse tiene esta marca establecida cuando el botón de la rueda del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="e76c4-137">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e76c4-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="e76c4-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-140">Análogo a un botón de la primera tecla del mouse extendido (XButton1).</span><span class="sxs-lookup"><span data-stu-id="e76c4-140">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="e76c4-141">Un puntero táctil no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="e76c4-141">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e76c4-142">Un puntero de lápiz no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="e76c4-142">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e76c4-143">Un puntero del mouse tiene esta marca establecida cuando el botón del primer Mouse extendido (XBUTTON1) está inactivo.</span><span class="sxs-lookup"><span data-stu-id="e76c4-143">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e76c4-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-145">0x00000100</span><span class="sxs-lookup"><span data-stu-id="e76c4-145">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-146">Análogo a un segundo botón de mouse extendido (XButton2).</span><span class="sxs-lookup"><span data-stu-id="e76c4-146">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="e76c4-147">Un puntero táctil no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="e76c4-147">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e76c4-148">Un puntero de lápiz no usa esta marca.</span><span class="sxs-lookup"><span data-stu-id="e76c4-148">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e76c4-149">Un puntero del mouse tiene esta marca establecida cuando el botón del segundo Mouse extendido (XBUTTON2) está inactivo.</span><span class="sxs-lookup"><span data-stu-id="e76c4-149">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="e76c4-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="e76c4-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-152">Indica que este puntero se ha designado como puntero primario.</span><span class="sxs-lookup"><span data-stu-id="e76c4-152">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="e76c4-153">Un puntero primario es un puntero único que puede realizar acciones más allá de las que están disponibles para los punteros no principales.</span><span class="sxs-lookup"><span data-stu-id="e76c4-153">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="e76c4-154">Por ejemplo, cuando un puntero primario establece contacto con la superficie de una ventana, puede proporcionar a la ventana una oportunidad de activar mediante el envío de un mensaje de [**WM_POINTERACTIVATE**](wm-pointeractivate.md) .</span><span class="sxs-lookup"><span data-stu-id="e76c4-154">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a [**WM_POINTERACTIVATE**](wm-pointeractivate.md) message.</span></span>

<span data-ttu-id="e76c4-155">El puntero principal se identifica a partir de todas las interacciones del usuario actual en el sistema (mouse, táctil, lápiz, etc.).</span><span class="sxs-lookup"><span data-stu-id="e76c4-155">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="e76c4-156">Por lo tanto, es posible que el puntero principal no esté asociado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e76c4-156">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="e76c4-157">El primer contacto en una interacción multitáctil se establece como el puntero principal.</span><span class="sxs-lookup"><span data-stu-id="e76c4-157">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="e76c4-158">Una vez que se identifica un puntero principal, todos los contactos deben levantarse antes de que se pueda identificar un nuevo contacto como puntero principal.</span><span class="sxs-lookup"><span data-stu-id="e76c4-158">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="e76c4-159">En el caso de las aplicaciones que no procesan la entrada de puntero, solo los eventos del puntero primario se promueven a los eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="e76c4-159">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="e76c4-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-161">0x000004000</span><span class="sxs-lookup"><span data-stu-id="e76c4-161">0x000004000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-162">La confianza es una sugerencia del dispositivo de origen sobre si el puntero representa una interacción intencionada o intencional, que es especialmente relevante para los punteros de PT_TOUCH en los que una interacción accidental (como con la palma de la mano) puede desencadenar la entrada.</span><span class="sxs-lookup"><span data-stu-id="e76c4-162">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="e76c4-163">La presencia de esta marca indica que el dispositivo de origen tiene una alta confianza de que esta entrada forma parte de una interacción prevista.</span><span class="sxs-lookup"><span data-stu-id="e76c4-163">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="e76c4-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-165">0x000008000</span><span class="sxs-lookup"><span data-stu-id="e76c4-165">0x000008000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-166">Indica que el puntero se está desasociando de una manera anómala, como cuando el sistema recibe una entrada no válida para el puntero o cuando un dispositivo con punteros activos se parte repentinamente.</span><span class="sxs-lookup"><span data-stu-id="e76c4-166">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="e76c4-167">Si la aplicación que recibe la entrada está en una posición para hacerlo, debe tratar la interacción como no completada e invertir los efectos del puntero en cuestión.</span><span class="sxs-lookup"><span data-stu-id="e76c4-167">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span><span class="sxs-lookup"><span data-stu-id="e76c4-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-169">0x00010000</span><span class="sxs-lookup"><span data-stu-id="e76c4-169">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-170">Indica que este puntero ha pasado a un estado de inactividad; es decir, se puso en contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="e76c4-170">Indicates that this pointer transitioned to a down state; that is, it made contact with the digitizer surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span><span class="sxs-lookup"><span data-stu-id="e76c4-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-172">0x00020000</span><span class="sxs-lookup"><span data-stu-id="e76c4-172">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-173">Indica que se trata de una actualización simple que no incluye los cambios de estado de puntero.</span><span class="sxs-lookup"><span data-stu-id="e76c4-173">Indicates that this is a simple update that does not include pointer state changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span><span class="sxs-lookup"><span data-stu-id="e76c4-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-175">0x00040000</span><span class="sxs-lookup"><span data-stu-id="e76c4-175">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-176">Indica que este puntero ha pasado a un estado up; es decir, ha finalizado el contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="e76c4-176">Indicates that this pointer transitioned to an up state; that is, contact with the digitizer surface ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span><span class="sxs-lookup"><span data-stu-id="e76c4-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-178">0x00080000</span><span class="sxs-lookup"><span data-stu-id="e76c4-178">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-179">Indica la entrada asociada a una rueda de puntero.</span><span class="sxs-lookup"><span data-stu-id="e76c4-179">Indicates input associated with a pointer wheel.</span></span> <span data-ttu-id="e76c4-180">En el caso de los punteros del mouse, es equivalente a la acción de la rueda de desplazamiento del mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="e76c4-180">For mouse pointers, this is equivalent to the action of the mouse scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span><span class="sxs-lookup"><span data-stu-id="e76c4-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="e76c4-182">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-183">Indica la entrada asociada a una rueda h de puntero.</span><span class="sxs-lookup"><span data-stu-id="e76c4-183">Indicates input associated with a pointer h-wheel.</span></span> <span data-ttu-id="e76c4-184">En el caso de los punteros del mouse, es equivalente a la acción de la rueda de desplazamiento horizontal del mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="e76c4-184">For mouse pointers, this is equivalent to the action of the mouse horizontal scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span><span class="sxs-lookup"><span data-stu-id="e76c4-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-186">0x00200000</span><span class="sxs-lookup"><span data-stu-id="e76c4-186">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-187">Indica que se ha capturado este puntero (asociado con) a otro elemento y el elemento original ha perdido la captura (vea [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span><span class="sxs-lookup"><span data-stu-id="e76c4-187">Indicates that this pointer was captured by (associated with) another element and the original element has lost capture (see [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e76c4-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="e76c4-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e76c4-189">0x00400000</span><span class="sxs-lookup"><span data-stu-id="e76c4-189">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="e76c4-190">Indica que este puntero tiene una transformación asociada.</span><span class="sxs-lookup"><span data-stu-id="e76c4-190">Indicates that this pointer has an associated transform.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e76c4-191">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e76c4-191">Remarks</span></span>

<span data-ttu-id="e76c4-192">XBUTTON1 y XBUTTON2 son botones adicionales que se usan en muchos dispositivos de mouse.</span><span class="sxs-lookup"><span data-stu-id="e76c4-192">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="e76c4-193">Devuelven los mismos datos que los botones estándar del mouse.</span><span class="sxs-lookup"><span data-stu-id="e76c4-193">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="e76c4-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e76c4-194">Requirements</span></span>



| <span data-ttu-id="e76c4-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="e76c4-195">Requirement</span></span> | <span data-ttu-id="e76c4-196">Value</span><span class="sxs-lookup"><span data-stu-id="e76c4-196">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e76c4-197">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e76c4-197">Minimum supported client</span></span><br/> | <span data-ttu-id="e76c4-198">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e76c4-198">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e76c4-199">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e76c4-199">Minimum supported server</span></span><br/> | <span data-ttu-id="e76c4-200">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e76c4-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e76c4-201">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e76c4-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="e76c4-202"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e76c4-202"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e76c4-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="e76c4-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76c4-204">Constantes</span><span class="sxs-lookup"><span data-stu-id="e76c4-204">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="e76c4-205">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="e76c4-205">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="e76c4-206">**POINTER_BUTTON_CHANGE_TYPE**</span><span class="sxs-lookup"><span data-stu-id="e76c4-206">**POINTER_BUTTON_CHANGE_TYPE**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 


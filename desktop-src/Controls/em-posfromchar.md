---
title: Mensaje de EM_POSFROMCHAR (Winuser. h)
description: Recupera las coordenadas del área de cliente de un carácter especificado en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534366"
---
# <a name="em_posfromchar-message"></a><span data-ttu-id="64816-105">\_Mensaje POSFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="64816-105">EM\_POSFROMCHAR message</span></span>

<span data-ttu-id="64816-106">Recupera las coordenadas del área de cliente de un carácter especificado en un control de edición.</span><span class="sxs-lookup"><span data-stu-id="64816-106">Retrieves the client area coordinates of a specified character in an edit control.</span></span> <span data-ttu-id="64816-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="64816-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="64816-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64816-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64816-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64816-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64816-110">**Edición enriquecida 1,0 y 3,0:** Puntero a una estructura [**Pointl**](/previous-versions//dd162807(v=vs.85)) que recibe las coordenadas del área de cliente del carácter.</span><span class="sxs-lookup"><span data-stu-id="64816-110">**Rich Edit 1.0 and 3.0:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that receives the client area coordinates of the character.</span></span> <span data-ttu-id="64816-111">Las coordenadas están en unidades de pantalla y son relativas a la esquina superior izquierda del área cliente del control.</span><span class="sxs-lookup"><span data-stu-id="64816-111">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="64816-112">**Controles de edición y edición enriquecida 2,0:** Índice de base cero del carácter.</span><span class="sxs-lookup"><span data-stu-id="64816-112">**Edit controls and Rich Edit 2.0:** The zero-based index of the character.</span></span>

</dd> <dt>

<span data-ttu-id="64816-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64816-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64816-114">**Edición enriquecida 1,0 y 3,0:** Índice de base cero del carácter.</span><span class="sxs-lookup"><span data-stu-id="64816-114">**Rich Edit 1.0 and 3.0:** The zero-based index of the character.</span></span>

<span data-ttu-id="64816-115">**Controles de edición y edición enriquecida 2,0:** Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="64816-115">**Edit controls and Rich Edit 2.0:** This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64816-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64816-116">Return value</span></span>

<span data-ttu-id="64816-117">**Edición enriquecida 1,0 y 3,0:** No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="64816-117">**Rich Edit 1.0 and 3.0:** The return value is not used.</span></span>

<span data-ttu-id="64816-118">**Controles de edición y edición enriquecida 2,0:** El valor devuelto contiene las coordenadas del área del cliente del carácter.</span><span class="sxs-lookup"><span data-stu-id="64816-118">**Edit controls and Rich Edit 2.0:** The return value contains the client area coordinates of the character.</span></span> <span data-ttu-id="64816-119">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordenada horizontal y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordenada vertical.</span><span class="sxs-lookup"><span data-stu-id="64816-119">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

## <a name="remarks"></a><span data-ttu-id="64816-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64816-120">Remarks</span></span>

<span data-ttu-id="64816-121">Una coordenada devuelta puede ser un valor negativo si el carácter especificado no se muestra en el área cliente del control de edición.</span><span class="sxs-lookup"><span data-stu-id="64816-121">A returned coordinate can be a negative value if the specified character is not displayed in the edit control's client area.</span></span> <span data-ttu-id="64816-122">Las coordenadas se truncan en valores enteros.</span><span class="sxs-lookup"><span data-stu-id="64816-122">The coordinates are truncated to integer values.</span></span>

<span data-ttu-id="64816-123">Si el carácter es un delimitador de línea, las coordenadas devueltas indican un punto situado más allá del último carácter visible de la línea.</span><span class="sxs-lookup"><span data-stu-id="64816-123">If the character is a line delimiter, the returned coordinates indicate a point just beyond the last visible character in the line.</span></span> <span data-ttu-id="64816-124">Si el índice especificado es mayor que el índice del último carácter del control, el control devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="64816-124">If the specified index is greater than the index of the last character in the control, the control returns -1.</span></span>

<span data-ttu-id="64816-125">**Edición enriquecida 3,0 y versiones posteriores:** Por compatibilidad con versiones anteriores, Microsoft Rich Edit 3,0 admite la sintaxis que usa Microsoft Rich Edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="64816-125">**Rich Edit 3.0 and later:** For backward compatibility, Microsoft Rich Edit 3.0 supports the syntax used by Microsoft Rich Edit 2.0.</span></span> <span data-ttu-id="64816-126">Si Microsoft Rich Edit 3,0 detecta que *wParam* no es un puntero [**Pointl**](/previous-versions//dd162807(v=vs.85)) válido, se supone que el mensaje se envió con la sintaxis de Microsoft Rich Edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="64816-126">If Microsoft Rich Edit 3.0 detects that *wParam* is not a valid [**POINTL**](/previous-versions//dd162807(v=vs.85)) pointer, it assumes the message was sent using the Microsoft Rich Edit 2.0 syntax.</span></span> <span data-ttu-id="64816-127">En este caso, utiliza el valor devuelto para devolver las coordenadas.</span><span class="sxs-lookup"><span data-stu-id="64816-127">In this case, it uses the return value to return the coordinates.</span></span>

<span data-ttu-id="64816-128">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="64816-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="64816-129">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="64816-129">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64816-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64816-130">Requirements</span></span>



| <span data-ttu-id="64816-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="64816-131">Requirement</span></span> | <span data-ttu-id="64816-132">Value</span><span class="sxs-lookup"><span data-stu-id="64816-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64816-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64816-133">Minimum supported client</span></span><br/> | <span data-ttu-id="64816-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="64816-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64816-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64816-135">Minimum supported server</span></span><br/> | <span data-ttu-id="64816-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="64816-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64816-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64816-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="64816-138"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64816-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64816-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="64816-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="64816-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="64816-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64816-141">**\_CHARFROMPOS em**</span><span class="sxs-lookup"><span data-stu-id="64816-141">**EM\_CHARFROMPOS**</span></span>](em-charfrompos.md)
</dt> <dt>

<span data-ttu-id="64816-142">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="64816-142">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="64816-143">[**PUNTO**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64816-143">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 


---
title: Mensaje de EM_CHARFROMPOS (Winuser. h)
description: Obtiene información sobre el carácter más cercano a un punto especificado en el área cliente de un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- EM_CHARFROMPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491500"
---
# <a name="em_charfrompos-message"></a><span data-ttu-id="430c0-105">\_Mensaje CHARFROMPOS em</span><span class="sxs-lookup"><span data-stu-id="430c0-105">EM\_CHARFROMPOS message</span></span>

<span data-ttu-id="430c0-106">Obtiene información sobre el carácter más cercano a un punto especificado en el área cliente de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="430c0-106">Gets information about the character closest to a specified point in the client area of an edit control.</span></span> <span data-ttu-id="430c0-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="430c0-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="430c0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="430c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="430c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="430c0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="430c0-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="430c0-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="430c0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="430c0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="430c0-112">Coordenadas de un punto en el área cliente del control.</span><span class="sxs-lookup"><span data-stu-id="430c0-112">The coordinates of a point in the control's client area.</span></span> <span data-ttu-id="430c0-113">Las coordenadas están en unidades de pantalla y son relativas a la esquina superior izquierda del área cliente del control.</span><span class="sxs-lookup"><span data-stu-id="430c0-113">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="430c0-114">**Controles Rich Edit:** Puntero a una estructura [**Pointl**](/previous-versions//dd162807(v=vs.85)) que contiene las coordenadas horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="430c0-114">**Rich edit controls:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that contains the horizontal and vertical coordinates.</span></span>

<span data-ttu-id="430c0-115">**Controles de edición:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordenada horizontal.</span><span class="sxs-lookup"><span data-stu-id="430c0-115">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate.</span></span> <span data-ttu-id="430c0-116">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordenada vertical.</span><span class="sxs-lookup"><span data-stu-id="430c0-116">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="430c0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="430c0-117">Return value</span></span>

<span data-ttu-id="430c0-118">**Controles Rich Edit:** El valor devuelto especifica el índice de carácter de base cero del carácter más próximo al punto especificado.</span><span class="sxs-lookup"><span data-stu-id="430c0-118">**Rich edit controls:** The return value specifies the zero-based character index of the character nearest the specified point.</span></span> <span data-ttu-id="430c0-119">El valor devuelto indica el último carácter del control de edición si el punto especificado está más allá del último carácter del control.</span><span class="sxs-lookup"><span data-stu-id="430c0-119">The return value indicates the last character in the edit control if the specified point is beyond the last character in the control.</span></span>

<span data-ttu-id="430c0-120">**Controles de edición:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el índice de base cero del carácter más próximo al punto especificado.</span><span class="sxs-lookup"><span data-stu-id="430c0-120">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the character nearest the specified point.</span></span> <span data-ttu-id="430c0-121">Este índice es relativo al principio del control, no al principio de la línea.</span><span class="sxs-lookup"><span data-stu-id="430c0-121">This index is relative to the beginning of the control, not the beginning of the line.</span></span> <span data-ttu-id="430c0-122">Si el punto especificado está más allá del último carácter del control de edición, el valor devuelto indica el último carácter del control.</span><span class="sxs-lookup"><span data-stu-id="430c0-122">If the specified point is beyond the last character in the edit control, the return value indicates the last character in the control.</span></span> <span data-ttu-id="430c0-123">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el índice de base cero de la línea que contiene el carácter.</span><span class="sxs-lookup"><span data-stu-id="430c0-123">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the line that contains the character.</span></span> <span data-ttu-id="430c0-124">En el caso de los controles de edición de una sola línea, este valor es cero.</span><span class="sxs-lookup"><span data-stu-id="430c0-124">For single-line edit controls, this value is zero.</span></span> <span data-ttu-id="430c0-125">El índice indica el delimitador de línea si el punto especificado está más allá del último carácter visible de una línea.</span><span class="sxs-lookup"><span data-stu-id="430c0-125">The index indicates the line delimiter if the specified point is beyond the last visible character in a line.</span></span>

## <a name="remarks"></a><span data-ttu-id="430c0-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="430c0-126">Remarks</span></span>

<span data-ttu-id="430c0-127">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="430c0-127">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="430c0-128">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="430c0-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="430c0-129">Si se pasa un punto a **em \_ CHARFROMPOS** como *lParam* y el punto está fuera de los límites del control de edición, el *lResult* es (65535, 65535).</span><span class="sxs-lookup"><span data-stu-id="430c0-129">If a point is passed to **EM\_CHARFROMPOS** as the *lParam* and the point is outside the bounds of the edit control, then the *lResult* is (65535, 65535).</span></span>

## <a name="requirements"></a><span data-ttu-id="430c0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="430c0-130">Requirements</span></span>



| <span data-ttu-id="430c0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="430c0-131">Requirement</span></span> | <span data-ttu-id="430c0-132">Value</span><span class="sxs-lookup"><span data-stu-id="430c0-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="430c0-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="430c0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="430c0-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="430c0-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="430c0-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="430c0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="430c0-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="430c0-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="430c0-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="430c0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="430c0-138"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="430c0-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="430c0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="430c0-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="430c0-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="430c0-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="430c0-141">**\_POSFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="430c0-141">**EM\_POSFROMCHAR**</span></span>](em-posfromchar.md)
</dt> <dt>

<span data-ttu-id="430c0-142">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="430c0-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="430c0-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="430c0-143">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

<span data-ttu-id="430c0-144">[**PUNTO**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="430c0-144">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 


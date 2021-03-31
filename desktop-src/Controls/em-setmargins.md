---
title: Mensaje de EM_SETMARGINS (Winuser. h)
description: Establece el ancho de los márgenes izquierdo y derecho de un control de edición. El mensaje vuelve a dibujar el control para reflejar los nuevos márgenes. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996565"
---
# <a name="em_setmargins-message"></a><span data-ttu-id="a88fb-106">\_Mensaje SETMARGINS em</span><span class="sxs-lookup"><span data-stu-id="a88fb-106">EM\_SETMARGINS message</span></span>

<span data-ttu-id="a88fb-107">Establece el ancho de los márgenes izquierdo y derecho de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="a88fb-107">Sets the widths of the left and right margins for an edit control.</span></span> <span data-ttu-id="a88fb-108">El mensaje vuelve a dibujar el control para reflejar los nuevos márgenes.</span><span class="sxs-lookup"><span data-stu-id="a88fb-108">The message redraws the control to reflect the new margins.</span></span> <span data-ttu-id="a88fb-109">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a88fb-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a88fb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a88fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a88fb-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a88fb-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a88fb-112">Márgenes que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="a88fb-112">The margins to set.</span></span> <span data-ttu-id="a88fb-113">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a88fb-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a88fb-114">Value</span><span class="sxs-lookup"><span data-stu-id="a88fb-114">Value</span></span>                                                                                                                                                            | <span data-ttu-id="a88fb-115">Significado</span><span class="sxs-lookup"><span data-stu-id="a88fb-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <span data-ttu-id="a88fb-116"><dt>**LEFTMARGIN de EC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a88fb-116"><dt>**EC\_LEFTMARGIN**</dt></span></span> </dl>    | <span data-ttu-id="a88fb-117">Establece el margen izquierdo.</span><span class="sxs-lookup"><span data-stu-id="a88fb-117">Sets the left margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <span data-ttu-id="a88fb-118"><dt>**RIGHTMARGIN de EC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a88fb-118"><dt>**EC\_RIGHTMARGIN**</dt></span></span> </dl> | <span data-ttu-id="a88fb-119">Establece el margen derecho.</span><span class="sxs-lookup"><span data-stu-id="a88fb-119">Sets the right margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <span data-ttu-id="a88fb-120"><dt>**USEFONTINFO de EC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a88fb-120"><dt>**EC\_USEFONTINFO**</dt></span></span> </dl> | <span data-ttu-id="a88fb-121">**Controles Rich Edit:** Establece los márgenes izquierdo y derecho en un ancho estrecho calculado con las métricas de texto de la fuente actual del control.</span><span class="sxs-lookup"><span data-stu-id="a88fb-121">**Rich edit controls:** Sets the left and right margins to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="a88fb-122">Si no se ha establecido ninguna fuente para el control, los márgenes se establecen en cero.</span><span class="sxs-lookup"><span data-stu-id="a88fb-122">If no font has been set for the control, the margins are set to zero.</span></span> <span data-ttu-id="a88fb-123">Se omite el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="a88fb-123">The *lParam* parameter is ignored.</span></span> <br/> <span data-ttu-id="a88fb-124">**Controles de edición:** El **valor \_ USEFONTINFO de EC** no se puede usar en el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a88fb-124">**Edit controls:** The **EC\_USEFONTINFO** value cannot be used in the *wParam* parameter.</span></span> <span data-ttu-id="a88fb-125">Solo se puede usar en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="a88fb-125">It can only be used in the *lParam* parameter.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a88fb-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a88fb-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a88fb-127">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el nuevo ancho del margen izquierdo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a88fb-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new width of the left margin, in pixels.</span></span> <span data-ttu-id="a88fb-128">Este valor se omite si *wParam* no incluye los valores de **\_ LEFTMARGIN de EC**.</span><span class="sxs-lookup"><span data-stu-id="a88fb-128">This value is ignored if *wParam* does not include **EC\_LEFTMARGIN**.</span></span>

<span data-ttu-id="a88fb-129">**Edite los controles y la edición enriquecida 3,0 y versiones posteriores:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) puede especificar el valor **\_ USEFONTINFO de EC** para establecer el margen izquierdo en un ancho estrecho calculado con las métricas de texto de la fuente actual del control.</span><span class="sxs-lookup"><span data-stu-id="a88fb-129">**Edit controls and Rich Edit 3.0 and later:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the left margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="a88fb-130">Si no se ha establecido ninguna fuente para el control, el margen se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="a88fb-130">If no font has been set for the control, the margin is set to zero.</span></span>

<span data-ttu-id="a88fb-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el nuevo ancho del margen derecho, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a88fb-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new width of the right margin, in pixels.</span></span> <span data-ttu-id="a88fb-132">Este valor se omite si *wParam* no incluye el **\_ RIGHTMARGIN de EC**.</span><span class="sxs-lookup"><span data-stu-id="a88fb-132">This value is ignored if *wParam* does not include **EC\_RIGHTMARGIN**.</span></span>

<span data-ttu-id="a88fb-133">**Edite los controles y la edición enriquecida 3,0 y versiones posteriores:** [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) puede especificar el valor **\_ USEFONTINFO de EC** para establecer el margen derecho en un ancho estrecho calculado con las métricas de texto de la fuente actual del control.</span><span class="sxs-lookup"><span data-stu-id="a88fb-133">**Edit controls and Rich Edit 3.0 and later:** The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the right margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="a88fb-134">Si no se ha establecido ninguna fuente para el control, el margen se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="a88fb-134">If no font has been set for the control, the margin is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a88fb-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a88fb-135">Return value</span></span>

<span data-ttu-id="a88fb-136">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a88fb-136">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a88fb-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a88fb-137">Remarks</span></span>

<span data-ttu-id="a88fb-138">**Controles de edición:** No se puede **usar \_ USEFONTINFO de EC** en el parámetro *wParam* , pero se puede usar en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="a88fb-138">**Edit controls:** You cannot use **EC\_USEFONTINFO** in the *wParam* parameter, but you can use it in the *lParam* parameter.</span></span>

<span data-ttu-id="a88fb-139">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a88fb-139">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a88fb-140">Todas las versiones de edición enriquecidas admiten el uso de **\_ USEFONTINFO de EC** en el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a88fb-140">All rich edit versions support the use of **EC\_USEFONTINFO** in the *wParam* parameter.</span></span> <span data-ttu-id="a88fb-141">Sin embargo, solo Microsoft Rich Edit 3,0 y versiones posteriores admiten el uso de **\_ USEFONTINFO de EC** en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="a88fb-141">However, only Microsoft Rich Edit 3.0 and later support the use of **EC\_USEFONTINFO** in the *lParam* parameter.</span></span> <span data-ttu-id="a88fb-142">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a88fb-142">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a88fb-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a88fb-143">Requirements</span></span>



| <span data-ttu-id="a88fb-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a88fb-144">Requirement</span></span> | <span data-ttu-id="a88fb-145">Value</span><span class="sxs-lookup"><span data-stu-id="a88fb-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a88fb-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a88fb-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a88fb-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a88fb-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a88fb-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a88fb-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a88fb-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a88fb-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a88fb-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a88fb-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="a88fb-151"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a88fb-151"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a88fb-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="a88fb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88fb-153">**\_GETMARGINS em**</span><span class="sxs-lookup"><span data-stu-id="a88fb-153">**EM\_GETMARGINS**</span></span>](em-getmargins.md)
</dt> </dl>

 


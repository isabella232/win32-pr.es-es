---
title: Mensaje de EM_SETRECT (Winuser. h)
description: Establece el rectángulo de formato de un control de edición multilínea.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12b171478b0cb9d47496d20d4d1b6b1e8ddd29a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079309"
---
# <a name="em_setrect-message"></a><span data-ttu-id="f9ab2-104">\_Mensaje SETRECT em</span><span class="sxs-lookup"><span data-stu-id="f9ab2-104">EM\_SETRECT message</span></span>

<span data-ttu-id="f9ab2-105">Establece el [rectángulo de formato](about-edit-controls.md) de un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="f9ab2-106">El rectángulo de formato es el rectángulo de limitación en el que el control dibuja el texto.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="f9ab2-107">El rectángulo de limitación es independiente del tamaño de la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-107">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="f9ab2-108">Este mensaje solo lo procesan los controles de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-108">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="f9ab2-109">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9ab2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9ab2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9ab2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9ab2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9ab2-112">**Edición enriquecida 2,0 y versiones posteriores:** Indica si *lParam* especifica coordenadas absolutas o relativas.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-112">**Rich Edit 2.0 and later:** Indicates whether *lParam* specifies absolute or relative coordinates.</span></span> <span data-ttu-id="f9ab2-113">Un valor de cero indica coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-113">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="f9ab2-114">Un valor de 1 indica desplazamientos respecto al rectángulo de formato actual.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-114">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="f9ab2-115">(Los desplazamientos pueden ser positivos o negativos).</span><span class="sxs-lookup"><span data-stu-id="f9ab2-115">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="f9ab2-116">**Controles de edición y edición enriquecida 1,0:** Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-116">**Edit controls and Rich Edit 1.0:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f9ab2-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9ab2-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9ab2-118">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica las nuevas dimensiones del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-118">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="f9ab2-119">Si este parámetro es **null**, el rectángulo de formato se establece en sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-119">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9ab2-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9ab2-120">Return value</span></span>

<span data-ttu-id="f9ab2-121">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9ab2-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9ab2-122">Remarks</span></span>

<span data-ttu-id="f9ab2-123">Si se establece *lParam* en **null** , no se produce ningún efecto si se instala un dispositivo táctil o si **em \_ SETRECT** se envía desde un subproceso que tiene un enlace instalado (vea [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span><span class="sxs-lookup"><span data-stu-id="f9ab2-123">Setting *lParam* to **NULL** has no effect if a touch device is installed, or if **EM\_SETRECT** is sent from a thread that has a hook installed (see [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span></span> <span data-ttu-id="f9ab2-124">En estos casos, *lParam* debe contener un puntero válido a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f9ab2-124">In these cases, *lParam* should contain a valid pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span>

<span data-ttu-id="f9ab2-125">El **mensaje \_ SETRECT em** hace que se vuelva a dibujar el texto del control de edición.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-125">The **EM\_SETRECT** message causes the text of the edit control to be redrawn.</span></span> <span data-ttu-id="f9ab2-126">Para cambiar el tamaño del rectángulo de formato sin volver a dibujar el texto, use el mensaje [**\_ SETRECTNP em**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="f9ab2-126">To change the size of the formatting rectangle without redrawing the text, use the [**EM\_SETRECTNP**](em-setrectnp.md) message.</span></span>

<span data-ttu-id="f9ab2-127">Cuando se crea un control de edición por primera vez, el rectángulo de formato se establece en un tamaño predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-127">When an edit control is first created, the formatting rectangle is set to a default size.</span></span> <span data-ttu-id="f9ab2-128">Puede usar el mensaje **\_ SETRECT em** para que el rectángulo de formato sea más grande o más pequeño que la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-128">You can use the **EM\_SETRECT** message to make the formatting rectangle larger or smaller than the edit control window.</span></span>

<span data-ttu-id="f9ab2-129">Si el control de edición no tiene una barra de desplazamiento horizontal y el rectángulo de formato se establece en un valor mayor que la ventana de control de edición, las líneas de texto que superen el ancho de la ventana de control de edición (pero menor que el ancho del rectángulo de formato) se recortan en lugar de ajustarse.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-129">If the edit control does not have a horizontal scroll bar, and the formatting rectangle is set to be larger than the edit control window, lines of text exceeding the width of the edit control window (but smaller than the width of the formatting rectangle) are clipped instead of wrapped.</span></span>

<span data-ttu-id="f9ab2-130">Si el control de edición contiene un borde, el rectángulo de formato se reduce con el tamaño del borde.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-130">If the edit control contains a border, the formatting rectangle is reduced by the size of the border.</span></span> <span data-ttu-id="f9ab2-131">Si está ajustando el rectángulo devuelto por un mensaje [**\_ GETRECT em**](em-getrect.md) , debe quitar el tamaño del borde antes de usar el rectángulo con el **mensaje \_ SETRECT em** .</span><span class="sxs-lookup"><span data-stu-id="f9ab2-131">If you are adjusting the rectangle returned by an [**EM\_GETRECT**](em-getrect.md) message, you must remove the size of the border before using the rectangle with the **EM\_SETRECT** message.</span></span>

<span data-ttu-id="f9ab2-132">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-132">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="f9ab2-133">El rectángulo de formato no incluye la barra de selección, que es un área no marcada a la izquierda de cada párrafo.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-133">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="f9ab2-134">Cuando el usuario hace clic en la barra de selección, se selecciona la línea correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f9ab2-134">When the user clicks in the selection bar, the corresponding line is selected.</span></span> <span data-ttu-id="f9ab2-135">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f9ab2-135">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ab2-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9ab2-136">Requirements</span></span>



| <span data-ttu-id="f9ab2-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9ab2-137">Requirement</span></span> | <span data-ttu-id="f9ab2-138">Value</span><span class="sxs-lookup"><span data-stu-id="f9ab2-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ab2-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9ab2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f9ab2-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f9ab2-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f9ab2-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9ab2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f9ab2-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9ab2-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f9ab2-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9ab2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9ab2-144"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9ab2-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9ab2-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9ab2-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9ab2-146">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f9ab2-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f9ab2-147">**\_GETRECT em**</span><span class="sxs-lookup"><span data-stu-id="f9ab2-147">**EM\_GETRECT**</span></span>](em-getrect.md)
</dt> <dt>

[<span data-ttu-id="f9ab2-148">**\_SETRECTNP em**</span><span class="sxs-lookup"><span data-stu-id="f9ab2-148">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="f9ab2-149">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="f9ab2-149">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="f9ab2-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9ab2-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 


---
title: Mensaje de EM_GETSEL (Winuser. h)
description: Obtiene las posiciones de los caracteres inicial y final (en TCHARs) de la selección actual en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079312"
---
# <a name="em_getsel-message"></a><span data-ttu-id="099b4-105">\_Mensaje GETSEL em</span><span class="sxs-lookup"><span data-stu-id="099b4-105">EM\_GETSEL message</span></span>

<span data-ttu-id="099b4-106">Obtiene las posiciones de los caracteres inicial y final (en **TCHAR** s) de la selección actual en un control de edición.</span><span class="sxs-lookup"><span data-stu-id="099b4-106">Gets the starting and ending character positions (in **TCHAR** s) of the current selection in an edit control.</span></span> <span data-ttu-id="099b4-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="099b4-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="099b4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="099b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099b4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="099b4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="099b4-110">Un puntero a un valor **DWORD** que recibe la posición inicial de la selección.</span><span class="sxs-lookup"><span data-stu-id="099b4-110">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="099b4-111">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="099b4-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="099b4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="099b4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="099b4-113">Puntero a un valor **DWORD** que recibe la posición del primer carácter no seleccionado después del final de la selección.</span><span class="sxs-lookup"><span data-stu-id="099b4-113">A pointer to a **DWORD** value that receives the position of the first unselected character after the end of the selection.</span></span> <span data-ttu-id="099b4-114">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="099b4-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099b4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="099b4-115">Return value</span></span>

<span data-ttu-id="099b4-116">El valor devuelto es un valor basado en cero con la posición inicial de la selección en [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y la posición del primer **TCHAR** después del último **TCHAR** seleccionado en el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="099b4-116">The return value is a zero-based value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the position of the first **TCHAR** after the last selected **TCHAR** in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="099b4-117">Si alguno de estos valores supera 65.535, el valor devuelto es-1.</span><span class="sxs-lookup"><span data-stu-id="099b4-117">If either of these values exceeds 65,535, the return value is -1.</span></span>

<span data-ttu-id="099b4-118">Es mejor usar los valores devueltos en *wParam* e *lParam* porque son valores de 32 bits completos.</span><span class="sxs-lookup"><span data-stu-id="099b4-118">It is better to use the values returned in *wParam* and *lParam* because they are full 32-bit values.</span></span>

## <a name="remarks"></a><span data-ttu-id="099b4-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="099b4-119">Remarks</span></span>

<span data-ttu-id="099b4-120">Si no hay ninguna selección, los valores inicial y final son la posición del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="099b4-120">If there is no selection, the starting and ending values are both the position of the caret.</span></span>

<span data-ttu-id="099b4-121">**Controles Rich Edit:** También puede usar el mensaje [**\_ EXGETSEL em**](em-exgetsel.md) para recuperar la misma información.</span><span class="sxs-lookup"><span data-stu-id="099b4-121">**Rich edit controls:** You can also use the [**EM\_EXGETSEL**](em-exgetsel.md) message to retrieve the same information.</span></span> <span data-ttu-id="099b4-122">**Em \_ EXGETSEL** también devuelve las posiciones de caracteres inicial y final como valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="099b4-122">**EM\_EXGETSEL** also returns starting and ending character positions as 32-bit values.</span></span>

<span data-ttu-id="099b4-123">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="099b4-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="099b4-124">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="099b4-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="099b4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="099b4-125">Requirements</span></span>



| <span data-ttu-id="099b4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="099b4-126">Requirement</span></span> | <span data-ttu-id="099b4-127">Value</span><span class="sxs-lookup"><span data-stu-id="099b4-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="099b4-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="099b4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="099b4-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="099b4-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="099b4-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="099b4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="099b4-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="099b4-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="099b4-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="099b4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="099b4-133"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="099b4-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="099b4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="099b4-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="099b4-135">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="099b4-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="099b4-136">**\_EXGETSEL em**</span><span class="sxs-lookup"><span data-stu-id="099b4-136">**EM\_EXGETSEL**</span></span>](em-exgetsel.md)
</dt> <dt>

[<span data-ttu-id="099b4-137">**\_SETSEL em**</span><span class="sxs-lookup"><span data-stu-id="099b4-137">**EM\_SETSEL**</span></span>](em-setsel.md)
</dt> </dl>

 


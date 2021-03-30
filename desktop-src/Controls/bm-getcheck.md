---
title: Mensaje de BM_GETCHECK (Winuser. h)
description: Obtiene el estado de activación de un botón de radio o casilla. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetCheck.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150982"
---
# <a name="bm_getcheck-message"></a><span data-ttu-id="26a2b-105">\_Mensaje GETCHECK de BM</span><span class="sxs-lookup"><span data-stu-id="26a2b-105">BM\_GETCHECK message</span></span>

<span data-ttu-id="26a2b-106">Obtiene el estado de activación de un botón de radio o casilla.</span><span class="sxs-lookup"><span data-stu-id="26a2b-106">Gets the check state of a radio button or check box.</span></span> <span data-ttu-id="26a2b-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) .</span><span class="sxs-lookup"><span data-stu-id="26a2b-107">You can send this message explicitly or use the [**Button\_GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="26a2b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26a2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26a2b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26a2b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26a2b-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="26a2b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="26a2b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26a2b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26a2b-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="26a2b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26a2b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26a2b-113">Return value</span></span>

<span data-ttu-id="26a2b-114">El valor devuelto de un botón creado con el estilo [**BS \_ autocheckbox**](button-styles.md), [**BS \_ autoradiobutton**](button-styles.md), [**BS \_ AUTO3STATE**](button-styles.md), la [**\_ casilla**](button-styles.md)BS, el [**\_ RADIOBUTTON de BS**](button-styles.md)o [**BS \_ 3STATE**](button-styles.md) puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="26a2b-114">The return value from a button created with the [**BS\_AUTOCHECKBOX**](button-styles.md), [**BS\_AUTORADIOBUTTON**](button-styles.md), [**BS\_AUTO3STATE**](button-styles.md), [**BS\_CHECKBOX**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), or [**BS\_3STATE**](button-styles.md) style can be one of the following.</span></span>



| <span data-ttu-id="26a2b-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="26a2b-115">Return code</span></span>                                                                                       | <span data-ttu-id="26a2b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="26a2b-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26a2b-117"><dt>**BST \_ comprobado**</dt></span><span class="sxs-lookup"><span data-stu-id="26a2b-117"><dt>**BST\_CHECKED**</dt></span></span> </dl>       | <span data-ttu-id="26a2b-118">Está activado.</span><span class="sxs-lookup"><span data-stu-id="26a2b-118">Button is checked.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="26a2b-119"><dt>**BST \_ indeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="26a2b-119"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="26a2b-120">El botón está atenuado, lo que indica un estado indeterminado (solo se aplica si el botón tiene el estilo [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="26a2b-120">Button is grayed, indicating an indeterminate state (applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style).</span></span><br/> |
| <dl> <span data-ttu-id="26a2b-121"><dt>**BST \_ DESactivado**</dt></span><span class="sxs-lookup"><span data-stu-id="26a2b-121"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>     | <span data-ttu-id="26a2b-122">El botón está desactivado</span><span class="sxs-lookup"><span data-stu-id="26a2b-122">Button is cleared</span></span><br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="26a2b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26a2b-123">Remarks</span></span>

<span data-ttu-id="26a2b-124">Si el botón tiene un estilo distinto de los enumerados, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="26a2b-124">If the button has a style other than those listed, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="26a2b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26a2b-125">Requirements</span></span>



| <span data-ttu-id="26a2b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="26a2b-126">Requirement</span></span> | <span data-ttu-id="26a2b-127">Value</span><span class="sxs-lookup"><span data-stu-id="26a2b-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26a2b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26a2b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="26a2b-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="26a2b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="26a2b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26a2b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="26a2b-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="26a2b-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="26a2b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26a2b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="26a2b-133"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26a2b-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26a2b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="26a2b-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="26a2b-135">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="26a2b-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="26a2b-136">**\_GETSTATE BM**</span><span class="sxs-lookup"><span data-stu-id="26a2b-136">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="26a2b-137">**\_SETCHECK BM**</span><span class="sxs-lookup"><span data-stu-id="26a2b-137">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 






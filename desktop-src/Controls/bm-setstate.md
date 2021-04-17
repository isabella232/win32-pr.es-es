---
title: Mensaje de BM_SETSTATE (Winuser. h)
description: Establece el estado de resaltado de un botón. El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera insertado. Puede enviar este mensaje explícitamente o usar la macro de botón \_ SetState.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656499"
---
# <a name="bm_setstate-message"></a><span data-ttu-id="40911-106">Mensaje de BM \_ SETSTATE</span><span class="sxs-lookup"><span data-stu-id="40911-106">BM\_SETSTATE message</span></span>

<span data-ttu-id="40911-107">Establece el estado de resaltado de un botón.</span><span class="sxs-lookup"><span data-stu-id="40911-107">Sets the highlight state of a button.</span></span> <span data-ttu-id="40911-108">El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera insertado.</span><span class="sxs-lookup"><span data-stu-id="40911-108">The highlight state indicates whether the button is highlighted as if the user had pushed it.</span></span> <span data-ttu-id="40911-109">Puede enviar este mensaje explícitamente o usar la macro de [**botón \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .</span><span class="sxs-lookup"><span data-stu-id="40911-109">You can send this message explicitly or use the [**Button\_SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="40911-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40911-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40911-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40911-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40911-112">Un **booleano** que especifica si el botón está resaltado.</span><span class="sxs-lookup"><span data-stu-id="40911-112">A **BOOL** that specifies whether the button is highlighted.</span></span> <span data-ttu-id="40911-113">Un valor de **true** resalta el botón.</span><span class="sxs-lookup"><span data-stu-id="40911-113">A value of **TRUE** highlights the button.</span></span> <span data-ttu-id="40911-114">Un valor **false** quita cualquier resaltado.</span><span class="sxs-lookup"><span data-stu-id="40911-114">A value of **FALSE** removes any highlighting.</span></span>

</dd> <dt>

<span data-ttu-id="40911-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40911-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40911-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="40911-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40911-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40911-117">Return value</span></span>

<span data-ttu-id="40911-118">Este mensaje siempre devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="40911-118">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="40911-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40911-119">Remarks</span></span>

<span data-ttu-id="40911-120">El resaltado solo afecta a la apariencia de un botón.</span><span class="sxs-lookup"><span data-stu-id="40911-120">Highlighting affects only the appearance of a button.</span></span> <span data-ttu-id="40911-121">No tiene ningún efecto en el estado de activación de un botón de radio o casilla.</span><span class="sxs-lookup"><span data-stu-id="40911-121">It has no effect on the check state of a radio button or check box.</span></span>

<span data-ttu-id="40911-122">Un botón se resalta automáticamente cuando el usuario coloca el cursor sobre él y presiona y mantiene presionado el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="40911-122">A button is automatically highlighted when the user positions the cursor over it and presses and holds the left mouse button.</span></span> <span data-ttu-id="40911-123">El resaltado se quita cuando el usuario suelta el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="40911-123">The highlighting is removed when the user releases the mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="40911-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40911-124">Requirements</span></span>



| <span data-ttu-id="40911-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="40911-125">Requirement</span></span> | <span data-ttu-id="40911-126">Value</span><span class="sxs-lookup"><span data-stu-id="40911-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40911-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40911-127">Minimum supported client</span></span><br/> | <span data-ttu-id="40911-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="40911-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="40911-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40911-129">Minimum supported server</span></span><br/> | <span data-ttu-id="40911-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="40911-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="40911-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40911-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="40911-132"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40911-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40911-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="40911-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="40911-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="40911-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="40911-135">**\_GETSTATE BM**</span><span class="sxs-lookup"><span data-stu-id="40911-135">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="40911-136">**\_SETCHECK BM**</span><span class="sxs-lookup"><span data-stu-id="40911-136">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 






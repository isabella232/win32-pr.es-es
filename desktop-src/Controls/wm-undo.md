---
title: Mensaje de WM_UNDO (Winuser. h)
description: Una aplicación envía un \_ mensaje de deshacer de WM a un control de edición para deshacer la última operación. Cuando este mensaje se envía a un control de edición, se restaura el texto previamente eliminado o se elimina el texto agregado previamente.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- WM_UNDO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491417"
---
# <a name="wm_undo-message"></a><span data-ttu-id="976eb-105">\_Mensaje de deshacer de WM</span><span class="sxs-lookup"><span data-stu-id="976eb-105">WM\_UNDO message</span></span>

<span data-ttu-id="976eb-106">Una aplicación envía un mensaje de **\_ Deshacer de WM** a un control de edición para deshacer la última operación.</span><span class="sxs-lookup"><span data-stu-id="976eb-106">An application sends a **WM\_UNDO** message to an edit control to undo the last operation.</span></span> <span data-ttu-id="976eb-107">Cuando este mensaje se envía a un control de edición, se restaura el texto previamente eliminado o se elimina el texto agregado previamente.</span><span class="sxs-lookup"><span data-stu-id="976eb-107">When this message is sent to an edit control, the previously deleted text is restored or the previously added text is deleted.</span></span>

## <a name="parameters"></a><span data-ttu-id="976eb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="976eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="976eb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="976eb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="976eb-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="976eb-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="976eb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="976eb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="976eb-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="976eb-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="976eb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="976eb-113">Return value</span></span>

<span data-ttu-id="976eb-114">Si el mensaje se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="976eb-114">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="976eb-115">Si se produce un error en el mensaje, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="976eb-115">If the message fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="976eb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="976eb-116">Remarks</span></span>

<span data-ttu-id="976eb-117">**Edición enriquecida:** Se recomienda el uso de la [**\_ función**](em-undo.md) deshacer en lugar de **WM \_ Undo**.</span><span class="sxs-lookup"><span data-stu-id="976eb-117">**Rich Edit:** It is recommended that [**EM\_UNDO**](em-undo.md) be used instead of **WM\_UNDO**.</span></span>

## <a name="requirements"></a><span data-ttu-id="976eb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="976eb-118">Requirements</span></span>



| <span data-ttu-id="976eb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="976eb-119">Requirement</span></span> | <span data-ttu-id="976eb-120">Value</span><span class="sxs-lookup"><span data-stu-id="976eb-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="976eb-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="976eb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="976eb-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="976eb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="976eb-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="976eb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="976eb-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="976eb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="976eb-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="976eb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="976eb-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="976eb-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="976eb-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="976eb-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="976eb-128">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="976eb-128">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="976eb-129">**\_borrado de WM**</span><span class="sxs-lookup"><span data-stu-id="976eb-129">**WM\_CLEAR**</span></span>](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[<span data-ttu-id="976eb-130">**copia de WM \_**</span><span class="sxs-lookup"><span data-stu-id="976eb-130">**WM\_COPY**</span></span>](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[<span data-ttu-id="976eb-131">**cortar de WM \_**</span><span class="sxs-lookup"><span data-stu-id="976eb-131">**WM\_CUT**</span></span>](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[<span data-ttu-id="976eb-132">**pegar de WM \_**</span><span class="sxs-lookup"><span data-stu-id="976eb-132">**WM\_PASTE**</span></span>](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 


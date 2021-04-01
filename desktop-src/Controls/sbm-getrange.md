---
title: Mensaje de SBM_GETRANGE (Winuser. h)
description: El \_ mensaje SBM GETRANGE se envía para recuperar los valores de posición mínimo y máximo del control de barra de desplazamiento.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- SBM_GETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996804"
---
# <a name="sbm_getrange-message"></a><span data-ttu-id="c5e1a-104">\_Mensaje GETRANGE SBM</span><span class="sxs-lookup"><span data-stu-id="c5e1a-104">SBM\_GETRANGE message</span></span>

<span data-ttu-id="c5e1a-105">El mensaje **SBM \_ GETRANGE** se envía para recuperar los valores de posición mínimo y máximo del control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="c5e1a-105">The **SBM\_GETRANGE** message is sent to retrieve the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="c5e1a-106">Las aplicaciones no deben enviar este mensaje directamente.</span><span class="sxs-lookup"><span data-stu-id="c5e1a-106">Applications should not send this message directly.</span></span> <span data-ttu-id="c5e1a-107">En su lugar, deben utilizar la función [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="c5e1a-107">Instead, they should use the [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) function.</span></span> <span data-ttu-id="c5e1a-108">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c5e1a-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="c5e1a-109">Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **GetScrollRange** funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="c5e1a-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5e1a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5e1a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e1a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5e1a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5e1a-112">Puntero a una variable que recibe la posición de desplazamiento mínima.</span><span class="sxs-lookup"><span data-stu-id="c5e1a-112">Pointer to a variable that receives the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="c5e1a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5e1a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5e1a-114">Puntero a una variable que recibe la posición de desplazamiento máxima.</span><span class="sxs-lookup"><span data-stu-id="c5e1a-114">Pointer to a variable that receives the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e1a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5e1a-115">Return value</span></span>

<span data-ttu-id="c5e1a-116">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c5e1a-116">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e1a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5e1a-117">Requirements</span></span>



| <span data-ttu-id="c5e1a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e1a-118">Requirement</span></span> | <span data-ttu-id="c5e1a-119">Value</span><span class="sxs-lookup"><span data-stu-id="c5e1a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e1a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5e1a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e1a-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c5e1a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c5e1a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5e1a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e1a-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5e1a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5e1a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5e1a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5e1a-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5e1a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5e1a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5e1a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5e1a-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c5e1a-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5e1a-128">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="c5e1a-128">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="c5e1a-129">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="c5e1a-129">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="c5e1a-130">**SBM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="c5e1a-130">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="c5e1a-131">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="c5e1a-131">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 


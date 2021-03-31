---
title: Mensaje de SBM_GETPOS (Winuser. h)
description: El \_ mensaje SBM GETPOS se envía para recuperar la posición actual del cuadro de desplazamiento de un control de barra de desplazamiento.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- SBM_GETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996805"
---
# <a name="sbm_getpos-message"></a><span data-ttu-id="53650-104">\_Mensaje GETPOS SBM</span><span class="sxs-lookup"><span data-stu-id="53650-104">SBM\_GETPOS message</span></span>

<span data-ttu-id="53650-105">El mensaje **SBM \_ GETPOS** se envía para recuperar la posición actual del cuadro de desplazamiento de un control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="53650-105">The **SBM\_GETPOS** message is sent to retrieve the current position of the scroll box of a scroll bar control.</span></span> <span data-ttu-id="53650-106">La posición actual es un valor relativo que depende del intervalo de desplazamiento actual.</span><span class="sxs-lookup"><span data-stu-id="53650-106">The current position is a relative value that depends on the current scrolling range.</span></span> <span data-ttu-id="53650-107">Por ejemplo, si el intervalo de desplazamiento es de 0 a 100 y el cuadro de desplazamiento está en el centro de la barra, la posición actual es 50.</span><span class="sxs-lookup"><span data-stu-id="53650-107">For example, if the scrolling range is 0 through 100 and the scroll box is in the middle of the bar, the current position is 50.</span></span>

<span data-ttu-id="53650-108">Las aplicaciones no deben enviar este mensaje directamente.</span><span class="sxs-lookup"><span data-stu-id="53650-108">Applications should not send this message directly.</span></span> <span data-ttu-id="53650-109">En su lugar, deben utilizar la función [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="53650-109">Instead, they should use the [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) function.</span></span> <span data-ttu-id="53650-110">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="53650-110">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="53650-111">Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **GetScrollPos** funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="53650-111">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollPos** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="53650-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53650-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53650-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53650-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53650-114">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="53650-114">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="53650-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53650-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53650-116">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="53650-116">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53650-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53650-117">Return value</span></span>

<span data-ttu-id="53650-118">El valor devuelto es la posición actual del cuadro de desplazamiento en la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="53650-118">The return value is the current position of the scroll box in the scroll bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="53650-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53650-119">Requirements</span></span>



| <span data-ttu-id="53650-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="53650-120">Requirement</span></span> | <span data-ttu-id="53650-121">Value</span><span class="sxs-lookup"><span data-stu-id="53650-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53650-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53650-122">Minimum supported client</span></span><br/> | <span data-ttu-id="53650-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="53650-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53650-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53650-124">Minimum supported server</span></span><br/> | <span data-ttu-id="53650-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="53650-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53650-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53650-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="53650-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53650-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53650-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="53650-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="53650-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="53650-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="53650-130">**SBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="53650-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="53650-131">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="53650-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="53650-132">**SBM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="53650-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="53650-133">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="53650-133">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 


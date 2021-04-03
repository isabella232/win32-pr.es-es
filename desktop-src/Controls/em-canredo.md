---
title: Mensaje EM_CANREDO (RichEdit. h)
description: Determina si hay alguna acción en la cola de rehacer del control.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- EM_CANREDO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905406"
---
# <a name="em_canredo-message"></a><span data-ttu-id="c00fa-104">\_Mensaje CANREDO em</span><span class="sxs-lookup"><span data-stu-id="c00fa-104">EM\_CANREDO message</span></span>

<span data-ttu-id="c00fa-105">Determina si hay alguna acción en la cola de rehacer del control.</span><span class="sxs-lookup"><span data-stu-id="c00fa-105">Determines whether there are any actions in the control redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="c00fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c00fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c00fa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c00fa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c00fa-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c00fa-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c00fa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c00fa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c00fa-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c00fa-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c00fa-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c00fa-111">Return value</span></span>

<span data-ttu-id="c00fa-112">Si hay acciones en la cola de rehacer de control, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c00fa-112">If there are actions in the control redo queue, the return value is a nonzero value.</span></span>

<span data-ttu-id="c00fa-113">Si la cola de puesta al día está vacía, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="c00fa-113">If the redo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c00fa-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c00fa-114">Remarks</span></span>

<span data-ttu-id="c00fa-115">Para rehacer la operación de deshacer más reciente, envíe el mensaje de [**\_ rehacer em**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="c00fa-115">To redo the most recent undo operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c00fa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c00fa-116">Requirements</span></span>



| <span data-ttu-id="c00fa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c00fa-117">Requirement</span></span> | <span data-ttu-id="c00fa-118">Value</span><span class="sxs-lookup"><span data-stu-id="c00fa-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c00fa-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c00fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c00fa-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c00fa-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c00fa-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c00fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c00fa-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c00fa-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c00fa-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c00fa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c00fa-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c00fa-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c00fa-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c00fa-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c00fa-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c00fa-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c00fa-127">**\_GETREDONAME em**</span><span class="sxs-lookup"><span data-stu-id="c00fa-127">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="c00fa-128">**\_GETUNDONAME em**</span><span class="sxs-lookup"><span data-stu-id="c00fa-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="c00fa-129">**rehacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="c00fa-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="c00fa-130">**deshacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="c00fa-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 






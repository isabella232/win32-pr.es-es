---
title: Mensaje de EM_NOSETFOCUS (commctrl. h)
description: Impide que un control de edición de una sola línea reciba el foco de teclado. Puede enviar este mensaje explícitamente o mediante la macro Edit \_ NoSetFocus.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- EM_NOSETFOCUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150760"
---
# <a name="em_nosetfocus-message"></a><span data-ttu-id="90d46-105">\_Mensaje NOSETFOCUS em</span><span class="sxs-lookup"><span data-stu-id="90d46-105">EM\_NOSETFOCUS message</span></span>

<span data-ttu-id="90d46-106">\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</span><span class="sxs-lookup"><span data-stu-id="90d46-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="90d46-107">Es posible que este mensaje no se admita en versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="90d46-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="90d46-108">Impide que un control de edición de una sola línea reciba el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="90d46-108">Prevents a single-line edit control from receiving keyboard focus.</span></span> <span data-ttu-id="90d46-109">Puede enviar este mensaje explícitamente o mediante la macro [**Edit \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) .</span><span class="sxs-lookup"><span data-stu-id="90d46-109">You can send this message explicitly or by using the [**Edit\_NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="90d46-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90d46-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90d46-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90d46-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90d46-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="90d46-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="90d46-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90d46-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90d46-114">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="90d46-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90d46-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90d46-115">Return value</span></span>

<span data-ttu-id="90d46-116">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="90d46-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="90d46-117">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="90d46-117">Security Considerations</span></span>

<span data-ttu-id="90d46-118">El uso de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="90d46-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="90d46-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90d46-119">Remarks</span></span>

<span data-ttu-id="90d46-120">Este mensaje se omite si el control de edición no es un control de edición de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="90d46-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="90d46-121">Después de enviar este mensaje, el efecto es permanente.</span><span class="sxs-lookup"><span data-stu-id="90d46-121">After this message is sent, the effect is permanent.</span></span>

## <a name="requirements"></a><span data-ttu-id="90d46-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90d46-122">Requirements</span></span>



| <span data-ttu-id="90d46-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="90d46-123">Requirement</span></span> | <span data-ttu-id="90d46-124">Value</span><span class="sxs-lookup"><span data-stu-id="90d46-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90d46-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90d46-125">Minimum supported client</span></span><br/> | <span data-ttu-id="90d46-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="90d46-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90d46-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90d46-127">Minimum supported server</span></span><br/> | <span data-ttu-id="90d46-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="90d46-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90d46-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90d46-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="90d46-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90d46-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90d46-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="90d46-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="90d46-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="90d46-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="90d46-133">**Editar \_ NoSetFocus**</span><span class="sxs-lookup"><span data-stu-id="90d46-133">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[<span data-ttu-id="90d46-134">**\_TAKEFOCUS em**</span><span class="sxs-lookup"><span data-stu-id="90d46-134">**EM\_TAKEFOCUS**</span></span>](em-takefocus.md)
</dt> </dl>

 

 






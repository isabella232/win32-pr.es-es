---
title: Mensaje de EM_TAKEFOCUS (commctrl. h)
description: Fuerza un control de edición de una sola línea para recibir el foco de teclado. Puede enviar este mensaje explícitamente o mediante la macro Edit \_ TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- EM_TAKEFOCUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490720"
---
# <a name="em_takefocus-message"></a><span data-ttu-id="7df85-105">\_Mensaje TAKEFOCUS em</span><span class="sxs-lookup"><span data-stu-id="7df85-105">EM\_TAKEFOCUS message</span></span>

<span data-ttu-id="7df85-106">\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</span><span class="sxs-lookup"><span data-stu-id="7df85-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="7df85-107">Es posible que este mensaje no se admita en versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7df85-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="7df85-108">Fuerza un control de edición de una sola línea para recibir el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="7df85-108">Forces a single-line edit control to receive keyboard focus.</span></span> <span data-ttu-id="7df85-109">Puede enviar este mensaje explícitamente o mediante la macro [**Edit \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .</span><span class="sxs-lookup"><span data-stu-id="7df85-109">You can send this message explicitly or by using the [**Edit\_TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7df85-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7df85-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df85-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7df85-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7df85-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7df85-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7df85-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7df85-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7df85-114">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7df85-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df85-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7df85-115">Return value</span></span>

<span data-ttu-id="7df85-116">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="7df85-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="7df85-117">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="7df85-117">Security Considerations</span></span>

<span data-ttu-id="7df85-118">El uso de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="7df85-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df85-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7df85-119">Remarks</span></span>

<span data-ttu-id="7df85-120">Este mensaje se omite si el control de edición no es un control de edición de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="7df85-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="7df85-121">Si el control de edición ha recibido previamente un mensaje [**\_ NOSETFOCUS em**](em-nosetfocus.md) , parecerá que el control de edición tiene el foco sin tenerlo realmente; de lo contrario, el control de edición recibirá el foco.</span><span class="sxs-lookup"><span data-stu-id="7df85-121">If the edit control previously received an [**EM\_NOSETFOCUS**](em-nosetfocus.md) message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df85-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df85-122">Requirements</span></span>



| <span data-ttu-id="7df85-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df85-123">Requirement</span></span> | <span data-ttu-id="7df85-124">Value</span><span class="sxs-lookup"><span data-stu-id="7df85-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7df85-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7df85-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7df85-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7df85-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7df85-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7df85-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7df85-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7df85-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7df85-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7df85-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7df85-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7df85-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df85-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7df85-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="7df85-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7df85-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7df85-133">**Editar \_ TakeFocus**</span><span class="sxs-lookup"><span data-stu-id="7df85-133">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[<span data-ttu-id="7df85-134">**\_NOSETFOCUS em**</span><span class="sxs-lookup"><span data-stu-id="7df85-134">**EM\_NOSETFOCUS**</span></span>](em-nosetfocus.md)
</dt> </dl>

 

 






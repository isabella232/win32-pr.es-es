---
title: Mensaje EM_SETEVENTMASK (RichEdit. h)
description: Establece la máscara de eventos para un control Rich Edit. La máscara de eventos especifica los códigos de notificación que el control envía a su ventana primaria.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492460"
---
# <a name="em_seteventmask-message"></a><span data-ttu-id="bdaad-105">\_Mensaje em SETEVENTMASK</span><span class="sxs-lookup"><span data-stu-id="bdaad-105">EM\_SETEVENTMASK message</span></span>

<span data-ttu-id="bdaad-106">Establece la máscara de eventos para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bdaad-106">Sets the event mask for a rich edit control.</span></span> <span data-ttu-id="bdaad-107">La máscara de eventos especifica los códigos de notificación que el control envía a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="bdaad-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdaad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdaad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdaad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdaad-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdaad-110">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bdaad-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bdaad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdaad-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdaad-112">Nueva máscara de eventos para el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bdaad-112">New event mask for the rich edit control.</span></span> <span data-ttu-id="bdaad-113">Para obtener una lista de máscaras de eventos, vea [**marcas de máscara de eventos de control de edición enriquecida**](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bdaad-113">For a list of event masks, see [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdaad-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdaad-114">Return value</span></span>

<span data-ttu-id="bdaad-115">Este mensaje devuelve la máscara de eventos anterior.</span><span class="sxs-lookup"><span data-stu-id="bdaad-115">This message returns the previous event mask.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdaad-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdaad-116">Remarks</span></span>

<span data-ttu-id="bdaad-117">La máscara de eventos predeterminada (antes de que se establezca) es ENM \_ None.</span><span class="sxs-lookup"><span data-stu-id="bdaad-117">The default event mask (before any is set) is ENM\_NONE.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdaad-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdaad-118">Requirements</span></span>



| <span data-ttu-id="bdaad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdaad-119">Requirement</span></span> | <span data-ttu-id="bdaad-120">Value</span><span class="sxs-lookup"><span data-stu-id="bdaad-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdaad-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdaad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bdaad-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bdaad-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdaad-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdaad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bdaad-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bdaad-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdaad-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdaad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdaad-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdaad-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdaad-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdaad-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="bdaad-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="bdaad-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bdaad-129">**\_GETEVENTMASK (EM**</span><span class="sxs-lookup"><span data-stu-id="bdaad-129">**EM\_GETEVENTMASK**</span></span>](em-geteventmask.md)
</dt> <dt>

[<span data-ttu-id="bdaad-130">**Marcas de máscara de eventos de control de edición enriquecida**</span><span class="sxs-lookup"><span data-stu-id="bdaad-130">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 






---
title: Mensaje EM_GETEVENTMASK (RichEdit. h)
description: Recupera la máscara de eventos para un control Rich Edit. La máscara de eventos especifica los códigos de notificación que el control envía a su ventana primaria.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- EM_GETEVENTMASK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996753"
---
# <a name="em_geteventmask-message"></a><span data-ttu-id="8b9b5-105">\_Mensaje GETEVENTMASK (EM</span><span class="sxs-lookup"><span data-stu-id="8b9b5-105">EM\_GETEVENTMASK message</span></span>

<span data-ttu-id="8b9b5-106">Recupera la máscara de eventos para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-106">Retrieves the event mask for a rich edit control.</span></span> <span data-ttu-id="8b9b5-107">La máscara de eventos especifica los códigos de notificación que el control envía a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b9b5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b9b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b9b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b9b5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b9b5-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8b9b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b9b5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b9b5-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b9b5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b9b5-113">Return value</span></span>

<span data-ttu-id="8b9b5-114">Este mensaje devuelve la máscara de eventos para el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-114">This message returns the event mask for the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b9b5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b9b5-115">Requirements</span></span>



| <span data-ttu-id="8b9b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b9b5-116">Requirement</span></span> | <span data-ttu-id="8b9b5-117">Value</span><span class="sxs-lookup"><span data-stu-id="8b9b5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9b5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b9b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8b9b5-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8b9b5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b9b5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b9b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8b9b5-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b9b5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b9b5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b9b5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b9b5-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b9b5-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b9b5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b9b5-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b9b5-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8b9b5-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8b9b5-126">**una \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="8b9b5-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="8b9b5-127">**Marcas de máscara de eventos de control de edición enriquecida**</span><span class="sxs-lookup"><span data-stu-id="8b9b5-127">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 






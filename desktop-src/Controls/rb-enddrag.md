---
title: Mensaje de RB_ENDDRAG (commctrl. h)
description: Finaliza la operación de arrastrar y colocar del control rebar. Este mensaje no hace que \_ se envíe una notificación de ENDDRAG de RBN.
ms.assetid: 4991dda6-32ea-4d3e-9d39-17c2b6995f09
keywords:
- RB_ENDDRAG controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6f201471b6f260555aacb9d89c1363492ed6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996725"
---
# <a name="rb_enddrag-message"></a><span data-ttu-id="cefb0-105">Mensaje de ENDDRAG de RB \_</span><span class="sxs-lookup"><span data-stu-id="cefb0-105">RB\_ENDDRAG message</span></span>

<span data-ttu-id="cefb0-106">Finaliza la operación de arrastrar y colocar del control rebar.</span><span class="sxs-lookup"><span data-stu-id="cefb0-106">Terminates the rebar control's drag-and-drop operation.</span></span> <span data-ttu-id="cefb0-107">Este mensaje no hace que se envíe una notificación de [ \_ ENDDRAG de RBN](rbn-enddrag.md) .</span><span class="sxs-lookup"><span data-stu-id="cefb0-107">This message does not cause an [RBN\_ENDDRAG](rbn-enddrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="cefb0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cefb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cefb0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cefb0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cefb0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cefb0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cefb0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cefb0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cefb0-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cefb0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cefb0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cefb0-113">Return value</span></span>

<span data-ttu-id="cefb0-114">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="cefb0-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cefb0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cefb0-115">Requirements</span></span>



| <span data-ttu-id="cefb0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cefb0-116">Requirement</span></span> | <span data-ttu-id="cefb0-117">Value</span><span class="sxs-lookup"><span data-stu-id="cefb0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cefb0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cefb0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cefb0-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cefb0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cefb0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cefb0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cefb0-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cefb0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cefb0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cefb0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cefb0-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cefb0-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cefb0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cefb0-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="cefb0-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cefb0-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cefb0-126">**\_BEGINDRAG RB**</span><span class="sxs-lookup"><span data-stu-id="cefb0-126">**RB\_BEGINDRAG**</span></span>](rb-begindrag.md)
</dt> <dt>

[<span data-ttu-id="cefb0-127">**\_DRAGMOVE RB**</span><span class="sxs-lookup"><span data-stu-id="cefb0-127">**RB\_DRAGMOVE**</span></span>](rb-dragmove.md)
</dt> </dl>

 

 






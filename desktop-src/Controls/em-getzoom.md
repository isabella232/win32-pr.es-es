---
title: Mensaje EM_GETZOOM (RichEdit. h)
description: Obtiene la relación de zoom actual. La ración de zoom siempre está entre 1/64 y 64. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- EM_GETZOOM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801370"
---
# <a name="em_getzoom-message"></a><span data-ttu-id="8a83a-106">\_Mensaje GETZOOM em</span><span class="sxs-lookup"><span data-stu-id="8a83a-106">EM\_GETZOOM message</span></span>

<span data-ttu-id="8a83a-107">Obtiene la relación de zoom actual para un control de edición de varias líneas o un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8a83a-107">Gets the current zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="8a83a-108">La ración de zoom siempre está entre 1/64 y 64.</span><span class="sxs-lookup"><span data-stu-id="8a83a-108">The zoom ration is always between 1/64 and 64.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a83a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a83a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a83a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a83a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a83a-111">Recibe el numerador de la relación de zoom.</span><span class="sxs-lookup"><span data-stu-id="8a83a-111">Receives the numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="8a83a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a83a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a83a-113">Recibe el denominador de la relación de zoom.</span><span class="sxs-lookup"><span data-stu-id="8a83a-113">Receives the denominator of the zoom ratio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a83a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a83a-114">Return value</span></span>

<span data-ttu-id="8a83a-115">El mensaje devuelve **true** si se procesa el mensaje, que será si *wParam* e *lParam* no son **null**.</span><span class="sxs-lookup"><span data-stu-id="8a83a-115">The message returns **TRUE** if message is processed, which it will be if both *wParam* and *lParam* are not **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a83a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a83a-116">Remarks</span></span>

<span data-ttu-id="8a83a-117">**Editar:** Compatible con Windows 10 1809 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8a83a-117">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="8a83a-118">El control de edición debe tener el conjunto de estilo extendido **es \_ ex \_** para el que este mensaje tiene un efecto, vea [Edit control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="8a83a-118">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="8a83a-119">Para obtener información sobre el control de edición, vea [controles de edición](edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8a83a-119">For information about the edit control, see [Edit Controls](edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a83a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a83a-120">Requirements</span></span>



| <span data-ttu-id="8a83a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a83a-121">Requirement</span></span> | <span data-ttu-id="8a83a-122">Value</span><span class="sxs-lookup"><span data-stu-id="8a83a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a83a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a83a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8a83a-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8a83a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a83a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a83a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8a83a-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a83a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a83a-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8a83a-127">Redistributable</span></span><br/>          | <span data-ttu-id="8a83a-128">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="8a83a-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="8a83a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a83a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a83a-130"><dt>RichEdit. h/commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a83a-130"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a83a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a83a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a83a-132">**\_SETZOOM em**</span><span class="sxs-lookup"><span data-stu-id="8a83a-132">**EM\_SETZOOM**</span></span>](em-setzoom.md)
</dt> </dl>

 

 






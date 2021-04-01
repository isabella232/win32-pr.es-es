---
title: Mensaje de TVM_SETINDENT (commctrl. h)
description: Establece el ancho de la sangría de un control de vista de árbol y vuelve a dibujar el control para reflejar el nuevo ancho. Puede enviar este mensaje explícitamente o mediante la \_ macro SetIndent de TreeView.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150452"
---
# <a name="tvm_setindent-message"></a><span data-ttu-id="aebac-105">\_Mensaje de SETINDENT TVM</span><span class="sxs-lookup"><span data-stu-id="aebac-105">TVM\_SETINDENT message</span></span>

<span data-ttu-id="aebac-106">Establece el ancho de la sangría de un control de vista de árbol y vuelve a dibujar el control para reflejar el nuevo ancho.</span><span class="sxs-lookup"><span data-stu-id="aebac-106">Sets the width of indentation for a tree-view control and redraws the control to reflect the new width.</span></span> <span data-ttu-id="aebac-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetIndent de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) .</span><span class="sxs-lookup"><span data-stu-id="aebac-107">You can send this message explicitly or by using the [**TreeView\_SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="aebac-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aebac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aebac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aebac-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aebac-110">Ancho, en píxeles, de la sangría.</span><span class="sxs-lookup"><span data-stu-id="aebac-110">Width, in pixels, of the indentation.</span></span> <span data-ttu-id="aebac-111">Si este parámetro es menor que el ancho mínimo definido por el sistema, el nuevo ancho se establece en el mínimo definido por el sistema.</span><span class="sxs-lookup"><span data-stu-id="aebac-111">If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum.</span></span>

</dd> <dt>

<span data-ttu-id="aebac-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aebac-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="aebac-113">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="aebac-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aebac-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aebac-114">Return value</span></span>

<span data-ttu-id="aebac-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="aebac-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aebac-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aebac-116">Remarks</span></span>

<span data-ttu-id="aebac-117">El valor de sangría mínima definido por el sistema suele ser de cinco píxeles, pero no es fijo.</span><span class="sxs-lookup"><span data-stu-id="aebac-117">The system-defined minimum indent value is typically five pixels, but it is not fixed.</span></span> <span data-ttu-id="aebac-118">Para recuperar el valor exacto de la sangría mínima en un sistema determinado, envíe un mensaje **TVM \_ SETINDENT** con *wParam* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="aebac-118">To retrieve the exact value of the minimum indent on a particular system, send a **TVM\_SETINDENT** message with *wParam* set to zero.</span></span> <span data-ttu-id="aebac-119">A continuación, envíe un mensaje [**TVM \_ GETINDENT**](tvm-getindent.md) para recuperar el valor de sangría mínima.</span><span class="sxs-lookup"><span data-stu-id="aebac-119">Then send a [**TVM\_GETINDENT**](tvm-getindent.md) message to retrieve the minimum indent value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aebac-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aebac-120">Requirements</span></span>



| <span data-ttu-id="aebac-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="aebac-121">Requirement</span></span> | <span data-ttu-id="aebac-122">Value</span><span class="sxs-lookup"><span data-stu-id="aebac-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aebac-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aebac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aebac-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aebac-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aebac-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aebac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aebac-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="aebac-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aebac-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aebac-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aebac-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aebac-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aebac-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="aebac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aebac-130">**SetIndent de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="aebac-130">**TreeView\_SetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 






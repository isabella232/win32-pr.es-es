---
title: Mensaje de TVM_ENDEDITLABELNOW (commctrl. h)
description: Finaliza la edición de la etiqueta de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro EndEditLabelNow de TreeView.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533975"
---
# <a name="tvm_endeditlabelnow-message"></a><span data-ttu-id="f8d0b-105">\_Mensaje de ENDEDITLABELNOW TVM</span><span class="sxs-lookup"><span data-stu-id="f8d0b-105">TVM\_ENDEDITLABELNOW message</span></span>

<span data-ttu-id="f8d0b-106">Finaliza la edición de la etiqueta de un elemento de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="f8d0b-106">Ends the editing of a tree-view item's label.</span></span> <span data-ttu-id="f8d0b-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ EndEditLabelNow de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .</span><span class="sxs-lookup"><span data-stu-id="f8d0b-107">You can send this message explicitly or by using the [**TreeView\_EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8d0b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8d0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8d0b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8d0b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8d0b-110">Variable que indica si la edición se cancela sin guardarse en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f8d0b-110">Variable that indicates whether the editing is canceled without being saved to the label.</span></span> <span data-ttu-id="f8d0b-111">Si este parámetro es **true**, el sistema cancela la edición sin guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="f8d0b-111">If this parameter is **TRUE**, the system cancels editing without saving the changes.</span></span> <span data-ttu-id="f8d0b-112">De lo contrario, el sistema guarda los cambios en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f8d0b-112">Otherwise, the system saves the changes to the label.</span></span>

</dd> <dt>

<span data-ttu-id="f8d0b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8d0b-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f8d0b-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f8d0b-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8d0b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8d0b-115">Return value</span></span>

<span data-ttu-id="f8d0b-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f8d0b-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8d0b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8d0b-117">Remarks</span></span>

<span data-ttu-id="f8d0b-118">Este mensaje hace que el código de notificación [ \_ ENDLABELEDIT de TVN](tvn-endlabeledit.md) se envíe a la ventana primaria del control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="f8d0b-118">This message causes the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code to be sent to the parent window of the tree-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8d0b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8d0b-119">Requirements</span></span>



| <span data-ttu-id="f8d0b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8d0b-120">Requirement</span></span> | <span data-ttu-id="f8d0b-121">Value</span><span class="sxs-lookup"><span data-stu-id="f8d0b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d0b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8d0b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f8d0b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8d0b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8d0b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8d0b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f8d0b-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8d0b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8d0b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8d0b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8d0b-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8d0b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






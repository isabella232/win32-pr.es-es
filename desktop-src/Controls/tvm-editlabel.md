---
title: Mensaje de TVM_EDITLABEL (commctrl. h)
description: Comienza la edición en contexto del texto del elemento especificado y reemplaza el texto del elemento por un control de edición de una sola línea que contiene el texto.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- TVM_EDITLABEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996206"
---
# <a name="tvm_editlabel-message"></a><span data-ttu-id="0118b-104">\_Mensaje de EDITLABEL TVM</span><span class="sxs-lookup"><span data-stu-id="0118b-104">TVM\_EDITLABEL message</span></span>

<span data-ttu-id="0118b-105">Comienza la edición en contexto del texto del elemento especificado y reemplaza el texto del elemento por un control de edición de una sola línea que contiene el texto.</span><span class="sxs-lookup"><span data-stu-id="0118b-105">Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text.</span></span> <span data-ttu-id="0118b-106">Este mensaje selecciona implícitamente y se centra en el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="0118b-106">This message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="0118b-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ EditLabel de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="0118b-107">You can send this message explicitly or by using the [**TreeView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0118b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0118b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0118b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0118b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0118b-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0118b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0118b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0118b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0118b-112">Identificador del elemento que se va a editar.</span><span class="sxs-lookup"><span data-stu-id="0118b-112">Handle to the item to edit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0118b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0118b-113">Return value</span></span>

<span data-ttu-id="0118b-114">Devuelve el identificador del control de edición que se usa para editar el texto del elemento si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0118b-114">Returns the handle to the edit control used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0118b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0118b-115">Remarks</span></span>

<span data-ttu-id="0118b-116">Este mensaje envía un código de notificación de [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) al elemento primario del control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="0118b-116">This message sends a [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code to the parent of the tree-view control.</span></span>

<span data-ttu-id="0118b-117">Cuando el usuario finaliza o cancela la edición, el control de edición se destruye y el identificador ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="0118b-117">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="0118b-118">Puede crear subclases del control de edición, pero no destruirlo.</span><span class="sxs-lookup"><span data-stu-id="0118b-118">You can subclass the edit control, but do not destroy it.</span></span>

<span data-ttu-id="0118b-119">El control debe tener el foco antes de enviar este mensaje al control.</span><span class="sxs-lookup"><span data-stu-id="0118b-119">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="0118b-120">El foco se puede establecer mediante la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="0118b-120">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0118b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0118b-121">Requirements</span></span>



| <span data-ttu-id="0118b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0118b-122">Requirement</span></span> | <span data-ttu-id="0118b-123">Value</span><span class="sxs-lookup"><span data-stu-id="0118b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0118b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0118b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0118b-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0118b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0118b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0118b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0118b-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0118b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0118b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0118b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0118b-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0118b-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0118b-130">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="0118b-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0118b-131">**TVM \_ EDITLABELW** (Unicode) y **TVM \_ EDITLABELA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0118b-131">**TVM\_EDITLABELW** (Unicode) and **TVM\_EDITLABELA** (ANSI)</span></span><br/>               |



 


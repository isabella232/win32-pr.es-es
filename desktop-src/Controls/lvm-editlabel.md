---
title: Mensaje de LVM_EDITLABEL (commctrl. h)
description: Comienza la edición en contexto del texto del elemento de vista de lista especificado. El mensaje selecciona y centra implícitamente el elemento especificado. Puede enviar este mensaje explícitamente o mediante la \_ macro EditLabel de ListView.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- LVM_EDITLABEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801124"
---
# <a name="lvm_editlabel-message"></a><span data-ttu-id="5dedb-106">\_Mensaje EDITLABEL LVM</span><span class="sxs-lookup"><span data-stu-id="5dedb-106">LVM\_EDITLABEL message</span></span>

<span data-ttu-id="5dedb-107">Comienza la edición en contexto del texto del elemento de vista de lista especificado.</span><span class="sxs-lookup"><span data-stu-id="5dedb-107">Begins in-place editing of the specified list-view item's text.</span></span> <span data-ttu-id="5dedb-108">El mensaje selecciona y centra implícitamente el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="5dedb-108">The message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="5dedb-109">Puede enviar este mensaje explícitamente o mediante la macro [**\_ EditLabel de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="5dedb-109">You can send this message explicitly or by using the [**ListView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5dedb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5dedb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dedb-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5dedb-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dedb-112">Índice del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="5dedb-112">The index of the list-view item.</span></span> <span data-ttu-id="5dedb-113">Para cancelar la edición, establezca el índice en-1.</span><span class="sxs-lookup"><span data-stu-id="5dedb-113">To cancel editing, set the index to -1.</span></span>

</dd> <dt>

<span data-ttu-id="5dedb-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5dedb-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5dedb-115">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5dedb-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dedb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5dedb-116">Return value</span></span>

<span data-ttu-id="5dedb-117">Devuelve el identificador del control de edición que se usa para editar el texto del elemento si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5dedb-117">Returns the handle to the edit control that is used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dedb-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5dedb-118">Remarks</span></span>

<span data-ttu-id="5dedb-119">Cuando el usuario finaliza o cancela la edición, el control de edición se destruye y el identificador ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="5dedb-119">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="5dedb-120">Puede crear una subclase del control de edición, pero no debe destruirlo.</span><span class="sxs-lookup"><span data-stu-id="5dedb-120">You can subclass the edit control, but you should not destroy it.</span></span>

<span data-ttu-id="5dedb-121">El control debe tener el foco antes de enviar este mensaje al control.</span><span class="sxs-lookup"><span data-stu-id="5dedb-121">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="5dedb-122">El foco se puede establecer mediante la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="5dedb-122">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

<span data-ttu-id="5dedb-123">Si *wParam* es-1, se envía un código de notificación [ \_ ENDLABELEDIT de LVN](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="5dedb-123">If *wParam* is -1, an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dedb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dedb-124">Requirements</span></span>



| <span data-ttu-id="5dedb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dedb-125">Requirement</span></span> | <span data-ttu-id="5dedb-126">Value</span><span class="sxs-lookup"><span data-stu-id="5dedb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5dedb-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dedb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5dedb-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5dedb-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5dedb-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dedb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5dedb-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5dedb-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5dedb-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5dedb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dedb-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dedb-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5dedb-133">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5dedb-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5dedb-134">**LVM \_ EDITLABELW** (Unicode) y **\_ EDITLABELA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5dedb-134">**LVM\_EDITLABELW** (Unicode) and **LVM\_EDITLABELA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5dedb-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5dedb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dedb-136">**CANCELMODE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5dedb-136">**WM\_CANCELMODE**</span></span>](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 


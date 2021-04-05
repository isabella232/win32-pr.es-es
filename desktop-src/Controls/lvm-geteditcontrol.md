---
title: Mensaje de LVM_GETEDITCONTROL (commctrl. h)
description: Obtiene el identificador del control de edición que se usa para editar el texto de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetEditControl de ListView.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078869"
---
# <a name="lvm_geteditcontrol-message"></a><span data-ttu-id="60bfe-105">\_Mensaje GETEDITCONTROL LVM</span><span class="sxs-lookup"><span data-stu-id="60bfe-105">LVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="60bfe-106">Obtiene el identificador del control de edición que se usa para editar el texto de un elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="60bfe-106">Gets the handle to the edit control being used to edit a list-view item's text.</span></span> <span data-ttu-id="60bfe-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetEditControl de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="60bfe-107">You can send this message explicitly or by using the [**ListView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="60bfe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60bfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60bfe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60bfe-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="60bfe-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="60bfe-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="60bfe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60bfe-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="60bfe-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="60bfe-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60bfe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60bfe-113">Return value</span></span>

<span data-ttu-id="60bfe-114">Devuelve el identificador del control de edición si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="60bfe-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="60bfe-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60bfe-115">Remarks</span></span>

<span data-ttu-id="60bfe-116">Cuando comienza la edición de etiquetas, se crea, coloca y Inicializa un control de edición.</span><span class="sxs-lookup"><span data-stu-id="60bfe-116">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="60bfe-117">Antes de que se muestre, el control de vista de lista envía a su ventana primaria un código de notificación [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="60bfe-117">Before it is displayed, the list-view control sends its parent window an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="60bfe-118">Para personalizar la edición de etiquetas, implemente un controlador para [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) y envíe un mensaje **LVM \_ GETEDITCONTROL** al control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="60bfe-118">To customize label editing, implement a handler for [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) and have it send an **LVM\_GETEDITCONTROL** message to the list-view control.</span></span> <span data-ttu-id="60bfe-119">Si se está editando una etiqueta, el valor devuelto será un identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="60bfe-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="60bfe-120">Use este identificador para personalizar el control de edición mediante el envío de los mensajes de **em \_ XXX** habituales.</span><span class="sxs-lookup"><span data-stu-id="60bfe-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="60bfe-121">Cuando el usuario finaliza o cancela la edición, el control de edición se destruye y el identificador ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="60bfe-121">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="60bfe-122">Puede crear una subclase del control de edición, pero no debe destruirlo.</span><span class="sxs-lookup"><span data-stu-id="60bfe-122">You can subclass the edit control, but you should not destroy it.</span></span> <span data-ttu-id="60bfe-123">Para cancelar la edición, envíe un mensaje de [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) al control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="60bfe-123">To cancel editing, send the list-view control a [**WM\_CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) message.</span></span>

<span data-ttu-id="60bfe-124">El elemento de vista de lista que se está editando es el elemento que tiene actualmente el foco, es decir, el elemento en el estado Focused.</span><span class="sxs-lookup"><span data-stu-id="60bfe-124">The list-view item being edited is the currently focused item that is, the item in the focused state.</span></span> <span data-ttu-id="60bfe-125">Para buscar un elemento en función de su estado, use el mensaje [**\_ GETNEXTITEM de LVM**](lvm-getnextitem.md) .</span><span class="sxs-lookup"><span data-stu-id="60bfe-125">To find an item based on its state, use the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="60bfe-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60bfe-126">Requirements</span></span>



| <span data-ttu-id="60bfe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="60bfe-127">Requirement</span></span> | <span data-ttu-id="60bfe-128">Value</span><span class="sxs-lookup"><span data-stu-id="60bfe-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60bfe-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60bfe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="60bfe-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="60bfe-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60bfe-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60bfe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="60bfe-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="60bfe-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60bfe-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60bfe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="60bfe-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60bfe-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60bfe-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="60bfe-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60bfe-136">**GetEditControl de ListView \_**</span><span class="sxs-lookup"><span data-stu-id="60bfe-136">**ListView\_GetEditControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 


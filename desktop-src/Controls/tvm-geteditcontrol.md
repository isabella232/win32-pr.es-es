---
title: Mensaje de TVM_GETEDITCONTROL (commctrl. h)
description: Recupera el identificador del control de edición que se usa para editar el texto de un elemento de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetEditControl de TreeView.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- TVM_GETEDITCONTROL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151046"
---
# <a name="tvm_geteditcontrol-message"></a><span data-ttu-id="00103-105">\_Mensaje de GETEDITCONTROL TVM</span><span class="sxs-lookup"><span data-stu-id="00103-105">TVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="00103-106">Recupera el identificador del control de edición que se usa para editar el texto de un elemento de la vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="00103-106">Retrieves the handle to the edit control being used to edit a tree-view item's text.</span></span> <span data-ttu-id="00103-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetEditControl de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="00103-107">You can send this message explicitly or by using the [**TreeView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="00103-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00103-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00103-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00103-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="00103-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="00103-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="00103-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00103-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="00103-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="00103-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00103-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00103-113">Return value</span></span>

<span data-ttu-id="00103-114">Devuelve el identificador del control de edición si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="00103-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="00103-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00103-115">Remarks</span></span>

<span data-ttu-id="00103-116">Cuando comienza la edición de etiquetas, se crea un control de edición, pero no se coloca ni se muestra.</span><span class="sxs-lookup"><span data-stu-id="00103-116">When label editing begins, an edit control is created, but not positioned or displayed.</span></span> <span data-ttu-id="00103-117">Antes de que se muestre, el control de vista de árbol envía a su ventana primaria un código de notificación [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="00103-117">Before it is displayed, the tree-view control sends its parent window an [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="00103-118">Para personalizar la edición de etiquetas, implemente un controlador para [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) y envíe un mensaje **TVM \_ GETEDITCONTROL** al control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="00103-118">To customize label editing, implement a handler for [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) and have it send a **TVM\_GETEDITCONTROL** message to the tree-view control.</span></span> <span data-ttu-id="00103-119">Si se está editando una etiqueta, el valor devuelto será un identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="00103-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="00103-120">Use este identificador para personalizar el control de edición mediante el envío de los mensajes de **em \_ XXX** habituales.</span><span class="sxs-lookup"><span data-stu-id="00103-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="00103-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00103-121">Requirements</span></span>



| <span data-ttu-id="00103-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="00103-122">Requirement</span></span> | <span data-ttu-id="00103-123">Value</span><span class="sxs-lookup"><span data-stu-id="00103-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00103-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00103-124">Minimum supported client</span></span><br/> | <span data-ttu-id="00103-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="00103-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00103-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00103-126">Minimum supported server</span></span><br/> | <span data-ttu-id="00103-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="00103-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00103-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00103-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="00103-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00103-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






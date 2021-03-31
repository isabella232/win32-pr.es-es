---
title: Mensaje EM_GETREDONAME (RichEdit. h)
description: Recupera el tipo de la siguiente acción, si existe, en la cola de rehacer del control Rich Edit.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996504"
---
# <a name="em_getredoname-message"></a><span data-ttu-id="f4676-104">\_Mensaje GETREDONAME em</span><span class="sxs-lookup"><span data-stu-id="f4676-104">EM\_GETREDONAME message</span></span>

<span data-ttu-id="f4676-105">Recupera el tipo de la siguiente acción, si existe, en la cola de rehacer del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f4676-105">Retrieves the type of the next action, if any, in the rich edit control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4676-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4676-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4676-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4676-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4676-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f4676-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f4676-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4676-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4676-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f4676-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4676-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4676-111">Return value</span></span>

<span data-ttu-id="f4676-112">Si la cola rehecha del control no está vacía, el valor devuelto es un valor de enumeración [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica el tipo de la siguiente acción en la cola de puesta al día del control.</span><span class="sxs-lookup"><span data-stu-id="f4676-112">If the redo queue for the control is not empty, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's redo queue.</span></span>

<span data-ttu-id="f4676-113">Si no hay ninguna acción que se puedan rehacer o se desconoce el tipo de la siguiente acción que se pueden rehacer, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="f4676-113">If there are no redoable actions or the type of the next redoable action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4676-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4676-114">Remarks</span></span>

<span data-ttu-id="f4676-115">Entre los tipos de acciones que se pueden deshacer o rehacer se incluyen las operaciones de escribir, eliminar, arrastrar y colocar, cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="f4676-115">The types of actions that can be undone or redone include typing, delete, drag-drop, cut, and paste operations.</span></span> <span data-ttu-id="f4676-116">Esta información puede ser útil para las aplicaciones que proporcionan una interfaz de usuario extendida para las operaciones de deshacer y rehacer, como un cuadro de lista desplegable de acciones que se pueden rehacer.</span><span class="sxs-lookup"><span data-stu-id="f4676-116">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of redoable actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4676-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4676-117">Requirements</span></span>



| <span data-ttu-id="f4676-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4676-118">Requirement</span></span> | <span data-ttu-id="f4676-119">Value</span><span class="sxs-lookup"><span data-stu-id="f4676-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4676-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4676-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4676-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f4676-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4676-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4676-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4676-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4676-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4676-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4676-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4676-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4676-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4676-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4676-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4676-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f4676-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f4676-128">**\_GETUNDONAME em**</span><span class="sxs-lookup"><span data-stu-id="f4676-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="f4676-129">**rehacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="f4676-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="f4676-130">**deshacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="f4676-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="f4676-131">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="f4676-131">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 






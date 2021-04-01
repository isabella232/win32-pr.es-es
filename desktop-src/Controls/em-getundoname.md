---
title: Mensaje EM_GETUNDONAME (RichEdit. h)
description: Microsoft Rich Edit 2,0 y versiones posteriores recupera el tipo de la siguiente acción de deshacer, si existe. Microsoft Rich Edit 1,0 este mensaje no se admite.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- EM_GETUNDONAME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996824"
---
# <a name="em_getundoname-message"></a><span data-ttu-id="e3d9b-104">\_Mensaje GETUNDONAME em</span><span class="sxs-lookup"><span data-stu-id="e3d9b-104">EM\_GETUNDONAME message</span></span>

<span data-ttu-id="e3d9b-105">Microsoft Rich Edit 2,0 y versiones posteriores: recupera el tipo de la siguiente acción de deshacer, si existe.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-105">Microsoft Rich Edit 2.0 and later: Retrieves the type of the next undo action, if any.</span></span>

<span data-ttu-id="e3d9b-106">Microsoft Rich Edit 1,0: este mensaje no se admite.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-106">Microsoft Rich Edit 1.0: This message is not supported.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3d9b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3d9b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3d9b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3d9b-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3d9b-109">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e3d9b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3d9b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3d9b-111">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3d9b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3d9b-112">Return value</span></span>

<span data-ttu-id="e3d9b-113">Si hay una acción de deshacer, el valor devuelto es un valor de enumeración [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica el tipo de la siguiente acción en la cola de deshacer del control.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-113">If there is an undo action, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's undo queue.</span></span>

<span data-ttu-id="e3d9b-114">Si no hay ninguna acción que se pueda deshacer o se desconoce el tipo de la siguiente acción de deshacer, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-114">If there are no actions that can be undone or the type of the next undo action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3d9b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3d9b-115">Remarks</span></span>

<span data-ttu-id="e3d9b-116">Entre los tipos de acciones que se pueden deshacer o rehacer se incluyen las operaciones de escribir, eliminar, arrastrar, colocar, cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-116">The types of actions that can be undone or redone include typing, delete, drag, drop, cut, and paste operations.</span></span> <span data-ttu-id="e3d9b-117">Esta información puede ser útil para las aplicaciones que proporcionan una interfaz de usuario extendida para las operaciones de deshacer y rehacer, como un cuadro de lista desplegable de acciones que se pueden deshacer.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-117">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of actions that can be undone.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d9b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3d9b-118">Requirements</span></span>



| <span data-ttu-id="e3d9b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3d9b-119">Requirement</span></span> | <span data-ttu-id="e3d9b-120">Value</span><span class="sxs-lookup"><span data-stu-id="e3d9b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d9b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3d9b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d9b-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e3d9b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3d9b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3d9b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d9b-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3d9b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3d9b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3d9b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3d9b-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3d9b-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3d9b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3d9b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e3d9b-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e3d9b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e3d9b-129">**\_GETREDONAME em**</span><span class="sxs-lookup"><span data-stu-id="e3d9b-129">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="e3d9b-130">**rehacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="e3d9b-130">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="e3d9b-131">**deshacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="e3d9b-131">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="e3d9b-132">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="e3d9b-132">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 






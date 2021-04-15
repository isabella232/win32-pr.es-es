---
title: Mensaje de CB_GETEXTENDEDUI (Winuser. h)
description: Determina si un cuadro combinado tiene la interfaz de usuario predeterminada o la interfaz de usuario extendida.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- CB_GETEXTENDEDUI controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490547"
---
# <a name="cb_getextendedui-message"></a><span data-ttu-id="f6fac-104">\_Mensaje GETEXTENDEDUI CB</span><span class="sxs-lookup"><span data-stu-id="f6fac-104">CB\_GETEXTENDEDUI message</span></span>

<span data-ttu-id="f6fac-105">Determina si un cuadro combinado tiene la interfaz de usuario predeterminada o la interfaz de usuario extendida.</span><span class="sxs-lookup"><span data-stu-id="f6fac-105">Determines whether a combo box has the default user interface or the extended user interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6fac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6fac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6fac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6fac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6fac-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f6fac-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f6fac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6fac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6fac-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f6fac-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6fac-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6fac-111">Return value</span></span>

<span data-ttu-id="f6fac-112">Si el cuadro combinado tiene la interfaz de usuario extendida, el valor devuelto es **true**; de lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="f6fac-112">If the combo box has the extended user interface, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6fac-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6fac-113">Remarks</span></span>

<span data-ttu-id="f6fac-114">De forma predeterminada, la tecla F4 abre o cierra la lista y la flecha hacia abajo cambia la selección actual.</span><span class="sxs-lookup"><span data-stu-id="f6fac-114">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="f6fac-115">En un cuadro combinado con la interfaz de usuario extendida, la tecla F4 está deshabilitada y, al presionar la tecla flecha abajo, se abre la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="f6fac-115">In a combo box with the extended user interface, the F4 key is disabled and pressing the DOWN ARROW key opens the drop-down list.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6fac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6fac-116">Requirements</span></span>



| <span data-ttu-id="f6fac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6fac-117">Requirement</span></span> | <span data-ttu-id="f6fac-118">Value</span><span class="sxs-lookup"><span data-stu-id="f6fac-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6fac-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6fac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f6fac-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f6fac-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f6fac-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6fac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f6fac-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6fac-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f6fac-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6fac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6fac-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6fac-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6fac-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6fac-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6fac-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f6fac-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f6fac-127">**CB \_ SETEXTENDEDUI**</span><span class="sxs-lookup"><span data-stu-id="f6fac-127">**CB\_SETEXTENDEDUI**</span></span>](cb-setextendedui.md)
</dt> <dt>

<span data-ttu-id="f6fac-128">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f6fac-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f6fac-129">Características del cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="f6fac-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 






---
title: Mensaje de LVM_SETSELECTIONMARK (commctrl. h)
description: Establece la marca de selección en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetSelectionMark de ListView.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801100"
---
# <a name="lvm_setselectionmark-message"></a><span data-ttu-id="54434-105">\_Mensaje SETSELECTIONMARK LVM</span><span class="sxs-lookup"><span data-stu-id="54434-105">LVM\_SETSELECTIONMARK message</span></span>

<span data-ttu-id="54434-106">Establece la marca de selección en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="54434-106">Sets the selection mark in a list-view control.</span></span> <span data-ttu-id="54434-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetSelectionMark de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="54434-107">You can send this message explicitly or use the [**ListView\_SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="54434-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54434-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54434-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54434-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="54434-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="54434-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="54434-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54434-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54434-112">Índice de base cero de la nueva marca de selección.</span><span class="sxs-lookup"><span data-stu-id="54434-112">Zero-based index of the new selection mark.</span></span> <span data-ttu-id="54434-113">Si se establece en-1, se quita la marca de selección.</span><span class="sxs-lookup"><span data-stu-id="54434-113">If set to -1, the selection mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54434-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54434-114">Return value</span></span>

<span data-ttu-id="54434-115">Devuelve la marca de selección anterior, o-1 si no hay ninguna marca de selección anterior.</span><span class="sxs-lookup"><span data-stu-id="54434-115">Returns the previous selection mark, or -1 if there is no previous selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="54434-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54434-116">Remarks</span></span>

<span data-ttu-id="54434-117">La *marca de selección* es el índice del elemento desde el que se inicia una selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="54434-117">The *selection mark* is the item index from which a multiple selection starts.</span></span> <span data-ttu-id="54434-118">Este mensaje no afecta al estado de selección del elemento.</span><span class="sxs-lookup"><span data-stu-id="54434-118">This message does not affect the selection state of the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="54434-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54434-119">Requirements</span></span>



| <span data-ttu-id="54434-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="54434-120">Requirement</span></span> | <span data-ttu-id="54434-121">Value</span><span class="sxs-lookup"><span data-stu-id="54434-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54434-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54434-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54434-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="54434-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54434-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54434-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54434-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="54434-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54434-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54434-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54434-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54434-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54434-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="54434-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54434-129">**\_GETSELECTIONMARK LVM**</span><span class="sxs-lookup"><span data-stu-id="54434-129">**LVM\_GETSELECTIONMARK**</span></span>](lvm-getselectionmark.md)
</dt> </dl>

 

 






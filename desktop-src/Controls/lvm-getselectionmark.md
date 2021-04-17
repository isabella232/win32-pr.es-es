---
title: Mensaje de LVM_GETSELECTIONMARK (commctrl. h)
description: Recupera la marca de selección de un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetSelectionMark de ListView.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- LVM_GETSELECTIONMARK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658339"
---
# <a name="lvm_getselectionmark-message"></a><span data-ttu-id="ecf46-105">\_Mensaje GETSELECTIONMARK LVM</span><span class="sxs-lookup"><span data-stu-id="ecf46-105">LVM\_GETSELECTIONMARK message</span></span>

<span data-ttu-id="ecf46-106">Recupera la marca de selección de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="ecf46-106">Retrieves the selection mark from a list-view control.</span></span> <span data-ttu-id="ecf46-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetSelectionMark de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="ecf46-107">You can send this message explicitly or use the [**ListView\_GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecf46-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecf46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf46-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecf46-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ecf46-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ecf46-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ecf46-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecf46-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ecf46-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ecf46-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecf46-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecf46-113">Return value</span></span>

<span data-ttu-id="ecf46-114">Devuelve la marca de selección de base cero, o-1 si no hay ninguna marca de selección.</span><span class="sxs-lookup"><span data-stu-id="ecf46-114">Returns the zero-based selection mark, or -1 if there is no selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf46-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecf46-115">Remarks</span></span>

<span data-ttu-id="ecf46-116">La *marca de selección* es el índice del elemento desde el que se inicia una selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="ecf46-116">The *selection mark* is the item index from which a multiple selection starts.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf46-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecf46-117">Requirements</span></span>



| <span data-ttu-id="ecf46-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecf46-118">Requirement</span></span> | <span data-ttu-id="ecf46-119">Value</span><span class="sxs-lookup"><span data-stu-id="ecf46-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf46-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecf46-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf46-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ecf46-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ecf46-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecf46-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf46-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecf46-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ecf46-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecf46-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecf46-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf46-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf46-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecf46-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf46-127">**\_SETSELECTIONMARK LVM**</span><span class="sxs-lookup"><span data-stu-id="ecf46-127">**LVM\_SETSELECTIONMARK**</span></span>](lvm-setselectionmark.md)
</dt> </dl>

 

 






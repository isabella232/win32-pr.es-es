---
title: Mensaje de LB_GETSELCOUNT (Winuser. h)
description: Obtiene el número total de elementos seleccionados en un cuadro de lista de selección múltiple.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- LB_GETSELCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150137"
---
# <a name="lb_getselcount-message"></a><span data-ttu-id="996fd-104">\_Mensaje lb GETSELCOUNT</span><span class="sxs-lookup"><span data-stu-id="996fd-104">LB\_GETSELCOUNT message</span></span>

<span data-ttu-id="996fd-105">Obtiene el número total de elementos seleccionados en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="996fd-105">Gets the total number of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="996fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="996fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="996fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="996fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="996fd-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="996fd-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="996fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="996fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="996fd-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="996fd-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="996fd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="996fd-111">Return value</span></span>

<span data-ttu-id="996fd-112">El valor devuelto es el recuento de los elementos seleccionados en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="996fd-112">The return value is the count of selected items in the list box.</span></span> <span data-ttu-id="996fd-113">Si el cuadro de lista es un cuadro de lista de selección única, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="996fd-113">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="996fd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="996fd-114">Requirements</span></span>



| <span data-ttu-id="996fd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="996fd-115">Requirement</span></span> | <span data-ttu-id="996fd-116">Value</span><span class="sxs-lookup"><span data-stu-id="996fd-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="996fd-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="996fd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="996fd-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="996fd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="996fd-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="996fd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="996fd-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="996fd-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="996fd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="996fd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="996fd-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="996fd-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="996fd-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="996fd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996fd-124">**LB \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="996fd-124">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 






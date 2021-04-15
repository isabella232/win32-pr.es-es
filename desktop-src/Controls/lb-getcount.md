---
title: Mensaje de LB_GETCOUNT (Winuser. h)
description: Obtiene el número de elementos de un cuadro de lista.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- LB_GETCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddedbd7b9165e00e722edbadbb8806a68417551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492856"
---
# <a name="lb_getcount-message"></a><span data-ttu-id="da32f-104">Mensaje de LB \_ GETCOUNT</span><span class="sxs-lookup"><span data-stu-id="da32f-104">LB\_GETCOUNT message</span></span>

<span data-ttu-id="da32f-105">Obtiene el número de elementos de un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="da32f-105">Gets the number of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="da32f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da32f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da32f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da32f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da32f-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="da32f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="da32f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da32f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da32f-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="da32f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da32f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da32f-111">Return value</span></span>

<span data-ttu-id="da32f-112">El valor devuelto es el número de elementos del cuadro de lista o LB \_ Err si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="da32f-112">The return value is the number of items in the list box, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="da32f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da32f-113">Remarks</span></span>

<span data-ttu-id="da32f-114">El recuento devuelto es uno mayor que el valor de índice del último elemento (el índice está basado en cero).</span><span class="sxs-lookup"><span data-stu-id="da32f-114">The returned count is one greater than the index value of the last item (the index is zero-based).</span></span>

## <a name="requirements"></a><span data-ttu-id="da32f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da32f-115">Requirements</span></span>



| <span data-ttu-id="da32f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="da32f-116">Requirement</span></span> | <span data-ttu-id="da32f-117">Value</span><span class="sxs-lookup"><span data-stu-id="da32f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da32f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da32f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="da32f-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="da32f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da32f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da32f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="da32f-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="da32f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da32f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da32f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="da32f-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da32f-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da32f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="da32f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da32f-125">**LB \_ SETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="da32f-125">**LB\_SETCOUNT**</span></span>](lb-setcount.md)
</dt> </dl>

 

 






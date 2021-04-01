---
title: Mensaje de LB_RESETCONTENT (Winuser. h)
description: Quita todos los elementos de un cuadro de lista.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- LB_RESETCONTENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0091871df045812dcaa7a159cc456a1350d20f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905518"
---
# <a name="lb_resetcontent-message"></a><span data-ttu-id="c32b5-104">\_Mensaje lb RESETCONTENT</span><span class="sxs-lookup"><span data-stu-id="c32b5-104">LB\_RESETCONTENT message</span></span>

<span data-ttu-id="c32b5-105">Quita todos los elementos de un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="c32b5-105">Removes all items from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c32b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c32b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c32b5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c32b5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c32b5-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c32b5-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c32b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c32b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c32b5-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c32b5-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c32b5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c32b5-111">Return value</span></span>

<span data-ttu-id="c32b5-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c32b5-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32b5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c32b5-113">Remarks</span></span>

<span data-ttu-id="c32b5-114">Si el cuadro de lista tiene un estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , el propietario del cuadro de lista recibe un mensaje de [**WM \_ DELETEITEM**](wm-deleteitem.md) para cada elemento del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="c32b5-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the owner of the list box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="c32b5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c32b5-115">Requirements</span></span>



| <span data-ttu-id="c32b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c32b5-116">Requirement</span></span> | <span data-ttu-id="c32b5-117">Value</span><span class="sxs-lookup"><span data-stu-id="c32b5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c32b5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c32b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c32b5-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c32b5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c32b5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c32b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c32b5-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c32b5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c32b5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c32b5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c32b5-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c32b5-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c32b5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c32b5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c32b5-125">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="c32b5-125">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 






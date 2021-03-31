---
title: Mensaje de LB_GETTOPINDEX (Winuser. h)
description: Obtiene el índice del primer elemento visible de un cuadro de lista.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- LB_GETTOPINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996429"
---
# <a name="lb_gettopindex-message"></a><span data-ttu-id="d0ac3-104">\_Mensaje lb GETTOPINDEX</span><span class="sxs-lookup"><span data-stu-id="d0ac3-104">LB\_GETTOPINDEX message</span></span>

<span data-ttu-id="d0ac3-105">Obtiene el índice del primer elemento visible de un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-105">Gets the index of the first visible item in a list box.</span></span> <span data-ttu-id="d0ac3-106">Inicialmente, el elemento con el índice 0 está en la parte superior del cuadro de lista, pero si el contenido del cuadro de lista se ha desplazado, es posible que haya otro elemento en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-106">Initially the item with index 0 is at the top of the list box, but if the list box contents have been scrolled another item may be at the top.</span></span> <span data-ttu-id="d0ac3-107">El primer elemento visible de un cuadro de lista de varias columnas es el elemento superior izquierdo.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-107">The first visible item in a multiple-column list box is the top-left item.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0ac3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0ac3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ac3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0ac3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ac3-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d0ac3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0ac3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ac3-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ac3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0ac3-113">Return value</span></span>

<span data-ttu-id="d0ac3-114">El valor devuelto es el índice del primer elemento visible en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="d0ac3-114">The return value is the index of the first visible item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ac3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0ac3-115">Requirements</span></span>



| <span data-ttu-id="d0ac3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0ac3-116">Requirement</span></span> | <span data-ttu-id="d0ac3-117">Value</span><span class="sxs-lookup"><span data-stu-id="d0ac3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ac3-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0ac3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ac3-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d0ac3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d0ac3-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0ac3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ac3-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0ac3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0ac3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0ac3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0ac3-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0ac3-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ac3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0ac3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ac3-125">**LB \_ SETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="d0ac3-125">**LB\_SETTOPINDEX**</span></span>](lb-settopindex.md)
</dt> </dl>

 

 






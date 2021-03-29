---
title: Mensaje de LB_GETANCHORINDEX (Winuser. h)
description: Obtiene el índice del elemento de delimitador \ 8212; es decir, el elemento desde el que se inicia una selección múltiple. Una selección múltiple abarca todos los elementos del elemento delimitador hasta el elemento del símbolo de intercalación.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getanchorindex.htm
keywords:
- LB_GETANCHORINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5502a234424b818bb46e9c4326839b5aff2f83d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535254"
---
# <a name="lb_getanchorindex-message"></a><span data-ttu-id="c778b-105">\_Mensaje lb GETANCHORINDEX</span><span class="sxs-lookup"><span data-stu-id="c778b-105">LB\_GETANCHORINDEX message</span></span>

<span data-ttu-id="c778b-106">Obtiene el índice del elemento delimitador, que es el elemento desde el que se inicia una selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="c778b-106">Gets the index of the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="c778b-107">Una selección múltiple abarca todos los elementos del elemento delimitador hasta el elemento del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="c778b-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="c778b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c778b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c778b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c778b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c778b-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c778b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c778b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c778b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c778b-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c778b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c778b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c778b-113">Return value</span></span>

<span data-ttu-id="c778b-114">El valor devuelto es el índice del elemento delimitador.</span><span class="sxs-lookup"><span data-stu-id="c778b-114">The return value is the index of the anchor item.</span></span>

## <a name="requirements"></a><span data-ttu-id="c778b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c778b-115">Requirements</span></span>



| <span data-ttu-id="c778b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c778b-116">Requirement</span></span> | <span data-ttu-id="c778b-117">Value</span><span class="sxs-lookup"><span data-stu-id="c778b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c778b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c778b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c778b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c778b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c778b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c778b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c778b-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c778b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c778b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c778b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c778b-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c778b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c778b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c778b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c778b-125">**LB \_ SETANCHORINDEX**</span><span class="sxs-lookup"><span data-stu-id="c778b-125">**LB\_SETANCHORINDEX**</span></span>](lb-setanchorindex.md)
</dt> </dl>

 

 






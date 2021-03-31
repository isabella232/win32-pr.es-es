---
title: Mensaje de HDM_ORDERTOINDEX (commctrl. h)
description: Recupera un valor de índice para un elemento en función de su orden en el control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header OrderToIndex.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- HDM_ORDERTOINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079308"
---
# <a name="hdm_ordertoindex-message"></a><span data-ttu-id="8a232-105">HDM \_ ORDERTOINDEX</span><span class="sxs-lookup"><span data-stu-id="8a232-105">HDM\_ORDERTOINDEX message</span></span>

<span data-ttu-id="8a232-106">Recupera un valor de índice para un elemento en función de su orden en el control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8a232-106">Retrieves an index value for an item based on its order in the header control.</span></span> <span data-ttu-id="8a232-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) .</span><span class="sxs-lookup"><span data-stu-id="8a232-107">You can send this message explicitly or use the [**Header\_OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a232-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a232-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a232-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a232-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a232-110">El orden en el que aparece el elemento dentro del control de encabezado, de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="8a232-110">The order in which the item appears within the header control, from left to right.</span></span> <span data-ttu-id="8a232-111">Por ejemplo, el valor de índice del elemento en la columna de la izquierda es 0.</span><span class="sxs-lookup"><span data-stu-id="8a232-111">For example, the index value of the item in the far left column would be 0.</span></span> <span data-ttu-id="8a232-112">El valor del siguiente elemento a la derecha sería 1, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="8a232-112">The value for the next item to the right would be 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8a232-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a232-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8a232-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8a232-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a232-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a232-115">Return value</span></span>

<span data-ttu-id="8a232-116">Devuelve un valor INT que indica el índice del elemento.</span><span class="sxs-lookup"><span data-stu-id="8a232-116">Returns INT that indicates the item index.</span></span> <span data-ttu-id="8a232-117">Si *wParam* no es válido (negativo o demasiado grande), el valor devuelto es igual a *wParam*.</span><span class="sxs-lookup"><span data-stu-id="8a232-117">If *wParam* is invalid (negative or too large), the return equals *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a232-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a232-118">Requirements</span></span>



| <span data-ttu-id="8a232-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a232-119">Requirement</span></span> | <span data-ttu-id="8a232-120">Value</span><span class="sxs-lookup"><span data-stu-id="8a232-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a232-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a232-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8a232-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8a232-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a232-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a232-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8a232-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a232-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a232-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a232-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a232-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a232-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






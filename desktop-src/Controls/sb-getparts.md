---
title: Mensaje de SB_GETPARTS (commctrl. h)
description: Recupera un recuento de los elementos de una ventana de estado. El mensaje también recupera la coordenada del borde derecho del número especificado de partes.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534833"
---
# <a name="sb_getparts-message"></a><span data-ttu-id="487f1-105">\_Mensaje GETPARTS de SB</span><span class="sxs-lookup"><span data-stu-id="487f1-105">SB\_GETPARTS message</span></span>

<span data-ttu-id="487f1-106">Recupera un recuento de los elementos de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="487f1-106">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="487f1-107">El mensaje también recupera la coordenada del borde derecho del número especificado de partes.</span><span class="sxs-lookup"><span data-stu-id="487f1-107">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span>

## <a name="parameters"></a><span data-ttu-id="487f1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="487f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="487f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="487f1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="487f1-110">Número de elementos para los que se van a recuperar las coordenadas.</span><span class="sxs-lookup"><span data-stu-id="487f1-110">Number of parts for which to retrieve coordinates.</span></span> <span data-ttu-id="487f1-111">Si este parámetro es mayor que el número de partes de la ventana, el mensaje solo recupera las coordenadas de los elementos existentes.</span><span class="sxs-lookup"><span data-stu-id="487f1-111">If this parameter is greater than the number of parts in the window, the message retrieves coordinates for existing parts only.</span></span>

</dd> <dt>

<span data-ttu-id="487f1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="487f1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="487f1-113">Puntero a una matriz de enteros que tiene el mismo número de elementos que las partes especificadas por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="487f1-113">Pointer to an integer array that has the same number of elements as parts specified by *wParam*.</span></span> <span data-ttu-id="487f1-114">Cada elemento de la matriz recibe la coordenada del cliente del borde derecho del elemento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="487f1-114">Each element in the array receives the client coordinate of the right edge of the corresponding part.</span></span> <span data-ttu-id="487f1-115">Si un elemento se establece en-1, la posición del borde derecho de esa parte se extiende hasta el borde derecho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="487f1-115">If an element is set to -1, the position of the right edge for that part extends to the right edge of the window.</span></span> <span data-ttu-id="487f1-116">Para recuperar el número actual de partes, establezca este parámetro en cero.</span><span class="sxs-lookup"><span data-stu-id="487f1-116">To retrieve the current number of parts, set this parameter to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="487f1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="487f1-117">Return value</span></span>

<span data-ttu-id="487f1-118">Devuelve el número de partes de la ventana.</span><span class="sxs-lookup"><span data-stu-id="487f1-118">Returns the number of parts in the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="487f1-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="487f1-119">Remarks</span></span>

<span data-ttu-id="487f1-120">Este mensaje siempre devuelve el número de partes de la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="487f1-120">This message always returns the number of parts in the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="487f1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="487f1-121">Requirements</span></span>



| <span data-ttu-id="487f1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="487f1-122">Requirement</span></span> | <span data-ttu-id="487f1-123">Value</span><span class="sxs-lookup"><span data-stu-id="487f1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="487f1-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="487f1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="487f1-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="487f1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="487f1-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="487f1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="487f1-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="487f1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="487f1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="487f1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="487f1-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="487f1-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






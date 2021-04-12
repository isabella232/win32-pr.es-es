---
title: Mensaje de LB_GETITEMRECT (Winuser. h)
description: Obtiene las dimensiones del rectángulo que delimita un elemento de cuadro de lista tal como se muestra actualmente en el cuadro de lista.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- LB_GETITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b66c7c1a3e9f93e90beea40869cecb2081cb20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490205"
---
# <a name="lb_getitemrect-message"></a><span data-ttu-id="07b60-104">\_Mensaje lb GETITEMRECT</span><span class="sxs-lookup"><span data-stu-id="07b60-104">LB\_GETITEMRECT message</span></span>

<span data-ttu-id="07b60-105">Obtiene las dimensiones del rectángulo que delimita un elemento de cuadro de lista tal como se muestra actualmente en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="07b60-105">Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="07b60-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07b60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07b60-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07b60-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07b60-108">El índice de base cero de un elemento.</span><span class="sxs-lookup"><span data-stu-id="07b60-108">The zero-based index of the item.</span></span>

<span data-ttu-id="07b60-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="07b60-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="07b60-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="07b60-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="07b60-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="07b60-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="07b60-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07b60-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07b60-113">Un puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá las coordenadas de cliente para el elemento en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="07b60-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the client coordinates for the item in the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07b60-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07b60-114">Return value</span></span>

<span data-ttu-id="07b60-115">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="07b60-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="07b60-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b60-116">Requirements</span></span>



| <span data-ttu-id="07b60-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b60-117">Requirement</span></span> | <span data-ttu-id="07b60-118">Value</span><span class="sxs-lookup"><span data-stu-id="07b60-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b60-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07b60-119">Minimum supported client</span></span><br/> | <span data-ttu-id="07b60-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="07b60-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="07b60-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07b60-121">Minimum supported server</span></span><br/> | <span data-ttu-id="07b60-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="07b60-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07b60-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07b60-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="07b60-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07b60-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b60-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="07b60-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="07b60-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07b60-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 


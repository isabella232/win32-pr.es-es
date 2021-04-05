---
title: Mensaje de LB_ITEMFROMPOINT (Winuser. h)
description: Obtiene el índice de base cero del elemento más próximo al punto especificado en un cuadro de lista.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803416"
---
# <a name="lb_itemfrompoint-message"></a><span data-ttu-id="0b952-104">\_Mensaje lb ITEMFROMPOINT</span><span class="sxs-lookup"><span data-stu-id="0b952-104">LB\_ITEMFROMPOINT message</span></span>

<span data-ttu-id="0b952-105">Obtiene el índice de base cero del elemento más próximo al punto especificado en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="0b952-105">Gets the zero-based index of the item nearest the specified point in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b952-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b952-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b952-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b952-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b952-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0b952-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b952-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b952-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b952-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la coordenada x de un punto, con respecto a la esquina superior izquierda del área cliente del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="0b952-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

<span data-ttu-id="0b952-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la coordenada y de un punto con respecto a la esquina superior izquierda del área cliente del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="0b952-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b952-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b952-112">Return value</span></span>

<span data-ttu-id="0b952-113">El valor devuelto contiene el índice del elemento más cercano en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b952-113">The return value contains the index of the nearest item in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span> <span data-ttu-id="0b952-114">El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es cero si el punto especificado se encuentra en el área cliente del cuadro de lista, o en uno si está fuera del área cliente.</span><span class="sxs-lookup"><span data-stu-id="0b952-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is zero if the specified point is in the client area of the list box, or one if it is outside the client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b952-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b952-115">Requirements</span></span>



| <span data-ttu-id="0b952-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b952-116">Requirement</span></span> | <span data-ttu-id="0b952-117">Value</span><span class="sxs-lookup"><span data-stu-id="0b952-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b952-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b952-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0b952-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0b952-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b952-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b952-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0b952-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b952-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b952-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b952-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b952-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b952-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b952-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b952-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b952-125">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="0b952-125">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 


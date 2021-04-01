---
title: Mensaje de LB_GETSEL (Winuser. h)
description: Obtiene el estado de selección de un elemento.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- LB_GETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d808935e65a1ea748c59d606aa2cf483748fb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905356"
---
# <a name="lb_getsel-message"></a><span data-ttu-id="d25f8-104">\_Mensaje lb GETSEL</span><span class="sxs-lookup"><span data-stu-id="d25f8-104">LB\_GETSEL message</span></span>

<span data-ttu-id="d25f8-105">Obtiene el estado de selección de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d25f8-105">Gets the selection state of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="d25f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d25f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d25f8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d25f8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d25f8-108">El índice de base cero de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d25f8-108">The zero-based index of the item.</span></span>

<span data-ttu-id="d25f8-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d25f8-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="d25f8-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="d25f8-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="d25f8-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="d25f8-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="d25f8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d25f8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d25f8-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d25f8-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d25f8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d25f8-114">Return value</span></span>

<span data-ttu-id="d25f8-115">Si se selecciona un elemento, el valor devuelto es mayor que cero; de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="d25f8-115">If an item is selected, the return value is greater than zero; otherwise, it is zero.</span></span> <span data-ttu-id="d25f8-116">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d25f8-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="d25f8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d25f8-117">Requirements</span></span>



| <span data-ttu-id="d25f8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d25f8-118">Requirement</span></span> | <span data-ttu-id="d25f8-119">Value</span><span class="sxs-lookup"><span data-stu-id="d25f8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d25f8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d25f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d25f8-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d25f8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d25f8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d25f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d25f8-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d25f8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d25f8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d25f8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d25f8-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d25f8-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d25f8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d25f8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25f8-127">**LB \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="d25f8-127">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 






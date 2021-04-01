---
title: Mensaje de LB_SELITEMRANGEEX (Winuser. h)
description: Selecciona uno o más elementos consecutivos en un cuadro de lista de selección múltiple.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996923"
---
# <a name="lb_selitemrangeex-message"></a><span data-ttu-id="34bf9-104">\_Mensaje lb SELITEMRANGEEX</span><span class="sxs-lookup"><span data-stu-id="34bf9-104">LB\_SELITEMRANGEEX message</span></span>

<span data-ttu-id="34bf9-105">Selecciona uno o más elementos consecutivos en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="34bf9-105">Selects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="34bf9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34bf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34bf9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34bf9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34bf9-108">Especifica el índice de base cero del primer elemento que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="34bf9-108">Specifies the zero-based index of the first item to select.</span></span>

<span data-ttu-id="34bf9-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="34bf9-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="34bf9-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="34bf9-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="34bf9-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="34bf9-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="34bf9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34bf9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34bf9-113">Especifica el índice de base cero del último elemento que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="34bf9-113">Specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34bf9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34bf9-114">Return value</span></span>

<span data-ttu-id="34bf9-115">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="34bf9-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="34bf9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34bf9-116">Remarks</span></span>

<span data-ttu-id="34bf9-117">Si el parámetro *wParam* es menor que el parámetro *lParam* , se selecciona el intervalo de elementos especificado.</span><span class="sxs-lookup"><span data-stu-id="34bf9-117">If the *wParam* parameter is less than the *lParam* parameter, the specified range of items is selected.</span></span> <span data-ttu-id="34bf9-118">Si *wParam* es mayor o igual que *lParam*, el intervalo se quita del intervalo de elementos especificado.</span><span class="sxs-lookup"><span data-stu-id="34bf9-118">If *wParam* is greater than or equal to *lParam*, the range is removed from the specified range of items.</span></span> <span data-ttu-id="34bf9-119">Para seleccionar solo un elemento, seleccione dos elementos y, a continuación, anule la selección del elemento no deseado.</span><span class="sxs-lookup"><span data-stu-id="34bf9-119">To select only one item, select two items and then deselect the unwanted item.</span></span>

<span data-ttu-id="34bf9-120">Use este mensaje solo con cuadros de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="34bf9-120">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="34bf9-121">Este mensaje puede seleccionar un intervalo solo dentro de los primeros 65.536 elementos.</span><span class="sxs-lookup"><span data-stu-id="34bf9-121">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="34bf9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34bf9-122">Requirements</span></span>



| <span data-ttu-id="34bf9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="34bf9-123">Requirement</span></span> | <span data-ttu-id="34bf9-124">Value</span><span class="sxs-lookup"><span data-stu-id="34bf9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34bf9-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34bf9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="34bf9-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="34bf9-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="34bf9-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34bf9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="34bf9-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="34bf9-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="34bf9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34bf9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="34bf9-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34bf9-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34bf9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="34bf9-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="34bf9-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="34bf9-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="34bf9-133">**LB \_ SELITEMRANGE**</span><span class="sxs-lookup"><span data-stu-id="34bf9-133">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> <dt>

[<span data-ttu-id="34bf9-134">**LB \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="34bf9-134">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 






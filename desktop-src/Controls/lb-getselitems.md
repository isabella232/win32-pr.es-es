---
title: Mensaje de LB_GETSELITEMS (Winuser. h)
description: Rellena un búfer con una matriz de enteros que especifican el número de elemento de los elementos seleccionados en un cuadro de lista de selección múltiple.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996466"
---
# <a name="lb_getselitems-message"></a><span data-ttu-id="e7ee0-104">\_Mensaje lb GETSELITEMS</span><span class="sxs-lookup"><span data-stu-id="e7ee0-104">LB\_GETSELITEMS message</span></span>

<span data-ttu-id="e7ee0-105">Rellena un búfer con una matriz de enteros que especifican el número de elemento de los elementos seleccionados en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-105">Fills a buffer with an array of integers that specify the item numbers of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7ee0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7ee0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7ee0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7ee0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7ee0-108">Número máximo de elementos seleccionados cuyos números de elemento se van a colocar en el búfer.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-108">The maximum number of selected items whose item numbers are to be placed in the buffer.</span></span>

<span data-ttu-id="e7ee0-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="e7ee0-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="e7ee0-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="e7ee0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7ee0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7ee0-113">Un puntero a un búfer lo suficientemente grande como para el número de enteros especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e7ee0-113">A pointer to a buffer large enough for the number of integers specified by the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7ee0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7ee0-114">Return value</span></span>

<span data-ttu-id="e7ee0-115">El valor devuelto es el número de elementos colocados en el búfer.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-115">The return value is the number of items placed in the buffer.</span></span> <span data-ttu-id="e7ee0-116">Si el cuadro de lista es un cuadro de lista de selección única, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="e7ee0-116">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ee0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7ee0-117">Requirements</span></span>



| <span data-ttu-id="e7ee0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ee0-118">Requirement</span></span> | <span data-ttu-id="e7ee0-119">Value</span><span class="sxs-lookup"><span data-stu-id="e7ee0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ee0-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7ee0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ee0-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e7ee0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7ee0-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7ee0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ee0-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7ee0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7ee0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7ee0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7ee0-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7ee0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ee0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7ee0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ee0-127">**LB \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="e7ee0-127">**LB\_GETSELCOUNT**</span></span>](lb-getselcount.md)
</dt> </dl>

 

 






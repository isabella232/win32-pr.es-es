---
title: Mensaje de LB_SETITEMHEIGHT (Winuser. h)
description: Establece el alto, en píxeles, de los elementos de un cuadro de lista. Si el cuadro de lista tiene el \_ estilo lbs OWNERDRAWVARIABLE, este mensaje establece el alto del elemento especificado por el parámetro wParam. De lo contrario, este mensaje establece el alto de todos los elementos del cuadro de lista.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492431"
---
# <a name="lb_setitemheight-message"></a><span data-ttu-id="6d56a-106">\_Mensaje lb SETITEMHEIGHT</span><span class="sxs-lookup"><span data-stu-id="6d56a-106">LB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="6d56a-107">Establece el alto, en píxeles, de los elementos de un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="6d56a-107">Sets the height, in pixels, of items in a list box.</span></span> <span data-ttu-id="6d56a-108">Si el cuadro de lista tiene el estilo [**lbs \_ OWNERDRAWVARIABLE**](list-box-styles.md) , este mensaje establece el alto del elemento especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="6d56a-108">If the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style, this message sets the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="6d56a-109">De lo contrario, este mensaje establece el alto de todos los elementos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="6d56a-109">Otherwise, this message sets the height of all items in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d56a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d56a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d56a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d56a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d56a-112">Especifica el índice de base cero del elemento en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="6d56a-112">Specifies the zero-based index of the item in the list box.</span></span> <span data-ttu-id="6d56a-113">Use este parámetro solo si el cuadro de lista tiene el estilo [**lbs \_ OWNERDRAWVARIABLE**](list-box-styles.md) ; de lo contrario, establézcalo en cero.</span><span class="sxs-lookup"><span data-stu-id="6d56a-113">Use this parameter only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, set it to zero.</span></span>

<span data-ttu-id="6d56a-114">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6d56a-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="6d56a-115">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="6d56a-115">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="6d56a-116">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="6d56a-116">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="6d56a-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d56a-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d56a-118">Especifica el alto, en píxeles, del elemento.</span><span class="sxs-lookup"><span data-stu-id="6d56a-118">Specifies the height, in pixels, of the item.</span></span> <span data-ttu-id="6d56a-119">El alto máximo es de 255 píxeles.</span><span class="sxs-lookup"><span data-stu-id="6d56a-119">The maximum height is 255 pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d56a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d56a-120">Return value</span></span>

<span data-ttu-id="6d56a-121">Si el índice o el alto no son válidos, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6d56a-121">If the index or height is invalid, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d56a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d56a-122">Requirements</span></span>



| <span data-ttu-id="6d56a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d56a-123">Requirement</span></span> | <span data-ttu-id="6d56a-124">Value</span><span class="sxs-lookup"><span data-stu-id="6d56a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d56a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d56a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6d56a-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6d56a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6d56a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d56a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6d56a-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d56a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6d56a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d56a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d56a-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d56a-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d56a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d56a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d56a-132">**LB \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="6d56a-132">**LB\_GETITEMHEIGHT**</span></span>](lb-getitemheight.md)
</dt> </dl>

 

 






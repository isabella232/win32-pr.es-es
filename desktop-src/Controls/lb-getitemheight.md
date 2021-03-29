---
title: Mensaje de LB_GETITEMHEIGHT (Winuser. h)
description: Obtiene el alto de los elementos de un cuadro de lista.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- LB_GETITEMHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905174"
---
# <a name="lb_getitemheight-message"></a><span data-ttu-id="35800-104">\_Mensaje lb GETITEMHEIGHT</span><span class="sxs-lookup"><span data-stu-id="35800-104">LB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="35800-105">Obtiene el alto de los elementos de un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="35800-105">Gets the height of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="35800-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35800-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35800-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35800-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35800-108">Índice de base cero del elemento de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="35800-108">The zero-based index of the list box item.</span></span> <span data-ttu-id="35800-109">Este índice solo se utiliza si el cuadro de lista tiene el estilo [**lbs \_ OWNERDRAWVARIABLE**](list-box-styles.md) ; de lo contrario, debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="35800-109">This index is used only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, it must be zero.</span></span>

<span data-ttu-id="35800-110">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="35800-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="35800-111">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="35800-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="35800-112">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="35800-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="35800-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35800-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35800-114">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="35800-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35800-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35800-115">Return value</span></span>

<span data-ttu-id="35800-116">El valor devuelto es el alto, en píxeles, de cada elemento del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="35800-116">The return value is the height, in pixels, of each item in the list box.</span></span> <span data-ttu-id="35800-117">El valor devuelto es el alto del elemento especificado por el parámetro *wParam* si el cuadro de lista tiene el estilo [**lbs \_ OWNERDRAWVARIABLE**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="35800-117">The return value is the height of the item specified by the *wParam* parameter if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style.</span></span> <span data-ttu-id="35800-118">El valor devuelto es LB \_ Err si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="35800-118">The return value is LB\_ERR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="35800-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35800-119">Requirements</span></span>



| <span data-ttu-id="35800-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="35800-120">Requirement</span></span> | <span data-ttu-id="35800-121">Value</span><span class="sxs-lookup"><span data-stu-id="35800-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35800-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35800-122">Minimum supported client</span></span><br/> | <span data-ttu-id="35800-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="35800-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="35800-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35800-124">Minimum supported server</span></span><br/> | <span data-ttu-id="35800-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="35800-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35800-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35800-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="35800-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35800-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35800-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="35800-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35800-129">**LB \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="35800-129">**LB\_SETITEMHEIGHT**</span></span>](lb-setitemheight.md)
</dt> </dl>

 

 






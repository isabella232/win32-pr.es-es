---
title: Mensaje de LB_SETCOUNT (Winuser. h)
description: Establece el recuento de elementos de un cuadro de lista creado con el \_ estilo lbs NoData y no se creó con el \_ estilo lb HASSTRINGS.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079657"
---
# <a name="lb_setcount-message"></a><span data-ttu-id="741d5-104">\_Mensaje lb SETCOUNT</span><span class="sxs-lookup"><span data-stu-id="741d5-104">LB\_SETCOUNT message</span></span>

<span data-ttu-id="741d5-105">Establece el recuento de elementos de un cuadro de lista creado con el estilo [**lbs \_ NoData**](list-box-styles.md) y no se creó con el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="741d5-105">Sets the count of items in a list box created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="741d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="741d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="741d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="741d5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="741d5-108">Especifica el nuevo recuento de elementos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="741d5-108">Specifies the new count of items in the list box.</span></span>

<span data-ttu-id="741d5-109">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="741d5-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="741d5-110">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="741d5-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="741d5-111">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="741d5-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="741d5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="741d5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="741d5-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="741d5-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="741d5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="741d5-114">Return value</span></span>

<span data-ttu-id="741d5-115">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="741d5-115">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="741d5-116">Si no hay memoria suficiente para almacenar los elementos, el valor devuelto es LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="741d5-116">If there is insufficient memory to store the items, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="741d5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="741d5-117">Remarks</span></span>

<span data-ttu-id="741d5-118">El mensaje **lb \_ SETCOUNT** solo se admite en los cuadros de lista creados con el estilo [**lbs \_ NoData**](list-box-styles.md) y no se crean con el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="741d5-118">The **LB\_SETCOUNT** message is supported only by list boxes created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span> <span data-ttu-id="741d5-119">El resto de los cuadros de lista devuelven LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="741d5-119">All other list boxes return LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="741d5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="741d5-120">Requirements</span></span>



| <span data-ttu-id="741d5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="741d5-121">Requirement</span></span> | <span data-ttu-id="741d5-122">Value</span><span class="sxs-lookup"><span data-stu-id="741d5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="741d5-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="741d5-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="741d5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="741d5-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="741d5-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="741d5-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="741d5-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="741d5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="741d5-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="741d5-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="741d5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="741d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741d5-130">**LB \_ GETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="741d5-130">**LB\_GETCOUNT**</span></span>](lb-getcount.md)
</dt> </dl>

 

 






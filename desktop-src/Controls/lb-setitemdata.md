---
title: Mensaje de LB_SETITEMDATA (Winuser. h)
description: Establece un valor asociado al elemento especificado en un cuadro de lista.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- LB_SETITEMDATA controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150903"
---
# <a name="lb_setitemdata-message"></a><span data-ttu-id="070ef-104">\_Mensaje lb SETITEMDATA</span><span class="sxs-lookup"><span data-stu-id="070ef-104">LB\_SETITEMDATA message</span></span>

<span data-ttu-id="070ef-105">Establece un valor asociado al elemento especificado en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="070ef-105">Sets a value associated with the specified item in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="070ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="070ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="070ef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="070ef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="070ef-108">Especifica el índice de base cero del elemento.</span><span class="sxs-lookup"><span data-stu-id="070ef-108">Specifies the zero-based index of the item.</span></span> <span data-ttu-id="070ef-109">Si este valor es-1, el valor *lParam* se aplica a todos los elementos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="070ef-109">If this value is -1, the *lParam* value applies to all items in the list box.</span></span>

<span data-ttu-id="070ef-110">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="070ef-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="070ef-111">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="070ef-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="070ef-112">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="070ef-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="070ef-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="070ef-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="070ef-114">Especifica el valor que se va a asociar al elemento.</span><span class="sxs-lookup"><span data-stu-id="070ef-114">Specifies the value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="070ef-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="070ef-115">Return value</span></span>

<span data-ttu-id="070ef-116">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="070ef-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="070ef-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="070ef-117">Remarks</span></span>

<span data-ttu-id="070ef-118">Si el elemento está en un cuadro de lista dibujado por el propietario creado sin el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) , este mensaje reemplaza el valor contenido en el parámetro *lParam* del mensaje [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) que agregó el elemento al cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="070ef-118">If the item is in an owner-drawn list box created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this message replaces the value contained in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="070ef-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="070ef-119">Requirements</span></span>



| <span data-ttu-id="070ef-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="070ef-120">Requirement</span></span> | <span data-ttu-id="070ef-121">Value</span><span class="sxs-lookup"><span data-stu-id="070ef-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070ef-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="070ef-122">Minimum supported client</span></span><br/> | <span data-ttu-id="070ef-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="070ef-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="070ef-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="070ef-124">Minimum supported server</span></span><br/> | <span data-ttu-id="070ef-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="070ef-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="070ef-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="070ef-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="070ef-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="070ef-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="070ef-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="070ef-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="070ef-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="070ef-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="070ef-130">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="070ef-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="070ef-131">**LB \_ GETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="070ef-131">**LB\_GETITEMDATA**</span></span>](lb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="070ef-132">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="070ef-132">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 






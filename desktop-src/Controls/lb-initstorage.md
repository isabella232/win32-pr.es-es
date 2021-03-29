---
title: Mensaje de LB_INITSTORAGE (Winuser. h)
description: Asigna memoria para almacenar los elementos del cuadro de lista. Este mensaje se usa antes de que una aplicación agregue un gran número de elementos a un cuadro de lista.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- LB_INITSTORAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490708"
---
# <a name="lb_initstorage-message"></a><span data-ttu-id="ffd08-105">\_Mensaje lb INITSTORAGE</span><span class="sxs-lookup"><span data-stu-id="ffd08-105">LB\_INITSTORAGE message</span></span>

<span data-ttu-id="ffd08-106">Asigna memoria para almacenar los elementos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="ffd08-106">Allocates memory for storing list box items.</span></span> <span data-ttu-id="ffd08-107">Este mensaje se usa antes de que una aplicación agregue un gran número de elementos a un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="ffd08-107">This message is used before an application adds a large number of items to a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="ffd08-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffd08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd08-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ffd08-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffd08-110">Número de elementos que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="ffd08-110">The number of items to add.</span></span>

<span data-ttu-id="ffd08-111">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ffd08-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="ffd08-112">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="ffd08-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="ffd08-113">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="ffd08-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="ffd08-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffd08-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffd08-115">Cantidad de memoria, en bytes, que se va a asignar para las cadenas de elementos.</span><span class="sxs-lookup"><span data-stu-id="ffd08-115">The amount of memory, in bytes, to allocate for item strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd08-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffd08-116">Return value</span></span>

<span data-ttu-id="ffd08-117">Si el mensaje se realiza correctamente, el valor devuelto es el número total de elementos para los que se ha asignado previamente la memoria, es decir, el número total de elementos agregados por todos los mensajes del **\_ INITSTORAGE** del error de carga correctos.</span><span class="sxs-lookup"><span data-stu-id="ffd08-117">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **LB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="ffd08-118">Si se produce un error en el mensaje, el valor devuelto es LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="ffd08-118">If the message fails, the return value is LB\_ERRSPACE.</span></span>

<span data-ttu-id="ffd08-119">Microsoft Windows NT 4,0: este mensaje no asigna la cantidad de memoria especificada; sin embargo, siempre devuelve el valor especificado en el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="ffd08-119">Microsoft Windows NT 4.0 : This message does not allocate the specified amount of memory; however, it always returns the value specified in the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd08-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffd08-120">Remarks</span></span>

<span data-ttu-id="ffd08-121">El mensaje **lb \_ INITSTORAGE** ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100).</span><span class="sxs-lookup"><span data-stu-id="ffd08-121">The **LB\_INITSTORAGE** message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="ffd08-122">Reserva la cantidad de memoria especificada de modo que los mensajes de [**lb \_ ADDSTRING**](lb-addstring.md), [**lb \_ INSERTSTRING**](lb-insertstring.md), [**lb \_ dir**](lb-dir.md)y [**lb \_ ADDFILE**](lb-addfile.md) posteriores tarden el menor tiempo posible.</span><span class="sxs-lookup"><span data-stu-id="ffd08-122">It reserves the specified amount of memory so that subsequent [**LB\_ADDSTRING**](lb-addstring.md), [**LB\_INSERTSTRING**](lb-insertstring.md), [**LB\_DIR**](lb-dir.md), and [**LB\_ADDFILE**](lb-addfile.md) messages take the shortest possible time.</span></span> <span data-ttu-id="ffd08-123">Puede usar estimaciones para los parámetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ffd08-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="ffd08-124">Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="ffd08-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd08-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffd08-125">Requirements</span></span>



| <span data-ttu-id="ffd08-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffd08-126">Requirement</span></span> | <span data-ttu-id="ffd08-127">Value</span><span class="sxs-lookup"><span data-stu-id="ffd08-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd08-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd08-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd08-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ffd08-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ffd08-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd08-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd08-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ffd08-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ffd08-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffd08-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd08-133"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffd08-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffd08-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffd08-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="ffd08-135">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ffd08-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ffd08-136">**LB \_ ADDFILE**</span><span class="sxs-lookup"><span data-stu-id="ffd08-136">**LB\_ADDFILE**</span></span>](lb-addfile.md)
</dt> <dt>

[<span data-ttu-id="ffd08-137">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="ffd08-137">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="ffd08-138">**DIR de LB \_**</span><span class="sxs-lookup"><span data-stu-id="ffd08-138">**LB\_DIR**</span></span>](lb-dir.md)
</dt> <dt>

[<span data-ttu-id="ffd08-139">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="ffd08-139">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 






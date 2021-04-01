---
title: Mensaje de CB_INITSTORAGE (Winuser. h)
description: Una aplicación envía el \_ mensaje de INITSTORAGE CB antes de agregar un gran número de elementos a la parte de cuadro de lista de un cuadro combinado. Este mensaje asigna memoria para almacenar los elementos del cuadro de lista.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- CB_INITSTORAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150267"
---
# <a name="cb_initstorage-message"></a><span data-ttu-id="2a7e2-105">\_Mensaje INITSTORAGE de CB</span><span class="sxs-lookup"><span data-stu-id="2a7e2-105">CB\_INITSTORAGE message</span></span>

<span data-ttu-id="2a7e2-106">Una aplicación envía el mensaje de **\_ INITSTORAGE CB** antes de agregar un gran número de elementos a la parte de cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="2a7e2-106">An application sends the **CB\_INITSTORAGE** message before adding a large number of items to the list box portion of a combo box.</span></span> <span data-ttu-id="2a7e2-107">Este mensaje asigna memoria para almacenar los elementos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="2a7e2-107">This message allocates memory for storing list box items.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a7e2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a7e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a7e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a7e2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a7e2-110">Número de elementos que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="2a7e2-110">The number of items to add.</span></span>

</dd> <dt>

<span data-ttu-id="2a7e2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a7e2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a7e2-112">Cantidad de memoria que se va a asignar para las cadenas de elementos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2a7e2-112">The amount of memory to allocate for item strings, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a7e2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a7e2-113">Return value</span></span>

<span data-ttu-id="2a7e2-114">Si el mensaje se realiza correctamente, el valor devuelto es el número total de elementos para los que se ha asignado previamente la memoria, es decir, el número total de elementos agregados por todos los mensajes del **\_ INITSTORAGE** del elemento CB correctos.</span><span class="sxs-lookup"><span data-stu-id="2a7e2-114">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **CB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="2a7e2-115">Si se produce un error en el mensaje, el valor devuelto es CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="2a7e2-115">If the message fails, the return value is CB\_ERRSPACE.</span></span>

<span data-ttu-id="2a7e2-116">El mensaje asigna memoria y devuelve los valores correctos y de error descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2a7e2-116">The message allocates memory and returns the success and error values described above.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a7e2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a7e2-117">Remarks</span></span>

<span data-ttu-id="2a7e2-118">El mensaje de **\_ INITSTORAGE de CB** ayuda a acelerar la inicialización de los cuadros combinados que tienen un gran número de elementos (más de 100).</span><span class="sxs-lookup"><span data-stu-id="2a7e2-118">The **CB\_INITSTORAGE** message helps speed up the initialization of combo boxes that have a large number of items (over 100).</span></span> <span data-ttu-id="2a7e2-119">Reserva la cantidad de memoria especificada para que los mensajes de la [**\_ dir**](cb-dir.md) [**CB \_ ADDSTRING**](cb-addstring.md), [**CB \_ INSERTSTRING**](cb-insertstring.md)y CB posteriores tarden el menor tiempo posible.</span><span class="sxs-lookup"><span data-stu-id="2a7e2-119">It reserves the specified amount of memory so that subsequent [**CB\_ADDSTRING**](cb-addstring.md), [**CB\_INSERTSTRING**](cb-insertstring.md), and [**CB\_DIR**](cb-dir.md) messages take the shortest possible time.</span></span> <span data-ttu-id="2a7e2-120">Puede usar estimaciones para los parámetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="2a7e2-120">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="2a7e2-121">Si sobrestima, se asigna la memoria adicional, si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="2a7e2-121">If you overestimate, the extra memory is allocated, if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a7e2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a7e2-122">Requirements</span></span>



| <span data-ttu-id="2a7e2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a7e2-123">Requirement</span></span> | <span data-ttu-id="2a7e2-124">Value</span><span class="sxs-lookup"><span data-stu-id="2a7e2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7e2-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a7e2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2a7e2-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2a7e2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2a7e2-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a7e2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2a7e2-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a7e2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a7e2-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a7e2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a7e2-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a7e2-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a7e2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a7e2-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a7e2-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2a7e2-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2a7e2-133">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="2a7e2-133">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="2a7e2-134">**\_directorio CB**</span><span class="sxs-lookup"><span data-stu-id="2a7e2-134">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="2a7e2-135">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="2a7e2-135">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 






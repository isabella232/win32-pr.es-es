---
title: Mensaje de LB_INSERTSTRING (Winuser. h)
description: Inserta una cadena o datos de elemento en un cuadro de lista. A diferencia del mensaje de LB \_ en lb, el \_ mensaje lb INSERTSTRING no hace que se ordene una lista con el \_ estilo de ordenación lbs.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- LB_INSERTSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150907"
---
# <a name="lb_insertstring-message"></a><span data-ttu-id="ce4a8-105">\_Mensaje lb INSERTSTRING</span><span class="sxs-lookup"><span data-stu-id="ce4a8-105">LB\_INSERTSTRING message</span></span>

<span data-ttu-id="ce4a8-106">Inserta una cadena o datos de elemento en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-106">Inserts a string or item data into a list box.</span></span> <span data-ttu-id="ce4a8-107">A diferencia del mensaje de [**lb en lb \_**](lb-addstring.md) , el mensaje **lb \_ INSERTSTRING** no hace que se ordene una lista con el estilo de [**\_ ordenación lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ce4a8-107">Unlike the [**LB\_ADDSTRING**](lb-addstring.md) message, the **LB\_INSERTSTRING** message does not cause a list with the [**LBS\_SORT**](list-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce4a8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce4a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce4a8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce4a8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4a8-110">Índice de base cero de la posición en la que se va a insertar la cadena.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="ce4a8-111">Si este parámetro es-1, la cadena se agrega al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="ce4a8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce4a8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4a8-113">Puntero a la cadena terminada en null que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="ce4a8-114">Si el cuadro de lista tiene un estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , este parámetro se almacena como datos de elemento en lugar de una cadena.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="ce4a8-115">Puede enviar los mensajes [**lb \_ GETITEMDATA**](lb-getitemdata.md) y [**lb \_ SETITEMDATA**](lb-setitemdata.md) para recuperar o modificar los datos del elemento.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-115">You can send the [**LB\_GETITEMDATA**](lb-getitemdata.md) and [**LB\_SETITEMDATA**](lb-setitemdata.md) messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce4a8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce4a8-116">Return value</span></span>

<span data-ttu-id="ce4a8-117">El valor devuelto es el índice de la posición en la que se insertó la cadena.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-117">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="ce4a8-118">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="ce4a8-119">Si no hay suficiente espacio para almacenar la nueva cadena, el valor devuelto es LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-119">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce4a8-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce4a8-120">Remarks</span></span>

<span data-ttu-id="ce4a8-121">El mensaje [**lb \_ INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100).</span><span class="sxs-lookup"><span data-stu-id="ce4a8-121">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="ce4a8-122">Reserva la cantidad de memoria especificada para que los mensajes de **lb \_ INSERTSTRING** posteriores tarden el menor tiempo posible.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-122">It reserves the specified amount of memory so that subsequent **LB\_INSERTSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="ce4a8-123">Puede usar estimaciones para los parámetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ce4a8-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="ce4a8-124">Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="ce4a8-125">Si el cuadro de lista tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e inserta una cadena más ancha que el cuadro de lista, envíe un mensaje [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparezca la barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-125">If the list box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="ce4a8-126">En el caso de una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-126">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="ce4a8-127">Esto puede causar problemas.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-127">This can cause problems.</span></span> <span data-ttu-id="ce4a8-128">Por ejemplo, los caracteres romanos acentuados en un cuadro de lista no Unicode en las ventanas japonesas se desactivarán.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-128">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="ce4a8-129">Para solucionar este error, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="ce4a8-129">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4a8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce4a8-130">Requirements</span></span>



| <span data-ttu-id="ce4a8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce4a8-131">Requirement</span></span> | <span data-ttu-id="ce4a8-132">Value</span><span class="sxs-lookup"><span data-stu-id="ce4a8-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4a8-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce4a8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ce4a8-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ce4a8-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ce4a8-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce4a8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ce4a8-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce4a8-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ce4a8-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce4a8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce4a8-138"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce4a8-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce4a8-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce4a8-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce4a8-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ce4a8-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ce4a8-141">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="ce4a8-141">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="ce4a8-142">**LB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="ce4a8-142">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="ce4a8-143">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="ce4a8-143">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 


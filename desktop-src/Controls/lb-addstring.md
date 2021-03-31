---
title: Mensaje de LB_ADDSTRING (Winuser. h)
description: Agrega una cadena a un cuadro de lista. Si el cuadro de lista no tiene el \_ estilo de ordenación lbs, la cadena se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista está ordenada.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079305"
---
# <a name="lb_addstring-message"></a><span data-ttu-id="1fb38-106">Mensaje de LB \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="1fb38-106">LB\_ADDSTRING message</span></span>

<span data-ttu-id="1fb38-107">Agrega una cadena a un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="1fb38-107">Adds a string to a list box.</span></span> <span data-ttu-id="1fb38-108">Si el cuadro de lista no tiene el estilo de [**\_ ordenación lbs**](list-box-styles.md) , la cadena se agrega al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="1fb38-108">If the list box does not have the [**LBS\_SORT**](list-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="1fb38-109">De lo contrario, la cadena se inserta en la lista y la lista está ordenada.</span><span class="sxs-lookup"><span data-stu-id="1fb38-109">Otherwise, the string is inserted into the list and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="1fb38-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fb38-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fb38-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1fb38-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fb38-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1fb38-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fb38-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fb38-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fb38-114">Puntero a la cadena terminada en null que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="1fb38-114">A pointer to the null-terminated string that is to be added.</span></span>

<span data-ttu-id="1fb38-115">Si el cuadro de lista tiene un estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , este parámetro se almacena como datos de elemento en lugar de una cadena.</span><span class="sxs-lookup"><span data-stu-id="1fb38-115">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="1fb38-116">Puede enviar los mensajes **lb \_ GETITEMDATA** y **lb \_ SETITEMDATA** para recuperar o modificar los datos del elemento.</span><span class="sxs-lookup"><span data-stu-id="1fb38-116">You can send the **LB\_GETITEMDATA** and **LB\_SETITEMDATA** messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fb38-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fb38-117">Return value</span></span>

<span data-ttu-id="1fb38-118">El valor devuelto es el índice de base cero de la cadena en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="1fb38-118">The return value is the zero-based index of the string in the list box.</span></span> <span data-ttu-id="1fb38-119">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="1fb38-119">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="1fb38-120">Si no hay suficiente espacio para almacenar la nueva cadena, el valor devuelto es LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="1fb38-120">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fb38-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fb38-121">Remarks</span></span>

<span data-ttu-id="1fb38-122">Si el cuadro de lista tiene un estilo dibujado por el propietario y el estilo de [**\_ ordenación lbs**](list-box-styles.md) , pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , el sistema envía el mensaje [**\_ COMPAREITEM de WM**](wm-compareitem.md) una o varias veces al propietario del cuadro de lista para colocar el nuevo elemento correctamente en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="1fb38-122">If the list box has an owner-drawn style and the [**LBS\_SORT**](list-box-styles.md) style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends the [**WM\_COMPAREITEM**](wm-compareitem.md) message one or more times to the owner of the list box to place the new item properly in the list box.</span></span>

<span data-ttu-id="1fb38-123">El mensaje [**lb \_ INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100).</span><span class="sxs-lookup"><span data-stu-id="1fb38-123">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="1fb38-124">Reserva la cantidad de memoria especificada para que los mensajes de **lb \_ ADDSTRING** posteriores tarden el menor tiempo posible.</span><span class="sxs-lookup"><span data-stu-id="1fb38-124">It reserves the specified amount of memory so that subsequent **LB\_ADDSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="1fb38-125">Puede usar estimaciones para los parámetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1fb38-125">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="1fb38-126">Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="1fb38-126">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="1fb38-127">Si el cuadro de lista tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) y agrega una cadena más ancha que el cuadro de lista, envíe un mensaje [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparezca la barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="1fb38-127">If the list box has the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="1fb38-128">En el caso de una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="1fb38-128">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="1fb38-129">Esto puede causar problemas.</span><span class="sxs-lookup"><span data-stu-id="1fb38-129">This can cause problems.</span></span> <span data-ttu-id="1fb38-130">Por ejemplo, los caracteres romanos acentuados en un cuadro de lista no Unicode en las ventanas japonesas se desactivarán.</span><span class="sxs-lookup"><span data-stu-id="1fb38-130">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="1fb38-131">Para solucionar este error, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="1fb38-131">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb38-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fb38-132">Requirements</span></span>



| <span data-ttu-id="1fb38-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb38-133">Requirement</span></span> | <span data-ttu-id="1fb38-134">Value</span><span class="sxs-lookup"><span data-stu-id="1fb38-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb38-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fb38-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb38-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1fb38-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1fb38-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fb38-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb38-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fb38-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1fb38-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fb38-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fb38-140"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fb38-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb38-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fb38-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="1fb38-142">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1fb38-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1fb38-143">**LB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="1fb38-143">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="1fb38-144">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="1fb38-144">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="1fb38-145">**LB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="1fb38-145">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="1fb38-146">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="1fb38-146">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="1fb38-147">**COMPAREITEM de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1fb38-147">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 


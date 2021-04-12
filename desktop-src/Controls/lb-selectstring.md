---
title: Mensaje de LB_SELECTSTRING (Winuser. h)
description: Busca un elemento que empiece con los caracteres de una cadena especificada en un cuadro de lista. Si se encuentra un elemento coincidente, se selecciona el elemento.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- LB_SELECTSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492442"
---
# <a name="lb_selectstring-message"></a><span data-ttu-id="5ac4c-105">\_Mensaje lb SELECTSTRING</span><span class="sxs-lookup"><span data-stu-id="5ac4c-105">LB\_SELECTSTRING message</span></span>

<span data-ttu-id="5ac4c-106">Busca un elemento que empiece con los caracteres de una cadena especificada en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-106">Searches a list box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="5ac4c-107">Si se encuentra un elemento coincidente, se selecciona el elemento.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-107">If a matching item is found, the item is selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ac4c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ac4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac4c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ac4c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac4c-110">Índice de base cero del elemento situado delante del primer elemento que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-110">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="5ac4c-111">Cuando la búsqueda alcanza la parte inferior del cuadro de lista, continúa desde la parte superior del cuadro de lista hasta el elemento especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="5ac4c-111">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="5ac4c-112">Si *wParam* es-1, se busca en el cuadro de lista completo desde el principio.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-112">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="5ac4c-113">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="5ac4c-114">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-114">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="5ac4c-115">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-115">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="5ac4c-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ac4c-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac4c-117">Puntero a la cadena terminada en null que contiene el prefijo que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-117">A pointer to the null-terminated string that contains the prefix for which to search.</span></span> <span data-ttu-id="5ac4c-118">La búsqueda es independiente de las mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-118">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac4c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ac4c-119">Return value</span></span>

<span data-ttu-id="5ac4c-120">Si la búsqueda se realiza correctamente, el valor devuelto es el índice del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-120">If the search is successful, the return value is the index of the selected item.</span></span> <span data-ttu-id="5ac4c-121">Si no se realiza la búsqueda, el valor devuelto es LB \_ Err y no se cambia la selección actual.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-121">If the search is unsuccessful, the return value is LB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac4c-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ac4c-122">Remarks</span></span>

<span data-ttu-id="5ac4c-123">Si es necesario, el cuadro de lista se desplaza para que el elemento seleccionado se muestre en la vista.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-123">The list box is scrolled, if necessary, to bring the selected item into view.</span></span>

<span data-ttu-id="5ac4c-124">No use este mensaje con un cuadro de lista que tenga los estilos [**lb \_ MULTIPLESEL**](list-box-styles.md) o [**lb \_ EXTENDEDSEL**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5ac4c-124">Do not use this message with a list box that has the [**LBS\_MULTIPLESEL**](list-box-styles.md) or the [**LBS\_EXTENDEDSEL**](list-box-styles.md) styles.</span></span>

<span data-ttu-id="5ac4c-125">Un elemento se selecciona solo si sus caracteres iniciales del punto inicial coinciden con los caracteres de la cadena especificada por el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5ac4c-125">An item is selected only if its initial characters from the starting point match the characters in the string specified by the *lParam* parameter.</span></span>

<span data-ttu-id="5ac4c-126">Si el cuadro de lista tiene el estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , la acción realizada por **lb \_ SELECTSTRING** dependerá de si se usa el estilo de [**\_ ordenación lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5ac4c-126">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_SELECTSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="5ac4c-127">Si se usa la **\_ ordenación lb** , el sistema envía mensajes de [**WM \_ COMPAREITEM**](wm-compareitem.md) al propietario del cuadro de lista para determinar qué elemento coincide con la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="5ac4c-127">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="5ac4c-128">De lo contrario, **lb \_ SELECTSTRING** intenta encontrar un elemento que tiene un valor Long (proporcionado como el parámetro *lParam* del [**mensaje \_ lb**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) que coincide con el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5ac4c-128">Otherwise, **LB\_SELECTSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac4c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ac4c-129">Requirements</span></span>



| <span data-ttu-id="5ac4c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac4c-130">Requirement</span></span> | <span data-ttu-id="5ac4c-131">Value</span><span class="sxs-lookup"><span data-stu-id="5ac4c-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac4c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ac4c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac4c-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5ac4c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ac4c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ac4c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac4c-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ac4c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ac4c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ac4c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac4c-137"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4c-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac4c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ac4c-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ac4c-139">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5ac4c-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ac4c-140">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="5ac4c-140">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="5ac4c-141">**LB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="5ac4c-141">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> <dt>

[<span data-ttu-id="5ac4c-142">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="5ac4c-142">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 






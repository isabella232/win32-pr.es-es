---
title: Mensaje de LB_FINDSTRINGEXACT (Winuser. h)
description: Busca la primera cadena del cuadro de lista que coincide exactamente con la cadena especificada, salvo que la búsqueda no distingue entre mayúsculas y minúsculas.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- LB_FINDSTRINGEXACT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079720"
---
# <a name="lb_findstringexact-message"></a><span data-ttu-id="c2013-104">\_Mensaje lb FindExactString con</span><span class="sxs-lookup"><span data-stu-id="c2013-104">LB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="c2013-105">Busca la primera cadena del cuadro de lista que coincide exactamente con la cadena especificada, salvo que la búsqueda no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c2013-105">Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2013-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2013-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2013-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2013-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2013-108">Índice de base cero del elemento situado delante del primer elemento que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="c2013-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="c2013-109">Cuando la búsqueda alcanza la parte inferior del cuadro de lista, continúa realizando una búsqueda desde la parte superior del cuadro de lista hasta el elemento especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="c2013-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="c2013-110">Si *wParam* es-1, se busca en el cuadro de lista completo desde el principio.</span><span class="sxs-lookup"><span data-stu-id="c2013-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="c2013-111">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c2013-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="c2013-112">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="c2013-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="c2013-113">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="c2013-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="c2013-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2013-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2013-115">Puntero a la cadena terminada en null que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="c2013-115">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="c2013-116">La búsqueda no distingue entre mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c2013-116">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2013-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2013-117">Return value</span></span>

<span data-ttu-id="c2013-118">El valor devuelto es el índice de base cero del elemento coincidente, o LB \_ Err si la búsqueda no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c2013-118">The return value is the zero-based index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2013-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2013-119">Remarks</span></span>

<span data-ttu-id="c2013-120">Esta función solo se realiza correctamente si la cadena especificada y un elemento de cuadro de lista tienen la misma longitud (excepto el valor null al final de la cadena especificada) y tienen exactamente los mismos caracteres.</span><span class="sxs-lookup"><span data-stu-id="c2013-120">This function is only successful if the specified string and a list box item have the same length (except for the null at the end of the specified string) and have exactly the same characters.</span></span>

<span data-ttu-id="c2013-121">Si el cuadro de lista tiene el estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , la acción realizada por **lb \_ FindExactString con** dependerá de si se usa el estilo de [**\_ ordenación lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c2013-121">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRINGEXACT** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="c2013-122">Si se usa la **\_ ordenación lb** , el sistema envía mensajes de [**WM \_ COMPAREITEM**](wm-compareitem.md) al propietario del cuadro de lista para determinar qué elemento coincide con la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="c2013-122">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="c2013-123">De lo contrario, **lb \_ FindExactString con** intenta encontrar un elemento que tiene un valor Long (proporcionado como el parámetro *lParam* del [**mensaje \_ lb**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) que coincide con el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c2013-123">Otherwise, **LB\_FINDSTRINGEXACT** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2013-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2013-124">Requirements</span></span>



| <span data-ttu-id="c2013-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2013-125">Requirement</span></span> | <span data-ttu-id="c2013-126">Value</span><span class="sxs-lookup"><span data-stu-id="c2013-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2013-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2013-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c2013-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c2013-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c2013-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2013-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c2013-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2013-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c2013-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2013-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2013-132"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2013-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2013-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2013-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2013-134">**LB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="c2013-134">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> </dl>

 

 






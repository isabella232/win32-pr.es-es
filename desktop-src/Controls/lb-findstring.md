---
title: Mensaje de LB_FINDSTRING (Winuser. h)
description: Busca la primera cadena de un cuadro de lista que comienza con la cadena especificada.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- LB_FINDSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b528dbafbc386af05a091f24c8c28327739f5d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492857"
---
# <a name="lb_findstring-message"></a><span data-ttu-id="4204d-104">\_Mensaje lb FINDSTRING</span><span class="sxs-lookup"><span data-stu-id="4204d-104">LB\_FINDSTRING message</span></span>

<span data-ttu-id="4204d-105">Busca la primera cadena de un cuadro de lista que comienza con la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="4204d-105">Finds the first string in a list box that begins with the specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="4204d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4204d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4204d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4204d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4204d-108">Índice de base cero del elemento situado delante del primer elemento que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="4204d-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="4204d-109">Cuando la búsqueda alcanza la parte inferior del cuadro de lista, continúa realizando una búsqueda desde la parte superior del cuadro de lista hasta el elemento especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="4204d-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="4204d-110">Si *wParam* es-1, se busca en el cuadro de lista completo desde el principio.</span><span class="sxs-lookup"><span data-stu-id="4204d-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="4204d-111">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4204d-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="4204d-112">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="4204d-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="4204d-113">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="4204d-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="4204d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4204d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4204d-115">Puntero a la cadena terminada en null que contiene la cadena que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="4204d-115">A pointer to the null-terminated string that contains the string for which to search.</span></span> <span data-ttu-id="4204d-116">La búsqueda es independiente de las mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4204d-116">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4204d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4204d-117">Return value</span></span>

<span data-ttu-id="4204d-118">El valor devuelto es el índice del elemento coincidente o LB \_ Err si la búsqueda no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4204d-118">The return value is the index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4204d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4204d-119">Remarks</span></span>

<span data-ttu-id="4204d-120">Si el cuadro de lista tiene el estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , la acción realizada por **lb \_ FINDSTRING** dependerá de si se usa el estilo de [**\_ ordenación lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4204d-120">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="4204d-121">Si se usa la **\_ ordenación lb** , el sistema envía mensajes de [**WM \_ COMPAREITEM**](wm-compareitem.md) al propietario del cuadro de lista para determinar qué elemento coincide con la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="4204d-121">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="4204d-122">De lo contrario, **lb \_ FINDSTRING** intenta encontrar un elemento que tiene un valor Long (proporcionado como el parámetro *lParam* del [**mensaje \_ lb**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) que coincide con el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="4204d-122">Otherwise, **LB\_FINDSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4204d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4204d-123">Requirements</span></span>



| <span data-ttu-id="4204d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4204d-124">Requirement</span></span> | <span data-ttu-id="4204d-125">Value</span><span class="sxs-lookup"><span data-stu-id="4204d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4204d-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4204d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4204d-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4204d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4204d-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4204d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4204d-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4204d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4204d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4204d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4204d-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4204d-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4204d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4204d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4204d-133">**LB \_ FindExactString con**</span><span class="sxs-lookup"><span data-stu-id="4204d-133">**LB\_FINDSTRINGEXACT**</span></span>](lb-findstringexact.md)
</dt> </dl>

 

 






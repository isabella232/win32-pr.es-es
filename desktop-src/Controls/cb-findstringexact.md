---
title: CB_FINDSTRINGEXACT mensaje (Winuser.h)
description: Busca la primera cadena de cuadro de lista en un cuadro combinado que coincide con la cadena especificada en el parámetro lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT mensaje Controles de Windows
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327180"
---
# <a name="cb_findstringexact-message"></a><span data-ttu-id="05f2e-104">Mensaje \_ FINDSTRINGEXACT de CB</span><span class="sxs-lookup"><span data-stu-id="05f2e-104">CB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="05f2e-105">Busca la primera cadena de cuadro de lista en un cuadro combinado que coincide con la cadena especificada en el *parámetro lParam.*</span><span class="sxs-lookup"><span data-stu-id="05f2e-105">Finds the first list box string in a combo box that matches the string specified in the *lParam* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="05f2e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05f2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f2e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05f2e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05f2e-108">Índice de base cero del elemento que precede al primer elemento en el que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="05f2e-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="05f2e-109">Cuando la búsqueda llega a la parte inferior del cuadro de lista, continúa desde la parte superior del cuadro de lista hasta el elemento especificado por el *parámetro wParam.*</span><span class="sxs-lookup"><span data-stu-id="05f2e-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="05f2e-110">Si *wParam es* -1, se busca todo el cuadro de lista desde el principio.</span><span class="sxs-lookup"><span data-stu-id="05f2e-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="05f2e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05f2e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05f2e-112">Puntero a la cadena terminada en NULL para la que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="05f2e-112">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="05f2e-113">La búsqueda no distingue mayúsculas de minúsculas, por lo que esta cadena puede contener cualquier combinación de letras mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="05f2e-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f2e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05f2e-114">Return value</span></span>

<span data-ttu-id="05f2e-115">El valor devuelto es el índice de base cero del elemento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="05f2e-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="05f2e-116">Si la búsqueda no se realiza correctamente, es CB \_ ERR.</span><span class="sxs-lookup"><span data-stu-id="05f2e-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="05f2e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05f2e-117">Remarks</span></span>

<span data-ttu-id="05f2e-118">Esta función se realiza correctamente solo si la cadena especificada y un elemento de cuadro combinado tienen la misma longitud (excepto el carácter nulo de terminación) y los mismos caracteres.</span><span class="sxs-lookup"><span data-stu-id="05f2e-118">This function is successful only if the specified string and a combo box item have the same length (except for the terminating null character) and the same characters.</span></span>

<span data-ttu-id="05f2e-119">Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) la funcionalidad del mensaje **\_ FINDSTRINGEXACT** de CB depende de si la aplicación usa el estilo [**CBS \_ SORT.**](combo-box-styles.md)</span><span class="sxs-lookup"><span data-stu-id="05f2e-119">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the functionality of **CB\_FINDSTRINGEXACT** message depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="05f2e-120">Si usa el estilo **\_ CBS SORT,** los mensajes [**\_ COMPAREITEM**](wm-compareitem.md) de WM se envían al propietario del cuadro combinado para determinar qué elemento coincide con la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="05f2e-120">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="05f2e-121">Si no usa el estilo SORT de **CBS, \_** el mensaje **\_ FINDSTRINGEXACT** de CB busca un elemento de lista que coincida con el valor del *parámetro lParam.*</span><span class="sxs-lookup"><span data-stu-id="05f2e-121">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRINGEXACT** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f2e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05f2e-122">Requirements</span></span>



| <span data-ttu-id="05f2e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="05f2e-123">Requirement</span></span> | <span data-ttu-id="05f2e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="05f2e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f2e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05f2e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="05f2e-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="05f2e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="05f2e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05f2e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="05f2e-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="05f2e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05f2e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05f2e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f2e-130"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="05f2e-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f2e-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="05f2e-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="05f2e-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="05f2e-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05f2e-133">**CB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="05f2e-133">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="05f2e-134">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="05f2e-134">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="05f2e-135">**COMPAREITEM de WM \_**</span><span class="sxs-lookup"><span data-stu-id="05f2e-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 






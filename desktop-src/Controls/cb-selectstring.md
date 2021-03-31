---
title: Mensaje de CB_SELECTSTRING (Winuser. h)
description: Busca un elemento que empiece con los caracteres de una cadena especificada en la lista de un cuadro combinado. Si se encuentra un elemento coincidente, se selecciona y se copia en el control de edición.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079357"
---
# <a name="cb_selectstring-message"></a><span data-ttu-id="0ee58-105">\_Mensaje SELECTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="0ee58-105">CB\_SELECTSTRING message</span></span>

<span data-ttu-id="0ee58-106">Busca un elemento que empiece con los caracteres de una cadena especificada en la lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="0ee58-106">Searches the list of a combo box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="0ee58-107">Si se encuentra un elemento coincidente, se selecciona y se copia en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="0ee58-107">If a matching item is found, it is selected and copied to the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ee58-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ee58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee58-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ee58-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ee58-110">Índice de base cero del elemento que precede al primer elemento que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="0ee58-110">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="0ee58-111">Cuando la búsqueda alcanza la parte inferior de la lista, continúa desde la parte superior de la lista hasta el elemento especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="0ee58-111">When the search reaches the bottom of the list, it continues from the top of the list back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="0ee58-112">Si *wParam* es-1, se busca en toda la lista desde el principio.</span><span class="sxs-lookup"><span data-stu-id="0ee58-112">If *wParam* is -1, the entire list is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="0ee58-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ee58-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ee58-114">Puntero a la cadena terminada en null que contiene los caracteres que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="0ee58-114">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="0ee58-115">La búsqueda no distingue entre mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0ee58-115">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee58-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ee58-116">Return value</span></span>

<span data-ttu-id="0ee58-117">Si se encuentra la cadena, el valor devuelto es el índice del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="0ee58-117">If the string is found, the return value is the index of the selected item.</span></span> <span data-ttu-id="0ee58-118">Si la búsqueda no se realiza correctamente, el valor devuelto es CB \_ Err y no se cambia la selección actual.</span><span class="sxs-lookup"><span data-stu-id="0ee58-118">If the search is unsuccessful, the return value is CB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee58-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ee58-119">Remarks</span></span>

<span data-ttu-id="0ee58-120">Solo se selecciona una cadena si los caracteres del punto inicial coinciden con los caracteres de la cadena de prefijo.</span><span class="sxs-lookup"><span data-stu-id="0ee58-120">A string is selected only if the characters from the starting point match the characters in the prefix string.</span></span>

<span data-ttu-id="0ee58-121">Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el mensaje **\_ SELECTSTRING de CB** dependerá de si usa el estilo de [**\_ ordenación CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0ee58-121">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_SELECTSTRING** message does depends on whether you use the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="0ee58-122">Si se usa el estilo de **\_ ordenación CBS** , el sistema envía mensajes de [**WM \_ COMPAREITEM**](wm-compareitem.md) al propietario del cuadro combinado para determinar qué elemento coincide con la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="0ee58-122">If the **CBS\_SORT** style is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="0ee58-123">Si no usa el estilo de **\_ ordenación CBS** , **CB \_ SELECTSTRING** intenta coincidir con el valor **DWORD** con el valor del parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="0ee58-123">If you do not use the **CBS\_SORT** style, **CB\_SELECTSTRING** attempts to match the **DWORD** value against the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee58-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ee58-124">Requirements</span></span>



| <span data-ttu-id="0ee58-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ee58-125">Requirement</span></span> | <span data-ttu-id="0ee58-126">Value</span><span class="sxs-lookup"><span data-stu-id="0ee58-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee58-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ee58-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0ee58-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0ee58-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0ee58-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ee58-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0ee58-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ee58-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0ee58-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ee58-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ee58-132"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ee58-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee58-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ee58-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="0ee58-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0ee58-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0ee58-135">**CB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="0ee58-135">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="0ee58-136">**CB \_ FindExactString con**</span><span class="sxs-lookup"><span data-stu-id="0ee58-136">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="0ee58-137">**CB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="0ee58-137">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="0ee58-138">**COMPAREITEM de WM \_**</span><span class="sxs-lookup"><span data-stu-id="0ee58-138">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 






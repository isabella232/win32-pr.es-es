---
title: Mensaje de CB_FINDSTRING (Winuser. h)
description: Busca un elemento que empiece con los caracteres de una cadena especificada en el cuadro de lista de un cuadro combinado.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- CB_FINDSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150269"
---
# <a name="cb_findstring-message"></a><span data-ttu-id="f0788-104">\_Mensaje FINDSTRING CB</span><span class="sxs-lookup"><span data-stu-id="f0788-104">CB\_FINDSTRING message</span></span>

<span data-ttu-id="f0788-105">Busca un elemento que empiece con los caracteres de una cadena especificada en el cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="f0788-105">Searches the list box of a combo box for an item beginning with the characters in a specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0788-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0788-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0788-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0788-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0788-108">Índice de base cero del elemento que precede al primer elemento que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="f0788-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="f0788-109">Cuando la búsqueda alcanza la parte inferior del cuadro de lista, continúa desde la parte superior del cuadro de lista hasta el elemento especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f0788-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="f0788-110">Si *wParam* es-1, se busca en el cuadro de lista completo desde el principio.</span><span class="sxs-lookup"><span data-stu-id="f0788-110">If *wParam* is  -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="f0788-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0788-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0788-112">Puntero a la cadena terminada en null que contiene los caracteres que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="f0788-112">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="f0788-113">La búsqueda no distingue entre mayúsculas y minúsculas, por lo que esta cadena puede contener cualquier combinación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f0788-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0788-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0788-114">Return value</span></span>

<span data-ttu-id="f0788-115">El valor devuelto es el índice de base cero del elemento coincidente.</span><span class="sxs-lookup"><span data-stu-id="f0788-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="f0788-116">Si la búsqueda no se realiza correctamente, se trata de un \_ error CB.</span><span class="sxs-lookup"><span data-stu-id="f0788-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0788-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0788-117">Remarks</span></span>

<span data-ttu-id="f0788-118">Si crea el cuadro combinado con un estilo dibujado por el propietario, pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , lo que hace el mensaje **\_ FINDSTRING de CB** depende de si la aplicación usa el estilo de [**\_ ordenación CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f0788-118">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_FINDSTRING** message does depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="f0788-119">Si usa el estilo **de \_ ordenación CBS** , los mensajes de [**WM \_ COMPAREITEM**](wm-compareitem.md) se envían al propietario del cuadro combinado para determinar qué elemento coincide con la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="f0788-119">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="f0788-120">Si no usa el estilo de **\_ ordenación CBS** , el mensaje **CB \_ FINDSTRING** busca un elemento de lista que coincida con el valor del parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f0788-120">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRING** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0788-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0788-121">Requirements</span></span>



| <span data-ttu-id="f0788-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0788-122">Requirement</span></span> | <span data-ttu-id="f0788-123">Value</span><span class="sxs-lookup"><span data-stu-id="f0788-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0788-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0788-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f0788-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f0788-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f0788-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0788-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f0788-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0788-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f0788-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0788-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0788-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0788-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0788-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0788-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="f0788-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f0788-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f0788-132">**CB \_ FindExactString con**</span><span class="sxs-lookup"><span data-stu-id="f0788-132">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="f0788-133">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="f0788-133">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="f0788-134">**CB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="f0788-134">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="f0788-135">**COMPAREITEM de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f0788-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 






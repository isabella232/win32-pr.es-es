---
title: Mensaje de CB_INSERTSTRING (Winuser. h)
description: Inserta una cadena o datos de elemento en la lista de un cuadro combinado. A diferencia del \_ mensaje CB ADDSTRING, el \_ mensaje CB INSERTSTRING no genera una lista con el estilo de \_ ordenación CBS que se va a ordenar.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490541"
---
# <a name="cb_insertstring-message"></a><span data-ttu-id="56f63-105">\_Mensaje INSERTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="56f63-105">CB\_INSERTSTRING message</span></span>

<span data-ttu-id="56f63-106">Inserta una cadena o datos de elemento en la lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="56f63-106">Inserts a string or item data into the list of a combo box.</span></span> <span data-ttu-id="56f63-107">A diferencia del mensaje [**CB \_ ADDSTRING**](cb-addstring.md) , el mensaje **CB \_ INSERTSTRING** no genera una lista con el estilo de [**\_ ordenación CBS**](combo-box-styles.md) que se va a ordenar.</span><span class="sxs-lookup"><span data-stu-id="56f63-107">Unlike the [**CB\_ADDSTRING**](cb-addstring.md) message, the **CB\_INSERTSTRING** message does not cause a list with the [**CBS\_SORT**](combo-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="56f63-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56f63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f63-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56f63-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56f63-110">Índice de base cero de la posición en la que se va a insertar la cadena.</span><span class="sxs-lookup"><span data-stu-id="56f63-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="56f63-111">Si este parámetro es-1, la cadena se agrega al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="56f63-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="56f63-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56f63-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56f63-113">Puntero a la cadena terminada en null que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="56f63-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="56f63-114">Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el valor del parámetro *lParam* se almacena en lugar de la cadena a la que apuntaría de otro modo.</span><span class="sxs-lookup"><span data-stu-id="56f63-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored rather than the string to which it would otherwise point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56f63-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56f63-115">Return value</span></span>

<span data-ttu-id="56f63-116">El valor devuelto es el índice de la posición en la que se insertó la cadena.</span><span class="sxs-lookup"><span data-stu-id="56f63-116">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="56f63-117">Si se produce un error, el valor devuelto es CB \_ error.</span><span class="sxs-lookup"><span data-stu-id="56f63-117">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="56f63-118">Si no hay suficiente espacio disponible para almacenar la nueva cadena, es CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="56f63-118">If there is insufficient space available to store the new string, it is CB\_ERRSPACE.</span></span>

<span data-ttu-id="56f63-119">Si el cuadro combinado tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e inserta una cadena más ancha que el cuadro combinado, debe enviar un mensaje [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparezca la barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="56f63-119">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the combo box, you should send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

## <a name="requirements"></a><span data-ttu-id="56f63-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56f63-120">Requirements</span></span>



| <span data-ttu-id="56f63-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="56f63-121">Requirement</span></span> | <span data-ttu-id="56f63-122">Value</span><span class="sxs-lookup"><span data-stu-id="56f63-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56f63-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56f63-123">Minimum supported client</span></span><br/> | <span data-ttu-id="56f63-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56f63-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="56f63-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56f63-125">Minimum supported server</span></span><br/> | <span data-ttu-id="56f63-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="56f63-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="56f63-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56f63-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="56f63-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56f63-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56f63-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="56f63-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="56f63-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="56f63-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="56f63-131">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="56f63-131">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="56f63-132">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="56f63-132">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="56f63-133">**\_directorio CB**</span><span class="sxs-lookup"><span data-stu-id="56f63-133">**CB\_DIR**</span></span>](cb-dir.md)
</dt> </dl>

 


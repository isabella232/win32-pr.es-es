---
title: Mensaje de CB_ADDSTRING (Winuser. h)
description: Agrega una cadena al cuadro de lista de un cuadro combinado. Si el cuadro combinado no tiene el estilo de \_ ordenación CBS, la cadena se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista está ordenada.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- CB_ADDSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996933"
---
# <a name="cb_addstring-message"></a><span data-ttu-id="cfcfa-106">Mensaje de CB \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="cfcfa-106">CB\_ADDSTRING message</span></span>

<span data-ttu-id="cfcfa-107">Agrega una cadena al cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-107">Adds a string to the list box of a combo box.</span></span> <span data-ttu-id="cfcfa-108">Si el cuadro combinado no tiene el estilo [**de \_ ordenación CBS**](combo-box-styles.md) , la cadena se agrega al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-108">If the combo box does not have the [**CBS\_SORT**](combo-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="cfcfa-109">De lo contrario, la cadena se inserta en la lista y la lista está ordenada.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-109">Otherwise, the string is inserted into the list, and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfcfa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfcfa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfcfa-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfcfa-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfcfa-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cfcfa-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfcfa-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfcfa-114">Puntero **LPCTSTR** a la cadena terminada en null que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-114">An **LPCTSTR** pointer to the null-terminated string to be added.</span></span> <span data-ttu-id="cfcfa-115">Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el valor del parámetro *lParam* se almacena como datos de elemento en lugar de la cadena a la que apuntaría de otro modo.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored as item data rather than the string it would otherwise point to.</span></span> <span data-ttu-id="cfcfa-116">Los datos de los elementos se pueden recuperar o modificar mediante el envío del mensaje [**CB \_ GETITEMDATA**](cb-getitemdata.md) o [**CB \_ SETITEMDATA**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="cfcfa-116">The item data can be retrieved or modified by sending the [**CB\_GETITEMDATA**](cb-getitemdata.md) or [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfcfa-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfcfa-117">Return value</span></span>

<span data-ttu-id="cfcfa-118">El valor devuelto es el índice de base cero de la cadena en el cuadro de lista del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-118">The return value is the zero-based index to the string in the list box of the combo box.</span></span> <span data-ttu-id="cfcfa-119">Si se produce un error, el valor devuelto es CB \_ error.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-119">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="cfcfa-120">Si no hay suficiente espacio disponible para almacenar la nueva cadena, es CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-120">If insufficient space is available to store the new string, it is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfcfa-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfcfa-121">Remarks</span></span>

<span data-ttu-id="cfcfa-122">Si crea un cuadro combinado dibujado por el propietario con el estilo de [**\_ ordenación CBS**](combo-box-styles.md) pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el mensaje [**\_ COMPAREITEM de WM**](wm-compareitem.md) se envía una o varias veces al propietario del cuadro combinado para que el nuevo elemento se pueda colocar correctamente en la lista.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-122">If you create an owner-drawn combo box with the [**CBS\_SORT**](combo-box-styles.md) style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the [**WM\_COMPAREITEM**](wm-compareitem.md) message is sent one or more times to the owner of the combo box so the new item can be properly placed in the list.</span></span>

<span data-ttu-id="cfcfa-123">Para insertar una cadena en una ubicación concreta de la lista, use el mensaje [**CB \_ INSERTSTRING**](cb-insertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="cfcfa-123">To insert a string at a specific location within the list, use the [**CB\_INSERTSTRING**](cb-insertstring.md) message.</span></span>

<span data-ttu-id="cfcfa-124">Si el cuadro combinado tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) y agrega una cadena más ancha que el cuadro combinado, envíe un mensaje [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparezca la barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-124">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the combo box, send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="cfcfa-125">**Comclt32.dll versión 5,0 o posterior:** Si se establece [**CBS \_ LOWERCASE**](combo-box-styles.md) o [**CBS \_ Uppercase**](combo-box-styles.md) , la versión Unicode de **CB \_ ADDSTRING** modifica la cadena.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-125">**Comclt32.dll version 5.0 or later:** If [**CBS\_LOWERCASE**](combo-box-styles.md) or [**CBS\_UPPERCASE**](combo-box-styles.md) is set, the Unicode version of **CB\_ADDSTRING** alters the string.</span></span> <span data-ttu-id="cfcfa-126">Si se usa la memoria global de solo lectura, se produce un error en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cfcfa-126">If using read-only global memory, this causes the application to fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfcfa-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfcfa-127">Requirements</span></span>



| <span data-ttu-id="cfcfa-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfcfa-128">Requirement</span></span> | <span data-ttu-id="cfcfa-129">Value</span><span class="sxs-lookup"><span data-stu-id="cfcfa-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfcfa-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfcfa-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cfcfa-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cfcfa-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cfcfa-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfcfa-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cfcfa-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfcfa-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cfcfa-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfcfa-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfcfa-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfcfa-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfcfa-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfcfa-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="cfcfa-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cfcfa-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cfcfa-138">**\_directorio CB**</span><span class="sxs-lookup"><span data-stu-id="cfcfa-138">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="cfcfa-139">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="cfcfa-139">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="cfcfa-140">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="cfcfa-140">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="cfcfa-141">**COMPAREITEM de WM \_**</span><span class="sxs-lookup"><span data-stu-id="cfcfa-141">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 


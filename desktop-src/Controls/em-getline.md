---
title: Mensaje de EM_GETLINE (Winuser. h)
description: Copia una línea de texto de un control de edición y la coloca en un búfer especificado. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETLINE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996009"
---
# <a name="em_getline-message-winuserh"></a><span data-ttu-id="48a85-105">Mensaje de EM_GETLINE (Winuser. h)</span><span class="sxs-lookup"><span data-stu-id="48a85-105">EM_GETLINE message (Winuser.h)</span></span>

<span data-ttu-id="48a85-106">Copia una línea de texto de un control de edición y la coloca en un búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="48a85-106">Copies a line of text from an edit control and places it in a specified buffer.</span></span> <span data-ttu-id="48a85-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="48a85-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="48a85-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48a85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48a85-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48a85-110">Índice de base cero de la línea que se va a recuperar de un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="48a85-110">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="48a85-111">Un valor de cero especifica la línea superior.</span><span class="sxs-lookup"><span data-stu-id="48a85-111">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="48a85-112">Este parámetro se omite en un control de edición de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="48a85-112">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="48a85-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48a85-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48a85-114">Puntero al búfer que recibe una copia de la línea.</span><span class="sxs-lookup"><span data-stu-id="48a85-114">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="48a85-115">Antes de enviar el mensaje, establezca la primera palabra de este búfer en el tamaño, en **TCHAR** s, del búfer.</span><span class="sxs-lookup"><span data-stu-id="48a85-115">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="48a85-116">Para texto ANSI, es el número de bytes; en el caso de texto Unicode, es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="48a85-116">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="48a85-117">La línea copiada sobrescribe el tamaño de la primera palabra.</span><span class="sxs-lookup"><span data-stu-id="48a85-117">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a85-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48a85-118">Return value</span></span>

<span data-ttu-id="48a85-119">El valor devuelto es el número **de elementos** que se han copiado.</span><span class="sxs-lookup"><span data-stu-id="48a85-119">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="48a85-120">El valor devuelto es cero si el número de línea especificado por el parámetro *wParam* es mayor que el número de líneas en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="48a85-120">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="48a85-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48a85-121">Remarks</span></span>

<span data-ttu-id="48a85-122">**Controles de edición:** La línea copiada no contiene un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="48a85-122">**Edit controls:** The copied line does not contain a terminating null character.</span></span>

<span data-ttu-id="48a85-123">**Controles Rich Edit:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="48a85-123">**Rich edit controls:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="48a85-124">La línea copiada no contiene un carácter nulo de terminación, a menos que no se haya copiado ningún texto.</span><span class="sxs-lookup"><span data-stu-id="48a85-124">The copied line does not contain a terminating null character, unless no text was copied.</span></span> <span data-ttu-id="48a85-125">Si no se ha copiado ningún texto, el mensaje coloca un carácter nulo al principio del búfer.</span><span class="sxs-lookup"><span data-stu-id="48a85-125">If no text was copied, the message places a null character at the beginning of the buffer.</span></span> <span data-ttu-id="48a85-126">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="48a85-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48a85-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48a85-127">Requirements</span></span>



| <span data-ttu-id="48a85-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a85-128">Requirement</span></span> | <span data-ttu-id="48a85-129">Value</span><span class="sxs-lookup"><span data-stu-id="48a85-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a85-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48a85-130">Minimum supported client</span></span><br/> | <span data-ttu-id="48a85-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="48a85-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="48a85-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48a85-132">Minimum supported server</span></span><br/> | <span data-ttu-id="48a85-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="48a85-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48a85-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48a85-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a85-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48a85-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a85-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="48a85-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="48a85-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="48a85-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="48a85-138">**\_LINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="48a85-138">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="48a85-139">**Editar \_ GetLine**</span><span class="sxs-lookup"><span data-stu-id="48a85-139">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

<span data-ttu-id="48a85-140">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="48a85-140">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="48a85-141">**GETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="48a85-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 


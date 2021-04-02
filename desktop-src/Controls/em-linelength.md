---
title: Mensaje de EM_LINELENGTH (Winuser. h)
description: Recupera la longitud, en caracteres, de una línea en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_LINELENGTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905480"
---
# <a name="em_linelength-message"></a><span data-ttu-id="74978-105">\_Mensaje LINELENGTH em</span><span class="sxs-lookup"><span data-stu-id="74978-105">EM\_LINELENGTH message</span></span>

<span data-ttu-id="74978-106">Recupera la longitud, en caracteres, de una línea en un control de edición.</span><span class="sxs-lookup"><span data-stu-id="74978-106">Retrieves the length, in characters, of a line in an edit control.</span></span> <span data-ttu-id="74978-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="74978-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="74978-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74978-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74978-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74978-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74978-110">Índice de carácter de un carácter de la línea cuya longitud se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="74978-110">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="74978-111">Si este parámetro es mayor que el número de caracteres del control, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="74978-111">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="74978-112">Este parámetro puede ser-1.</span><span class="sxs-lookup"><span data-stu-id="74978-112">This parameter can be -1.</span></span> <span data-ttu-id="74978-113">En este caso, el mensaje devuelve el número de caracteres no seleccionados en líneas que contienen los caracteres seleccionados.</span><span class="sxs-lookup"><span data-stu-id="74978-113">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="74978-114">Por ejemplo, si la selección se extiende desde el cuarto carácter de una línea hasta el octavo carácter desde el final de la línea siguiente, el valor devuelto sería 10 (tres caracteres en la primera línea y siete en el siguiente).</span><span class="sxs-lookup"><span data-stu-id="74978-114">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="74978-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74978-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74978-116">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="74978-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74978-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74978-117">Return value</span></span>

<span data-ttu-id="74978-118">En el caso de los controles de edición multilínea, el valor devuelto es la longitud, en **TCHAR** s, de la línea especificada por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="74978-118">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter.</span></span> <span data-ttu-id="74978-119">Para texto ANSI, es el número de bytes; en el caso de texto Unicode, es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="74978-119">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="74978-120">No incluye el carácter de retorno de carro al final de la línea.</span><span class="sxs-lookup"><span data-stu-id="74978-120">It does not include the carriage-return character at the end of the line.</span></span>

<span data-ttu-id="74978-121">En el caso de los controles de edición de una sola línea, el valor devuelto es la longitud, en **TCHAR** s, del texto del control de edición.</span><span class="sxs-lookup"><span data-stu-id="74978-121">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="74978-122">Si *wParam* es mayor que el número de caracteres del control, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="74978-122">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="74978-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74978-123">Remarks</span></span>

<span data-ttu-id="74978-124">Use el [**mensaje \_ LINEINDEX em**](em-lineindex.md) para recuperar un índice de carácter para un número de línea determinado dentro de un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="74978-124">Use the [**EM\_LINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control.</span></span>

<span data-ttu-id="74978-125">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="74978-125">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="74978-126">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="74978-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74978-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74978-127">Requirements</span></span>



| <span data-ttu-id="74978-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="74978-128">Requirement</span></span> | <span data-ttu-id="74978-129">Value</span><span class="sxs-lookup"><span data-stu-id="74978-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74978-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74978-130">Minimum supported client</span></span><br/> | <span data-ttu-id="74978-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="74978-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="74978-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74978-132">Minimum supported server</span></span><br/> | <span data-ttu-id="74978-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="74978-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74978-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74978-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="74978-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74978-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74978-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="74978-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74978-137">**\_LINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="74978-137">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 






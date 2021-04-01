---
title: Mensaje EM_SETTEXTMODE (RichEdit. h)
description: Establece el modo de texto o el nivel de deshacer de un control Rich Edit. Se produce un error en el mensaje si el control contiene texto.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996559"
---
# <a name="em_settextmode-message"></a><span data-ttu-id="bce20-105">\_Mensaje SETTEXTMODE em</span><span class="sxs-lookup"><span data-stu-id="bce20-105">EM\_SETTEXTMODE message</span></span>

<span data-ttu-id="bce20-106">Establece el modo de texto o el nivel de deshacer de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bce20-106">Sets the text mode or undo level of a rich edit control.</span></span> <span data-ttu-id="bce20-107">Se produce un error en el mensaje si el control contiene texto.</span><span class="sxs-lookup"><span data-stu-id="bce20-107">The message fails if the control contains any text.</span></span>

## <a name="parameters"></a><span data-ttu-id="bce20-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bce20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce20-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bce20-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bce20-110">Uno o más valores del tipo de enumeración [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="bce20-110">One or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="bce20-111">Los valores especifican los nuevos valores para el modo de texto y los parámetros de nivel de deshacer del control.</span><span class="sxs-lookup"><span data-stu-id="bce20-111">The values specify the new settings for the control's text mode and undo level parameters.</span></span>

<span data-ttu-id="bce20-112">Especifique uno de los siguientes valores para establecer el parámetro de modo de texto.</span><span class="sxs-lookup"><span data-stu-id="bce20-112">Specify one of the following values to set the text mode parameter.</span></span> <span data-ttu-id="bce20-113">Si no especifica un valor en modo de texto, el modo de texto permanece en su configuración actual.</span><span class="sxs-lookup"><span data-stu-id="bce20-113">If you do not specify a text mode value, the text mode remains at its current setting.</span></span> 

| <span data-ttu-id="bce20-114">Value</span><span class="sxs-lookup"><span data-stu-id="bce20-114">Value</span></span>                                          | <span data-ttu-id="bce20-115">Significado</span><span class="sxs-lookup"><span data-stu-id="bce20-115">Meaning</span></span>                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bce20-116">**\_texto sin formato de TM**</span><span class="sxs-lookup"><span data-stu-id="bce20-116">**TM\_PLAINTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="bce20-117">Indica el modo de texto sin formato, en el que el control es similar a un control de edición estándar.</span><span class="sxs-lookup"><span data-stu-id="bce20-117">Indicates plain text mode, in which the control is similar to a standard edit control.</span></span> <span data-ttu-id="bce20-118">Para obtener más información sobre el modo de texto sin formato, vea la sección Comentarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="bce20-118">For more information about plain text mode, see the following Remarks section.</span></span> |
| [<span data-ttu-id="bce20-119">**TM \_ RICHTEXT**</span><span class="sxs-lookup"><span data-stu-id="bce20-119">**TM\_RICHTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="bce20-120">Indica el modo de texto enriquecido, en el que el control tiene una funcionalidad estándar de edición enriquecida.</span><span class="sxs-lookup"><span data-stu-id="bce20-120">Indicates rich text mode, in which the control has standard rich edit functionality.</span></span> <span data-ttu-id="bce20-121">El modo de texto enriquecido es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bce20-121">Rich text mode is the default setting.</span></span>                                           |



 

<span data-ttu-id="bce20-122">Especifique uno de los siguientes valores para establecer el parámetro de nivel de deshacer.</span><span class="sxs-lookup"><span data-stu-id="bce20-122">Specify one of the following values to set the undo level parameter.</span></span> <span data-ttu-id="bce20-123">Si no especifica un valor de nivel de deshacer, el nivel de deshacer se mantiene en su configuración actual.</span><span class="sxs-lookup"><span data-stu-id="bce20-123">If you do not specify an undo level value, the undo level remains at its current setting.</span></span> 

| <span data-ttu-id="bce20-124">Value</span><span class="sxs-lookup"><span data-stu-id="bce20-124">Value</span></span>                                                      | <span data-ttu-id="bce20-125">Significado</span><span class="sxs-lookup"><span data-stu-id="bce20-125">Meaning</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bce20-126">**TM \_ SINGLELEVELUNDO**</span><span class="sxs-lookup"><span data-stu-id="bce20-126">**TM\_SINGLELEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="bce20-127">El control permite al usuario deshacer solo la última acción que se puede deshacer.</span><span class="sxs-lookup"><span data-stu-id="bce20-127">The control allows the user to undo only the last action that can be undone.</span></span>                                                                                                       |
| [<span data-ttu-id="bce20-128">**TM \_ MULTILEVELUNDO**</span><span class="sxs-lookup"><span data-stu-id="bce20-128">**TM\_MULTILEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="bce20-129">El control admite varias operaciones de deshacer.</span><span class="sxs-lookup"><span data-stu-id="bce20-129">The control supports multiple undo operations.</span></span> <span data-ttu-id="bce20-130">Esta es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bce20-130">This is the default setting.</span></span> <span data-ttu-id="bce20-131">Use el [**mensaje \_ SETUNDOLIMIT em**](em-setundolimit.md) para establecer el número máximo de acciones de deshacer.</span><span class="sxs-lookup"><span data-stu-id="bce20-131">Use the [**EM\_SETUNDOLIMIT**](em-setundolimit.md) message to set the maximum number of undo actions.</span></span> |



 

<span data-ttu-id="bce20-132">Especifique uno de los siguientes valores para establecer el parámetro de página de códigos.</span><span class="sxs-lookup"><span data-stu-id="bce20-132">Specify one of the following values to set the code page parameter.</span></span> <span data-ttu-id="bce20-133">Si no especifica un valor de página de códigos, la página de códigos permanece en su configuración actual.</span><span class="sxs-lookup"><span data-stu-id="bce20-133">If you do not specify an code page value, the code page remains at its current setting.</span></span> 

| <span data-ttu-id="bce20-134">Value</span><span class="sxs-lookup"><span data-stu-id="bce20-134">Value</span></span>                                                    | <span data-ttu-id="bce20-135">Significado</span><span class="sxs-lookup"><span data-stu-id="bce20-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bce20-136">**TM \_ SINGLECODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="bce20-136">**TM\_SINGLECODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="bce20-137">El control solo permite el teclado inglés y un teclado correspondientes al Juego de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bce20-137">The control only allows the English keyboard and a keyboard corresponding to the default character set.</span></span> <span data-ttu-id="bce20-138">Por ejemplo, podría tener griego e inglés.</span><span class="sxs-lookup"><span data-stu-id="bce20-138">For example, you could have Greek and English.</span></span> <span data-ttu-id="bce20-139">Tenga en cuenta que esto evita que el texto Unicode entre en el control.</span><span class="sxs-lookup"><span data-stu-id="bce20-139">Note that this prevents Unicode text from entering the control.</span></span> <span data-ttu-id="bce20-140">Por ejemplo, use este valor si un control Rich Edit debe estar restringido a texto ANSI.</span><span class="sxs-lookup"><span data-stu-id="bce20-140">For example, use this value if a Rich Edit control must be restricted to ANSI text.</span></span> |
| [<span data-ttu-id="bce20-141">**TM \_ MULTICODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="bce20-141">**TM\_MULTICODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="bce20-142">El control permite varias páginas de códigos y texto Unicode en el control.</span><span class="sxs-lookup"><span data-stu-id="bce20-142">The control allows multiple code pages and Unicode text into the control.</span></span> <span data-ttu-id="bce20-143">Esta es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bce20-143">This is the default setting.</span></span>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="bce20-144">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bce20-144">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bce20-145">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bce20-145">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce20-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bce20-146">Return value</span></span>

<span data-ttu-id="bce20-147">Si el mensaje se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="bce20-147">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="bce20-148">Si se produce un error en el mensaje, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bce20-148">If the message fails, the return value is a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bce20-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bce20-149">Remarks</span></span>

<span data-ttu-id="bce20-150">En el modo de texto enriquecido, un control Rich Edit tiene una funcionalidad estándar de edición enriquecida.</span><span class="sxs-lookup"><span data-stu-id="bce20-150">In rich text mode, a rich edit control has standard rich edit functionality.</span></span> <span data-ttu-id="bce20-151">Sin embargo, en modo de texto sin formato, el control es similar a un control de edición estándar:</span><span class="sxs-lookup"><span data-stu-id="bce20-151">However, in plain text mode, the control is similar to a standard edit control:</span></span>

-   <span data-ttu-id="bce20-152">El texto de un control de texto sin formato solo puede tener un formato (por ejemplo, negrita, 10 PTO y Arial).</span><span class="sxs-lookup"><span data-stu-id="bce20-152">The text in a plain text control can have only one format (such as Bold, 10pt Arial).</span></span>
-   <span data-ttu-id="bce20-153">El usuario no puede pegar formatos de texto enriquecido, como el formato de texto enriquecido (RTF) o los objetos incrustados en un control de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="bce20-153">The user cannot paste rich text formats, such as Rich Text Format (RTF) or embedded objects into a plain text control.</span></span>
-   <span data-ttu-id="bce20-154">Los controles de modo de texto enriquecido siempre tienen un marcador de fin de documento o un retorno de carro predeterminados para dar formato a los párrafos.</span><span class="sxs-lookup"><span data-stu-id="bce20-154">Rich text mode controls always have a default end-of-document marker or carriage return, to format paragraphs.</span></span> <span data-ttu-id="bce20-155">Los controles de texto sin formato, por otro lado, no necesitan el marcador de fin de documento predeterminado, por lo que se omite.</span><span class="sxs-lookup"><span data-stu-id="bce20-155">Plain text controls, on the other hand, do not need the default, end-of-document marker, so it is omitted.</span></span>

<span data-ttu-id="bce20-156">El control no debe contener texto cuando recibe el mensaje **\_ SETTEXTMODE em** .</span><span class="sxs-lookup"><span data-stu-id="bce20-156">The control must contain no text when it receives the **EM\_SETTEXTMODE** message.</span></span> <span data-ttu-id="bce20-157">Para asegurarse de que no hay texto, envíe un mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) con una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="bce20-157">To ensure there is no text, send a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message with an empty string ("").</span></span>

## <a name="requirements"></a><span data-ttu-id="bce20-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bce20-158">Requirements</span></span>



| <span data-ttu-id="bce20-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="bce20-159">Requirement</span></span> | <span data-ttu-id="bce20-160">Value</span><span class="sxs-lookup"><span data-stu-id="bce20-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bce20-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bce20-161">Minimum supported client</span></span><br/> | <span data-ttu-id="bce20-162">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bce20-162">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bce20-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bce20-163">Minimum supported server</span></span><br/> | <span data-ttu-id="bce20-164">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bce20-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bce20-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bce20-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="bce20-166"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bce20-166"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bce20-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="bce20-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce20-168">**\_GETTEXTMODE em**</span><span class="sxs-lookup"><span data-stu-id="bce20-168">**EM\_GETTEXTMODE**</span></span>](em-gettextmode.md)
</dt> <dt>

[<span data-ttu-id="bce20-169">**\_SETUNDOLIMIT em**</span><span class="sxs-lookup"><span data-stu-id="bce20-169">**EM\_SETUNDOLIMIT**</span></span>](em-setundolimit.md)
</dt> <dt>

[<span data-ttu-id="bce20-170">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="bce20-170">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[<span data-ttu-id="bce20-171">**SETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="bce20-171">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 


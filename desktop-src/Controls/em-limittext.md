---
title: EM_LIMITTEXT mensaje (Winuser.h)
description: 'EM_LIMITTEXT mensaje: establece el límite de texto de un control de edición.'
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- EM_LIMITTEXT mensaje Controles de Windows
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80ce29d4ee5155f6b3c5c32609366982655a078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109793"
---
# <a name="em_limittext-message"></a><span data-ttu-id="0685a-104">Mensaje \_ LIMITTEXT DE EM</span><span class="sxs-lookup"><span data-stu-id="0685a-104">EM\_LIMITTEXT message</span></span>

<span data-ttu-id="0685a-105">Establece el límite de texto de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="0685a-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="0685a-106">El límite de texto es la cantidad máxima de texto, en **TCHAR** s, que el usuario puede escribir en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="0685a-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="0685a-107">Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.</span><span class="sxs-lookup"><span data-stu-id="0685a-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="0685a-108">Para los controles de edición y Microsoft Rich Edit 1.0, se usan bytes.</span><span class="sxs-lookup"><span data-stu-id="0685a-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="0685a-109">Para Microsoft Rich Edit 2.0 y versiones posteriores, se usan caracteres.</span><span class="sxs-lookup"><span data-stu-id="0685a-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

## <a name="parameters"></a><span data-ttu-id="0685a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0685a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0685a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0685a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0685a-112">Número máximo de **TCHAR** que el usuario puede especificar.</span><span class="sxs-lookup"><span data-stu-id="0685a-112">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="0685a-113">En el caso del texto ANSI, este es el número de bytes; para texto Unicode, este es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0685a-113">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="0685a-114">Este número no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="0685a-114">This number does not include the terminating null character.</span></span>

<span data-ttu-id="0685a-115">**Controles de edición enriquecciones:** Si este parámetro es cero, la longitud del texto se establece en 64 000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0685a-115">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="0685a-116">Si este parámetro es cero, la longitud del texto se establece 0x7FFFFFFE caracteres para los controles de edición de una sola línea o -1 para los controles de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="0685a-116">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or -1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="0685a-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0685a-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0685a-118">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0685a-118">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0685a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0685a-119">Return value</span></span>

<span data-ttu-id="0685a-120">Este mensaje no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="0685a-120">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0685a-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0685a-121">Remarks</span></span>

<span data-ttu-id="0685a-122">El **mensaje EM \_ LIMITTEXT** limita solo el texto que el usuario puede escribir.</span><span class="sxs-lookup"><span data-stu-id="0685a-122">The **EM\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="0685a-123">No afecta a ningún texto que ya esté en el control de edición cuando se envía el mensaje, ni afecta a la longitud del texto copiado en el control de edición por el mensaje [**\_ SETTEXT de WM.**](/windows/desktop/winmsg/wm-settext)</span><span class="sxs-lookup"><span data-stu-id="0685a-123">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="0685a-124">Si una aplicación usa el mensaje **\_ SETTEXT** de WM para colocar más texto en un control de edición que el especificado en el mensaje **EM \_ LIMITTEXT,** el usuario puede editar todo el contenido del control de edición.</span><span class="sxs-lookup"><span data-stu-id="0685a-124">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_LIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="0685a-125">Antes **de llamar a EM \_ LIMITTEXT,** el límite predeterminado para la cantidad de texto que un usuario puede escribir en un control de edición es de 32 767 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0685a-125">Before **EM\_LIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="0685a-126">Para los controles de edición de una sola línea, el límite de texto es 0x7FFFFFFE bytes o el valor del parámetro *wParam,* lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="0685a-126">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="0685a-127">Para los controles de edición multilínea, este valor es -1 byte o el valor del parámetro *wParam,* lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="0685a-127">For multiline edit controls, this value is either -1 byte or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="0685a-128">**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0685a-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="0685a-129">Use el mensaje [**EM \_ EXLIMITTEXT para**](em-exlimittext.md) valores de longitud de texto mayores que 64 000.</span><span class="sxs-lookup"><span data-stu-id="0685a-129">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="0685a-130">Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0685a-130">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0685a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0685a-131">Requirements</span></span>



| <span data-ttu-id="0685a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0685a-132">Requirement</span></span> | <span data-ttu-id="0685a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0685a-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0685a-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0685a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0685a-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0685a-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0685a-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0685a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0685a-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0685a-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0685a-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0685a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0685a-139"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0685a-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0685a-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0685a-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="0685a-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0685a-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0685a-142">**EM \_ EXLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="0685a-142">**EM\_EXLIMITTEXT**</span></span>](em-exlimittext.md)
</dt> <dt>

[<span data-ttu-id="0685a-143">**Editar \_ LimitText**</span><span class="sxs-lookup"><span data-stu-id="0685a-143">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

<span data-ttu-id="0685a-144">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="0685a-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0685a-145">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="0685a-145">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 


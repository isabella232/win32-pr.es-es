---
title: EM_SETLIMITTEXT mensaje (Winuser.h)
description: 'EM_SETLIMITTEXT mensaje: establece el límite de texto de un control de edición.'
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT de mensajes controles de Windows
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66d4e03b5c1824ab501226482fcf51fb9121cba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109753"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="2c6e4-104">Mensaje \_ EM SETLIMITTEXT</span><span class="sxs-lookup"><span data-stu-id="2c6e4-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="2c6e4-105">Establece el límite de texto de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="2c6e4-106">El límite de texto es la cantidad máxima de texto, en **TCHAR,** que el usuario puede escribir en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="2c6e4-107">Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="2c6e4-108">Para los controles de edición y Microsoft Rich Edit 1.0, se usan bytes.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="2c6e4-109">Para Microsoft Rich Edit 2.0 y versiones posteriores, se usan caracteres.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="2c6e4-110">El **mensaje EM \_ SETLIMITTEXT** es idéntico al mensaje [**EM \_ LIMITTEXT.**](em-limittext.md)</span><span class="sxs-lookup"><span data-stu-id="2c6e4-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c6e4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c6e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c6e4-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c6e4-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c6e4-113">Número máximo de **TCHAR que** el usuario puede especificar.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="2c6e4-114">Para el texto ANSI, este es el número de bytes; Para el texto Unicode, este es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="2c6e4-115">Este número no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="2c6e4-116">**Controles de edición enriquecciones:** Si este parámetro es cero, la longitud del texto se establece en 64 000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="2c6e4-117">Si este parámetro es cero, la longitud del texto se establece en 0x7FFFFFFE para los controles de edición de una sola línea o 1 para los controles de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="2c6e4-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c6e4-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c6e4-119">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c6e4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c6e4-120">Return value</span></span>

<span data-ttu-id="2c6e4-121">Este mensaje no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c6e4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c6e4-122">Remarks</span></span>

<span data-ttu-id="2c6e4-123">El **mensaje EM \_ SETLIMITTEXT** limita solo el texto que el usuario puede escribir.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="2c6e4-124">No afecta a ningún texto que ya esté en el control de edición cuando se envía el mensaje, ni afecta a la longitud del texto copiado en el control de edición por el mensaje [**\_ SETTEXT de WM.**](/windows/desktop/winmsg/wm-settext)</span><span class="sxs-lookup"><span data-stu-id="2c6e4-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="2c6e4-125">Si una aplicación usa el mensaje **\_ SETTEXT** de WM para colocar más texto en un control de edición que el especificado en el mensaje **EM \_ SETLIMITTEXT,** el usuario puede editar todo el contenido del control de edición.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="2c6e4-126">Antes de llamar a **EM \_ SETLIMITTEXT,** el límite predeterminado para la cantidad de texto que un usuario puede escribir en un control de edición es de 32 767 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="2c6e4-127">Para los controles de edición de una sola línea, el límite de texto es 0x7FFFFFFE bytes o el valor del parámetro *wParam,* lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="2c6e4-128">Para los controles de edición multilínea, este valor es de 1 bytes o el valor del *parámetro wParam,* lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="2c6e4-129">**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="2c6e4-130">Use el mensaje [**EM \_ EXLIMITTEXT para**](em-exlimittext.md) valores de longitud de texto mayores que 64 000.</span><span class="sxs-lookup"><span data-stu-id="2c6e4-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="2c6e4-131">Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="2c6e4-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c6e4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c6e4-132">Requirements</span></span>



| <span data-ttu-id="2c6e4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c6e4-133">Requirement</span></span> | <span data-ttu-id="2c6e4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2c6e4-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6e4-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c6e4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2c6e4-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2c6e4-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c6e4-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c6e4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2c6e4-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c6e4-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c6e4-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c6e4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c6e4-140"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c6e4-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c6e4-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2c6e4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c6e4-142">**EM \_ GETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="2c6e4-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 


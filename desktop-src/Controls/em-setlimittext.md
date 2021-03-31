---
title: Mensaje de EM_SETLIMITTEXT (Winuser. h)
description: Establece el límite de texto de un control de edición.
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT controles de mensajes de Windows
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
ms.openlocfilehash: 5c138e6d7fed75fa8da2e7a6b93308632c250e7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802654"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="59ad4-104">\_Mensaje SETLIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="59ad4-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="59ad4-105">Establece el límite de texto de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="59ad4-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="59ad4-106">El límite de texto es la cantidad máxima de texto, en **TCHAR** s, que el usuario puede escribir en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="59ad4-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="59ad4-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="59ad4-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="59ad4-108">En el caso de los controles de edición y Microsoft Rich Edit 1,0, se usan bytes.</span><span class="sxs-lookup"><span data-stu-id="59ad4-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="59ad4-109">En el caso de Microsoft Rich Edit 2,0 y versiones posteriores, se usan caracteres.</span><span class="sxs-lookup"><span data-stu-id="59ad4-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="59ad4-110">El mensaje **em \_ SETLIMITTEXT** es idéntico al mensaje [**\_ LIMITTEXT em**](em-limittext.md) .</span><span class="sxs-lookup"><span data-stu-id="59ad4-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="59ad4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59ad4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ad4-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59ad4-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ad4-113">El número máximo de **TCHAR** s que el usuario puede escribir.</span><span class="sxs-lookup"><span data-stu-id="59ad4-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="59ad4-114">Para texto ANSI, es el número de bytes; en el caso de texto Unicode, es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="59ad4-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="59ad4-115">Este número no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="59ad4-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="59ad4-116">**Controles Rich Edit:** Si este parámetro es cero, la longitud del texto se establece en 64.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="59ad4-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="59ad4-117">Si este parámetro es cero, la longitud del texto se establece en 0x7FFFFFFE caracteres para los controles de edición de una sola línea o en 1 para los controles de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="59ad4-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="59ad4-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59ad4-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ad4-119">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="59ad4-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59ad4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59ad4-120">Return value</span></span>

<span data-ttu-id="59ad4-121">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="59ad4-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ad4-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59ad4-122">Remarks</span></span>

<span data-ttu-id="59ad4-123">El **mensaje \_ SETLIMITTEXT em** limita solo el texto que el usuario puede escribir.</span><span class="sxs-lookup"><span data-stu-id="59ad4-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="59ad4-124">No afecta a ningún texto que ya esté en el control de edición cuando se envía el mensaje, ni afecta a la longitud del texto copiado en el control de edición por el mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="59ad4-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="59ad4-125">Si una aplicación utiliza el mensaje de **WM \_ SETTEXT** para colocar más texto en un control de edición que se especifica en el mensaje **\_ SETLIMITTEXT em** , el usuario puede editar todo el contenido del control de edición.</span><span class="sxs-lookup"><span data-stu-id="59ad4-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="59ad4-126">Antes de que se llame a **em \_ SETLIMITTEXT** , el límite predeterminado para la cantidad de texto que un usuario puede escribir en un control de edición es de 32.767 caracteres.</span><span class="sxs-lookup"><span data-stu-id="59ad4-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="59ad4-127">En el caso de los controles de edición de una sola línea, el límite del texto es 0x7FFFFFFE bytes o el valor del parámetro *wParam* , el que sea menor.</span><span class="sxs-lookup"><span data-stu-id="59ad4-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="59ad4-128">En el caso de los controles de edición multilínea, este valor es 1 bytes o el valor del parámetro *wParam* , el que sea menor.</span><span class="sxs-lookup"><span data-stu-id="59ad4-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="59ad4-129">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="59ad4-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="59ad4-130">Use el mensaje [**em \_ EXLIMITTEXT**](em-exlimittext.md) para valores de longitud de texto mayor que 64.000.</span><span class="sxs-lookup"><span data-stu-id="59ad4-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="59ad4-131">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="59ad4-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59ad4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59ad4-132">Requirements</span></span>



| <span data-ttu-id="59ad4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ad4-133">Requirement</span></span> | <span data-ttu-id="59ad4-134">Value</span><span class="sxs-lookup"><span data-stu-id="59ad4-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ad4-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ad4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="59ad4-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="59ad4-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="59ad4-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ad4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="59ad4-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="59ad4-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59ad4-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59ad4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ad4-140"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59ad4-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59ad4-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="59ad4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ad4-142">**\_GETLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="59ad4-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 


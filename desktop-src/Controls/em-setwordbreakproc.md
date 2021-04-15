---
title: Mensaje de EM_SETWORDBREAKPROC (Winuser. h)
description: Reemplaza la función de ajuste de la configuración predeterminada de un control de edición por una función de ajuste de la aplicación definida por la aplicación. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- EM_SETWORDBREAKPROC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534360"
---
# <a name="em_setwordbreakproc-message"></a><span data-ttu-id="f1222-105">\_Mensaje SETWORDBREAKPROC em</span><span class="sxs-lookup"><span data-stu-id="f1222-105">EM\_SETWORDBREAKPROC message</span></span>

<span data-ttu-id="f1222-106">Reemplaza la función de ajuste de la configuración predeterminada de un control de edición por una función de ajuste de la aplicación definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f1222-106">Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function.</span></span> <span data-ttu-id="f1222-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f1222-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1222-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1222-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1222-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1222-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1222-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f1222-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1222-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1222-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1222-112">La dirección de la función de ajuste de la aplicación definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f1222-112">The address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="f1222-113">Para obtener más información sobre las líneas de interrupción, vea la descripción de la función de devolución de llamada [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .</span><span class="sxs-lookup"><span data-stu-id="f1222-113">For more information about breaking lines, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1222-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1222-114">Return value</span></span>

<span data-ttu-id="f1222-115">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f1222-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1222-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1222-116">Remarks</span></span>

<span data-ttu-id="f1222-117">Una función WordWrap examina un búfer de texto que contiene el texto que se va a enviar a la pantalla, buscando la primera palabra que no cabe en la línea de pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="f1222-117">A Wordwrap function scans a text buffer that contains text to be sent to the screen, looking for the first word that does not fit on the current screen line.</span></span> <span data-ttu-id="f1222-118">La función WordWrap coloca esta palabra al principio de la línea siguiente en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f1222-118">The Wordwrap function places this word at the beginning of the next line on the screen.</span></span>

<span data-ttu-id="f1222-119">Una función WordWrap define el punto en el que el sistema debe dividir una línea de texto para los controles de edición de varias líneas, normalmente en un carácter de espacio que separa dos palabras.</span><span class="sxs-lookup"><span data-stu-id="f1222-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span> <span data-ttu-id="f1222-120">Un control de edición multilínea o de una sola línea podría llamar a esta función cuando el usuario presiona las teclas de dirección en combinación con la tecla CTRL para desplace el símbolo de intercalación a la palabra siguiente o a la palabra anterior.</span><span class="sxs-lookup"><span data-stu-id="f1222-120">Either a multiline or a single-line edit control might call this function when the user presses arrow keys in combination with the CTRL key to move the caret to the next word or previous word.</span></span> <span data-ttu-id="f1222-121">La función WordWrap predeterminada divide una línea de texto en un carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="f1222-121">The default Wordwrap function breaks a line of text at a space character.</span></span> <span data-ttu-id="f1222-122">La función definida por la aplicación puede definir que el ajuste de velocidad se produzca en un guion o un carácter distinto del carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="f1222-122">The application-defined function may define the Wordwrap to occur at a hyphen or a character other than the space character.</span></span>

<span data-ttu-id="f1222-123">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f1222-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="f1222-124">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f1222-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1222-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1222-125">Requirements</span></span>



| <span data-ttu-id="f1222-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1222-126">Requirement</span></span> | <span data-ttu-id="f1222-127">Value</span><span class="sxs-lookup"><span data-stu-id="f1222-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1222-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1222-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f1222-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f1222-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f1222-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1222-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f1222-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1222-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f1222-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1222-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1222-133"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1222-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1222-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1222-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1222-135">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f1222-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f1222-136">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="f1222-136">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="f1222-137">**\_FMTLINES em**</span><span class="sxs-lookup"><span data-stu-id="f1222-137">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="f1222-138">**\_GETWORDBREAKPROC em**</span><span class="sxs-lookup"><span data-stu-id="f1222-138">**EM\_GETWORDBREAKPROC**</span></span>](em-getwordbreakproc.md)
</dt> </dl>

 


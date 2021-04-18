---
title: Mensaje de EM_GETWORDBREAKPROC (Winuser. h)
description: Obtiene la dirección de la función de ajuste de la actual. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- EM_GETWORDBREAKPROC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491999"
---
# <a name="em_getwordbreakproc-message"></a><span data-ttu-id="30e09-105">\_Mensaje GETWORDBREAKPROC em</span><span class="sxs-lookup"><span data-stu-id="30e09-105">EM\_GETWORDBREAKPROC message</span></span>

<span data-ttu-id="30e09-106">Obtiene la dirección de la función de ajuste de la actual.</span><span class="sxs-lookup"><span data-stu-id="30e09-106">Gets the address of the current Wordwrap function.</span></span> <span data-ttu-id="30e09-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="30e09-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="30e09-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30e09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e09-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30e09-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e09-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="30e09-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="30e09-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30e09-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e09-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="30e09-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e09-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30e09-113">Return value</span></span>

<span data-ttu-id="30e09-114">El valor devuelto especifica la dirección de la función de ajuste de la aplicación definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="30e09-114">The return value specifies the address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="30e09-115">El valor devuelto es **null** si no existe ninguna función WordWrap.</span><span class="sxs-lookup"><span data-stu-id="30e09-115">The return value is **NULL** if no Wordwrap function exists.</span></span>

## <a name="remarks"></a><span data-ttu-id="30e09-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30e09-116">Remarks</span></span>

<span data-ttu-id="30e09-117">Una función WordWrap recorre un búfer de texto que contiene el texto que se va a enviar a la pantalla, buscando la primera palabra que no cabe en la línea de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="30e09-117">A Wordwrap function scans a text buffer that contains text to be sent to the display, looking for the first word that does not fit on the current display line.</span></span> <span data-ttu-id="30e09-118">La función WordWrap coloca esta palabra al principio de la línea siguiente en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="30e09-118">The wordwrap function places this word at the beginning of the next line on the display.</span></span> <span data-ttu-id="30e09-119">Una función WordWrap define el punto en el que el sistema debe dividir una línea de texto para los controles de edición de varias líneas, normalmente en un carácter de espacio que separa dos palabras.</span><span class="sxs-lookup"><span data-stu-id="30e09-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span>

<span data-ttu-id="30e09-120">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="30e09-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="30e09-121">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="30e09-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30e09-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30e09-122">Requirements</span></span>



| <span data-ttu-id="30e09-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="30e09-123">Requirement</span></span> | <span data-ttu-id="30e09-124">Value</span><span class="sxs-lookup"><span data-stu-id="30e09-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30e09-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30e09-125">Minimum supported client</span></span><br/> | <span data-ttu-id="30e09-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="30e09-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="30e09-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30e09-127">Minimum supported server</span></span><br/> | <span data-ttu-id="30e09-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="30e09-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30e09-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30e09-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="30e09-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30e09-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30e09-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="30e09-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="30e09-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="30e09-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30e09-133">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="30e09-133">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="30e09-134">**\_FMTLINES em**</span><span class="sxs-lookup"><span data-stu-id="30e09-134">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="30e09-135">**\_SETWORDBREAKPROC em**</span><span class="sxs-lookup"><span data-stu-id="30e09-135">**EM\_SETWORDBREAKPROC**</span></span>](em-setwordbreakproc.md)
</dt> </dl>

 


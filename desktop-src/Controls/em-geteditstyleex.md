---
title: Mensaje EM_GETEDITSTYLEEX (RichEdit. h)
description: Recupera las marcas de estilo de edición extendida actual.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905300"
---
# <a name="em_geteditstyleex-message"></a><span data-ttu-id="1e396-104">\_Mensaje GETEDITSTYLEEX em</span><span class="sxs-lookup"><span data-stu-id="1e396-104">EM\_GETEDITSTYLEEX message</span></span>

<span data-ttu-id="1e396-105">Recupera las marcas de estilo de edición extendida actual.</span><span class="sxs-lookup"><span data-stu-id="1e396-105">Retrieves the current extended edit style flags.</span></span>


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a><span data-ttu-id="1e396-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e396-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e396-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e396-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e396-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1e396-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1e396-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e396-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e396-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1e396-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e396-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e396-111">Return value</span></span>

<span data-ttu-id="1e396-112">Devuelve las marcas de estilo de edición extendida, que pueden incluir uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1e396-112">Returns the extended edit style flags, which can include one or more of the following values.</span></span>



| <span data-ttu-id="1e396-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1e396-113">Return code</span></span>                                                                                                | <span data-ttu-id="1e396-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e396-114">Description</span></span>                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e396-115"><dt>**SES \_ ex \_ HANDLEFRIENDLYURL**</dt></span><span class="sxs-lookup"><span data-stu-id="1e396-115"><dt>**SES\_EX\_HANDLEFRIENDLYURL**</dt></span></span> </dl>  | <span data-ttu-id="1e396-116">Mostrar los vínculos de nombre descriptivo con el mismo color de texto y subrayado como vínculos automáticos, siempre que el formato temporal sea t Used o use el texto Autocolor (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="1e396-116">Display friendly name links with the same text color and underlining as automatic links, provided that temporary formatting isn t used or uses text autocolor (default: 0).</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="1e396-117"><dt>**SES \_ ex \_ multitoque**</dt></span><span class="sxs-lookup"><span data-stu-id="1e396-117"><dt>**SES\_EX\_MULTITOUCH**</dt></span></span> </dl>         | <span data-ttu-id="1e396-118">Habilite la compatibilidad con Touch en Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1e396-118">Enable touch support in Rich Edit.</span></span> <span data-ttu-id="1e396-119">Esto incluye la selección, la posición del símbolo de intercalación y la invocación del menú contextual.</span><span class="sxs-lookup"><span data-stu-id="1e396-119">This includes selection, caret placement, and context-menu invocation.</span></span> <span data-ttu-id="1e396-120">Cuando no se establece esta marca, el toque se emula mediante comandos del mouse, que no tienen en cuenta los detalles del modo táctil (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="1e396-120">When this flag is not set, touch is emulated by mouse commands, which do not take touch-mode specifics into account (default: 0).</span></span> <br/>      |
| <dl> <span data-ttu-id="1e396-121"><dt>**SES \_ ex \_ NOACETATESELECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="1e396-121"><dt>**SES\_EX\_NOACETATESELECTION**</dt></span></span> </dl> | <span data-ttu-id="1e396-122">Muestra el texto seleccionado con el texto de selección clásico de Windows y los colores de fondo en lugar del color de acetato de fondo (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="1e396-122">Display selected text using classic Windows selection text and background colors instead of background acetate color (default: 0).</span></span> <br/>                                                                                                               |
| <dl> <span data-ttu-id="1e396-123"><dt>**SES \_ = \_ nomath**</dt></span><span class="sxs-lookup"><span data-stu-id="1e396-123"><dt>**SES\_EX\_NOMATH**</dt></span></span> </dl>             | <span data-ttu-id="1e396-124">Deshabilitar la inserción de zonas matemáticas (valor predeterminado: 1).</span><span class="sxs-lookup"><span data-stu-id="1e396-124">Disable insertion of math zones (default: 1).</span></span> <span data-ttu-id="1e396-125">Para habilitar la edición y visualización de matemáticas, envíe el mensaje [**em \_ SETEDITSTYLEEX**](em-seteditstyleex.md) con *wParam* establecido en 0 y *lParam* establecido en **SES @ \_ \_ nomath**.</span><span class="sxs-lookup"><span data-stu-id="1e396-125">To enable math editing and display, send the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message with *wParam* set to 0, and *lParam* set to **SES\_EX\_NOMATH**.</span></span> <br/>                              |
| <dl> <span data-ttu-id="1e396-126"><dt>**SES, \_ ex \_ importante**</dt></span><span class="sxs-lookup"><span data-stu-id="1e396-126"><dt>**SES\_EX\_NOTABLE**</dt></span></span> </dl>            | <span data-ttu-id="1e396-127">Deshabilitar la inserción de tablas.</span><span class="sxs-lookup"><span data-stu-id="1e396-127">Disable insertion of tables.</span></span> <span data-ttu-id="1e396-128">El [**mensaje \_ INSERTTABLE em**](em-inserttable.md) devuelve **e \_ FAIL** y las tablas RTF se omiten (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="1e396-128">The [**EM\_INSERTTABLE**](em-inserttable.md) message returns **E\_FAIL** and RTF tables are skipped (default: 0).</span></span> <br/>                                                                                                  |
| <dl> <span data-ttu-id="1e396-129"><dt>**SES \_ ex \_ USESINGLELINE**</dt></span><span class="sxs-lookup"><span data-stu-id="1e396-129"><dt>**SES\_EX\_USESINGLELINE**</dt></span></span> </dl>      | <span data-ttu-id="1e396-130">Permite que un control multilínea actúe como un control de una sola línea con la capacidad de desplazarse verticalmente cuando el alto de una sola línea es mayor que el alto de la ventana (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="1e396-130">Enable a multiline control to act like a single-line control with the ability to scroll vertically when the single-line height is greater than the window height (default: 0).</span></span> <br/>                                                                   |
| <dl> <span data-ttu-id="1e396-131"><dt>**HIDETEMPFORMAT de SES \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e396-131"><dt>**SES\_HIDETEMPFORMAT**</dt></span></span> </dl>         | <span data-ttu-id="1e396-132">Oculte el formato temporal que se crea cuando se llama a [**ITextFont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) con **tomApplyTmp**.</span><span class="sxs-lookup"><span data-stu-id="1e396-132">Hide temporary formatting that is created when [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) is called with **tomApplyTmp**.</span></span> <span data-ttu-id="1e396-133">Por ejemplo, los comprobadores ortográficos usan este formato para mostrar un subrayado ondulado en palabras posiblemente mal escritas.</span><span class="sxs-lookup"><span data-stu-id="1e396-133">For example, such formatting is used by spell checkers to display a squiggly underline under possibly misspelled words.</span></span><br/> |
| <dl> <span data-ttu-id="1e396-134"><dt>**SES \_ ex \_ USEMOUSEWPARAM**</dt></span><span class="sxs-lookup"><span data-stu-id="1e396-134"><dt>**SES\_EX\_USEMOUSEWPARAM**</dt></span></span> </dl>     | <span data-ttu-id="1e396-135">Use *wParam* al controlar el mensaje de [**\_ MOUSEMOVE de WM**](/windows/desktop/inputdev/wm-mousemove) y no llame a [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="1e396-135">Use *wParam* when handling the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message and do not call [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="1e396-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e396-136">Requirements</span></span>



| <span data-ttu-id="1e396-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e396-137">Requirement</span></span> | <span data-ttu-id="1e396-138">Value</span><span class="sxs-lookup"><span data-stu-id="1e396-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e396-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e396-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1e396-140">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e396-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1e396-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e396-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1e396-142">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e396-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e396-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e396-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e396-144"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e396-144"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e396-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e396-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e396-146">**\_SETEDITSTYLEEX em**</span><span class="sxs-lookup"><span data-stu-id="1e396-146">**EM\_SETEDITSTYLEEX**</span></span>](em-seteditstyleex.md)
</dt> </dl>

 


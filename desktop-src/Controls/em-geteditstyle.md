---
title: Mensaje EM_GETEDITSTYLE (RichEdit. h)
description: Recupera las marcas de estilo de edición actuales.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- EM_GETEDITSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079487"
---
# <a name="em_geteditstyle-message"></a><span data-ttu-id="c34ae-104">\_Mensaje del GETEDITSTYLE em</span><span class="sxs-lookup"><span data-stu-id="c34ae-104">EM\_GETEDITSTYLE message</span></span>

<span data-ttu-id="c34ae-105">Recupera las marcas de estilo de edición actuales.</span><span class="sxs-lookup"><span data-stu-id="c34ae-105">Retrieves the current edit style flags.</span></span>

## <a name="parameters"></a><span data-ttu-id="c34ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c34ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c34ae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c34ae-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c34ae-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c34ae-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c34ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c34ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c34ae-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c34ae-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c34ae-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c34ae-111">Return value</span></span>

<span data-ttu-id="c34ae-112">Devuelve las marcas de estilo de edición actuales, que pueden incluir uno o varios de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c34ae-112">Returns the current edit style flags, which can include one or more of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c34ae-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c34ae-113">Return code</span></span></th>
<th><span data-ttu-id="c34ae-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c34ae-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-116">La edición enriquecida llamará al bip del sistema si el usuario intenta escribir más de los caracteres máximos.</span><span class="sxs-lookup"><span data-stu-id="c34ae-116">Rich Edit will call the system beeper if the user attempts to enter more than the maximum characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-117"><dt><strong>SES_BIDI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-117"><dt><strong>SES_BIDI</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-118">Activa el procesamiento bidireccional.</span><span class="sxs-lookup"><span data-stu-id="c34ae-118">Turns on bidirectional processing.</span></span> <span data-ttu-id="c34ae-119">Esto se activa automáticamente en Rich Edit si alguno de los siguientes estilos de ventana está activo: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c34ae-119">This is automatically turned on by Rich Edit if any of the following window styles are active: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span></span> <span data-ttu-id="c34ae-120">Sin embargo, esta configuración es útil para controlar estos estilos de ventana cuando se usa una implementación personalizada de <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-120">However, this setting is useful for handling these window styles when using a custom implementation of <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-122"><strong>Windows XP con SP1</strong>: permite la inserción de objetos incrustados mediante TSF (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-122"><strong>Windows XP with SP1</strong>: Allow embedded objects to be inserted using TSF (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-124"><strong>Windows XP con SP1</strong>: permite sugerencias de revisión de TSF (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-124"><strong>Windows XP with SP1</strong>: Allows TSF proofing tips (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-126"><strong>Windows XP con SP1</strong>: permite las sugerencias de interacciones de TSF (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-126"><strong>Windows XP with SP1</strong>: Allows TSF SmartTag tips (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-128"><strong>Windows 8</strong>: no se permite el acceso de lectura y escritura del bloqueo TSF.</span><span class="sxs-lookup"><span data-stu-id="c34ae-128"><strong>Windows 8</strong>: Do not allow the TSF lock read/write access.</span></span> <span data-ttu-id="c34ae-129">Esto detiene la entrada TSF.</span><span class="sxs-lookup"><span data-stu-id="c34ae-129">This pauses TSF input.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-131"><strong>Windows 8</strong>: se muestran fuentes con una ligadura Fi con las características OpenType predeterminadas, lo que da como resultado una tipografía mejorada (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-131"><strong>Windows 8</strong>: Fonts with an fi ligature are displayed with default OpenType features resulting in improved typography (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-133"><strong>Windows XP con SP1</strong>: usar fuentes en modo de borrador para mostrar texto.</span><span class="sxs-lookup"><span data-stu-id="c34ae-133"><strong>Windows XP with SP1</strong>: Use draft mode fonts to display text.</span></span> <span data-ttu-id="c34ae-134">El modo borrador es una opción de accesibilidad en la que el control muestra el texto con una sola fuente; la fuente viene determinada por la configuración del sistema para la fuente utilizada en los cuadros de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c34ae-134">Draft mode is an accessibility option where the control displays the text with a single font; the font is determined by the system setting for the font used in message boxes.</span></span> <span data-ttu-id="c34ae-135">Por ejemplo, los usuarios accesibles pueden leer texto más fácilmente si es uniforme, en lugar de una combinación de fuentes y estilos (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-135">For example, accessible users may read text easier if it is uniform, rather than a mix of fonts and styles (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-136"><dt><strong>SES_EMULATE10</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-136"><dt><strong>SES_EMULATE10</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-137"><strong>Windows 8</strong>: emular el comportamiento de RichEdit 1,0.</span><span class="sxs-lookup"><span data-stu-id="c34ae-137"><strong>Windows 8</strong>: Emulate RichEdit 1.0 behavior.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c34ae-138">Si realmente desea este comportamiento, use el riched32.dll de Windows en lugar de riched20.dll o msftedit.dll.</span><span class="sxs-lookup"><span data-stu-id="c34ae-138">If you really want this behavior, use the Windows riched32.dll instead of riched20.dll or msftedit.dll.</span></span> <span data-ttu-id="c34ae-139">Riched32.dll tenía más funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="c34ae-139">Riched32.dll had more functionality.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-141">Cuando este bit está activado, la edición enriquecida intenta emular el control de edición del sistema (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-141">When this bit is on, rich edit attempts to emulate the system edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-143">Extiende el color de fondo hasta los bordes del rectángulo del cliente (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-143">Extends the background color all the way to the edges of the client rectangle (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-145"><strong>Windows XP con SP1</strong>: Si el ancho de las líneas de cuadrícula de la tabla es cero, no se muestran las líneas de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="c34ae-145"><strong>Windows XP with SP1</strong>: If the width of table gridlines is zero, gridlines are not displayed.</span></span> <span data-ttu-id="c34ae-146">Esto es equivalente a la característica ocultar líneas de cuadrícula del menú Tabla de Word (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-146">This is equivalent to the hide gridlines feature in Word's table menu (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-148"><strong>Windows 8</strong>: cuando el cursor está sobre un vínculo, se muestra una información sobre herramientas con la dirección del vínculo de destino (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-148"><strong>Windows 8</strong>: When the cursor is over a link, display a tooltip with the target link address (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-150"><strong>Windows 8</strong>: proporcione información de símbolo de intercalación lógica en lugar de un mapa de bits de símbolo de intercalación, como se describe en <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost:: TxSetCaretPos</strong></a> (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-150"><strong>Windows 8</strong>: Provide logical caret information instead of a caret bitmap as described in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-151"><dt><strong>SES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-151"><dt><strong>SES_LOWERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-152">Convierte todos los caracteres de entrada a minúsculas (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-152">Converts all input characters to lowercase (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-153"><dt><strong>SES_MAPCPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-153"><dt><strong>SES_MAPCPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-154">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="c34ae-154">Obsolete.</span></span> <span data-ttu-id="c34ae-155">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="c34ae-155">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-156"><dt><strong>SES_MULTISELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-156"><dt><strong>SES_MULTISELECT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-157"><strong>Windows 8</strong>: habilitación de la multiselección con selecciones de mouse individuales realizadas mientras se presiona la tecla Ctrl (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-157"><strong>Windows 8</strong>: Enable multiselection with individual mouse selections made while the Ctrl key is pressed (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-159"><strong>Windows 8</strong>: no ajuste el alto de línea para el texto asiático oriental (valor predeterminado: 0, que ajusta el alto de línea en un 15%).</span><span class="sxs-lookup"><span data-stu-id="c34ae-159"><strong>Windows 8</strong>: Do not adjust line height for East Asian text (default: 0 which adjusts the line height by 15%).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-161">Envía <a href="en-link.md">EN_LINK</a> notificación de los vínculos que no tienen el foco.</span><span class="sxs-lookup"><span data-stu-id="c34ae-161">Sends <a href="en-link.md">EN_LINK</a> notification from links that do not have focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-162"><dt><strong>SES_NOIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-162"><dt><strong>SES_NOIME</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-163">No permite los IME para esta instancia del control Rich Edit (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-163">Disallows IMEs for this instance of the rich edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-165">Cuando este bit está activado, la edición enriquecida no comprueba la secuencia de texto escrito.</span><span class="sxs-lookup"><span data-stu-id="c34ae-165">When this bit is on, rich edit does not verify the sequence of typed text.</span></span> <span data-ttu-id="c34ae-166">Algunos lenguajes (como el tailandés y el vietnamita) requieren comprobar el orden de las secuencias de entrada antes de enviarlo a la memoria auxiliar (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-166">Some languages (such as Thai and Vietnamese) require verifying the input sequence order before submitting it to the backing store (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-168">Cuando se produce KillFocus, se desplaza al principio del texto (la posición del carácter es igual a 0) (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-168">When KillFocus occurs, scroll to the beginning of the text (character position equal to 0) (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-170"><strong>Windows 8</strong>: agregar o eliminar un espacio según el contexto al quitar texto (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-170"><strong>Windows 8</strong>: Add or delete a space according to the context when dropping text (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-171"><dt><strong>SES_USECRLF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-171"><dt><strong>SES_USECRLF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-172">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="c34ae-172">Obsolete.</span></span> <span data-ttu-id="c34ae-173">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="c34ae-173">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-175"><strong>Windows 8</strong>: Si la opción seleccionar palabra está activa, asegúrese de que la ubicación de destino está en un límite de palabras (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-175"><strong>Windows 8</strong>: If word select is active, ensure that the drop location is at a word boundary (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-176"><dt><strong>SES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-176"><dt><strong>SES_UPPERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-177">Convierte todos los caracteres de entrada a mayúsculas (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-177">Converts all input characters to uppercase (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-178"><dt><strong>SES_USEAIMM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-178"><dt><strong>SES_USEAIMM</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-179">Usa el componente del método de entrada IMM activo que se incluye con Internet Explorer 4,0 o posterior (valor predeterminado: 0).</span><span class="sxs-lookup"><span data-stu-id="c34ae-179">Uses the Active IMM input method component that ships with Internet Explorer 4.0 or later (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-180"><dt><strong>SES_USEATFONT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-180"><dt><strong>SES_USEATFONT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-181"><strong>Windows XP con SP1</strong>: usa una @ Font, que está diseñada para texto vertical; se usa con el estilo de ventana <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c34ae-181"><strong>Windows XP with SP1</strong>: Uses an @ font, which is designed for vertical text; this is used with the <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> window style.</span></span> <span data-ttu-id="c34ae-182">El nombre de @ Font comienza con el símbolo @, por ejemplo, &quot; @Batang &quot; (valor predeterminado: 0, pero se activa automáticamente para el diseño de texto vertical).</span><span class="sxs-lookup"><span data-stu-id="c34ae-182">The name of an @ font begins with the @ symbol, for example, &quot;@Batang&quot; (default: 0, but is automatically turned on for vertical text layout).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c34ae-183"><dt><strong>SES_USECTF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-183"><dt><strong>SES_USECTF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-184"><strong>Windows XP con SP1</strong>: activa la compatibilidad con TSF.</span><span class="sxs-lookup"><span data-stu-id="c34ae-184"><strong>Windows XP with SP1</strong>: Turns on TSF support.</span></span> <span data-ttu-id="c34ae-185">(valor predeterminado: 0)</span><span class="sxs-lookup"><span data-stu-id="c34ae-185">(default: 0)</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c34ae-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c34ae-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c34ae-187">Activa la traducción de CRCRLFs a CRs.</span><span class="sxs-lookup"><span data-stu-id="c34ae-187">Turns on translation of CRCRLFs to CRs.</span></span> <span data-ttu-id="c34ae-188">Cuando este bit está activado y se lee un archivo en, todas las instancias de CRCRLF se convertirán en un sistema informatizado de modo interno.</span><span class="sxs-lookup"><span data-stu-id="c34ae-188">When this bit is on and a file is read in, all instances of CRCRLF will be converted to hard CRs internally.</span></span> <span data-ttu-id="c34ae-189">Esto afectará al ajuste del texto.</span><span class="sxs-lookup"><span data-stu-id="c34ae-189">This will affect the text wrapping.</span></span> <span data-ttu-id="c34ae-190">Tenga en cuenta que si este tipo de archivo se guarda como texto sin formato, el sistema de almacenamiento de archivos de almacenamiento se reemplazará por CRLFs.</span><span class="sxs-lookup"><span data-stu-id="c34ae-190">Note that if such a file is saved as plain text, the CRs will be replaced by CRLFs.</span></span> <span data-ttu-id="c34ae-191">Este es el estándar. txt para texto sin formato (valor predeterminado: 0, que elimina CRCRLFs en la entrada).</span><span class="sxs-lookup"><span data-stu-id="c34ae-191">This is the .txt standard for plain text (default: 0, which deletes CRCRLFs on input).</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c34ae-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c34ae-192">Requirements</span></span>



| <span data-ttu-id="c34ae-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="c34ae-193">Requirement</span></span> | <span data-ttu-id="c34ae-194">Value</span><span class="sxs-lookup"><span data-stu-id="c34ae-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c34ae-195">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c34ae-195">Minimum supported client</span></span><br/> | <span data-ttu-id="c34ae-196">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c34ae-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c34ae-197">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c34ae-197">Minimum supported server</span></span><br/> | <span data-ttu-id="c34ae-198">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c34ae-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c34ae-199">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c34ae-199">Redistributable</span></span><br/>          | <span data-ttu-id="c34ae-200">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="c34ae-200">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="c34ae-201">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c34ae-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="c34ae-202"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c34ae-202"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c34ae-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="c34ae-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c34ae-204">**\_SETEDITSTYLE em**</span><span class="sxs-lookup"><span data-stu-id="c34ae-204">**EM\_SETEDITSTYLE**</span></span>](em-seteditstyle.md)
</dt> </dl>

 


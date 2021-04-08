---
description: En el caso de una aplicación que trabaja con texto sin formato, Uniscribe proporciona las funciones de ScriptString \* .
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Uso de las funciones ScriptString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a2df5e7515bd605ad48cc7a246941e9b6f08f2
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078562"
---
# <a name="using-the-scriptstring-functions"></a><span data-ttu-id="3fde0-103">Uso de las funciones ScriptString</span><span class="sxs-lookup"><span data-stu-id="3fde0-103">Using the ScriptString Functions</span></span>

<span data-ttu-id="3fde0-104">En el caso de una aplicación que trabaja con texto sin formato, Uniscribe proporciona las funciones de **ScriptString \*** .</span><span class="sxs-lookup"><span data-stu-id="3fde0-104">For an application dealing with unformatted text, Uniscribe provides the **ScriptString\*** functions.</span></span> <span data-ttu-id="3fde0-105">Estas funciones son similares a [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)y [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), pero proporcionan compatibilidad completa con scripts complejos, incluida la colocación del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="3fde0-105">These functions are similar to [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext), and [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), but they provide full complex script support, including caret placement.</span></span> <span data-ttu-id="3fde0-106">Estas funciones son similares a las demás funciones de Uniscribe, pero se adaptan a los requisitos más sencillos del procesamiento de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="3fde0-106">These functions are similar to the other Uniscribe functions, but are tailored to the simpler requirements of plain text processing.</span></span>

<span data-ttu-id="3fde0-107">En la tabla siguiente se detallan las funciones de **ScriptString \*** y cualquier homólogo de las demás funciones de.</span><span class="sxs-lookup"><span data-stu-id="3fde0-107">The following table details the **ScriptString\*** functions and any counterparts in the other Uniscribe functions.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3fde0-108">Función</span><span class="sxs-lookup"><span data-stu-id="3fde0-108">Function</span></span></th>
<th><span data-ttu-id="3fde0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fde0-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3fde0-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-111">Analiza el texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="3fde0-111">Analyzes plain text.</span></span> <span data-ttu-id="3fde0-112">Esta función corresponde a las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="3fde0-112">This function corresponds to the following functions:</span></span><br/> <dl><span data-ttu-id="3fde0-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span></span><br /><span data-ttu-id="3fde0-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span></span><br /><span data-ttu-id="3fde0-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span></span><br /><span data-ttu-id="3fde0-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span></span><br /><span data-ttu-id="3fde0-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span></span><br /><span data-ttu-id="3fde0-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span></span><br /><span data-ttu-id="3fde0-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fde0-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-121">Recupera la coordenada x de una posición de carácter.</span><span class="sxs-lookup"><span data-stu-id="3fde0-121">Retrieves the x coordinate for a character position.</span></span> <span data-ttu-id="3fde0-122">Esta función corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3fde0-122">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3fde0-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-124">Libera una estructura de <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3fde0-124">Frees a <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fde0-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-126">Convierte los anchos visuales en anchos lógicos.</span><span class="sxs-lookup"><span data-stu-id="3fde0-126">Converts visual widths to logical widths.</span></span> <span data-ttu-id="3fde0-127">Esta función corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3fde0-127">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3fde0-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-129">Asigna las posiciones del glifo de caracteres de forma similar a <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, solo para uso heredado.</span><span class="sxs-lookup"><span data-stu-id="3fde0-129">Maps character glyph positions in a similar way to <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, for legacy use only.</span></span> <span data-ttu-id="3fde0-130">Esta función no funciona bien con los scripts que generan más de un glifo por punto de código.</span><span class="sxs-lookup"><span data-stu-id="3fde0-130">This function does not work well with scripts that generate more than one glyph per code point.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fde0-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-132">Muestra el texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="3fde0-132">Displays plain text.</span></span> <span data-ttu-id="3fde0-133">Esta función corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3fde0-133">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3fde0-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-135">Devuelve un puntero a la longitud de una cadena de texto sin formato recortada.</span><span class="sxs-lookup"><span data-stu-id="3fde0-135">Returns a pointer to the length of a clipped plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fde0-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-137">Devuelve un puntero al búfer de atributos lógicos para una cadena de texto sin formato analizada.</span><span class="sxs-lookup"><span data-stu-id="3fde0-137">Returns a pointer to the logical attributes buffer for an analyzed plain text string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3fde0-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-139">Devuelve un puntero al tamaño (ancho y alto) de una cadena de texto sin formato analizado.</span><span class="sxs-lookup"><span data-stu-id="3fde0-139">Returns a pointer to the size (width and height) for an analyzed plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fde0-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-141">Identifica las secuencias de punto de código no válidas en el script especificado.</span><span class="sxs-lookup"><span data-stu-id="3fde0-141">Identifies code point sequences not valid in the given script.</span></span> <span data-ttu-id="3fde0-142">Esta función es diferente de <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, que identifica los puntos de código que no están presentes en una fuente.</span><span class="sxs-lookup"><span data-stu-id="3fde0-142">This function is different from <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, which identifies code points not present in a font.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3fde0-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span><span class="sxs-lookup"><span data-stu-id="3fde0-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span></span></td>
<td><span data-ttu-id="3fde0-144">Convierte una coordenada x en una posición de carácter.</span><span class="sxs-lookup"><span data-stu-id="3fde0-144">Converts an x coordinate to a character position.</span></span> <span data-ttu-id="3fde0-145">Esta función corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3fde0-145">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3fde0-146">Para mostrar solo texto sin formato sin modificaciones, una aplicación debe llamar a [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)y [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span><span class="sxs-lookup"><span data-stu-id="3fde0-146">To only display plain text without any modifications, an application should call [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), and then [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span></span> <span data-ttu-id="3fde0-147">Las otras funciones se usan para modificar el texto sin formato antes de mostrarse.</span><span class="sxs-lookup"><span data-stu-id="3fde0-147">The other functions are used to modify the plain text before display.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fde0-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3fde0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fde0-149">Usar Uniscribe</span><span class="sxs-lookup"><span data-stu-id="3fde0-149">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 

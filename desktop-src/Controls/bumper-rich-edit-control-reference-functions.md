---
title: Funciones de edición enriquecidas
description: Funciones de edición enriquecidas
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105653206"
---
# <a name="rich-edit-functions"></a><span data-ttu-id="99b0f-103">Funciones de edición enriquecidas</span><span class="sxs-lookup"><span data-stu-id="99b0f-103">Rich Edit Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99b0f-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="99b0f-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99b0f-105">Tema</span><span class="sxs-lookup"><span data-stu-id="99b0f-105">Topic</span></span></th>
<th><span data-ttu-id="99b0f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="99b0f-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="99b0f-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-108">La función <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> es una función de devolución de llamada definida por la aplicación que se usa con el mensaje de <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="99b0f-108">The <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> function is an application-defined callback function that is used with the <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99b0f-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-110">La función <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> es una función de devolución de llamada definida por la aplicación que se usa con los mensajes <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> y <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="99b0f-110">The <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> function is an application defined callback function used with the <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> and <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> messages.</span></span> <span data-ttu-id="99b0f-111">Se utiliza para transferir un flujo de datos dentro o fuera de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="99b0f-111">It is used to transfer a stream of data into or out of a rich edit control.</span></span> <span data-ttu-id="99b0f-112">El tipo <strong>EDITSTREAMCALLBACK</strong> define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="99b0f-112">The <strong>EDITSTREAMCALLBACK</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="99b0f-113"><em>EditStreamCallback</em> es un marcador de posición para el nombre de la función definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="99b0f-113"><em>EditStreamCallback</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99b0f-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-115">La función <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> es una función de devolución de llamada definida por la aplicación que se usa con el mensaje de <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="99b0f-115">The <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> function is an application defined callback function used with the <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> message.</span></span> <span data-ttu-id="99b0f-116">Determina el índice de caracteres de la separación de palabras o la clase de caracteres y las marcas de separación de palabras de los caracteres del texto especificado.</span><span class="sxs-lookup"><span data-stu-id="99b0f-116">It determines the character index of the word break or the character class and word-break flags of the characters in the specified text.</span></span> <span data-ttu-id="99b0f-117">El tipo <strong>EDITWORDBREAKPROCEX</strong> define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="99b0f-117">The <strong>EDITWORDBREAKPROCEX</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="99b0f-118"><em>EditWordBreakProcEx</em> es un marcador de posición para el nombre de la función definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="99b0f-118"><em>EditWordBreakProcEx</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99b0f-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-120">Recupera el carácter alfanumérico matemático de formato de transformación Unicode (UTF)-32 que corresponde al carácter de plano básico multilingüe (BMP) y al estilo matemático especificados.</span><span class="sxs-lookup"><span data-stu-id="99b0f-120">Retrieves the Unicode Transformation Format (UTF)-32 math alphanumeric character that corresponds to the specified Basic Multilingual Plane (BMP) character and math style.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99b0f-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-122">Recupera el estilo matemático y el código de carácter de plano básico multilingüe (BMP) vertical que corresponde al byte final especificado de un par suplente matemático.</span><span class="sxs-lookup"><span data-stu-id="99b0f-122">Retrieves the math style and the upright Basic Multilingual Plane (BMP) character code that corresponds to the specified trailing byte of a math surrogate pair.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99b0f-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-124">La función <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> es una función de devolución de llamada definida por la aplicación que se usa con el mensaje de <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="99b0f-124">The <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> function is an application defined callback function used with the <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> message.</span></span> <span data-ttu-id="99b0f-125">Determina cómo se realiza la división en guiones en un control Rich Edit de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="99b0f-125">It determines how hyphenation is done in a Microsoft Rich Edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99b0f-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-127">Convierte los objetos matemáticos e inline integrados en el intervalo especificado en un formato lineal.</span><span class="sxs-lookup"><span data-stu-id="99b0f-127">Translates the built-up math, ruby, and other inline objects in the specified range to linear form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99b0f-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-129">Convierte las matemáticas de formato lineal de un intervalo en un formulario integrado, o modifica el formulario integrado actual.</span><span class="sxs-lookup"><span data-stu-id="99b0f-129">Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99b0f-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-131">Convierte los caracteres matemáticos en el intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="99b0f-131">Translates the math characters in the specified range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99b0f-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span><span class="sxs-lookup"><span data-stu-id="99b0f-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span></span><br/></td>
<td><span data-ttu-id="99b0f-133">Registra dos nombres de clase, REListBox20W y RECombobox20W, que se pueden usar para crear ventanas de cuadro de lista o de cuadro combinado de edición enriquecida.</span><span class="sxs-lookup"><span data-stu-id="99b0f-133">Registers two class names, REListBox20W and RECombobox20W, that could be used to create Rich Edit listbox or combobox windows.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="99b0f-134">Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</span><span class="sxs-lookup"><span data-stu-id="99b0f-134">Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="99b0f-135">Es posible que esta función no se admita en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="99b0f-135">This function may not be supported in future versions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 


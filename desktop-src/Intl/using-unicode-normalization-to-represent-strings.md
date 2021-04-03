---
description: Las aplicaciones pueden utilizar Unicode para representar cadenas en varios formatos.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Usar la normalización Unicode para representar cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913690"
---
# <a name="using-unicode-normalization-to-represent-strings"></a><span data-ttu-id="e2eca-103">Usar la normalización Unicode para representar cadenas</span><span class="sxs-lookup"><span data-stu-id="e2eca-103">Using Unicode Normalization to Represent Strings</span></span>

<span data-ttu-id="e2eca-104">Las aplicaciones pueden utilizar Unicode para representar cadenas en varios formatos.</span><span class="sxs-lookup"><span data-stu-id="e2eca-104">Applications can use Unicode to represent strings in multiple forms.</span></span> <span data-ttu-id="e2eca-105">Como la aceptación de Unicode ha crecido, especialmente a través de Internet, la necesidad ha surgido para eliminar las diferencias no esenciales en las cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2eca-105">As Unicode acceptance has grown, especially via the Internet, the need has arisen to eliminate non-essential differences in Unicode strings.</span></span> <span data-ttu-id="e2eca-106">Varias representaciones para una combinación de caracteres complican el software, por ejemplo, cuando un servidor web responde a una solicitud de página o un vinculador busca un identificador determinado en una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e2eca-106">Multiple representations for a combination of characters complicate software, for example, when a Web server responds to a page request or a linker seeks a particular identifier in a library.</span></span>

> [!Caution]  
> <span data-ttu-id="e2eca-107">Puede parecer que las distintas cadenas Unicode son visualmente idénticas, lo que plantea problemas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e2eca-107">Different Unicode strings can appear to be visually identical, raising security concerns.</span></span> <span data-ttu-id="e2eca-108">Para obtener más información, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="e2eca-108">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

<span data-ttu-id="e2eca-109">En respuesta a este requisito, el consorcio Unicode ha definido un proceso denominado "normalización", que genera una representación binaria para cualquiera de las representaciones binarias equivalentes de un carácter.</span><span class="sxs-lookup"><span data-stu-id="e2eca-109">In response to this requirement, the Unicode Consortium has defined a process called "normalization," which produces one binary representation for any of the equivalent binary representations of a character.</span></span> <span data-ttu-id="e2eca-110">Una vez normalizada, dos cadenas son equivalentes si y solo si tienen representaciones binarias idénticas.</span><span class="sxs-lookup"><span data-stu-id="e2eca-110">Once normalized, two strings are equivalent if and only if they have identical binary representations.</span></span> <span data-ttu-id="e2eca-111">La normalización elimina algunas diferencias, pero conserva el uso de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e2eca-111">The normalization eliminates some differences but preserves case.</span></span>

<span data-ttu-id="e2eca-112">Para usar la normalización Unicode, una aplicación puede llamar a las funciones [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) y [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) para reorganizar las cadenas acccording a Unicode 4,0 TR \# 15.</span><span class="sxs-lookup"><span data-stu-id="e2eca-112">To use Unicode normalization, an application can call the [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) and [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) functions for rearrangement of strings acccording to Unicode 4.0 TR\#15.</span></span> <span data-ttu-id="e2eca-113">La normalización puede ayudar a mejorar la seguridad al reducir las representaciones de cadena alternativas que tienen el mismo significado lingüístico.</span><span class="sxs-lookup"><span data-stu-id="e2eca-113">Normalization can help improve security by reducing alternate string representations that have the same linguistic meaning.</span></span> <span data-ttu-id="e2eca-114">No obstante, recuerde que la normalización no puede eliminar completamente las representaciones alternativas.</span><span class="sxs-lookup"><span data-stu-id="e2eca-114">Remember, however, that normalization cannot eliminate alternate representations entirely.</span></span>

<span data-ttu-id="e2eca-115">Para obtener una descripción detallada de los estándares Unicode para la normalización, consulte el [Anexo 15 del estándar Unicode ( \# formas de normalización de Unicode](https://www.unicode.org/reports/tr15) ) (UAX \# 15).</span><span class="sxs-lookup"><span data-stu-id="e2eca-115">For a detailed description of the Unicode standards for normalization, refer to [Unicode Standard Annex \#15: Unicode Normalization Forms](https://www.unicode.org/reports/tr15) (UAX \#15).</span></span>

> [!Caution]  
> <span data-ttu-id="e2eca-116">Dado que la normalización puede cambiar la forma de una cadena, los mecanismos de seguridad o los algoritmos de validación de caracteres deben implementarse normalmente después de la normalización.</span><span class="sxs-lookup"><span data-stu-id="e2eca-116">Because normalization can change the form of a string, security mechanisms or character validation algorithms should usually be implemented after normalization.</span></span> <span data-ttu-id="e2eca-117">Para obtener más información, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="e2eca-117">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="provide-multiple-representations-of-the-same-string"></a><span data-ttu-id="e2eca-118">Proporcionar varias representaciones de la misma cadena</span><span class="sxs-lookup"><span data-stu-id="e2eca-118">Provide Multiple Representations of the Same String</span></span>

<span data-ttu-id="e2eca-119">En muchos casos, Unicode permite varias representaciones de lo que es, lingüísticamente, la misma cadena.</span><span class="sxs-lookup"><span data-stu-id="e2eca-119">In many cases, Unicode allows multiple representations of what is, linguistically, the same string.</span></span> <span data-ttu-id="e2eca-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e2eca-120">For example:</span></span>

-   <span data-ttu-id="e2eca-121">La mayúscula A con el diéresis (diéresis) se puede representar como un único punto de código Unicode "Ä" (U + 00C4) o la combinación de mayúsculas A y el carácter de diéresis de combinación ("A" + "̈", es decir, U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="e2eca-121">Capital A with dieresis (umlaut) can be represented either as a single Unicode code point "Ä" (U+00C4) or the combination of Capital A and the combining Dieresis character ("A" + "¨", that is, U+0041 U+0308).</span></span> <span data-ttu-id="e2eca-122">Las consideraciones similares se aplican a muchos otros caracteres con marcas diacríticas.</span><span class="sxs-lookup"><span data-stu-id="e2eca-122">Similar considerations apply for many other characters with diacritic marks.</span></span>
-   <span data-ttu-id="e2eca-123">Un solo se puede representar de la manera habitual (letra mayúscula latina A, U + 0041) o por la letra mayúscula latina de ancho completo A (U + FF21).</span><span class="sxs-lookup"><span data-stu-id="e2eca-123">Capital A itself can be represented either in the usual manner (Latin Capital Letter A, U+0041) or by Fullwidth Latin Capital Letter A (U+FF21).</span></span> <span data-ttu-id="e2eca-124">Se aplican consideraciones similares para las demás letras latinas simples (mayúsculas y minúsculas) y para los caracteres katakana usados en la escritura en japonés.</span><span class="sxs-lookup"><span data-stu-id="e2eca-124">Similar considerations apply for the other simple Latin letters (both uppercase and lowercase) and for the katakana characters used in writing Japanese.</span></span>
-   <span data-ttu-id="e2eca-125">La cadena "fi" se puede representar mediante los caracteres "f" y "i" (U + 0066 U + 0069) o por la ligadura "fi" (U + FB01).</span><span class="sxs-lookup"><span data-stu-id="e2eca-125">The string "fi" can be represented either by the characters "f" and "i" (U+0066 U+0069) or by the ligature "ﬁ" (U+FB01).</span></span> <span data-ttu-id="e2eca-126">Se aplican consideraciones similares para muchas otras combinaciones de caracteres para los que Unicode define las ligaduras.</span><span class="sxs-lookup"><span data-stu-id="e2eca-126">Similar considerations apply for many other combinations of characters for which Unicode defines ligatures.</span></span>

## <a name="use-the-four-defined-normalization-forms"></a><span data-ttu-id="e2eca-127">Usar las cuatro formas de normalización definidas</span><span class="sxs-lookup"><span data-stu-id="e2eca-127">Use the Four Defined Normalization Forms</span></span>

<span data-ttu-id="e2eca-128">Las aplicaciones pueden realizar la normalización Unicode mediante varios algoritmos, denominados "formas de normalización", que obedecen las distintas reglas.</span><span class="sxs-lookup"><span data-stu-id="e2eca-128">Your applications can perform Unicode normalization using several algorithms, called "normalization forms," that obey different rules.</span></span> <span data-ttu-id="e2eca-129">Unicode Consortium ha definido cuatro formas de normalización: NFC (formulario C), NFD (formulario D), NFKC (formulario KC) y NFKD (Form KD).</span><span class="sxs-lookup"><span data-stu-id="e2eca-129">The Unicode Consortium has defined four normalization forms: NFC (form C), NFD (form D), NFKC (form KC), and NFKD (form KD).</span></span> <span data-ttu-id="e2eca-130">Cada formulario elimina algunas diferencias, pero conserva el uso de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e2eca-130">Each form eliminates some differences but preserves case.</span></span> <span data-ttu-id="e2eca-131">Win32 y el .NET Framework admiten las cuatro formas de normalización.</span><span class="sxs-lookup"><span data-stu-id="e2eca-131">Win32 and the .NET Framework support all four normalization forms.</span></span>

<span data-ttu-id="e2eca-132">La [**\_ forma**](/windows/desktop/api/Winnls/ne-winnls-norm_form) de tipo de enumeración NLS es compatible con las cuatro formas estándar de normalización Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2eca-132">The NLS enumeration type [**NORM\_FORM**](/windows/desktop/api/Winnls/ne-winnls-norm_form) supports the four standard Unicode normalization forms.</span></span> <span data-ttu-id="e2eca-133">Los formularios C y D proporcionan formas canónicas para las cadenas.</span><span class="sxs-lookup"><span data-stu-id="e2eca-133">Forms C and D provide canonical forms for strings.</span></span> <span data-ttu-id="e2eca-134">Los formularios no canónicos KC y KD proporcionan compatibilidad adicional y pueden revelar ciertas equivalencias semánticas que no son aparentes en los formularios C y D. Sin embargo, lo hacen a costa de una determinada pérdida de información y, por lo general, no deben usarse como una manera canónica de almacenar cadenas.</span><span class="sxs-lookup"><span data-stu-id="e2eca-134">Non-canonical forms KC and KD provide further compatibility, and can reveal certain semantic equivalences that are not apparent in forms C and D. However, they do so at the expense of a certain loss of information, and generally should not be used as a canonical way to store strings.</span></span>

<span data-ttu-id="e2eca-135">De las dos formas canónicas, el formulario C es un formulario "compuesto" y un formulario D es un formulario "descompuesto".</span><span class="sxs-lookup"><span data-stu-id="e2eca-135">Of the two canonical forms, form C is a "composed" form and form D is a "decomposed" form.</span></span> <span data-ttu-id="e2eca-136">Por ejemplo, el formulario C usa el punto de código Unicode "Ä" (U + 00C4), mientras que el formulario D USA ("A" + "̈", que es U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="e2eca-136">For example, form C uses the single Unicode code point "Ä" (U+00C4), while form D uses ("A" + "¨", that is U+0041 U+0308).</span></span> <span data-ttu-id="e2eca-137">Se representan de forma idéntica, ya que "̈" (U + 0308) es un carácter de combinación.</span><span class="sxs-lookup"><span data-stu-id="e2eca-137">These render identically, because "¨" (U+0308) is a combining character.</span></span> <span data-ttu-id="e2eca-138">El formato D puede usar cualquier número de puntos de código para representar un punto de código único utilizado por el formulario C.</span><span class="sxs-lookup"><span data-stu-id="e2eca-138">Form D can use any number of code points to represent a single code point used by form C.</span></span>

<span data-ttu-id="e2eca-139">Si dos cadenas son idénticas en el formulario C o en el formulario D, son idénticas en el otro formulario.</span><span class="sxs-lookup"><span data-stu-id="e2eca-139">If two strings are identical in either form C or form D, they are identical in the other form.</span></span> <span data-ttu-id="e2eca-140">Además, cuando se representa correctamente, se muestran indistinguidamente entre sí y desde la cadena no normalizada original.</span><span class="sxs-lookup"><span data-stu-id="e2eca-140">Furthermore, when correctly rendered, they display indistinguishably from one another and from the original non-normalized string.</span></span>

<span data-ttu-id="e2eca-141">Una vez normalizadas, las cadenas no se pueden devolver de forma coherente a su representación original.</span><span class="sxs-lookup"><span data-stu-id="e2eca-141">Once normalized, strings cannot be consistently returned to their original representation.</span></span> <span data-ttu-id="e2eca-142">Por ejemplo, si una cadena con una mezcla de representaciones de caracteres compuestas y descompuestas se convierte en un formato normalizado, no hay ninguna manera de anular la normalización de la cadena mixta original.</span><span class="sxs-lookup"><span data-stu-id="e2eca-142">For example, if a string with a mixture of composed and decomposed character representations is converted to a normalized form, there is no way to un-normalize it to the original mixed string.</span></span> <span data-ttu-id="e2eca-143">Por lo tanto, si una aplicación requiere la representación original de la cadena, debe almacenar esa representación explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e2eca-143">Therefore, if an application requires the original representation of the string, it must store that representation explicitly.</span></span> <span data-ttu-id="e2eca-144">Sin embargo, la conversión entre las dos formas canónicas es reversible.</span><span class="sxs-lookup"><span data-stu-id="e2eca-144">However, converting between the two canonical forms is reversible.</span></span> <span data-ttu-id="e2eca-145">Una cadena del formulario C se puede convertir al formato D y después volver al formulario C, y el resultado es idéntico a la cadena de C del formulario original.</span><span class="sxs-lookup"><span data-stu-id="e2eca-145">A string in form C can be converted to form D and then back to form C, and the result is identical to the original form C string.</span></span>

<span data-ttu-id="e2eca-146">Los formularios KC y KD son similares a los formularios C y D, respectivamente, pero estos "formularios de compatibilidad" tienen asignaciones adicionales de caracteres compatibles con el formato básico de cada carácter.</span><span class="sxs-lookup"><span data-stu-id="e2eca-146">Forms KC and KD are similar to forms C and D, respectively, but these "compatibility forms" have additional mappings of compatible characters to the basic form of each character.</span></span> <span data-ttu-id="e2eca-147">Estas asignaciones pueden provocar que se pierdan variaciones de caracteres menores.</span><span class="sxs-lookup"><span data-stu-id="e2eca-147">Such mappings can cause minor character variations to be lost.</span></span> <span data-ttu-id="e2eca-148">Combinan ciertos caracteres que son visualmente distintos.</span><span class="sxs-lookup"><span data-stu-id="e2eca-148">They combine certain characters that are visually distinct.</span></span> <span data-ttu-id="e2eca-149">Por ejemplo, combinan caracteres de ancho completo y de ancho medio con el mismo significado semántico, o con distintas formas de la misma letra árabe, o la ligadura "fi" (U + FB01) y el par de caracteres "fi" (U + 0066 U + 0069).</span><span class="sxs-lookup"><span data-stu-id="e2eca-149">For example, they combine full-width and half-width characters with the same semantic meaning, or different forms of the same Arabic letter, or the ligature "ﬁ" (U+FB01) and the character pair "fi" (U+0066 U+0069).</span></span> <span data-ttu-id="e2eca-150">También combinan algunos caracteres que a veces pueden tener un significado semántico diferente, como un dígito escrito como superíndice, como un subíndice, o incluido en un círculo.</span><span class="sxs-lookup"><span data-stu-id="e2eca-150">They also combine some characters that might sometimes have a different semantic meaning, such as a digit written as a superscript, as a subscript, or enclosed in a circle.</span></span> <span data-ttu-id="e2eca-151">Debido a esta pérdida de información, los formularios KC y KD generalmente no deben usarse como formas canónicas de cadenas, pero son útiles para determinadas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e2eca-151">Because of this information loss, forms KC and KD generally should not be used as canonical forms of strings, but they are useful for certain applications.</span></span>

<span data-ttu-id="e2eca-152">El formulario KC es un formulario compuesto y el formulario KD es un formulario descompuesto.</span><span class="sxs-lookup"><span data-stu-id="e2eca-152">Form KC is a composed form and form KD is a decomposed form.</span></span> <span data-ttu-id="e2eca-153">La aplicación puede avanzar y retroceder entre los formularios KC y KD, pero no hay ninguna manera coherente de pasar del formulario KC o KD a la cadena original, incluso si la cadena original está en la forma C o D.</span><span class="sxs-lookup"><span data-stu-id="e2eca-153">The application can go back and forth between forms KC and KD, but there is no consistent way to go from form KC or KD back to the original string, even if the original string is in form C or D.</span></span>

<span data-ttu-id="e2eca-154">Windows, las aplicaciones de Microsoft y el .NET Framework generalmente generan caracteres en el formulario C mediante métodos de entrada normales.</span><span class="sxs-lookup"><span data-stu-id="e2eca-154">Windows, Microsoft applications, and the .NET Framework generally generate characters in form C using normal input methods.</span></span> <span data-ttu-id="e2eca-155">Para la mayoría de los propósitos de Windows, el formulario C es la forma preferida.</span><span class="sxs-lookup"><span data-stu-id="e2eca-155">For most purposes on Windows, form C is the preferred form.</span></span> <span data-ttu-id="e2eca-156">Por ejemplo, los caracteres del formulario C se generan mediante la entrada del teclado de Windows.</span><span class="sxs-lookup"><span data-stu-id="e2eca-156">For example, characters in form C are produced by Windows keyboard input.</span></span> <span data-ttu-id="e2eca-157">Sin embargo, los caracteres importados desde la web y otras plataformas pueden introducir otras formas de normalización en el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="e2eca-157">However, characters imported from the Web and other platforms can introduce other normalization forms into the data stream.</span></span>

<span data-ttu-id="e2eca-158">Los ejemplos siguientes se extraen de UAX \# 15 y muestran las diferencias entre las cuatro formas de normalización.</span><span class="sxs-lookup"><span data-stu-id="e2eca-158">The following examples are drawn from UAX \#15, and illustrate the differences among the four normalization forms.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e2eca-159">Original</span><span class="sxs-lookup"><span data-stu-id="e2eca-159">Original</span></span></th>
<th><span data-ttu-id="e2eca-160">Formulario D</span><span class="sxs-lookup"><span data-stu-id="e2eca-160">Form D</span></span></th>
<th><span data-ttu-id="e2eca-161">Formulario C</span><span class="sxs-lookup"><span data-stu-id="e2eca-161">Form C</span></span></th>
<th><span data-ttu-id="e2eca-162">Notas</span><span class="sxs-lookup"><span data-stu-id="e2eca-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2eca-163">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-163">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="e2eca-164">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-164">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="e2eca-165">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-165">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="e2eca-166">El ffi_ligature (U + FB03) no se descompone porque tiene una asignación de compatibilidad, no una asignación canónica. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e2eca-166">The ffi_ligature (U+FB03) is not decomposed, because it has a compatibility mapping, not a canonical mapping.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-167">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-167">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="e2eca-168">&quot;A\u0308\uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-168">&quot;A\u0308\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="e2eca-169">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-169">&quot;Ä\uFB03n&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e2eca-170">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-170">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="e2eca-171">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-171">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="e2eca-172">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-172">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="e2eca-173">El número romano IV (U + 2163) no se descompone. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e2eca-173">The ROMAN NUMERAL IV (U+2163) is not decomposed.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-174">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-174">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="e2eca-175">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-175">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="e2eca-176">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-176">&quot;Henry \u2163&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e2eca-177">ga</span><span class="sxs-lookup"><span data-stu-id="e2eca-177">ga</span></span></td>
<td><span data-ttu-id="e2eca-178">Ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-178">ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-179">ga</span><span class="sxs-lookup"><span data-stu-id="e2eca-179">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="e2eca-180">Los diferentes equivalentes de compatibilidad de un solo carácter japonés no dan como resultado la misma cadena de la forma C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e2eca-180">Different compatibility equivalents of a single Japanese character do not result in the same string in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-181">Ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-181">ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-182">Ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-182">ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-183">ga</span><span class="sxs-lookup"><span data-stu-id="e2eca-183">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e2eca-184">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="e2eca-184">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="e2eca-185">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="e2eca-185">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="e2eca-186">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="e2eca-186">hw_ka +hw_ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-187">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="e2eca-187">ka +hw_ten</span></span></td>
<td><span data-ttu-id="e2eca-188">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="e2eca-188">ka +hw_ten</span></span></td>
<td><span data-ttu-id="e2eca-189">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="e2eca-189">ka +hw_ten</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e2eca-190">hw_ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-190">hw_ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-191">hw_ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-191">hw_ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-192">hw_ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-192">hw_ka +ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-193">kaks</span><span class="sxs-lookup"><span data-stu-id="e2eca-193">kaks</span></span></td>
<td><span data-ttu-id="e2eca-194">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="e2eca-194">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="e2eca-195">kaks</span><span class="sxs-lookup"><span data-stu-id="e2eca-195">kaks</span></span></td>
<td><span data-ttu-id="e2eca-196">Las sílabas hangul se mantienen en la normalización.</span><span class="sxs-lookup"><span data-stu-id="e2eca-196">Hangul syllables are maintained under normalization.</span></span><br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e2eca-197">Original</span><span class="sxs-lookup"><span data-stu-id="e2eca-197">Original</span></span></th>
<th><span data-ttu-id="e2eca-198">Formulario KD</span><span class="sxs-lookup"><span data-stu-id="e2eca-198">Form KD</span></span></th>
<th><span data-ttu-id="e2eca-199">Formulario KC</span><span class="sxs-lookup"><span data-stu-id="e2eca-199">Form KC</span></span></th>
<th><span data-ttu-id="e2eca-200">Notas</span><span class="sxs-lookup"><span data-stu-id="e2eca-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2eca-201">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-201">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="e2eca-202">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-202">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="e2eca-203">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-203">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="e2eca-204">El ffi_ligature (U + FB03) se descompone en el formulario KC, pero no en el formulario C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e2eca-204">The ffi_ligature (U+FB03) is decomposed in form KC, but not in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-205">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-205">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="e2eca-206">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-206">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="e2eca-207">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-207">&quot;Äffin&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e2eca-208">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-208">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="e2eca-209">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-209">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="e2eca-210">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-210">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="e2eca-211">Las cadenas resultantes son idénticas en el formulario KC. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e2eca-211">The resulting strings here are identical in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-212">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-212">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="e2eca-213">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-213">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="e2eca-214">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="e2eca-214">&quot;Henry IV&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e2eca-215">ga</span><span class="sxs-lookup"><span data-stu-id="e2eca-215">ga</span></span></td>
<td><span data-ttu-id="e2eca-216">Ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-216">ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-217">ga</span><span class="sxs-lookup"><span data-stu-id="e2eca-217">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="e2eca-218">Los diferentes equivalentes de compatibilidad de un solo carácter japonés dan como resultado la misma cadena en el formulario KC. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e2eca-218">Different compatibility equivalents of a single Japanese character result in the same string in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-219">Ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-219">ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-220">Ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-220">ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-221">ga</span><span class="sxs-lookup"><span data-stu-id="e2eca-221">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e2eca-222">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="e2eca-222">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="e2eca-223">Ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-223">ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-224">ga</span><span class="sxs-lookup"><span data-stu-id="e2eca-224">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-225">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="e2eca-225">ka +hw_ten</span></span></td>
<td><span data-ttu-id="e2eca-226">Ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-226">ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-227">ga</span><span class="sxs-lookup"><span data-stu-id="e2eca-227">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e2eca-228">hw_ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-228">hw_ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-229">Ka + diez</span><span class="sxs-lookup"><span data-stu-id="e2eca-229">ka +ten</span></span></td>
<td><span data-ttu-id="e2eca-230">ga</span><span class="sxs-lookup"><span data-stu-id="e2eca-230">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e2eca-231">kaks</span><span class="sxs-lookup"><span data-stu-id="e2eca-231">kaks</span></span></td>
<td><span data-ttu-id="e2eca-232">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="e2eca-232">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="e2eca-233">kaks</span><span class="sxs-lookup"><span data-stu-id="e2eca-233">kaks</span></span></td>
<td><span data-ttu-id="e2eca-234">Las sílabas hangul se mantienen en la normalización.</span><span class="sxs-lookup"><span data-stu-id="e2eca-234">Hangul syllables are maintained under normalization.</span></span> <span data-ttu-id="e2eca-235">En versiones anteriores de Unicode, los caracteres Jamo como KS <sub>f</sub> tenían asignaciones de compatibilidad a k <sub>f</sub> + s. <sub></sub></span><span class="sxs-lookup"><span data-stu-id="e2eca-235">In earlier Unicode versions, jamo characters like ks <sub>f</sub> had compatibility mappings to k <sub>f</sub> + s <sub>f</sub>.</span></span> <span data-ttu-id="e2eca-236">Estas asignaciones se quitaron en Unicode 2.1.9 para asegurarse de que se mantienen las sílabas hangul.</span><span class="sxs-lookup"><span data-stu-id="e2eca-236">These mappings were removed in Unicode 2.1.9 to ensure that Hangul syllables are maintained.</span></span><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="e2eca-237">Las dos tablas anteriores tienen un copyright de © 1998-2006 Unicode, Inc. Todos los derechos reservados.</span><span class="sxs-lookup"><span data-stu-id="e2eca-237">The two tables above have a copyright of © 1998-2006 Unicode, Inc. All Rights Reserved.</span></span>

 

## <a name="use-composed-forms-for-single-glyphs"></a><span data-ttu-id="e2eca-238">Usar formularios compuestos para glifos únicos</span><span class="sxs-lookup"><span data-stu-id="e2eca-238">Use Composed Forms for Single Glyphs</span></span>

<span data-ttu-id="e2eca-239">Muchas secuencias de caracteres que corresponden a un solo glifo no tienen formas compuestas.</span><span class="sxs-lookup"><span data-stu-id="e2eca-239">Many character sequences that correspond to a single glyph do not have composed forms.</span></span> <span data-ttu-id="e2eca-240">Incluso cuando se normaliza con el formulario C, un solo glifo visual o elemento de texto lógico pueden estar compuestos de varios puntos de código Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2eca-240">Even when normalized by form C, a single visual glyph or logical text element can be composed of multiple Unicode code points.</span></span> <span data-ttu-id="e2eca-241">Por ejemplo, varios caracteres usados al escribir Lituano tienen signos de dos dobles, ya que solo tienen formularios descompuestos.</span><span class="sxs-lookup"><span data-stu-id="e2eca-241">For example, several characters used in writing Lithuanian have double diacritics, as they have only decomposed forms.</span></span> <span data-ttu-id="e2eca-242">Un ejemplo es una U minúscula con Macron y tildes ("ū̃", U + 016B U + 0303, donde el primer punto de código es una U minúscula con Macron y el segundo es un acento agudo de combinación).</span><span class="sxs-lookup"><span data-stu-id="e2eca-242">An example is lowercase U with macron and tilde ("ū̃", U+016b U+0303, where the first code point is a lowercase U with macron and the second is a combining acute accent).</span></span>

## <a name="example"></a><span data-ttu-id="e2eca-243">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2eca-243">Example</span></span>

<span data-ttu-id="e2eca-244">Un ejemplo relevante puede encontrarse en [NLS: ejemplo de normalización Unicode](nls--unicode-normalization-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e2eca-244">A relevant example can be found in [NLS: Unicode Normalization Sample](nls--unicode-normalization-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2eca-245">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2eca-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2eca-246">Uso de la compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="e2eca-246">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="e2eca-247">Consideraciones de seguridad: características internacionales</span><span class="sxs-lookup"><span data-stu-id="e2eca-247">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> <dt>

[<span data-ttu-id="e2eca-248">**IsNormalizedString**</span><span class="sxs-lookup"><span data-stu-id="e2eca-248">**IsNormalizedString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[<span data-ttu-id="e2eca-249">**NormalizeString**</span><span class="sxs-lookup"><span data-stu-id="e2eca-249">**NormalizeString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 





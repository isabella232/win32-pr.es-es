---
title: Cadenas
description: En esta sección se describen las funciones de cadena.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- recursos, cadenas
- cadenas
- funciones de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795225"
---
# <a name="strings"></a><span data-ttu-id="7007c-106">Cadenas</span><span class="sxs-lookup"><span data-stu-id="7007c-106">Strings</span></span>

<span data-ttu-id="7007c-107">En esta sección se describen las funciones de cadena y se explica cómo usarlas en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7007c-107">This section describes the string functions and explains how to use them in your applications.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="7007c-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7007c-108">In This Section</span></span>



| <span data-ttu-id="7007c-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="7007c-109">Name</span></span>                                     | <span data-ttu-id="7007c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7007c-110">Description</span></span>                                             |
|------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="7007c-111">Acerca de las cadenas</span><span class="sxs-lookup"><span data-stu-id="7007c-111">About Strings</span></span>](about-strings.md)       | <span data-ttu-id="7007c-112">Describe las funciones de cadena.</span><span class="sxs-lookup"><span data-stu-id="7007c-112">Discusses the string functions.</span></span><br/>              |
| [<span data-ttu-id="7007c-113">Acerca de strsafe. h</span><span class="sxs-lookup"><span data-stu-id="7007c-113">About Strsafe.h</span></span>](strsafe-ovw.md)       | <span data-ttu-id="7007c-114">Describe las funciones de cadena en strsafe. h.</span><span class="sxs-lookup"><span data-stu-id="7007c-114">Discusses the string functions in Strsafe.h.</span></span><br/> |
| [<span data-ttu-id="7007c-115">Referencia de cadena</span><span class="sxs-lookup"><span data-stu-id="7007c-115">String Reference</span></span>](string-reference.md) | <span data-ttu-id="7007c-116">Contiene la referencia de la API.</span><span class="sxs-lookup"><span data-stu-id="7007c-116">Contains the API reference.</span></span><br/>                  |



 

### <a name="string-functions"></a><span data-ttu-id="7007c-117">Funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="7007c-117">String Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7007c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="7007c-118">Name</span></span></th>
<th><span data-ttu-id="7007c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7007c-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7007c-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span></span></td>
<td><span data-ttu-id="7007c-121">Convierte una cadena de caracteres o un carácter individual en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7007c-121">Converts a character string or a single character to lowercase.</span></span> <span data-ttu-id="7007c-122">Si el operando es una cadena de caracteres, la función convierte los caracteres en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7007c-122">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span></span></td>
<td><span data-ttu-id="7007c-124">Convierte los caracteres en mayúsculas de un búfer en caracteres en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7007c-124">Converts uppercase characters in a buffer to lowercase characters.</span></span> <span data-ttu-id="7007c-125">La función convierte los caracteres en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7007c-125">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span></span></td>
<td><span data-ttu-id="7007c-127">Recupera un puntero al siguiente carácter de una cadena.</span><span class="sxs-lookup"><span data-stu-id="7007c-127">Retrieves a pointer to the next character in a string.</span></span> <span data-ttu-id="7007c-128">Esta función puede controlar cadenas que se componen de caracteres de un solo byte o de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="7007c-128">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span></span></td>
<td><span data-ttu-id="7007c-130">Recupera el puntero al siguiente carácter de una cadena.</span><span class="sxs-lookup"><span data-stu-id="7007c-130">Retrieves the pointer to the next character in a string.</span></span> <span data-ttu-id="7007c-131">Esta función puede controlar cadenas que se componen de caracteres de un solo byte o de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="7007c-131">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span></span></td>
<td><span data-ttu-id="7007c-133">Recupera un puntero al carácter anterior en una cadena.</span><span class="sxs-lookup"><span data-stu-id="7007c-133">Retrieves a pointer to the preceding character in a string.</span></span> <span data-ttu-id="7007c-134">Esta función puede controlar cadenas que se componen de caracteres de un solo byte o de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="7007c-134">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span></span></td>
<td><span data-ttu-id="7007c-136">Recupera el puntero al carácter anterior en una cadena.</span><span class="sxs-lookup"><span data-stu-id="7007c-136">Retrieves the pointer to the preceding character in a string.</span></span> <span data-ttu-id="7007c-137">Esta función puede controlar cadenas que se componen de caracteres de un solo byte o de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="7007c-137">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span></span></td>
<td><span data-ttu-id="7007c-139">Convierte una cadena en el juego de caracteres definido por el OEM.</span><span class="sxs-lookup"><span data-stu-id="7007c-139">Translates a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span></span></td>
<td><span data-ttu-id="7007c-141">Convierte un número especificado de caracteres de una cadena en el juego de caracteres definido por el OEM.</span><span class="sxs-lookup"><span data-stu-id="7007c-141">Translates a specified number of characters in a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span></span></td>
<td><span data-ttu-id="7007c-143">Convierte una cadena de caracteres o un carácter individual en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="7007c-143">Converts a character string or a single character to uppercase.</span></span> <span data-ttu-id="7007c-144">Si el operando es una cadena de caracteres, la función convierte los caracteres en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7007c-144">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span></span></td>
<td><span data-ttu-id="7007c-146">Convierte los caracteres en minúsculas de un búfer en caracteres en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="7007c-146">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="7007c-147">La función convierte los caracteres en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7007c-147">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span></span></td>
<td><span data-ttu-id="7007c-149">Compara dos cadenas de caracteres con la configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-149">Compares two character strings, using the specified locale.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7007c-150">Para ofrecer compatibilidad con Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> o la versión Unicode de <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7007c-150">For compatibility with Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> or the Unicode version of <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span></span></td>
<td><span data-ttu-id="7007c-152">Compara dos cadenas Unicode (caracteres anchos) con la configuración regional especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-152">Compares two Unicode (wide character) strings, using the specified locale.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span></span></td>
<td><span data-ttu-id="7007c-154">Asigna una cadena a otra, realizando una opción de transformación especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-154">Maps one string to another, performing a specified transformation option.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span></span></td>
<td><span data-ttu-id="7007c-156">Recupera información de tipo de carácter de los caracteres de la cadena de origen especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-156">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="7007c-157">Para cada carácter de la cadena, la función establece uno o varios bits en el elemento de 16 bits correspondiente de la matriz de salida.</span><span class="sxs-lookup"><span data-stu-id="7007c-157">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="7007c-158">Cada bit identifica un tipo de carácter determinado, como si el carácter es una letra, un dígito o ninguno de los dos.</span><span class="sxs-lookup"><span data-stu-id="7007c-158">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span></span></td>
<td><span data-ttu-id="7007c-160">Recupera información de tipo de carácter de los caracteres de la cadena de origen especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-160">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="7007c-161">Para cada carácter de la cadena, la función establece uno o varios bits en el elemento de 16 bits correspondiente de la matriz de salida.</span><span class="sxs-lookup"><span data-stu-id="7007c-161">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="7007c-162">Cada bit identifica un tipo de carácter determinado, como si el carácter es una letra, un dígito o ninguno de los dos.</span><span class="sxs-lookup"><span data-stu-id="7007c-162">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span> <br/> <span data-ttu-id="7007c-163">A diferencia de sus parientes cercanos <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> y <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exhibe un comportamiento estándar mediante el uso del modificador de <strong> # definición de Unicode</strong> .</span><span class="sxs-lookup"><span data-stu-id="7007c-163">Unlike its close relatives <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exhibits standard behavior through the use of the <strong>#define UNICODE</strong> switch.</span></span> <span data-ttu-id="7007c-164">Es la función recomendada.</span><span class="sxs-lookup"><span data-stu-id="7007c-164">It is the recommended function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span></span></td>
<td><span data-ttu-id="7007c-166">Recupera información de tipo de carácter de los caracteres de la cadena de origen especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-166">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="7007c-167">Para cada carácter de la cadena, la función establece uno o varios bits en el elemento de 16 bits correspondiente de la matriz de salida.</span><span class="sxs-lookup"><span data-stu-id="7007c-167">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="7007c-168">Cada bit identifica un tipo de carácter determinado, como si el carácter es una letra, un dígito o ninguno de los dos.</span><span class="sxs-lookup"><span data-stu-id="7007c-168">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span></span></td>
<td><span data-ttu-id="7007c-170">Determina si un carácter es un carácter alfabético.</span><span class="sxs-lookup"><span data-stu-id="7007c-170">Determines whether a character is an alphabetical character.</span></span> <span data-ttu-id="7007c-171">Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="7007c-171">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span></span></td>
<td><span data-ttu-id="7007c-173">Determina si un carácter es un carácter alfabético o numérico.</span><span class="sxs-lookup"><span data-stu-id="7007c-173">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="7007c-174">Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="7007c-174">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span></span></td>
<td><span data-ttu-id="7007c-176">Determina si un carácter está en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7007c-176">Determines whether a character is lowercase.</span></span> <span data-ttu-id="7007c-177">Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="7007c-177">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span></span></td>
<td><span data-ttu-id="7007c-179">Determina si un carácter está en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="7007c-179">Determines whether a character is uppercase.</span></span> <span data-ttu-id="7007c-180">Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="7007c-180">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>Fall</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span></span></td>
<td><span data-ttu-id="7007c-182">Carga un recurso de cadena desde el archivo ejecutable asociado a un módulo especificado, copia la cadena en un búfer y anexa un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="7007c-182">Loads a string resource from the executable file associated with a specified module, copies the string into a buffer, and appends a terminating NULL character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span></span></td>
<td><span data-ttu-id="7007c-184">Anexa una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-184">Appends one string to another.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span></span></td>
<td><span data-ttu-id="7007c-186">Compara dos cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7007c-186">Compares two character strings.</span></span> <span data-ttu-id="7007c-187">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7007c-187">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span></span></td>
<td><span data-ttu-id="7007c-189">Compara dos cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7007c-189">Compares two character strings.</span></span> <span data-ttu-id="7007c-190">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7007c-190">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span></span></td>
<td><span data-ttu-id="7007c-192">Copia una cadena en un búfer.</span><span class="sxs-lookup"><span data-stu-id="7007c-192">Copies a string to a buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span></span></td>
<td><span data-ttu-id="7007c-194">Copia un número especificado de caracteres de una cadena de origen en un búfer.</span><span class="sxs-lookup"><span data-stu-id="7007c-194">Copies a specified number of characters from a source string into a buffer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span></span></td>
<td><span data-ttu-id="7007c-196">Determina la longitud de la cadena especificada (sin incluir el carácter nulo de terminación).</span><span class="sxs-lookup"><span data-stu-id="7007c-196">Determines the length of the specified string (not including the terminating null character).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span></span></td>
<td><span data-ttu-id="7007c-198">Convierte una cadena del juego de caracteres definido por el OEM en una cadena ANSI o de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="7007c-198">Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span></span></td>
<td><span data-ttu-id="7007c-200">Convierte un número especificado de caracteres de una cadena del juego de caracteres definido por el OEM en una cadena ANSI o de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="7007c-200">Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7007c-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span></span></td>
<td><span data-ttu-id="7007c-202">Escribe datos con formato en el búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="7007c-202">Writes formatted data to the specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7007c-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="7007c-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span></span></td>
<td><span data-ttu-id="7007c-204">Escribe datos con formato en el búfer especificado mediante un puntero a una lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="7007c-204">Writes formatted data to the specified buffer using a pointer to a list of arguments.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a><span data-ttu-id="7007c-205">Funciones strsafe</span><span class="sxs-lookup"><span data-stu-id="7007c-205">Strsafe Functions</span></span>



| <span data-ttu-id="7007c-206">Nombre</span><span class="sxs-lookup"><span data-stu-id="7007c-206">Name</span></span>                                             | <span data-ttu-id="7007c-207">Descripción</span><span class="sxs-lookup"><span data-stu-id="7007c-207">Description</span></span>                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7007c-208">**StringCbCat**</span><span class="sxs-lookup"><span data-stu-id="7007c-208">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | <span data-ttu-id="7007c-209">Concatena una cadena en otra cadena.</span><span class="sxs-lookup"><span data-stu-id="7007c-209">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="7007c-210">**StringCbCatEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-210">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | <span data-ttu-id="7007c-211">Concatena una cadena en otra cadena.</span><span class="sxs-lookup"><span data-stu-id="7007c-211">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="7007c-212">**StringCbCatN**</span><span class="sxs-lookup"><span data-stu-id="7007c-212">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | <span data-ttu-id="7007c-213">Concatena el número especificado de bytes de una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-213">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="7007c-214">**StringCbCatNEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-214">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | <span data-ttu-id="7007c-215">Concatena el número especificado de bytes de una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-215">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="7007c-216">**StringCbCopy**</span><span class="sxs-lookup"><span data-stu-id="7007c-216">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | <span data-ttu-id="7007c-217">Copia una cadena en otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-217">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="7007c-218">**StringCbCopyEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-218">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | <span data-ttu-id="7007c-219">Copia una cadena en otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-219">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="7007c-220">**StringCbCopyN**</span><span class="sxs-lookup"><span data-stu-id="7007c-220">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | <span data-ttu-id="7007c-221">Copia el número especificado de bytes de una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-221">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="7007c-222">**StringCbCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-222">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | <span data-ttu-id="7007c-223">Copia el número especificado de bytes de una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-223">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="7007c-224">**StringCbGets**</span><span class="sxs-lookup"><span data-stu-id="7007c-224">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | <span data-ttu-id="7007c-225">Obtiene una línea de texto de stdin, hasta el carácter de nueva línea (' \\ n ') y lo incluye.</span><span class="sxs-lookup"><span data-stu-id="7007c-225">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="7007c-226">**StringCbGetsEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-226">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | <span data-ttu-id="7007c-227">Obtiene una línea de texto de stdin, hasta el carácter de nueva línea (' \\ n ') y lo incluye.</span><span class="sxs-lookup"><span data-stu-id="7007c-227">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="7007c-228">**StringCbLength**</span><span class="sxs-lookup"><span data-stu-id="7007c-228">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | <span data-ttu-id="7007c-229">Determina si una cadena supera la longitud especificada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7007c-229">Determines whether a string exceeds the specified length, in bytes.</span></span><br/>                   |
| [<span data-ttu-id="7007c-230">**StringCbPrintf**</span><span class="sxs-lookup"><span data-stu-id="7007c-230">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | <span data-ttu-id="7007c-231">Escribe datos con formato en la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-231">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="7007c-232">**StringCbPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-232">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | <span data-ttu-id="7007c-233">Escribe datos con formato en la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-233">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="7007c-234">**StringCbVPrintf**</span><span class="sxs-lookup"><span data-stu-id="7007c-234">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | <span data-ttu-id="7007c-235">Escribe datos con formato en la cadena especificada utilizando un puntero a una lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="7007c-235">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="7007c-236">**StringCbVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-236">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | <span data-ttu-id="7007c-237">Escribe datos con formato en la cadena especificada utilizando un puntero a una lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="7007c-237">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="7007c-238">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="7007c-238">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | <span data-ttu-id="7007c-239">Concatena una cadena en otra cadena.</span><span class="sxs-lookup"><span data-stu-id="7007c-239">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="7007c-240">**StringCchCatEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-240">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | <span data-ttu-id="7007c-241">Concatena una cadena en otra cadena.</span><span class="sxs-lookup"><span data-stu-id="7007c-241">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="7007c-242">**StringCchCatN**</span><span class="sxs-lookup"><span data-stu-id="7007c-242">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | <span data-ttu-id="7007c-243">Concatena el número especificado de caracteres de una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-243">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="7007c-244">**StringCchCatNEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-244">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | <span data-ttu-id="7007c-245">Concatena el número especificado de caracteres de una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-245">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="7007c-246">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="7007c-246">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | <span data-ttu-id="7007c-247">Copia una cadena en otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-247">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="7007c-248">**StringCchCopyEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-248">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | <span data-ttu-id="7007c-249">Copia una cadena en otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-249">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="7007c-250">**StringCchCopyN**</span><span class="sxs-lookup"><span data-stu-id="7007c-250">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | <span data-ttu-id="7007c-251">Copia el número especificado de caracteres de una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-251">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="7007c-252">**StringCchCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-252">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | <span data-ttu-id="7007c-253">Copia el número especificado de caracteres de una cadena a otra.</span><span class="sxs-lookup"><span data-stu-id="7007c-253">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="7007c-254">**StringCchGets**</span><span class="sxs-lookup"><span data-stu-id="7007c-254">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | <span data-ttu-id="7007c-255">Obtiene una línea de texto de stdin, hasta el carácter de nueva línea (' \\ n ') y lo incluye.</span><span class="sxs-lookup"><span data-stu-id="7007c-255">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="7007c-256">**StringCchGetsEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-256">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | <span data-ttu-id="7007c-257">Obtiene una línea de texto de stdin, hasta el carácter de nueva línea (' \\ n ') y lo incluye.</span><span class="sxs-lookup"><span data-stu-id="7007c-257">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="7007c-258">**StringCchLength**</span><span class="sxs-lookup"><span data-stu-id="7007c-258">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | <span data-ttu-id="7007c-259">Determina si una cadena supera la longitud especificada, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="7007c-259">Determines whether a string exceeds the specified length, in characters.</span></span><br/>              |
| [<span data-ttu-id="7007c-260">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="7007c-260">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | <span data-ttu-id="7007c-261">Escribe datos con formato en la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-261">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="7007c-262">**StringCchPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-262">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | <span data-ttu-id="7007c-263">Escribe datos con formato en la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="7007c-263">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="7007c-264">**StringCchVPrintf**</span><span class="sxs-lookup"><span data-stu-id="7007c-264">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | <span data-ttu-id="7007c-265">Escribe datos con formato en la cadena especificada utilizando un puntero a una lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="7007c-265">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="7007c-266">**StringCchVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="7007c-266">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | <span data-ttu-id="7007c-267">Escribe datos con formato en la cadena especificada utilizando un puntero a una lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="7007c-267">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |



 

 


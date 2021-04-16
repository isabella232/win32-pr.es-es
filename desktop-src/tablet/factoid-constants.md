---
description: Define valores de cadena constantes que se usan para aumentar la precisión del reconocimiento proporcionando información contextual al reconocedor.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Constantes Factoid (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1353a4989ddfb5af3865788c0fa7fdc2d377f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542150"
---
# <a name="factoid-constants"></a><span data-ttu-id="913d0-103">Constantes de Factoid</span><span class="sxs-lookup"><span data-stu-id="913d0-103">Factoid Constants</span></span>

<span data-ttu-id="913d0-104">Define valores de cadena constantes que se usan para aumentar la precisión del reconocimiento proporcionando información contextual al reconocedor.</span><span class="sxs-lookup"><span data-stu-id="913d0-104">Defines constant string values that are used to increase recognition accuracy by providing contextual information to the recognizer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="913d0-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="913d0-105">Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="913d0-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="913d0-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <span data-ttu-id="913d0-107"><dt><strong>FACTOID_NONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-107"><dt><strong>FACTOID_NONE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-108">Deshabilita todos los demás Factoids y diccionarios.</span><span class="sxs-lookup"><span data-stu-id="913d0-108">Disables all other factoids and dictionaries.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <span data-ttu-id="913d0-109"><dt><strong>FACTOID_DEFAULT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-109"><dt> <strong>FACTOID_DEFAULT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-110">La configuración predeterminada de Factoids para idiomas occidentales incluye el Diccionario del sistema, el Diccionario del usuario, varios signos de puntuación, y el Web y el número Factoid.</span><span class="sxs-lookup"><span data-stu-id="913d0-110">The Default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the Web and Number factoid.</span></span> <span data-ttu-id="913d0-111">La configuración predeterminada de Factoids para idiomas de Asia oriental incluye todos los caracteres admitidos por el reconocedor.</span><span class="sxs-lookup"><span data-stu-id="913d0-111">The Default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <span data-ttu-id="913d0-112"><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-112"><dt> <strong>FACTOID_SYSTEMDICTIONARY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-113">Indica a un reconocedor que use solo el Diccionario del sistema.</span><span class="sxs-lookup"><span data-stu-id="913d0-113">Indicates to a recognizer to use the system dictionary only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <span data-ttu-id="913d0-114"><dt><strong>FACTOID_WORDLIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-114"><dt> <strong>FACTOID_WORDLIST</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-115">Indica a un reconocedor que utilice una lista de palabras definida mediante programación.</span><span class="sxs-lookup"><span data-stu-id="913d0-115">Indicates to a recognizer to use a programmatically-defined list of words.</span></span> <span data-ttu-id="913d0-116">La lista de palabras se define mediante la <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>propiedad de lista de palabras de</strong></a> un objeto <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="913d0-116">The list of words is defined by the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> property of a <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="913d0-117">Si se agrega una cadena a una lista de palabras, las versiones en mayúsculas también se agregan implícitamente.</span><span class="sxs-lookup"><span data-stu-id="913d0-117">If a string is added to a word list, its capitalized versions are also implicitly added.</span></span> <span data-ttu-id="913d0-118">Por ejemplo, agregar &quot; Hello &quot; implícitamente agrega &quot; Hello &quot; y &quot; Hello &quot; .</span><span class="sxs-lookup"><span data-stu-id="913d0-118">For instance, adding &quot;hello&quot; implicitly adds &quot;Hello&quot; and &quot;HELLO&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <span data-ttu-id="913d0-119"><dt><strong>FACTOID_EMAIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-119"><dt> <strong>FACTOID_EMAIL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-120">Indica a un reconocedor que busque una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="913d0-120">Indicates to a recognizer to look for an email address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="913d0-121">Se debe usar una dirección de correo electrónico completa, como &quot; someone@example.com &quot; , para este Factoid.</span><span class="sxs-lookup"><span data-stu-id="913d0-121">A fully qualified email address, such as &quot;someone@example.com&quot;, must be used for this factoid.</span></span> <span data-ttu-id="913d0-122">No se reconoce un alias propio, como &quot; alguien &quot; .</span><span class="sxs-lookup"><span data-stu-id="913d0-122">A lone alias, such as &quot;someone&quot;, is not recognized.</span></span>
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <span data-ttu-id="913d0-123"><dt><strong>FACTOID_WEB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-123"><dt><strong>FACTOID_WEB</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-124">Indica a un reconocedor que busque una dirección Web.</span><span class="sxs-lookup"><span data-stu-id="913d0-124">Indicates to a recognizer to look for a Web address.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <span data-ttu-id="913d0-125"><dt><strong>FACTOID_ONECHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-125"><dt> <strong>FACTOID_ONECHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-126">Indica a un reconocedor que busque un solo carácter.</span><span class="sxs-lookup"><span data-stu-id="913d0-126">Indicates to a recognizer to look for a single character.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="913d0-127">Este Factoid busca cualquier carácter ANSI aislado.</span><span class="sxs-lookup"><span data-stu-id="913d0-127">This factoid looks for any isolated ANSI character.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <span data-ttu-id="913d0-128"><dt><strong>FACTOID_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-128"><dt> <strong>FACTOID_NUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-129">Indica a un reconocedor que busque un número.</span><span class="sxs-lookup"><span data-stu-id="913d0-129">Indicates to a recognizer to look for a number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="913d0-130">Los valores numéricos incluyen separadores, decimales, ordinales y otros símbolos numéricos usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="913d0-130">Numeric values include separators, decimals, ordinals and other commonly used numeric symbols.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <span data-ttu-id="913d0-131"><dt><strong>FACTOID_DIGIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-131"><dt> <strong>FACTOID_DIGIT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-132">Indica a un reconocedor que busque un solo dígito, del 0 al 9.</span><span class="sxs-lookup"><span data-stu-id="913d0-132">Indicates to a recognizer to look for a single digit, 0 through 9.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <span data-ttu-id="913d0-133"><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-133"><dt> <strong>FACTOID_NUMBERSIMPLE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-134">Proporciona un contexto numérico simple a un reconocedor.</span><span class="sxs-lookup"><span data-stu-id="913d0-134">Provides a simple numeric context to a recognizer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="913d0-135">Este Factoid no es compatible con esta versión del SDK de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="913d0-135">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <span data-ttu-id="913d0-136"><dt><strong>FACTOID_CURRENCY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-136"><dt> <strong>FACTOID_CURRENCY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-137">Indica a un reconocedor que busque caracteres que denotan un valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="913d0-137">Indicates to a recognizer to look for characters that denote a currency value.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <span data-ttu-id="913d0-138"><dt><strong>FACTOID_POSTALCODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-138"><dt> <strong>FACTOID_POSTALCODE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-139">Indica a un reconocedor que busque códigos postales.</span><span class="sxs-lookup"><span data-stu-id="913d0-139">Indicates to a recognizer to look for postal codes.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <span data-ttu-id="913d0-140"><dt><strong>FACTOID_PERCENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-140"><dt> <strong>FACTOID_PERCENT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-141">Indica a un reconocedor que busque porcentajes.</span><span class="sxs-lookup"><span data-stu-id="913d0-141">Indicates to a recognizer to look for percentages.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <span data-ttu-id="913d0-142"><dt><strong>FACTOID_DATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-142"><dt> <strong>FACTOID_DATE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-143">Indica a un reconocedor que busque caracteres que denotan una fecha.</span><span class="sxs-lookup"><span data-stu-id="913d0-143">Indicates to a recognizer to look for characters that denote a date.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <span data-ttu-id="913d0-144"><dt><strong>FACTOID_TIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-144"><dt> <strong>FACTOID_TIME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-145">Indica a un reconocedor que busque caracteres que denotan una hora.</span><span class="sxs-lookup"><span data-stu-id="913d0-145">Indicates to a recognizer to look for characters that denote a time.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <span data-ttu-id="913d0-146"><dt><strong>FACTOID_TELEPHONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-146"><dt> <strong>FACTOID_TELEPHONE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-147">Indica a un reconocedor que busque caracteres que denotan un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="913d0-147">Indicates to a recognizer to look for characters that denote a telephone number.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <span data-ttu-id="913d0-148"><dt><strong>FACTOID_FILENAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-148"><dt> <strong>FACTOID_FILENAME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-149">Indica a un reconocedor que busque caracteres que denotan un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="913d0-149">Indicates to a recognizer to look for characters that denote a file name.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <span data-ttu-id="913d0-150"><dt><strong>FACTOID_UPPERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-150"><dt> <strong>FACTOID_UPPERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-151">Indica a un reconocedor que busque un solo carácter en mayúscula: de la a a la Z.</span><span class="sxs-lookup"><span data-stu-id="913d0-151">Indicates to a recognizer to look for a single uppercase character: A through Z.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <span data-ttu-id="913d0-152"><dt><strong>FACTOID_LOWERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-152"><dt> <strong>FACTOID_LOWERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-153">Indica a un reconocedor que busque un solo carácter en minúscula: de la a a la Z.</span><span class="sxs-lookup"><span data-stu-id="913d0-153">Indicates to a recognizer to look for a single lowercase character: A through Z.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="913d0-154">Este Factoid no es compatible con esta versión del SDK de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="913d0-154">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <span data-ttu-id="913d0-155"><dt><strong>FACTOID_PUNCCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-155"><dt> <strong>FACTOID_PUNCCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-156">Indica a un reconocedor que busque caracteres de puntuación.</span><span class="sxs-lookup"><span data-stu-id="913d0-156">Indicates to a recognizer to look for punctuation characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="913d0-157">Este Factoid no es compatible con esta versión del SDK de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="913d0-157">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <span data-ttu-id="913d0-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-159">Indica a un reconocedor que busque caracteres kanji, Katakana y hiragana usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="913d0-159">Indicates to a recognizer to look for commonly used Kanji, Katakana, and Hiragana characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <span data-ttu-id="913d0-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-161">Indica a un reconocedor que busque caracteres de chino simplificado de uso frecuente.</span><span class="sxs-lookup"><span data-stu-id="913d0-161">Indicates to a recognizer to look for commonly used Simplified Chinese characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <span data-ttu-id="913d0-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-163">Indica a un reconocedor que busque caracteres de chino tradicional usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="913d0-163">Indicates to a recognizer to look for commonly used Traditional Chinese characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <span data-ttu-id="913d0-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-165">Indica a un reconocedor que busque caracteres coreanos usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="913d0-165">Indicates to a recognizer to look for commonly used Korean characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <span data-ttu-id="913d0-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-167">Indica a un reconocedor que busque únicamente caracteres hiragana.</span><span class="sxs-lookup"><span data-stu-id="913d0-167">Indicates to a recognizer to look for Hiragana characters only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <span data-ttu-id="913d0-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-169">Indica a un reconocedor que busque solo caracteres katakana.</span><span class="sxs-lookup"><span data-stu-id="913d0-169">Indicates to a recognizer to look for Katakana characters only.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <span data-ttu-id="913d0-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-171">Indica a un reconocedor que busque caracteres kanji usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="913d0-171">Indicates to a recognizer to look for commonly used kanji characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <span data-ttu-id="913d0-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-173">Indica a un reconocedor que busque caracteres kanji poco usados.</span><span class="sxs-lookup"><span data-stu-id="913d0-173">Indicates to a recognizer to look for rarely used kanji characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="913d0-174">Este Factoid no es compatible con esta versión del SDK de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="913d0-174">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <span data-ttu-id="913d0-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-176">Indica a un reconocedor que busque caracteres Bopomofo.</span><span class="sxs-lookup"><span data-stu-id="913d0-176">Indicates to a recognizer to look for Bopomofo characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <span data-ttu-id="913d0-177"><dt><strong>FACTOID_JAMO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-177"><dt><strong>FACTOID_JAMO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-178">Indica a un reconocedor que busque caracteres Jamo de compatibilidad con hangul.</span><span class="sxs-lookup"><span data-stu-id="913d0-178">Indicates to a recognizer to look for Hangul compatibility Jamo characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <span data-ttu-id="913d0-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-180">Indica a un reconocedor que busque caracteres hangul usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="913d0-180">Indicates to a recognizer to look for commonly used Hangul characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <span data-ttu-id="913d0-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="913d0-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="913d0-182">Indica a un reconocedor que busque caracteres hangul poco usados.</span><span class="sxs-lookup"><span data-stu-id="913d0-182">Indicates to a recognizer to look for rarely used Hangul characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="913d0-183">Este Factoid no es compatible con esta versión del SDK de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="913d0-183">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="913d0-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="913d0-184">Remarks</span></span>

<span data-ttu-id="913d0-185">En C++, puede tener acceso a estas constantes en el archivo de encabezado Msinkaut. h, que se encuentra en <systemdrive> el \\ Directorio: archivos de programa \\ Microsoft Tablet PC Platform SDK \\ include Si instaló el SDK en la ubicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="913d0-185">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="913d0-186">Estas constantes son WCHARs, no BSTR.</span><span class="sxs-lookup"><span data-stu-id="913d0-186">These constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="913d0-187">Deben convertirse en BSTR antes de usarse como parámetros para los métodos de objeto.</span><span class="sxs-lookup"><span data-stu-id="913d0-187">They must be converted into BSTRs before use as parameters to object methods.</span></span> <span data-ttu-id="913d0-188">Para obtener más información sobre el tipo de datos BSTR, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="913d0-188">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="913d0-189">En el caso de los reconocedores de scripts latinos, los Factoids definidos en esta clase solo se proporcionan por compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="913d0-189">For recognizers of Latin script, the factoids defined in this class are provided for backward compatibility only.</span></span> <span data-ttu-id="913d0-190">Para el nuevo desarrollo, se recomienda usar los valores definidos en la función [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) .</span><span class="sxs-lookup"><span data-stu-id="913d0-190">For new development, you are encouraged to use the values defined in the [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) function.</span></span> <span data-ttu-id="913d0-191">Para obtener más información, consulte [uso de contexto para mejorar la precisión](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="913d0-191">For details, see [Using Context to Improve Accuracy](using-context-to-improve-accuracy.md).</span></span>

 

<span data-ttu-id="913d0-192">Utilice estos identificadores para especificar qué Factoid se debe usar durante el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="913d0-192">Use these identifiers to specify which factoid should be used during recognition.</span></span>

<span data-ttu-id="913d0-193">Las siguientes combinaciones de Factoids solo se admiten para idiomas occidentales.</span><span class="sxs-lookup"><span data-stu-id="913d0-193">The following combinations of factoids are supported for western languages only.</span></span> <span data-ttu-id="913d0-194">No tienen definiciones independientes, pero son entradas de literal de cadena aceptables para la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) de los objetos que usan Factoids.</span><span class="sxs-lookup"><span data-stu-id="913d0-194">These do not have separate definitions, but are acceptable string literal inputs to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of objects that use factoids.</span></span> <span data-ttu-id="913d0-195">Estas constantes de cadena de Factoid permiten que la entrada coincida con cualquiera de los Factoids de la expresión.</span><span class="sxs-lookup"><span data-stu-id="913d0-195">These factoid string constants allow the input to match any of the factoids in the expression.</span></span>



| <span data-ttu-id="913d0-196">Combinación</span><span class="sxs-lookup"><span data-stu-id="913d0-196">Combination</span></span>               | <span data-ttu-id="913d0-197">Definición</span><span class="sxs-lookup"><span data-stu-id="913d0-197">Definition</span></span>                                                |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="913d0-198">" \| palabras Web"</span><span class="sxs-lookup"><span data-stu-id="913d0-198">"WEB\|WORDLIST"</span></span>           | <span data-ttu-id="913d0-199">La Factoid web o la lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="913d0-199">The Web factoid or the word list.</span></span>                         |
| <span data-ttu-id="913d0-200">"palabras de correo electrónico \| "</span><span class="sxs-lookup"><span data-stu-id="913d0-200">"EMAIL\|WORDLIST"</span></span>         | <span data-ttu-id="913d0-201">Factoid de correo electrónico o la lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="913d0-201">The Email factoid or the word list.</span></span>                       |
| <span data-ttu-id="913d0-202">"nombre de archivo \| Web \|</span><span class="sxs-lookup"><span data-stu-id="913d0-202">"FILENAME\|WEB\|WORDLIST"</span></span> | <span data-ttu-id="913d0-203">El nombre de archivo Factoid o la Factoid web o la lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="913d0-203">The Filename factoid or the Web factoid or the word list.</span></span> |



 

<span data-ttu-id="913d0-204">Si usa el control [InkEdit](inkedit-control-reference.md) , Factoid se puede establecer como una propiedad del control.</span><span class="sxs-lookup"><span data-stu-id="913d0-204">If you are using the [InkEdit](inkedit-control-reference.md) control, the factoid can be set as a property of the control.</span></span>

<span data-ttu-id="913d0-205">Si usa las API de la plataforma de Tablet PC, puede establecer la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) en un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="913d0-205">If you are using the Tablet PC Platform APIs, you can set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on an [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

<span data-ttu-id="913d0-206">Como alternativa, puede establecer esta propiedad con la constante de cadena Factoid real.</span><span class="sxs-lookup"><span data-stu-id="913d0-206">Alternatively, you can set this property with the actual factoid string constant.</span></span>

> [!Note]  
> <span data-ttu-id="913d0-207">Las constantes de cadena de Factoid distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="913d0-207">Factoid string constants are case sensitive.</span></span> <span data-ttu-id="913d0-208">Para obtener más información sobre Factoids y cómo usarlos, vea usar el contexto para [mejorar la precisión](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="913d0-208">For more information about factoids and how to use them, see Using Context to [Improve Accuracy](using-context-to-improve-accuracy.md).</span></span> <span data-ttu-id="913d0-209">Para determinar si un Factoid está disponible en un idioma específico, consulte [Factoids compatible de la versión 1](supported-factoids-from-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="913d0-209">To determine whether a factoid is available in a specific language, see [Supported Factoids from Version 1](supported-factoids-from-version-1.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="913d0-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="913d0-210">Requirements</span></span>



| <span data-ttu-id="913d0-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="913d0-211">Requirement</span></span> | <span data-ttu-id="913d0-212">Value</span><span class="sxs-lookup"><span data-stu-id="913d0-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="913d0-213">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="913d0-213">Minimum supported client</span></span><br/> | <span data-ttu-id="913d0-214">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="913d0-214">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="913d0-215">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="913d0-215">Minimum supported server</span></span><br/> | <span data-ttu-id="913d0-216">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="913d0-216">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="913d0-217">Encabezado</span><span class="sxs-lookup"><span data-stu-id="913d0-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="913d0-218"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="913d0-218"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913d0-219">Vea también</span><span class="sxs-lookup"><span data-stu-id="913d0-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="913d0-220">[**Propiedad Factoid \[ clase InkRecognizeContext\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="913d0-220">[**Factoid Property \[InkRecognizeContext Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="913d0-221">[**Propiedad Factoid \[ clase PenInputPanel\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="913d0-221">[**Factoid Property \[PenInputPanel Class\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="913d0-222">[**Control InkEdit de la propiedad Factoid \[\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="913d0-222">[**Factoid Property \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span></span>
</dt> <dt>

[<span data-ttu-id="913d0-223">Usar el contexto para mejorar la precisión</span><span class="sxs-lookup"><span data-stu-id="913d0-223">Using Context to Improve Accuracy</span></span>](using-context-to-improve-accuracy.md)
</dt> <dt>

[<span data-ttu-id="913d0-224">Factoids admitido de la versión 1</span><span class="sxs-lookup"><span data-stu-id="913d0-224">Supported Factoids from Version 1</span></span>](supported-factoids-from-version-1.md)
</dt> </dl>

 


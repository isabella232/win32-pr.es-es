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
# <a name="factoid-constants"></a>Constantes de Factoid

Define valores de cadena constantes que se usan para aumentar la precisión del reconocimiento proporcionando información contextual al reconocedor.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Nombre</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <dt><strong>FACTOID_NONE</strong></dt> </dl></td>
<td style="text-align: left;">Deshabilita todos los demás Factoids y diccionarios.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <dt><strong>FACTOID_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">La configuración predeterminada de Factoids para idiomas occidentales incluye el Diccionario del sistema, el Diccionario del usuario, varios signos de puntuación, y el Web y el número Factoid. La configuración predeterminada de Factoids para idiomas de Asia oriental incluye todos los caracteres admitidos por el reconocedor. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que use solo el Diccionario del sistema.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <dt><strong>FACTOID_WORDLIST</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que utilice una lista de palabras definida mediante programación. La lista de palabras se define mediante la <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>propiedad de lista de palabras de</strong></a> un objeto <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> . <br/>
<blockquote>
[!Note]<br />
Si se agrega una cadena a una lista de palabras, las versiones en mayúsculas también se agregan implícitamente. Por ejemplo, agregar &quot; Hello &quot; implícitamente agrega &quot; Hello &quot; y &quot; Hello &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <dt><strong>FACTOID_EMAIL</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque una dirección de correo electrónico.<br/>
<blockquote>
[!Note]<br />
Se debe usar una dirección de correo electrónico completa, como &quot; someone@example.com &quot; , para este Factoid. No se reconoce un alias propio, como &quot; alguien &quot; .
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <dt><strong>FACTOID_WEB</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque una dirección Web.<br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <dt><strong>FACTOID_ONECHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque un solo carácter.<br/>
<blockquote>
[!Note]<br />
Este Factoid busca cualquier carácter ANSI aislado.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <dt><strong>FACTOID_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque un número.<br/>
<blockquote>
[!Note]<br />
Los valores numéricos incluyen separadores, decimales, ordinales y otros símbolos numéricos usados con frecuencia.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <dt><strong>FACTOID_DIGIT</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque un solo dígito, del 0 al 9.<br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </dl></td>
<td style="text-align: left;">Proporciona un contexto numérico simple a un reconocedor.<br/>
<blockquote>
[!Note]<br />
Este Factoid no es compatible con esta versión del SDK de Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <dt><strong>FACTOID_CURRENCY</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres que denotan un valor de moneda.<br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <dt><strong>FACTOID_POSTALCODE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque códigos postales.<br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <dt><strong>FACTOID_PERCENT</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque porcentajes.<br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <dt><strong>FACTOID_DATE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres que denotan una fecha.<br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <dt><strong>FACTOID_TIME</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres que denotan una hora.<br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <dt><strong>FACTOID_TELEPHONE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres que denotan un número de teléfono.<br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <dt><strong>FACTOID_FILENAME</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres que denotan un nombre de archivo.<br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <dt><strong>FACTOID_UPPERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque un solo carácter en mayúscula: de la a a la Z.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <dt><strong>FACTOID_LOWERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque un solo carácter en minúscula: de la a a la Z.<br/>
<blockquote>
[!Note]<br />
Este Factoid no es compatible con esta versión del SDK de Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <dt><strong>FACTOID_PUNCCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres de puntuación.<br/>
<blockquote>
[!Note]<br />
Este Factoid no es compatible con esta versión del SDK de Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres kanji, Katakana y hiragana usados con frecuencia.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres de chino simplificado de uso frecuente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres de chino tradicional usados con frecuencia.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <dt><strong>FACTOID_KOREANCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres coreanos usados con frecuencia.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <dt><strong>FACTOID_HIRAGANA</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque únicamente caracteres hiragana.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <dt><strong>FACTOID_KATAKANA</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque solo caracteres katakana.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <dt><strong>FACTOID_KANJICOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres kanji usados con frecuencia.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <dt><strong>FACTOID_KANJIRARE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres kanji poco usados.<br/>
<blockquote>
[!Note]<br />
Este Factoid no es compatible con esta versión del SDK de Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <dt><strong>FACTOID_BOPOMOFO</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres Bopomofo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <dt><strong>FACTOID_JAMO</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres Jamo de compatibilidad con hangul.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <dt><strong>FACTOID_HANGULCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres hangul usados con frecuencia.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <dt><strong>FACTOID_HANGULRARE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un reconocedor que busque caracteres hangul poco usados.<br/>
<blockquote>
[!Note]<br />
Este Factoid no es compatible con esta versión del SDK de Tablet PC.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

En C++, puede tener acceso a estas constantes en el archivo de encabezado Msinkaut. h, que se encuentra en <systemdrive> el \\ Directorio: archivos de programa \\ Microsoft Tablet PC Platform SDK \\ include Si instaló el SDK en la ubicación predeterminada.

> [!Note]  
> Estas constantes son WCHARs, no BSTR. Deben convertirse en BSTR antes de usarse como parámetros para los métodos de objeto. Para obtener más información sobre el tipo de datos BSTR, vea [usar la biblioteca com](using-the-com-library.md).

 

> [!Note]  
> En el caso de los reconocedores de scripts latinos, los Factoids definidos en esta clase solo se proporcionan por compatibilidad con versiones anteriores. Para el nuevo desarrollo, se recomienda usar los valores definidos en la función [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) . Para obtener más información, consulte [uso de contexto para mejorar la precisión](using-context-to-improve-accuracy.md).

 

Utilice estos identificadores para especificar qué Factoid se debe usar durante el reconocimiento.

Las siguientes combinaciones de Factoids solo se admiten para idiomas occidentales. No tienen definiciones independientes, pero son entradas de literal de cadena aceptables para la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) de los objetos que usan Factoids. Estas constantes de cadena de Factoid permiten que la entrada coincida con cualquiera de los Factoids de la expresión.



| Combinación               | Definición                                                |
|---------------------------|-----------------------------------------------------------|
| " \| palabras Web"           | La Factoid web o la lista de palabras.                         |
| "palabras de correo electrónico \| "         | Factoid de correo electrónico o la lista de palabras.                       |
| "nombre de archivo \| Web \| | El nombre de archivo Factoid o la Factoid web o la lista de palabras. |



 

Si usa el control [InkEdit](inkedit-control-reference.md) , Factoid se puede establecer como una propiedad del control.

Si usa las API de la plataforma de Tablet PC, puede establecer la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) en un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) .

Como alternativa, puede establecer esta propiedad con la constante de cadena Factoid real.

> [!Note]  
> Las constantes de cadena de Factoid distinguen mayúsculas de minúsculas. Para obtener más información sobre Factoids y cómo usarlos, vea usar el contexto para [mejorar la precisión](using-context-to-improve-accuracy.md). Para determinar si un Factoid está disponible en un idioma específico, consulte [Factoids compatible de la versión 1](supported-factoids-from-version-1.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedad Factoid \[ clase InkRecognizeContext\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**Propiedad Factoid \[ clase PenInputPanel\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**Control InkEdit de la propiedad Factoid \[\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[Usar el contexto para mejorar la precisión](using-context-to-improve-accuracy.md)
</dt> <dt>

[Factoids admitido de la versión 1](supported-factoids-from-version-1.md)
</dt> </dl>

 


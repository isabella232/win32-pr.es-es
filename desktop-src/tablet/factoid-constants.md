---
description: Define valores de cadena constante que se usan para aumentar la precisión del reconocimiento proporcionando información contextual al reconocedor.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Constantes factoid (Ms ashut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa748c84f8bd39f18f83e1ec72474bcfbe3017f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883674"
---
# <a name="factoid-constants"></a>Constantes factoid

Define valores de cadena constante que se usan para aumentar la precisión del reconocimiento proporcionando información contextual al reconocedor.




| Nombre | Descripción | 
|------|-------------|
| <span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl><dt><strong>FACTOID_NONE</strong></dt></dl> | Deshabilita todos los demás factoids y diccionarios.<br /> | 
| <span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl><dt><strong>FACTOID_DEFAULT</strong></dt></dl> | La configuración Predeterminada para factoids para idiomas del oeste incluye el diccionario del sistema, el diccionario de usuarios, varias puntuaciones y el factoid Web y Number. La configuración Predeterminada para factoids para idiomas de Asia Oriental incluye todos los caracteres admitidos por el reconocedor. <br /> | 
| <span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt></dl> | Indica a un reconocedor que use solo el diccionario del sistema.<br /> | 
| <span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl><dt><strong>FACTOID_WORDLIST</strong></dt></dl> | Indica a un reconocedor que use una lista de palabras definida mediante programación. La lista de palabras se define mediante la <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>propiedad WordList</strong></a> de un <a href="inkrecognizercontext-class.md"><strong>objeto InkRecognizerContext.</strong></a> <br /><blockquote>[!Note]<br />Si se agrega una cadena a una lista de palabras, también se agregan implícitamente sus versiones en mayúsculas. Por ejemplo, agregar "hello" agrega implícitamente "Hello" y "HELLO".</blockquote><br /> | 
| <span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl><dt><strong>FACTOID_EMAIL</strong></dt></dl> | Indica a un reconocedor que busque una dirección de correo electrónico.<br /><blockquote>[!Note]<br />Se debe usar una dirección de correo electrónico completa, como someone@example.com "", para este factoid. No se reconoce un alias solo, como "alguien".</blockquote><br /><pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre> | 
| <span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl><dt><strong>FACTOID_WEB</strong></dt></dl> | Indica a un reconocedor que busque una dirección web.<br /><pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre> | 
| <span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl><dt><strong>FACTOID_ONECHAR</strong></dt></dl> | Indica a un reconocedor que busque un solo carácter.<br /><blockquote>[!Note]<br />Este factoid busca cualquier carácter ANSI aislado.</blockquote><br /> | 
| <span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl><dt><strong>FACTOID_NUMBER</strong></dt></dl> | Indica a un reconocedor que busque un número.<br /><blockquote>[!Note]<br />Los valores numéricos incluyen separadores, decimales, ordinales y otros símbolos numéricos de uso frecuente.</blockquote><br /> | 
| <span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl><dt><strong>FACTOID_DIGIT</strong></dt></dl> | Indica a un reconocedor que busque un solo dígito, de 0 a 9.<br /><pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre> | 
| <span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt></dl> | Proporciona un contexto numérico simple a un reconocedor.<br /><blockquote>[!Note]<br />Este factoid no se admite en esta versión del SDK de Tablet PC.</blockquote><br /> | 
| <span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl><dt><strong>FACTOID_CURRENCY</strong></dt></dl> | Indica a un reconocedor que busque caracteres que denotan un valor de moneda.<br /><pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre> | 
| <span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl><dt><strong>FACTOID_POSTALCODE</strong></dt></dl> | Indica a un reconocedor que busque códigos postales.<br /><pre class="syntax" data-space="preserve"><code>98112</code></pre> | 
| <span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl><dt><strong>FACTOID_PERCENT</strong></dt></dl> | Indica a un reconocedor que busque porcentajes.<br /><pre class="syntax" data-space="preserve"><code>87%</code></pre> | 
| <span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl><dt><strong>FACTOID_DATE</strong></dt></dl> | Indica a un reconocedor que busque caracteres que denotan una fecha.<br /><pre class="syntax" data-space="preserve"><code>10/30/2001, '01, 31/12, 12/99, 1999-2000</code></pre> | 
| <span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl><dt><strong>FACTOID_TIME</strong></dt></dl> | Indica a un reconocedor que busque caracteres que denotan una hora.<br /><pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre> | 
| <span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl><dt><strong>FACTOID_TELEPHONE</strong></dt></dl> | Indica a un reconocedor que busque caracteres que denotan un número de teléfono.<br /><pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre> | 
| <span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl><dt><strong>FACTOID_FILENAME</strong></dt></dl> | Indica a un reconocedor que busque caracteres que denotan un nombre de archivo.<br /><pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre> | 
| <span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl><dt><strong>FACTOID_UPPERCHAR</strong></dt></dl> | Indica a un reconocedor que busque un único carácter en mayúsculas: de la A a la Z.<br /> | 
| <span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl><dt><strong>FACTOID_LOWERCHAR</strong></dt></dl> | Indica a un reconocedor que busque un único carácter en minúsculas: de A a Z.<br /><blockquote>[!Note]<br />Este factoid no se admite en esta versión del SDK de Tablet PC.</blockquote><br /> | 
| <span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl><dt><strong>FACTOID_PUNCCHAR</strong></dt></dl> | Indica a un reconocedor que busque caracteres de puntuación.<br /><blockquote>[!Note]<br />Este factoid no se admite en esta versión del SDK de Tablet PC.</blockquote><br /> | 
| <span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl><dt><strong>FACTOID_JAPANESECOMMON</strong></dt></dl> | Indica a un reconocedor que busque caracteres Kanji, Katakana e Hiragana de uso frecuente.<br /> | 
| <span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt></dl> | Indica a un reconocedor que busque caracteres de chino simplificado usados habitualmente.<br /> | 
| <span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt></dl> | Indica a un reconocedor que busque caracteres de chino tradicional usados habitualmente.<br /> | 
| <span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl><dt><strong>FACTOID_KOREANCOMMON</strong></dt></dl> | Indica a un reconocedor que busque caracteres coreanos de uso frecuente.<br /> | 
| <span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl><dt><strong>FACTOID_HIRAGANA</strong></dt></dl> | Indica a un reconocedor que busque solo caracteres Hiragana.<br /> | 
| <span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl><dt><strong>FACTOID_KATAKANA</strong></dt></dl> | Indica a un reconocedor que busque solo caracteres Katakana.<br /> | 
| <span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl><dt><strong>FACTOID_KANJICOMMON</strong></dt></dl> | Indica a un reconocedor que busque caracteres kanji usados con frecuencia.<br /> | 
| <span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl><dt><strong>FACTOID_KANJIRARE</strong></dt></dl> | Indica a un reconocedor que busque caracteres kanji que rara vez se usan.<br /><blockquote>[!Note]<br />Este factoid no se admite en esta versión del SDK de Tablet PC.</blockquote><br /> | 
| <span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl><dt><strong>FACTOID_BOPOMOFO</strong></dt></dl> | Indica a un reconocedor que busque caracteres Bopomofo.<br /> | 
| <span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl><dt><strong>FACTOID_JAMO</strong></dt></dl> | Indica a un reconocedor que busque caracteres Jamo de compatibilidad con Hangul.<br /> | 
| <span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl><dt><strong>FACTOID_HANGULCOMMON</strong></dt></dl> | Indica a un reconocedor que busque caracteres Hangul usados habitualmente.<br /> | 
| <span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl><dt><strong>FACTOID_HANGULRARE</strong></dt></dl> | Indica a un reconocedor que busque caracteres Hangul que rara vez se usan.<br /><blockquote>[!Note]<br />Este factoid no se admite en esta versión del SDK de Tablet PC.</blockquote><br /> | 




## <a name="remarks"></a>Comentarios

En C++, puede acceder a estas constantes en el archivo de encabezado Ms ldaput.h, que se encuentra en el directorio systemdrive : Archivos de programa del SDK de la plataforma de PC para tabletas de Microsoft si instaló el SDK en la ubicación &lt; &gt; \\ \\ \\ predeterminada.

> [!Note]  
> Estas constantes son WCHAR, no BSTR. Deben convertirse en BSTR antes de usarlos como parámetros para los métodos de objeto. Para obtener más información sobre el tipo de datos BSTR, vea [Usar la biblioteca COM](using-the-com-library.md).

 

> [!Note]  
> Para los reconocedores de script latino, los factoids definidos en esta clase solo se proporcionan por compatibilidad con versiones anteriores. Para un nuevo desarrollo, se recomienda usar los valores definidos en la [función SetInputScope.](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) Para obtener más información, [vea Usar contexto para mejorar la precisión.](using-context-to-improve-accuracy.md)

 

Use estos identificadores para especificar qué factoid debe usarse durante el reconocimiento.

Las siguientes combinaciones de factoids solo se admiten en idiomas del oeste. No tienen definiciones independientes, pero son entradas literales de cadena aceptables para la [**propiedad Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) de objetos que usan factoids. Estas constantes de cadena factoid permiten que la entrada coincida con cualquiera de los factoids de la expresión.



| Combinación               | Definición                                                |
|---------------------------|-----------------------------------------------------------|
| "WEB \| WORDLIST"           | El elemento factoid web o la lista de palabras.                         |
| "EMAIL \| WORDLIST"         | El factoid de correo electrónico o la lista de palabras.                       |
| "FILENAME \| WEB \| WORDLIST" | El factoid nombre de archivo, el factoid web o la lista de palabras. |



 

Si usa el control [InkEdit,](inkedit-control-reference.md) el factoid se puede establecer como una propiedad del control .

Si usa las API de la plataforma de Tablet PC, puede establecer la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) en un [**objeto InkRecognizerContext.**](inkrecognizercontext-class.md)

Como alternativa, puede establecer esta propiedad con la constante de cadena factoid real.

> [!Note]  
> Las constantes de cadena factoid distinguen mayúsculas de minúsculas. Para obtener más información sobre los factoids y cómo usarlos, vea Usar contexto para [mejorar la precisión.](using-context-to-improve-accuracy.md) Para determinar si un factoid está disponible en un lenguaje específico, consulte [Supported Factoids from Version 1 ( Factoids admitidos de la versión 1).](supported-factoids-from-version-1.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Factoid Property \[ InkRecognizeContext (Clase)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**Factoid Property \[ PenInputPanel (clase)\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**Propiedad Factoid \[ InkEdit (control)\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[Uso del contexto para mejorar la precisión](using-context-to-improve-accuracy.md)
</dt> <dt>

[Factoids admitidos de la versión 1](supported-factoids-from-version-1.md)
</dt> </dl>

 


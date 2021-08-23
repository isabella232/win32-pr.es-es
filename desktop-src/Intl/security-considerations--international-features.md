---
description: En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con las características de soporte técnico internacional.
ms.assetid: 4034f479-ad29-4c6f-82c6-977f420c4d4d
title: 'Consideraciones de seguridad: Características internacionales'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e61566fdf51b80a76e5c8997018f35ce421dee6dd0e1b9e290888d96576249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147057"
---
# <a name="security-considerations-international-features"></a>Consideraciones de seguridad: Características internacionales

En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con las características de soporte técnico internacional. Puede usarlo como punto de partida y, a continuación, ver la documentación de la tecnología internacional de interés para las consideraciones de seguridad específicas de la tecnología.

En este tema se incluyen las siguientes secciones.

-   [Consideraciones de seguridad para las funciones de conversión de caracteres](#security-considerations-for-character-conversion-functions)
-   [Consideraciones de seguridad para las funciones de comparación](#security-considerations-for-comparison-functions)
-   [Consideraciones de seguridad para los juegos de caracteres en nombres de archivo](#security-considerations-for-character-sets-in-file-names)
-   [Consideraciones de seguridad para nombres de dominio internacionalizados](#security-considerations-for-internationalized-domain-names)
-   [Consideraciones de seguridad para las funciones ANSI](#security-considerations-for-ansi-functions)
-   [Consideraciones de seguridad para la normalización Unicode](#security-considerations-for-unicode-normalization)

## <a name="security-considerations-for-character-conversion-functions"></a>Consideraciones de seguridad para las funciones de conversión de caracteres

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) son las funciones Unicode y juego de caracteres más usadas para convertir caracteres entre ANSI y Unicode. Estas funciones tienen la posibilidad de provocar riesgos de seguridad porque cuentan los elementos de los búferes de entrada y salida de forma diferente. Por ejemplo, [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) toma un búfer de entrada en bytes y coloca los caracteres convertidos en un tamaño de búfer en caracteres Unicode. Cuando la aplicación usa esta función, debe cambiar el tamaño de los búferes correctamente para evitar una saturación del búfer.

[**WideCharToMultiByte tiene**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) como valor predeterminado la asignación de "mejor ajuste" para las páginas de códigos, como 1252. Sin embargo, este tipo de asignación permite varias representaciones de la misma cadena, lo que podría dejar a la aplicación vulnerable a ataques. Por ejemplo, la letra mayúscula de latín A con diéresis (" A") podría asignarse a la letra mayúscula de latín A ("A"); un carácter Unicode en un idioma asiático podría asignarse a una barra diagonal ("/"). Se prefiere el uso de la marca \_ WC NO BEST FIT \_ \_ \_ CHARS desde una perspectiva de seguridad.

Algunas páginas de códigos, por ejemplo, las páginas de códigos 5022x (iso-2022-x), son intrínsecamente inseguras porque permiten varias representaciones de la misma cadena. El código escrito correctamente realiza comprobaciones de seguridad en el formato Unicode, pero estos tipos de páginas de códigos amplían la susceptibilidad a ataques de las aplicaciones y se deben evitar si es posible.

## <a name="security-considerations-for-comparison-functions"></a>Consideraciones de seguridad para las funciones de comparación

Las comparaciones de cadenas pueden presentar posibles problemas de seguridad. Dado que todas las funciones de comparación son ligeramente diferentes, una función podría notificar dos cadenas como iguales, mientras que otra función podría considerarlas distintas. Las siguientes son varias funciones que las aplicaciones pueden usar para comparar cadenas:

-   [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). Compara dos cadenas de caracteres según las reglas de la configuración regional, sin diferenciar mayúsculas de minúsculas. La función compara las cadenas comprobando los primeros caracteres entre sí, los segundos caracteres entre sí, y así sucesivamente, hasta que encuentra una desigualdad o alcanza los extremos de las cadenas.
-   [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa). Compara cadenas mediante técnicas similares a las de [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). La única diferencia es que [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) realiza una comparación de cadenas que distingue mayúsculas de minúsculas.
-   [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) (Windows Vista y versiones posteriores). Realice una comparación de cadenas en una configuración regional proporcionada por la aplicación. [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) es similar a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), pero identifica una configuración regional por nombre de configuración regional [en](locale-names.md) lugar del [identificador de configuración regional](locale-identifiers.md). Estas funciones son similares a [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) y [lstrcmp,](/windows/win32/api/winbase/nf-winbase-lstrcmpa) salvo que funcionan en una configuración regional específica en lugar de en una configuración regional seleccionada por el usuario.
-   [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) (Windows Vista y versiones posteriores). Compara dos cadenas Unicode para probar la equivalencia binaria. Excepto la opción de no tener en cuenta mayúsculas de minúsculas, esta función no tiene en cuenta todas las equivalencias no [](sorting.md) binarias y comprueba la igualdad de todos los puntos de código, incluidos los puntos de código a los que no se les da ningún peso en los esquemas de ordenación lingüísticos. Tenga en cuenta que las demás funciones de comparación mencionadas en este tema no prueban la igualdad de todos los puntos de código.
-   [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) (Windows Vista y versiones posteriores). Busque una cadena Unicode en otra cadena Unicode. [**FindNLSStringEx es**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) similar a [**FindNLSString,**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)salvo que identifica una configuración regional por nombre de configuración regional en lugar de por identificador de configuración regional.
-   [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) (Windows 7 y versiones posteriores). Busca una cadena Unicode en otra cadena Unicode. La aplicación debe usar esta función en lugar de [**FindNLSString para**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) todas las comparaciones no lingüísticas.

Al [igual que lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) [y lstrcmp,](/windows/win32/api/winbase/nf-winbase-lstrcmpa) [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) evalúa las cadenas carácter a carácter. Sin embargo, muchos idiomas tienen elementos de varios caracteres, por ejemplo, el elemento de dos caracteres "CH" en español tradicional. Dado [**que CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) usa la configuración regional que ofrece la aplicación para identificar elementos de varios caracteres y [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) y [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) usan la configuración regional del subproceso, es posible que cadenas idénticas no se comparen como iguales.

[**CompareString omite**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) los caracteres no definidos y, por tanto, devuelve cero (que indica cadenas iguales) para muchos pares de cadenas que son bastante distintos. Una cadena puede contener valores que no se asignan a ningún carácter o pueden contener caracteres con semántica fuera del dominio de la aplicación, como caracteres de control en una dirección URL. Las aplicaciones que usan esta función deben proporcionar controladores de errores y cadenas de prueba para asegurarse de que son válidas antes de usarlos.

> [!Note]  
> Para Windows Vista y versiones posteriores, [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) es similar a [**CompareString.**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) Los problemas de seguridad son idénticos para estas funciones.

 

Se aplican problemas de seguridad similares a las funciones, [**como FindNLSString,**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)que hacen comparaciones implícitas. Según las marcas establecidas, los resultados de llamar a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) para buscar una cadena dentro de otra cadena pueden diferir considerablemente.

> [!Note]  
> Para Windows Vista y versiones posteriores, [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) es similar a [**FindNLSString.**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) Los problemas de seguridad son idénticos para estas funciones.

 

## <a name="security-considerations-for-character-sets-in-file-names"></a>Consideraciones de seguridad para los juegos de caracteres en nombres de archivo

Windows página de códigos y los juegos de caracteres OEM que se usan en sistemas en japonés contienen el símbolo Yen ():) en lugar de una barra diagonal inversa ( \\ ). Por lo tanto, el carácter Yen es un carácter prohibido para los sistemas de archivos NTFS y FAT. Al asignar Unicode a una página de códigos en japonés, las funciones de conversión asignan la barra diagonal inversa (U+005C) y el símbolo Yen Unicode normal (U+00A5) a este mismo carácter. Por motivos de seguridad, las aplicaciones normalmente no deben permitir el carácter U+00A5 en una cadena Unicode que se pueda convertir para su uso como nombre de archivo FAT.

## <a name="security-considerations-for-internationalized-domain-names"></a>Consideraciones de seguridad para nombres de dominio internacionalizados

Los nombres de dominio internacionalizados (IDN) se especifican mediante el grupo de trabajo de red [RFC 3490:](http://www.faqs.org/rfcs/rfc3490.html)Internacionalización de nombres de dominio en aplicaciones (IDNA). El estándar presenta una serie de problemas de seguridad.

Los glifos que representan determinados caracteres de scripts diferentes pueden parecer similares o incluso idénticos. Por ejemplo, en muchas fuentes, la minúscula cirílica A ("a") no se puede diferenciar de la minúscula latín A ("a"). No hay ninguna manera de decir visualmente que "example.com" y "example.com" son dos nombres de dominio diferentes, uno con una minúscula A en el nombre y la otra con una minúscula cirílica A. Un sitio host sin escrúpulos puede usar esta ambigüedad visual para pretender ser otro sitio en un ataque de suplantación.

El juego de caracteres extendido que IDNA permite para los IDN también tiene potencial de suplantación dentro de un script determinado. Por ejemplo, hay un gran parecido entre el guion menos ("-" U+002D), el guion ("—" U+2010), el guion sin separación ("-" U+2011), el guion de la figura ("\u2012" U+2012), el guion en ("–" U+2013) y el signo menos ("−" U+2212).

Problemas similares surgen de determinadas composiciones de compatibilidad. Por ejemplo, el único carácter Unicode NUMBER TWENTY FULL STOP ("20.", U+249B) se convierte en "20". (U+0032 U+0030 U+002E) en un paso NamePrep, antes de la conversión a Punycode. En otras palabras, esta composición inserta un punto (detención completa). Estas composiciones tienen potencial de suplantación.

La combinación de scripts diferentes en un IDN no indica necesariamente suplantación de identidad o intención falsa. Informe técnico [ \# 36:](https://www.unicode.org/reports/tr36/#international_domain_names) Consideraciones de seguridad Unicode proporciona varios ejemplos de identificadores razonables que contienen una combinación de scripts, como XML-.com (" 囍ଥ" es ruso para "documentos").

Los ataques de suplantación de identidad no están restringidos a los IDN. Por ejemplo, "rnicrosoft.com" se parece mucho a "microsoft.com", pero es un nombre ASCII. Además, se puede realizar un ataque de suplantación por daños en un nombre. Agregar etiquetas adicionales después de un nombre de marca conocido, o incluir el nombre de marca en la ruta de acceso de una dirección URL etiquetada como segura, puede confundir a los usuarios principiantes, independientemente del uso del IDN. En algunas configuraciones regionales, los IDN son necesarios y el formato Punycode de estos nombres es inaceptable, ya que hace que los nombres parezcan de tipo "sin sentido".

Para obtener más información sobre los problemas de seguridad mencionados aquí, además de un gran número de otros problemas relevantes para IDNA, vea [Technical Report \# 36: Unicode Security Considerations](https://www.unicode.org/reports/tr36/#international_domain_names). Junto con discusiones detalladas sobre los problemas de seguridad relacionados con IDNA, este informe ofrece sugerencias para tratar con identificadores sospechosos en las aplicaciones.

## <a name="security-considerations-for-ansi-functions"></a>Consideraciones de seguridad para las funciones ANSI

> [!Note]  
> Se recomienda usar Unicode en las aplicaciones globalizadas, especialmente en las nuevas, si es posible. Debe usar funciones ANSI solo si tiene motivos de reemplazo para no usar Unicode, por ejemplo, la conformidad con un protocolo anterior que no admite Unicode.

 

Muchas funciones de National Language Support (NLS), como [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) y [**GetCalendarInfo,**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)tienen versiones ANSI específicas, en este caso, **GetLocaleInfoA** y **GetCalendarInfoA,** respectivamente. Cuando la aplicación usa la versión ANSI de una función con un sistema operativo basado en Unicode, como Windows NT, Windows 2000, Windows XP o Windows Vista, la función puede producir resultados indefinidos. Si tiene una razón atractiva para usar funciones ANSI con este tipo de sistema operativo, asegúrese de que los datos pasados por la aplicación son válidos para ANSI.

## <a name="security-considerations-for-unicode-normalization"></a>Consideraciones de seguridad para la normalización Unicode

Puesto que la normalización Unicode puede cambiar la forma de una cadena, los mecanismos de seguridad o los algoritmos de validación de caracteres normalmente se deben implementar después de la normalización. Por ejemplo, considere una aplicación con una interfaz web que acepta un nombre de archivo, pero no acepta un nombre de ruta de acceso. Un U+FF43 U+FF1A U+FF3C U+FF57 U+FF49 U+FF4E U+FF44 U+FF4F U+FF57 U+FF53 cambia a `(c : \ w i n d o w s)` U+0063 U+0 01A U+003C U+0077 U+0069 U+006E U+0064 U+006F U+0077 U+0073 con normalización de KC de `(c:\windows)` forma. Si una aplicación comprueba la presencia de los caracteres de dos puntos y barra diagonal inversa antes de implementar la normalización, el resultado puede ser el acceso involuntario a archivos.

Aunque la normalización Unicode es un elemento para proteger los sistemas operativos, recuerde que la normalización no es un sustituto de una directiva de seguridad completa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Juegos de caracteres usados en nombres de archivo](character-sets-used-in-file-names.md)
</dt> <dt>

[Convenciones para Prototipos de función](conventions-for-function-prototypes.md)
</dt> <dt>

[Control de la ordenación en las aplicaciones](handling-sorting-in-your-applications.md)
</dt> <dt>

[Control de nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[Unicode](unicode.md)
</dt> </dl>

 

 

---
description: En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con las características de soporte técnico internacional.
ms.assetid: 4034f479-ad29-4c6f-82c6-977f420c4d4d
title: 'Consideraciones de seguridad: características internacionales'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb9f8b849e9fb1a07f01031832449b9c9027ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279355"
---
# <a name="security-considerations-international-features"></a>Consideraciones de seguridad: características internacionales

En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con las características de soporte técnico internacional. Puede usarlo como punto de partida y ver la documentación de la tecnología internacional de interés para las consideraciones de seguridad específicas de la tecnología.

En este tema se incluyen las siguientes secciones.

-   [Consideraciones de seguridad para las funciones de conversión de caracteres](#security-considerations-for-character-conversion-functions)
-   [Consideraciones de seguridad para las funciones de comparación](#security-considerations-for-comparison-functions)
-   [Consideraciones de seguridad para juegos de caracteres en nombres de archivo](#security-considerations-for-character-sets-in-file-names)
-   [Consideraciones de seguridad para nombres de dominio internacionalizados](#security-considerations-for-internationalized-domain-names)
-   [Consideraciones de seguridad para las funciones ANSI](#security-considerations-for-ansi-functions)
-   [Consideraciones de seguridad para la normalización Unicode](#security-considerations-for-unicode-normalization)

## <a name="security-considerations-for-character-conversion-functions"></a>Consideraciones de seguridad para las funciones de conversión de caracteres

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) son las funciones de Unicode y de juego de caracteres que se usan con más frecuencia para convertir caracteres entre ANSI y Unicode. Estas funciones tienen el potencial de provocar riesgos de seguridad porque cuentan los elementos de los búferes de entrada y salida de manera diferente. Por ejemplo, [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) toma un búfer de entrada contado en bytes y coloca los caracteres convertidos en un búfer con el tamaño de los caracteres Unicode. Cuando la aplicación usa esta función, debe cambiar el tamaño de los búferes correctamente para evitar una saturación del búfer.

[**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) tiene como valor predeterminado la asignación "mejor ajuste" para las páginas de códigos, como 1252. Sin embargo, este tipo de asignación permite varias representaciones de la misma cadena, lo que puede hacer que la aplicación sea vulnerable a ataques. Por ejemplo, la letra mayúscula latina a con diéresis ("Ä") podría asignarse a la letra mayúscula latina a ("A"); un carácter Unicode en un idioma Asiático puede asignarse a una barra diagonal ("/"). El uso de la \_ marca CT no \_ se recomiendan los \_ caracteres de ajuste no recomendado \_ es preferible desde una perspectiva de seguridad.

Algunas páginas de códigos, por ejemplo, las páginas de códigos 5022x (ISO-2022-x), son intrínsecamente inseguras porque permiten varias representaciones de la misma cadena. El código escrito correctamente realiza comprobaciones de seguridad en el formato Unicode, pero estos tipos de páginas de códigos amplían la susceptibilidad de ataque de las aplicaciones y deben evitarse si es posible.

## <a name="security-considerations-for-comparison-functions"></a>Consideraciones de seguridad para las funciones de comparación

Las comparaciones de cadenas pueden presentar problemas de seguridad. Dado que todas las funciones de comparación son ligeramente diferentes, una función podría notificar dos cadenas como iguales, mientras que otra podría considerarlas distintas. A continuación se muestran varias funciones que las aplicaciones pueden usar para comparar cadenas:

-   [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). Compara dos cadenas de caracteres según las reglas de la configuración regional, sin distinción de mayúsculas y minúsculas. La función compara las cadenas comprobando los primeros caracteres entre sí, los segundos entre sí, etc., hasta que encuentra una desigualdad o alcanza los extremos de las cadenas.
-   [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa). Compara cadenas mediante técnicas similares a las de [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). La única diferencia es que [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) realiza una comparación de cadenas que distingue entre mayúsculas y minúsculas.
-   [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) (Windows Vista y versiones posteriores). Realice una comparación de cadenas en una configuración regional proporcionada por la aplicación. [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) es similar a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), pero identifica una configuración regional por [el nombre de la configuración regional](locale-names.md) en lugar del [identificador de configuración regional](locale-identifiers.md). Estas funciones son similares a [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) y [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) , salvo que operan en una configuración regional específica en lugar de en una configuración regional seleccionada por el usuario.
-   [**Comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) (Windows Vista y versiones posteriores). Compara dos cadenas Unicode para probar la equivalencia binaria. Excepto en el caso de que no se distinga entre mayúsculas y minúsculas, esta función no tiene en cuenta todas las equivalencias no binarias y comprueba la igualdad de todos los puntos de código, incluidos los puntos de código a los que no se les da ningún peso en los esquemas de [ordenación](sorting.md) lingüísticos. Tenga en cuenta que las demás funciones de comparación mencionadas en este tema no prueban la igualdad de todos los puntos de código.
-   [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) (Windows Vista y versiones posteriores). Busque una cadena Unicode en otra cadena Unicode. [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) es similar a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), salvo que identifica una configuración regional mediante el nombre de configuración regional en lugar del identificador de configuración regional.
-   [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) (Windows 7 y versiones posteriores). Busca una cadena Unicode en otra cadena Unicode. La aplicación debe usar esta función en lugar de [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) para todas las comparaciones no lingüísticas.

Como [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) y [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) evalúa las cadenas carácter a carácter. Sin embargo, muchos lenguajes tienen elementos de varios caracteres, por ejemplo, el elemento de dos caracteres "CH" en español tradicional. Dado que [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) usa la configuración regional proporcionada por la aplicación para identificar elementos de varios caracteres y [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) y [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) usan la configuración regional del subproceso, es posible que las cadenas idénticas no se comparen como iguales.

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) omite los caracteres no definidos y, por tanto, devuelve cero (que indica cadenas iguales) para muchos pares de cadenas que son bastante distintos. Una cadena puede contener valores que no se asignan a ningún carácter o que contengan caracteres con semántica fuera del dominio de la aplicación, como los caracteres de control de una dirección URL. Las aplicaciones que utilizan esta función deben proporcionar controladores de error y cadenas de prueba para asegurarse de que son válidas antes de utilizarlas.

> [!Note]  
> En Windows Vista y versiones posteriores, [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) es similar a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). Los problemas de seguridad son idénticos para estas funciones.

 

Se aplican problemas de seguridad similares a las funciones, como [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), que realizan comparaciones implícitas. Dependiendo de las marcas que se establezcan, los resultados de llamar a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) para buscar una cadena en otra cadena pueden diferir considerablemente.

> [!Note]  
> En Windows Vista y versiones posteriores, [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) es similar a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring). Los problemas de seguridad son idénticos para estas funciones.

 

## <a name="security-considerations-for-character-sets-in-file-names"></a>Consideraciones de seguridad para juegos de caracteres en nombres de archivo

La página de códigos de Windows y los juegos de caracteres OEM utilizados en los sistemas de idioma japonés contienen el símbolo del yen (¥) en lugar de una barra diagonal inversa ( \\ ). Por lo tanto, el carácter del yen es un carácter prohibido para los sistemas de archivos NTFS y FAT. Al asignar Unicode a una página de códigos en japonés, las funciones de conversión asignan la barra diagonal inversa (U + 005C) y el símbolo de yen Unicode normal (U + 00A5) a este mismo carácter. Por motivos de seguridad, las aplicaciones no suelen permitir el carácter U + 00A5 en una cadena Unicode que podría convertirse para su uso como nombre de archivo FAT.

## <a name="security-considerations-for-internationalized-domain-names"></a>Consideraciones de seguridad para nombres de dominio internacionalizados

Los nombres de dominio internacionalizados (IDN) se especifican mediante el grupo de trabajo [de red RFC 3490: internacionalización de nombres de dominio en las aplicaciones (IDNA)](http://www.faqs.org/rfcs/rfc3490.html). El estándar presenta una serie de problemas de seguridad.

Los glifos que representan ciertos caracteres de distintos scripts pueden ser similares o incluso idénticos. Por ejemplo, en muchas fuentes, no se distinguen las minúsculas ("a") de la letra latina minúscula a ("a"). No hay ninguna manera de indicar visualmente que "example.com" y "example.com" son dos nombres de dominio diferentes, uno con latín en minúsculas en el nombre, el otro con una letra cirílica minúscula A. Un sitio host no escrupuloso puede utilizar esta ambigüedad visual para fingir que es otro sitio en un ataque de suplantación de identidad.

El juego de caracteres extendidos que el IDNA permite para IDN también tiene potencial de suplantación de identidad en un script determinado. Por ejemplo, hay un gran similitud entre el guión menos ("-" U + 002D). el guion ("-" U + 2010), el guion sin interrupción ("-" U + 2011), el guión de la figura ("\u2012" U + 2012), el guión en ("–" U + 2013) y el signo menos ("−" U + 2212).

Se producen problemas similares con ciertas composiciones de compatibilidad. Por ejemplo, el número de carácter Unicode veinte STOP completo ("20.", U + 249B) se convierte en "20". (U + 0032 U + 0030 U + 002E) en un paso NamePrep, antes de la conversión a Punycode. En otras palabras, esta composición inserta un punto (detención completa). Estas composiciones tienen potencial de suplantación de identidad.

La combinación de distintos scripts en un IDN no indica necesariamente la suplantación de identidad o la intención engañosa. [Informe técnico \# 36: las consideraciones de seguridad de Unicode](https://www.unicode.org/reports/tr36/#international_domain_names) proporcionan varios ejemplos de IDN razonables que contienen una combinación de scripts, como XML-Документы. com ("Документы" es ruso para "documentos").

Los ataques de suplantación de identidad no están restringidos a IDN. Por ejemplo, "rnicrosoft.com" es muy similar a "microsoft.com", pero es un nombre ASCII. Además, se puede producir un ataque de suplantación de identidad por daños en un nombre. Agregar etiquetas adicionales después de un nombre de marca bien conocido, o incluir el nombre de la marca en la ruta de acceso de una dirección URL etiquetada como segura, puede confundir a los usuarios inexpertos, independientemente del uso de IDN. En algunas configuraciones regionales, se requieren IDN y el formato Punycode de estos nombres no es aceptable, ya que hace que los nombres parezcan galimatíass.

Para obtener más información sobre los problemas de seguridad que se mencionan aquí, además de un gran número de problemas relacionados con IDNA, consulte el [informe técnico \# 36: consideraciones de seguridad de Unicode](https://www.unicode.org/reports/tr36/#international_domain_names). Junto con los debates detallados de los problemas de seguridad relacionados con IDNA, este informe ofrece sugerencias para tratar con los IDN sospechosos en las aplicaciones.

## <a name="security-considerations-for-ansi-functions"></a>Consideraciones de seguridad para las funciones ANSI

> [!Note]  
> Se recomienda usar Unicode en las aplicaciones globalizadas, especialmente las nuevas, si es posible. Solo debe usar funciones ANSI si tiene motivos invalidables para no usar Unicode, por ejemplo, la conformidad con un protocolo anterior que no admita Unicode.

 

Muchas funciones de compatibilidad con el idioma nacional (NLS), como [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) y [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), tienen versiones de ANSI específicas, en este caso, **GetLocaleInfoA** y **GetCalendarInfoA**, respectivamente. Cuando la aplicación usa la versión ANSI de una función con un sistema operativo basado en Unicode, como Windows NT, Windows 2000, Windows XP o Windows Vista, la función puede producir un error o generar resultados indefinidos. Si tiene una razón convincente para usar funciones ANSI con este sistema operativo, asegúrese de que los datos que pasa la aplicación sean válidos para ANSI.

## <a name="security-considerations-for-unicode-normalization"></a>Consideraciones de seguridad para la normalización Unicode

Dado que la normalización Unicode puede cambiar la forma de una cadena, los mecanismos de seguridad o los algoritmos de validación de caracteres deben implementarse normalmente después de la normalización. Por ejemplo, considere una aplicación con una interfaz web que acepte un nombre de archivo, pero que no acepte un nombre de ruta de acceso. Un cambio de ancho completo U + FF43 U + FF1A U + FF3C U + FF57 U + FF49 U + FF4E u + FF44 u + FF4F u + FF57 u + FF53 `(c : \ w i n d o w s)` cambia a u + 0063 u + 001A u + 003C u + 0077 u + 0069 u + 006E u + 0064 u + 006F u + 0077 con el `(c:\windows)` formato de la normalización de KC. Si una aplicación comprueba la presencia de los caracteres de dos puntos y la barra diagonal inversa antes de implementar la normalización, el resultado puede ser un acceso de archivo involuntario.

Aunque la normalización Unicode es un elemento de proteger los sistemas operativos, recuerde que la normalización no es un reemplazo de una directiva de seguridad completa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Juegos de caracteres usados en nombres de archivo](character-sets-used-in-file-names.md)
</dt> <dt>

[Convenciones para Prototipos de función](conventions-for-function-prototypes.md)
</dt> <dt>

[Controlar la ordenación en las aplicaciones](handling-sorting-in-your-applications.md)
</dt> <dt>

[Administrar nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[Unicode](unicode.md)
</dt> </dl>

 

 

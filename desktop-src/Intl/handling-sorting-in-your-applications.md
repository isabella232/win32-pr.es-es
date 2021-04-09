---
description: Algunas aplicaciones, como Microsoft Active Directory, Microsoft Exchange y Microsoft Access, mantienen una base de datos que se puede ordenar de las cadenas de configuración regional y de idioma indizadas por nombre (cadena UTF-16) y sus pesos de ordenación asociados.
ms.assetid: c8fc32bd-02bd-4a40-a836-d9ad9f69c209
title: Controlar la ordenación en las aplicaciones
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: c0bba3d78a5219781226ecf58292ed461c902090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913698"
---
# <a name="handling-sorting-in-your-applications"></a>Controlar la ordenación en las aplicaciones

Algunas aplicaciones, como Microsoft Active Directory, Microsoft Exchange y Microsoft Access, mantienen una base de datos que se puede ordenar de las cadenas de configuración regional y de idioma indizadas por nombre (cadena UTF-16) y sus pesos de ordenación asociados.

La [ordenación](sorting.md) suele ser intuitiva para los usuarios en sus propias configuraciones regionales. Sin embargo, puede ser no intuitivo para los desarrolladores de aplicaciones. En este tema se tratan las consideraciones para controlar la ordenación en las aplicaciones. La ordenación puede ser lingüística o ordinal (no lingüística).

## <a name="sorting-functions"></a>Funciones de ordenación

Puede usar una variedad de funciones de ordenación en las aplicaciones:

-   Funciones de comparación de cadenas NLS. Algunos ejemplos son [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)y [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal). Vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md) para obtener una explicación de los problemas de seguridad relacionados con las funciones de comparación de cadenas.
-   Funciones contenedoras que llaman internamente a las funciones de comparación de cadenas. Las funciones más comunes son [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) y [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), que llaman a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw).

Normalmente, las funciones de ordenación evalúan las cadenas carácter a carácter. Sin embargo, muchos lenguajes tienen elementos de varios caracteres, como el par de dos caracteres "CH" en español tradicional. [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) usan el identificador o el nombre de configuración regional proporcionado por la aplicación para identificar elementos de varios caracteres. Por el contrario, [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)y [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) usan la configuración regional del usuario.

Otro ejemplo es vietnamita, que contiene muchos elementos de dos caracteres, como las mayúsculas y minúsculas válidas, el caso de título y las formas en minúsculas de "GI", que son "GI", "GI" y "GI", respectivamente. Cualquiera de estas formas se trata como un elemento de ordenación único y, si se omite el uso de mayúsculas, se compara como igual. Sin embargo, dado que "gI" no es válido como un solo elemento, [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**Lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)y [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) tratan "GI" como dos elementos independientes.

Las funciones [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa), [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)y [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) usan de forma predeterminada una técnica de tipo "palabra Sort". Para este tipo de ordenación, todos los signos de puntuación y otros caracteres no alfanuméricos, excepto el guión y el apóstrofo, van antes de cualquier carácter alfanumérico. El guión y el apóstrofo se tratan de forma diferente a los demás caracteres no alfanuméricos para garantizar que las palabras como "Coop" y "Co-op" se mantienen juntas en una lista ordenada.

En lugar de una palabra, la aplicación puede solicitar una técnica de "orden de cadena" de las funciones de ordenación mediante la especificación de la \_ marca Sort STRINGSORT. Una ordenación por cadena trata el guion y el apóstrofo como cualquier otro carácter no alfanumérico. Sus posiciones en la secuencia de ordenación son anteriores a los caracteres alfanuméricos.

En la tabla siguiente se comparan los resultados de una palabra sort con los resultados de una ordenación de cadena. 

| Orden de palabras | Orden de cadena |
|-----------|-------------|
| billet    | de la factura      |
| factura     | billet      |
| de la factura    | factura       |
| no puede    | podrá       |
| suficiencia      | no puede      |
| podrá     | suficiencia        |
| timado       | Co-op       |
| cooperación      | timado         |
| Co-op     | cooperación        |



 

## <a name="sort-strings-linguistically"></a>Ordenar cadenas lingüísticamente

Las funciones [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) comprueban la igualdad lingüística. Las aplicaciones deben usar estas funciones con la configuración regional correcta para ordenar las cadenas lingüísticamente.

> [!Note]  
> Por compatibilidad con Unicode, una aplicación debe preferir [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) o la versión Unicode de [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). Otro motivo para preferir [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) es que Microsoft está migrando hacia el uso de nombres de configuración regional en lugar de identificadores de configuración regional para nuevas configuraciones regionales, por motivos de interoperabilidad. Cualquier aplicación que se ejecute solo en Windows Vista y versiones posteriores debe utilizar [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex).

 

Otra forma de probar la igualdad lingüística es usar [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) o [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), que siempre usan una palabra Sort. La función [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) llama a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) con la \_ marca Norm IGNORECASE, mientras que [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) lo llama sin esa marca. Para obtener información general sobre el uso de las funciones de contenedor, vea [**cadenas**](../menurc/strings.md).

Las funciones recuperan los resultados lingüísticamente adecuados para todas las configuraciones regionales. Las expectativas de los usuarios para diferentes configuraciones regionales pueden diferir significativamente en el comportamiento de ordenación, tal como se muestra en los ejemplos siguientes.

-   Muchas configuraciones regionales equivalen a la ligadura AE (æ) con las letras AE. Sin embargo, islandés (Islandia) considera una letra independiente y la coloca después de Z en la secuencia de ordenación.
-   Un anillo (Å) normalmente se ordena simplemente con una diferencia diacrítica de. Sin embargo, sueco (Suecia) coloca un anillo después de Z en la secuencia de ordenación.

Las funciones intentan comprobar rigurosamente que los puntos de código definidos en el estándar Unicode son canonmente iguales a una cadena de puntos de código equivalentes. Por ejemplo, el punto de código que representa una "u" minúscula con un diéresis (ü) es de forma canónica igual a una "u" minúscula combinada con el diéresis (̈). Tenga en cuenta, sin embargo, que la equivalencia canónica no siempre es posible.

Como casi todos los datos especificados mediante los teclados de Windows y los editores de métodos de entrada (IME) se ajustan a la normalización del formulario C definida en el estándar Unicode, la conversión de los datos entrantes de otras plataformas mediante las funciones de normalización de Unicode NLS proporciona resultados más coherentes, especialmente para las configuraciones regionales que usan el script tibetano o hangul Para obtener más información sobre la compatibilidad con la normalización Unicode en Windows Vista y versiones posteriores, vea [usar la normalización Unicode para representar cadenas](using-unicode-normalization-to-represent-strings.md).

Cuando la comparación de cadenas sigue a la preferencia de idioma del usuario, por ejemplo, al ordenar los elementos de un control ListView ordenado, la aplicación puede realizar una de las acciones siguientes:

-   Llame a [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) o [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) con la configuración regional del usuario.
-   Llame a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) para definir una configuración regional para la comparación, pasar marcas adicionales, insertar caracteres nulos o pasar longitudes explícitas para que coincidan con partes de una cadena.

Cuando los resultados de la comparación deben ser coherentes independientemente de la configuración regional, por ejemplo, al comparar los datos recuperados con una lista predefinida o un valor interno, la aplicación debe usar [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) con el parámetro de *configuración regional* establecido en configuración regional \_ invariable. Para [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), una de las siguientes llamadas coincidirá aunque mystr sea "INLAP". En este caso, se producirá un error en una llamada a [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) que depende de la configuración regional si la configuración regional actual es vietnamita.

En Windows XP:


```C++
int iReturn = CompareString(LOCALE_INVARIANT, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



En sistemas operativos anteriores:


```C++
DWORD lcid = MAKELCID(MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US), SORT_DEFAULT);
int iReturn = CompareString(lcid, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



## <a name="sort-strings-ordinally"></a>Ordenar cadenas ordinalmente

En el caso de la ordenación ordinal (no lingüística), las aplicaciones siempre deben usar la función [**comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) .

> [!Note]  
> Esta función solo está disponible para Windows Vista y versiones posteriores.

 

[**Comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) compara dos cadenas [Unicode](unicode.md) para comprobar la igualdad binaria, en lugar de la igualdad lingüística. Algunos ejemplos de estas cadenas no lingüísticas son los nombres de archivo NTFS, las variables de entorno y los nombres de las exclusiones mutuas, las canalizaciones con nombre o los buzones. A excepción de la opción de no distinguir mayúsculas de minúsculas, esta función no tiene en cuenta todas las equivalencias no binarias. A diferencia de otras funciones de ordenación, se prueba la igualdad de todos los puntos de código, incluidos aquellos que no tienen ningún peso en los esquemas de ordenación lingüísticos.

Todas las instrucciones siguientes se aplican a [**comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) en comparaciones binarias, pero no a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)o [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia).

-   Las secuencias canónicamente equivalentes en Unicode, como la letra latina minúscula A con anillo superior (U + 00e5) y la letra latina minúscula A + anillo inferior (U + 0061 U + 030a), no son iguales aunque parezcan idénticas ("å").
-   Cadenas parecidas de forma canónica en Unicode, como letra latina minúscula y mayúscula (U + 028f) y letra mayúscula latina y (U + 0059), que tienen un aspecto muy similar ("ʏ" e "y") y solo varían en función de algunas ponderaciones de mayúsculas y minúsculas especiales de las tablas lingüísticas, se consideran caracteres totalmente diferentes. Incluso si la aplicación establece *bIgnoreCase* en **true**, estas cadenas se comparan como diferentes.
-   Los puntos de código que se definen pero no tienen ningún peso lingüístico de ordenación, como la Unión de ancho cero (U + 200D), se tratan como si tuvieran sus pesos de punto de código.
-   Los puntos de código que se definen en versiones posteriores de Unicode pero que no tienen ningún peso en las tablas lingüísticas actuales se tratan como si tuvieran los pesos de los puntos de código.
-   Los puntos de código sin definir por Unicode se tratan como si tuvieran sus pesos de punto de código.
-   Cuando la aplicación establece *bIgnoreCase* en **true**, la función asigna el caso mediante la tabla uppercasing del sistema operativo, en lugar de la información de las tablas de ordenación lingüística. Por lo tanto, la asignación es independiente de la configuración regional.

Para obtener más información sobre las secuencias canónicamente equivalentes en Unicode y cadenas similares canónicas en Unicode, vea [usar la normalización Unicode para representar cadenas](using-unicode-normalization-to-represent-strings.md).

## <a name="sort-code-points"></a>Ordenar puntos de código

Algunos puntos de código Unicode no tienen ninguna ponderación, por ejemplo, sin separador de ancho cero U + 200C. Las funciones de ordenación evalúan intencionadamente los puntos de código sin peso como equivalentes porque no tienen ningún peso en la ordenación. En Windows Vista y versiones posteriores, la aplicación puede ordenar estos puntos de código mediante una llamada a las funciones de comparación de cadenas NLS, especialmente [**comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), para la evaluación de todos los puntos de código de un literal, un sentido binario, por ejemplo, en la validación de contraseñas. En los sistemas operativos anteriores a Windows Vista, la aplicación debe usar la función de tiempo de ejecución de C **strcmp** o **wcscmp**.

Las funciones de ordenación omiten los signos diacríticos, como un acento BREVE sin ESPACIAdo U + 0306, cuando la aplicación especifica la marca hlink no \_ espacio. Del mismo modo, estas funciones omiten los símbolos, por ejemplo, el signo igual, U + 003d, cuando \_ se especifica la marca de símbolos hlink. En Windows Vista y versiones posteriores, la aplicación llama a [**comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) para la evaluación de los signos diacríticos y los puntos de código de símbolos en un literal, una sensación binaria. En los sistemas operativos anteriores a Windows Vista, la aplicación debe usar **strcmp** o **wcscmp**.

Algunos puntos de código, como 0xFFFF y 0x058b, actualmente no están asignados en Unicode. Estos puntos de código no reciben ningún peso en la ordenación y nunca se deben pasar a las funciones de ordenación. La aplicación debe usar [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) para detectar puntos de código no Unicode en un flujo de datos.

> [!Note]  
> Los resultados de [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) pueden variar en función de la versión de Unicode pasada si se agrega un carácter a Unicode en una versión posterior y se agrega posteriormente a las tablas de ordenación de Windows. Para obtener más información, vea [usar ordenar versiones](#use-sort-versioning).

 

## <a name="sort-digits-as-numbers"></a>Ordenar dígitos como números

En Windows 7 y versiones posteriores, la aplicación puede llamar a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) mediante la \_ marca DIGITSASNUMBERS de ordenación. Esta marca admite la ordenación que trata los dígitos como números, por ejemplo, la ordenación de "2" antes de "10".

Tenga en cuenta que el uso de esta marca no es adecuado para los dígitos hexadecimales como los siguientes. <dl> 01AF  
1BCD  
002A  
12FA  
AB1C  
AB02  
AB12  
</dl>

En este caso, los "números" se ordenan en orden, pero el usuario percibe una lista hexadecimal ordenada de forma incorrecta.

## <a name="map-strings"></a>Cadenas de mapa

La aplicación utiliza la función [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) para asignar cadenas, si \_ no se especifica LCMAP SORTKEY. Una cadena asignada está terminada en NULL si la cadena de origen termina en NULL.

Al transformar entre mayúsculas y minúsculas, la función no garantiza que un carácter individual se asigne a un solo carácter. Por ejemplo, las \_ marcas de mayúsculas y minúsculas de LCMAP y LCMAP \_ pueden asignar el alemán sostenido ("ß") a sí mismo. Como alternativa, la \_ marca de mayúsculas LCMAP puede asignar "ß" a "SS" y la \_ marca LCMAP en minúsculas puede asignar "SS" a "ß". El comportamiento depende de la versión de NLS.

Al transformar entre mayúsculas y minúsculas, la función no es sensible al contexto. Por ejemplo, mientras que la marca de mayúsculas LCMAPs asigna correctamente el carácter griego en minúsculas (" \_ σ") y el Sigma final en minúsculas ("σ") al griego en mayúsculas ("σ"), la marca de LCMAP \_ en minúsculas siempre asigna "σ" a "σ", nunca a "σ".

De forma predeterminada, la función asigna la "i" minúscula a la "I" mayúscula, incluso cuando el parámetro de *configuración regional* especifica turco o azerbaiyano. Para invalidar este comportamiento para turco o azerbaiyano, la aplicación debe especificar \_ la \_ grafía lingüística LCMAP. Si esta marca se especifica con la configuración regional adecuada, "ı" (en minúsculas I sin punto) es la forma en minúsculas de "I" (en mayúsculas y minúsculas) y "i" (punteada en minúsculas) es la forma en minúsculas de "i" (en mayúsculas I).

Si \_ se especifica la marca hiragana LCMAP para asignar caracteres katakana a caracteres hiragana y \_ no se especifica LCMAP ancho de la anchura, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) solo asignan caracteres de ancho completo a hiragana. En este caso, los caracteres katakana de un ancho medio se colocan como en la cadena de destino, sin ninguna asignación a hiragana. La aplicación debe especificar LCMAP \_ ancho completo para asignar caracteres katakana de ancho medio a hiragana. La razón de esta restricción es que todos los caracteres hiragana son caracteres de ancho completo.

Si la aplicación necesita quitar caracteres de la cadena de origen, puede llamar a la función de asignación con las \_ marcas IGNORESYMBOLS y Norm \_ IGNORENONSPACE establecidas, y todas las demás marcas desactivadas. Si la aplicación realiza esta acción con una cadena de origen que no termina en null, es posible que la función devuelva una cadena vacía y no devuelva un error.

## <a name="create-sort-keys"></a>Crear claves de ordenación

Cuando la aplicación especifica LCMAP \_ SORTKEY, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) genera una clave de ordenación, una matriz binaria de valores de byte. La clave de ordenación no es una cadena verdadera y sus valores representan el comportamiento de ordenación de la cadena de origen, pero no son valores de presentación significativos.

> [!Note]  
> La función omite la kashida árabe durante la generación de un criterio de ordenación. Si una aplicación llama a la función para crear una clave de ordenación para una cadena que contiene un kashida árabe, la función no crea ningún valor de clave de ordenación.

 

La clave de ordenación puede contener un número impar de bytes. La \_ marca LCMAP BYTEREV solo invierte un número par de bytes. El último byte (posición impar) de la clave de ordenación no se revierte. Si la terminación de 0x00 es un byte impar, sigue siendo el último byte de la clave de ordenación. Si la terminación de 0x00 es un byte de posición par, intercambia posiciones con el byte que lo precede.

Al generar la clave de ordenación, la función trata el guión y el apóstrofo de forma diferente a otros símbolos de puntuación, por lo que las palabras como "Coop" y "Co-op" permanecen juntas en una lista. Todos los símbolos de puntuación distintos del guion y el apóstrofo se ordenan antes que los caracteres alfanuméricos. La aplicación puede cambiar este comportamiento estableciendo la marca SORT \_ STRINGSORT, como se describe en [funciones de ordenación](#sorting-functions).

Cuando se usa en [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp), la clave de ordenación produce el mismo orden que cuando se usa la cadena de origen en [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex). Se debe usar la función [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp) en lugar de [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp), porque la clave de ordenación puede tener bytes nulos incrustados.

## <a name="use-sort-versioning"></a>Usar el control de versiones

Una tabla de [ordenación](sorting.md) tiene dos números que identifican su versión: la versión definida y la versión NLS. Ambos números son valores DWORD, compuesto por un valor principal y un valor menor. El primer byte de un valor está reservado, los dos bytes siguientes representan la versión principal y el último byte representa la versión secundaria. En términos hexadecimales, el patrón es 0xRRMMMMmm, donde R es igual a Reserved, M es igual a Major y m es igual a Minor. Por ejemplo, una versión principal de 3 con una versión secundaria de 4 se representa como 0x304.

La versión definida identifica el repertorio de puntos de código y es el mismo para todas las configuraciones regionales. La versión principal aumenta para indicar los cambios en los puntos de código existentes. La versión secundaria incrementa para indicar que se han agregado puntos de código, pero que no se ha cambiado ningún punto de código existente previamente.

La versión de NLS es específica de un [identificador de configuración](locale-identifiers.md) regional o de un nombre de [configuración regional](locale-names.md)y realiza un seguimiento de los cambios en los pesos de los puntos de código de la configuración regional afectada. La versión principal aumenta cuando se cambian los pesos para los puntos de código que ya se pueden ordenar. La versión secundaria aumenta cuando se asignan pesos a los nuevos puntos de código, pero todos los demás pesos de puntos de código que se pueden ordenar con anterioridad permanecen inalterados.

> [!Note]  
> En el caso de una versión principal, se modifican uno o varios puntos de código para que la aplicación deba volver a indizar todos los datos para que las comparaciones sean válidas. En el caso de una versión secundaria, no se mueve nada, pero se agregan puntos de código. Para este tipo de versión, la aplicación solo tiene que volver a indexar las cadenas con valores que no se pudieron ordenar previamente.

 

> [!IMPORTANT]
> Se ha cambiado la versión principal en Windows 8. Los datos creados en versiones anteriores de Windows se deben volver a indizar.

 

Las versiones definidas y NLS se aplican a los puntos de código que se pueden ordenar y se recuperan mediante la función [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) con la \_ marca LCMAP SORTKEY y también se usan en las funciones [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)y [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) . Si uno o más puntos de código de una cadena no se pueden ordenar, la función [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) devuelve **false** cuando esa cadena se pasa como un parámetro.

La aplicación puede llamar a [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) o [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) para recuperar la versión definida y la versión NLS para una tabla de ordenación.

## <a name="index-the-database"></a>Indexación de la base de datos

Por motivos de rendimiento, la aplicación debe seguir este procedimiento al indizar la base de datos.

**Para indizar correctamente la base de datos**

1.  Para cada función, almacene la versión de NLS, las claves de ordenación de dicha versión y una indicación de la ordenación de cada cadena indizada.
2.  Cuando se incrementa la versión secundaria, se vuelven a indizar cadenas que no se pudieron ordenar previamente. Las cadenas afectadas en esta actualización se deben limitar a las que [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) ha devuelto previamente como **false**.
3.  Cuando aumente la versión principal, vuelva a indexar todas las cadenas, ya que los pesos actualizados podrían cambiar el comportamiento de cualquier cadena. Las versiones principales son muy poco frecuentes.

Los problemas de indización de bases de datos pueden surgir por los siguientes motivos:

-   Un sistema operativo posterior puede definir puntos de código sin definir para un sistema operativo anterior, con lo que se cambia la ordenación.
-   Los puntos de código pueden tener diferentes ponderaciones de ordenación en distintos sistemas operativos, debido a las correcciones de compatibilidad de idioma.

Para minimizar la necesidad de volver a indexar la base de datos en estas circunstancias, la aplicación puede utilizar [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) para diferenciar las definidas de las cadenas sin definir para que la aplicación pueda rechazar cadenas con puntos de código sin definir. El uso de [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) o [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) permite a la aplicación determinar si un cambio de NLS afecta a la configuración regional utilizada para una tabla de índice determinada. Si el cambio no tiene ningún efecto en la configuración regional, la aplicación no tiene necesidad de volver a indexar la tabla.

## <a name="examples"></a>Ejemplos

En la tabla siguiente se muestran los efectos de ciertas marcas utilizadas con las funciones de ordenación. En cada caso, la selección de marcas determina si dos caracteres diferentes se consideran iguales para la ordenación.



| Carácter 1                                                        | Carácter 2                                             | Valor predeterminado | NORMA \_ IGNOREWIDTH | NORMA \_ IGNOREKANA | NORMA \_ IGNOREWIDTH \| NORMIGNOREKANA |
|--------------------------------------------------------------------|---------------------------------------------------------|---------|-------------------|------------------|------------------------------------|
| "あ"<br/> U + 3042 LETRA HIRAGANA A<br/>                | "ガ"<br/> U + 30A2 LETRA KATAKANA A<br/>     | Iguales | Iguales           | Equal            | Equal                              |
| "ｵ"<br/> U + FF75 LETRA KATAKANA DE ANCHO MEDIO O<br/>       | "オ"<br/> U + 30AA LETRA KATAKANA O<br/>     | Iguales | Equal             | Iguales          | Equal                              |
| B<br/> U + FF22 DE ANCHO COMPLETO LATÍN LETRA MAYÚSCULA B<br/> | "B"<br/> U + 0042 LETRA MAYÚSCULA LATINA B<br/> | Iguales | Equal             | Iguales          | Equal                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con National Language](using-national-language-support.md)
</dt> <dt>

[Ordenación](sorting.md)
</dt> <dt>

[Recuperar y establecer la información de configuración regional](retrieving-and-setting-locale-information.md)
</dt> <dt>

[Usar la normalización Unicode para representar cadenas](using-unicode-normalization-to-represent-strings.md)
</dt> <dt>

[Consideraciones de seguridad: características internacionales](security-considerations--international-features.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)
</dt> <dt>

[**Comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)
</dt> <dt>

[**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)
</dt> <dt>

[**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)
</dt> <dt>

[**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> <dt>

[**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)
</dt> </dl>

 

 

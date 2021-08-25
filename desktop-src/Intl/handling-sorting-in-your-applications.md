---
description: Algunas aplicaciones, como Microsoft Active Directory, Microsoft Exchange y Microsoft Access, mantienen una base de datos ordenable de cadenas de idioma y configuración regional indexadas por nombre (cadena UTF-16) y sus ponderaciones de ordenación asociadas.
ms.assetid: c8fc32bd-02bd-4a40-a836-d9ad9f69c209
title: Control de la ordenación en las aplicaciones
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 73c7ca897cb5f83e5a073205341f8b0d0f96ff2d0a9d4c7144a914cd5c96c44d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822695"
---
# <a name="handling-sorting-in-your-applications"></a>Control de la ordenación en las aplicaciones

Algunas aplicaciones, como Microsoft Active Directory, Microsoft Exchange y Microsoft Access, mantienen una base de datos ordenable de cadenas de idioma y configuración regional indexadas por nombre (cadena UTF-16) y sus ponderaciones de ordenación asociadas.

[La ordenación](sorting.md) suele ser intuitiva para los usuarios en sus propias configuraciones regionales. Sin embargo, puede no ser intuitivo para los desarrolladores de aplicaciones. En este tema se de analizan las consideraciones para controlar la ordenación en las aplicaciones. La ordenación puede ser lingüística o ordinal (no lingüística).

## <a name="sorting-functions"></a>Funciones de ordenación

Puede usar diversas funciones de ordenación en las aplicaciones:

-   Funciones de comparación de cadenas NLS. Algunos ejemplos son [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**CompareStringOrdinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) [**LCMapString,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) [**LCMapStringEx,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) [**FindNLSString,**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)y [**FindStringOrdinal.**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) Vea [Security Considerations: International Features (Consideraciones de seguridad: características internacionales)](security-considerations--international-features.md) para obtener una explicación de los problemas de seguridad relacionados con las funciones de comparación de cadenas.
-   Funciones contenedoras que llaman internamente a las funciones de comparación de cadenas. Las funciones más comunes son [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) y [**lstrcmpi,**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)que llaman [**a CompareString.**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)

Normalmente, las funciones de ordenación evalúan las cadenas carácter por carácter. Sin embargo, muchos idiomas tienen elementos de varios caracteres, como el par de dos caracteres "CH" en español tradicional. [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) usan el nombre o el identificador de configuración regional proporcionados por la aplicación para identificar elementos de varios caracteres. En cambio, [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)y [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) usan la configuración regional del usuario.

Otro ejemplo es La insondable, que contiene muchos elementos de dos caracteres, como las formas válidas en mayúsculas, mayúsculas y minúsculas de "GI", que son "GI, "Gi" y "gi", respectivamente. Cualquiera de estas formas se trata como un elemento de ordenación único y, si se omite el uso de mayúsculas y minúsculas, se compara como igual. Sin embargo, dado que "gI" no es válido como un único elemento, [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)y [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) tratan "gI" como dos elementos independientes.

Las funciones [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa), [**lstrcmpi,**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) [**LCMapString,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) [**LCMapStringEx,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)y [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) usan de forma predeterminada una técnica de "ordenación de palabras". Para este tipo de ordenación, todos los signos de puntuación y otros caracteres no alfanuméricos, excepto el guion y el apóstrofo, están delante de cualquier carácter alfanumérico. El guion y el apóstrofo se tratan de forma diferente a los demás caracteres no alfanuméricos para garantizar que palabras como "byte" y "co-op" permanezcan juntas en una lista ordenada.

En lugar de una ordenación de palabras, la aplicación puede solicitar una técnica de "ordenación de cadena" de las funciones de ordenación especificando la marca \_ SORT STRINGSORT. Una ordenación de cadena trata el guion y el apóstrofo como cualquier otro carácter no alfanumérico. Sus posiciones en la secuencia de ordenación son anteriores a los caracteres alfanuméricos.

En la tabla siguiente se comparan los resultados de una ordenación de palabras con los resultados de una ordenación de cadena. 

| Ordenación de palabras | Ordenación de cadenas |
|-----------|-------------|
| Billete    | de facturas      |
| Cuentas     | Billete      |
| de facturas    | Cuentas       |
| no puede    | No       |
| hipocresía      | no puede      |
| No     | hipocresía        |
| con       | cooperación       |
| Coop      | con         |
| cooperación     | Coop        |



 

## <a name="sort-strings-linguistically"></a>Ordenar cadenas lingüísticamente

Las [**funciones CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) prueban la igualdad lingüística. Las aplicaciones deben usar estas funciones con la configuración regional correcta para ordenar cadenas lingüísticamente.

> [!Note]  
> Por compatibilidad con Unicode, una aplicación debe preferir [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) o la versión Unicode de [**CompareString.**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) Otro motivo para preferir [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) es que Microsoft migra hacia el uso de nombres de configuración regional en lugar de identificadores de configuración regional para nuevas configuraciones regionales, por motivos de interoperabilidad. Cualquier aplicación que se ejecute solo en Windows Vista y versiones posteriores debe usar [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex).

 

Otra manera de probar la igualdad lingüística es [**usar lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) o [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), que siempre usan una ordenación de palabras. La [**función lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) llama [**a CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) con la marca \_ NORM IGNORECASE, mientras que [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) la llama sin esa marca. Para obtener información general sobre el uso de las funciones contenedoras, vea [**Cadenas**](../menurc/strings.md).

Las funciones recuperan resultados lingüísticamente adecuados para todas las configuraciones regionales. Las expectativas del usuario para diferentes configuraciones regionales pueden diferir significativamente en el comportamiento de ordenación, como se muestra en los ejemplos siguientes.

-   Muchas configuraciones regionales equivalen a la ligadura ae ( eth) con las letras ae. Sin embargo, Islandés (Islandés) la considera una letra independiente y la coloca después de Z en la secuencia de ordenación.
-   Normalmente, el anillo A ( A) se ordena con una diferencia diacrítica de A. Sin embargo, el sueco (Noruega) coloca el anillo A después de Z en la secuencia de ordenación.

Las funciones intentan comprobar rigurosamente que los puntos de código definidos en el estándar Unicode son canónicamente iguales a una cadena de puntos de código equivalentes. Por ejemplo, el punto de código que representa una "u" minúscula con una diéresis (ü) es canónicamente igual a una "u" en minúscula combinada con la diéresis ( categóricamente). Sin embargo, tenga en cuenta que la equivalencia canónica no siempre es posible.

Como casi todos los datos especificados mediante teclados y editores de métodos de entrada (IME) de Windows se ajustan a la forma de normalización de C definida en el estándar Unicode, la conversión de datos entrantes de otras plataformas mediante las funciones de normalización Unicode nls proporciona resultados más coherentes, especialmente para las configuraciones regionales que usan el script de Scripts o el script Hangul para hangul moderno. Para obtener más información sobre la compatibilidad con la normalización Unicode en Windows Vista y versiones posteriores, vea [Using Unicode Normalization to Represent Strings](using-unicode-normalization-to-represent-strings.md).

Cuando la comparación de cadenas sigue las preferencias de idioma del usuario, por ejemplo, al ordenar elementos para un control ListView ordenado, la aplicación puede realizar una de las siguientes acciones:

-   Llame [**a lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) [**o lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) con la configuración regional del usuario.
-   Llame a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) para definir una configuración regional para la comparación, para pasar marcas adicionales, para insertar caracteres NULL o para pasar longitudes explícitas para que coincidan con partes de una cadena.

Cuando los resultados de la comparación deben ser coherentes independientemente de la configuración regional, por ejemplo, al comparar los datos recuperados con una lista predefinida o un valor interno, la aplicación debe usar [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) con el parámetro *Locale* establecido en LOCALE \_ INVARIANT. Para [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), cualquiera de las siguientes llamadas coincidirá incluso si mystr es "INLAP". En este caso, se producirá un error en una llamada a [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) que tenga en cuenta la configuración regional si la configuración regional actual es Desenlazable.

En Windows XP:


```C++
int iReturn = CompareString(LOCALE_INVARIANT, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



En sistemas operativos anteriores:


```C++
DWORD lcid = MAKELCID(MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US), SORT_DEFAULT);
int iReturn = CompareString(lcid, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



## <a name="sort-strings-ordinally"></a>Ordenar cadenas de forma orinal

Para la ordenación ordinal (no lingüística), las aplicaciones siempre deben usar la [**función CompareStringOrdinal.**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)

> [!Note]  
> Esta función solo está disponible para Windows Vista y versiones posteriores.

 

[**CompareStringOrdinal compara**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) dos cadenas [Unicode](unicode.md) para comprobar la igualdad binaria, en lugar de la igualdad lingüística. Algunos ejemplos de estas cadenas no lingüísticas son los nombres de archivo NTFS, las variables de entorno y los nombres de exclusiones mutuas, canalizaciones con nombre o mailslots. A excepción de la opción de no tener en cuenta mayúsculas de minúsculas, esta función no tiene en cuenta todas las equivalencias no binarias. A diferencia de otras funciones de ordenación, comprueba la igualdad de todos los puntos de código, incluidos aquellos a los que no se les da ningún peso en los esquemas de ordenación lingüísticos.

Todas las instrucciones siguientes se aplican a [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) en comparaciones binarias, pero no a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)o [**lstrcmpi.**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

-   Las secuencias canónicamente equivalentes en Unicode, como LATIN SMALL LETTER A WITH RING ABOVE (U+00e5) y LATIN SMALL LETTER A + COMBINING RING ABOVE (U+0061 U+030a), no son iguales aunque parezcan idénticas ("ov").
-   Las cadenas canónicamente similares en Unicode, como LATIN LETTER SMALL CAPITAL Y (U+028f) y LATIN CAPITAL LETTER Y (U+0059), que tienen un aspecto muy similar ("ʏ" e "Y") y varían solo por algunos pesos de mayúsculas y minúsculas especiales en las tablas lingüísticas, se consideran caracteres completamente diferentes. Incluso si la aplicación establece *bIgnoreCase* en **TRUE,** estas cadenas se comparan como diferentes.
-   Los puntos de código definidos pero que no tienen ninguna ponderación de ordenación lingüística, como ZERO WIDTH JOINER (U+200d), se tratan como que tienen sus pesos de punto de código.
-   Los puntos de código que se definen en versiones posteriores de Unicode pero que no tienen peso en las tablas lingüísticas actuales se tratan como si tengan sus pesos de punto de código.
-   Los puntos de código no definidos por Unicode se tratan como que tienen sus pesos de punto de código.
-   Cuando la aplicación establece *bIgnoreCase* en **TRUE,** la función asigna mayúsculas y minúsculas mediante la tabla de mayúsculas del sistema operativo, en lugar de la información de las tablas de ordenación lingüística. Por lo tanto, la asignación es independiente de la configuración regional.

Para obtener más información sobre secuencias canónicamente equivalentes en Unicode y cadenas canónicamente similares en Unicode, vea [Using Unicode Normalization to Represent Strings](using-unicode-normalization-to-represent-strings.md).

## <a name="sort-code-points"></a>Ordenar puntos de código

Algunos puntos de código Unicode no tienen peso, por ejemplo, ZERO WIDTH NON JOINER, U+200c. Las funciones de ordenación evalúan intencionadamente los puntos de código sin peso como equivalentes porque no tienen peso en la ordenación. En Windows Vista y versiones posteriores, la aplicación puede ordenar estos puntos de código llamando a las funciones de comparación de cadenas NLS, especialmente [**CompareStringOrdinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)para evaluar todos los puntos de código en un literal, un sentido binario, por ejemplo, en la validación de contraseñas. En sistemas operativos Windows Vista, la aplicación debe usar la función en tiempo de ejecución de C **strcmp** o **wcscmp**.

Las funciones de ordenación omiten los signos diacríticos, como NON SPACING BREVE, U+0306, cuando la aplicación especifica la marca \_ NONSPACE de hlink. De forma similar, estas funciones omiten los símbolos, por ejemplo, EQUALS SIGN, U+003d , cuando se especifica la marca hlink \_ SYMBOLS. En Windows Vista y versiones posteriores, la aplicación llama a [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) para la evaluación de signos diacríticos y puntos de código de símbolos en un sentido binario literal. En sistemas operativos Windows Vista, la aplicación debe usar **strcmp** o **wcscmp**.

Algunos puntos de código, como 0xFFFF y 0x058b, no están asignados actualmente en Unicode. Estos puntos de código no reciben ningún peso en la ordenación y nunca se deben pasar a las funciones de ordenación. La aplicación debe usar [**IsNLSDefinedString para**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) detectar puntos de código no Unicode en un flujo de datos.

> [!Note]  
> Los resultados de [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) pueden variar en función de la versión de Unicode pasada si se agrega un carácter a Unicode en una versión posterior y posteriormente se agrega a las tablas de ordenación Windows datos. Para obtener más información, [vea Usar control de versiones de ordenación.](#use-sort-versioning)

 

## <a name="sort-digits-as-numbers"></a>Ordenar dígitos como números

En Windows 7 y versiones posteriores, la aplicación puede llamar a [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) mediante la marca SORT \_ DIGITSASNUMBERS. Esta marca admite la ordenación que trata los dígitos como números, por ejemplo, la ordenación de "2" antes de "10".

Tenga en cuenta que el uso de esta marca no es adecuado para dígitos hexadecimales como los siguientes. <dl> 01AF  
1BCD  
002a  
12FA  
AB1C  
AB02  
AB12  
</dl>

En este caso, los "números" se ordenan por orden, pero el usuario percibe una lista hexadecimal mal ordenada.

## <a name="map-strings"></a>Cadenas de mapa

La aplicación usa las [**funciones LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) para asignar cadenas, si no se especifica \_ LCMAP SORTKEY. Una cadena asignada termina en NULL si la cadena de origen termina en NULL.

Al transformar entre mayúsculas y minúsculas, la función no garantiza que un solo carácter se asigne a un solo carácter. Por ejemplo, las marcas LCMAP LOWERCASE y LCMAP UPPERCASE pueden asignar el alemán \_ \_ Sharp S ("gie") a sí mismo. Como alternativa, la marca LCMAP UPPERCASE puede asignar "ntes" a "SS" y la marca LCMAP LOWERCASE puede asignar \_ \_ "SS" a "ntes". El comportamiento depende de la versión de NLS.

Al transformar entre mayúsculas y minúsculas, la función no es sensible al contexto. Por ejemplo, mientras que la marca LCMAP UPPERCASE asigna correctamente los valores de sigma en minúscula griego ("σ") y sigma final en minúsculas griego ("σ") a sigma en mayúsculas griego ("Σ"), la marca LCMAP LOWERCASE siempre asigna \_ \_ "Σ" a "σ", nunca a "σ".

De forma predeterminada, la función asigna la "i" minúscula a la "I" en mayúscula, incluso cuando el parámetro *Locale* especifica turco o inocuo. Para invalidar este comportamiento para turco o no turco, la aplicación debe especificar LCMAP \_ LINGUISTIC \_ CASING. Si esta marca se especifica con la configuración regional adecuada, "eto" (I sin puntos en minúsculas) es la forma minúscula de "I" (I sin puntos mayúsculas) e "i" (I con puntos en minúsculas) es la forma minúscula de "eto" (I con puntos en mayúsculas).

Si se especifica la marca LCMAP HIRAGANA para asignar caracteres katakana a caracteres hiragana y no se especifica \_ LCMAP \_ FULLWIDTH, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) solo asigna caracteres de ancho completo a hiragana. En este caso, los caracteres katakana de ancho medio se colocan como en la cadena de destino, sin asignación a hiragana. La aplicación debe especificar LCMAP FULLWIDTH para asignar caracteres \_ katakana de ancho medio a hiragana. La razón de esta restricción es que todos los caracteres hiragana son caracteres de ancho completo.

Si la aplicación necesita quitar caracteres de la cadena de origen, puede llamar a la función de asignación con las marcas NORM \_ IGNORESYMBOLS y NORM IGNORENONSPACE establecidas y todas las demás marcas \_ desactivadas. Si la aplicación lo hace con una cadena de origen que no termina en NULL, es posible que la función devuelva una cadena vacía y no devuelva un error.

## <a name="create-sort-keys"></a>Crear claves de ordenación

Cuando la aplicación especifica LCMAP \_ SORTKEY, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) genera una clave de ordenación, una matriz binaria de valores de bytes. La clave de ordenación no es una cadena verdadera y sus valores representan el comportamiento de ordenación de la cadena de origen, pero no son valores para mostrar significativos.

> [!Note]  
> La función omite el kashida árabe durante la generación de una clave de ordenación. Si una aplicación llama a la función para crear una clave de ordenación para una cadena que contiene un kashida árabe, la función no crea ningún valor de clave de ordenación.

 

La clave de ordenación puede contener un número impar de bytes. La marca BYTEREV de LCMAP \_ solo invierte un número par de bytes. El último byte (posición impar) de la clave de ordenación no se invierte. Si la terminación 0x00 byte es un byte con posición impar, sigue siendo el último byte de la clave de ordenación. Si el byte 0x00 terminación es un byte de posición uniforme, intercambia posiciones con el byte que lo precede.

Al generar la clave de ordenación, la función trata el guion y el apóstrofo de forma diferente a otros símbolos de puntuación, de modo que palabras como "clo" y "cooperación" permanezcan juntas en una lista. Todos los símbolos de puntuación distintos del guion y el apóstrofo se ordenan antes que los caracteres alfanuméricos. La aplicación puede cambiar este comportamiento estableciendo la marca SORT \_ STRINGSORT, como se describe en [Funciones de ordenación](#sorting-functions).

Cuando se usa [en memcmp,](/cpp/c-runtime-library/reference/memcmp-wmemcmp)la clave de ordenación genera el mismo orden que cuando se usa la cadena de origen en [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx.**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) La [función memcmp debe](/cpp/c-runtime-library/reference/memcmp-wmemcmp) usarse en lugar de [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp), porque la clave de ordenación puede tener bytes nulos incrustados.

## <a name="use-sort-versioning"></a>Uso del control de versiones de ordenación

Una [tabla de ordenación](sorting.md) tiene dos números que identifican su versión: la versión definida y la versión nls. Ambos números son valores DWORD, compuestos por un valor principal y un valor menor. El primer byte de un valor está reservado, los dos bytes siguientes representan la versión principal y el último byte representa la versión secundaria. En términos hexadecimales, el patrón es 0xRRMMMMmm, donde R es igual a Reservado, M es igual a principal y m es menor. Por ejemplo, una versión principal de 3 con una versión secundaria de 4 se representa como 0x304.

La versión definida identifica el idioma de los puntos de código y es el mismo para todas las configuraciones regionales. La versión principal se incrementa para indicar los cambios en los puntos de código existentes. La versión secundaria se incrementa para indicar que se han agregado puntos de código, pero que no se ha cambiado ningún punto de código existente previamente.

La versión de NLS es específica de un identificador de configuración [regional](locale-identifiers.md) o un nombre de configuración [regional,](locale-names.md)y realiza un seguimiento de los cambios en los pesos de punto de código de la configuración regional afectada. La versión principal se incrementa cuando se cambian los pesos de los puntos de código que ya se pueden ordenar. La versión secundaria se incrementa cuando se asignan pesos a los nuevos puntos de código, pero todos los demás pesos de punto de código que se pueden ordenar previamente permanecen sin cambios.

> [!Note]  
> Para una versión principal, se cambian uno o varios puntos de código para que la aplicación deba volver a indexar todos los datos para que las comparaciones sean válidas. Para una versión secundaria, no se mueve nada, pero se agregan puntos de código. Para este tipo de versión, la aplicación solo tiene que volver a indexar cadenas con valores no disponibles previamente.

 

> [!IMPORTANT]
> La versión principal se ha cambiado en Windows 8. Los datos creados en versiones anteriores Windows deben volver a indexar.

 

Las versiones definidas y NLS se aplican a los puntos de código ordenables recuperados mediante las funciones [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) con la marca LCMAP SORTKEY, y también se usan en las funciones \_ [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)y [**FindNLSStringEx.**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) Si uno o varios puntos de código de una cadena no son configurables, la función [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) devuelve **FALSE** cuando esa cadena se le pasa como parámetro.

La aplicación puede llamar a [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) o [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) para recuperar la versión definida y la versión NLS para una tabla de ordenación.

## <a name="index-the-database"></a>Indexación de la base de datos

Por motivos de rendimiento, la aplicación debe seguir este procedimiento al indexar la base de datos.

**Para indexar correctamente la base de datos**

1.  Para cada función, almacene la versión de NLS, las claves de ordenación de esa versión y una indicación de la ordenación de cada cadena indizada.
2.  Cuando se incremente la versión secundaria, vuelva a indexar las cadenas que antes no se pueden indexar. Las cadenas afectadas en esta actualización deben limitarse a las que [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) ha devuelto previamente **FALSE.**
3.  Cuando se incremente la versión principal, vuelva a indexar todas las cadenas porque las ponderaciones actualizadas podrían cambiar el comportamiento de cualquier cadena. Las versiones principales son muy poco frecuentes.

Pueden surgir problemas de indexación de base de datos por los siguientes motivos:

-   Un sistema operativo posterior puede definir puntos de código que no están definidos para un sistema operativo anterior, lo que cambia la ordenación.
-   Los puntos de código pueden tener distintos pesos de ordenación en sistemas operativos diferentes, debido a correcciones en la compatibilidad con idiomas.

Para minimizar la necesidad de volver a indexar la base de datos en estas circunstancias, la aplicación puede usar [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) para diferenciar las cadenas definidas de las cadenas no definidas para que la aplicación pueda rechazar cadenas con puntos de código indefinidos. El uso [**de GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) o [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) permite a la aplicación determinar si un cambio de NLS afecta a la configuración regional usada para una tabla de índice determinada. Si el cambio no tiene ningún efecto en la configuración regional, la aplicación no tiene necesidad de volver a indexar la tabla.

## <a name="examples"></a>Ejemplos

En la tabla siguiente se muestran los efectos de determinadas marcas que se usan con las funciones de ordenación. En cada caso, la selección de marcas determina si dos caracteres diferentes se consideran iguales con fines de ordenación.



| Carácter 1                                                        | Carácter 2                                             | Valor predeterminado | NORM \_ IGNOREWIDTH | NORM \_ IGNOREKANA | NORM \_ IGNOREWIDTH\| NORMIGNOREKANA |
|--------------------------------------------------------------------|---------------------------------------------------------|---------|-------------------|------------------|------------------------------------|
| "あ"<br/> U+3042 HIRAGANA LETTER A<br/>                | "ガ"<br/> U+30A2 KATAKANA LETTER A<br/>     | Desigual | Desigual           | Igual            | Igual                              |
| "ｵ"<br/> U+FF75 HALFWIDTH KATAKANA LETTER O<br/>       | "オ"<br/> U+30AA KATAKANA LETTER O<br/>     | Desigual | Igual             | Desigual          | Igual                              |
| "B"<br/> U+FF22 FULLWIDTH LATIN CAPITAL LETTER B<br/> | "B"<br/> U+0042 LATIN CAPITAL LETTER B<br/> | Desigual | Igual             | Desigual          | Igual                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con idiomas nacionales](using-national-language-support.md)
</dt> <dt>

[Ordenación](sorting.md)
</dt> <dt>

[Recuperar y establecer información de configuración regional](retrieving-and-setting-locale-information.md)
</dt> <dt>

[Usar la normalización Unicode para representar cadenas](using-unicode-normalization-to-represent-strings.md)
</dt> <dt>

[Consideraciones de seguridad: Características internacionales](security-considerations--international-features.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)
</dt> <dt>

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)
</dt> <dt>

[**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)
</dt> <dt>

[**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)
</dt> <dt>

[**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> <dt>

[**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)
</dt> </dl>

 

 

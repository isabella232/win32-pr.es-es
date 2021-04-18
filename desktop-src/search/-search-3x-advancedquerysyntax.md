---
description: La sintaxis de consulta avanzada (AQS) es la sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para refinar y restringir los parámetros de búsqueda.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Usar la sintaxis de consulta avanzada mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720342"
---
# <a name="using-advanced-query-syntax-programmatically"></a>Usar la sintaxis de consulta avanzada mediante programación

La sintaxis de consulta avanzada (AQS) es la sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para refinar y restringir los parámetros de búsqueda. AQS lo emplean los desarrolladores para compilar consultas mediante programación (y los usuarios para restringir sus parámetros de búsqueda). AQS canónico se presentó en Windows 7 y se debe usar en Windows 7 y versiones posteriores para generar consultas AQS mediante programación.

Este tema se organiza de la siguiente manera:

-   [Acerca de la sintaxis de consulta avanzada](#about-advanced-query-syntax)
    -   [Ejemplos](#examples)
    -   [Propiedades](#properties)
-   [Uso de palabras clave en idiomas locales](#keyword-use-in-local-languages)
-   [Sintaxis de consulta avanzada canónica en Windows 7](#canonical-advanced-query-syntax-in-windows-7)
    -   [Ejemplos](#examples)
    -   [Operadores de consulta](#query-operators)
    -   [Valores de consulta](#query-values)
-   [Restricciones de ámbito](#scope-restrictions)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-advanced-query-syntax"></a>Acerca de la sintaxis de consulta avanzada

Una consulta consta de consultas básicas conectadas con AND, OR y NOT, tal y como se muestra en la siguiente sintaxis de ejemplo:

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> AQS no distingue entre mayúsculas y minúsculas, con la excepción de AND, OR y NOT, que debe estar en mayúsculas.

 

Si una consulta tiene dos o más usos de AND u OR, se enlazarán de izquierda a derecha, independientemente de si es AND u or. Es decir, la consulta "Apple AND Perat o ciruela" se interpretará como si se hubiera escrito como "(Apple y peral) o ciruela", y la consulta, "Apple o pera y ciruela", se interpretará como si estuviera escrita como "(Apple o pera) y ciruela". Por lo tanto, si un documento contiene la palabra ciruela pero no Apple ni pera, la primera consulta la devolverá, pero la segunda consulta no. Por lo tanto, se recomienda utilizar paréntesis explícitos para cualquier consulta que combine AND y OR para evitar errores o interpretaciones erróneas.

Una consulta básica busca elementos que satisfacen una restricción de una propiedad. La única parte necesaria de una consulta básica es la restricción o el valor de búsqueda. Si no se especifica una propiedad, Windows Search busca en todas las propiedades. <restr> representa la restricción de búsqueda.

Los siguientes formatos para una consulta básica son válidos:

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

Una propiedad se designa mediante una palabra clave como Author o size, o bien mediante un nombre de propiedad canónico como [System. DateModified](../properties/props-system-datemodified.md). Los formatos válidos para una propiedad son los siguientes:

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

Un operador indica una operación como < o =. Para obtener una lista de operadores válidos, vea la sección operadores de consulta más adelante en este tema.

Una restricción básica es una restricción simple de una propiedad que se puede escribir sin paréntesis:

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

Una restricción es un valor de búsqueda, como un valor numérico o un valor de cadena, opcionalmente con un operador. Los formatos válidos para una restricción son los siguientes:

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

Si no especifica ningún operador, Windows Search elige el operador más apropiado para la consulta:

-   En el caso de una propiedad de cadena, \_ \_ se supone el operador COP Word STARTSWITH $<.
-   Para todas las demás propiedades, \_ se supone el operador COP igual que.

Para el uso mediante programación de AQS, se recomienda tener siempre un operador explícito. El formato válido para buscar un valor simple o un intervalo de valores es el siguiente:

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

Un valor simple puede constar de cualquiera de los siguientes tipos:

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a>Ejemplos

Una consulta que busca un documento que contenga la fase "Last Quarter", creada por Theresa o lee y que se guardó en la carpeta Mis documentos, combina tres consultas básicas de la siguiente manera:

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

Las tres consultas básicas son:

-   "último trimestre"
-   Autor: (Theresa o Lee)
-   carpeta: mis documentos

Una consulta básica que usa sintaxis canónica es:

``` syntax
System.Size:>1kb
```

### <a name="properties"></a>Propiedades

Se hace referencia a las propiedades mediante una palabra clave, que puede ser un nombre de propiedad canónico en Windows 7 y versiones posteriores. AQS en la interfaz de usuario de Windows puede usar la etiqueta en lugar del nombre de propiedad canónico, como Author en lugar de [System. Author](../properties/props-system-author.md). En Windows Vista y versiones anteriores, era posible usar etiquetas en inglés independientemente del idioma de la interfaz de usuario. En Windows 7 y versiones posteriores, Windows Search solo reconoce palabras clave en el idioma de la interfaz de usuario predeterminado actual.

### <a name="support-for-custom-properties"></a>Compatibilidad con propiedades personalizadas

En Windows Vista y versiones anteriores, las propiedades personalizadas no estaban disponibles en AQS. En Windows 7 y versiones posteriores, AQS funciona con propiedades personalizadas que se registran con el sistema de propiedades. Para obtener más información sobre la creación de propiedades personalizadas, vea [sistema de propiedades](../properties/building-property-handlers.md).

### <a name="datetime-properties-in-windows-8"></a>Propiedades DateTime en Windows 8

A partir de Windows 8, las propiedades DateTime (como [System. DateModified](../properties/props-system-datemodified.md)) admiten el formato canónico de fecha y hora especificado por [ISO-8601](https://www.w3.org/TR/NOTE-datetime), incluida opcionalmente la zona horaria UTC.

-   **Windows 8 y versiones anteriores, fecha y hora sin zona horaria UTC:** *yyyy* - *mm* - *DDTHH*:*mm*:*SS*

    Este formato especifica una hora local, independientemente de la configuración regional del usuario o del sistema.

-   **Windows 8, fecha y hora con la zona horaria UTC:** *yyyy* - *mm* - *DDTHH*:*mm*:*ssTZD*

    Este formato especifica una hora en la zona horaria UTC especificada.

## <a name="keyword-use-in-local-languages"></a>Uso de palabras clave en idiomas locales

En Windows 7 y versiones posteriores, las palabras clave de teclas de complemento solo funcionan en el idioma del sistema, como las palabras clave alemanas solo en un sistema operativo alemán y en inglés solo en un sistema operativo en inglés. [System. Author](../properties/props-system-author.md) es una palabra clave canónica y el valor de tecla de acceso de la propiedad System. Author es Author, por ejemplo. La introducción de las palabras clave canónicas compensa el hecho de que las palabras clave de la tecla de teclas de carácter de idioma no se reconocen universalmente en todos los sistemas operativos, independientemente del lenguaje, como era el caso en Windows Vista y versiones anteriores.

> [!Note]  
> En Windows 7 y versiones posteriores, Windows Search solo reconoce palabras clave en el idioma predeterminado actual y no en inglés, a menos que el inglés sea el valor predeterminado actual. Se recomienda que los desarrolladores utilicen siempre sintaxis canónica para que su aplicación no tenga problemas de idioma con las palabras clave.

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a>Sintaxis de consulta avanzada canónica en Windows 7

Se presentó la sintaxis canónica para las palabras clave de Windows 7. Un ejemplo de una consulta con una propiedad canónica es `System.Message.FromAddress:=me@microsoft.com` . Al codificar consultas en aplicaciones que se ejecutan en Windows 7 y versiones posteriores, debe usar la sintaxis canónica para generar consultas AQS mediante programación. Si no usa la sintaxis canónica y la aplicación se implementa en un idioma de interfaz de usuario o en una configuración regional diferente del lenguaje del código de aplicación, las consultas no se interpretarán correctamente.

Las convenciones de la sintaxis de palabra clave canónica son las siguientes:

-   La sintaxis canónica para una propiedad es su nombre canónico, como `System.Photo.LightSource` . Los nombres canónicos no distinguen mayúsculas de minúsculas.
-   La sintaxis canónica para los operadores booleanos consta de las palabras clave AND, OR y NOT, en mayúsculas.
-   Los operadores <, >, =, etc., no están localizados y, por tanto, también forman parte de la sintaxis canónica.
-   Si una propiedad `P` tiene valores enumerados o intervalos denominados N ₁ a NK, la sintaxis canónica del valor o del intervalo *I* es el nombre canónico de P, seguido del carácter \# , seguido de N <sub>I</sub>, tal y como se muestra en el ejemplo siguiente:
    -   `System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` , y así sucesivamente.
-   Para un tipo semántico definido T con valores o intervalos denominados N ₁ a NK, la sintaxis canónica del valor o del intervalo *I* es el nombre canónico de T, seguido del carácter \# , seguido de N <sub>I</sub>, como se muestra en el ejemplo siguiente:
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   Para los valores literales como palabras o frases, la sintaxis canónica es la misma que la sintaxis normal. Ejemplos de consultas con valores literales en sintaxis canónica son:
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> No hay ninguna sintaxis canónica para los números en Windows 7 y versiones posteriores. Dado que los formatos de punto flotante varían entre las configuraciones regionales, no se admite el uso de una consulta canónica que implique una constante de punto flotante. Por el contrario, las constantes de tipo entero solo se pueden escribir con dígitos (sin separadores para miles) y se pueden usar de forma segura en consultas canónicas en Windows 7 y versiones posteriores.

 

### <a name="examples"></a>Ejemplos

En la tabla siguiente se muestran algunos ejemplos de propiedades canónicas y la sintaxis para usarlas.



| Tipo de propiedad canónica | Ejemplo                                                                                     | Sintaxis                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor de cadena               | [System.Author](../properties/props-system-author.md)<br/>    | El valor de cadena se busca en la propiedad Author: <br/>`System.Author:Jacobs`                                                                                                                                                              |
| Intervalo de enumeración          | [System. Priority](../properties/props-system-priority.md)             | La propiedad Priority puede tener un intervalo de valores numéricos:<br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| Boolean                    | [System. IsDeleted](../properties/props-system-isdeleted.md)<br/> | Los valores booleanos se pueden usar con cualquier propiedad booleana:<br/>`System.IsDeleted:System.StructuredQueryType.Boolean#True` y `System.IsDeleted:System.StructuredQueryType.Boolean#False`                                                             |
| Numérico                  | [System. Size](../properties/props-system-size.md)<br/>      | No es posible escribir de forma segura una consulta canónica que implique una constante de punto flotante, ya que los formatos de punto flotante varían entre las configuraciones regionales. Los enteros se deben escribir sin separadores para miles. Por ejemplo:<br/>`System.Size:<12345` |



 

Para obtener más información sobre las propiedades canónicas y el sistema de propiedades en general, consulte [propiedades del sistema](../properties/props.md). También puede hacer referencia a los archivos de encabezado públicos.

### <a name="query-operators"></a>Operadores de consulta

Si una propiedad, p, tiene varios valores para algún elemento, una consulta AQS para p: <restr> devuelve el elemento si <restr> es **true** para al menos uno de los valores. ( <restr> representa una restricción).

La sintaxis que se muestra en la tabla siguiente consta de un operador, un símbolo de operador, un ejemplo y una descripción de ejemplo. El operador y el símbolo se pueden usar en cualquier lenguaje e incluirse en cualquier consulta. No use los \_ operadores específicos de la aplicación COP IMPLICIT o COP \_ \_ . Algunos de los operadores tienen símbolos intercambiables.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Operator</th>
<th>Símbolo</th>
<th>Ejemplo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COP_EQUAL</td>
<td>=<br/></td>
<td>System. FileExtension: = &quot; . txt&quot;<br/></td>
<td>El valor es String &quot; <em>. txt</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_NOTEQUAL</td>
<td>≠<br/> -<br/> &lt;&gt;<br/> NOT<br/> - -<br/></td>
<td>System. Kind: ≠ imagen<br/> System. Photo. DateTaken:-[] ¹<br/> System. Kind: &lt; &gt; imagen<br/> System. Kind: no imagen<br/> System. Kind:--imagen<br/></td>
<td>La propiedad <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> no es una imagen.<br/> La propiedad <a href="/windows/desktop/properties/props-system-photo-datetaken">System. Photo. DateTaken</a> tiene un valor.<br/> La propiedad <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> no es una imagen. <br/> La propiedad <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> no es una imagen. <br/> Los operadores Double no aplicados a la misma propiedad no se cancelan. Por lo tanto, System. Kind:--Picture es equivalente a System. Kind:-Picture y System. Kind: NOT Picture.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHAN</td>
<td>&lt;<br/></td>
<td>System. Size: &lt; 1 KB<br/></td>
<td>Este valor es menor que <em>1 KB</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHAN</td>
<td>&gt;<br/></td>
<td>System. ItemDate: &gt; System. StructuredQueryType. DateTime # Today<br/></td>
<td>Este valor es mayor que <em>hoy</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHANOREQUAL</td>
<td>&lt;=<br/> ≤<br/></td>
<td>System. Size: &lt; = 1 KB<br/></td>
<td>Este valor es menor o igual que <em>1 KB</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHANOREQUAL</td>
<td>&gt;=<br/> ≥<br/></td>
<td>System. Size: &gt; = 1 KB<br/></td>
<td>Este valor es igual o mayor que <em>1 KB</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_STARTSWITH</td>
<td>~&lt;<br/></td>
<td>System. FileName: ~ &lt; &quot; C++ manual&quot;<br/></td>
<td>Busca los elementos en los que el nombre de archivo comienza con los caracteres de &quot; <em>C++ manual</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_ENDSWITH</td>
<td>~&gt;<br/></td>
<td>System. Photo. CameraModel: ~ &gt; no<br/></td>
<td>Busca los elementos en los que el valor de propiedad termina con los caracteres <em>no</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_CONTAINS</td>
<td>~=<br/> ~~<br/></td>
<td>System. Subject. ~ = round <br/> System. Search. autosummary: ~ ~ Round<br/></td>
<td>Busca un mensaje que tenga esta cadena en el asunto y coincidirá con &quot; las reglas de<em>redondeo</em> g &quot; por ejemplo.<br/> Busca todos los elementos con un Autoresumen que contenga los caracteres <em>redondeados</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_NOTCONTAINS</td>
<td>~!<br/></td>
<td>System. Author: ~! &quot; Sanjay&quot;<br/></td>
<td>Busca los autores que no tienen la secuencia de caracteres &quot; <em>Sanjay</em> &quot; en ellos.<br/></td>
</tr>
<tr class="odd">
<td>COP_DOSWILDCARDS</td>
<td>~ <br/></td>
<td>System. FileName: ~ &quot; MIC? osoft W * d&quot;<br/></td>
<td>Busca archivos en los que el nombre de archivo empieza por <em>MIC</em>, seguido de algún carácter seguido de <em>osoft w</em>, seguido de los caracteres que terminan en <em>d</em>. <br/> El signo ? los caracteres y * no se interpretan literalmente y funcionan como caracteres comodín de estilo de DOS:<br/>
<ul>
<li>? coincide con un carácter arbitrario.</li>
<li>* coincide con cero o más caracteres arbitrarios.</li>
</ul></td>
</tr>
<tr class="even">
<td>COP_WORD_EQUAL</td>
<td>$=<br/> $$<br/></td>
<td>System. StructuredQuery. virtual. from: $ = &quot; Sanjay Jacobs&quot;<br/></td>
<td>Para Windows 7 y versiones posteriores. Busca la frase &quot; <em>Sanjay Jacobs</em> &quot; en todas las propiedades. La palabra <em>Sanjay</em> debe ir seguida de la palabra <em>Jacobs</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_WORD_STARTSWITH</td>
<td>$<<br/></td>
<td>System. Author: $<&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td>Para Windows 7 y versiones posteriores. Busca cualquier elemento donde Author contenga una palabra que empiece con los caracteres &quot; <em>San</em> &quot; .<br/> Busca cualquier archivo en el que el nombre de archivo contenga una palabra que comience por <em>micro</em>, seguida de una palabra que comience por <em>exe</em>.<br/></td>
</tr>
</tbody>
</table>



 

¹ los corchetes vacíos ( \[ \] ) denotan "sin valor".

En el caso de las propiedades de cadena, la operación predeterminada es COP \_ Word \_ comienza \_ con o COP \_ Word \_ igual.

### <a name="query-values"></a>Valores de consulta

En la tabla siguiente se muestran ejemplos útiles de cómo se pueden restringir los valores de consulta.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor/símbolo</th>
<th>Ejemplos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>auto<br/></td>
<td>Cualquier secuencia de caracteres que se puede buscar. La cadena no debe contener espacios en blanco ni combinaciones de caracteres que formen parte de la sintaxis. En este ejemplo se busca una palabra que comience por <em>auto</em>.<br/></td>
</tr>
<tr class="even">
<td>Cadena entre comillas &quot;&quot;</td>
<td>&quot;CONCLUSIONES: &quot; &quot; el &quot; &quot; equipo azul &quot; &quot; es válido&quot;<br/></td>
<td>Cualquier secuencia de caracteres. La cadena no se interpreta como parte de la sintaxis.<br/> Las comillas se pueden incluir en una consulta si se duplican. Este ejemplo busca <em>el &quot; &quot; equipo azul</em>.<br/></td>
</tr>
<tr class="odd">
<td>Entero</td>
<td>5678<br/></td>
<td>Use solo dígitos para enteros. No use ningún separador para miles.<br/></td>
</tr>
<tr class="even">
<td>Número de punto flotante</td>
<td>5678,1234<br/></td>
<td>Dado que los formatos de punto flotante varían entre las configuraciones regionales, una consulta canónica no puede usar una constante de punto flotante. El uso de sintaxis canónica con números de punto flotante no es seguro para la localización. <br/></td>
</tr>
<tr class="odd">
<td>Booleano <strong>true</strong> / <strong>false</strong></td>
<td>System. IsRead: = System. StructuredQueryType. Boolean # true<br/> System. IsEncrypted:-System. StructuredQueryType. Boolean # false<br/></td>
<td>Valor booleano <strong>true</strong> .<br/> Valor booleano <strong>falso</strong> .<br/></td>
</tr>
<tr class="even">
<td>[]</td>
<td>System. Keywords: = []<br/></td>
<td>Los corchetes vacíos indican que no hay ningún valor. Este ejemplo busca todos los elementos que no se han etiquetado. <br/></td>
</tr>
<tr class="odd">
<td>Fechas absolutas</td>
<td>System. ItemDate: 1/26/2010<br/> SystemDateModified 10/15/2002 19:00<br/></td>
<td>Busca elementos con una fecha del 26 de enero de 2010.<br/> Busca los elementos que se modificaron el 15 de octubre de 2002 entre las horas 19:00:00 y 19:00:59. <br/>
<blockquote>
[!Note]<br />
Dado que los formatos de fecha (como los formatos de punto flotante) varían entre las configuraciones regionales, no se admite el uso de sintaxis canónica con fechas absolutas y no es seguro para la localización.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Fechas relativas</td>
<td>System. ItemDate: System. StructuredQueryType. DateTime # Today<br/> System. DateAcquired: System. StructuredQueryType. DateTime # NextMonth<br/> System. Message. DateReceived: System. StructuredQueryType. DateTime # LastYear<br/></td>
<td>Busca elementos con la fecha de hoy.<br/> Busca elementos con una fecha en el mes siguiente.<br/> Busca elementos con una fecha en el último año.<br/>
<blockquote>
[!Note]<br />
Además de buscar en fechas y intervalos de fechas específicos, AQS reconoce los valores de fecha relativos (como <em>hoy</em>, <em>mañana</em>, <em>nextweek</em>, <em>Nextmonth</em>) y Day (como el <em>martes</em> o el lunes). <em> Miércoles</em>) y mes (<em>febrero</em>).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>..</td>
<td>System. ItemDate: 11/05/04.. 11/10/04 System. Size: 5 KB.. 10 KB<br/></td>
<td>Los puntos dobles indican un intervalo de valores. Busca elementos con una fecha comprendida entre 11/05/04 y 11/10/04, ambos incluidos.<br/> Busca elementos entre 5 y 10 KB de tamaño.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a>Restricciones de ámbito

Los usuarios pueden limitar el ámbito de las búsquedas a ubicaciones de carpeta o almacenes de datos específicos. Por ejemplo, si utiliza varias cuentas de correo electrónico y desea limitar una consulta a Microsoft Outlook o Microsoft Outlook Express, puede utilizar `System.Search.Store:mapi` o `System.Search.Store:oe` respectivamente. En la tabla siguiente se muestran algunos ejemplos de cómo restringir una búsqueda por almacén de datos.



| Restricción de búsqueda por almacén de datos  | Palabra clave | Ejemplo                                     |
|--------------------------------|---------|---------------------------------------------|
| Archivos                          | archivo    | System. Search. Store: archivo                    |
| Outlook                        | interfaz    | System. Search. Store: MAPI                    |
| Outlook Express                | oe      | System. Search. Store: OE                      |
| Archivos sin conexión                  | CSC     | System. Search. Store: CSC                     |
| Carpeta específica en la unidad local | folder  | System. ItemFolderNameDisplay: C: " \\ carpeta" |



 

## <a name="additional-resources"></a>Recursos adicionales

-   En Windows 7 y versiones posteriores, una opción de menú contextual puede estar disponible en función de si se cumple una condición de AQS. Para obtener más información, vea "obtener el comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada" en [crear controladores de menú contextuales](../shell/context-menu-handlers.md).
-   Las consultas AQS se pueden limitar a tipos específicos de archivos, que se conocen como tipos de archivo. Para obtener más información, vea [tipos de archivo y asociaciones](../shell/fa-intro.md). Para obtener documentación de referencia de propiedades, vea [System. Kind](../properties/props-system-kind.md)y [System. KindText](../properties/props-system-kindtext.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Uso de enfoques de SQL y AQS para consultar el índice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Consultar el índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Consultar el índice con el protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Consultar el índice con la sintaxis SQL de Windows Search](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 

---
description: Advanced Query Syntax (AQS) es la sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para restringir y restringir los parámetros de búsqueda.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Uso de la sintaxis de consulta avanzada mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebde3119199d84f67315c2db73343d5dffc58ad
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880696"
---
# <a name="using-advanced-query-syntax-programmatically"></a>Uso de la sintaxis de consulta avanzada mediante programación

Advanced Query Syntax (AQS) es la sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para restringir y restringir los parámetros de búsqueda. Los desarrolladores emplean AQS para compilar consultas mediante programación (y para que los usuarios limiten sus parámetros de búsqueda). AQS canónico se introdujo en Windows 7 y debe usarse en Windows 7 y versiones posteriores para generar consultas de AQS mediante programación.

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

Una consulta consta de consultas básicas conectadas con AND, OR y NOT, como se muestra en la sintaxis de ejemplo siguiente:

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
> AQS no distingue mayúsculas de minúsculas, a excepción de AND, OR y NOT, que deben estar en mayúsculas.

 

Si una consulta tiene dos o más usos de AND u OR, se enlazarán de izquierda a derecha, independientemente de si es AND o OR. Es decir, la consulta "manzana Y manzana O cirón" se interpretará como si se hubiera escrito como "(manzana Y manzana) OR manzana", y la consulta, "manzana O manzana Y manzana", se interpretará como si se hubiera escrito como "(manzana O manzana) Y manzana". Por lo tanto, si un documento contiene la palabra cirón, pero ni manzana, ni pie, la primera consulta lo devolverá, pero la segunda consulta no. Por lo tanto, se recomienda usar paréntesis explícitos para cualquier consulta que combine AND y OR para evitar errores o interpretaciones erróneas.

Una consulta básica busca elementos que cumplan una restricción sobre una propiedad. La única parte necesaria de una consulta básica es la restricción o el valor de búsqueda. Si no especifica una propiedad, Windows Buscar busca en todas las propiedades. &lt;restr &gt; representa la restricción de búsqueda.

Los siguientes formularios para una consulta básica son válidos:

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

Una propiedad se designa mediante una palabra clave como author o size, o por un nombre de propiedad canónico como [System.DateModified.](../properties/props-system-datemodified.md) Los formularios válidos para una propiedad son los siguientes:

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

Un operador indica una operación como < o =. Para obtener una lista de operadores válidos, vea la sección Operadores de consulta más adelante en este tema.

Una restricción básica es una restricción simple en una propiedad que se puede escribir sin paréntesis:

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

Una restricción es un valor de búsqueda, como un valor numérico o un valor de cadena, opcionalmente con un operador . Los formularios válidos para una restricción son los siguientes:

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

Si no especifica un operador, Windows Search elige el operador más adecuado para la consulta:

-   Para una propiedad de cadena, se supone que el operador \_ COP WORD \_ STARTSWITH $< .
-   Para todas las demás propiedades, se supone que el \_ operador COP EQUAL = .

Para el uso mediante programación de AQS, se recomienda tener siempre un operador explícito. El formulario válido para buscar un valor simple o un intervalo de valores es el siguiente:

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

Una consulta que busca un documento que contiene la fase "último trimestre", que ha creado Theresa o Lee y que se guardó en la carpeta MyDocs, combina tres consultas básicas como sigue:

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

Las tres consultas básicas son:

-   "último trimestre"
-   author:(theresa OR lee)
-   folder:MyDocs

Una consulta básica que usa la sintaxis canónica es:

``` syntax
System.Size:>1kb
```

### <a name="properties"></a>Propiedades

Una palabra clave hace referencia a las propiedades, que puede ser un nombre de propiedad canónico en Windows 7 y versiones posteriores. AQS en la interfaz Windows usuario puede usar la etiqueta en lugar del nombre de propiedad canónica, como author en lugar de [System.Author](../properties/props-system-author.md). En Windows Vista y versiones anteriores era posible usar etiquetas en inglés independientemente del idioma de la interfaz de usuario. En Windows 7 y versiones posteriores, Windows Search reconoce palabras clave solo en el lenguaje de interfaz de usuario predeterminado actual.

### <a name="support-for-custom-properties"></a>Compatibilidad con propiedades personalizadas

En Windows Vista y versiones anteriores, las propiedades personalizadas no estaban disponibles en AQS. En Windows 7 y versiones posteriores, AQS funciona con propiedades personalizadas registradas en el sistema de propiedades. Para obtener más información sobre cómo crear propiedades personalizadas, vea [Sistema de propiedades](../properties/building-property-handlers.md).

### <a name="datetime-properties-in-windows-8"></a>Propiedades DateTime en Windows 8

A partir Windows 8, las propiedades DateTime (como [System.DateModified)](../properties/props-system-datemodified.md)admiten el formato de fecha y hora canónico especificado por [ISO-8601,](https://www.w3.org/TR/NOTE-datetime)incluyendo opcionalmente la zona horaria UTC.

-   **Windows 8 y anteriores, fecha y** hora sin zona horaria UTC: *YYYY* - *MM* - *DDThh*:*mm*:*ss*

    Este formato especifica una hora local, independientemente de la configuración regional del usuario o del sistema.

-   **Windows 8, fecha y hora con zona** horaria UTC: *YYYY* - *MM* - *DDThh*:*mm*:*ssTZD*

    Este formato especifica una hora en la zona horaria UTC especificada.

## <a name="keyword-use-in-local-languages"></a>Uso de palabras clave en idiomas locales

En Windows 7 y versiones posteriores, las palabras clave mnemónicas solo funcionan en el idioma del sistema, como las palabras clave alemanas solo en un sistema operativo alemán y las palabras clave en inglés solo en un sistema operativo en inglés. [System.Author es](../properties/props-system-author.md) una palabra clave canónica y el valor mnemotécnico de la propiedad System.Author es Author, por ejemplo. La introducción de palabras clave canónicas compensa el hecho de que las palabras clave mnemotécnicas en inglés ya no se reconocen universalmente en todos los sistemas operativos independientemente del idioma, como era el caso en Windows Vista y versiones anteriores.

> [!Note]  
> En Windows 7 y versiones posteriores, Windows Search reconoce palabras clave solo en el idioma predeterminado actual y no en inglés a menos que el inglés sea el valor predeterminado actual. Se recomienda que los desarrolladores siempre usen la sintaxis canónica para que su aplicación no tenga problemas de lenguaje con las palabras clave.

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a>Sintaxis de consulta avanzada canónica en Windows 7

Se introdujo la sintaxis canónica para las palabras clave Windows 7. Un ejemplo de una consulta con una propiedad canónica es `System.Message.FromAddress:=me@microsoft.com` . Al codificar consultas en aplicaciones que se ejecutan en Windows 7 y versiones posteriores, debe usar la sintaxis canónica para generar consultas de AQS mediante programación. Si no usa la sintaxis canónica y la aplicación se implementa en una configuración regional o un lenguaje de interfaz de usuario diferente del idioma del código de la aplicación, las consultas no se interpretarán correctamente.

Las convenciones para la sintaxis de palabras clave canónicas son las siguientes:

-   La sintaxis canónica de una propiedad es su nombre canónico, como `System.Photo.LightSource` . Los nombres canónicos no distinguen mayúsculas de minúsculas.
-   La sintaxis canónica de los operadores booleanos consta de las palabras clave AND, OR y NOT, en mayúsculas.
-   Los operadores <, >, =, etc., no se localizan y, por tanto, también forman parte de la sintaxis canónica.
-   Si una propiedad ha enumerado valores o `P` intervalos denominados N₁ a través de Nk, la sintaxis canónica del valor o intervalo I es el nombre canónico de P, seguido del carácter , seguido de N I , como se muestra en el \# ejemplo siguiente:<sub></sub>
    -   `System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` , etc.
-   En el caso de un tipo semántico definido T con valores o intervalos denominados N₁ a través de Vez, la sintaxis canónica del valor o intervalo I es el nombre canónico de T, seguido del carácter , seguido de N I , como se muestra en \# el ejemplo siguiente:<sub></sub>
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   Para los valores literales, como palabras o frases, la sintaxis canónica es la misma que la sintaxis normal. Algunos ejemplos de consultas con valores literales en sintaxis canónica son:
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> No hay ninguna sintaxis canónica para los números de Windows 7 y versiones posteriores. Dado que los formatos de punto flotante varían entre configuraciones regionales, no se admite el uso de una consulta canónica que implique una constante de punto flotante. Las constantes de enteros, en cambio, solo se pueden escribir con dígitos (sin separadores para miles) y se pueden usar de forma segura en consultas canónicas en Windows 7 y versiones posteriores.

 

### <a name="examples"></a>Ejemplos

En la tabla siguiente se muestran algunos ejemplos de propiedades canónicas y la sintaxis para su uso.



| Tipo de propiedad canónica | Ejemplo                                                                                     | Syntax                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor de cadena               | [System.Author](../properties/props-system-author.md)<br/>    | Se busca el valor de cadena en la propiedad author: <br/>`System.Author:Jacobs`                                                                                                                                                              |
| Intervalo de enumeración          | [System.Priority](../properties/props-system-priority.md)             | La propiedad priority puede tener un intervalo de valores numéricos:<br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| Boolean                    | [System.IsDeleted](../properties/props-system-isdeleted.md)<br/> | Los valores booleanos se pueden usar con cualquier propiedad booleana:<br/>`System.IsDeleted:System.StructuredQueryType.Boolean#True`Y `System.IsDeleted:System.StructuredQueryType.Boolean#False`                                                             |
| Numérico                  | [System.Size](../properties/props-system-size.md)<br/>      | No es posible escribir de forma segura una consulta canónica que implique una constante de punto flotante, ya que los formatos de punto flotante varían entre configuraciones regionales. Los enteros deben escribirse sin separadores para miles. Por ejemplo:<br/>`System.Size:<12345` |



 

Para obtener más información sobre las propiedades canónicas y el sistema de propiedades en general, vea [Propiedades del sistema](../properties/props.md). Como alternativa, consulte los archivos de encabezado públicos.

### <a name="query-operators"></a>Operadores de consulta

Si una propiedad, p, tiene varios valores para algún elemento, una consulta de AQS para p: restr devuelve el elemento si restr es true para al menos uno &lt; &gt; de los &lt; &gt; valores.  ( &lt; restr &gt; representa una restricción).

La sintaxis enumerada en la tabla siguiente consta de un operador, un símbolo de operador, un ejemplo y una descripción de ejemplo. El operador y el símbolo se pueden usar en cualquier idioma e incluirse en cualquier consulta. No use los operadores \_ COP IMPLICIT o COP APPLICATION \_ \_ SPECIFIC. Algunos de los operadores tienen símbolos intercambiables.



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Operador</th>
<th>Símbolo</th>
<th>Ejemplo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COP_EQUAL</td>
<td>=<br/></td>
<td>System.FileExtension:= &quot;.txt&quot;<br/></td>
<td>El valor es la cadena &quot; <em>.txt</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_NOTEQUAL</td>
<td>≠<br/> -<br/> &lt;&gt;<br/> NOT<br/> - -<br/></td>
<td>System.Kind:≠picture<br/> System.Photo.DateTaken:-[]¹<br/> System.Kind: &lt; &gt; imagen<br/> System.Kind:NOT picture<br/> System.Kind:- -picture<br/></td>
<td>La <a href="/windows/desktop/properties/props-system-kind">propiedad System.Kind</a> no es una imagen.<br/> La <a href="/windows/desktop/properties/props-system-photo-datetaken">propiedad System.Photo.DateTaken</a> tiene un valor.<br/> La <a href="/windows/desktop/properties/props-system-kind">propiedad System.Kind</a> no es una imagen. <br/> La <a href="/windows/desktop/properties/props-system-kind">propiedad System.Kind</a> no es una imagen. <br/> Los operadores Double NOT aplicados a la misma propiedad no se cancelan. Por lo tanto, System.Kind:- -picture equivale a System.Kind:-picture y System.Kind:NOT picture.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHAN</td>
<td>&lt;<br/></td>
<td>System.Size: &lt; 1 kb<br/></td>
<td>Este valor es inferior a <em>1 kb.</em><br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHAN</td>
<td>&gt;<br/></td>
<td>System.ItemDate: &gt; System.StructuredQueryType.DateTime#Today<br/></td>
<td>Este valor es mayor que <em>hoy en día.</em><br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHANOREQUAL</td>
<td>&lt;=<br/> ≤<br/></td>
<td>System.Size: &lt; =1 kb<br/></td>
<td>Este valor es menor o igual que <em>1 kb.</em><br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHANOREQUAL</td>
<td>&gt;=<br/> ≥<br/></td>
<td>System.Size: &gt; =1 kb<br/></td>
<td>Este valor es igual o mayor que <em>1 kb.</em><br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_STARTSWITH</td>
<td>~&lt;<br/></td>
<td>System.FileName:~ &lt; &quot; C++ Primer&quot;<br/></td>
<td>Busca los elementos en los que el nombre de archivo comienza con los caracteres &quot; <em>C++ Primer</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_ENDSWITH</td>
<td>~&gt;<br/></td>
<td>System.Photo.CameraModel:~ &gt; non<br/></td>
<td>Busca los elementos en los que el valor de propiedad termina con los caracteres <em>distintos de</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_CONTAINS</td>
<td>~=<br/> ~~<br/></td>
<td>System.Subject.~=round <br/> System.Search.Autosummary:~~round<br/></td>
<td>Busca un mensaje que tiene esta cadena en el asunto y que coincidirá con las reglas de &quot; <em>redondeo</em> &quot; g, por ejemplo.<br/> Busca todos los elementos con un resumen automático que contiene los caracteres <em>redondeados.</em><br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_NOTCONTAINS</td>
<td>~!<br/></td>
<td>System.Author:~! &quot; Sanjay&quot;<br/></td>
<td>Busca autores que no tienen la secuencia de caracteres &quot; <em>sanjay</em> &quot; en ellos.<br/></td>
</tr>
<tr class="odd">
<td>COP_DOSWILDCARDS</td>
<td>~ <br/></td>
<td>System.FileName:~ &quot; Mic?osoft W*d&quot;<br/></td>
<td>Busca archivos donde el nombre de archivo comienza por <em>Mic</em>, seguido de algún carácter, seguido de <em>osoft w</em>, seguido de cualquier carácter que termine con <em>d</em>. <br/> El signo ? Los caracteres y * no se interpretan literalmente y funcionan como caracteres comodín de estilo DOS:<br/>
<ul>
<li>? coincide con un carácter arbitrario.</li>
<li>* coincide con cero o más caracteres arbitrarios.</li>
</ul></td>
</tr>
<tr class="even">
<td>COP_WORD_EQUAL</td>
<td>$=<br/> $$<br/></td>
<td>System.StructuredQuery.Virtual.From:$= &quot; SanjayMentes&quot;<br/></td>
<td>Para Windows 7 y versiones posteriores. Busca la frase &quot; <em>SanjayRías en</em> &quot; todas las propiedades From. La palabra <em>Sanjay</em> debe ir seguida de la <em>palabra Necesidad.</em><br/></td>
</tr>
<tr class="odd">
<td>COP_WORD_STARTSWITH</td>
<td>$<<br/></td>
<td>System.Author:$<&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td>Para Windows 7 y versiones posteriores. Busca cualquier elemento en el que Author contenga una palabra que empiece por los caracteres &quot; <em>San</em> &quot; .<br/> Busca cualquier archivo en el que el nombre de archivo contenga una palabra que empiece por <em>micro</em>, seguida de una palabra que empiece por <em>exe</em>.<br/></td>
</tr>
</tbody>
</table>



 

¹ Los corchetes vacíos ( \[ \] ) denotan "sin valor".

Para las propiedades de cadena, la operación predeterminada es COP \_ WORD STARTS WITH o COP WORD \_ \_ \_ \_ EQUAL.

### <a name="query-values"></a>Valores de consulta

En la tabla siguiente se muestran ejemplos útiles de cómo se pueden restringir los valores de consulta.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valor o símbolo</th>
<th>Ejemplos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>auto<br/></td>
<td>Cualquier secuencia de caracteres que se puedan buscar. La cadena no debe contener espacios en blanco ni combinaciones de caracteres que forman parte de la sintaxis. En este ejemplo se busca una palabra que comienza por <em>auto</em>.<br/></td>
</tr>
<tr class="even">
<td>Cadena entre comillas &quot;&quot;</td>
<td>&quot;Conclusiones: válido &quot; &quot; El equipo &quot; &quot; &quot; &quot; azul&quot;<br/></td>
<td>Cualquier secuencia de caracteres. La cadena no se interpreta como parte de la sintaxis.<br/> Las comillas se pueden incluir en una consulta si se duplican. En este ejemplo se busca <em>El &quot; equipo &quot; azul.</em><br/></td>
</tr>
<tr class="odd">
<td>Entero</td>
<td>5678<br/></td>
<td>Use solo dígitos para enteros. No use separadores para miles.<br/></td>
</tr>
<tr class="even">
<td>Número de punto flotante</td>
<td>5678.1234<br/></td>
<td>Dado que los formatos de punto flotante varían entre configuraciones regionales, una consulta canónica no puede usar una constante de punto flotante. El uso de la sintaxis canónica con números de punto flotante no es seguro para la localización. <br/></td>
</tr>
<tr class="odd">
<td>Boolean <strong>true</strong> / <strong>false</strong></td>
<td>System.IsRead:=System.StructuredQueryType.Boolean#True<br/> System.IsEncrypted:-System.StructuredQueryType.Boolean#False<br/></td>
<td>Valor <strong>booleano TRUE.</strong><br/> Valor <strong>booleano FALSE.</strong><br/></td>
</tr>
<tr class="even">
<td>[]</td>
<td>System.Keywords:=[]<br/></td>
<td>Los corchetes vacíos indican que no hay ningún valor. En este ejemplo se encuentran todos los elementos que no se han etiquetado. <br/></td>
</tr>
<tr class="odd">
<td>Fechas absolutas</td>
<td>System.ItemDate:26/1/2010<br/> SystemDateModified 10/15/2002 19:00<br/></td>
<td>Busca elementos con una fecha del 26 de enero de 2010.<br/> Busca los elementos que se modificaron el 15 de octubre de 2002 entre las 19:00:00 y las 19:00:59. <br/>
<blockquote>
[!Note]<br />
Dado que los formatos de fecha (como los formatos de punto flotante) varían entre configuraciones regionales, no se admite el uso de sintaxis canónica con fechas absolutas y no es seguro para la localización.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Fechas relativas</td>
<td>System.ItemDate:System.StructuredQueryType.DateTime#Today<br/> System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth<br/> System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear<br/></td>
<td>Busca elementos con la fecha de hoy.<br/> Busca elementos con una fecha en el mes siguiente.<br/> Busca elementos con una fecha del último año.<br/>
<blockquote>
[!Note]<br />
Además de buscar fechas e intervalos de fechas específicos, AQS reconoce los valores de fecha <em></em> relativos (como <em>hoy</em>, <em>mañana</em> <em>,</em>próxima semana <em>,</em>próximo mes) y día (como martes o <em>lunes). Miércoles</em>) y mes (<em>febrero</em>).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>..</td>
<td>System.ItemDate:11/05/04..11/10/04 System.Size:5kb.. 10 kb<br/></td>
<td>Los puntos dobles indican un intervalo de valores. Busca elementos con una fecha entre el 11/05/04 y el 11/10/04, ambos inclusive.<br/> Busca elementos de entre 5 y 10 kb de tamaño.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a>Restricciones de ámbito

Los usuarios pueden limitar el ámbito de sus búsquedas a ubicaciones de carpetas o almacenes de datos específicos. Por ejemplo, si usa varias cuentas de correo electrónico y desea limitar una consulta a Microsoft Outlook o Microsoft Outlook Express, puede usar o `System.Search.Store:mapi` `System.Search.Store:oe` respectivamente. En la tabla siguiente se muestran algunos ejemplos de cómo restringir una búsqueda por almacén de datos.



| Restricción de la búsqueda por almacén de datos  | Palabra clave | Ejemplo                                     |
|--------------------------------|---------|---------------------------------------------|
| Archivos                          | archivo    | System.Search.Store:file                    |
| Outlook                        | Mapi    | System.Search.Store:mapi                    |
| Outlook Express                | oe      | System.Search.Store:oe                      |
| Archivos sin conexión                  | Csc     | System.Search.Store:csc                     |
| Carpeta específica en la unidad local | folder  | System.ItemFolderNameDisplay:C:" \\ MyFolder" |



 

## <a name="additional-resources"></a>Recursos adicionales

-   En Windows 7 y versiones posteriores, puede haber una opción de menú contextual disponible en función de si se cumple una condición de AQS. Para obtener más información, vea "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" (Obtener comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada) en [Creating Context Menu Handlers](../shell/context-menu-handlers.md).
-   Las consultas de AQS se pueden limitar a tipos específicos de archivos, que se conocen como tipos de archivo. Para obtener más información, vea [Tipos de archivo y asociaciones](../shell/fa-intro.md). Para obtener documentación de referencia de propiedades, [vea System.Kind](../properties/props-system-kind.md)y [System.KindText](../properties/props-system-kindtext.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Usar SQL y enfoques de AQS para consultar el índice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Consulta del índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Consulta del índice con el protocolo search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Consulta del índice con la sintaxis Windows búsqueda SQL búsqueda](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 

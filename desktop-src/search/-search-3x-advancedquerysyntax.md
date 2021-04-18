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
# <a name="using-advanced-query-syntax-programmatically"></a><span data-ttu-id="f3fe0-103">Usar la sintaxis de consulta avanzada mediante programación</span><span class="sxs-lookup"><span data-stu-id="f3fe0-103">Using Advanced Query Syntax Programmatically</span></span>

<span data-ttu-id="f3fe0-104">La sintaxis de consulta avanzada (AQS) es la sintaxis de consulta predeterminada que usa Windows Search para consultar el índice y para refinar y restringir los parámetros de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-104">Advanced Query Syntax (AQS) is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="f3fe0-105">AQS lo emplean los desarrolladores para compilar consultas mediante programación (y los usuarios para restringir sus parámetros de búsqueda).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-105">AQS is employed by developers to build queries programmatically (and by users to narrow their search parameters).</span></span> <span data-ttu-id="f3fe0-106">AQS canónico se presentó en Windows 7 y se debe usar en Windows 7 y versiones posteriores para generar consultas AQS mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-106">Canonical AQS was introduced in Windows 7 and must be used in Windows 7 and later to programmatically generate AQS queries.</span></span>

<span data-ttu-id="f3fe0-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f3fe0-108">Acerca de la sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="f3fe0-108">About Advanced Query Syntax</span></span>](#about-advanced-query-syntax)
    -   [<span data-ttu-id="f3fe0-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f3fe0-109">Examples</span></span>](#examples)
    -   [<span data-ttu-id="f3fe0-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3fe0-110">Properties</span></span>](#properties)
-   [<span data-ttu-id="f3fe0-111">Uso de palabras clave en idiomas locales</span><span class="sxs-lookup"><span data-stu-id="f3fe0-111">Keyword Use in Local Languages</span></span>](#keyword-use-in-local-languages)
-   [<span data-ttu-id="f3fe0-112">Sintaxis de consulta avanzada canónica en Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3fe0-112">Canonical Advanced Query Syntax in Windows 7</span></span>](#canonical-advanced-query-syntax-in-windows-7)
    -   [<span data-ttu-id="f3fe0-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f3fe0-113">Examples</span></span>](#examples)
    -   [<span data-ttu-id="f3fe0-114">Operadores de consulta</span><span class="sxs-lookup"><span data-stu-id="f3fe0-114">Query Operators</span></span>](#query-operators)
    -   [<span data-ttu-id="f3fe0-115">Valores de consulta</span><span class="sxs-lookup"><span data-stu-id="f3fe0-115">Query Values</span></span>](#query-values)
-   [<span data-ttu-id="f3fe0-116">Restricciones de ámbito</span><span class="sxs-lookup"><span data-stu-id="f3fe0-116">Scope Restrictions</span></span>](#scope-restrictions)
-   [<span data-ttu-id="f3fe0-117">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f3fe0-117">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="f3fe0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3fe0-118">Related topics</span></span>](#related-topics)

## <a name="about-advanced-query-syntax"></a><span data-ttu-id="f3fe0-119">Acerca de la sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="f3fe0-119">About Advanced Query Syntax</span></span>

<span data-ttu-id="f3fe0-120">Una consulta consta de consultas básicas conectadas con AND, OR y NOT, tal y como se muestra en la siguiente sintaxis de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-120">A query consists of basic queries connected with AND, OR, and NOT, as shown in the following example syntax:</span></span>

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
> <span data-ttu-id="f3fe0-121">AQS no distingue entre mayúsculas y minúsculas, con la excepción de AND, OR y NOT, que debe estar en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-121">AQS is not case sensitive, with the exception of AND, OR, and NOT, which must be in all uppercase.</span></span>

 

<span data-ttu-id="f3fe0-122">Si una consulta tiene dos o más usos de AND u OR, se enlazarán de izquierda a derecha, independientemente de si es AND u or.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-122">If a query has two or more uses of AND or OR, they will bind from left to right, regardless of whether it is AND or OR.</span></span> <span data-ttu-id="f3fe0-123">Es decir, la consulta "Apple AND Perat o ciruela" se interpretará como si se hubiera escrito como "(Apple y peral) o ciruela", y la consulta, "Apple o pera y ciruela", se interpretará como si estuviera escrita como "(Apple o pera) y ciruela".</span><span class="sxs-lookup"><span data-stu-id="f3fe0-123">That is, the query, "apple AND pear OR plum" will be interpreted as if it were written as "(apple AND pear) OR plum", and the query, "apple OR pear AND plum", will be interpreted as if it were written as "(apple OR pear) AND plum".</span></span> <span data-ttu-id="f3fe0-124">Por lo tanto, si un documento contiene la palabra ciruela pero no Apple ni pera, la primera consulta la devolverá, pero la segunda consulta no.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-124">So if a document contains the word plum but neither apple, nor pear, the first query will return it but the second query will not.</span></span> <span data-ttu-id="f3fe0-125">Por lo tanto, se recomienda utilizar paréntesis explícitos para cualquier consulta que combine AND y OR para evitar errores o interpretaciones erróneas.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-125">Hence, we recommend that you use explicit parentheses for any query that mixes AND and OR to avoid mistakes or misinterpretations.</span></span>

<span data-ttu-id="f3fe0-126">Una consulta básica busca elementos que satisfacen una restricción de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-126">A basic query searches for items that satisfy a restriction over a property.</span></span> <span data-ttu-id="f3fe0-127">La única parte necesaria de una consulta básica es la restricción o el valor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-127">The only required portion of a basic query is the restriction or search value.</span></span> <span data-ttu-id="f3fe0-128">Si no se especifica una propiedad, Windows Search busca en todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-128">If you do not specify a property, Windows Search searches all properties.</span></span> <span data-ttu-id="f3fe0-129"><restr> representa la restricción de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-129"><restr> represents the search restriction.</span></span>

<span data-ttu-id="f3fe0-130">Los siguientes formatos para una consulta básica son válidos:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-130">The following forms for a basic query are valid:</span></span>

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

<span data-ttu-id="f3fe0-131">Una propiedad se designa mediante una palabra clave como Author o size, o bien mediante un nombre de propiedad canónico como [System. DateModified](../properties/props-system-datemodified.md).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-131">A property is designated by a keyword such as author or size, or by a canonical property name such as [System.DateModified](../properties/props-system-datemodified.md).</span></span> <span data-ttu-id="f3fe0-132">Los formatos válidos para una propiedad son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-132">Valid forms for a property are as follows:</span></span>

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

<span data-ttu-id="f3fe0-133">Un operador indica una operación como < o =.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-133">An operator indicates an operation such as < or =.</span></span> <span data-ttu-id="f3fe0-134">Para obtener una lista de operadores válidos, vea la sección operadores de consulta más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-134">For a list of valid operators, see the Query Operators section later in this topic.</span></span>

<span data-ttu-id="f3fe0-135">Una restricción básica es una restricción simple de una propiedad que se puede escribir sin paréntesis:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-135">A basic restriction is a simple restriction on a property that can be written without parentheses:</span></span>

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

<span data-ttu-id="f3fe0-136">Una restricción es un valor de búsqueda, como un valor numérico o un valor de cadena, opcionalmente con un operador.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-136">A restriction is a search value such as a number value or string value, optionally with an operator.</span></span> <span data-ttu-id="f3fe0-137">Los formatos válidos para una restricción son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-137">Valid forms for a restriction are as follows:</span></span>

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

<span data-ttu-id="f3fe0-138">Si no especifica ningún operador, Windows Search elige el operador más apropiado para la consulta:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-138">If you do not specify an operator, Windows Search chooses the most appropriate operator for your query:</span></span>

-   <span data-ttu-id="f3fe0-139">En el caso de una propiedad de cadena, \_ \_ se supone el operador COP Word STARTSWITH $<.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-139">For a string property, the COP\_WORD\_STARTSWITH $< operator is assumed.</span></span>
-   <span data-ttu-id="f3fe0-140">Para todas las demás propiedades, \_ se supone el operador COP igual que.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-140">For all other properties, the COP\_EQUAL = operator is assumed.</span></span>

<span data-ttu-id="f3fe0-141">Para el uso mediante programación de AQS, se recomienda tener siempre un operador explícito.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-141">For the programmatic use of AQS, we recommend that you always have an explicit operator.</span></span> <span data-ttu-id="f3fe0-142">El formato válido para buscar un valor simple o un intervalo de valores es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-142">The valid form for searching a simple value or value range is as follows:</span></span>

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

<span data-ttu-id="f3fe0-143">Un valor simple puede constar de cualquiera de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-143">A simple value can consist of any of the following types:</span></span>

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

### <a name="examples"></a><span data-ttu-id="f3fe0-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f3fe0-144">Examples</span></span>

<span data-ttu-id="f3fe0-145">Una consulta que busca un documento que contenga la fase "Last Quarter", creada por Theresa o lee y que se guardó en la carpeta Mis documentos, combina tres consultas básicas de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-145">A query that searches for a document containing the phase "last quarter," authored by Theresa or Lee, and that was saved to the folder MyDocs, combines three basic queries as follows:</span></span>

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

<span data-ttu-id="f3fe0-146">Las tres consultas básicas son:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-146">The three basic queries are:</span></span>

-   <span data-ttu-id="f3fe0-147">"último trimestre"</span><span class="sxs-lookup"><span data-stu-id="f3fe0-147">"last quarter"</span></span>
-   <span data-ttu-id="f3fe0-148">Autor: (Theresa o Lee)</span><span class="sxs-lookup"><span data-stu-id="f3fe0-148">author:(theresa OR lee)</span></span>
-   <span data-ttu-id="f3fe0-149">carpeta: mis documentos</span><span class="sxs-lookup"><span data-stu-id="f3fe0-149">folder:MyDocs</span></span>

<span data-ttu-id="f3fe0-150">Una consulta básica que usa sintaxis canónica es:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-150">A basic query that uses canonical syntax is:</span></span>

``` syntax
System.Size:>1kb
```

### <a name="properties"></a><span data-ttu-id="f3fe0-151">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3fe0-151">Properties</span></span>

<span data-ttu-id="f3fe0-152">Se hace referencia a las propiedades mediante una palabra clave, que puede ser un nombre de propiedad canónico en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-152">Properties are referred to by a keyword, which can be a canonical property name in Windows 7 and later.</span></span> <span data-ttu-id="f3fe0-153">AQS en la interfaz de usuario de Windows puede usar la etiqueta en lugar del nombre de propiedad canónico, como Author en lugar de [System. Author](../properties/props-system-author.md).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-153">AQS in the Windows UI can use the label instead of the canonical property name, such as author instead of [System.Author](../properties/props-system-author.md).</span></span> <span data-ttu-id="f3fe0-154">En Windows Vista y versiones anteriores, era posible usar etiquetas en inglés independientemente del idioma de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-154">In Windows Vista and earlier it was possible to use English labels regardless of the UI language.</span></span> <span data-ttu-id="f3fe0-155">En Windows 7 y versiones posteriores, Windows Search solo reconoce palabras clave en el idioma de la interfaz de usuario predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-155">In Windows 7 and later, Windows Search recognizes keywords in the current default UI language only.</span></span>

### <a name="support-for-custom-properties"></a><span data-ttu-id="f3fe0-156">Compatibilidad con propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="f3fe0-156">Support for Custom Properties</span></span>

<span data-ttu-id="f3fe0-157">En Windows Vista y versiones anteriores, las propiedades personalizadas no estaban disponibles en AQS.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-157">In Windows Vista and earlier, custom properties were not available in AQS.</span></span> <span data-ttu-id="f3fe0-158">En Windows 7 y versiones posteriores, AQS funciona con propiedades personalizadas que se registran con el sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-158">In Windows 7 and later, AQS works with custom properties that are registered with the property system.</span></span> <span data-ttu-id="f3fe0-159">Para obtener más información sobre la creación de propiedades personalizadas, vea [sistema de propiedades](../properties/building-property-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-159">For more information on creating custom properties, see [Property System](../properties/building-property-handlers.md).</span></span>

### <a name="datetime-properties-in-windows-8"></a><span data-ttu-id="f3fe0-160">Propiedades DateTime en Windows 8</span><span class="sxs-lookup"><span data-stu-id="f3fe0-160">DateTime properties in Windows 8</span></span>

<span data-ttu-id="f3fe0-161">A partir de Windows 8, las propiedades DateTime (como [System. DateModified](../properties/props-system-datemodified.md)) admiten el formato canónico de fecha y hora especificado por [ISO-8601](https://www.w3.org/TR/NOTE-datetime), incluida opcionalmente la zona horaria UTC.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-161">As of Windows 8, DateTime properties (like [System.DateModified](../properties/props-system-datemodified.md)) support the canonical date and time format specified by [ISO-8601](https://www.w3.org/TR/NOTE-datetime), optionally including the UTC time zone.</span></span>

-   <span data-ttu-id="f3fe0-162">**Windows 8 y versiones anteriores, fecha y hora sin zona horaria UTC:** *yyyy* - *mm* - *DDTHH*:*mm*:*SS*</span><span class="sxs-lookup"><span data-stu-id="f3fe0-162">**Windows 8 and earlier, date-time without UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ss*</span></span>

    <span data-ttu-id="f3fe0-163">Este formato especifica una hora local, independientemente de la configuración regional del usuario o del sistema.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-163">This format specifies a local time, regardless of the user or system locale.</span></span>

-   <span data-ttu-id="f3fe0-164">**Windows 8, fecha y hora con la zona horaria UTC:** *yyyy* - *mm* - *DDTHH*:*mm*:*ssTZD*</span><span class="sxs-lookup"><span data-stu-id="f3fe0-164">**Windows 8, date-time with UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ssTZD*</span></span>

    <span data-ttu-id="f3fe0-165">Este formato especifica una hora en la zona horaria UTC especificada.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-165">This format specifies a time at the specified UTC time zone.</span></span>

## <a name="keyword-use-in-local-languages"></a><span data-ttu-id="f3fe0-166">Uso de palabras clave en idiomas locales</span><span class="sxs-lookup"><span data-stu-id="f3fe0-166">Keyword Use in Local Languages</span></span>

<span data-ttu-id="f3fe0-167">En Windows 7 y versiones posteriores, las palabras clave de teclas de complemento solo funcionan en el idioma del sistema, como las palabras clave alemanas solo en un sistema operativo alemán y en inglés solo en un sistema operativo en inglés.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-167">In Windows 7 and later, mnemonic keywords work in the system language only, such as German keywords only on a German operating system, and English keywords only on an English operating system.</span></span> <span data-ttu-id="f3fe0-168">[System. Author](../properties/props-system-author.md) es una palabra clave canónica y el valor de tecla de acceso de la propiedad System. Author es Author, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-168">[System.Author](../properties/props-system-author.md) is a canonical keyword, and the mnemonic value for the System.Author property is Author, for example.</span></span> <span data-ttu-id="f3fe0-169">La introducción de las palabras clave canónicas compensa el hecho de que las palabras clave de la tecla de teclas de carácter de idioma no se reconocen universalmente en todos los sistemas operativos, independientemente del lenguaje, como era el caso en Windows Vista y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-169">The introduction of canonical keywords compensates for the fact that English mnemonic keywords are no longer universally recognized on all operating systems regardless of language, as was the case in Windows Vista and earlier.</span></span>

> [!Note]  
> <span data-ttu-id="f3fe0-170">En Windows 7 y versiones posteriores, Windows Search solo reconoce palabras clave en el idioma predeterminado actual y no en inglés, a menos que el inglés sea el valor predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-170">In Windows 7 and later, Windows Search recognizes keywords in the current default language only, and not in English unless English is the current default.</span></span> <span data-ttu-id="f3fe0-171">Se recomienda que los desarrolladores utilicen siempre sintaxis canónica para que su aplicación no tenga problemas de idioma con las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-171">We recommend that developers always use canonical syntax so that their application won't have language problems with keywords.</span></span>

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a><span data-ttu-id="f3fe0-172">Sintaxis de consulta avanzada canónica en Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3fe0-172">Canonical Advanced Query Syntax in Windows 7</span></span>

<span data-ttu-id="f3fe0-173">Se presentó la sintaxis canónica para las palabras clave de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-173">Canonical syntax was introduced for keywords in Windows 7.</span></span> <span data-ttu-id="f3fe0-174">Un ejemplo de una consulta con una propiedad canónica es `System.Message.FromAddress:=me@microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="f3fe0-174">An example of a query with a canonical property is `System.Message.FromAddress:=me@microsoft.com`.</span></span> <span data-ttu-id="f3fe0-175">Al codificar consultas en aplicaciones que se ejecutan en Windows 7 y versiones posteriores, debe usar la sintaxis canónica para generar consultas AQS mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-175">When coding queries in applications running on Windows 7 and later, you must use canonical syntax to programmatically generate AQS queries.</span></span> <span data-ttu-id="f3fe0-176">Si no usa la sintaxis canónica y la aplicación se implementa en un idioma de interfaz de usuario o en una configuración regional diferente del lenguaje del código de aplicación, las consultas no se interpretarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-176">If you do not use canonical syntax and your application is deployed in a locale or UI language different from the language in the application code, your queries will not be interpreted correctly.</span></span>

<span data-ttu-id="f3fe0-177">Las convenciones de la sintaxis de palabra clave canónica son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-177">The conventions for canonical keyword syntax are as follows:</span></span>

-   <span data-ttu-id="f3fe0-178">La sintaxis canónica para una propiedad es su nombre canónico, como `System.Photo.LightSource` .</span><span class="sxs-lookup"><span data-stu-id="f3fe0-178">The canonical syntax for a property is its canonical name, such as `System.Photo.LightSource`.</span></span> <span data-ttu-id="f3fe0-179">Los nombres canónicos no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-179">Canonical names are not case sensitive.</span></span>
-   <span data-ttu-id="f3fe0-180">La sintaxis canónica para los operadores booleanos consta de las palabras clave AND, OR y NOT, en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-180">The canonical syntax for the Boolean operators consists of the keywords AND, OR, and NOT, in all uppercase.</span></span>
-   <span data-ttu-id="f3fe0-181">Los operadores <, >, =, etc., no están localizados y, por tanto, también forman parte de la sintaxis canónica.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-181">The operators <, >, =, and so forth, are not localized and are thus also part of the canonical syntax.</span></span>
-   <span data-ttu-id="f3fe0-182">Si una propiedad `P` tiene valores enumerados o intervalos denominados N ₁ a NK, la sintaxis canónica del valor o del intervalo *I* es el nombre canónico de P, seguido del carácter \# , seguido de N <sub>I</sub>, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-182">If a property `P` has enumerated values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for P, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   <span data-ttu-id="f3fe0-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` , y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA`, and so forth.</span></span>
-   <span data-ttu-id="f3fe0-184">Para un tipo semántico definido T con valores o intervalos denominados N ₁ a NK, la sintaxis canónica del valor o del intervalo *I* es el nombre canónico de T, seguido del carácter \# , seguido de N <sub>I</sub>, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-184">For a defined semantic type T with values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for T, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   <span data-ttu-id="f3fe0-185">Para los valores literales como palabras o frases, la sintaxis canónica es la misma que la sintaxis normal.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-185">For literal values such as words or phrases, the canonical syntax is the same as the regular syntax.</span></span> <span data-ttu-id="f3fe0-186">Ejemplos de consultas con valores literales en sintaxis canónica son:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-186">Examples of queries with literal values in canonical syntax are:</span></span>
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> <span data-ttu-id="f3fe0-187">No hay ninguna sintaxis canónica para los números en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-187">There is no canonical syntax for numbers in Windows 7 and later.</span></span> <span data-ttu-id="f3fe0-188">Dado que los formatos de punto flotante varían entre las configuraciones regionales, no se admite el uso de una consulta canónica que implique una constante de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-188">Because floating point formats vary among locales, the use of a canonical query that involves a floating point constant is not supported.</span></span> <span data-ttu-id="f3fe0-189">Por el contrario, las constantes de tipo entero solo se pueden escribir con dígitos (sin separadores para miles) y se pueden usar de forma segura en consultas canónicas en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-189">Integer constants, in contrast, can be written using only digits (no separators for thousands) and can be safely used in canonical queries in Windows 7 and later.</span></span>

 

### <a name="examples"></a><span data-ttu-id="f3fe0-190">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f3fe0-190">Examples</span></span>

<span data-ttu-id="f3fe0-191">En la tabla siguiente se muestran algunos ejemplos de propiedades canónicas y la sintaxis para usarlas.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-191">The following table shows some examples of canonical properties and the syntax for using them.</span></span>



| <span data-ttu-id="f3fe0-192">Tipo de propiedad canónica</span><span class="sxs-lookup"><span data-stu-id="f3fe0-192">Type of canonical property</span></span> | <span data-ttu-id="f3fe0-193">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3fe0-193">Example</span></span>                                                                                     | <span data-ttu-id="f3fe0-194">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3fe0-194">Syntax</span></span>                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3fe0-195">Valor de cadena</span><span class="sxs-lookup"><span data-stu-id="f3fe0-195">String value</span></span>               | [<span data-ttu-id="f3fe0-196">System.Author</span><span class="sxs-lookup"><span data-stu-id="f3fe0-196">System.Author</span></span>](../properties/props-system-author.md)<br/>    | <span data-ttu-id="f3fe0-197">El valor de cadena se busca en la propiedad Author:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-197">The string value is searched for in the author property:</span></span> <br/>`System.Author:Jacobs`                                                                                                                                                              |
| <span data-ttu-id="f3fe0-198">Intervalo de enumeración</span><span class="sxs-lookup"><span data-stu-id="f3fe0-198">Enumeration range</span></span>          | [<span data-ttu-id="f3fe0-199">System. Priority</span><span class="sxs-lookup"><span data-stu-id="f3fe0-199">System.Priority</span></span>](../properties/props-system-priority.md)             | <span data-ttu-id="f3fe0-200">La propiedad Priority puede tener un intervalo de valores numéricos:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-200">The priority property can have a numerical value range:</span></span><br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| <span data-ttu-id="f3fe0-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="f3fe0-201">Boolean</span></span>                    | [<span data-ttu-id="f3fe0-202">System. IsDeleted</span><span class="sxs-lookup"><span data-stu-id="f3fe0-202">System.IsDeleted</span></span>](../properties/props-system-isdeleted.md)<br/> | <span data-ttu-id="f3fe0-203">Los valores booleanos se pueden usar con cualquier propiedad booleana:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-203">Boolean values can be used with any Boolean property:</span></span><br/><span data-ttu-id="f3fe0-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True` y `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span><span class="sxs-lookup"><span data-stu-id="f3fe0-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, and `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span></span>                                                             |
| <span data-ttu-id="f3fe0-205">Numérico</span><span class="sxs-lookup"><span data-stu-id="f3fe0-205">Numerical</span></span>                  | [<span data-ttu-id="f3fe0-206">System. Size</span><span class="sxs-lookup"><span data-stu-id="f3fe0-206">System.Size</span></span>](../properties/props-system-size.md)<br/>      | <span data-ttu-id="f3fe0-207">No es posible escribir de forma segura una consulta canónica que implique una constante de punto flotante, ya que los formatos de punto flotante varían entre las configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-207">It is not possible to write safely a canonical query that involves a floating point constant, because floating point formats vary among locales.</span></span> <span data-ttu-id="f3fe0-208">Los enteros se deben escribir sin separadores para miles.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-208">Integers must be written with no separators for thousands.</span></span> <span data-ttu-id="f3fe0-209">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-209">For example:</span></span><br/>`System.Size:<12345` |



 

<span data-ttu-id="f3fe0-210">Para obtener más información sobre las propiedades canónicas y el sistema de propiedades en general, consulte [propiedades del sistema](../properties/props.md).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-210">For more information about canonical properties and the property system generally, see [System Properties](../properties/props.md).</span></span> <span data-ttu-id="f3fe0-211">También puede hacer referencia a los archivos de encabezado públicos.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-211">Alternatively, refer to the public header files.</span></span>

### <a name="query-operators"></a><span data-ttu-id="f3fe0-212">Operadores de consulta</span><span class="sxs-lookup"><span data-stu-id="f3fe0-212">Query Operators</span></span>

<span data-ttu-id="f3fe0-213">Si una propiedad, p, tiene varios valores para algún elemento, una consulta AQS para p: <restr> devuelve el elemento si <restr> es **true** para al menos uno de los valores.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-213">If a property, p, has multiple values for some item, an AQS query for p:<restr> returns the item if <restr> is **true** for at least one of the values.</span></span> <span data-ttu-id="f3fe0-214">( <restr> representa una restricción).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-214">(<restr> represents a restriction.)</span></span>

<span data-ttu-id="f3fe0-215">La sintaxis que se muestra en la tabla siguiente consta de un operador, un símbolo de operador, un ejemplo y una descripción de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-215">The syntax listed in the following table consists of an operator, operator symbol, example and example description.</span></span> <span data-ttu-id="f3fe0-216">El operador y el símbolo se pueden usar en cualquier lenguaje e incluirse en cualquier consulta.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-216">The operator and symbol can be used in any language and included in any query.</span></span> <span data-ttu-id="f3fe0-217">No use los \_ operadores específicos de la aplicación COP IMPLICIT o COP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f3fe0-217">Do not use the COP\_IMPLICIT or COP\_APPLICATION\_SPECIFIC operators.</span></span> <span data-ttu-id="f3fe0-218">Algunos de los operadores tienen símbolos intercambiables.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-218">Some of the operators have interchangeable symbols.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3fe0-219">Operator</span><span class="sxs-lookup"><span data-stu-id="f3fe0-219">Operator</span></span></th>
<th><span data-ttu-id="f3fe0-220">Símbolo</span><span class="sxs-lookup"><span data-stu-id="f3fe0-220">Symbol</span></span></th>
<th><span data-ttu-id="f3fe0-221">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3fe0-221">Example</span></span></th>
<th><span data-ttu-id="f3fe0-222">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3fe0-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3fe0-223">COP_EQUAL</span><span class="sxs-lookup"><span data-stu-id="f3fe0-223">COP_EQUAL</span></span></td>
<td>=<br/></td>
<td><span data-ttu-id="f3fe0-224">System. FileExtension: = &quot; . txt&quot;</span><span class="sxs-lookup"><span data-stu-id="f3fe0-224">System.FileExtension:=&quot;.txt&quot;</span></span><br/></td>
<td><span data-ttu-id="f3fe0-225">El valor es String &quot; <em>. txt</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="f3fe0-225">The value is the string &quot;<em>.txt</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-226">COP_NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="f3fe0-226">COP_NOTEQUAL</span></span></td>
<td><span data-ttu-id="f3fe0-227">≠</span><span class="sxs-lookup"><span data-stu-id="f3fe0-227">≠</span></span><br/> -<br/> &lt;&gt;<br/> <span data-ttu-id="f3fe0-228">NOT</span><span class="sxs-lookup"><span data-stu-id="f3fe0-228">NOT</span></span><br/> - -<br/></td>
<td><span data-ttu-id="f3fe0-229">System. Kind: ≠ imagen</span><span class="sxs-lookup"><span data-stu-id="f3fe0-229">System.Kind:≠picture</span></span><br/> <span data-ttu-id="f3fe0-230">System. Photo. DateTaken:-[] ¹</span><span class="sxs-lookup"><span data-stu-id="f3fe0-230">System.Photo.DateTaken:-[]¹</span></span><br/> <span data-ttu-id="f3fe0-231">System. Kind: &lt; &gt; imagen</span><span class="sxs-lookup"><span data-stu-id="f3fe0-231">System.Kind:&lt;&gt;picture</span></span><br/> <span data-ttu-id="f3fe0-232">System. Kind: no imagen</span><span class="sxs-lookup"><span data-stu-id="f3fe0-232">System.Kind:NOT picture</span></span><br/> <span data-ttu-id="f3fe0-233">System. Kind:--imagen</span><span class="sxs-lookup"><span data-stu-id="f3fe0-233">System.Kind:- -picture</span></span><br/></td>
<td><span data-ttu-id="f3fe0-234">La propiedad <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> no es una imagen.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-234">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span><br/> <span data-ttu-id="f3fe0-235">La propiedad <a href="/windows/desktop/properties/props-system-photo-datetaken">System. Photo. DateTaken</a> tiene un valor.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-235">The <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken</a> property has a value.</span></span><br/> <span data-ttu-id="f3fe0-236">La propiedad <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> no es una imagen.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-236">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="f3fe0-237">La propiedad <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> no es una imagen.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-237">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="f3fe0-238">Los operadores Double no aplicados a la misma propiedad no se cancelan. Por lo tanto, System. Kind:--Picture es equivalente a System. Kind:-Picture y System. Kind: NOT Picture.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-238">Double NOT operators applied to the same property do not cancel out. Hence, System.Kind:- -picture is equivalent to System.Kind:-picture and System.Kind:NOT picture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-239">COP_LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="f3fe0-239">COP_LESSTHAN</span></span></td>
<td>&lt;<br/></td>
<td><span data-ttu-id="f3fe0-240">System. Size: &lt; 1 KB</span><span class="sxs-lookup"><span data-stu-id="f3fe0-240">System.Size:&lt;1kb</span></span><br/></td>
<td><span data-ttu-id="f3fe0-241">Este valor es menor que <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-241">This value is less than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-242">COP_GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="f3fe0-242">COP_GREATERTHAN</span></span></td>
<td>&gt;<br/></td>
<td><span data-ttu-id="f3fe0-243">System. ItemDate: &gt; System. StructuredQueryType. DateTime # Today</span><span class="sxs-lookup"><span data-stu-id="f3fe0-243">System.ItemDate:&gt;System.StructuredQueryType.DateTime#Today</span></span><br/></td>
<td><span data-ttu-id="f3fe0-244">Este valor es mayor que <em>hoy</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-244">This value is greater than <em>today</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-245">COP_LESSTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="f3fe0-245">COP_LESSTHANOREQUAL</span></span></td>
<td>&lt;=<br/> <span data-ttu-id="f3fe0-246">≤</span><span class="sxs-lookup"><span data-stu-id="f3fe0-246">≤</span></span><br/></td>
<td><span data-ttu-id="f3fe0-247">System. Size: &lt; = 1 KB</span><span class="sxs-lookup"><span data-stu-id="f3fe0-247">System.Size:&lt;=1kb</span></span><br/></td>
<td><span data-ttu-id="f3fe0-248">Este valor es menor o igual que <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-248">This value is less than or equal to <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-249">COP_GREATERTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="f3fe0-249">COP_GREATERTHANOREQUAL</span></span></td>
<td>&gt;=<br/> <span data-ttu-id="f3fe0-250">≥</span><span class="sxs-lookup"><span data-stu-id="f3fe0-250">≥</span></span><br/></td>
<td><span data-ttu-id="f3fe0-251">System. Size: &gt; = 1 KB</span><span class="sxs-lookup"><span data-stu-id="f3fe0-251">System.Size:&gt;=1kb</span></span><br/></td>
<td><span data-ttu-id="f3fe0-252">Este valor es igual o mayor que <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-252">This value is equal to or greater than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-253">COP_VALUE_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="f3fe0-253">COP_VALUE_STARTSWITH</span></span></td>
<td>~&lt;<br/></td>
<td><span data-ttu-id="f3fe0-254">System. FileName: ~ &lt; &quot; C++ manual&quot;</span><span class="sxs-lookup"><span data-stu-id="f3fe0-254">System.FileName:~&lt;&quot;C++ Primer&quot;</span></span><br/></td>
<td><span data-ttu-id="f3fe0-255">Busca los elementos en los que el nombre de archivo comienza con los caracteres de &quot; <em>C++ manual</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="f3fe0-255">Finds items where the file name begins with the characters &quot;<em>C++ Primer</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-256">COP_VALUE_ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="f3fe0-256">COP_VALUE_ENDSWITH</span></span></td>
<td>~&gt;<br/></td>
<td><span data-ttu-id="f3fe0-257">System. Photo. CameraModel: ~ &gt; no</span><span class="sxs-lookup"><span data-stu-id="f3fe0-257">System.Photo.CameraModel:~&gt;non</span></span><br/></td>
<td><span data-ttu-id="f3fe0-258">Busca los elementos en los que el valor de propiedad termina con los caracteres <em>no</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-258">Finds items where the property value ends with the characters <em>non</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-259">COP_VALUE_CONTAINS</span><span class="sxs-lookup"><span data-stu-id="f3fe0-259">COP_VALUE_CONTAINS</span></span></td>
<td>~=<br/> ~~<br/></td>
<td><span data-ttu-id="f3fe0-260">System. Subject. ~ = round</span><span class="sxs-lookup"><span data-stu-id="f3fe0-260">System.Subject.~=round</span></span> <br/> <span data-ttu-id="f3fe0-261">System. Search. autosummary: ~ ~ Round</span><span class="sxs-lookup"><span data-stu-id="f3fe0-261">System.Search.Autosummary:~~round</span></span><br/></td>
<td><span data-ttu-id="f3fe0-262">Busca un mensaje que tenga esta cadena en el asunto y coincidirá con &quot; las reglas de<em>redondeo</em> g &quot; por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-262">Finds a message that has this string in the subject, and will match &quot;g<em>round</em> rules&quot; for example.</span></span><br/> <span data-ttu-id="f3fe0-263">Busca todos los elementos con un Autoresumen que contenga los caracteres <em>redondeados</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-263">Finds all items with an Autosummary that contains the characters <em>round</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-264">COP_VALUE_NOTCONTAINS</span><span class="sxs-lookup"><span data-stu-id="f3fe0-264">COP_VALUE_NOTCONTAINS</span></span></td>
<td><span data-ttu-id="f3fe0-265">~!</span><span class="sxs-lookup"><span data-stu-id="f3fe0-265">~!</span></span><br/></td>
<td><span data-ttu-id="f3fe0-266">System. Author: ~! &quot; Sanjay&quot;</span><span class="sxs-lookup"><span data-stu-id="f3fe0-266">System.Author:~!&quot;sanjay&quot;</span></span><br/></td>
<td><span data-ttu-id="f3fe0-267">Busca los autores que no tienen la secuencia de caracteres &quot; <em>Sanjay</em> &quot; en ellos.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-267">Finds authors that do not have the character sequence&quot;<em>sanjay</em>&quot; in them.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-268">COP_DOSWILDCARDS</span><span class="sxs-lookup"><span data-stu-id="f3fe0-268">COP_DOSWILDCARDS</span></span></td>
<td>~ <br/></td>
<td><span data-ttu-id="f3fe0-269">System. FileName: ~ &quot; MIC? osoft W \* d&quot;</span><span class="sxs-lookup"><span data-stu-id="f3fe0-269">System.FileName:~&quot;Mic?osoft W\*d&quot;</span></span><br/></td>
<td><span data-ttu-id="f3fe0-270">Busca archivos en los que el nombre de archivo empieza por <em>MIC</em>, seguido de algún carácter seguido de <em>osoft w</em>, seguido de los caracteres que terminan en <em>d</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-270">Finds files where the file name starts with <em>Mic</em>, followed by some character, followed by <em>osoft w</em>, followed by any characters ending with <em>d</em>.</span></span> <br/> <span data-ttu-id="f3fe0-271">El signo ?</span><span class="sxs-lookup"><span data-stu-id="f3fe0-271">The ?</span></span> <span data-ttu-id="f3fe0-272">los caracteres y \* no se interpretan literalmente y funcionan como caracteres comodín de estilo de DOS:</span><span class="sxs-lookup"><span data-stu-id="f3fe0-272">and \* characters are not interpreted literally, and work like DOS-style wildcard characters:</span></span><br/>
<ul>
<li><span data-ttu-id="f3fe0-273">?</span><span class="sxs-lookup"><span data-stu-id="f3fe0-273">?</span></span> <span data-ttu-id="f3fe0-274">coincide con un carácter arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-274">matches one arbitrary character.</span></span></li>
<li><span data-ttu-id="f3fe0-275">\* coincide con cero o más caracteres arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-275">\* matches zero or more arbitrary characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-276">COP_WORD_EQUAL</span><span class="sxs-lookup"><span data-stu-id="f3fe0-276">COP_WORD_EQUAL</span></span></td>
<td>$=<br/> $$<br/></td>
<td><span data-ttu-id="f3fe0-277">System. StructuredQuery. virtual. from: $ = &quot; Sanjay Jacobs&quot;</span><span class="sxs-lookup"><span data-stu-id="f3fe0-277">System.StructuredQuery.Virtual.From:$=&quot;Sanjay Jacobs&quot;</span></span><br/></td>
<td><span data-ttu-id="f3fe0-278">Para Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-278">For Windows 7 and later.</span></span> <span data-ttu-id="f3fe0-279">Busca la frase &quot; <em>Sanjay Jacobs</em> &quot; en todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-279">Finds the phrase &quot;<em>Sanjay Jacobs</em>&quot; in all From properties.</span></span> <span data-ttu-id="f3fe0-280">La palabra <em>Sanjay</em> debe ir seguida de la palabra <em>Jacobs</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-280">The word <em>Sanjay</em> must be followed by the word <em>Jacobs</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-281">COP_WORD_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="f3fe0-281">COP_WORD_STARTSWITH</span></span></td>
<td>$<<br/></td>
<td><span data-ttu-id="f3fe0-282">System. Author: $</span><span class="sxs-lookup"><span data-stu-id="f3fe0-282">System.Author:$</span></span><&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td><span data-ttu-id="f3fe0-283">Para Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-283">For Windows 7 and later.</span></span> <span data-ttu-id="f3fe0-284">Busca cualquier elemento donde Author contenga una palabra que empiece con los caracteres &quot; <em>San</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="f3fe0-284">Finds any item where Author contains a word starting with the characters &quot;<em>San</em>&quot;.</span></span><br/> <span data-ttu-id="f3fe0-285">Busca cualquier archivo en el que el nombre de archivo contenga una palabra que comience por <em>micro</em>, seguida de una palabra que comience por <em>exe</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-285">Finds any file in which the file name contains a word starting with <em>micro</em>, followed by a word starting with <em>exe</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f3fe0-286">¹ los corchetes vacíos ( \[ \] ) denotan "sin valor".</span><span class="sxs-lookup"><span data-stu-id="f3fe0-286">¹ Empty square brackets (\[\]) denote "no value".</span></span>

<span data-ttu-id="f3fe0-287">En el caso de las propiedades de cadena, la operación predeterminada es COP \_ Word \_ comienza \_ con o COP \_ Word \_ igual.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-287">For string properties the default operation is either COP\_WORD\_STARTS\_WITH or COP\_WORD\_EQUAL.</span></span>

### <a name="query-values"></a><span data-ttu-id="f3fe0-288">Valores de consulta</span><span class="sxs-lookup"><span data-stu-id="f3fe0-288">Query Values</span></span>

<span data-ttu-id="f3fe0-289">En la tabla siguiente se muestran ejemplos útiles de cómo se pueden restringir los valores de consulta.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-289">Useful examples of how query values can be restricted are listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3fe0-290">Valor/símbolo</span><span class="sxs-lookup"><span data-stu-id="f3fe0-290">Value/symbol</span></span></th>
<th><span data-ttu-id="f3fe0-291">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f3fe0-291">Examples</span></span></th>
<th><span data-ttu-id="f3fe0-292">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3fe0-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3fe0-293">String</span><span class="sxs-lookup"><span data-stu-id="f3fe0-293">String</span></span></td>
<td><span data-ttu-id="f3fe0-294">auto</span><span class="sxs-lookup"><span data-stu-id="f3fe0-294">auto</span></span><br/></td>
<td><span data-ttu-id="f3fe0-295">Cualquier secuencia de caracteres que se puede buscar.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-295">Any sequence of characters that can be searched for.</span></span> <span data-ttu-id="f3fe0-296">La cadena no debe contener espacios en blanco ni combinaciones de caracteres que formen parte de la sintaxis.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-296">The string must not contain whitespace or character combinations that are part of the syntax.</span></span> <span data-ttu-id="f3fe0-297">En este ejemplo se busca una palabra que comience por <em>auto</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-297">This example searches for a word beginning with <em>auto</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-298">Cadena entre comillas &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="f3fe0-298">Quoted string &quot;&quot;</span></span></td>
<td><span data-ttu-id="f3fe0-299">&quot;CONCLUSIONES: &quot; &quot; el &quot; &quot; equipo azul &quot; &quot; es válido&quot;</span><span class="sxs-lookup"><span data-stu-id="f3fe0-299">&quot;Conclusions: valid&quot; &quot;The &quot;&quot;blue&quot;&quot; team&quot;</span></span><br/></td>
<td><span data-ttu-id="f3fe0-300">Cualquier secuencia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-300">Any sequence of characters.</span></span> <span data-ttu-id="f3fe0-301">La cadena no se interpreta como parte de la sintaxis.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-301">The string is not interpreted as part of the syntax.</span></span><br/> <span data-ttu-id="f3fe0-302">Las comillas se pueden incluir en una consulta si se duplican.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-302">Quotation marks can be included in a query if they are doubled.</span></span> <span data-ttu-id="f3fe0-303">Este ejemplo busca <em>el &quot; &quot; equipo azul</em>.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-303">This example searches for <em>The &quot;blue&quot; team</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-304">Entero</span><span class="sxs-lookup"><span data-stu-id="f3fe0-304">Integer</span></span></td>
<td><span data-ttu-id="f3fe0-305">5678</span><span class="sxs-lookup"><span data-stu-id="f3fe0-305">5678</span></span><br/></td>
<td><span data-ttu-id="f3fe0-306">Use solo dígitos para enteros.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-306">Use only digits for integers.</span></span> <span data-ttu-id="f3fe0-307">No use ningún separador para miles.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-307">Do not use any separators for thousands.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-308">Número de punto flotante</span><span class="sxs-lookup"><span data-stu-id="f3fe0-308">Floating point number</span></span></td>
<td><span data-ttu-id="f3fe0-309">5678,1234</span><span class="sxs-lookup"><span data-stu-id="f3fe0-309">5678.1234</span></span><br/></td>
<td><span data-ttu-id="f3fe0-310">Dado que los formatos de punto flotante varían entre las configuraciones regionales, una consulta canónica no puede usar una constante de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-310">Because floating point formats vary among locales, a canonical query cannot use a floating point constant.</span></span> <span data-ttu-id="f3fe0-311">El uso de sintaxis canónica con números de punto flotante no es seguro para la localización.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-311">The use of canonical syntax with floating point numbers is not localization safe.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-312">Booleano <strong>true</strong> / <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="f3fe0-312">Boolean <strong>true</strong>/<strong>false</strong></span></span></td>
<td><span data-ttu-id="f3fe0-313">System. IsRead: = System. StructuredQueryType. Boolean # true</span><span class="sxs-lookup"><span data-stu-id="f3fe0-313">System.IsRead:=System.StructuredQueryType.Boolean#True</span></span><br/> <span data-ttu-id="f3fe0-314">System. IsEncrypted:-System. StructuredQueryType. Boolean # false</span><span class="sxs-lookup"><span data-stu-id="f3fe0-314">System.IsEncrypted:-System.StructuredQueryType.Boolean#False</span></span><br/></td>
<td><span data-ttu-id="f3fe0-315">Valor booleano <strong>true</strong> .</span><span class="sxs-lookup"><span data-stu-id="f3fe0-315">The <strong>TRUE</strong> Boolean value.</span></span><br/> <span data-ttu-id="f3fe0-316">Valor booleano <strong>falso</strong> .</span><span class="sxs-lookup"><span data-stu-id="f3fe0-316">The <strong>FALSE</strong> Boolean value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-317">[]</span><span class="sxs-lookup"><span data-stu-id="f3fe0-317">[]</span></span></td>
<td><span data-ttu-id="f3fe0-318">System. Keywords: = []</span><span class="sxs-lookup"><span data-stu-id="f3fe0-318">System.Keywords:=[]</span></span><br/></td>
<td><span data-ttu-id="f3fe0-319">Los corchetes vacíos indican que no hay ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-319">Empty square brackets denote that there is no value.</span></span> <span data-ttu-id="f3fe0-320">Este ejemplo busca todos los elementos que no se han etiquetado.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-320">This example finds all items that have not been tagged.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-321">Fechas absolutas</span><span class="sxs-lookup"><span data-stu-id="f3fe0-321">Absolute dates</span></span></td>
<td><span data-ttu-id="f3fe0-322">System. ItemDate: 1/26/2010</span><span class="sxs-lookup"><span data-stu-id="f3fe0-322">System.ItemDate:1/26/2010</span></span><br/> <span data-ttu-id="f3fe0-323">SystemDateModified 10/15/2002 19:00</span><span class="sxs-lookup"><span data-stu-id="f3fe0-323">SystemDateModified 10/15/2002 19:00</span></span><br/></td>
<td><span data-ttu-id="f3fe0-324">Busca elementos con una fecha del 26 de enero de 2010.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-324">Finds items with a date of 26 January 2010.</span></span><br/> <span data-ttu-id="f3fe0-325">Busca los elementos que se modificaron el 15 de octubre de 2002 entre las horas 19:00:00 y 19:00:59.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-325">Finds items that were modified on 15 October 2002 between the hours 19:00:00 and 19:00:59.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3fe0-326">Dado que los formatos de fecha (como los formatos de punto flotante) varían entre las configuraciones regionales, no se admite el uso de sintaxis canónica con fechas absolutas y no es seguro para la localización.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-326">Because date formats (like floating point formats) vary among locales, the use of canonical syntax with absolute dates is not supported and is not localization safe.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fe0-327">Fechas relativas</span><span class="sxs-lookup"><span data-stu-id="f3fe0-327">Relative dates</span></span></td>
<td><span data-ttu-id="f3fe0-328">System. ItemDate: System. StructuredQueryType. DateTime # Today</span><span class="sxs-lookup"><span data-stu-id="f3fe0-328">System.ItemDate:System.StructuredQueryType.DateTime#Today</span></span><br/> <span data-ttu-id="f3fe0-329">System. DateAcquired: System. StructuredQueryType. DateTime # NextMonth</span><span class="sxs-lookup"><span data-stu-id="f3fe0-329">System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth</span></span><br/> <span data-ttu-id="f3fe0-330">System. Message. DateReceived: System. StructuredQueryType. DateTime # LastYear</span><span class="sxs-lookup"><span data-stu-id="f3fe0-330">System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear</span></span><br/></td>
<td><span data-ttu-id="f3fe0-331">Busca elementos con la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-331">Finds items with today's date.</span></span><br/> <span data-ttu-id="f3fe0-332">Busca elementos con una fecha en el mes siguiente.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-332">Finds items with a date in the next month.</span></span><br/> <span data-ttu-id="f3fe0-333">Busca elementos con una fecha en el último año.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-333">Finds items with a date in the last year.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3fe0-334">Además de buscar en fechas y intervalos de fechas específicos, AQS reconoce los valores de fecha relativos (como <em>hoy</em>, <em>mañana</em>, <em>nextweek</em>, <em>Nextmonth</em>) y Day (como el <em>martes</em> o el lunes). <em> Miércoles</em>) y mes (<em>febrero</em>).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-334">In addition to searching on specific dates and date ranges, AQS recognizes relative date values (like <em>today</em>, <em>tomorrow</em>, <em>nextweek</em>, <em>nextmonth</em>), and day (like <em>Tuesday</em> or <em>Monday..Wednesday</em>), and month (<em>February</em>).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fe0-335">..</span><span class="sxs-lookup"><span data-stu-id="f3fe0-335">..</span></span></td>
<td><span data-ttu-id="f3fe0-336">System. ItemDate: 11/05/04.. 11/10/04 System. Size: 5 KB.. 10 KB</span><span class="sxs-lookup"><span data-stu-id="f3fe0-336">System.ItemDate:11/05/04..11/10/04 System.Size:5kb..10kb</span></span><br/></td>
<td><span data-ttu-id="f3fe0-337">Los puntos dobles indican un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-337">Double periods indicate a value range.</span></span> <span data-ttu-id="f3fe0-338">Busca elementos con una fecha comprendida entre 11/05/04 y 11/10/04, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-338">Finds items with a date between 11/05/04 and 11/10/04, inclusive.</span></span><br/> <span data-ttu-id="f3fe0-339">Busca elementos entre 5 y 10 KB de tamaño.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-339">Finds items between 5 and 10kb in size.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a><span data-ttu-id="f3fe0-340">Restricciones de ámbito</span><span class="sxs-lookup"><span data-stu-id="f3fe0-340">Scope Restrictions</span></span>

<span data-ttu-id="f3fe0-341">Los usuarios pueden limitar el ámbito de las búsquedas a ubicaciones de carpeta o almacenes de datos específicos.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-341">Users can limit the scope of their searches to specific folder locations or data stores.</span></span> <span data-ttu-id="f3fe0-342">Por ejemplo, si utiliza varias cuentas de correo electrónico y desea limitar una consulta a Microsoft Outlook o Microsoft Outlook Express, puede utilizar `System.Search.Store:mapi` o `System.Search.Store:oe` respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-342">For example, if you use several email accounts and you want to limit a query to either Microsoft Outlook or Microsoft Outlook Express, you can use `System.Search.Store:mapi` or `System.Search.Store:oe` respectively.</span></span> <span data-ttu-id="f3fe0-343">En la tabla siguiente se muestran algunos ejemplos de cómo restringir una búsqueda por almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-343">The following table shows some examples of how to restrict a search by data store.</span></span>



| <span data-ttu-id="f3fe0-344">Restricción de búsqueda por almacén de datos</span><span class="sxs-lookup"><span data-stu-id="f3fe0-344">Restrict search by data store</span></span>  | <span data-ttu-id="f3fe0-345">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="f3fe0-345">Keyword</span></span> | <span data-ttu-id="f3fe0-346">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3fe0-346">Example</span></span>                                     |
|--------------------------------|---------|---------------------------------------------|
| <span data-ttu-id="f3fe0-347">Archivos</span><span class="sxs-lookup"><span data-stu-id="f3fe0-347">Files</span></span>                          | <span data-ttu-id="f3fe0-348">archivo</span><span class="sxs-lookup"><span data-stu-id="f3fe0-348">file</span></span>    | <span data-ttu-id="f3fe0-349">System. Search. Store: archivo</span><span class="sxs-lookup"><span data-stu-id="f3fe0-349">System.Search.Store:file</span></span>                    |
| <span data-ttu-id="f3fe0-350">Outlook</span><span class="sxs-lookup"><span data-stu-id="f3fe0-350">Outlook</span></span>                        | <span data-ttu-id="f3fe0-351">interfaz</span><span class="sxs-lookup"><span data-stu-id="f3fe0-351">mapi</span></span>    | <span data-ttu-id="f3fe0-352">System. Search. Store: MAPI</span><span class="sxs-lookup"><span data-stu-id="f3fe0-352">System.Search.Store:mapi</span></span>                    |
| <span data-ttu-id="f3fe0-353">Outlook Express</span><span class="sxs-lookup"><span data-stu-id="f3fe0-353">Outlook Express</span></span>                | <span data-ttu-id="f3fe0-354">oe</span><span class="sxs-lookup"><span data-stu-id="f3fe0-354">oe</span></span>      | <span data-ttu-id="f3fe0-355">System. Search. Store: OE</span><span class="sxs-lookup"><span data-stu-id="f3fe0-355">System.Search.Store:oe</span></span>                      |
| <span data-ttu-id="f3fe0-356">Archivos sin conexión</span><span class="sxs-lookup"><span data-stu-id="f3fe0-356">Offline files</span></span>                  | <span data-ttu-id="f3fe0-357">CSC</span><span class="sxs-lookup"><span data-stu-id="f3fe0-357">csc</span></span>     | <span data-ttu-id="f3fe0-358">System. Search. Store: CSC</span><span class="sxs-lookup"><span data-stu-id="f3fe0-358">System.Search.Store:csc</span></span>                     |
| <span data-ttu-id="f3fe0-359">Carpeta específica en la unidad local</span><span class="sxs-lookup"><span data-stu-id="f3fe0-359">Specific folder on local drive</span></span> | <span data-ttu-id="f3fe0-360">folder</span><span class="sxs-lookup"><span data-stu-id="f3fe0-360">folder</span></span>  | <span data-ttu-id="f3fe0-361">System. ItemFolderNameDisplay: C: " \\ carpeta"</span><span class="sxs-lookup"><span data-stu-id="f3fe0-361">System.ItemFolderNameDisplay:C:"\\MyFolder"</span></span> |



 

## <a name="additional-resources"></a><span data-ttu-id="f3fe0-362">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f3fe0-362">Additional Resources</span></span>

-   <span data-ttu-id="f3fe0-363">En Windows 7 y versiones posteriores, una opción de menú contextual puede estar disponible en función de si se cumple una condición de AQS.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-363">In Windows 7 and later, a shortcut menu option can be available based on whether an AQS condition is met.</span></span> <span data-ttu-id="f3fe0-364">Para obtener más información, vea "obtener el comportamiento dinámico para verbos estáticos mediante la sintaxis de consulta avanzada" en [crear controladores de menú contextuales](../shell/context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-364">For more information, see "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" in [Creating Context Menu Handlers](../shell/context-menu-handlers.md).</span></span>
-   <span data-ttu-id="f3fe0-365">Las consultas AQS se pueden limitar a tipos específicos de archivos, que se conocen como tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f3fe0-365">AQS queries can be limited to specific types of files, which are known as file kinds.</span></span> <span data-ttu-id="f3fe0-366">Para obtener más información, vea [tipos de archivo y asociaciones](../shell/fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-366">For more information, see [File Types and Associations](../shell/fa-intro.md).</span></span> <span data-ttu-id="f3fe0-367">Para obtener documentación de referencia de propiedades, vea [System. Kind](../properties/props-system-kind.md)y [System. KindText](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="f3fe0-367">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3fe0-368">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3fe0-368">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3fe0-369">Consulta del índice mediante programación</span><span class="sxs-lookup"><span data-stu-id="f3fe0-369">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="f3fe0-370">Uso de enfoques de SQL y AQS para consultar el índice</span><span class="sxs-lookup"><span data-stu-id="f3fe0-370">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="f3fe0-371">Consultar el índice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="f3fe0-371">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="f3fe0-372">Consultar el índice con el protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="f3fe0-372">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="f3fe0-373">Consultar el índice con la sintaxis SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="f3fe0-373">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 

---
title: Definiciones de tipos, declaraciones de construcción e importaciones
description: Las definiciones de tipo, las declaraciones de construcción y las importaciones se pueden producir fuera del cuerpo de la interfaz.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- interfaces MIDL, definiciones de tipo
- interfaces MIDL, declaraciones de construcción
- interfaces MIDL, importaciones
- definiciones de tipos MIDL
- declaraciones de construcción MIDL
- importa MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665615"
---
# <a name="type-definitions-construct-declarations-and-imports"></a><span data-ttu-id="922f2-109">Definiciones de tipos, declaraciones de construcción e importaciones</span><span class="sxs-lookup"><span data-stu-id="922f2-109">Type Definitions, Construct Declarations, and Imports</span></span>

<span data-ttu-id="922f2-110">Las definiciones de tipo, las declaraciones de construcción y las importaciones se pueden producir fuera del cuerpo de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="922f2-110">Type definitions, construct declarations, and imports can occur outside of the interface body.</span></span> <span data-ttu-id="922f2-111">Todas las definiciones del archivo IDL principal aparecerán en el archivo de encabezado generado y todos los procedimientos de todas las interfaces en el archivo IDL principal generarán rutinas de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="922f2-111">All definitions from the main IDL file will appear in the generated header file, and all the procedures from all the interfaces in the main IDL file will generate stub routines.</span></span> <span data-ttu-id="922f2-112">Esto permite a las aplicaciones que admiten varias interfaces combinar archivos IDL en un único archivo IDL combinado.</span><span class="sxs-lookup"><span data-stu-id="922f2-112">This enables applications that support multiple interfaces to merge IDL files into a single, combined IDL file.</span></span>

<span data-ttu-id="922f2-113">Como resultado, requiere menos tiempo para compilar los archivos y también permite que MIDL reduzca las redundancias en el código auxiliar generado.</span><span class="sxs-lookup"><span data-stu-id="922f2-113">As a result, it requires less time to compile the files and also allows MIDL to reduce redundancies in the generated stubs.</span></span> <span data-ttu-id="922f2-114">Esto puede mejorar significativamente las interfaces de [**objeto**](object.md) a través de la capacidad de compartir código común para las interfaces base y las interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="922f2-114">This can significantly improve [**object**](object.md) interfaces through the ability to share common code for base interfaces and derived interfaces.</span></span> <span data-ttu-id="922f2-115">En el caso de las interfaces que no son de **objeto** , los nombres de procedimiento deben ser únicos en todas las interfaces.</span><span class="sxs-lookup"><span data-stu-id="922f2-115">For non- **object** interfaces, the procedure names must be unique across all the interfaces.</span></span> <span data-ttu-id="922f2-116">En el caso de las interfaces de **objeto** , los nombres de procedimiento deben ser únicos solo dentro de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="922f2-116">For **object** interfaces, the procedure names need to be unique only within an interface.</span></span> <span data-ttu-id="922f2-117">Tenga en cuenta que no se permiten varias interfaces cuando se usa el modificador [**/OSF**](-osf.md)</span><span class="sxs-lookup"><span data-stu-id="922f2-117">Note that multiple interfaces are not permitted when you use the [**/osf**](-osf.md) switch.</span></span>

## <a name="declarative-constructs"></a><span data-ttu-id="922f2-118">Construcciones declarativas</span><span class="sxs-lookup"><span data-stu-id="922f2-118">Declarative Constructs</span></span>

<span data-ttu-id="922f2-119">La sintaxis de las construcciones declarativas en el archivo IDL es similar a la de C. MIDL es compatible con todas las construcciones declarativas de C/C++ de Microsoft, excepto las siguientes:</span><span class="sxs-lookup"><span data-stu-id="922f2-119">The syntax for declarative constructs in the IDL file is similar to that for C. MIDL supports all Microsoft C/C++ declarative constructs except the following:</span></span>

-   <span data-ttu-id="922f2-120">Declaradores de estilo más antiguos que permiten especificar un declarador sin un especificador de tipo, como:</span><span class="sxs-lookup"><span data-stu-id="922f2-120">Older style declarators that allow a declarator to be specified without a type specifier, such as:</span></span>

    ``` syntax
    x (y) 
    short x (y)
    ```

-   <span data-ttu-id="922f2-121">Declaraciones con inicializadores (MIDL solo acepta declaraciones que se ajusten a la sintaxis de MIDL [**const**](const.md) ).</span><span class="sxs-lookup"><span data-stu-id="922f2-121">Declarations with initializers (MIDL only accepts declarations that conform to the MIDL [**const**](const.md) syntax).</span></span>

<span data-ttu-id="922f2-122">La palabra clave [**Import**](import.md) especifica los nombres de uno o varios archivos IDL que se van a importar.</span><span class="sxs-lookup"><span data-stu-id="922f2-122">The [**import**](import.md) keyword specifies the names of one or more IDL files to import.</span></span> <span data-ttu-id="922f2-123">La Directiva de importación es similar a la directiva [**include**](include.md) de C, salvo que solo los tipos de datos se asimilan al archivo IDL de importación.</span><span class="sxs-lookup"><span data-stu-id="922f2-123">The import directive is similar to the C [**include**](include.md) directive, except that only data types are assimilated into the importing IDL file.</span></span>

## <a name="constant-declaration"></a><span data-ttu-id="922f2-124">Declaración de constantes</span><span class="sxs-lookup"><span data-stu-id="922f2-124">Constant Declaration</span></span>

<span data-ttu-id="922f2-125">La declaración de constante especifica constantes de [**tipo booleano**](boolean.md), entero, carácter, caracteres anchos, cadenas y **void \*** .</span><span class="sxs-lookup"><span data-stu-id="922f2-125">The constant declaration specifies [**Boolean**](boolean.md), integer, character, wide-character, string, and **void \*** constants.</span></span> <span data-ttu-id="922f2-126">Para obtener más información, vea [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="922f2-126">For more information, see [**const**](const.md).</span></span>

## <a name="general-declaration"></a><span data-ttu-id="922f2-127">Declaración general</span><span class="sxs-lookup"><span data-stu-id="922f2-127">General Declaration</span></span>

<span data-ttu-id="922f2-128">Una declaración general es similar a la instrucción [**typedef**](typedef.md) de C con la adición de atributos de tipo IDL.</span><span class="sxs-lookup"><span data-stu-id="922f2-128">A general declaration is similar to the C [**typedef**](typedef.md) statement with the addition of IDL type attributes.</span></span> <span data-ttu-id="922f2-129">Excepto en el modo [**/OSF**](-osf.md) , el compilador MIDL también permite una declaración implícita en forma de definición de variable.</span><span class="sxs-lookup"><span data-stu-id="922f2-129">Except in [**/osf**](-osf.md) mode, the MIDL compiler also allows an implicit declaration in the form of a variable definition.</span></span>

## <a name="function-declaration"></a><span data-ttu-id="922f2-130">Declaración de función</span><span class="sxs-lookup"><span data-stu-id="922f2-130">Function Declaration</span></span>

<span data-ttu-id="922f2-131">El declarador de función es un caso especial de la declaración general.</span><span class="sxs-lookup"><span data-stu-id="922f2-131">The function declarator is a special case of the general declaration.</span></span> <span data-ttu-id="922f2-132">Puede usar atributos IDL para especificar el comportamiento del tipo de valor devuelto de la función y de cada uno de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="922f2-132">You can use IDL attributes to specify the behavior of the function return type and each of the parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="922f2-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="922f2-133">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 





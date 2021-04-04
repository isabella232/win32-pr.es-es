---
title: Diferencias entre MIDL y MkTypLib
description: Diferencias entre MIDL y MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL y ODL MIDL, diferencias entre MIDL y MkTypLib
- MkTypLib (MIDL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076363"
---
# <a name="differences-between-midl-and-mktyplib"></a><span data-ttu-id="41b79-105">Diferencias entre MIDL y MkTypLib</span><span class="sxs-lookup"><span data-stu-id="41b79-105">Differences Between MIDL and MkTypLib</span></span>

> [!Note]  
> <span data-ttu-id="41b79-106">La herramienta Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="41b79-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="41b79-107">En su lugar, utilice el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="41b79-107">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="41b79-108">Existen algunas áreas clave en las que el compilador MIDL difiere de MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="41b79-108">There are a few key areas in which the MIDL compiler differs from MkTypLib.</span></span> <span data-ttu-id="41b79-109">La mayoría de estas diferencias surgen porque MIDL está orientado más hacia la sintaxis de C que a MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="41b79-109">Most of these differences arise because MIDL is oriented more toward C-syntax than MkTypLib.</span></span>

<span data-ttu-id="41b79-110">En general, querrá usar la sintaxis de MIDL en los archivos IDL.</span><span class="sxs-lookup"><span data-stu-id="41b79-110">In general, you will want to use the MIDL syntax in your IDL files.</span></span> <span data-ttu-id="41b79-111">Sin embargo, si necesita compilar un archivo ODL existente o mantener la compatibilidad con MkTypLib, use la opción del compilador de MIDL [**/mktyplib203**](-mktyplib203.md) para forzar que MIDL se comporte como Mkktyplib.exe, versión 2,03.</span><span class="sxs-lookup"><span data-stu-id="41b79-111">However, if you need to compile an existing ODL file, or otherwise maintain compatibility with MkTypLib, use the [**/mktyplib203**](-mktyplib203.md) MIDL compiler option to force MIDL to behave like Mkktyplib.exe, version 2.03.</span></span> <span data-ttu-id="41b79-112">(Esta es la última versión de la herramienta MkTypLib). En concreto, la opción **/mktyplib203** resuelve estas diferencias:</span><span class="sxs-lookup"><span data-stu-id="41b79-112">(This is the last release of the MkTypLib tool.) Specifically, the **/mktyplib203** option resolves these differences:</span></span>

-   <span data-ttu-id="41b79-113">Sintaxis de TypeDef para tipos de datos complejos</span><span class="sxs-lookup"><span data-stu-id="41b79-113">typedef syntax for complex data types</span></span>

    <span data-ttu-id="41b79-114">En MkTypLib, las dos definiciones siguientes generan un registro TKIND \_ para "This \_ struct" en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="41b79-114">In MkTypLib, both of the following definitions generate a TKIND\_RECORD for "this\_struct" in the type library.</span></span> <span data-ttu-id="41b79-115">La etiqueta "struct \_ Tag" es opcional y, si se utiliza, no se mostrará en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="41b79-115">The tag "struct\_tag" is optional and, if used, will not show up in the type library.</span></span>

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    <span data-ttu-id="41b79-116">Si falta una etiqueta opcional, MIDL la generará, con lo que se agregará una etiqueta a la definición proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="41b79-116">If an optional tag is missing, MIDL will generate it, effectively adding a tag to the definition supplied by the user.</span></span> <span data-ttu-id="41b79-117">Dado que la primera definición tiene una etiqueta, MIDL generará un \_ registro TKIND para "This \_ struct" y un \_ alias TKIND para "This \_ struct" (que define "This \_ struct" como alias para "struct \_ Tag").</span><span class="sxs-lookup"><span data-stu-id="41b79-117">Since the first definition has a tag, MIDL will generate a TKIND\_RECORD for "this\_struct" and a TKIND\_ALIAS for "this\_struct" (defining "this\_struct" as an alias for "struct\_tag").</span></span> <span data-ttu-id="41b79-118">Dado que la etiqueta falta en la segunda definición, MIDL generará un \_ registro TKIND para un nombre alterado, interno a MIDL, que no es significativo para el usuario y un \_ alias TKIND para "ese \_ struct".</span><span class="sxs-lookup"><span data-stu-id="41b79-118">Because the tag is missing in the second definition, MIDL will generate a TKIND\_RECORD for a mangled name, internal to MIDL, that is not meaningful to the user and a TKIND\_ALIAS for "that\_struct".</span></span>

    <span data-ttu-id="41b79-119">Esto tiene implicaciones potenciales para los exploradores de biblioteca de tipos que simplemente muestran el nombre de un registro en su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="41b79-119">This has potential implications for type library browsers that simply show the name of a record in their user interface.</span></span> <span data-ttu-id="41b79-120">Si espera que un \_ registro TKIND tenga un nombre real, los nombres irreconocibles podrían aparecer en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="41b79-120">If you expect a TKIND\_RECORD to have a real name, unrecognizable names could appear in the user interface.</span></span> <span data-ttu-id="41b79-121">Este comportamiento también se aplica a las definiciones de [**Unión**](union.md) y [**enumeración**](enum.md) , con el compilador MIDL que genera TKIND \_ uniones y TKIND \_ enumeraciones, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="41b79-121">This behavior also applies to [**union**](union.md) and [**enum**](enum.md) definitions, with the MIDL compiler generating TKIND\_UNIONs and TKIND\_ENUMs, respectively.</span></span>

    <span data-ttu-id="41b79-122">MIDL también permite definiciones de [**struct**](struct.md), [**Union**](union.md)y [**enum**](enum.md) de estilo C.</span><span class="sxs-lookup"><span data-stu-id="41b79-122">MIDL also allows C-style [**struct**](struct.md), [**union**](union.md), and [**enum**](enum.md) definitions.</span></span> <span data-ttu-id="41b79-123">Por ejemplo, la siguiente definición es válida en MIDL:</span><span class="sxs-lookup"><span data-stu-id="41b79-123">For example, the following definition is legal in MIDL:</span></span>

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   <span data-ttu-id="41b79-124">tipos de datos booleanos</span><span class="sxs-lookup"><span data-stu-id="41b79-124">Boolean data types</span></span>

    <span data-ttu-id="41b79-125">En MkTypLib, el tipo base [**booleano**](boolean.md) y el tipo de datos MkTypLib bool equivalen a VT \_ bool, que se asigna a la variante \_ bool y que se define como un valor [**Short**](short.md).</span><span class="sxs-lookup"><span data-stu-id="41b79-125">In MkTypLib, the [**Boolean**](boolean.md) base type and the MkTypLib data type BOOL equate to VT\_BOOL, which maps to VARIANT\_BOOL, and which is defined as a [**short**](short.md).</span></span> <span data-ttu-id="41b79-126">En MIDL, el tipo base **booleano** es equivalente a VT \_ UI1, que se define como un [**carácter sin signo**](unsigned.md)y el tipo de datos bool se define como un [**valor Long**](long.md).</span><span class="sxs-lookup"><span data-stu-id="41b79-126">In MIDL, the **Boolean** base type is equivalent to VT\_UI1, which is defined as an [**unsigned char**](unsigned.md), and the BOOL data type is defined as a [**long**](long.md).</span></span> <span data-ttu-id="41b79-127">Esto conduce a dificultades si se mezcla la sintaxis IDL y la sintaxis ODL en el mismo archivo mientras se sigue intentando mantener la compatibilidad con MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="41b79-127">This leads to difficulties if you mix IDL syntax and ODL syntax in the same file while still trying to maintain compatibility with MkTypLib.</span></span> <span data-ttu-id="41b79-128">Dado que los tipos de datos tienen tamaños diferentes, el código de serialización no coincidirá con lo que se describe en la información de tipo.</span><span class="sxs-lookup"><span data-stu-id="41b79-128">Because the data types are different sizes, the marshaling code will not match what is described in the type information.</span></span> <span data-ttu-id="41b79-129">Si desea un VT \_ bool en la biblioteca de tipos, debe usar el tipo de \_ datos Variant bool.</span><span class="sxs-lookup"><span data-stu-id="41b79-129">If you want a VT\_BOOL in your type library, you should use the VARIANT\_BOOL data type.</span></span>

-   <span data-ttu-id="41b79-130">Definiciones de GUID en archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="41b79-130">GUID definitions in header files</span></span>

    <span data-ttu-id="41b79-131">En MkTypLib, los GUID se definen en el archivo de encabezado con una macro que se puede compilar condicionalmente para generar una predefinición de GUID o un GUID con instancias.</span><span class="sxs-lookup"><span data-stu-id="41b79-131">In MkTypLib, GUIDs are defined in the header file with a macro that can be conditionally compiled to generate either a GUID predefinition or an instantiated GUID.</span></span> <span data-ttu-id="41b79-132">MIDL normalmente coloca las predefiniciones de GUID en los archivos de encabezado generados y las instancias GUID solo en el archivo generado por el modificador [**/IID**](-iid.md)</span><span class="sxs-lookup"><span data-stu-id="41b79-132">MIDL normally puts GUID predefinitions in its generated header files and GUID instantiations only in the file generated by the [**/iid**](-iid.md) switch.</span></span>

<span data-ttu-id="41b79-133">Las siguientes diferencias de comportamiento no se pueden resolver mediante el modificador [**/mktyplib203**](-mktyplib203.md) :</span><span class="sxs-lookup"><span data-stu-id="41b79-133">The following differences in behavior cannot be resolved by using the [**/mktyplib203**](-mktyplib203.md) switch:</span></span>

-   <span data-ttu-id="41b79-134">Distinción entre mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="41b79-134">Case sensitivity</span></span>

    <span data-ttu-id="41b79-135">MIDL distingue mayúsculas de minúsculas, la automatización OLE no lo es.</span><span class="sxs-lookup"><span data-stu-id="41b79-135">MIDL is case sensitive, OLE Automation is not.</span></span>

-   <span data-ttu-id="41b79-136">Ámbito de los símbolos en una declaración de enumeración</span><span class="sxs-lookup"><span data-stu-id="41b79-136">Scope of symbols in an enum declaration</span></span>

    <span data-ttu-id="41b79-137">En MkTypLib, el ámbito de los símbolos de una enumeración es local.</span><span class="sxs-lookup"><span data-stu-id="41b79-137">In MkTypLib the scope of symbols in an enum is local.</span></span> <span data-ttu-id="41b79-138">En MIDL, el ámbito de los símbolos en una enumeración es global, como en C. Por ejemplo, el siguiente código se compilará en MkTypLib, pero generará un error de nombre duplicado en MIDL:</span><span class="sxs-lookup"><span data-stu-id="41b79-138">In MIDL, the scope of symbols in an enum is global, as it is in C. For example, the following code will compile in MkTypLib, but will generate a duplicate name error in MIDL:</span></span>

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   <span data-ttu-id="41b79-139">Ámbito de atributo público</span><span class="sxs-lookup"><span data-stu-id="41b79-139">Scope of public attribute</span></span>

    <span data-ttu-id="41b79-140">Si aplica el atributo [**público**](public.md) a un bloque de interfaz, MkTypLib trata cada typedef dentro de ese bloque de interfaz como público.</span><span class="sxs-lookup"><span data-stu-id="41b79-140">If you apply the [**public**](public.md) attribute to an interface block, MkTypLib treats every typedef inside that interface block as public.</span></span> <span data-ttu-id="41b79-141">MIDL requiere que aplique explícitamente el atributo **público** a las definiciones de usuario que desee que sean públicas.</span><span class="sxs-lookup"><span data-stu-id="41b79-141">MIDL requires that you explicitly apply the **public** attribute to those typedefs that you want public.</span></span>

-   <span data-ttu-id="41b79-142">Orden de búsqueda de importlib</span><span class="sxs-lookup"><span data-stu-id="41b79-142">Importlib search order</span></span>

    <span data-ttu-id="41b79-143">Si importa más de una biblioteca de tipos y estas bibliotecas contienen referencias duplicadas, MkTypLib la resuelve con la primera referencia que encuentre.</span><span class="sxs-lookup"><span data-stu-id="41b79-143">If you import more than one type library, and if these libraries contain duplicate references, MkTypLib resolves this by using the first reference that it finds.</span></span> <span data-ttu-id="41b79-144">MIDL usará la última referencia que encuentre.</span><span class="sxs-lookup"><span data-stu-id="41b79-144">MIDL will use the last reference that it finds.</span></span> <span data-ttu-id="41b79-145">Por ejemplo, dada la siguiente sintaxis de ODL, la biblioteca C usará la definición de tipo MOO de la biblioteca A si se compila con MkTypLib y la definición de tipo MOO de la biblioteca B Si se compila con MIDL:</span><span class="sxs-lookup"><span data-stu-id="41b79-145">For example, given the following ODL syntax, library C will use the MOO typedef from library A if you compile with MkTypLib, and the MOO typedef from library B if you compile with MIDL:</span></span>

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    <span data-ttu-id="41b79-146">La solución adecuada para esto es calificar cada referencia con el nombre de la biblioteca de importación correcto, de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="41b79-146">The appropriate workaround for this is to qualify each such reference with the correct import library name, like this:</span></span>

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   <span data-ttu-id="41b79-147">No se reconoce el tipo de datos VOID</span><span class="sxs-lookup"><span data-stu-id="41b79-147">VOID data type not recognized</span></span>

    <span data-ttu-id="41b79-148">MIDL reconoce el tipo de datos [**void**](void.md) del lenguaje C y no reconoce el tipo de datos void de OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="41b79-148">MIDL recognizes the C-language [**void**](void.md) data type and does not recognize the OLE Automation VOID data type.</span></span> <span data-ttu-id="41b79-149">Si tiene un archivo ODL que usa VOID, coloque esta definición en la parte superior del archivo:</span><span class="sxs-lookup"><span data-stu-id="41b79-149">If you have an ODL file that uses VOID, place this definition at the top of the file:</span></span>

    ``` syntax
#define VOID void
    ```

-   <span data-ttu-id="41b79-150">Notación exponencial</span><span class="sxs-lookup"><span data-stu-id="41b79-150">Exponential notation</span></span>

    <span data-ttu-id="41b79-151">MIDL requiere que los valores expresados en la notación exponencial estén incluidos entre comillas.</span><span class="sxs-lookup"><span data-stu-id="41b79-151">MIDL requires that values expressed in exponential notation be contained within quotation marks.</span></span> <span data-ttu-id="41b79-152">Por ejemplo, "-2.5 E + 3"</span><span class="sxs-lookup"><span data-stu-id="41b79-152">For example, "-2.5E+3"</span></span>

-   <span data-ttu-id="41b79-153">Constantes y valores de LCID</span><span class="sxs-lookup"><span data-stu-id="41b79-153">LCID values and constants</span></span>

    <span data-ttu-id="41b79-154">Normalmente, MIDL no tiene en cuenta el LCID al analizar archivos.</span><span class="sxs-lookup"><span data-stu-id="41b79-154">Normally MIDL does not consider the LCID when parsing files.</span></span> <span data-ttu-id="41b79-155">Para forzar este comportamiento para un valor, o si necesita usar la notación específica de la configuración regional al definir una constante, incluya el valor o la constante entre comillas.</span><span class="sxs-lookup"><span data-stu-id="41b79-155">To force this behavior for a value, or if you need to use locale-specific notation when defining a constant, enclose the value or constant in quotation marks.</span></span>

<span data-ttu-id="41b79-156">Para obtener más información, vea [**/mktyplib203**](-mktyplib203.md), [**/IID**](-iid.md)y [serialización de tipos de datos OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="41b79-156">For more information, see [**/mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md), and [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 





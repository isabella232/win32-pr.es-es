---
title: Trabajar con definiciones en archivos IDL
description: En esta página se describe por qué los símbolos definidos con \ define desaparecen del compilador MIDL y archivos H generados y lo que se puede hacer al respecto. Esta explicación se aplica a todos los archivos procesados por MIDL, como los archivos \. idl, \. ACF, \. h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL del compilador MIDL, tratar con define
- define MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075678"
---
# <a name="dealing-with-defines-in-idl-files"></a><span data-ttu-id="6a444-106">Trabajar con \# definiciones en archivos IDL</span><span class="sxs-lookup"><span data-stu-id="6a444-106">Dealing with \#defines in IDL Files</span></span>

<span data-ttu-id="6a444-107">En esta página se describe por qué los símbolos definidos con una **\# definición** desaparecen del compilador MIDL archivos H generados y lo que se puede hacer al respecto.</span><span class="sxs-lookup"><span data-stu-id="6a444-107">This page describes why symbols defined with a **\#define** disappear from the MIDL compiler generated H files, and what can be done about it.</span></span> <span data-ttu-id="6a444-108">Esta explicación se aplica a todos los archivos procesados por MIDL, como \* archivos. idl, \* . ACF y \* . h.</span><span class="sxs-lookup"><span data-stu-id="6a444-108">This explanation applies to any files processed by MIDL, such as \*.idl, \*.acf, \*.h files.</span></span>

<span data-ttu-id="6a444-109">La desaparición de símbolos de **\# definición** es el resultado de que MIDL delegue el preprocesamiento de los archivos de entrada a un preprocesador.</span><span class="sxs-lookup"><span data-stu-id="6a444-109">The disappearance of **\#define** symbols is a result of MIDL delegating the preprocessing of input files to a preprocessor.</span></span> <span data-ttu-id="6a444-110">De forma predeterminada, el preprocesador es un preprocesador de C/C++ del entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="6a444-110">By default, the preprocessor is a C/C++ preprocessor from the build environment.</span></span> <span data-ttu-id="6a444-111">Después del preprocesamiento, el flujo de entrada MIDL recibe solo las \# directivas de preprocesador de línea.</span><span class="sxs-lookup"><span data-stu-id="6a444-111">After preprocessing, the input stream MIDL receives has only \#line preprocessor directives.</span></span> <span data-ttu-id="6a444-112">En concreto, el preprocesador revierte todas las definiciones de macro en los archivos de entrada y, por consiguiente, MIDL no puede detectar su presencia.</span><span class="sxs-lookup"><span data-stu-id="6a444-112">In particular, the preprocessor unrolls all macro definitions in input files, and therefore, MIDL cannot detect their presence.</span></span> <span data-ttu-id="6a444-113">Por consiguiente, cuando MIDL Replica definiciones de tipo de un archivo de entrada en el archivo H generado, las definiciones \# no se replican.</span><span class="sxs-lookup"><span data-stu-id="6a444-113">Consequently, when MIDL replicates type definitions from an input file to the generated H file, the \#defines are not replicated.</span></span> <span data-ttu-id="6a444-114">Por lo tanto, no use \# define directamente en archivos IDL si se van a utilizar más adelante desde el archivo H generado.</span><span class="sxs-lookup"><span data-stu-id="6a444-114">Therefore, do not use \#defines directly in IDL files if they are to be used later from the generated H file.</span></span>

<span data-ttu-id="6a444-115">Se recomiendan las cuatro soluciones alternativas siguientes:</span><span class="sxs-lookup"><span data-stu-id="6a444-115">The following four workarounds are recommended:</span></span>

-   <span data-ttu-id="6a444-116">Use la especificación de declaración [**const**](const.md) .</span><span class="sxs-lookup"><span data-stu-id="6a444-116">Use the [**const**](const.md) declaration specification.</span></span>
-   <span data-ttu-id="6a444-117">Use archivos de encabezado independientes que se importen o incluyan en el archivo IDL y que se incluyan más adelante en el código fuente de C.</span><span class="sxs-lookup"><span data-stu-id="6a444-117">Use separate header files that are imported or included in the IDL file, and later included in the C-source code.</span></span>
-   <span data-ttu-id="6a444-118">Use constantes de enumeración en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="6a444-118">Use enumeration constants in the IDL file.</span></span>
-   <span data-ttu-id="6a444-119">Use [**CPP \_ Quote**](cpp-quote.md) para reproducir la **\# definición** en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="6a444-119">Use [**cpp\_quote**](cpp-quote.md) to reproduce **\#define** in the generated header file.</span></span>

<span data-ttu-id="6a444-120">Puede reproducir constantes de manifiesto mediante la **Sintaxis de declaración de constantes de IDL**.</span><span class="sxs-lookup"><span data-stu-id="6a444-120">You can reproduce manifest constants using the **IDL constant-declaration syntax**.</span></span> <span data-ttu-id="6a444-121">Tenga en cuenta que [**const**](const.md) en la declaración de constante IDL es diferente de la semántica de C/C++ **const** y simplemente presenta una constante con nombre para una compilación de IDL.</span><span class="sxs-lookup"><span data-stu-id="6a444-121">Note that the [**const**](const.md) in the IDL constant-declaration is different from C/C++ **const** semantics, and simply introduces a named constant for an IDL compilation.</span></span> <span data-ttu-id="6a444-122">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6a444-122">For example:</span></span>

``` syntax
const short ARRSIZE = 10
```

<span data-ttu-id="6a444-123">Este ejemplo especifica que **ARRSIZE** es una constante con un valor de 10.</span><span class="sxs-lookup"><span data-stu-id="6a444-123">This example specifies that **ARRSIZE** is a constant with a value of 10.</span></span> <span data-ttu-id="6a444-124">Las constantes con nombre se pueden usar en declaradores de matriz IDL y en otros lugares donde un programador de C usaría un manifiesto definido.</span><span class="sxs-lookup"><span data-stu-id="6a444-124">Named constants can be used in IDL array declarators and other places where a C programmer would use a manifest defines.</span></span> <span data-ttu-id="6a444-125">Además, esta sintaxis da como resultado la generación de la siguiente línea en el archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6a444-125">In addition, this syntax results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

<span data-ttu-id="6a444-126">Otra manera de controlar las **\#** instrucciones de definición consiste en empaquetarlas en un archivo de encabezado independiente, ya sea en un archivo dedicado a **\#** definir instrucciones o en un archivo que contenga solo definiciones de tipo.</span><span class="sxs-lookup"><span data-stu-id="6a444-126">Another way to handle **\#** define statements is to package them in a separate header file, either into a file devoted to **\#** define statements or into a file that contains only type definitions.</span></span> <span data-ttu-id="6a444-127">Un archivo que contenga solo directivas de preprocesador puede incluirse de forma segura en el archivo IDL y en los archivos de código fuente de C.</span><span class="sxs-lookup"><span data-stu-id="6a444-127">A file that contains only preprocessor directives may be safely included both by the IDL file and the C-source files.</span></span> <span data-ttu-id="6a444-128">Aunque las directivas no estarán disponibles en el archivo de encabezado generado por el compilador MIDL, el programa de origen C puede incluir el archivo de encabezado independiente.</span><span class="sxs-lookup"><span data-stu-id="6a444-128">Although the directives will not be available in the header file generated by the MIDL compiler, the C-source program can include the separate header file.</span></span> <span data-ttu-id="6a444-129">De forma similar, un archivo de encabezado con **\#** instrucciones de definición y definiciones de tipos regulares se puede importar desde el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="6a444-129">In a similar fashion, a header file with **\#** define statements and regular type definitions can be imported from your IDL file.</span></span> <span data-ttu-id="6a444-130">Este enfoque encapsula las **\#** instrucciones de definición y typedef mediante su uso en un archivo H de modo que los **\#** símbolos de definición no se usan directamente en el archivo IDL de importación.</span><span class="sxs-lookup"><span data-stu-id="6a444-130">This approach encapsulates the **\#** define and typedef statements by using them in an H file such that the **\#** define symbols are not used in the importing IDL file directly.</span></span> <span data-ttu-id="6a444-131">La importación de un archivo de encabezado o IDL a otro archivo IDL impide que las instrucciones typedef se repliquen en el archivo H generado por MIDL (que, a diferencia de las **\#** instrucciones include).</span><span class="sxs-lookup"><span data-stu-id="6a444-131">Importing a header or IDL file to another IDL file prevents the typedef statements from being replicated to the H file generated by MIDL (which is in contrast to **\#** include statements).</span></span> <span data-ttu-id="6a444-132">Este enfoque permite hacer referencia al archivo de encabezado original de forma segura desde el código C a lo largo del archivo H generado sin tener un problema con las definiciones duplicadas.</span><span class="sxs-lookup"><span data-stu-id="6a444-132">This approach allows the original header file to be safely referenced from the C code along the generated H file without having a problem with duplicated definitions.</span></span>

<span data-ttu-id="6a444-133">El uso de constantes de enumeración en el archivo IDL también es eficaz.</span><span class="sxs-lookup"><span data-stu-id="6a444-133">Use of enumeration constants in the IDL file is also effective.</span></span> <span data-ttu-id="6a444-134">Estas constantes se pueden usar en expresiones constantes en IDL, por ejemplo, en declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="6a444-134">These constants can be used in constant expressions in IDL, for example, in array declarators.</span></span> <span data-ttu-id="6a444-135">Las constantes de enumeración no se quitan durante las primeras fases de la compilación de MIDL por parte del preprocesador del compilador de C, por lo que las constantes de enumeración están disponibles en el archivo de encabezado generado por el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="6a444-135">Enumeration constants are not removed during the early phases of MIDL compilation by the C-compiler preprocessor, so enumeration constants are available in the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="6a444-136">Considere la instrucción siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a444-136">Consider the following statement:</span></span>

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

<span data-ttu-id="6a444-137">Esta instrucción no se quitará durante la compilación de MIDL del preprocesador de C y la definición de tipo se replicará en el archivo H generado.</span><span class="sxs-lookup"><span data-stu-id="6a444-137">This statement will not be removed during MIDL compilation by the C preprocessor and the typedef will be replicated to the generated H file.</span></span> <span data-ttu-id="6a444-138">La constante MAXSTRINGCOUNT está disponible para los programas de origen de C que incluyen el archivo de encabezado generado por el compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="6a444-138">The constant MAXSTRINGCOUNT is available to C-source programs that include the header file generated by the MIDL compiler.</span></span>

<span data-ttu-id="6a444-139">Por último, se puede usar la Directiva de [**\_ comillas de CPP**](cpp-quote.md) de MIDL para escribir una cadena arbitraria directamente en el archivo H generado.</span><span class="sxs-lookup"><span data-stu-id="6a444-139">Finally, the [**cpp\_quote**](cpp-quote.md) directive of MIDL can be used to write out an arbitrary string directly into the generated H file.</span></span> <span data-ttu-id="6a444-140">Por ejemplo, para obtener la constante de manifiesto utilizada anteriormente en esta página con la **\_ comilla CPP**, se puede usar la siguiente instrucción:</span><span class="sxs-lookup"><span data-stu-id="6a444-140">For example, to get the manifest constant used previously on this page with **cpp\_quote**, the following statement can be used:</span></span>

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

<span data-ttu-id="6a444-141">Esta instrucción da como resultado la generación de la siguiente línea en el archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6a444-141">This statement results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

 

 





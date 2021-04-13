---
title: Importar archivos y bibliotecas de tipos
description: Las palabras clave de MIDL incluyen, Import y importlib permiten volver a usar el código haciendo referencia a los archivos de encabezado, IDL y lenguaje de definición de objetos (ODL) existentes, y a las bibliotecas de tipos compiladas.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, tareas, importar archivos y bibliotecas de tipos
- importar MIDL
- bibliotecas de tipos MIDL, importar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104362397"
---
# <a name="importing-files-and-type-libraries"></a><span data-ttu-id="ea561-106">Importar archivos y bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="ea561-106">Importing Files and Type Libraries</span></span>

<span data-ttu-id="ea561-107">Las palabras clave de MIDL [**incluyen**](include.md), [**Import**](import.md)y [**importlib**](importlib.md) permiten volver a usar el código haciendo referencia a los archivos de encabezado, IDL y lenguaje de definición de objetos (ODL) existentes, y a las bibliotecas de tipos compiladas.</span><span class="sxs-lookup"><span data-stu-id="ea561-107">The MIDL keywords [**include**](include.md), [**import**](import.md), and [**importlib**](importlib.md) let you reuse code by referencing existing header, IDL, and object definition language (ODL) files, and compiled type libraries.</span></span>

<span data-ttu-id="ea561-108">La Directiva de [**inclusión**](include.md) ACF le permite especificar en un archivo ACF uno o más archivos de encabezado del lenguaje C que se incluirán en el código auxiliar generado por MIDL.</span><span class="sxs-lookup"><span data-stu-id="ea561-108">The ACF [**include**](include.md) directive lets you specify in an ACF file one or more C-language header files to be included in the MIDL-generated stub code.</span></span> <span data-ttu-id="ea561-109">El archivo generado tendrá una línea con una directiva de **\# inclusión** de C-preprocesador con el archivo de encabezado indicado.</span><span class="sxs-lookup"><span data-stu-id="ea561-109">The generated file will have a line with a **\#include** C-preprocessor directive with the indicated header file.</span></span> <span data-ttu-id="ea561-110">Utilice esta directiva **include** para traer archivos de encabezado específicos de un entorno operativo determinado y que no contengan la información necesaria para la interfaz entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="ea561-110">Use this **include** directive to bring in header files that are specific to a particular operating environment and that do not contain information necessary for the interface between client and server.</span></span> <span data-ttu-id="ea561-111">No utilice **include** para los archivos de encabezado que contengan tipos de datos que desee que estén disponibles para el archivo IDL; en su lugar, use la Directiva de [**importación**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="ea561-111">Do not use **include** for header files containing data types that you want available to the IDL file; instead, use the [**import**](import.md) directive.</span></span>

## <a name="example-1"></a><span data-ttu-id="ea561-112">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea561-112">Example 1</span></span>

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

<span data-ttu-id="ea561-113">La Directiva de [**importación**](import.md) de IDL es el método estándar para traer definiciones de tipo y de interfaz de otros archivos IDL (o ODL) y archivos de encabezado en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="ea561-113">The IDL [**import**](import.md) directive is the standard method for bringing type and interface definitions from other IDL (or ODL) files and header files into your IDL file.</span></span> <span data-ttu-id="ea561-114">Todas las instrucciones IDL del archivo importado, como definiciones de tipo, declaraciones [**const**](const.md) y definiciones de interfaz, pasan a estar disponibles para el archivo IDL de importación.</span><span class="sxs-lookup"><span data-stu-id="ea561-114">All IDL statements in the imported file, such as typedefs, [**const**](const.md) declarations, and interface definitions become available to the importing IDL file.</span></span>

<span data-ttu-id="ea561-115">Como la Directiva de preprocesador de lenguaje C **\# incluye**, la directiva [**Import**](import.md) indica al compilador que incluya los tipos de datos que se definieron en los archivos IDL importados.</span><span class="sxs-lookup"><span data-stu-id="ea561-115">Like the C-language preprocessor directive **\#include**, the [**import**](import.md) directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="ea561-116">A diferencia de la directiva **\# include** , la directiva **Import** omite los prototipos de procedimiento, ya que no se genera ningún código auxiliar para nada en el archivo importado.</span><span class="sxs-lookup"><span data-stu-id="ea561-116">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span> <span data-ttu-id="ea561-117">Dado que el preprocesador se invoca por separado para el archivo importado, las directivas de preprocesador (por ejemplo, \* \*) no se transportan al archivo IDL de importación.</span><span class="sxs-lookup"><span data-stu-id="ea561-117">Because the preprocessor is invoked separately for the imported file, preprocessor directives (such as \*\*) do not carry over to the importing IDL file.</span></span>

<span data-ttu-id="ea561-118">Para obtener información adicional sobre cómo usar [**importar**](import.md) para incluir archivos de encabezado del sistema en un archivo IDL, vea [importar archivos de encabezado del sistema](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="ea561-118">For additional information on using [**import**](import.md) to include system header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

## <a name="example-2"></a><span data-ttu-id="ea561-119">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea561-119">Example 2</span></span>

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

<span data-ttu-id="ea561-120">La Directiva ODL [**importlib**](importlib.md) le permite hacer referencia a una biblioteca de tipos compilada en el archivo IDL o ODL.</span><span class="sxs-lookup"><span data-stu-id="ea561-120">The ODL [**importlib**](importlib.md) directive lets you reference a compiled type library in your IDL or ODL file.</span></span> <span data-ttu-id="ea561-121">La directiva **importlib** debe estar dentro de una instrucción [**Library**](library.md) y debe preceder a otras descripciones de tipo de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ea561-121">The **importlib** directive must be inside a [**library**](library.md) statement, and must precede other type descriptions in the library.</span></span> <span data-ttu-id="ea561-122">La biblioteca importada, así como la biblioteca generada, deben estar disponibles para la aplicación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ea561-122">The imported library, as well as the generated library, must be available to the application at runtime.</span></span>

## <a name="example-3"></a><span data-ttu-id="ea561-123">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="ea561-123">Example 3</span></span>

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

<span data-ttu-id="ea561-124">También puede usar la directiva **\# include** del preprocesador C para incluir encabezados y otros archivos en el archivo IDL o ODL.</span><span class="sxs-lookup"><span data-stu-id="ea561-124">You can also use the C-preprocessor **\#include** directive to include headers and other files in your IDL or ODL file.</span></span> <span data-ttu-id="ea561-125">No obstante, tenga en cuenta que esta directiva incluirá literalmente todo el contenido del archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="ea561-125">Be aware, however, that this directive will literally include the entire contents of the specified file.</span></span> <span data-ttu-id="ea561-126">Si un archivo de encabezado contiene prototipos que no necesita o desea en los archivos de código auxiliar generados por MIDL, o si contiene definiciones de tipo no utilizables, debe usar la Directiva de [**importación**](import.md) MIDL en lugar de la directiva **\# include** .</span><span class="sxs-lookup"><span data-stu-id="ea561-126">If a header file contains prototypes that you do not need or want in the MIDL-generated stub files, or if it contains nonremotable type definitions, you should use the MIDL [**import**](import.md) directive instead of the **\#include** directive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea561-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea561-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea561-128">**importar**</span><span class="sxs-lookup"><span data-stu-id="ea561-128">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="ea561-129">**importlib**</span><span class="sxs-lookup"><span data-stu-id="ea561-129">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="ea561-130">**inclui**</span><span class="sxs-lookup"><span data-stu-id="ea561-130">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="ea561-131">Importación de archivos de encabezado del sistema</span><span class="sxs-lookup"><span data-stu-id="ea561-131">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 





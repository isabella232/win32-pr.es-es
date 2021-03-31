---
title: Guardar la salida del preprocesador
description: La visualización de la salida del preprocesador puede ser un método eficaz de solución de problemas, como cuando se produce una sintaxis de preprocesador IDL, C o C, o cuando los valores fantasma en la línea de comandos de MIDL dan como resultado errores de los informes de MIDL.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL del compilador MIDL, guardar la salida del preprocesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418817"
---
# <a name="saving-preprocessor-output"></a><span data-ttu-id="4a5e8-104">Guardar la salida del preprocesador</span><span class="sxs-lookup"><span data-stu-id="4a5e8-104">Saving Preprocessor Output</span></span>

<span data-ttu-id="4a5e8-105">La visualización de la salida del preprocesador puede ser un método eficaz de solución de problemas, como cuando se produce una sintaxis de preprocesador IDL, C o C, o cuando los valores fantasma en la línea de comandos de MIDL dan como resultado errores de los informes de MIDL.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-105">Viewing preprocessor output can be an effective troubleshooting method, such as when invalid IDL, C, or C-preprocessor syntax occurs, or when bogus -D values on the MIDL command line result in MIDL reporting arcane errors.</span></span> <span data-ttu-id="4a5e8-106">Los desarrolladores también pueden querer examinar la salida del preprocesador para determinar qué archivos y definiciones estaban presentes en el flujo de entrada del compilador, por ejemplo, cuando se debe resolver un caso difícil de conflicto de redefinición de tipo.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-106">Developers may also want to examine preprocessor output to determine which files and definitions were present in the compiler input stream, such as when a difficult case of type redefinition conflict must be resolved.</span></span> <span data-ttu-id="4a5e8-107">O menos comúnmente, algunos desarrolladores pueden querer forzar los conmutadores privados en el preprocesador con [**/CPP \_ OPT**](-cpp-opt.md), o bien, puede que desee ver cómo funcionan los conmutadores.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-107">Or less commonly, certain developers may want to force private switches on the preprocessor with [**/cpp\_opt**](-cpp-opt.md), or may want to see how the switches work.</span></span>

<span data-ttu-id="4a5e8-108">La forma más sencilla y molesta de obtener los archivos preprocesados de una ejecución de compilación de MIDL es usar el modificador [**-savePP**](-savepp.md) .</span><span class="sxs-lookup"><span data-stu-id="4a5e8-108">The easiest and the least obtrusive way to obtain the preprocessed files from a MIDL compile run is to use the [**-savePP**](-savepp.md) switch.</span></span> <span data-ttu-id="4a5e8-109">El modificador **-savePP** simplemente impide que MIDL elimine los archivos temporales que el preprocesador pasa de nuevo a MIDL.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-109">The **-savePP** switch simply prevents MIDL from deleting the temporary files that the preprocessor passes back to MIDL.</span></span> <span data-ttu-id="4a5e8-110">Tenga en cuenta lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-110">Consider the following:</span></span>

<span data-ttu-id="4a5e8-111">**MIDL-savePP-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1-Oicf-env Win32 stub. idl**</span><span class="sxs-lookup"><span data-stu-id="4a5e8-111">**midl -savePP -Id:\\nt\\public\\sdk\\inc -DNTENV=1 -Oicf -env win32 stub.idl**</span></span>

<span data-ttu-id="4a5e8-112">Esta directiva compila stub. idl, conserva todos los archivos de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-112">This directive compiles Stub.idl, yet preserves all preprocessor files.</span></span>

> [!Note]  
> <span data-ttu-id="4a5e8-113">MIDL genera ejecuciones de preprocesador independientes para archivos IDL y ACF (si existen), así como para todos los archivos importados.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-113">MIDL spawns separate preprocessor runs for IDL and ACF file (if present) as well as for every imported file.</span></span>

 

<span data-ttu-id="4a5e8-114">En el caso de una compilación DCOM, normalmente se generan varios archivos de preprocesador, aunque MIDL los procesa como un flujo de entrada contiguo virtual.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-114">For a DCOM compile, several preprocessor files are typically produced, even though they are processed by MIDL as a virtual contiguous input stream.</span></span> <span data-ttu-id="4a5e8-115">En un entorno de programación de Windows típico, los archivos temporales se pueden encontrar en el directorio Temp como nombres de archivo como MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-115">In a typical Windows programming environment, the temporary files can be found in the Temp directory as file names such as MID\*.tmp.</span></span> <span data-ttu-id="4a5e8-116">Si se conserva la salida del preprocesador, se recomienda inspeccionar los archivos recientes en el directorio temporal para identificar qué archivos están asociados con qué ejecución del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-116">If preserving preprocessor output, it is good practice to watch for recent files in the Temp directory to identify which files are associated with which preprocessor run.</span></span>

<span data-ttu-id="4a5e8-117">En casos sencillos, como cuando el archivo IDL compilado no importa otros archivos directa o indirectamente, o al examinar el archivo de nivel superior, el preprocesador se puede invocar directamente.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-117">In simple cases, such as when the compiled IDL file does not import other files directly or indirectly, or when examining the top-level file, the preprocessor can be invoked directly.</span></span> <span data-ttu-id="4a5e8-118">La ejecución directa del preprocesador de C/C++ puede revelar errores enmascarados o confundidos por MIDL.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-118">Executing C/C++ preprocessor directly can reveal errors masked or confused by MIDL.</span></span> <span data-ttu-id="4a5e8-119">Por ejemplo, las dos líneas de comandos de preprocesador siguientes se pueden usar para la línea MIDL previamente entrecomillada:</span><span class="sxs-lookup"><span data-stu-id="4a5e8-119">For example, the following two preprocessor command lines can be used for the previously quoted MIDL line:</span></span>

<span data-ttu-id="4a5e8-120">**CL/E/nologo-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1 stub. idl > stub. PP**</span><span class="sxs-lookup"><span data-stu-id="4a5e8-120">**cl /E /nologo -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl > stub.pp**</span></span>

<span data-ttu-id="4a5e8-121">**CL/E/P-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1 stub. idl**</span><span class="sxs-lookup"><span data-stu-id="4a5e8-121">**cl /E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl**</span></span>

<span data-ttu-id="4a5e8-122">En el primero de estos dos ejemplos, **/e** [**/nologo**](-nologo.md) son los modificadores que MIDL agrega al invocar al preprocesador.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-122">In the first of these two examples, **/E** [**/nologo**](-nologo.md) are the switches that MIDL adds when invoking the preprocessor.</span></span> <span data-ttu-id="4a5e8-123">La salida del preprocesador se envía a stdout (la pantalla) y, por tanto, requiere la redirección a un archivo para su examen.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-123">The preprocessor output is sent to stdout (the screen), and therefore requires redirection to a file for examination.</span></span> <span data-ttu-id="4a5e8-124">En el segundo de estos ejemplos, **/p** dirige el preprocesador para redirigir la salida a un \* archivo. i; en este caso, se crearía un archivo stub. i en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-124">In the second of these examples, **/P** directs the preprocessor to redirect the output to a \*.i file; in this case a Stub.i file would be created in the current directory.</span></span>

<span data-ttu-id="4a5e8-125">El modificador [**\_ OPT de/CPP**](-cpp-opt.md) también se puede usar para obtener un archivo preprocesado, pero es difícil y inferior a los métodos mencionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-125">The [**/cpp\_opt**](-cpp-opt.md) switch can also be used to obtain a preprocessed file, but is difficult and inferior to the previously mentioned methods.</span></span> <span data-ttu-id="4a5e8-126">En el ejemplo siguiente también se genera un archivo stub. i, como se hizo en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="4a5e8-126">The following example also produces a Stub.i file, as did the previous example.</span></span> <span data-ttu-id="4a5e8-127">Las comillas en el ejemplo siguiente son esenciales:</span><span class="sxs-lookup"><span data-stu-id="4a5e8-127">The quotes in the following example are essential:</span></span>

<span data-ttu-id="4a5e8-128">**MIDL-Oicf-Win32-CPP \_ OPT "/E/p-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1" stub. idl**</span><span class="sxs-lookup"><span data-stu-id="4a5e8-128">**Midl -Oicf -win32 -cpp\_opt "/E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1" stub.idl**</span></span>

 

 





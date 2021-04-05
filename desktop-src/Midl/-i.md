---
title: Modificador/i
description: El modificador/I especifica los directorios en los que se van a buscar archivos IDL importados, archivos de encabezado incluidos y archivos ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I modificador MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076844"
---
# <a name="i-switch"></a><span data-ttu-id="6b5b7-104">Modificador/i</span><span class="sxs-lookup"><span data-stu-id="6b5b7-104">/I switch</span></span>

<span data-ttu-id="6b5b7-105">El modificador **/i** especifica los directorios en los que se van a buscar archivos IDL importados, archivos de encabezado incluidos y archivos ACF.</span><span class="sxs-lookup"><span data-stu-id="6b5b7-105">The **/I** switch specifies directories to be searched for imported IDL files, included header files, and ACF files.</span></span>

``` syntax
midl /I include_path
```

## <a name="switch-options"></a><span data-ttu-id="6b5b7-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="6b5b7-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="6b5b7-107">*Ruta de inclusión \_*</span><span class="sxs-lookup"><span data-stu-id="6b5b7-107">*include\_path*</span></span> 
</dt> <dd>

<span data-ttu-id="6b5b7-108">Especifica uno o más directorios que contienen archivos de importación, inclusión y ACF.</span><span class="sxs-lookup"><span data-stu-id="6b5b7-108">Specifies one or more directories that contain import, include, and ACF files.</span></span> <span data-ttu-id="6b5b7-109">El espacio en blanco entre el modificador **/i** y la *ruta de \_ acceso de inclusión* es opcional.</span><span class="sxs-lookup"><span data-stu-id="6b5b7-109">White space between the **/I** switch and *include\_path* is optional.</span></span> <span data-ttu-id="6b5b7-110">Separe varios directorios con un carácter de punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="6b5b7-110">Separate multiple directories with a semicolon character (;).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b5b7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b5b7-111">Remarks</span></span>

<span data-ttu-id="6b5b7-112">Puede aparecer más de un directorio con cada modificador **/i** y puede aparecer más de un modificador **/i** con cada invocación del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="6b5b7-112">More than one directory can appear with each **/I** switch, and more than one **/I** switch can appear with each MIDL compiler invocation.</span></span> <span data-ttu-id="6b5b7-113">Los directorios se buscan en el orden en que se especifican.</span><span class="sxs-lookup"><span data-stu-id="6b5b7-113">Directories are searched in the order they are specified.</span></span>

<span data-ttu-id="6b5b7-114">El compilador MIDL pasa también el valor del modificador **/i** al preprocesador de c del compilador de c.</span><span class="sxs-lookup"><span data-stu-id="6b5b7-114">The **/I** switch setting is also passed by the MIDL compiler to the C compiler's C preprocessor.</span></span> <span data-ttu-id="6b5b7-115">Cuando el modificador [**\_ cmd de/CPP**](-cpp-cmd.md) está presente y el modificador [**\_ OPT de/CPP**](-cpp-opt.md) no es, el compilador MIDL concatena la cadena especificada por el modificador **/CPP \_ cmd** con las opciones **/i**, [**/d**](-d.md)y [**/U**](-u.md) y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF.</span><span class="sxs-lookup"><span data-stu-id="6b5b7-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the **/I**, [**/D**](-d.md), and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="6b5b7-116">El modificador de compilador de MIDL **/i** no se pasa al preprocesador cuando se especifica el modificador del compilador MIDL **/no \_ CPP** o **/CPP \_ OPC** .</span><span class="sxs-lookup"><span data-stu-id="6b5b7-116">The MIDL compiler switch **/I** is not passed to the preprocessor when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

<span data-ttu-id="6b5b7-117">En los entornos de sistema operativo de Microsoft (Windows de 64 bits, Windows de 32 bits, Windows de 16 bits y MS-DOS), los directorios se buscan en la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b5b7-117">In Microsoft operating-system environments (64-bit Windows, 32-bit Windows, 16-bit Windows, and MS-DOS), directories are searched in the following sequence:</span></span>

1.  <span data-ttu-id="6b5b7-118">Directorio actual</span><span class="sxs-lookup"><span data-stu-id="6b5b7-118">Current directory</span></span>
2.  <span data-ttu-id="6b5b7-119">Directorios especificados por el modificador **/i** (en el orden en el que siguen el modificador)</span><span class="sxs-lookup"><span data-stu-id="6b5b7-119">Directories specified by the **/I** switch (in the order they follow the switch)</span></span>
3.  <span data-ttu-id="6b5b7-120">Directorios especificados por la variable de entorno INCLUDE</span><span class="sxs-lookup"><span data-stu-id="6b5b7-120">Directories specified by the INCLUDE environment variable</span></span>

<span data-ttu-id="6b5b7-121">Cuando se especifican directorios con el modificador **/i** , el modificador [**/no \_ Def \_ Idir**](-no-def-idir.md) indica al compilador de MIDL que omita el directorio actual, omita los directorios especificados por la variable de entorno include y busque solo los directorios especificados.</span><span class="sxs-lookup"><span data-stu-id="6b5b7-121">When directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to ignore the current directory, ignore the directories specified by the INCLUDE environment variable, and search only the specified directories.</span></span>

<span data-ttu-id="6b5b7-122">Cuando no se especifica ningún directorio con el modificador **/i** , el modificador [**/no \_ Def \_ Idir**](-no-def-idir.md) indica al compilador de MIDL que busque solo el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="6b5b7-122">When no directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="6b5b7-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6b5b7-123">Examples</span></span>

<span data-ttu-id="6b5b7-124">**MIDL/I c: \\ include; c: \\ include \\ h/i \\ include2 nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="6b5b7-124">**midl /I c:\\include;c:\\include\\h /I\\include2 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6b5b7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b5b7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b5b7-126">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="6b5b7-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6b5b7-127">**/acf**</span><span class="sxs-lookup"><span data-stu-id="6b5b7-127">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="6b5b7-128">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="6b5b7-128">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="6b5b7-129">**/CPP \_ OPC**</span><span class="sxs-lookup"><span data-stu-id="6b5b7-129">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="6b5b7-130">**/no \_ Def \_ Idir**</span><span class="sxs-lookup"><span data-stu-id="6b5b7-130">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 





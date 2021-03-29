---
title: Requisitos del preprocesador de C para MIDL
description: Esta página se aplica solo a los desarrolladores que tienen razones específicas para reemplazar el preprocesador de C/C++ de Microsoft como el preprocesador usado por MIDL, o a los desarrolladores que deben especificar modificadores de preprocesador personalizados.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- 'MIDL del compilador MIDL, C: preprocesador, requisitos'
- 'C: preprocesador MIDL, requisitos'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994455"
---
# <a name="c-preprocessor-requirements-for-midl"></a><span data-ttu-id="0a970-105">Requisitos del preprocesador de C para MIDL</span><span class="sxs-lookup"><span data-stu-id="0a970-105">C-Preprocessor Requirements for MIDL</span></span>

<span data-ttu-id="0a970-106">Esta página se aplica solo a los desarrolladores que tienen razones específicas para reemplazar el preprocesador de C/C++ de Microsoft como el preprocesador usado por MIDL, o a los desarrolladores que deben especificar modificadores de preprocesador personalizados.</span><span class="sxs-lookup"><span data-stu-id="0a970-106">This page applies only to developers who have specific reasons to replace the Microsoft C/C++ preprocessor as the preprocessor used by MIDL, or to developers who must specify customized preprocessor switches.</span></span> <span data-ttu-id="0a970-107">Los modificadores MIDL [**/CPP \_ cmd**](-cpp-cmd.md), [**/CPP \_ OPC**](-cpp-opt.md)y [**/no \_ CPP**](-no-cpp-nocpp.md) se utilizan para invalidar el comportamiento predeterminado del compilador.</span><span class="sxs-lookup"><span data-stu-id="0a970-107">The MIDL switches [**/cpp\_cmd**](-cpp-cmd.md), [**/cpp\_opt**](-cpp-opt.md), and [**/no\_cpp**](-no-cpp-nocpp.md) are used to override the default behavior of the compiler.</span></span> <span data-ttu-id="0a970-108">Normalmente, no hay ningún motivo para reemplazar el preprocesador de Microsoft C/C++ ni para especificar modificadores de preprocesador personalizados.</span><span class="sxs-lookup"><span data-stu-id="0a970-108">There is typically no reason to replace the Microsoft C/C++ preprocessor, nor to specify customized preprocessor switches.</span></span>

<span data-ttu-id="0a970-109">El compilador MIDL usa un preprocesador de C durante el procesamiento inicial del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="0a970-109">The MIDL compiler uses a C preprocessor during initial processing of the IDL file.</span></span> <span data-ttu-id="0a970-110">El entorno de compilación usado al compilar los archivos IDL está asociado a un preprocesador de C/C++ predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0a970-110">The build environment used when compiling the IDL files is associated with a default C/C++ preprocessor.</span></span> <span data-ttu-id="0a970-111">Si se va a usar un preprocesador diferente, el modificador del compilador MIDL [**/CPP \_ cmd**](-cpp-cmd.md) habilita una invalidación del nombre del preprocesador de C/C++ predeterminado:</span><span class="sxs-lookup"><span data-stu-id="0a970-111">If a different preprocessor is to be used, the MIDL compiler switch [**/cpp\_cmd**](-cpp-cmd.md) enables an override of the default C/C++-preprocessor name:</span></span>

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span data-ttu-id="0a970-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*nombre del preprocesador \_*</span><span class="sxs-lookup"><span data-stu-id="0a970-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*preprocessor\_name*</span></span>
</dt> <dd>

<span data-ttu-id="0a970-113">Especifica el nombre del preprocesador que va a usar MIDL.</span><span class="sxs-lookup"><span data-stu-id="0a970-113">Specifies the name of the preprocessor to be used by MIDL.</span></span> <span data-ttu-id="0a970-114">Se puede especificar con una ruta de acceso al archivo binario.</span><span class="sxs-lookup"><span data-stu-id="0a970-114">May be specified with a path to the binary.</span></span> <span data-ttu-id="0a970-115">La extensión. exe es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a970-115">The .exe extension is optional.</span></span>

</dd> <dt>

<span data-ttu-id="0a970-116"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="0a970-116"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="0a970-117">Especifica el nombre del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="0a970-117">Specifies the name of the IDL file.</span></span>

</dd> </dl>

-   <span data-ttu-id="0a970-118">El compilador MIDL espera que cualquier preprocesador respete las convenciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="0a970-118">The MIDL compiler expects any preprocessor to observe the following conventions:</span></span>
-   <span data-ttu-id="0a970-119">El archivo de entrada se especifica como el último argumento de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0a970-119">The input file is specified as the last argument on the command line.</span></span>
-   <span data-ttu-id="0a970-120">El preprocesador debe redirigir la salida al dispositivo de salida estándar, stdout.</span><span class="sxs-lookup"><span data-stu-id="0a970-120">The preprocessor must redirect output to the standard output device, stdout.</span></span>
-   <span data-ttu-id="0a970-121">En el flujo de salida del preprocesador, las directivas de **\# línea** están presentes para permitir mejores mensajes de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0a970-121">In the output stream of the preprocessor, the **\#line** directives are present to enable better diagnostic messages.</span></span>
-   <span data-ttu-id="0a970-122">Las directivas de línea son las únicas directivas de preprocesador en el flujo de salida.</span><span class="sxs-lookup"><span data-stu-id="0a970-122">The line directives are the only preprocessor directives in the output stream.</span></span>

<span data-ttu-id="0a970-123">MIDL supone que el preprocesador generado ha quitado todas las directivas de preprocesador del flujo de entrada del compilador, con la excepción de las repeticiones de la Directiva de línea necesarias para identificar la ubicación de origen en los mensajes del compilador.</span><span class="sxs-lookup"><span data-stu-id="0a970-123">MIDL assumes that the spawned preprocessor has removed all preprocessor directives from the input stream of the compiler, with the exception of the occurrences of the line directive necessary for pinpointing source location in compiler messages.</span></span> <span data-ttu-id="0a970-124">Cuando se indica un preprocesador diferente del preprocesador de C/C++ de Microsoft, o cuando se especifican opciones del preprocesador con el modificador [**/CPP \_ OPC**](-cpp-opt.md) , se requiere una opción de preprocesador adecuada que coloque las directivas de línea en el flujo de entrada del compilador.</span><span class="sxs-lookup"><span data-stu-id="0a970-124">When indicating a preprocessor different from the Microsoft C/C++ preprocessor, or when specifying preprocessor options with the [**/cpp\_opt**](-cpp-opt.md) switch, specifying an appropriate preprocessor option that puts the line directives in the input stream of the compiler is required.</span></span> <span data-ttu-id="0a970-125">Por ejemplo, para el preprocesador de C/C++ de Microsoft, debe usarse la opción **/e** :</span><span class="sxs-lookup"><span data-stu-id="0a970-125">For example, for the Microsoft C/C++ preprocessor the **/E** option would have to be used:</span></span>

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

<span data-ttu-id="0a970-126">La Directiva de **\# línea** es aceptada por MIDL en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="0a970-126">The **\#line** directive is accepted by MIDL in one of the following forms:</span></span>

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

<span data-ttu-id="0a970-127">Para obtener una descripción completa de la directiva line y otras directivas de preprocesador, vea la documentación del compilador de C que se está usando.</span><span class="sxs-lookup"><span data-stu-id="0a970-127">For a complete description of the line directive and other preprocessor directives, see the documentation for the C-compiler being used.</span></span>

<span data-ttu-id="0a970-128">MIDL solo acepta la Directiva de preprocesador de línea.</span><span class="sxs-lookup"><span data-stu-id="0a970-128">MIDL accepts only the line preprocessor directive.</span></span> <span data-ttu-id="0a970-129">Por lo tanto, si se utiliza el modificador [**/no \_ CPP**](-no-cpp-nocpp.md) , el archivo de entrada no debe tener otras directivas de preprocesador, o el archivo de entrada se debe haber procesado antes de invocar MIDL.</span><span class="sxs-lookup"><span data-stu-id="0a970-129">Therefore, if the [**/no\_cpp**](-no-cpp-nocpp.md) switch is used, the input file must not have other preprocessor directives, or the input file must have been processed prior to invoking MIDL.</span></span>

<span data-ttu-id="0a970-130">Para obtener más información, vea [trabajar con las \# definiciones de los archivos IDL](dealing-with-defines-in-idl-files-2.md).</span><span class="sxs-lookup"><span data-stu-id="0a970-130">For more information, see [Dealing with \#defines in IDL Files](dealing-with-defines-in-idl-files-2.md).</span></span>

 

 





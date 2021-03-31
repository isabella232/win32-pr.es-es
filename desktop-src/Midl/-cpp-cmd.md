---
title: modificador/cpp_cmd
description: El \_ modificador cmd de/CPP especifica el preprocesador que el compilador MIDL utiliza para preprocesar los archivos de entrada.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd modificador MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784234"
---
# <a name="cpp_cmd-switch"></a><span data-ttu-id="64e71-104">\_modificador cmd de/CPP</span><span class="sxs-lookup"><span data-stu-id="64e71-104">/cpp\_cmd switch</span></span>

<span data-ttu-id="64e71-105">El modificador **\_ cmd de/CPP** especifica el preprocesador que el compilador MIDL utiliza para preprocesar los archivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="64e71-105">The **/cpp\_cmd** switch specifies the preprocessor that the MIDL compiler uses to preprocess input files.</span></span>

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a><span data-ttu-id="64e71-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="64e71-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="64e71-107">*\_Binario de preprocesador de C \_*</span><span class="sxs-lookup"><span data-stu-id="64e71-107">*C\_preprocessor\_binary*</span></span> 
</dt> <dd>

<span data-ttu-id="64e71-108">Especifica el comando que invoca el preprocesador.</span><span class="sxs-lookup"><span data-stu-id="64e71-108">Specifies the command that invokes the preprocessor.</span></span> <span data-ttu-id="64e71-109">Este comando permite a los desarrolladores reemplazar el preprocesador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="64e71-109">This command allows developers to override the default preprocessor.</span></span> <span data-ttu-id="64e71-110">De forma predeterminada, MIDL invoca el compilador de C/C++ de Microsoft desde el entorno de compilación de la máquina de compilación.</span><span class="sxs-lookup"><span data-stu-id="64e71-110">By default, MIDL invokes the Microsoft C/C++ compiler from the build machine's build environment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64e71-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64e71-111">Remarks</span></span>

<span data-ttu-id="64e71-112">El *argumento \_ \_ binario del preprocesador de C* para el modificador puede especificar la ruta de acceso completa; el sufijo y las comillas exe son opcionales.</span><span class="sxs-lookup"><span data-stu-id="64e71-112">The *C\_preprocessor\_binary* argument to the switch may specify the full path; the exe suffix and quotes are optional.</span></span> <span data-ttu-id="64e71-113">Normalmente, los desarrolladores usan el modificador para elegir una versión concreta del preprocesador de C/C++ de Microsoft o equivalente en el entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="64e71-113">Typically, developers use the switch to choose a particular version of the Microsoft C/C++ preprocessor or equivalent in the build environment.</span></span> <span data-ttu-id="64e71-114">En este caso, no es necesario usar el modificador [**\_ OPT/CPP**](-cpp-opt.md) con **/CPP \_ cmd**.</span><span class="sxs-lookup"><span data-stu-id="64e71-114">In this case, it is not necessary to use the [**/cpp\_opt**](-cpp-opt.md) switch with **/cpp\_cmd**.</span></span>

<span data-ttu-id="64e71-115">Cuando se usa un preprocesador que no es de Microsoft, en especial cuando el preprocesador especificado no dirige su salida a stdout, se debe especificar el modificador de compilador de C que redirige la salida a stdout como parte del modificador [**/CPP \_ OPC**](-cpp-opt.md) del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="64e71-115">When using a non-Microsoft preprocessor, especially when the specified preprocessor does not direct its output to stdout, the C compiler switch that redirects output to stdout as part of the MIDL compiler [**/cpp\_opt**](-cpp-opt.md) switch must be specified.</span></span> <span data-ttu-id="64e71-116">Vea [requisitos del preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md) para obtener más información</span><span class="sxs-lookup"><span data-stu-id="64e71-116">See [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for details</span></span>

<span data-ttu-id="64e71-117">El preprocesador se invoca mediante una cadena de comando que se forma a partir de la información proporcionada al compilador de MIDL mediante los modificadores **/CPP \_ cmd**, [**/CPP \_ OPC**](-cpp-opt.md), [**/d**](-d.md), [**/i**](-i.md)y [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="64e71-117">The preprocessor is invoked by a command string that is formed from the information provided to the MIDL compiler by **/cpp\_cmd**, [**/cpp\_opt**](-cpp-opt.md), [**/D**](-d.md), [**/I**](-i.md), and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="64e71-118">En la tabla siguiente se resume cómo se construye la cadena de comandos para cada combinación de modificadores **/CPP \_ cmd** y **/CPP \_ OPC** .</span><span class="sxs-lookup"><span data-stu-id="64e71-118">The following table summarizes how the command string is constructed for each combination of **/cpp\_cmd** and **/cpp\_opt** switches.</span></span>

<span data-ttu-id="64e71-119">Cuando no se especifica el modificador **/CPP \_ cmd** , el compilador MIDL invoca el compilador de Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="64e71-119">When the **/cpp\_cmd** switch is not specified, the MIDL compiler invokes the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="64e71-120">MIDL usa un binario Cl.exe que se encuentra en el entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="64e71-120">MIDL uses a Cl.exe binary found in the build environment.</span></span>

<span data-ttu-id="64e71-121">Cuando el modificador [**\_ OPT/CPP**](-cpp-opt.md) no está presente, el compilador MIDL concatena la cadena especificada por el modificador **\_ cmd/CPP** con la información especificada por las opciones de MIDL [**/i**](-i.md), [**/d**](-d.md) y [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="64e71-121">When the [**/cpp\_opt**](-cpp-opt.md) switch is not present, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the information specified by the MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) options.</span></span> <span data-ttu-id="64e71-122">La cadena/E también se concatena con la cadena de invocación del compilador de C para indicar que el compilador de C/C++ solo debe realizar el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="64e71-122">The string /E is also concatenated to the C-compiler invocation string to indicate that the C/C++ compiler should perform preprocessing only.</span></span> <span data-ttu-id="64e71-123">El modificador [**/nologo**](-nologo.md) se agrega para suprimir el banner del compilador de C/C++.</span><span class="sxs-lookup"><span data-stu-id="64e71-123">The [**/nologo**](-nologo.md) switch is added to suppress the C/C++ compiler banner.</span></span> <span data-ttu-id="64e71-124">El compilador MIDL usa la cadena concatenada para invocar el preprocesador de C para IDL de nivel superior, así como los archivos IDL importados, y también para los archivos ACF correspondientes presentes.</span><span class="sxs-lookup"><span data-stu-id="64e71-124">The MIDL compiler uses the concatenated string to invoke the C preprocessor for top-level IDL as well as imported IDL files, and also for any present, corresponding ACF files.</span></span>

<span data-ttu-id="64e71-125">Cuando el modificador [**\_ OPT/CPP**](-cpp-opt.md) está presente, que debe ser un caso poco frecuente en las plataformas actuales de 32 bits y 64 bits, el compilador MIDL concatena la cadena especificada por el modificador **\_ cmd/CPP** con la cadena especificada por el modificador **/CPP \_ OPC** .</span><span class="sxs-lookup"><span data-stu-id="64e71-125">When the [**/cpp\_opt**](-cpp-opt.md) switch is present, which should be a rare case for the current 32-bit and 64-bit platforms, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the string specified by the **/cpp\_opt** switch.</span></span> <span data-ttu-id="64e71-126">El compilador MIDL utiliza la cadena concatenada para invocar el binario del preprocesador indicado en lugar del preprocesador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="64e71-126">The MIDL compiler uses the concatenated string to invoke the indicated preprocessor binary in place of the default preprocessor.</span></span> <span data-ttu-id="64e71-127">Cuando el modificador **\_ OPT/CPP** está presente, ni las opciones del compilador de MIDL especificadas por los modificadores [**/I**](-i.md), [**/d**](-d.md)y [**/u**](-u.md) ni el modificador del compilador de C/e se concatenan con la cadena.</span><span class="sxs-lookup"><span data-stu-id="64e71-127">When the **/cpp\_opt** switch is present, neither the MIDL compiler options specified by the [**/I**](-i.md), [**/D**](-d.md), and [**/U**](-u.md) switches nor the C compiler switch /E is concatenated with the string.</span></span> <span data-ttu-id="64e71-128">Debe proporcionar la opción/E, o equivalente, como parte de la cadena.</span><span class="sxs-lookup"><span data-stu-id="64e71-128">You must supply the /E option, or equivalent, as part of the string.</span></span>



| <span data-ttu-id="64e71-129">\_¿está presente/CPP cmd?</span><span class="sxs-lookup"><span data-stu-id="64e71-129">/cpp\_cmd present?</span></span> | <span data-ttu-id="64e71-130">\_¿/CPP está disponible?</span><span class="sxs-lookup"><span data-stu-id="64e71-130">/cpp\_opt present?</span></span> | <span data-ttu-id="64e71-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="64e71-131">Description</span></span>                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64e71-132">No (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="64e71-132">No (default)</span></span>       | <span data-ttu-id="64e71-133">No (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="64e71-133">No (default)</span></span>       | <span data-ttu-id="64e71-134">Invoca el compilador de Microsoft C/C++ predeterminado con la configuración obtenida de los modificadores de MIDL [**/i**](-i.md), [**/d**](-d.md) y [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="64e71-134">Invokes the default Microsoft C/C++ compiler with settings obtained from MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="64e71-135">Agrega los modificadores de preprocesador/E y [**/nologo**](-nologo.md).</span><span class="sxs-lookup"><span data-stu-id="64e71-135">Adds the preprocessor switches /E and [**/nologo**](-nologo.md).</span></span> |
| <span data-ttu-id="64e71-136">Sí</span><span class="sxs-lookup"><span data-stu-id="64e71-136">Yes</span></span>                | <span data-ttu-id="64e71-137">No</span><span class="sxs-lookup"><span data-stu-id="64e71-137">No</span></span>                 | <span data-ttu-id="64e71-138">Invoca el binario del preprocesador indicado con los mismos modificadores anteriores.</span><span class="sxs-lookup"><span data-stu-id="64e71-138">Invokes the indicated preprocessor binary with the same switches as above.</span></span>                                                                                                                                        |
| <span data-ttu-id="64e71-139">No</span><span class="sxs-lookup"><span data-stu-id="64e71-139">No</span></span>                 | <span data-ttu-id="64e71-140">Sí</span><span class="sxs-lookup"><span data-stu-id="64e71-140">Yes</span></span>                | <span data-ttu-id="64e71-141">Invoca el compilador de C de Microsoft con las opciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="64e71-141">Invokes the Microsoft C compiler with specified options.</span></span> <span data-ttu-id="64e71-142">No usa las opciones de MIDL [**/i**](-i.md), [**/d**](-d.md), [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="64e71-142">Does not use MIDL [**/I**](-i.md), [**/D**](-d.md), [**/U**](-u.md) options.</span></span> <span data-ttu-id="64e71-143">Debe proporcionar/E como parte de [**/CPP \_ OPT**](-cpp-opt.md).</span><span class="sxs-lookup"><span data-stu-id="64e71-143">You must supply /E as part of [**/cpp\_opt**](-cpp-opt.md).</span></span>             |
| <span data-ttu-id="64e71-144">Sí</span><span class="sxs-lookup"><span data-stu-id="64e71-144">Yes</span></span>                | <span data-ttu-id="64e71-145">Sí</span><span class="sxs-lookup"><span data-stu-id="64e71-145">Yes</span></span>                | <span data-ttu-id="64e71-146">Invoca el binario del preprocesador especificado solo con las opciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="64e71-146">Invokes the specified preprocessor binary with specified options only.</span></span> <span data-ttu-id="64e71-147">Debe usar comillas.</span><span class="sxs-lookup"><span data-stu-id="64e71-147">You must use quotes.</span></span>                                                                                                                       |



 

## <a name="examples"></a><span data-ttu-id="64e71-148">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="64e71-148">Examples</span></span>

<span data-ttu-id="64e71-149">**MIDL/CPP \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="64e71-149">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="64e71-150">**MIDL/CPP \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="64e71-150">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="64e71-151">**MIDL/CPP \_ OPT "/E/DFLAG = true/IC: \\ Inc" nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="64e71-151">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="64e71-152">**MIDL/CPP \_ cmd "CL"/CPP \_ OPT "/e/DFLAG = true/IC: \\ Inc" nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="64e71-152">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="64e71-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="64e71-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e71-154">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="64e71-154">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="64e71-155">**/CPP \_ OPC**</span><span class="sxs-lookup"><span data-stu-id="64e71-155">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="64e71-156">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="64e71-156">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="64e71-157">**/no \_ CPP**</span><span class="sxs-lookup"><span data-stu-id="64e71-157">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="64e71-158">Requisitos del preprocesador de C para MIDL</span><span class="sxs-lookup"><span data-stu-id="64e71-158">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 





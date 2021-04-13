---
title: modificador/cpp_opt
description: El \_ modificador/CPP OPC especifica las opciones que se van a pasar al preprocesador de C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt modificador MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104421686"
---
# <a name="cpp_opt-switch"></a><span data-ttu-id="87d6a-104">/CPP \_ OPC</span><span class="sxs-lookup"><span data-stu-id="87d6a-104">/cpp\_opt switch</span></span>

<span data-ttu-id="87d6a-105">El modificador **/CPP \_ OPC** especifica las opciones que se van a pasar al preprocesador de C/C++.</span><span class="sxs-lookup"><span data-stu-id="87d6a-105">The **/cpp\_opt** switch specifies options to pass to the C/C++ preprocessor.</span></span>

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a><span data-ttu-id="87d6a-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="87d6a-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="87d6a-107">*\_Opción de preprocesador de C \_*</span><span class="sxs-lookup"><span data-stu-id="87d6a-107">*C\_preprocessor\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="87d6a-108">Especifica la opción de línea de comandos asociada al preprocesador invocado.</span><span class="sxs-lookup"><span data-stu-id="87d6a-108">Specifies command-line option associated with the invoked preprocessor.</span></span> 

<span data-ttu-id="87d6a-109">**Nota**: para los preprocesadores de Microsoft c/C++, debe proporcionar el `/E` modificador como parte de la cadena de *\_ \_ opción del preprocesador de c* .</span><span class="sxs-lookup"><span data-stu-id="87d6a-109">**Note**: For the Microsoft C/C++ preprocessors you must supply the `/E` switch as part of the *C\_preprocessor\_option* string.</span></span> 

<span data-ttu-id="87d6a-110">Se requieren comillas cuando se usa más de una opción y para espacios.</span><span class="sxs-lookup"><span data-stu-id="87d6a-110">Quotes are required when more than one option is used, and for spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87d6a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87d6a-111">Remarks</span></span>

<span data-ttu-id="87d6a-112">No use este modificador a menos que haya un motivo específico para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="87d6a-112">Do not use this switch unless there is a specific reason for doing so.</span></span> <span data-ttu-id="87d6a-113">Consulte [los requisitos del preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md) para obtener información importante sobre el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="87d6a-113">Consult [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for important information regarding preprocessing.</span></span>

<span data-ttu-id="87d6a-114">El modificador **\_ OPT/CPP** se puede usar con o sin el modificador [**\_ cmd de/CPP**](-cpp-cmd.md) .</span><span class="sxs-lookup"><span data-stu-id="87d6a-114">The **/cpp\_opt** switch can be used with or without the [**/cpp\_cmd**](-cpp-cmd.md) switch.</span></span> <span data-ttu-id="87d6a-115">Consulte **/CPP \_ cmd** para obtener detalles sobre cómo se construye la línea de comandos del preprocesador en cualquier caso.</span><span class="sxs-lookup"><span data-stu-id="87d6a-115">Consult **/cpp\_cmd** for details of how the preprocessor command line is constructed in either case.</span></span>

<span data-ttu-id="87d6a-116">El modificador **\_ OPT de/CPP** , si se especifica, siempre debe incluirse `/E` para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="87d6a-116">The **/cpp\_opt** switch, if specified, must always include `/E` in order to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="87d6a-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="87d6a-117">Examples</span></span>

<span data-ttu-id="87d6a-118">**MIDL/CPP \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="87d6a-118">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="87d6a-119">**MIDL/CPP \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="87d6a-119">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="87d6a-120">**MIDL/CPP \_ OPT "/E/DFLAG = true/IC: \\ Inc" nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="87d6a-120">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="87d6a-121">**MIDL/CPP \_ cmd "CL"/CPP \_ OPT "/e/DFLAG = true/IC: \\ Inc" nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="87d6a-121">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="87d6a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="87d6a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d6a-123">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="87d6a-123">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="87d6a-124">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="87d6a-124">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="87d6a-125">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="87d6a-125">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="87d6a-126">**/no \_ CPP**</span><span class="sxs-lookup"><span data-stu-id="87d6a-126">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="87d6a-127">Requisitos del preprocesador de C para MIDL</span><span class="sxs-lookup"><span data-stu-id="87d6a-127">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 





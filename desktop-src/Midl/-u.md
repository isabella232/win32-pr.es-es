---
title: Modificador/u
description: El modificador/U quita cualquier definición anterior de un nombre pasando el nombre al preprocesador de C como si se tratase de una directiva \ undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U modificador MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148915"
---
# <a name="u-switch"></a><span data-ttu-id="f1d2b-104">Modificador/u</span><span class="sxs-lookup"><span data-stu-id="f1d2b-104">/U switch</span></span>

<span data-ttu-id="f1d2b-105">El modificador **/u** quita cualquier definición anterior de un nombre pasando el nombre al preprocesador de C como si se tratase de una directiva **\# undefine** .</span><span class="sxs-lookup"><span data-stu-id="f1d2b-105">The **/U** switch removes any previous definition of a name by passing the name to the C preprocessor as if by a **\#undefine** directive.</span></span>

``` syntax
midl /U name
```

## <a name="switch-options"></a><span data-ttu-id="f1d2b-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="f1d2b-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="f1d2b-107">*name*</span><span class="sxs-lookup"><span data-stu-id="f1d2b-107">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="f1d2b-108">Especifica un nombre definido que se va a pasar al preprocesador de C como si se realizara una directiva **\# undefine** .</span><span class="sxs-lookup"><span data-stu-id="f1d2b-108">Specifies a defined name to be passed to the C preprocessor as if by a **\#undefine** directive.</span></span> <span data-ttu-id="f1d2b-109">El preprocesador de C o el predefinido por el usuario predefine el nombre.</span><span class="sxs-lookup"><span data-stu-id="f1d2b-109">The name is predefined by the C preprocessor or previously defined by the user.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1d2b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1d2b-110">Remarks</span></span>

<span data-ttu-id="f1d2b-111">Se pueden usar varias directivas de **/u** en una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f1d2b-111">Multiple **/U** directives can be used in a command line.</span></span> <span data-ttu-id="f1d2b-112">El espacio en blanco entre el modificador **/u** y el nombre no definido es opcional.</span><span class="sxs-lookup"><span data-stu-id="f1d2b-112">White space between the **/U** switch and the undefined name is optional.</span></span>

<span data-ttu-id="f1d2b-113">Cuando el modificador [**\_ cmd de/CPP**](-cpp-cmd.md) está presente y el modificador [**\_ OPT de/CPP**](-cpp-opt.md) no es, el compilador MIDL concatena la cadena especificada por el \_ modificador/CPP cmd con las opciones [**/i**](-i.md), [**/d**](-d.md)y **/u** y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF.</span><span class="sxs-lookup"><span data-stu-id="f1d2b-113">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the /cpp\_cmd switch with the [**/I**](-i.md), [**/D**](-d.md), and **/U** options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="f1d2b-114">El modificador del compilador de MIDL se omite cuando se especifica **el modificador** del compilador de MIDL **/no \_ CPP** o **/CPP \_ OPC** .</span><span class="sxs-lookup"><span data-stu-id="f1d2b-114">The MIDL compiler switch **/U** is ignored when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="f1d2b-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f1d2b-115">Examples</span></span>

<span data-ttu-id="f1d2b-116">**MIDL/UUNICODE nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="f1d2b-116">**midl /UUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f1d2b-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1d2b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d2b-118">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="f1d2b-118">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f1d2b-119">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="f1d2b-119">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="f1d2b-120">**/CPP \_ OPC**</span><span class="sxs-lookup"><span data-stu-id="f1d2b-120">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="f1d2b-121">**/D.**</span><span class="sxs-lookup"><span data-stu-id="f1d2b-121">**/D**</span></span>](-d.md)
</dt> <dt>

[<span data-ttu-id="f1d2b-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="f1d2b-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="f1d2b-123">**/no \_ CPP**</span><span class="sxs-lookup"><span data-stu-id="f1d2b-123">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 





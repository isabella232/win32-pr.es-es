---
title: /D (modificador)
description: El modificador/D define un nombre y un valor opcional que se va a pasar al preprocesador de C como si se realizara una directiva \ define. Se pueden usar varias directivas/D en una línea de comandos.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D modificador MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148938"
---
# <a name="d-switch"></a><span data-ttu-id="29c6d-105">/D (modificador)</span><span class="sxs-lookup"><span data-stu-id="29c6d-105">/D switch</span></span>

<span data-ttu-id="29c6d-106">El modificador **/d** define un nombre y un valor opcional que se va a pasar al preprocesador de C como si se realizara una directiva de **\# definición** .</span><span class="sxs-lookup"><span data-stu-id="29c6d-106">The **/D** switch defines a name and an optional value to be passed to the C preprocessor as if by a **\#define** directive.</span></span> <span data-ttu-id="29c6d-107">Se pueden usar varias directivas **/d** en una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="29c6d-107">Multiple **/D** directives can be used in a command line.</span></span>

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a><span data-ttu-id="29c6d-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="29c6d-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="29c6d-109">*name*</span><span class="sxs-lookup"><span data-stu-id="29c6d-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="29c6d-110">Especifica un nombre definido que se pasa al preprocesador de C cuando el modificador [**\_ cmd/CPP**](-cpp-cmd.md) está presente y el modificador [**/CPP \_ OPC**](-cpp-opt.md) no está presente.</span><span class="sxs-lookup"><span data-stu-id="29c6d-110">Specifies a defined name that is passed to the C preprocessor when the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not present.</span></span>

</dd> <dt>

<span data-ttu-id="29c6d-111">*definición*</span><span class="sxs-lookup"><span data-stu-id="29c6d-111">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="29c6d-112">Especifica un valor asociado al nombre definido.</span><span class="sxs-lookup"><span data-stu-id="29c6d-112">Specifies a value associated with the defined name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29c6d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29c6d-113">Remarks</span></span>

<span data-ttu-id="29c6d-114">El espacio en blanco entre el modificador **/d** y el nombre definido es opcional.</span><span class="sxs-lookup"><span data-stu-id="29c6d-114">White space between the **/D** switch and the defined name is optional.</span></span>

<span data-ttu-id="29c6d-115">Cuando el modificador [**\_ cmd de/CPP**](-cpp-cmd.md) está presente y el modificador [**\_ OPT de/CPP**](-cpp-opt.md) no es, el compilador MIDL concatena la cadena especificada por el modificador **/CPP \_ cmd** con las opciones [**/i**](-i.md), **/d** y [**/U**](-u.md) y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF.</span><span class="sxs-lookup"><span data-stu-id="29c6d-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the [**/I**](-i.md), **/D**, and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span>

<span data-ttu-id="29c6d-116">Se omite el modificador de compilador de MIDL **/d** cuando se especifica el modificador del compilador MIDL [/no \_ CPP](-no-cpp-nocpp.md) o [**/CPP \_ OPC**](-cpp-opt.md) .</span><span class="sxs-lookup"><span data-stu-id="29c6d-116">The MIDL compiler switch **/D** is ignored when the MIDL compiler switch [/no\_cpp](-no-cpp-nocpp.md) or [**/cpp\_opt**](-cpp-opt.md) is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="29c6d-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="29c6d-117">Examples</span></span>

<span data-ttu-id="29c6d-118">**MIDL-DUNICODE nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="29c6d-118">**midl -DUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="29c6d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="29c6d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29c6d-120">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="29c6d-120">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="29c6d-121">**/CPP \_ OPC**</span><span class="sxs-lookup"><span data-stu-id="29c6d-121">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="29c6d-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="29c6d-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="29c6d-123">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="29c6d-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="29c6d-124">**/no \_ CPP**</span><span class="sxs-lookup"><span data-stu-id="29c6d-124">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="29c6d-125">**/U**</span><span class="sxs-lookup"><span data-stu-id="29c6d-125">**/U**</span></span>](-u.md)
</dt> </dl>

 

 





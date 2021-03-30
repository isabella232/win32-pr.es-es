---
title: modificador/align
description: El modificador/Align es funcionalmente igual que la opción/ZP de MIDL y el compilador MIDL lo reconoce únicamente para mantener la compatibilidad con MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- modificador/align MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532721"
---
# <a name="align-switch"></a><span data-ttu-id="2317b-104">modificador/align</span><span class="sxs-lookup"><span data-stu-id="2317b-104">/align switch</span></span>

<span data-ttu-id="2317b-105">El modificador **/align** es funcionalmente igual que la opción [**/ZP**](-zp.md) de MIDL y el compilador MIDL lo reconoce únicamente para mantener la compatibilidad con MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="2317b-105">The **/align** switch is functionally the same as the MIDL [**/Zp**](-zp.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="2317b-106">La herramienta Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="2317b-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="2317b-107">En su lugar, utilice el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="2317b-107">Use the MIDL compiler instead.</span></span>

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a><span data-ttu-id="2317b-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="2317b-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="2317b-109">*ecuación*</span><span class="sxs-lookup"><span data-stu-id="2317b-109">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="2317b-110">Especifica la alineación de los tipos de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2317b-110">Specifies the alignment for types in the library.</span></span> <span data-ttu-id="2317b-111">El valor de *alineación* puede ser 1, 2, 4 u 8.</span><span class="sxs-lookup"><span data-stu-id="2317b-111">The *alignment* value can be 1, 2, 4, or 8.</span></span> <span data-ttu-id="2317b-112">El valor 1 indica la alineación natural; *n* indica la alineación en byte *n*.</span><span class="sxs-lookup"><span data-stu-id="2317b-112">The value 1 indicates natural alignment; *n* indicates alignment on byte *n*.</span></span> <span data-ttu-id="2317b-113">Cuando no se especifica el modificador **/align** , el valor predeterminado es 8.</span><span class="sxs-lookup"><span data-stu-id="2317b-113">When you do not specify the **/align** switch, the default is 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2317b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2317b-114">Remarks</span></span>

<span data-ttu-id="2317b-115">Si va a generar un nuevo archivo make, use el modificador [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="2317b-115">If you are generating a new makefile, use the [**/Zp**](-zp.md) switch.</span></span>

<span data-ttu-id="2317b-116">El valor de alineación corresponde al valor de la opción [**/ZP**](-zp.md) usado por el compilador de C/C++ de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2317b-116">The alignment value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="2317b-117">Asegúrese de especificar la misma alineación al invocar al compilador de C como cuando se invoca el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="2317b-117">Be sure that you specify the same alignment when you invoke the C compiler as when you invoke the MIDL compiler.</span></span>

<span data-ttu-id="2317b-118">Para obtener más información, vea la documentación de programación de Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="2317b-118">For more information, see your Microsoft C/C++ programming documentation.</span></span> <span data-ttu-id="2317b-119">Para obtener una explicación de los posibles peligros en el uso de niveles de empaquetado no estándar, vea el tema de ayuda de [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="2317b-119">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="2317b-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2317b-120">Examples</span></span>

<span data-ttu-id="2317b-121">**MIDL/align: 4 FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="2317b-121">**midl /align:4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="2317b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2317b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2317b-123">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="2317b-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="2317b-124">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="2317b-124">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 





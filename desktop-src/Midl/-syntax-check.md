---
title: modificador/syntax_check
description: El \_ modificador de comprobación/Syntax indica que el compilador solo comprueba la sintaxis y no genera archivos de salida.
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check modificador MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784013"
---
# <a name="syntax_check-switch"></a><span data-ttu-id="bb1c6-104">\_modificador de comprobación de/Syntax</span><span class="sxs-lookup"><span data-stu-id="bb1c6-104">/syntax\_check switch</span></span>

<span data-ttu-id="bb1c6-105">El modificador de **\_ comprobación/Syntax** indica que el compilador solo comprueba la sintaxis y no genera archivos de salida.</span><span class="sxs-lookup"><span data-stu-id="bb1c6-105">The **/syntax\_check** switch indicates that the compiler checks only syntax and does not generate output files.</span></span>

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a><span data-ttu-id="bb1c6-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="bb1c6-106">Switch Options</span></span>

<span data-ttu-id="bb1c6-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bb1c6-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb1c6-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb1c6-108">Remarks</span></span>

<span data-ttu-id="bb1c6-109">Este modificador invalida todos los demás modificadores que especifican información acerca de los archivos de salida.</span><span class="sxs-lookup"><span data-stu-id="bb1c6-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="bb1c6-110">También puede especificar el modo de comprobación de sintaxis con la opción del compilador de MIDL [**/ZS**](-zs.md).</span><span class="sxs-lookup"><span data-stu-id="bb1c6-110">You can also specify syntax-checking mode with the MIDL compiler option [**/Zs**](-zs.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bb1c6-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bb1c6-111">Examples</span></span>

<span data-ttu-id="bb1c6-112">**MIDL/ZS nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="bb1c6-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="bb1c6-113">**/Syntax de MIDL \_ : Compruebe FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="bb1c6-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="bb1c6-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb1c6-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb1c6-115">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="bb1c6-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="bb1c6-116">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="bb1c6-116">**/Zs**</span></span>](-zs.md)
</dt> </dl>

 

 





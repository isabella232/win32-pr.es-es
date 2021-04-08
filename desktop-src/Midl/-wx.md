---
title: /WX (modificador)
description: El modificador/WX indica al compilador de MIDL que controle todos los errores en el nivel de advertencia dado como errores.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX (modificador) MIDL
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904153"
---
# <a name="wx-switch"></a><span data-ttu-id="4d672-104">/WX (modificador)</span><span class="sxs-lookup"><span data-stu-id="4d672-104">/WX switch</span></span>

<span data-ttu-id="4d672-105">El modificador **/WX** indica al compilador de MIDL que controle todos los errores en el nivel de advertencia dado como errores.</span><span class="sxs-lookup"><span data-stu-id="4d672-105">The **/WX** switch instructs the MIDL compiler to handle all errors at the given warning level as errors.</span></span>

``` syntax
midl /WX
```

## <a name="switch-options"></a><span data-ttu-id="4d672-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="4d672-106">Switch Options</span></span>

<span data-ttu-id="4d672-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4d672-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d672-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d672-108">Remarks</span></span>

<span data-ttu-id="4d672-109">Si se especifica el modificador **/WX** y no se especifica el modificador [**/w**](-w.md)*n* , todas las advertencias en el nivel predeterminado, nivel 1, se tratan como errores.</span><span class="sxs-lookup"><span data-stu-id="4d672-109">If the **/WX** switch is specified and the [**/W**](-w.md)*n* switch is not specified, all warnings at the default level, level 1, are treated as errors.</span></span>

<span data-ttu-id="4d672-110">El modificador [**/w**](-w.md)*n* indica al compilador que muestre todas las advertencias en el nivel *n* y **/WX** indica al compilador que controle todas las advertencias como errores.</span><span class="sxs-lookup"><span data-stu-id="4d672-110">The [**/W**](-w.md)*n* switch directs the compiler to display all warnings at level *n* and **/WX** directs the compiler to handle all warnings as errors.</span></span> <span data-ttu-id="4d672-111">La combinación de estos dos modificadores indica al compilador que controle todas las advertencias en el nivel *n* como errores.</span><span class="sxs-lookup"><span data-stu-id="4d672-111">The combination of these two switches directs the compiler to handle all warnings at level *n* as errors.</span></span>

<span data-ttu-id="4d672-112">Los errores son diferentes de las advertencias.</span><span class="sxs-lookup"><span data-stu-id="4d672-112">Errors are different from warnings.</span></span> <span data-ttu-id="4d672-113">Los errores hacen que el compilador MIDL detenga el procesamiento del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="4d672-113">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="4d672-114">Las advertencias hacen que el compilador MIDL emita un mensaje informativo y continúe procesando el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="4d672-114">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="4d672-115">Warning-LEVEL cero (0) indica al compilador de MIDL que debe suprimir la información de advertencia.</span><span class="sxs-lookup"><span data-stu-id="4d672-115">Warning-level zero (0) directs the MIDL compiler to suppress warning information.</span></span> <span data-ttu-id="4d672-116">Cuando se combinan los modificadores **/W0** y **/WX** , el compilador MIDL suprime toda la información de advertencia.</span><span class="sxs-lookup"><span data-stu-id="4d672-116">When the **/W0** and **/WX** switches are combined, the MIDL compiler suppresses all warning information.</span></span> <span data-ttu-id="4d672-117">En este caso, el modificador **/WX** no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="4d672-117">In this case, the **/WX** switch has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="4d672-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4d672-118">Examples</span></span>

<span data-ttu-id="4d672-119">**MIDL/WX FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="4d672-119">**midl /WX filename.idl**</span></span>

<span data-ttu-id="4d672-120">**MIDL/W3/WX FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="4d672-120">**midl /W3 /WX filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="4d672-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d672-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d672-122">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="4d672-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="4d672-123">**/W**</span><span class="sxs-lookup"><span data-stu-id="4d672-123">**/W**</span></span>](-w.md)
</dt> </dl>

 

 





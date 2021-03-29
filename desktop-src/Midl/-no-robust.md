---
title: modificador/no_robust
description: El \_ conmutador/no robusto indica al compilador de MIDL que debe deshabilitar explícitamente la característica de línea de comandos de/ROBUST. El modificador de la línea de comandos de/ROBUST y sus características asociadas son la configuración predeterminada del compilador para MIDL versión 6.0.359 y versiones posteriores.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust modificador MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784307"
---
# <a name="no_robust-switch"></a><span data-ttu-id="61795-105">\_cambio sólido de/no</span><span class="sxs-lookup"><span data-stu-id="61795-105">/no\_robust switch</span></span>

<span data-ttu-id="61795-106">El conmutador **/no \_ robusto** indica al compilador de MIDL que debe deshabilitar explícitamente la característica de línea de comandos de [**/Robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="61795-106">The **/no\_robust** switch directs the MIDL compiler to explicitly disable the [**/robust**](-robust.md) command line feature.</span></span> <span data-ttu-id="61795-107">El modificador de la línea de comandos de **/Robust** y sus características asociadas son la configuración predeterminada del compilador para MIDL versión 6.0.359 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61795-107">The **/robust** command line switch and its associated features is the default compiler setting for MIDL version 6.0.359 and later.</span></span>

``` syntax
midl /no_robust
```

## <a name="switch-options"></a><span data-ttu-id="61795-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="61795-108">Switch Options</span></span>

<span data-ttu-id="61795-109">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="61795-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="61795-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61795-110">Remarks</span></span>

<span data-ttu-id="61795-111">Con la versión 6.0.359 de MIDL y versiones posteriores, el compilador MIDL establece [**/Robust**](-robust.md) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="61795-111">With MIDL version 6.0.359 and later, the MIDL compiler sets [**/robust**](-robust.md) by default.</span></span> <span data-ttu-id="61795-112">El modificador de línea de comandos de **/no \_ Robust** se debe usar para deshabilitar la característica de **/Robust** si los códigos auxiliares generados deben ejecutarse en Microsoft Windows NT, Windows 95/98 o Windows me.</span><span class="sxs-lookup"><span data-stu-id="61795-112">The **/no\_robust** command line switch must be used to disable the **/robust** feature if generated stubs need to run on Microsoft WindowsÂ NT, WindowsÂ 95/98, or WindowsÂ Me.</span></span>

## <a name="examples"></a><span data-ttu-id="61795-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="61795-113">Examples</span></span>

<span data-ttu-id="61795-114">**MIDL/no \_ Robust FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="61795-114">**midl /no\_robust filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="61795-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="61795-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61795-116">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="61795-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="61795-117">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="61795-117">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 





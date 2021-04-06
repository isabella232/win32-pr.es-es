---
title: modificador/mktyplib203
description: El modificador/mktyplib203 obliga al compilador de MIDL a analizar el archivo de entrada.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- /mktyplib203 modificador MIDL
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8fd972355c2f6d37300c60f4bf74e76bf4396
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904177"
---
# <a name="mktyplib203-switch"></a><span data-ttu-id="3a466-104">modificador/mktyplib203</span><span class="sxs-lookup"><span data-stu-id="3a466-104">/mktyplib203 switch</span></span>

<span data-ttu-id="3a466-105">El modificador **/mktyplib203** obliga al compilador de MIDL a analizar el archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="3a466-105">The **/mktyplib203** switch forces the MIDL compiler to parse the input file.</span></span>

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a><span data-ttu-id="3a466-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="3a466-106">Switch Options</span></span>

<span data-ttu-id="3a466-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3a466-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a466-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a466-108">Remarks</span></span>

<span data-ttu-id="3a466-109">Para usar el modificador **/mktyplib203** , el archivo de entrada debe seguir la sintaxis de ODL exactamente, lo que significa que no se pueden colocar instrucciones fuera del bloque de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3a466-109">In order to use the **/mktyplib203** switch, the input file must follow the ODL syntax exactly, which means you cannot place any statements outside of the library block.</span></span> <span data-ttu-id="3a466-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3a466-110">Examples</span></span>

<span data-ttu-id="3a466-111">**/mktyplib203 myoldodl. ODL de MIDL**</span><span class="sxs-lookup"><span data-stu-id="3a466-111">**midl /mktyplib203 myoldodl.odl**</span></span>

<span data-ttu-id="3a466-112">**MIDL/mktyplib203 oldhabit. idl**</span><span class="sxs-lookup"><span data-stu-id="3a466-112">**midl /mktyplib203 oldhabit.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="3a466-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a466-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a466-114">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="3a466-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="3a466-115">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="3a466-115">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 





---
title: modificador/Win64
description: El modificador/Win64 indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de 64 bits. Tenga en cuenta que este modificador está obsoleto.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- /Win64 modificador MIDL
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358026"
---
# <a name="win64-switch"></a><span data-ttu-id="7bcad-104">modificador/Win64</span><span class="sxs-lookup"><span data-stu-id="7bcad-104">/win64 switch</span></span>

<span data-ttu-id="7bcad-105">El modificador **/Win64** indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7bcad-105">The **/win64** switch directs the MIDL compiler to generate stub files, or a type library file, for a 64-bit environment.</span></span>

> [!Note]  
> <span data-ttu-id="7bcad-106">Este modificador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7bcad-106">This switch is obsolete.</span></span> <span data-ttu-id="7bcad-107">En su lugar, use el modificador [**/ia64**](-ia64.md) o [**/AMD64**](-amd64.md) .</span><span class="sxs-lookup"><span data-stu-id="7bcad-107">Please use the [**/ia64**](-ia64.md) or [**/amd64**](-amd64.md) switch instead.</span></span> <span data-ttu-id="7bcad-108">El modificador **/Win64** es equivalente al modificador **/ia64** .</span><span class="sxs-lookup"><span data-stu-id="7bcad-108">The **/win64** switch is equivalent to the **/ia64** switch.</span></span>

 

``` syntax
midl /win64
```

## <a name="switch-options"></a><span data-ttu-id="7bcad-109">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="7bcad-109">Switch Options</span></span>

<span data-ttu-id="7bcad-110">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7bcad-110">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bcad-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bcad-111">Remarks</span></span>

<span data-ttu-id="7bcad-112">El modificador **/Win64** es equivalente a establecer el modificador [**/env**](-env.md) en Win64.</span><span class="sxs-lookup"><span data-stu-id="7bcad-112">The **/win64** switch is equivalent to setting the [**/env**](-env.md) switch to win64.</span></span>

> [!Note]  
> <span data-ttu-id="7bcad-113">No es posible usar MIDL.exe para generar un TLB de 64 bits en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7bcad-113">It is not possible to use MIDL.exe to produce a 64bit tlb on Windows 2000.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="7bcad-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bcad-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bcad-115">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="7bcad-115">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="7bcad-116">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="7bcad-116">**/ia64**</span></span>](-ia64.md)
</dt> <dt>

[<span data-ttu-id="7bcad-117">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="7bcad-117">**/amd64**</span></span>](-amd64.md)
</dt> </dl>

 

 





---
title: AllMemoryBarrier función)
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a memoria.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- AllMemoryBarrier de función HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419717"
---
# <a name="allmemorybarrier-function"></a><span data-ttu-id="38edb-104">AllMemoryBarrier función)</span><span class="sxs-lookup"><span data-stu-id="38edb-104">AllMemoryBarrier function</span></span>

<span data-ttu-id="38edb-105">Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a memoria.</span><span class="sxs-lookup"><span data-stu-id="38edb-105">Blocks execution of all threads in a group until all memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="38edb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38edb-106">Syntax</span></span>

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="38edb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38edb-107">Parameters</span></span>

<span data-ttu-id="38edb-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="38edb-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38edb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38edb-109">Return value</span></span>

<span data-ttu-id="38edb-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="38edb-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38edb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38edb-111">Remarks</span></span>

<span data-ttu-id="38edb-112">Una barrera de memoria garantiza que se han completado las operaciones de memoria pendientes.</span><span class="sxs-lookup"><span data-stu-id="38edb-112">A memory barrier guarantees that outstanding memory operations have completed.</span></span> <span data-ttu-id="38edb-113">Los subprocesos se sincronizan a barreras GroupSync.</span><span class="sxs-lookup"><span data-stu-id="38edb-113">Threads are synchronized at GroupSync barriers.</span></span> <span data-ttu-id="38edb-114">Esto puede bloquear un subproceso o subprocesos si hay operaciones de memoria en curso.</span><span class="sxs-lookup"><span data-stu-id="38edb-114">This may stall a thread or threads if memory operations are in progress.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="38edb-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="38edb-115">Minimum Shader Model</span></span>

<span data-ttu-id="38edb-116">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="38edb-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="38edb-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="38edb-117">Shader Model</span></span>                                                                | <span data-ttu-id="38edb-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="38edb-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="38edb-119">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="38edb-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="38edb-120">sí</span><span class="sxs-lookup"><span data-stu-id="38edb-120">yes</span></span>       |



 

<span data-ttu-id="38edb-121">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="38edb-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="38edb-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="38edb-122">Vertex</span></span> | <span data-ttu-id="38edb-123">Casco</span><span class="sxs-lookup"><span data-stu-id="38edb-123">Hull</span></span> | <span data-ttu-id="38edb-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="38edb-124">Domain</span></span> | <span data-ttu-id="38edb-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="38edb-125">Geometry</span></span> | <span data-ttu-id="38edb-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="38edb-126">Pixel</span></span> | <span data-ttu-id="38edb-127">Compute</span><span class="sxs-lookup"><span data-stu-id="38edb-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="38edb-128">x</span><span class="sxs-lookup"><span data-stu-id="38edb-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="38edb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="38edb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38edb-130">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="38edb-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="38edb-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="38edb-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





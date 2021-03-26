---
title: DeviceMemoryBarrier función)
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a la memoria del dispositivo.
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- DeviceMemoryBarrier de función HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875b780f528000d46ba31bb979072d6d462fa91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419253"
---
# <a name="devicememorybarrier-function"></a><span data-ttu-id="6f435-104">DeviceMemoryBarrier función)</span><span class="sxs-lookup"><span data-stu-id="6f435-104">DeviceMemoryBarrier function</span></span>

<span data-ttu-id="6f435-105">Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos a la memoria del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f435-105">Blocks execution of all threads in a group until all device memory accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f435-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f435-106">Syntax</span></span>

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="6f435-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f435-107">Parameters</span></span>

<span data-ttu-id="6f435-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6f435-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f435-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f435-109">Return value</span></span>

<span data-ttu-id="6f435-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6f435-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f435-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f435-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="6f435-112">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6f435-112">Minimum Shader Model</span></span>

<span data-ttu-id="6f435-113">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6f435-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6f435-114">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6f435-114">Shader Model</span></span>                                                                | <span data-ttu-id="6f435-115">Compatible</span><span class="sxs-lookup"><span data-stu-id="6f435-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6f435-116">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="6f435-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6f435-117">sí</span><span class="sxs-lookup"><span data-stu-id="6f435-117">yes</span></span>       |



 

<span data-ttu-id="6f435-118">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6f435-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="6f435-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="6f435-119">Vertex</span></span> | <span data-ttu-id="6f435-120">Casco</span><span class="sxs-lookup"><span data-stu-id="6f435-120">Hull</span></span> | <span data-ttu-id="6f435-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="6f435-121">Domain</span></span> | <span data-ttu-id="6f435-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="6f435-122">Geometry</span></span> | <span data-ttu-id="6f435-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="6f435-123">Pixel</span></span> | <span data-ttu-id="6f435-124">Compute</span><span class="sxs-lookup"><span data-stu-id="6f435-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6f435-125">x</span><span class="sxs-lookup"><span data-stu-id="6f435-125">x</span></span>     | <span data-ttu-id="6f435-126">x</span><span class="sxs-lookup"><span data-stu-id="6f435-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6f435-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f435-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f435-128">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="6f435-128">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="6f435-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6f435-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





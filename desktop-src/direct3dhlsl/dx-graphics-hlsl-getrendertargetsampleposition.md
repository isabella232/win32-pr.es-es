---
title: GetRenderTargetSamplePosition
description: Obtiene la posición de muestreo (x, y) de un índice de ejemplo determinado.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- HLSL de GetRenderTargetSamplePosition
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0cd944b175522ab7d722ae791f3548c6633b71
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783311"
---
# <a name="getrendertargetsampleposition"></a><span data-ttu-id="d25f6-104">GetRenderTargetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="d25f6-104">GetRenderTargetSamplePosition</span></span>

<span data-ttu-id="d25f6-105">Obtiene la posición de muestreo (x, y) de un índice de ejemplo determinado.</span><span class="sxs-lookup"><span data-stu-id="d25f6-105">Gets the sampling position (x,y) for a given sample index.</span></span>



|                                                                                  |
|----------------------------------------------------------------------------------|
| <span data-ttu-id="d25f6-106">Float<2> GetRenderTargetSamplePosition (en int<1> index</span><span class="sxs-lookup"><span data-stu-id="d25f6-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span></span><br/><span data-ttu-id="d25f6-107">);</span><span class="sxs-lookup"><span data-stu-id="d25f6-107">);</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="d25f6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d25f6-108">Parameters</span></span>



| <span data-ttu-id="d25f6-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="d25f6-109">Item</span></span>                                                                                       | <span data-ttu-id="d25f6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d25f6-110">Description</span></span>                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="d25f6-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Ajustar*</span><span class="sxs-lookup"><span data-stu-id="d25f6-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span></span><br/> | <span data-ttu-id="d25f6-112">\[en \] un índice de ejemplo basado en cero.</span><span class="sxs-lookup"><span data-stu-id="d25f6-112">\[in\] A zero-based sample index.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d25f6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d25f6-113">Return Value</span></span>

<span data-ttu-id="d25f6-114">Posición (x, y) del ejemplo determinado.</span><span class="sxs-lookup"><span data-stu-id="d25f6-114">The (x,y) position of the given sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="d25f6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d25f6-115">Remarks</span></span>

<span data-ttu-id="d25f6-116">Use esta función y [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) para averiguar el número y la posición de las ubicaciones de muestreo para un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="d25f6-116">Use this function and [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="d25f6-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d25f6-117">Minimum Shader Model</span></span>

<span data-ttu-id="d25f6-118">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d25f6-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d25f6-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d25f6-119">Shader Model</span></span>                                                        | <span data-ttu-id="d25f6-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="d25f6-120">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="d25f6-121">Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="d25f6-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="d25f6-122">sí</span><span class="sxs-lookup"><span data-stu-id="d25f6-122">yes</span></span>       |
| [<span data-ttu-id="d25f6-123">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d25f6-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="d25f6-124">no</span><span class="sxs-lookup"><span data-stu-id="d25f6-124">no</span></span>        |
| [<span data-ttu-id="d25f6-125">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d25f6-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="d25f6-126">no</span><span class="sxs-lookup"><span data-stu-id="d25f6-126">no</span></span>        |
| [<span data-ttu-id="d25f6-127">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d25f6-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="d25f6-128">No</span><span class="sxs-lookup"><span data-stu-id="d25f6-128">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="d25f6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d25f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25f6-130">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d25f6-130">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 






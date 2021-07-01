---
title: GetRenderTargetSamplePosition
description: Obtiene la posición de muestreo (x,y) de un índice de ejemplo determinado.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120580"
---
# <a name="getrendertargetsampleposition"></a><span data-ttu-id="dbe08-104">GetRenderTargetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="dbe08-104">GetRenderTargetSamplePosition</span></span>

<span data-ttu-id="dbe08-105">Obtiene la posición de muestreo (x,y) de un índice de ejemplo determinado.</span><span class="sxs-lookup"><span data-stu-id="dbe08-105">Gets the sampling position (x,y) for a given sample index.</span></span>

<span data-ttu-id="dbe08-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span><span class="sxs-lookup"><span data-stu-id="dbe08-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span></span><br/><span data-ttu-id="dbe08-107">);</span><span class="sxs-lookup"><span data-stu-id="dbe08-107">);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="dbe08-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbe08-108">Parameters</span></span>



| <span data-ttu-id="dbe08-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="dbe08-109">Item</span></span>                                                                                       | <span data-ttu-id="dbe08-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbe08-110">Description</span></span>                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="dbe08-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Índice*</span><span class="sxs-lookup"><span data-stu-id="dbe08-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span></span><br/> | <span data-ttu-id="dbe08-112">\[en \] un índice de ejemplo de base cero.</span><span class="sxs-lookup"><span data-stu-id="dbe08-112">\[in\] A zero-based sample index.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="dbe08-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbe08-113">Return Value</span></span>

<span data-ttu-id="dbe08-114">Posición (x,y) del ejemplo dado.</span><span class="sxs-lookup"><span data-stu-id="dbe08-114">The (x,y) position of the given sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe08-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbe08-115">Remarks</span></span>

<span data-ttu-id="dbe08-116">Use esta función y [**GetRenderTargetSampleCount para**](dx-graphics-hlsl-getrendertargetsamplecount.md) averiguar el número y la posición de las ubicaciones de muestreo de un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="dbe08-116">Use this function and [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="dbe08-117">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="dbe08-117">Minimum Shader Model</span></span>

<span data-ttu-id="dbe08-118">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dbe08-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dbe08-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="dbe08-119">Shader Model</span></span>                                                        | <span data-ttu-id="dbe08-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="dbe08-120">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="dbe08-121">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y modelos de sombreador posteriores</span><span class="sxs-lookup"><span data-stu-id="dbe08-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="dbe08-122">Sí</span><span class="sxs-lookup"><span data-stu-id="dbe08-122">yes</span></span>       |
| [<span data-ttu-id="dbe08-123">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dbe08-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="dbe08-124">No</span><span class="sxs-lookup"><span data-stu-id="dbe08-124">no</span></span>        |
| [<span data-ttu-id="dbe08-125">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dbe08-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="dbe08-126">No</span><span class="sxs-lookup"><span data-stu-id="dbe08-126">no</span></span>        |
| [<span data-ttu-id="dbe08-127">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dbe08-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="dbe08-128">No</span><span class="sxs-lookup"><span data-stu-id="dbe08-128">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="dbe08-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbe08-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe08-130">**Funciones intrínsecas (HLSL de DirectX)**</span><span class="sxs-lookup"><span data-stu-id="dbe08-130">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 






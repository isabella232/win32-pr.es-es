---
title: 'ConsumeStructuredBuffer:: consume (función)'
description: Quita un valor del final del búfer.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Usar HLSL de función
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104076995"
---
# <a name="consume-function"></a><span data-ttu-id="cff4a-104">Consume (función)</span><span class="sxs-lookup"><span data-stu-id="cff4a-104">Consume function</span></span>

<span data-ttu-id="cff4a-105">Quita un valor del final del búfer.</span><span class="sxs-lookup"><span data-stu-id="cff4a-105">Removes a value from the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff4a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cff4a-106">Syntax</span></span>

``` syntax
T Consume(void);
```

## <a name="parameters"></a><span data-ttu-id="cff4a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cff4a-107">Parameters</span></span>

<span data-ttu-id="cff4a-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cff4a-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cff4a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cff4a-109">Return value</span></span>

<span data-ttu-id="cff4a-110">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="cff4a-110">Type: **T**</span></span>

<span data-ttu-id="cff4a-111">El valor quitado (puede ser una estructura).</span><span class="sxs-lookup"><span data-stu-id="cff4a-111">The value removed (can be a structure).</span></span>

## <a name="remarks"></a><span data-ttu-id="cff4a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cff4a-112">Remarks</span></span>

<span data-ttu-id="cff4a-113">T puede ser cualquier tipo de datos, incluida una estructura.</span><span class="sxs-lookup"><span data-stu-id="cff4a-113">T can be any data type including a structure.</span></span>

<span data-ttu-id="cff4a-114">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="cff4a-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cff4a-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="cff4a-115">Vertex</span></span> | <span data-ttu-id="cff4a-116">Casco</span><span class="sxs-lookup"><span data-stu-id="cff4a-116">Hull</span></span> | <span data-ttu-id="cff4a-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="cff4a-117">Domain</span></span> | <span data-ttu-id="cff4a-118">Geometría</span><span class="sxs-lookup"><span data-stu-id="cff4a-118">Geometry</span></span> | <span data-ttu-id="cff4a-119">Píxel</span><span class="sxs-lookup"><span data-stu-id="cff4a-119">Pixel</span></span> | <span data-ttu-id="cff4a-120">Compute</span><span class="sxs-lookup"><span data-stu-id="cff4a-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cff4a-121">x</span><span class="sxs-lookup"><span data-stu-id="cff4a-121">x</span></span>      | <span data-ttu-id="cff4a-122">x</span><span class="sxs-lookup"><span data-stu-id="cff4a-122">x</span></span>    | <span data-ttu-id="cff4a-123">x</span><span class="sxs-lookup"><span data-stu-id="cff4a-123">x</span></span>      | <span data-ttu-id="cff4a-124">x</span><span class="sxs-lookup"><span data-stu-id="cff4a-124">x</span></span>        | <span data-ttu-id="cff4a-125">x</span><span class="sxs-lookup"><span data-stu-id="cff4a-125">x</span></span>     | <span data-ttu-id="cff4a-126">x</span><span class="sxs-lookup"><span data-stu-id="cff4a-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cff4a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cff4a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff4a-128">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="cff4a-128">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="cff4a-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="cff4a-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





---
title: 'Texture2DMS:: GetSamplePosition (función)'
description: Devuelve la posición de ejemplo para el índice de ejemplo proporcionado.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- GetSamplePosition de función HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533711"
---
# <a name="texture2dmsgetsampleposition-function"></a><span data-ttu-id="c306f-104">Texture2DMS:: GetSamplePosition (función)</span><span class="sxs-lookup"><span data-stu-id="c306f-104">Texture2DMS::GetSamplePosition function</span></span>

<span data-ttu-id="c306f-105">Devuelve la posición de ejemplo para el índice de ejemplo proporcionado.</span><span class="sxs-lookup"><span data-stu-id="c306f-105">Returns the sample position for the sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="c306f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c306f-106">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="c306f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c306f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c306f-108">*sampleindex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c306f-108">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c306f-109">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c306f-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c306f-110">Índice de base cero de una ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c306f-110">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c306f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c306f-111">Return value</span></span>

<span data-ttu-id="c306f-112">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="c306f-112">Type: **float2**</span></span>

<span data-ttu-id="c306f-113">Una ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c306f-113">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="c306f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c306f-114">Remarks</span></span>

<span data-ttu-id="c306f-115">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c306f-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c306f-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="c306f-116">Vertex</span></span> | <span data-ttu-id="c306f-117">Casco</span><span class="sxs-lookup"><span data-stu-id="c306f-117">Hull</span></span> | <span data-ttu-id="c306f-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="c306f-118">Domain</span></span> | <span data-ttu-id="c306f-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="c306f-119">Geometry</span></span> | <span data-ttu-id="c306f-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="c306f-120">Pixel</span></span> | <span data-ttu-id="c306f-121">Compute</span><span class="sxs-lookup"><span data-stu-id="c306f-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c306f-122">x</span><span class="sxs-lookup"><span data-stu-id="c306f-122">x</span></span>      | <span data-ttu-id="c306f-123">x</span><span class="sxs-lookup"><span data-stu-id="c306f-123">x</span></span>    | <span data-ttu-id="c306f-124">x</span><span class="sxs-lookup"><span data-stu-id="c306f-124">x</span></span>      | <span data-ttu-id="c306f-125">x</span><span class="sxs-lookup"><span data-stu-id="c306f-125">x</span></span>        | <span data-ttu-id="c306f-126">x</span><span class="sxs-lookup"><span data-stu-id="c306f-126">x</span></span>     | <span data-ttu-id="c306f-127">x</span><span class="sxs-lookup"><span data-stu-id="c306f-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c306f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c306f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c306f-129">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="c306f-129">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="c306f-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c306f-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

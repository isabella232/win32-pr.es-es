---
title: 'Texture2DMSArray:: GetSamplePosition (función)'
description: 'Obtiene la posición del ejemplo especificado. | Texture2DMSArray:: GetSamplePosition (función)'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
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
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280186"
---
# <a name="texture2dmsarraygetsampleposition-function"></a><span data-ttu-id="dc2cc-105">Texture2DMSArray:: GetSamplePosition (función)</span><span class="sxs-lookup"><span data-stu-id="dc2cc-105">Texture2DMSArray::GetSamplePosition function</span></span>

<span data-ttu-id="dc2cc-106">Obtiene la posición del ejemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="dc2cc-106">Gets the position of the specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc2cc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc2cc-107">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="dc2cc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc2cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc2cc-109">*sampleindex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc2cc-109">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc2cc-110">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc2cc-110">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dc2cc-111">Índice de base cero de una ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="dc2cc-111">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc2cc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc2cc-112">Return value</span></span>

<span data-ttu-id="dc2cc-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="dc2cc-113">Type: **float2**</span></span>

<span data-ttu-id="dc2cc-114">Una ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="dc2cc-114">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc2cc-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc2cc-115">Remarks</span></span>

<span data-ttu-id="dc2cc-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="dc2cc-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="dc2cc-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="dc2cc-117">Vertex</span></span> | <span data-ttu-id="dc2cc-118">Casco</span><span class="sxs-lookup"><span data-stu-id="dc2cc-118">Hull</span></span> | <span data-ttu-id="dc2cc-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="dc2cc-119">Domain</span></span> | <span data-ttu-id="dc2cc-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="dc2cc-120">Geometry</span></span> | <span data-ttu-id="dc2cc-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="dc2cc-121">Pixel</span></span> | <span data-ttu-id="dc2cc-122">Compute</span><span class="sxs-lookup"><span data-stu-id="dc2cc-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="dc2cc-123">x</span><span class="sxs-lookup"><span data-stu-id="dc2cc-123">x</span></span>      | <span data-ttu-id="dc2cc-124">x</span><span class="sxs-lookup"><span data-stu-id="dc2cc-124">x</span></span>    | <span data-ttu-id="dc2cc-125">x</span><span class="sxs-lookup"><span data-stu-id="dc2cc-125">x</span></span>      | <span data-ttu-id="dc2cc-126">x</span><span class="sxs-lookup"><span data-stu-id="dc2cc-126">x</span></span>        | <span data-ttu-id="dc2cc-127">x</span><span class="sxs-lookup"><span data-stu-id="dc2cc-127">x</span></span>     | <span data-ttu-id="dc2cc-128">x</span><span class="sxs-lookup"><span data-stu-id="dc2cc-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dc2cc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc2cc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc2cc-130">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="dc2cc-130">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="dc2cc-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="dc2cc-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

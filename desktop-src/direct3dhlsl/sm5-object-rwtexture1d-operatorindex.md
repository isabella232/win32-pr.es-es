---
title: 'RWTexture1D:: Operator (función)'
description: 'Devuelve una variable de recurso. | RWTexture1D:: Operator (función)'
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
keywords:
- Función de operador HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547510"
---
# <a name="rwtexture1doperator--function"></a><span data-ttu-id="18472-105">RWTexture1D:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="18472-105">RWTexture1D::Operator  function</span></span>

<span data-ttu-id="18472-106">Devuelve una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="18472-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="18472-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18472-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="18472-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18472-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18472-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="18472-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18472-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="18472-110">Type: **uint**</span></span>

<span data-ttu-id="18472-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="18472-111">The index position.</span></span> <span data-ttu-id="18472-112">Contiene la coordenada x.</span><span class="sxs-lookup"><span data-stu-id="18472-112">Contains the x coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18472-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18472-113">Return value</span></span>

<span data-ttu-id="18472-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="18472-114">Type: **R**</span></span>

<span data-ttu-id="18472-115">Variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="18472-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="18472-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18472-116">Remarks</span></span>

<span data-ttu-id="18472-117">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="18472-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="18472-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="18472-118">Vertex</span></span> | <span data-ttu-id="18472-119">Casco</span><span class="sxs-lookup"><span data-stu-id="18472-119">Hull</span></span> | <span data-ttu-id="18472-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="18472-120">Domain</span></span> | <span data-ttu-id="18472-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="18472-121">Geometry</span></span> | <span data-ttu-id="18472-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="18472-122">Pixel</span></span> | <span data-ttu-id="18472-123">Compute</span><span class="sxs-lookup"><span data-stu-id="18472-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="18472-124">x</span><span class="sxs-lookup"><span data-stu-id="18472-124">x</span></span>     | <span data-ttu-id="18472-125">x</span><span class="sxs-lookup"><span data-stu-id="18472-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="18472-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="18472-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18472-127">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="18472-127">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="18472-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="18472-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





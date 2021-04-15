---
title: 'RWTexture3D:: Operator (función)'
description: Devuelve una variable de recurso de un RWTexture3D.
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
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
ms.openlocfilehash: e41ff4db387c4d0926083419082fd589005d96a6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104984127"
---
# <a name="rwtexture3doperator--function"></a><span data-ttu-id="e8c41-104">RWTexture3D:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="e8c41-104">RWTexture3D::Operator  function</span></span>

<span data-ttu-id="e8c41-105">Devuelve una variable de recurso de un [**RWTexture3D**](sm5-object-rwtexture3d.md).</span><span class="sxs-lookup"><span data-stu-id="e8c41-105">Returns a resource variable of a [**RWTexture3D**](sm5-object-rwtexture3d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c41-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8c41-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="e8c41-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8c41-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c41-108">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e8c41-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c41-109">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="e8c41-109">Type: **uint3**</span></span>

<span data-ttu-id="e8c41-110">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="e8c41-110">The index position.</span></span> <span data-ttu-id="e8c41-111">Contiene las coordenadas (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="e8c41-111">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c41-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8c41-112">Return value</span></span>

<span data-ttu-id="e8c41-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="e8c41-113">Type: **R**</span></span>

<span data-ttu-id="e8c41-114">Variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="e8c41-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c41-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8c41-115">Remarks</span></span>

<span data-ttu-id="e8c41-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e8c41-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e8c41-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="e8c41-117">Vertex</span></span> | <span data-ttu-id="e8c41-118">Casco</span><span class="sxs-lookup"><span data-stu-id="e8c41-118">Hull</span></span> | <span data-ttu-id="e8c41-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="e8c41-119">Domain</span></span> | <span data-ttu-id="e8c41-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="e8c41-120">Geometry</span></span> | <span data-ttu-id="e8c41-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="e8c41-121">Pixel</span></span> | <span data-ttu-id="e8c41-122">Compute</span><span class="sxs-lookup"><span data-stu-id="e8c41-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e8c41-123">x</span><span class="sxs-lookup"><span data-stu-id="e8c41-123">x</span></span>     | <span data-ttu-id="e8c41-124">x</span><span class="sxs-lookup"><span data-stu-id="e8c41-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e8c41-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8c41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c41-126">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="e8c41-126">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="e8c41-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e8c41-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





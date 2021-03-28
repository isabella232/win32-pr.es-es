---
title: 'Texture2DMS:: Operator (función)'
description: Recupera un valor del recurso en la ubicación proporcionada en el índice de ejemplo 0.
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
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
ms.openlocfilehash: 6ae7976e6871dc2547ed5c372e1551e5bf0ca148
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104984139"
---
# <a name="texture2dmsoperator--function"></a><span data-ttu-id="48498-104">Texture2DMS:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="48498-104">Texture2DMS::Operator  function</span></span>

<span data-ttu-id="48498-105">Recupera un valor del recurso en la ubicación proporcionada en el índice de ejemplo 0.</span><span class="sxs-lookup"><span data-stu-id="48498-105">Retrieves a value from the resource at the location provided at sample index 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="48498-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48498-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="48498-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48498-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48498-108">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="48498-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48498-109">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="48498-109">Type: **uint2**</span></span>

<span data-ttu-id="48498-110">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="48498-110">The index position.</span></span> <span data-ttu-id="48498-111">Contiene las coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="48498-111">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48498-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48498-112">Return value</span></span>

<span data-ttu-id="48498-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="48498-113">Type: **R**</span></span>

<span data-ttu-id="48498-114">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="48498-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="48498-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48498-115">Remarks</span></span>

<span data-ttu-id="48498-116">Para seleccionar un ejemplo determinado, consulte el [**ejemplo. \[Operador \] . \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="48498-116">To select a particular sample, refer to [**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md).</span></span>

<span data-ttu-id="48498-117">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="48498-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="48498-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="48498-118">Vertex</span></span> | <span data-ttu-id="48498-119">Casco</span><span class="sxs-lookup"><span data-stu-id="48498-119">Hull</span></span> | <span data-ttu-id="48498-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="48498-120">Domain</span></span> | <span data-ttu-id="48498-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="48498-121">Geometry</span></span> | <span data-ttu-id="48498-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="48498-122">Pixel</span></span> | <span data-ttu-id="48498-123">Compute</span><span class="sxs-lookup"><span data-stu-id="48498-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="48498-124">x</span><span class="sxs-lookup"><span data-stu-id="48498-124">x</span></span>      | <span data-ttu-id="48498-125">x</span><span class="sxs-lookup"><span data-stu-id="48498-125">x</span></span>    | <span data-ttu-id="48498-126">x</span><span class="sxs-lookup"><span data-stu-id="48498-126">x</span></span>      | <span data-ttu-id="48498-127">x</span><span class="sxs-lookup"><span data-stu-id="48498-127">x</span></span>        | <span data-ttu-id="48498-128">x</span><span class="sxs-lookup"><span data-stu-id="48498-128">x</span></span>     | <span data-ttu-id="48498-129">x</span><span class="sxs-lookup"><span data-stu-id="48498-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="48498-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="48498-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48498-131">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="48498-131">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="48498-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="48498-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





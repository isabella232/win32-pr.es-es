---
title: EvaluateAttributeAtCentroid función)
description: Evalúa en el píxel centroide.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- EvaluateAttributeAtCentroid de función HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419574"
---
# <a name="evaluateattributeatcentroid-function"></a><span data-ttu-id="65493-104">EvaluateAttributeAtCentroid función)</span><span class="sxs-lookup"><span data-stu-id="65493-104">EvaluateAttributeAtCentroid function</span></span>

<span data-ttu-id="65493-105">Evalúa en el píxel centroide.</span><span class="sxs-lookup"><span data-stu-id="65493-105">Evaluates at the pixel centroid.</span></span>

## <a name="syntax"></a><span data-ttu-id="65493-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65493-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a><span data-ttu-id="65493-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65493-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65493-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="65493-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65493-109">Tipo: **attrib Numeric**</span><span class="sxs-lookup"><span data-stu-id="65493-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="65493-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="65493-110">The input value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65493-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65493-111">Remarks</span></span>

<span data-ttu-id="65493-112">El modo de interpolación puede ser **lineal** o **lineal \_ sin \_ perspectiva** en la variable.</span><span class="sxs-lookup"><span data-stu-id="65493-112">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="65493-113">Se omite el uso de **centroide** o **Sample** .</span><span class="sxs-lookup"><span data-stu-id="65493-113">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="65493-114">También se permiten atributos con interpolación constante, en cuyo caso se omite el índice de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="65493-114">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="65493-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="65493-115">Minimum Shader Model</span></span>

<span data-ttu-id="65493-116">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="65493-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="65493-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="65493-117">Shader Model</span></span>                                                                | <span data-ttu-id="65493-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="65493-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="65493-119">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="65493-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="65493-120">sí</span><span class="sxs-lookup"><span data-stu-id="65493-120">yes</span></span>       |



 

<span data-ttu-id="65493-121">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="65493-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="65493-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="65493-122">Vertex</span></span> | <span data-ttu-id="65493-123">Casco</span><span class="sxs-lookup"><span data-stu-id="65493-123">Hull</span></span> | <span data-ttu-id="65493-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="65493-124">Domain</span></span> | <span data-ttu-id="65493-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="65493-125">Geometry</span></span> | <span data-ttu-id="65493-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="65493-126">Pixel</span></span> | <span data-ttu-id="65493-127">Compute</span><span class="sxs-lookup"><span data-stu-id="65493-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="65493-128">x</span><span class="sxs-lookup"><span data-stu-id="65493-128">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="65493-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="65493-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65493-130">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="65493-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="65493-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="65493-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





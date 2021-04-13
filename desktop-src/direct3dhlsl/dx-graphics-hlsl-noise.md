---
title: noise
description: Genera un valor aleatorio mediante el algoritmo Perlen-Noise.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- HLSL de ruido
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421645"
---
# <a name="noise"></a><span data-ttu-id="abcfb-104">noise</span><span class="sxs-lookup"><span data-stu-id="abcfb-104">noise</span></span>

<span data-ttu-id="abcfb-105">Genera un valor aleatorio mediante el algoritmo Perlen-Noise.</span><span class="sxs-lookup"><span data-stu-id="abcfb-105">Generates a random value using the Perlin-noise algorithm.</span></span>




| <span data-ttu-id="abcfb-106">*RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="abcfb-106">*ret* noise(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="abcfb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abcfb-107">Parameters</span></span>



| <span data-ttu-id="abcfb-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="abcfb-108">Item</span></span>                                                   | <span data-ttu-id="abcfb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="abcfb-109">Description</span></span>                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="abcfb-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="abcfb-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="abcfb-111">\[en \] un vector de punto flotante a partir del cual se generará el ruido de Perl.</span><span class="sxs-lookup"><span data-stu-id="abcfb-111">\[in\] A floating-point vector from which to generate Perlin noise.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="abcfb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abcfb-112">Return Value</span></span>

<span data-ttu-id="abcfb-113">Valor de ruido de Perlen dentro de un intervalo entre-1 y 1.</span><span class="sxs-lookup"><span data-stu-id="abcfb-113">The Perlin noise value within a range between -1 and 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="abcfb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abcfb-114">Remarks</span></span>

<span data-ttu-id="abcfb-115">Los valores de ruido de Perlen cambian sin problemas de un punto a otro en un espacio, lo que crea valores de aspecto natural y generados de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="abcfb-115">Perlin noise values change smoothly from one point to another over a space, creating natural looking, randomly generated values.</span></span> <span data-ttu-id="abcfb-116">Puede usar Perlen ruido para generar texturas de procedimientos para efectos como humo y fuego.</span><span class="sxs-lookup"><span data-stu-id="abcfb-116">You can use Perlin noise to generate procedural textures for effects like smoke and fire.</span></span>

## <a name="type-description"></a><span data-ttu-id="abcfb-117">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="abcfb-117">Type Description</span></span>



| <span data-ttu-id="abcfb-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="abcfb-118">Name</span></span>  | [<span data-ttu-id="abcfb-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="abcfb-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="abcfb-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="abcfb-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="abcfb-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="abcfb-121">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="abcfb-122">*x*</span><span class="sxs-lookup"><span data-stu-id="abcfb-122">*x*</span></span>   | [<span data-ttu-id="abcfb-123">**medios**</span><span class="sxs-lookup"><span data-stu-id="abcfb-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="abcfb-124">**flot**</span><span class="sxs-lookup"><span data-stu-id="abcfb-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="abcfb-125">cualquiera</span><span class="sxs-lookup"><span data-stu-id="abcfb-125">any</span></span>  |
| <span data-ttu-id="abcfb-126">*direcc*</span><span class="sxs-lookup"><span data-stu-id="abcfb-126">*ret*</span></span> | [<span data-ttu-id="abcfb-127">**escalar**</span><span class="sxs-lookup"><span data-stu-id="abcfb-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="abcfb-128">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="abcfb-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="abcfb-129">1</span><span class="sxs-lookup"><span data-stu-id="abcfb-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="abcfb-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="abcfb-130">Minimum Shader Model</span></span>

<span data-ttu-id="abcfb-131">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="abcfb-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="abcfb-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="abcfb-132">Shader Model</span></span>                                                                       | <span data-ttu-id="abcfb-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="abcfb-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="abcfb-134">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="abcfb-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="abcfb-135">no</span><span class="sxs-lookup"><span data-stu-id="abcfb-135">no</span></span>                  |
| [<span data-ttu-id="abcfb-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="abcfb-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="abcfb-137">sí ( \_ solo TX 1 \_ 0)</span><span class="sxs-lookup"><span data-stu-id="abcfb-137">yes (tx\_1\_0 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="abcfb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="abcfb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abcfb-139">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="abcfb-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


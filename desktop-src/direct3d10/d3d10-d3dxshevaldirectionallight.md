---
description: 'Función D3DXSHEvalDirectionalLight (D3DX10.h): evalúa una luz direccional y devuelve datos esféricos esféricos (SH).'
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: Función D3DXSHEvalDirectionalLight (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 551dad8081af2b0138be4758682d5a660f621141
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108603"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a><span data-ttu-id="43ec4-103">Función D3DXSHEvalDirectionalLight (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="43ec4-103">D3DXSHEvalDirectionalLight function (D3DX10.h)</span></span>

<span data-ttu-id="43ec4-104">Evalúa una luz direccional y devuelve datos esféricos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="43ec4-104">Evaluates a directional light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ec4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43ec4-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="43ec4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43ec4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ec4-107">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43ec4-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ec4-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43ec4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43ec4-109">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="43ec4-109">Order of the SH evaluation.</span></span> <span data-ttu-id="43ec4-110">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="43ec4-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="43ec4-111">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="43ec4-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="43ec4-112">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="43ec4-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="43ec4-113">*pDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43ec4-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ec4-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="43ec4-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="43ec4-115">Puntero al vector de dirección del eje del hemisferio (x, y, z) en el que se evalúan las funciones de base sh.</span><span class="sxs-lookup"><span data-stu-id="43ec4-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="43ec4-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="43ec4-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="43ec4-117">*RIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43ec4-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ec4-118">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43ec4-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43ec4-119">Intensidad roja de la luz.</span><span class="sxs-lookup"><span data-stu-id="43ec4-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="43ec4-120">*GIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43ec4-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ec4-121">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43ec4-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43ec4-122">Intensidad verde de la luz.</span><span class="sxs-lookup"><span data-stu-id="43ec4-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="43ec4-123">*BIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43ec4-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ec4-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43ec4-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43ec4-125">Intensidad azul de la luz.</span><span class="sxs-lookup"><span data-stu-id="43ec4-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="43ec4-126">*pROut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43ec4-126">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ec4-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43ec4-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43ec4-128">Puntero al vector SH de salida para el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="43ec4-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="43ec4-129">*pGOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43ec4-129">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ec4-130">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43ec4-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43ec4-131">Puntero opcional al vector SH de salida para el componente verde.</span><span class="sxs-lookup"><span data-stu-id="43ec4-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="43ec4-132">*pBOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43ec4-132">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ec4-133">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43ec4-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43ec4-134">Puntero opcional al vector SH de salida para el componente azul.</span><span class="sxs-lookup"><span data-stu-id="43ec4-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ec4-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43ec4-135">Return value</span></span>

<span data-ttu-id="43ec4-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43ec4-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43ec4-137">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43ec4-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="43ec4-138">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="43ec4-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="43ec4-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43ec4-139">Remarks</span></span>

<span data-ttu-id="43ec4-140">El vector de salida se calcula de modo que si la relación de intensidad R/G/B es igual a 1, el resultado de la radiación de salida de un punto directamente debajo de la luz en un objeto difuso con un albedo de 1 sería 1,0.</span><span class="sxs-lookup"><span data-stu-id="43ec4-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="43ec4-141">Esto calculará tres ejemplos espectrales; se devolverá pROut, mientras que se pueden devolver pGOut y pBOut.</span><span class="sxs-lookup"><span data-stu-id="43ec4-141">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="43ec4-142">En la esfera con radio de unidad, como se muestra en la ilustración siguiente, la dirección se puede especificar simplemente con theta, el ángulo sobre el eje Z en la dirección de la derecha y el ángulo de z.</span><span class="sxs-lookup"><span data-stu-id="43ec4-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="43ec4-144">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (theta, phi) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="43ec4-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="43ec4-145">El ángulo de theta varía en el intervalo de 0 a 2 pi, mientras que el de phi varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="43ec4-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="43ec4-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43ec4-147">Requirements</span></span>



| <span data-ttu-id="43ec4-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="43ec4-148">Requirement</span></span> | <span data-ttu-id="43ec4-149">Value</span><span class="sxs-lookup"><span data-stu-id="43ec4-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43ec4-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43ec4-150">Header</span></span><br/>  | <dl> <span data-ttu-id="43ec4-151"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="43ec4-151"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="43ec4-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43ec4-152">Library</span></span><br/> | <dl> <span data-ttu-id="43ec4-153"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="43ec4-153"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43ec4-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="43ec4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ec4-155">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="43ec4-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

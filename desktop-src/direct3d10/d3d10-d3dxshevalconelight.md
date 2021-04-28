---
description: 'Función D3DXSHEvalConeLight (D3DX10.h): evalúa una luz que es un cono de intensidad constante y devuelve datos de armónica esférica esférica (SH).'
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: Función D3DXSHEvalConeLight (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fc11e7bab4cbbd6c8a685b289d4bde476cd465ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108613"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a><span data-ttu-id="4de53-103">Función D3DXSHEvalConeLight (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="4de53-103">D3DXSHEvalConeLight function (D3DX10.h)</span></span>

<span data-ttu-id="4de53-104">Evalúa una luz que es un cono de intensidad constante y devuelve datos esféricos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="4de53-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4de53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4de53-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="4de53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4de53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4de53-107">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4de53-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de53-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4de53-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4de53-109">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="4de53-109">Order of the SH evaluation.</span></span> <span data-ttu-id="4de53-110">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="4de53-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="4de53-111">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="4de53-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="4de53-112">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="4de53-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="4de53-113">*pDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4de53-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de53-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4de53-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4de53-115">Puntero al vector de dirección del eje del hemisferio (x, y, z) en el que se evalúan las funciones de base sh.</span><span class="sxs-lookup"><span data-stu-id="4de53-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="4de53-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4de53-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4de53-117">*Radio* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4de53-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de53-118">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4de53-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4de53-119">Radio de cono en radianes.</span><span class="sxs-lookup"><span data-stu-id="4de53-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="4de53-120">*RIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4de53-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de53-121">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4de53-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4de53-122">Intensidad roja de la luz.</span><span class="sxs-lookup"><span data-stu-id="4de53-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="4de53-123">*GIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4de53-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de53-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4de53-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4de53-125">Intensidad verde de la luz.</span><span class="sxs-lookup"><span data-stu-id="4de53-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="4de53-126">*BIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4de53-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de53-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4de53-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4de53-128">Intensidad azul de la luz.</span><span class="sxs-lookup"><span data-stu-id="4de53-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="4de53-129">*pROut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4de53-129">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de53-130">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4de53-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4de53-131">Puntero al vector SH de salida para el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="4de53-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="4de53-132">*pGOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4de53-132">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de53-133">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4de53-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4de53-134">Puntero al vector SH de salida para el componente verde.</span><span class="sxs-lookup"><span data-stu-id="4de53-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="4de53-135">*pBOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4de53-135">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de53-136">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4de53-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4de53-137">Puntero al vector SH de salida para el componente azul.</span><span class="sxs-lookup"><span data-stu-id="4de53-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4de53-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4de53-138">Return value</span></span>

<span data-ttu-id="4de53-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4de53-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4de53-140">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4de53-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4de53-141">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4de53-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4de53-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4de53-142">Remarks</span></span>

<span data-ttu-id="4de53-143">Evalúa una luz que es un cono de intensidad constante y devuelve datos sh espectrales.</span><span class="sxs-lookup"><span data-stu-id="4de53-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="4de53-144">El vector de salida se calcula de modo que si la relación de intensidad R/G/B es igual a 1, la intensidad de salida de un punto directamente debajo de la luz (orientada en la dirección del cono en un objeto difuso con un albedo de 1) sería 1,0.</span><span class="sxs-lookup"><span data-stu-id="4de53-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="4de53-145">Esto calculará tres ejemplos espectrales; se devolverá pROut, mientras que se pueden devolver pGOut y pBOut.</span><span class="sxs-lookup"><span data-stu-id="4de53-145">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="4de53-146">En la esfera con radio de unidad, como se muestra en la ilustración siguiente, la dirección se puede especificar simplemente con theta, el ángulo sobre el eje Z en la dirección derecha y el ángulo de la z.</span><span class="sxs-lookup"><span data-stu-id="4de53-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="4de53-148">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (theta, phi) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="4de53-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="4de53-149">El ángulo de theta varía en el intervalo de 0 a 2 pi, mientras que phi varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="4de53-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="4de53-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4de53-151">Requirements</span></span>



| <span data-ttu-id="4de53-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="4de53-152">Requirement</span></span> | <span data-ttu-id="4de53-153">Value</span><span class="sxs-lookup"><span data-stu-id="4de53-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4de53-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4de53-154">Header</span></span><br/>  | <dl> <span data-ttu-id="4de53-155"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="4de53-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4de53-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4de53-156">Library</span></span><br/> | <dl> <span data-ttu-id="4de53-157"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4de53-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de53-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4de53-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de53-159">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="4de53-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

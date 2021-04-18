---
description: Evalúa una luz que es un cono de intensidad constante y devuelve datos armónicos esféricos (SH).
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: Función D3DXSHEvalConeLight (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2400fe0430e008ea1b704ee4daef51eeee7bd7a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104550776"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a><span data-ttu-id="31b41-103">Función D3DXSHEvalConeLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="31b41-103">D3DXSHEvalConeLight function (D3dx9math.h)</span></span>

<span data-ttu-id="31b41-104">Evalúa una luz que es un cono de intensidad constante y devuelve datos armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="31b41-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31b41-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="31b41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31b41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b41-107">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="31b41-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b41-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31b41-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31b41-109">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="31b41-109">Order of the SH evaluation.</span></span> <span data-ttu-id="31b41-110">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="31b41-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="31b41-111">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="31b41-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="31b41-112">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="31b41-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="31b41-113">*pDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31b41-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b41-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="31b41-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="31b41-115">Puntero al vector de dirección del eje hemisferio (x, y, z) en el que se van a evaluar las funciones de base de SH.</span><span class="sxs-lookup"><span data-stu-id="31b41-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="31b41-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="31b41-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="31b41-117">*RADIUS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31b41-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b41-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31b41-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31b41-119">Radio del cono en radianes.</span><span class="sxs-lookup"><span data-stu-id="31b41-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="31b41-120">*RIntensity* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31b41-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b41-121">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31b41-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31b41-122">Intensidad roja de la luz.</span><span class="sxs-lookup"><span data-stu-id="31b41-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="31b41-123">*GIntensity* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31b41-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b41-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31b41-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31b41-125">Intensidad verde de la luz.</span><span class="sxs-lookup"><span data-stu-id="31b41-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="31b41-126">*BIntensity* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31b41-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b41-127">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31b41-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31b41-128">Intensidad azul de la luz.</span><span class="sxs-lookup"><span data-stu-id="31b41-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="31b41-129">*pROut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31b41-129">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31b41-130">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31b41-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31b41-131">Puntero al vector SH de salida para el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="31b41-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="31b41-132">*pGOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31b41-132">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31b41-133">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31b41-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31b41-134">Puntero al vector SH de salida del componente verde.</span><span class="sxs-lookup"><span data-stu-id="31b41-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="31b41-135">*pBOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31b41-135">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31b41-136">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31b41-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31b41-137">Puntero al vector SH de salida para el componente azul.</span><span class="sxs-lookup"><span data-stu-id="31b41-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b41-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31b41-138">Return value</span></span>

<span data-ttu-id="31b41-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31b41-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31b41-140">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31b41-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="31b41-141">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="31b41-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="31b41-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31b41-142">Remarks</span></span>

<span data-ttu-id="31b41-143">Evalúa una luz que es un cono de intensidad constante y devuelve datos de SH espectrales.</span><span class="sxs-lookup"><span data-stu-id="31b41-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="31b41-144">El vector de salida se calcula de modo que si la relación de intensidad R/G/B es igual a 1, el Radiance de salida de un punto directamente bajo la luz (orientada en la dirección del cono en un objeto difuso con un albedo de 1) sería 1,0.</span><span class="sxs-lookup"><span data-stu-id="31b41-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="31b41-145">Se calcularán tres muestras espectrales; se devolverá *pROut* , mientras que *pGOut* y *pBOut* se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="31b41-145">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="31b41-146">En la esfera con radio de unidad, tal y como se muestra en la siguiente ilustración, la dirección se puede especificar simplemente con Theta, el ángulo del eje z en la dirección de la [mano derecha](coordinate-systems.md)y la PHI, el ángulo de z.</span><span class="sxs-lookup"><span data-stu-id="31b41-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="31b41-148">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (Theta, PHI) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="31b41-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="31b41-149">El ángulo Zeta varía en el intervalo de 0 a 2 PI, mientras que la PHI varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="31b41-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre las coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="31b41-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31b41-151">Requirements</span></span>



| <span data-ttu-id="31b41-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="31b41-152">Requirement</span></span> | <span data-ttu-id="31b41-153">Value</span><span class="sxs-lookup"><span data-stu-id="31b41-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31b41-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31b41-154">Header</span></span><br/>  | <dl> <span data-ttu-id="31b41-155"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b41-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="31b41-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31b41-156">Library</span></span><br/> | <dl> <span data-ttu-id="31b41-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31b41-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31b41-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="31b41-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b41-159">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="31b41-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="31b41-160">Transferencia Radiance precalculada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="31b41-160">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 

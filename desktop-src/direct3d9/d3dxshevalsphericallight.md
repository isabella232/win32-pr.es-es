---
description: Evalúa una luz esférica y devuelve datos armónicos esféricos (SH).
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: Función D3DXSHEvalSphericalLight (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8581b4284e270b6df587be1a71fcf11f29c843d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362523"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a><span data-ttu-id="7fb45-103">Función D3DXSHEvalSphericalLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7fb45-103">D3DXSHEvalSphericalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="7fb45-104">Evalúa una luz esférica y devuelve datos armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="7fb45-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fb45-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fb45-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pPos,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="7fb45-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fb45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fb45-107">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7fb45-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb45-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb45-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7fb45-109">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="7fb45-109">Order of the SH evaluation.</span></span> <span data-ttu-id="7fb45-110">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="7fb45-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="7fb45-111">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="7fb45-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="7fb45-112">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="7fb45-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="7fb45-113">*pPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7fb45-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb45-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7fb45-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7fb45-115">Puntero a la posición de la luz.</span><span class="sxs-lookup"><span data-stu-id="7fb45-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="7fb45-116">*RADIUS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7fb45-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb45-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb45-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7fb45-118">Radio de la fuente de luz esférica.</span><span class="sxs-lookup"><span data-stu-id="7fb45-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="7fb45-119">*RIntensity* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7fb45-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb45-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb45-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7fb45-121">Intensidad roja de la luz.</span><span class="sxs-lookup"><span data-stu-id="7fb45-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="7fb45-122">*GIntensity* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7fb45-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb45-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb45-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7fb45-124">Intensidad verde de la luz.</span><span class="sxs-lookup"><span data-stu-id="7fb45-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="7fb45-125">*BIntensity* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7fb45-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb45-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb45-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7fb45-127">Intensidad azul de la luz.</span><span class="sxs-lookup"><span data-stu-id="7fb45-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="7fb45-128">*pROut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7fb45-128">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb45-129">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7fb45-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7fb45-130">Puntero al vector SH de salida para el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="7fb45-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="7fb45-131">*pGOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7fb45-131">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb45-132">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7fb45-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7fb45-133">Puntero al vector SH de salida del componente verde.</span><span class="sxs-lookup"><span data-stu-id="7fb45-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="7fb45-134">*pBOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7fb45-134">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fb45-135">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7fb45-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7fb45-136">Puntero al vector SH de salida para el componente azul.</span><span class="sxs-lookup"><span data-stu-id="7fb45-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fb45-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fb45-137">Return value</span></span>

<span data-ttu-id="7fb45-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7fb45-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7fb45-139">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7fb45-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7fb45-140">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7fb45-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fb45-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fb45-141">Remarks</span></span>

<span data-ttu-id="7fb45-142">Evalúa una luz esférica y devuelve datos de SH espectrales.</span><span class="sxs-lookup"><span data-stu-id="7fb45-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="7fb45-143">No hay ninguna normalización de la intensidad de la luz, como ocurre con las [luces direccionales](light-types.md), por lo que hay que tener cuidado al especificar las intensidades.</span><span class="sxs-lookup"><span data-stu-id="7fb45-143">There is no normalization of the intensity of the light like there is for [directional lights](light-types.md), so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="7fb45-144">Se calcularán tres muestras espectrales; se devolverá *pROut* , mientras que *pGOut* y *pBOut* se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="7fb45-144">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="7fb45-145">En la esfera con radio de unidad, tal y como se muestra en la siguiente ilustración, la dirección se puede especificar simplemente con Theta, el ángulo del eje z en la dirección de la [mano derecha](coordinate-systems.md)y la PHI, el ángulo de z.</span><span class="sxs-lookup"><span data-stu-id="7fb45-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="7fb45-147">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (Theta, PHI) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="7fb45-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="7fb45-148">El ángulo Zeta varía en el intervalo de 0 a 2 PI, mientras que la PHI varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="7fb45-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre las coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="7fb45-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fb45-150">Requirements</span></span>



| <span data-ttu-id="7fb45-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fb45-151">Requirement</span></span> | <span data-ttu-id="7fb45-152">Value</span><span class="sxs-lookup"><span data-stu-id="7fb45-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fb45-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fb45-153">Header</span></span><br/>  | <dl> <span data-ttu-id="7fb45-154"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fb45-154"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7fb45-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7fb45-155">Library</span></span><br/> | <dl> <span data-ttu-id="7fb45-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fb45-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7fb45-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fb45-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb45-158">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="7fb45-158">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7fb45-159">Transferencia Radiance precalculada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7fb45-159">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 

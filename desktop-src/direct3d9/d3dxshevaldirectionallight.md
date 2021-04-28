---
description: 'Función D3DXSHEvalDirectionalLight (D3dx9math.h): evalúa una luz direccional y devuelve datos esféricos esféricos (SH).'
ms.assetid: 6e2e9b02-13bb-4cef-ae9d-343fbf64e5d7
title: Función D3DXSHEvalDirectionalLight (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488682eca230c8da6cc5048aded4a7a1e7f71bfd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117913"
---
# <a name="d3dxshevaldirectionallight-function-d3dx9mathh"></a><span data-ttu-id="0b491-103">Función D3DXSHEvalDirectionalLight (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="0b491-103">D3DXSHEvalDirectionalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="0b491-104">Evalúa una luz [direccional y](light-types.md) devuelve datos esféricos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="0b491-104">Evaluates a [directional light](light-types.md) and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b491-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b491-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="0b491-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b491-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b491-107">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0b491-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b491-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b491-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b491-109">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="0b491-109">Order of the SH evaluation.</span></span> <span data-ttu-id="0b491-110">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="0b491-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="0b491-111">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="0b491-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="0b491-112">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="0b491-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="0b491-113">*pDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0b491-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b491-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b491-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0b491-115">Puntero al vector de dirección del eje del hemisferio (x, y, z) en el que se evalúan las funciones de base sh.</span><span class="sxs-lookup"><span data-stu-id="0b491-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="0b491-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0b491-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0b491-117">*RIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0b491-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b491-118">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b491-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b491-119">Intensidad roja de la luz.</span><span class="sxs-lookup"><span data-stu-id="0b491-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="0b491-120">*GIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0b491-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b491-121">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b491-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b491-122">Intensidad verde de la luz.</span><span class="sxs-lookup"><span data-stu-id="0b491-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="0b491-123">*BIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0b491-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b491-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b491-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b491-125">Intensidad azul de la luz.</span><span class="sxs-lookup"><span data-stu-id="0b491-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="0b491-126">*pROut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0b491-126">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b491-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b491-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b491-128">Puntero al vector SH de salida para el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="0b491-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="0b491-129">*pGOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0b491-129">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b491-130">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b491-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b491-131">Puntero opcional al vector SH de salida para el componente verde.</span><span class="sxs-lookup"><span data-stu-id="0b491-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="0b491-132">*pBOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0b491-132">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b491-133">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b491-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b491-134">Puntero opcional al vector SH de salida para el componente azul.</span><span class="sxs-lookup"><span data-stu-id="0b491-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b491-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b491-135">Return value</span></span>

<span data-ttu-id="0b491-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b491-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b491-137">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b491-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0b491-138">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0b491-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b491-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b491-139">Remarks</span></span>

<span data-ttu-id="0b491-140">El vector de salida se calcula de modo que si la relación de intensidad R/G/B es igual a 1, el resultado de la radiación de salida de un punto directamente debajo de la luz en un objeto difuso con un albedo de 1 sería 1,0.</span><span class="sxs-lookup"><span data-stu-id="0b491-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="0b491-141">Esto calculará tres ejemplos espectrales; *se devolverá pROut,* mientras que se pueden devolver *pGOut* y *pBOut.*</span><span class="sxs-lookup"><span data-stu-id="0b491-141">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="0b491-142">En la esfera con radio de unidad, como se muestra en la ilustración siguiente, la dirección [](coordinate-systems.md)se puede especificar simplemente con theta, el ángulo sobre el eje Z en la dirección de la derecha y el ángulo de z.</span><span class="sxs-lookup"><span data-stu-id="0b491-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="0b491-144">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (theta, phi) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="0b491-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="0b491-145">El ángulo de theta varía en el intervalo de 0 a 2 pi, mientras que el de phi varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="0b491-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="0b491-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b491-147">Requirements</span></span>



| <span data-ttu-id="0b491-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b491-148">Requirement</span></span> | <span data-ttu-id="0b491-149">Value</span><span class="sxs-lookup"><span data-stu-id="0b491-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b491-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b491-150">Header</span></span><br/>  | <dl> <span data-ttu-id="0b491-151"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0b491-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0b491-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b491-152">Library</span></span><br/> | <dl> <span data-ttu-id="0b491-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b491-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b491-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0b491-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b491-155">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="0b491-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0b491-156">Transferencia de radiancia precalutada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0b491-156">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 

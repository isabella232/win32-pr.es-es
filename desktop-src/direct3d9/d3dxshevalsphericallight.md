---
description: 'Función D3DXSHEvalSphericalLight (D3dx9math.h): evalúa una luz esférica y devuelve datos de armónica esférica esférica (SH).'
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: Función D3DXSHEvalSphericalLight (D3dx9math.h)
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
ms.openlocfilehash: db671d58806d999e07b1aac1e8e4da2fb38acc6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117893"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a><span data-ttu-id="bafae-103">Función D3DXSHEvalSphericalLight (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="bafae-103">D3DXSHEvalSphericalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="bafae-104">Evalúa una luz esférica y devuelve datos esféricos de armónica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="bafae-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bafae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bafae-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="bafae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bafae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bafae-107">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bafae-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafae-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bafae-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bafae-109">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="bafae-109">Order of the SH evaluation.</span></span> <span data-ttu-id="bafae-110">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="bafae-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="bafae-111">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="bafae-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="bafae-112">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="bafae-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="bafae-113">*pPos* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bafae-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafae-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bafae-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bafae-115">Puntero a la posición ligera.</span><span class="sxs-lookup"><span data-stu-id="bafae-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="bafae-116">*Radio* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bafae-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafae-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bafae-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bafae-118">Radio de la fuente de luz esférica.</span><span class="sxs-lookup"><span data-stu-id="bafae-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="bafae-119">*RIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bafae-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafae-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bafae-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bafae-121">Intensidad roja de la luz.</span><span class="sxs-lookup"><span data-stu-id="bafae-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="bafae-122">*GIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bafae-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafae-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bafae-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bafae-124">Intensidad verde de la luz.</span><span class="sxs-lookup"><span data-stu-id="bafae-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="bafae-125">*BIntensity* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bafae-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafae-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bafae-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bafae-127">Intensidad azul de la luz.</span><span class="sxs-lookup"><span data-stu-id="bafae-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="bafae-128">*pROut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bafae-128">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafae-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bafae-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bafae-130">Puntero al vector SH de salida para el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="bafae-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="bafae-131">*pGOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bafae-131">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafae-132">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bafae-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bafae-133">Puntero al vector SH de salida para el componente verde.</span><span class="sxs-lookup"><span data-stu-id="bafae-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="bafae-134">*pBOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bafae-134">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafae-135">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bafae-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bafae-136">Puntero al vector SH de salida para el componente azul.</span><span class="sxs-lookup"><span data-stu-id="bafae-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bafae-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bafae-137">Return value</span></span>

<span data-ttu-id="bafae-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bafae-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bafae-139">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bafae-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bafae-140">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bafae-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bafae-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bafae-141">Remarks</span></span>

<span data-ttu-id="bafae-142">Evalúa una luz esférica y devuelve datos sh espectrales.</span><span class="sxs-lookup"><span data-stu-id="bafae-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="bafae-143">No hay ninguna normalización de la intensidad [](light-types.md)de la luz como para las luces direccionales, por lo que debe tener cuidado al especificar las intensidades.</span><span class="sxs-lookup"><span data-stu-id="bafae-143">There is no normalization of the intensity of the light like there is for [directional lights](light-types.md), so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="bafae-144">Esto calculará tres ejemplos espectrales; *se devolverá pROut,* mientras que se pueden devolver *pGOut* y *pBOut.*</span><span class="sxs-lookup"><span data-stu-id="bafae-144">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="bafae-145">En la esfera con radio de unidad, como se muestra en la ilustración siguiente, la dirección [](coordinate-systems.md)se puede especificar simplemente con theta, el ángulo sobre el eje Z en la dirección derecha y el ángulo de la z.</span><span class="sxs-lookup"><span data-stu-id="bafae-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="bafae-147">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (theta, phi) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="bafae-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="bafae-148">El ángulo de theta varía en el intervalo de 0 a 2 pi, mientras que phi varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="bafae-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="bafae-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bafae-150">Requirements</span></span>



| <span data-ttu-id="bafae-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="bafae-151">Requirement</span></span> | <span data-ttu-id="bafae-152">Value</span><span class="sxs-lookup"><span data-stu-id="bafae-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bafae-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bafae-153">Header</span></span><br/>  | <dl> <span data-ttu-id="bafae-154"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bafae-154"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bafae-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bafae-155">Library</span></span><br/> | <dl> <span data-ttu-id="bafae-156"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bafae-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bafae-157">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bafae-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bafae-158">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="bafae-158">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bafae-159">Transferencia de radiancia precalutada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bafae-159">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 

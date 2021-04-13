---
description: Evalúa una luz que es una interpolación lineal entre dos colores en la esfera.
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: Función D3DXSHEvalHemisphereLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c6ff3359ce0629eec472e4da24a31c24196c7f15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362664"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a><span data-ttu-id="2078d-103">Función D3DXSHEvalHemisphereLight (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="2078d-103">D3DXSHEvalHemisphereLight function (D3DX10.h)</span></span>

<span data-ttu-id="2078d-104">Evalúa una luz que es una interpolación lineal entre dos colores en la esfera.</span><span class="sxs-lookup"><span data-stu-id="2078d-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="2078d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2078d-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="2078d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2078d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2078d-107">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2078d-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2078d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2078d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2078d-109">Orden de evaluación de armónicos esférico (SH).</span><span class="sxs-lookup"><span data-stu-id="2078d-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="2078d-110">Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="2078d-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2078d-111">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="2078d-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2078d-112">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="2078d-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2078d-113">*pDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2078d-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2078d-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2078d-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2078d-115">Puntero al vector de dirección del eje hemisferio (x, y, z) en el que se van a evaluar las funciones de base de SH.</span><span class="sxs-lookup"><span data-stu-id="2078d-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="2078d-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2078d-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2078d-117">*Parte superior* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2078d-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2078d-118">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2078d-118">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="2078d-119">Color del cielo.</span><span class="sxs-lookup"><span data-stu-id="2078d-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="2078d-120">*Inferior* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2078d-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2078d-121">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2078d-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="2078d-122">Color de fondo.</span><span class="sxs-lookup"><span data-stu-id="2078d-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="2078d-123">*pROut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2078d-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2078d-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2078d-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2078d-125">Puntero al vector SH de salida para el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="2078d-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="2078d-126">*pGOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2078d-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2078d-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2078d-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2078d-128">Puntero al vector SH de salida del componente verde.</span><span class="sxs-lookup"><span data-stu-id="2078d-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="2078d-129">*pBOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2078d-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2078d-130">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2078d-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2078d-131">Puntero al vector SH de salida para el componente azul.</span><span class="sxs-lookup"><span data-stu-id="2078d-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2078d-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2078d-132">Return value</span></span>

<span data-ttu-id="2078d-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2078d-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2078d-134">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2078d-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2078d-135">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2078d-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2078d-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2078d-136">Remarks</span></span>

<span data-ttu-id="2078d-137">La interpolación se realiza linealmente entre los dos puntos, no en la superficie de la esfera (es decir, si el eje era (0, 0, 1) es lineal en Z, no en el ángulo azimuthal).</span><span class="sxs-lookup"><span data-stu-id="2078d-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="2078d-138">La función de iluminación esférica resultante se normaliza de modo que un punto en una superficie difusa perfecta sin sombreado y una normal señalada en la dirección pDir daría como resultado Radiance de salida con un valor de 1 (si el color superior fuera blanco y el color inferior era negro).</span><span class="sxs-lookup"><span data-stu-id="2078d-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction pDir would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="2078d-139">Se trata de un modelo muy sencillo, donde la parte superior representa la intensidad del "cielo" y la parte inferior representa la intensidad de la "base".</span><span class="sxs-lookup"><span data-stu-id="2078d-139">This is a very simple model where Top represents the intensity of the "sky" and Bottom represents the intensity of the "ground."</span></span>

<span data-ttu-id="2078d-140">En la esfera con radio de unidad, tal y como se muestra en la siguiente ilustración, la dirección se puede especificar simplemente con Theta, el ángulo del eje z en la dirección de la mano derecha y la PHI, el ángulo de z.</span><span class="sxs-lookup"><span data-stu-id="2078d-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="2078d-142">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (Theta, PHI) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="2078d-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="2078d-143">El ángulo Zeta varía en el intervalo de 0 a 2 PI, mientras que la PHI varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="2078d-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre las coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="2078d-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2078d-145">Requirements</span></span>



| <span data-ttu-id="2078d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="2078d-146">Requirement</span></span> | <span data-ttu-id="2078d-147">Value</span><span class="sxs-lookup"><span data-stu-id="2078d-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2078d-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2078d-148">Header</span></span><br/>  | <dl> <span data-ttu-id="2078d-149"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2078d-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2078d-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2078d-150">Library</span></span><br/> | <dl> <span data-ttu-id="2078d-151"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2078d-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2078d-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="2078d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2078d-153">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="2078d-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

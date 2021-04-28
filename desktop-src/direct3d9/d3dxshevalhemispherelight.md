---
description: 'Función D3DXSHEvalPxisphereLight (D3dx9math.h): evalúa una luz que es una interpolación lineal entre dos colores sobre la esfera.'
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: Función D3DXSHEvalRriisphereLight (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc06dcf866c21cc5dcb96b23dea5a4640293fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093973"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a><span data-ttu-id="54754-103">Función D3DXSHEvalRriisphereLight (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="54754-103">D3DXSHEvalHemisphereLight function (D3dx9math.h)</span></span>

<span data-ttu-id="54754-104">Evalúa una luz que es una interpolación lineal entre dos colores sobre la esfera.</span><span class="sxs-lookup"><span data-stu-id="54754-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="54754-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54754-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="54754-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54754-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54754-107">*Pedido* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54754-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54754-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54754-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54754-109">Orden de la evaluación del armónico esférico (SH).</span><span class="sxs-lookup"><span data-stu-id="54754-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="54754-110">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="54754-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="54754-111">La evaluación genera coeficientes order-to-order.</span><span class="sxs-lookup"><span data-stu-id="54754-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="54754-112">El grado de la evaluación es Order - 1.</span><span class="sxs-lookup"><span data-stu-id="54754-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="54754-113">*pDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54754-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54754-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="54754-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="54754-115">Puntero al vector de dirección del eje (x, y, z) en el que se evaluarán las funciones de base sh.</span><span class="sxs-lookup"><span data-stu-id="54754-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="54754-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="54754-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="54754-117">*Top* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54754-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54754-118">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="54754-118">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="54754-119">Color del cielo.</span><span class="sxs-lookup"><span data-stu-id="54754-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="54754-120">*Inferior* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54754-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54754-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="54754-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="54754-122">Color del suelo.</span><span class="sxs-lookup"><span data-stu-id="54754-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="54754-123">*pROut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54754-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54754-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="54754-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54754-125">Puntero al vector SH de salida para el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="54754-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="54754-126">*pGOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54754-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54754-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="54754-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54754-128">Puntero al vector SH de salida para el componente verde.</span><span class="sxs-lookup"><span data-stu-id="54754-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="54754-129">*pBOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="54754-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54754-130">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="54754-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54754-131">Puntero al vector SH de salida para el componente azul.</span><span class="sxs-lookup"><span data-stu-id="54754-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54754-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54754-132">Return value</span></span>

<span data-ttu-id="54754-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54754-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54754-134">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54754-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="54754-135">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="54754-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="54754-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54754-136">Remarks</span></span>

<span data-ttu-id="54754-137">La interpolación se realiza linealmente entre los dos puntos, no sobre la superficie de la esfera (es decir, si el eje era (0,0,1) es lineal en Z, no en el ángulo azimu angle).</span><span class="sxs-lookup"><span data-stu-id="54754-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="54754-138">La función de iluminación esférica resultante se normaliza de modo que un punto en una superficie perfectamente difusa sin sombras y un punto normal en la dirección *pDir* daría como resultado un brillo de salida con un valor de 1 (si el color superior era blanco y el color inferior era negro).</span><span class="sxs-lookup"><span data-stu-id="54754-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction *pDir* would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="54754-139">Se trata de un modelo muy sencillo donde *Top* representa la intensidad del "cielo" y *Bottom* representa la intensidad del "suelo".</span><span class="sxs-lookup"><span data-stu-id="54754-139">This is a very simple model where *Top* represents the intensity of the "sky" and *Bottom* represents the intensity of the "ground."</span></span>

<span data-ttu-id="54754-140">En la esfera con radio de unidad, como se muestra en la ilustración siguiente, la dirección [](coordinate-systems.md)se puede especificar simplemente con theta, el ángulo sobre el eje Z en la dirección derecha y el ángulo de la z.</span><span class="sxs-lookup"><span data-stu-id="54754-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

<span data-ttu-id="54754-142">Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (theta, phi) en la esfera de unidad.</span><span class="sxs-lookup"><span data-stu-id="54754-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="54754-143">El ángulo de theta varía en el intervalo de 0 a 2 pi, mientras que phi varía de 0 a pi.</span><span class="sxs-lookup"><span data-stu-id="54754-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![ecuaciones de la relación entre coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="54754-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54754-145">Requirements</span></span>



| <span data-ttu-id="54754-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="54754-146">Requirement</span></span> | <span data-ttu-id="54754-147">Value</span><span class="sxs-lookup"><span data-stu-id="54754-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54754-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54754-148">Header</span></span><br/>  | <dl> <span data-ttu-id="54754-149"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="54754-149"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="54754-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54754-150">Library</span></span><br/> | <dl> <span data-ttu-id="54754-151"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="54754-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54754-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="54754-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54754-153">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="54754-153">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="54754-154">Transferencia de radiancia precalutada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="54754-154">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 

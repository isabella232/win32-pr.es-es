---
description: Crea una matriz de proyección ortográfica personalizada y de mano derecha.
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: Función D3DXMatrixOrthoOffCenterRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3b5b544a4144ebc283686385638435ec42b4d801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721495"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="184e7-103">Función D3DXMatrixOrthoOffCenterRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="184e7-103">D3DXMatrixOrthoOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="184e7-104">Crea una matriz de proyección ortográfica personalizada y de mano derecha.</span><span class="sxs-lookup"><span data-stu-id="184e7-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="184e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="184e7-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="184e7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="184e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="184e7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="184e7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="184e7-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="184e7-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="184e7-109">Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="184e7-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="184e7-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="184e7-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184e7-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="184e7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="184e7-112">Valor x mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="184e7-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="184e7-113">*r* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="184e7-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184e7-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="184e7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="184e7-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="184e7-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="184e7-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="184e7-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184e7-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="184e7-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="184e7-118">Valor y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="184e7-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="184e7-119">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="184e7-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184e7-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="184e7-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="184e7-121">Valor y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="184e7-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="184e7-122">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="184e7-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184e7-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="184e7-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="184e7-124">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="184e7-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="184e7-125">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="184e7-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184e7-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="184e7-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="184e7-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="184e7-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="184e7-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="184e7-128">Return value</span></span>

<span data-ttu-id="184e7-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="184e7-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="184e7-130">Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="184e7-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="184e7-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="184e7-131">Remarks</span></span>

<span data-ttu-id="184e7-132">La función [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) es un caso especial de la función D3DXMatrixOrthoOffCenterRH.</span><span class="sxs-lookup"><span data-stu-id="184e7-132">The [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) function is a special case of the D3DXMatrixOrthoOffCenterRH function.</span></span> <span data-ttu-id="184e7-133">Para crear la misma proyección mediante D3DXMatrixOrthoOffCenterRH, use los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="184e7-133">To create the same projection using D3DXMatrixOrthoOffCenterRH, use the following values:</span></span>

<span data-ttu-id="184e7-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="184e7-134">l = -w/2,</span></span>

<span data-ttu-id="184e7-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="184e7-135">r = w/2,</span></span>

<span data-ttu-id="184e7-136">b =-h/2 y</span><span class="sxs-lookup"><span data-stu-id="184e7-136">b = -h/2, and</span></span>

<span data-ttu-id="184e7-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="184e7-137">t = h/2.</span></span>

<span data-ttu-id="184e7-138">Todos los parámetros de la función D3DXMatrixOrthoOffCenterRH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="184e7-138">All the parameters of the D3DXMatrixOrthoOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="184e7-139">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="184e7-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="184e7-140">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="184e7-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="184e7-141">De esta manera, la función D3DXMatrixOrthoOffCenterRH se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="184e7-141">In this way, the D3DXMatrixOrthoOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="184e7-142">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="184e7-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="184e7-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="184e7-143">Requirements</span></span>



| <span data-ttu-id="184e7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="184e7-144">Requirement</span></span> | <span data-ttu-id="184e7-145">Value</span><span class="sxs-lookup"><span data-stu-id="184e7-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="184e7-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="184e7-146">Header</span></span><br/>  | <dl> <span data-ttu-id="184e7-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="184e7-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="184e7-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="184e7-148">Library</span></span><br/> | <dl> <span data-ttu-id="184e7-149"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="184e7-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="184e7-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="184e7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184e7-151">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="184e7-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

---
description: Crea una matriz de proyección ortográfica personalizada y de mano derecha.
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: Función D3DXMatrixOrthoOffCenterRH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7de5e4b3a872ea7466840e511fc0a57448861b55
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718394"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="0353a-103">Función D3DXMatrixOrthoOffCenterRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0353a-103">D3DXMatrixOrthoOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="0353a-104">Crea una matriz de proyección ortográfica personalizada y de mano derecha.</span><span class="sxs-lookup"><span data-stu-id="0353a-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0353a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0353a-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0353a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0353a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0353a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0353a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0353a-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0353a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0353a-109">Puntero al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="0353a-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="0353a-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0353a-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0353a-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0353a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0353a-112">Valor x mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="0353a-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0353a-113">*r* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0353a-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0353a-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0353a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0353a-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="0353a-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0353a-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0353a-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0353a-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0353a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0353a-118">Valor y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="0353a-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0353a-119">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0353a-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0353a-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0353a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0353a-121">Valor y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="0353a-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0353a-122">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0353a-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0353a-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0353a-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0353a-124">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="0353a-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0353a-125">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0353a-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0353a-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0353a-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0353a-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="0353a-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0353a-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0353a-128">Return value</span></span>

<span data-ttu-id="0353a-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0353a-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0353a-130">Puntero al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="0353a-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0353a-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0353a-131">Remarks</span></span>

<span data-ttu-id="0353a-132">La función [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) es un caso especial de la función **D3DXMatrixOrthoOffCenterRH** .</span><span class="sxs-lookup"><span data-stu-id="0353a-132">The [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) function is a special case of the **D3DXMatrixOrthoOffCenterRH** function.</span></span> <span data-ttu-id="0353a-133">Para crear la misma proyección mediante **D3DXMatrixOrthoOffCenterRH**, use los siguientes valores: l =-w/2, r = w/2, b =-h/2 y t = h/2.</span><span class="sxs-lookup"><span data-stu-id="0353a-133">To create the same projection using **D3DXMatrixOrthoOffCenterRH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="0353a-134">Todos los parámetros de la función **D3DXMatrixOrthoOffCenterRH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="0353a-134">All the parameters of the **D3DXMatrixOrthoOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="0353a-135">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="0353a-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="0353a-136">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="0353a-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0353a-137">De esta manera, la función **D3DXMatrixOrthoOffCenterRH** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="0353a-137">In this way, the **D3DXMatrixOrthoOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0353a-138">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="0353a-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="0353a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0353a-139">Requirements</span></span>



| <span data-ttu-id="0353a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0353a-140">Requirement</span></span> | <span data-ttu-id="0353a-141">Value</span><span class="sxs-lookup"><span data-stu-id="0353a-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0353a-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0353a-142">Header</span></span><br/>  | <dl> <span data-ttu-id="0353a-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0353a-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0353a-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0353a-144">Library</span></span><br/> | <dl> <span data-ttu-id="0353a-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0353a-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0353a-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="0353a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0353a-147">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="0353a-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0353a-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="0353a-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="0353a-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="0353a-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="0353a-150">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="0353a-150">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 

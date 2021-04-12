---
description: Crea una matriz de proyección ortográfica a la izquierda.
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: Función D3DXMatrixOrthoLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4aaf4a1a770ba0200a6afe389d37e248b9f4c7de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362684"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a><span data-ttu-id="85e17-103">Función D3DXMatrixOrthoLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="85e17-103">D3DXMatrixOrthoLH function (D3dx9math.h)</span></span>

<span data-ttu-id="85e17-104">Crea una matriz de proyección ortográfica a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="85e17-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e17-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85e17-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="85e17-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85e17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85e17-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="85e17-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85e17-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="85e17-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="85e17-109">Puntero al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="85e17-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="85e17-110">*w* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="85e17-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e17-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85e17-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85e17-112">Ancho del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="85e17-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="85e17-113">*h* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="85e17-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e17-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85e17-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85e17-115">Alto del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="85e17-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="85e17-116">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85e17-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e17-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85e17-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85e17-118">Valor z mínimo del volumen de vista, al que se hace referencia como z-near.</span><span class="sxs-lookup"><span data-stu-id="85e17-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="85e17-119">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85e17-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e17-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85e17-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85e17-121">Valor z máximo del volumen de vista, al que se hace referencia como z-lejano.</span><span class="sxs-lookup"><span data-stu-id="85e17-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85e17-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85e17-122">Return value</span></span>

<span data-ttu-id="85e17-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="85e17-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="85e17-124">Puntero al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="85e17-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="85e17-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85e17-125">Remarks</span></span>

<span data-ttu-id="85e17-126">Todos los parámetros de la función **D3DXMatrixOrthoLH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="85e17-126">All the parameters of the **D3DXMatrixOrthoLH** function are distances in camera space.</span></span> <span data-ttu-id="85e17-127">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="85e17-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="85e17-128">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="85e17-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="85e17-129">De esta manera, la función **D3DXMatrixOrthoLH** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="85e17-129">In this way, the **D3DXMatrixOrthoLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="85e17-130">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="85e17-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a><span data-ttu-id="85e17-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85e17-131">Requirements</span></span>



| <span data-ttu-id="85e17-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="85e17-132">Requirement</span></span> | <span data-ttu-id="85e17-133">Value</span><span class="sxs-lookup"><span data-stu-id="85e17-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85e17-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85e17-134">Header</span></span><br/>  | <dl> <span data-ttu-id="85e17-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="85e17-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="85e17-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85e17-136">Library</span></span><br/> | <dl> <span data-ttu-id="85e17-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85e17-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85e17-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="85e17-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e17-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="85e17-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="85e17-140">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="85e17-140">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="85e17-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="85e17-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="85e17-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="85e17-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 

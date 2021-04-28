---
description: 'Función D3DXMatrixOrthoLH (D3DX10Math.h): crea una matriz de proyección ortográfica de mano izquierda.'
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Función D3DXMatrixOrthoLH (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 73cd5d9b809a0eb442db57e91c3788d2548a8c33
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113103"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a><span data-ttu-id="b5bbe-103">Función D3DXMatrixOrthoLH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="b5bbe-103">D3DXMatrixOrthoLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b5bbe-104">Crea una matriz de proyección ortográfica a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5bbe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5bbe-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="b5bbe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5bbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5bbe-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b5bbe-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5bbe-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5bbe-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5bbe-109">Puntero al [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="b5bbe-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5bbe-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5bbe-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5bbe-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5bbe-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5bbe-112">Ancho del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b5bbe-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5bbe-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5bbe-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5bbe-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5bbe-115">Alto del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b5bbe-116">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b5bbe-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5bbe-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5bbe-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5bbe-118">Valor z mínimo del volumen de vista que se conoce como z-near.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="b5bbe-119">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b5bbe-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5bbe-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5bbe-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5bbe-121">Valor z máximo del volumen de vista que se conoce como z-far.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5bbe-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5bbe-122">Return value</span></span>

<span data-ttu-id="b5bbe-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5bbe-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5bbe-124">Puntero al [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="b5bbe-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5bbe-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5bbe-125">Remarks</span></span>

<span data-ttu-id="b5bbe-126">Todos los parámetros de la función D3DXMatrixOrthoLH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-126">All the parameters of the D3DXMatrixOrthoLH function are distances in camera space.</span></span> <span data-ttu-id="b5bbe-127">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b5bbe-128">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b5bbe-129">De este modo, la función D3DXMatrixOrthoLH se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-129">In this way, the D3DXMatrixOrthoLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b5bbe-130">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="b5bbe-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="b5bbe-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5bbe-131">Requirements</span></span>



| <span data-ttu-id="b5bbe-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5bbe-132">Requirement</span></span> | <span data-ttu-id="b5bbe-133">Value</span><span class="sxs-lookup"><span data-stu-id="b5bbe-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5bbe-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5bbe-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b5bbe-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b5bbe-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5bbe-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5bbe-136">Library</span></span><br/> | <dl> <span data-ttu-id="b5bbe-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5bbe-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5bbe-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b5bbe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5bbe-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="b5bbe-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

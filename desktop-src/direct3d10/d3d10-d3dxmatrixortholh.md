---
description: Crea una matriz de proyección ortográfica a la izquierda.
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Función D3DXMatrixOrthoLH (D3DX10Math. h)
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
ms.openlocfilehash: 0b49e6008b52f7060075688730c72f5f5d3f725a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280469"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a><span data-ttu-id="8cdc8-103">Función D3DXMatrixOrthoLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8cdc8-103">D3DXMatrixOrthoLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="8cdc8-104">Crea una matriz de proyección ortográfica a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cdc8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cdc8-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="8cdc8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cdc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cdc8-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8cdc8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cdc8-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cdc8-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8cdc8-109">Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cdc8-110">*w* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8cdc8-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cdc8-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cdc8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cdc8-112">Ancho del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8cdc8-113">*h* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8cdc8-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cdc8-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cdc8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cdc8-115">Alto del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8cdc8-116">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cdc8-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cdc8-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cdc8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cdc8-118">Valor z mínimo del volumen de vista, al que se hace referencia como z-near.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="8cdc8-119">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cdc8-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cdc8-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cdc8-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cdc8-121">Valor z máximo del volumen de vista, al que se hace referencia como z-lejano.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cdc8-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cdc8-122">Return value</span></span>

<span data-ttu-id="8cdc8-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cdc8-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8cdc8-124">Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8cdc8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cdc8-125">Remarks</span></span>

<span data-ttu-id="8cdc8-126">Todos los parámetros de la función D3DXMatrixOrthoLH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-126">All the parameters of the D3DXMatrixOrthoLH function are distances in camera space.</span></span> <span data-ttu-id="8cdc8-127">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="8cdc8-128">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8cdc8-129">De esta manera, la función D3DXMatrixOrthoLH se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-129">In this way, the D3DXMatrixOrthoLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8cdc8-130">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="8cdc8-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="8cdc8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cdc8-131">Requirements</span></span>



| <span data-ttu-id="8cdc8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cdc8-132">Requirement</span></span> | <span data-ttu-id="8cdc8-133">Value</span><span class="sxs-lookup"><span data-stu-id="8cdc8-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cdc8-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cdc8-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8cdc8-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cdc8-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8cdc8-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cdc8-136">Library</span></span><br/> | <dl> <span data-ttu-id="8cdc8-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cdc8-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8cdc8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cdc8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cdc8-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="8cdc8-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

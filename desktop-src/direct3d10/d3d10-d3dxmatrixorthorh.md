---
description: Crea una matriz de proyección ortográfica de mano derecha.
ms.assetid: e6673ff4-06a2-4a16-b72e-5ca69ddf2438
title: Función D3DXMatrixOrthoRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a8883f2690fa5a5f0bfa1bb1570163b714974b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721494"
---
# <a name="d3dxmatrixorthorh-function-d3dx10mathh"></a><span data-ttu-id="00dcb-103">Función D3DXMatrixOrthoRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="00dcb-103">D3DXMatrixOrthoRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="00dcb-104">Crea una matriz de proyección ortográfica de mano derecha.</span><span class="sxs-lookup"><span data-stu-id="00dcb-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="00dcb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00dcb-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="00dcb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00dcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00dcb-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="00dcb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcb-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="00dcb-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="00dcb-109">Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="00dcb-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="00dcb-110">*w* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="00dcb-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcb-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00dcb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00dcb-112">Ancho del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="00dcb-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="00dcb-113">*h* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="00dcb-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcb-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00dcb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00dcb-115">Alto del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="00dcb-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="00dcb-116">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00dcb-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcb-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00dcb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00dcb-118">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="00dcb-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="00dcb-119">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00dcb-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dcb-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00dcb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00dcb-121">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="00dcb-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00dcb-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00dcb-122">Return value</span></span>

<span data-ttu-id="00dcb-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="00dcb-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="00dcb-124">Puntero al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="00dcb-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00dcb-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00dcb-125">Remarks</span></span>

<span data-ttu-id="00dcb-126">Todos los parámetros de la función D3DXMatrixOrthoRH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="00dcb-126">All the parameters of the D3DXMatrixOrthoRH function are distances in camera space.</span></span> <span data-ttu-id="00dcb-127">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="00dcb-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="00dcb-128">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="00dcb-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="00dcb-129">De esta manera, la función D3DXMatrixOrthoRH se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="00dcb-129">In this way, the D3DXMatrixOrthoRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="00dcb-130">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="00dcb-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="00dcb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00dcb-131">Requirements</span></span>



| <span data-ttu-id="00dcb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="00dcb-132">Requirement</span></span> | <span data-ttu-id="00dcb-133">Value</span><span class="sxs-lookup"><span data-stu-id="00dcb-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00dcb-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00dcb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="00dcb-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="00dcb-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="00dcb-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00dcb-136">Library</span></span><br/> | <dl> <span data-ttu-id="00dcb-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00dcb-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="00dcb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="00dcb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00dcb-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="00dcb-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

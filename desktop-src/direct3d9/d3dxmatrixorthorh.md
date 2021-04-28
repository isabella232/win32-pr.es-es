---
description: 'Función D3DXMatrixOrthoRH (D3dx9math.h): crea una matriz de proyección ortográfica a la derecha.'
ms.assetid: 6b9b50d5-0307-4fc7-a28d-8f42d2a21bf0
title: Función D3DXMatrixOrthoRH (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d34a8379851d80ae8734c7f32cc0dc5977af2088
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107443"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a><span data-ttu-id="a14e9-103">Función D3DXMatrixOrthoRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a14e9-103">D3DXMatrixOrthoRH function (D3dx9math.h)</span></span>

<span data-ttu-id="a14e9-104">Crea una matriz de proyección ortográfica con la mano derecha.</span><span class="sxs-lookup"><span data-stu-id="a14e9-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a14e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a14e9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="a14e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a14e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a14e9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a14e9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a14e9-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a14e9-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a14e9-109">Puntero al [**D3DXMATRIX resultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="a14e9-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a14e9-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a14e9-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a14e9-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a14e9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a14e9-112">Ancho del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="a14e9-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a14e9-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a14e9-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a14e9-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a14e9-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a14e9-115">Alto del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="a14e9-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a14e9-116">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a14e9-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a14e9-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a14e9-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a14e9-118">Valor Z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="a14e9-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a14e9-119">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a14e9-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a14e9-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a14e9-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a14e9-121">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="a14e9-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a14e9-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a14e9-122">Return value</span></span>

<span data-ttu-id="a14e9-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a14e9-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a14e9-124">Puntero al [**D3DXMATRIX resultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="a14e9-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a14e9-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a14e9-125">Remarks</span></span>

<span data-ttu-id="a14e9-126">Todos los parámetros de la **función D3DXMatrixOrthoRH** son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="a14e9-126">All the parameters of the **D3DXMatrixOrthoRH** function are distances in camera space.</span></span> <span data-ttu-id="a14e9-127">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="a14e9-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="a14e9-128">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="a14e9-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a14e9-129">De esta manera, la **función D3DXMatrixOrthoRH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="a14e9-129">In this way, the **D3DXMatrixOrthoRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a14e9-130">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="a14e9-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="a14e9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a14e9-131">Requirements</span></span>



| <span data-ttu-id="a14e9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a14e9-132">Requirement</span></span> | <span data-ttu-id="a14e9-133">Value</span><span class="sxs-lookup"><span data-stu-id="a14e9-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a14e9-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a14e9-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a14e9-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a14e9-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a14e9-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a14e9-136">Library</span></span><br/> | <dl> <span data-ttu-id="a14e9-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a14e9-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a14e9-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a14e9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14e9-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="a14e9-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a14e9-140">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="a14e9-140">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="a14e9-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="a14e9-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="a14e9-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="a14e9-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 

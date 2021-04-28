---
description: 'Función D3DXMatrixPerspectiveFovLH (D3DX10Math.h): crea una matriz de proyección de perspectiva a la izquierda basada en un campo de vista.'
ms.assetid: 35ee12d6-0a58-4b00-ac8f-82f82215f02e
title: Función D3DXMatrixPerspectiveFovLH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cea1bec170664993332b1cde1de375c416209209
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113093"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx10mathh"></a><span data-ttu-id="bd60a-103">Función D3DXMatrixPerspectiveFovLH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="bd60a-103">D3DXMatrixPerspectiveFovLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="bd60a-104">Crea una matriz de proyección de perspectiva a la izquierda basada en un campo visual.</span><span class="sxs-lookup"><span data-stu-id="bd60a-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd60a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd60a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="bd60a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd60a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd60a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bd60a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd60a-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd60a-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bd60a-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="bd60a-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bd60a-110">*fovy* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bd60a-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd60a-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd60a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd60a-112">Campo de vista en la dirección y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="bd60a-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="bd60a-113">*Aspecto* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bd60a-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd60a-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd60a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd60a-115">Relación de aspecto, definida como ancho del espacio de vista dividido por alto.</span><span class="sxs-lookup"><span data-stu-id="bd60a-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="bd60a-116">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bd60a-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd60a-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd60a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd60a-118">Valor Z del plano de vista cercano.</span><span class="sxs-lookup"><span data-stu-id="bd60a-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="bd60a-119">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bd60a-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd60a-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd60a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd60a-121">Valor Z del plano de vista lejano.</span><span class="sxs-lookup"><span data-stu-id="bd60a-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd60a-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd60a-122">Return value</span></span>

<span data-ttu-id="bd60a-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd60a-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bd60a-124">Puntero a una estructura D3DXMATRIX que es una matriz de proyección de perspectiva a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="bd60a-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd60a-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd60a-125">Remarks</span></span>

<span data-ttu-id="bd60a-126">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="bd60a-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bd60a-127">De esta manera, la función D3DXMatrixPerspectiveFovLH se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="bd60a-127">In this way, the D3DXMatrixPerspectiveFovLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="bd60a-128">Esta función calcula la matriz devuelta como se muestra:</span><span class="sxs-lookup"><span data-stu-id="bd60a-128">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="bd60a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd60a-129">Requirements</span></span>



| <span data-ttu-id="bd60a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd60a-130">Requirement</span></span> | <span data-ttu-id="bd60a-131">Value</span><span class="sxs-lookup"><span data-stu-id="bd60a-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd60a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd60a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="bd60a-133"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bd60a-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bd60a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd60a-134">Library</span></span><br/> | <dl> <span data-ttu-id="bd60a-135"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd60a-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd60a-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bd60a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd60a-137">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="bd60a-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

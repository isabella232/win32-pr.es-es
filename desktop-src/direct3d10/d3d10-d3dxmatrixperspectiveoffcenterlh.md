---
description: Crea una matriz de proyección de perspectiva personalizada y diestro.
ms.assetid: 73616fcc-1799-4e65-92b9-2d8f500c326e
title: Función D3DXMatrixPerspectiveOffCenterLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2fb289c0dff148850b8174ccb04a3e3fbfa79d92
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721532"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="cf459-103">Función D3DXMatrixPerspectiveOffCenterLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cf459-103">D3DXMatrixPerspectiveOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="cf459-104">Crea una matriz de proyección de perspectiva personalizada y diestro.</span><span class="sxs-lookup"><span data-stu-id="cf459-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf459-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf459-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="cf459-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf459-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf459-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cf459-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf459-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf459-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cf459-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="cf459-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cf459-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cf459-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf459-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf459-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf459-112">Valor x mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="cf459-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cf459-113">*r* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cf459-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf459-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf459-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf459-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="cf459-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cf459-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cf459-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf459-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf459-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf459-118">Valor y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="cf459-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cf459-119">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cf459-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf459-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf459-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf459-121">Valor y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="cf459-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cf459-122">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf459-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf459-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf459-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf459-124">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="cf459-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cf459-125">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf459-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf459-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf459-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf459-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="cf459-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf459-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf459-128">Return value</span></span>

<span data-ttu-id="cf459-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf459-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cf459-130">Puntero a una estructura D3DXMATRIX que es una matriz personalizada de proyección de perspectiva que se ha personalizado.</span><span class="sxs-lookup"><span data-stu-id="cf459-130">Pointer to a D3DXMATRIX structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf459-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf459-131">Remarks</span></span>

<span data-ttu-id="cf459-132">Todos los parámetros de la función D3DXMatrixPerspectiveOffCenterLH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="cf459-132">All the parameters of the D3DXMatrixPerspectiveOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="cf459-133">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="cf459-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="cf459-134">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="cf459-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cf459-135">De esta manera, la función D3DXMatrixPerspectiveOffCenterLH se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="cf459-135">In this way, the D3DXMatrixPerspectiveOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cf459-136">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="cf459-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="cf459-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf459-137">Requirements</span></span>



| <span data-ttu-id="cf459-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf459-138">Requirement</span></span> | <span data-ttu-id="cf459-139">Value</span><span class="sxs-lookup"><span data-stu-id="cf459-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf459-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf459-140">Header</span></span><br/>  | <dl> <span data-ttu-id="cf459-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf459-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cf459-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf459-142">Library</span></span><br/> | <dl> <span data-ttu-id="cf459-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf459-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf459-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf459-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf459-145">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="cf459-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

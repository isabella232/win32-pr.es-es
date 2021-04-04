---
description: Crea una matriz de proyección de perspectiva a la derecha personalizada.
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: Función D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54fc98658d5466acd69d3245af7488c40cd352c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083787"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="62dd5-103">Función D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="62dd5-103">D3DXMatrixPerspectiveOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="62dd5-104">Crea una matriz de proyección de perspectiva a la derecha personalizada.</span><span class="sxs-lookup"><span data-stu-id="62dd5-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="62dd5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62dd5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="62dd5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62dd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62dd5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="62dd5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62dd5-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="62dd5-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="62dd5-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="62dd5-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="62dd5-110">*l* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="62dd5-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dd5-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62dd5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62dd5-112">Valor x mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="62dd5-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="62dd5-113">*r* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="62dd5-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dd5-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62dd5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62dd5-115">Valor x máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="62dd5-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="62dd5-116">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="62dd5-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dd5-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62dd5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62dd5-118">Valor y mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="62dd5-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="62dd5-119">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="62dd5-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dd5-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62dd5-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62dd5-121">Valor y máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="62dd5-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="62dd5-122">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62dd5-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dd5-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62dd5-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62dd5-124">Valor z mínimo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="62dd5-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="62dd5-125">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62dd5-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dd5-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62dd5-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62dd5-127">Valor z máximo del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="62dd5-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62dd5-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62dd5-128">Return value</span></span>

<span data-ttu-id="62dd5-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="62dd5-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="62dd5-130">Puntero a una estructura D3DXMATRIX que es una matriz de proyección de perspectiva personalizada y con forma de derecha.</span><span class="sxs-lookup"><span data-stu-id="62dd5-130">Pointer to a D3DXMATRIX structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="62dd5-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62dd5-131">Remarks</span></span>

<span data-ttu-id="62dd5-132">Todos los parámetros de la función D3DXMatrixPerspectiveOffCenterRH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="62dd5-132">All the parameters of the D3DXMatrixPerspectiveOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="62dd5-133">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="62dd5-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="62dd5-134">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="62dd5-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="62dd5-135">De esta manera, la función D3DXMatrixPerspectiveOffCenterRH se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="62dd5-135">In this way, the D3DXMatrixPerspectiveOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="62dd5-136">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="62dd5-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="62dd5-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62dd5-137">Requirements</span></span>



| <span data-ttu-id="62dd5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="62dd5-138">Requirement</span></span> | <span data-ttu-id="62dd5-139">Value</span><span class="sxs-lookup"><span data-stu-id="62dd5-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62dd5-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62dd5-140">Header</span></span><br/>  | <dl> <span data-ttu-id="62dd5-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="62dd5-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="62dd5-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62dd5-142">Library</span></span><br/> | <dl> <span data-ttu-id="62dd5-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62dd5-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62dd5-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="62dd5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62dd5-145">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="62dd5-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

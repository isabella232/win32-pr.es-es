---
description: Crea una matriz de proyección de perspectiva izquierda
ms.assetid: 5fd8da67-ff12-42fa-b915-b50fa2680b32
title: Función D3DXMatrixPerspectiveLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 400967b5e4a25244c50dbd6093fa2079700ba4eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721533"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a><span data-ttu-id="2ae54-103">Función D3DXMatrixPerspectiveLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2ae54-103">D3DXMatrixPerspectiveLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="2ae54-104">Crea una matriz de proyección de perspectiva izquierda</span><span class="sxs-lookup"><span data-stu-id="2ae54-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae54-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ae54-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="2ae54-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ae54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ae54-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2ae54-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae54-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ae54-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ae54-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2ae54-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2ae54-110">*w* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2ae54-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae54-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ae54-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ae54-112">Ancho del volumen de vista en el plano de vista próximo.</span><span class="sxs-lookup"><span data-stu-id="2ae54-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2ae54-113">*h* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2ae54-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae54-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ae54-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ae54-115">Alto del volumen de vista en el plano de vista próximo.</span><span class="sxs-lookup"><span data-stu-id="2ae54-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2ae54-116">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ae54-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae54-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ae54-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ae54-118">Valor Z del plano de vista próximo.</span><span class="sxs-lookup"><span data-stu-id="2ae54-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2ae54-119">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ae54-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae54-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ae54-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ae54-121">Valor Z del plano de vista lejano.</span><span class="sxs-lookup"><span data-stu-id="2ae54-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ae54-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ae54-122">Return value</span></span>

<span data-ttu-id="2ae54-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ae54-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ae54-124">Puntero a una estructura D3DXMATRIX que es una matriz de proyección de perspectiva izquierda.</span><span class="sxs-lookup"><span data-stu-id="2ae54-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ae54-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ae54-125">Remarks</span></span>

<span data-ttu-id="2ae54-126">Todos los parámetros de la función D3DXMatrixPerspectiveLH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="2ae54-126">All the parameters of the D3DXMatrixPerspectiveLH function are distances in camera space.</span></span> <span data-ttu-id="2ae54-127">Los parámetros describen las dimensiones del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="2ae54-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="2ae54-128">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="2ae54-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2ae54-129">De esta manera, la función D3DXMatrixPerspectiveLH se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="2ae54-129">In this way, the D3DXMatrixPerspectiveLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2ae54-130">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="2ae54-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="2ae54-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ae54-131">Requirements</span></span>



| <span data-ttu-id="2ae54-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae54-132">Requirement</span></span> | <span data-ttu-id="2ae54-133">Value</span><span class="sxs-lookup"><span data-stu-id="2ae54-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae54-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ae54-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2ae54-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ae54-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2ae54-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ae54-136">Library</span></span><br/> | <dl> <span data-ttu-id="2ae54-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ae54-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ae54-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ae54-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae54-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="2ae54-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

---
description: Crea una matriz que gira alrededor del eje z.
ms.assetid: a168ea24-0cec-4e1b-a128-e9dadedf190b
title: Función D3DXMatrixRotationZ (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3dfe1d3d43e4110c4e7554c75fba3ac89a69ccb3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280460"
---
# <a name="d3dxmatrixrotationz-function-d3dx10mathh"></a><span data-ttu-id="ed486-103">Función D3DXMatrixRotationZ (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ed486-103">D3DXMatrixRotationZ function (D3DX10Math.h)</span></span>

<span data-ttu-id="ed486-104">Crea una matriz que gira alrededor del eje z.</span><span class="sxs-lookup"><span data-stu-id="ed486-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed486-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed486-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="ed486-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed486-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed486-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ed486-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed486-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed486-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ed486-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ed486-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ed486-110">*Ángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed486-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed486-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed486-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed486-112">Ángulo de rotación, en radianes.</span><span class="sxs-lookup"><span data-stu-id="ed486-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="ed486-113">Los ángulos se miden en el sentido de las agujas del reloj cuando se ven desde el eje de giro (lado positivo) hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="ed486-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed486-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed486-114">Return value</span></span>

<span data-ttu-id="ed486-115">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed486-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ed486-116">Puntero a una estructura D3DXMATRIX girada alrededor del eje z.</span><span class="sxs-lookup"><span data-stu-id="ed486-116">Pointer to a D3DXMATRIX structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed486-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed486-117">Remarks</span></span>

<span data-ttu-id="ed486-118">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="ed486-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ed486-119">De esta manera, la función D3DXMatrixRotationZ se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="ed486-119">In this way, the D3DXMatrixRotationZ function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed486-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed486-120">Requirements</span></span>



| <span data-ttu-id="ed486-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed486-121">Requirement</span></span> | <span data-ttu-id="ed486-122">Value</span><span class="sxs-lookup"><span data-stu-id="ed486-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed486-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed486-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ed486-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed486-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ed486-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed486-125">Library</span></span><br/> | <dl> <span data-ttu-id="ed486-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed486-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed486-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed486-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed486-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="ed486-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

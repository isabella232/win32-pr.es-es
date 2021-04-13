---
description: Transforma una matriz (x, y, z, 1) por una matriz determinada.
ms.assetid: fd7ab674-5e42-4265-afad-ae5a00dabcdb
title: Función D3DXVec3TransformArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b515c98be82aa47801b333c4b25680e0e464b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362474"
---
# <a name="d3dxvec3transformarray-function-d3dx9mathh"></a><span data-ttu-id="32258-103">Función D3DXVec3TransformArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="32258-103">D3DXVec3TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="32258-104">Transforma una matriz (x, y, z, 1) por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="32258-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="32258-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32258-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="32258-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32258-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32258-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="32258-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32258-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="32258-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="32258-109">Puntero a la matriz [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="32258-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="32258-110">Retrasos  \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32258-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32258-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32258-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32258-112">Intervalo entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="32258-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="32258-113">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32258-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32258-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="32258-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="32258-115">Puntero a la matriz de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="32258-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="32258-116">*VStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32258-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32258-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32258-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32258-118">Intervalo entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="32258-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="32258-119">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32258-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32258-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="32258-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="32258-121">Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="32258-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="32258-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32258-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32258-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32258-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32258-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="32258-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32258-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32258-125">Return value</span></span>

<span data-ttu-id="32258-126">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="32258-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="32258-127">Puntero a una matriz transformada [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="32258-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="32258-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32258-128">Remarks</span></span>

<span data-ttu-id="32258-129">Esta función transforma la matriz *PV* (x, y, z, 1) de la matriz *PM*.</span><span class="sxs-lookup"><span data-stu-id="32258-129">This function transforms the array *pV* (x, y, z, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="32258-130">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="32258-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="32258-131">De esta manera, la función **D3DXVec3TransformArray** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="32258-131">In this way, the **D3DXVec3TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="32258-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32258-132">Requirements</span></span>



| <span data-ttu-id="32258-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="32258-133">Requirement</span></span> | <span data-ttu-id="32258-134">Value</span><span class="sxs-lookup"><span data-stu-id="32258-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32258-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32258-135">Header</span></span><br/>  | <dl> <span data-ttu-id="32258-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="32258-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="32258-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32258-137">Library</span></span><br/> | <dl> <span data-ttu-id="32258-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32258-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32258-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="32258-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32258-140">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="32258-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 

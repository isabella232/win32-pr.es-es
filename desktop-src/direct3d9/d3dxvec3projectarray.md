---
description: Proyecta una matriz (x, y, z, 0) del espacio de objeto en el espacio de la pantalla.
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: Función D3DXVec3ProjectArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f802d8ab564f2cbfe1cc60ad6aed13959bef9383
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718535"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a><span data-ttu-id="0aadd-103">Función D3DXVec3ProjectArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0aadd-103">D3DXVec3ProjectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="0aadd-104">Proyecta una matriz (x, y, z, 0) del espacio de objeto en el espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0aadd-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aadd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0aadd-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a><span data-ttu-id="0aadd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0aadd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aadd-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0aadd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0aadd-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0aadd-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0aadd-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="0aadd-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0aadd-110">Retrasos  \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aadd-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aadd-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0aadd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0aadd-112">Intervalo entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="0aadd-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="0aadd-113">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aadd-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aadd-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0aadd-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0aadd-115">Puntero a la estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="0aadd-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0aadd-116">*VStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aadd-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aadd-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0aadd-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0aadd-118">Intervalo entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="0aadd-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="0aadd-119">*pViewport* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aadd-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aadd-120">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="0aadd-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="0aadd-121">Puntero a una estructura [**D3DVIEWPORT9**](d3dviewport9.md) que representa la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="0aadd-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="0aadd-122">*pProjection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aadd-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aadd-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0aadd-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0aadd-124">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="0aadd-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0aadd-125">*pView* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aadd-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aadd-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0aadd-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0aadd-127">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz de la vista.</span><span class="sxs-lookup"><span data-stu-id="0aadd-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0aadd-128">*pWorld* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aadd-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aadd-129">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0aadd-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0aadd-130">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz universal.</span><span class="sxs-lookup"><span data-stu-id="0aadd-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0aadd-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0aadd-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aadd-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0aadd-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0aadd-133">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="0aadd-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aadd-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0aadd-134">Return value</span></span>

<span data-ttu-id="0aadd-135">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0aadd-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0aadd-136">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es la matriz proyectada desde el espacio de objeto hasta el espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0aadd-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aadd-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0aadd-137">Remarks</span></span>

<span data-ttu-id="0aadd-138">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="0aadd-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0aadd-139">De esta manera, la función **D3DXVec3ProjectArray** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="0aadd-139">In this way, the **D3DXVec3ProjectArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aadd-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aadd-140">Requirements</span></span>



| <span data-ttu-id="0aadd-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aadd-141">Requirement</span></span> | <span data-ttu-id="0aadd-142">Value</span><span class="sxs-lookup"><span data-stu-id="0aadd-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0aadd-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aadd-143">Header</span></span><br/>  | <dl> <span data-ttu-id="0aadd-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aadd-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0aadd-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0aadd-145">Library</span></span><br/> | <dl> <span data-ttu-id="0aadd-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0aadd-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0aadd-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aadd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aadd-148">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="0aadd-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0aadd-149">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="0aadd-149">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 

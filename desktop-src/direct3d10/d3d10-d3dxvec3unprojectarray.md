---
description: Proyecta una matriz (x, y, z, 0) del espacio de pantalla en el espacio de objeto.
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: Función D3DXVec3UnprojectArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c7293339145253f817e8ed8b6812906b49792193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678775"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a><span data-ttu-id="c1e8f-103">Función D3DXVec3UnprojectArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c1e8f-103">D3DXVec3UnprojectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="c1e8f-104">Proyecta una matriz (x, y, z, 0) del espacio de pantalla en el espacio de objeto.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1e8f-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a><span data-ttu-id="c1e8f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1e8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e8f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8f-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1e8f-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c1e8f-109">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c1e8f-110">Retrasos  \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8f-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1e8f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1e8f-112">Intervalo entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c1e8f-113">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8f-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1e8f-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c1e8f-115">Puntero a la estructura de D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="c1e8f-116">*VStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8f-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1e8f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1e8f-118">Intervalo entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c1e8f-119">*pViewport* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8f-120">Tipo: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="c1e8f-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="c1e8f-121">Puntero a una [**\_ ventanilla D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)que representa la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="c1e8f-122">*pProjection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8f-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1e8f-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c1e8f-124">Puntero a una estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que representa la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="c1e8f-125">*pView* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8f-126">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1e8f-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c1e8f-127">Puntero a una estructura D3DXMATRIX que representa la matriz de la vista.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="c1e8f-128">*pWorld* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8f-129">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1e8f-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c1e8f-130">Puntero a una estructura D3DXMATRIX que representa la matriz universal.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="c1e8f-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8f-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1e8f-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1e8f-133">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e8f-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1e8f-134">Return value</span></span>

<span data-ttu-id="c1e8f-135">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1e8f-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c1e8f-136">Puntero a una estructura D3DXVECTOR3 que es la matriz proyectada desde el espacio de la pantalla hasta el espacio del objeto.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-136">Pointer to a D3DXVECTOR3 structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e8f-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1e8f-137">Remarks</span></span>

<span data-ttu-id="c1e8f-138">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c1e8f-139">De esta manera, la función [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="c1e8f-139">In this way, the [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e8f-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1e8f-140">Requirements</span></span>



| <span data-ttu-id="c1e8f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1e8f-141">Requirement</span></span> | <span data-ttu-id="c1e8f-142">Value</span><span class="sxs-lookup"><span data-stu-id="c1e8f-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e8f-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1e8f-143">Header</span></span><br/> | <dl> <span data-ttu-id="c1e8f-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e8f-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e8f-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1e8f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e8f-146">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c1e8f-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

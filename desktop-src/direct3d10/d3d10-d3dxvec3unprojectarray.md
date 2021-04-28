---
description: 'Función D3DXVec3UnprojectArray (D3DX10Math.h): proyecta una matriz (x, y, z, 0) desde el espacio de pantalla al espacio de objetos.'
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: Función D3DXVec3UnprojectArray (D3DX10Math.h)
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
ms.openlocfilehash: 727744445e952fa0135feff944c768aaba1aba36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103013"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a><span data-ttu-id="c8371-103">Función D3DXVec3UnprojectArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="c8371-103">D3DXVec3UnprojectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="c8371-104">Proyecta una matriz (x, y, z, 0) desde el espacio de pantalla al espacio de objetos.</span><span class="sxs-lookup"><span data-stu-id="c8371-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8371-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8371-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c8371-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8371-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8371-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c8371-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8371-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8371-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8371-109">Puntero a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c8371-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8371-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8371-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8371-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8371-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8371-112">Pasos entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="c8371-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c8371-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8371-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8371-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8371-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8371-115">Puntero a la estructura D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="c8371-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="c8371-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8371-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8371-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8371-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8371-118">Pasos entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8371-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c8371-119">*pViewport* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8371-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8371-120">Tipo: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="c8371-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="c8371-121">Puntero a una [**ventanilla D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)que representa la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="c8371-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="c8371-122">*pProjection* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8371-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8371-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8371-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8371-124">Puntero a una [**estructura D3DXMATRIX,**](d3d10-d3dxmatrix.md) que representa la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="c8371-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="c8371-125">*pView* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8371-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8371-126">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8371-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8371-127">Puntero a una estructura D3DXMATRIX, que representa la matriz de vistas.</span><span class="sxs-lookup"><span data-stu-id="c8371-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="c8371-128">*pWorld* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8371-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8371-129">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8371-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8371-130">Puntero a una estructura D3DXMATRIX, que representa la matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="c8371-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="c8371-131">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c8371-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8371-132">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8371-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8371-133">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c8371-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8371-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8371-134">Return value</span></span>

<span data-ttu-id="c8371-135">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8371-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8371-136">Puntero a una estructura D3DXVECTOR3 que es la matriz proyectada desde el espacio de pantalla al espacio de objetos.</span><span class="sxs-lookup"><span data-stu-id="c8371-136">Pointer to a D3DXVECTOR3 structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8371-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8371-137">Remarks</span></span>

<span data-ttu-id="c8371-138">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="c8371-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c8371-139">De esta manera, la [**función D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="c8371-139">In this way, the [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8371-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8371-140">Requirements</span></span>



| <span data-ttu-id="c8371-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8371-141">Requirement</span></span> | <span data-ttu-id="c8371-142">Value</span><span class="sxs-lookup"><span data-stu-id="c8371-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8371-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8371-143">Header</span></span><br/> | <dl> <span data-ttu-id="c8371-144"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c8371-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8371-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c8371-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8371-146">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c8371-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

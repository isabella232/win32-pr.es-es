---
description: Proyecta una matriz (x, y, z, 0) del espacio de pantalla en el espacio de objeto.
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: Función D3DXVec3UnprojectArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3af4cc05b5f8ee30c624f904df7e2ae5cd4b844a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003936"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a><span data-ttu-id="261ae-103">Función D3DXVec3UnprojectArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="261ae-103">D3DXVec3UnprojectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="261ae-104">Proyecta una matriz (x, y, z, 0) del espacio de pantalla en el espacio de objeto.</span><span class="sxs-lookup"><span data-stu-id="261ae-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="261ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="261ae-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
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



## <a name="parameters"></a><span data-ttu-id="261ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="261ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="261ae-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="261ae-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="261ae-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="261ae-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="261ae-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="261ae-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="261ae-110">Retrasos  \[ de\]</span><span class="sxs-lookup"><span data-stu-id="261ae-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261ae-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="261ae-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="261ae-112">Intervalo entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="261ae-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="261ae-113">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="261ae-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261ae-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="261ae-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="261ae-115">Puntero a la estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="261ae-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="261ae-116">*VStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="261ae-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261ae-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="261ae-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="261ae-118">Intervalo entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="261ae-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="261ae-119">*pViewport* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="261ae-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261ae-120">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="261ae-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="261ae-121">Puntero a una estructura [**D3DVIEWPORT9**](d3dviewport9.md) que representa la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="261ae-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="261ae-122">*pProjection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="261ae-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261ae-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="261ae-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="261ae-124">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="261ae-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="261ae-125">*pView* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="261ae-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261ae-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="261ae-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="261ae-127">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz de la vista.</span><span class="sxs-lookup"><span data-stu-id="261ae-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="261ae-128">*pWorld* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="261ae-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261ae-129">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="261ae-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="261ae-130">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz universal.</span><span class="sxs-lookup"><span data-stu-id="261ae-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="261ae-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="261ae-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="261ae-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="261ae-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="261ae-133">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="261ae-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="261ae-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="261ae-134">Return value</span></span>

<span data-ttu-id="261ae-135">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="261ae-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="261ae-136">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es la matriz proyectada desde el espacio de la pantalla hasta el espacio del objeto.</span><span class="sxs-lookup"><span data-stu-id="261ae-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="261ae-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="261ae-137">Remarks</span></span>

<span data-ttu-id="261ae-138">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="261ae-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="261ae-139">De esta manera, la función [**D3DXVec3Unproject**](d3dxvec3unproject.md) se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="261ae-139">In this way, the [**D3DXVec3Unproject**](d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="261ae-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="261ae-140">Requirements</span></span>



| <span data-ttu-id="261ae-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="261ae-141">Requirement</span></span> | <span data-ttu-id="261ae-142">Value</span><span class="sxs-lookup"><span data-stu-id="261ae-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="261ae-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="261ae-143">Header</span></span><br/>  | <dl> <span data-ttu-id="261ae-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="261ae-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="261ae-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="261ae-145">Library</span></span><br/> | <dl> <span data-ttu-id="261ae-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="261ae-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="261ae-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="261ae-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="261ae-148">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="261ae-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="261ae-149">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="261ae-149">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 

---
description: 'Función D3DXVec3UnprojectArray (D3dx9math.h): proyecta una matriz (x, y, z, 0) desde el espacio de pantalla al espacio del objeto.'
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: Función D3DXVec3UnprojectArray (D3dx9math.h)
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
ms.openlocfilehash: 67e42b30a8f8d44bb9b21668a515a202436b7631
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097723"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a><span data-ttu-id="230b7-103">Función D3DXVec3UnprojectArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="230b7-103">D3DXVec3UnprojectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="230b7-104">Proyecta una matriz (x, y, z, 0) desde el espacio de pantalla al espacio de objetos.</span><span class="sxs-lookup"><span data-stu-id="230b7-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="230b7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="230b7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="230b7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="230b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="230b7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="230b7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="230b7-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="230b7-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="230b7-109">Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="230b7-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="230b7-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="230b7-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230b7-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="230b7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="230b7-112">Pasos entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="230b7-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="230b7-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="230b7-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230b7-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="230b7-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="230b7-115">Puntero a la estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.</span><span class="sxs-lookup"><span data-stu-id="230b7-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="230b7-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="230b7-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230b7-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="230b7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="230b7-118">Pasos entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="230b7-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="230b7-119">*pViewport* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="230b7-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230b7-120">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="230b7-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="230b7-121">Puntero a una [**estructura D3DVIEWPORT9,**](d3dviewport9.md) que representa la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="230b7-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="230b7-122">*pProjection* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="230b7-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230b7-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="230b7-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="230b7-124">Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="230b7-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="230b7-125">*pView* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="230b7-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230b7-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="230b7-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="230b7-127">Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz de vistas.</span><span class="sxs-lookup"><span data-stu-id="230b7-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="230b7-128">*pWorld* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="230b7-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230b7-129">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="230b7-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="230b7-130">Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="230b7-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="230b7-131">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="230b7-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="230b7-132">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="230b7-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="230b7-133">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="230b7-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="230b7-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="230b7-134">Return value</span></span>

<span data-ttu-id="230b7-135">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="230b7-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="230b7-136">Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) que es la matriz proyectada desde el espacio de pantalla al espacio de objetos.</span><span class="sxs-lookup"><span data-stu-id="230b7-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="230b7-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="230b7-137">Remarks</span></span>

<span data-ttu-id="230b7-138">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="230b7-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="230b7-139">De esta manera, la [**función D3DXVec3Unproject**](d3dxvec3unproject.md) se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="230b7-139">In this way, the [**D3DXVec3Unproject**](d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="230b7-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="230b7-140">Requirements</span></span>



| <span data-ttu-id="230b7-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="230b7-141">Requirement</span></span> | <span data-ttu-id="230b7-142">Value</span><span class="sxs-lookup"><span data-stu-id="230b7-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="230b7-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="230b7-143">Header</span></span><br/>  | <dl> <span data-ttu-id="230b7-144"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="230b7-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="230b7-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="230b7-145">Library</span></span><br/> | <dl> <span data-ttu-id="230b7-146"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="230b7-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="230b7-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="230b7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230b7-148">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="230b7-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="230b7-149">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="230b7-149">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 

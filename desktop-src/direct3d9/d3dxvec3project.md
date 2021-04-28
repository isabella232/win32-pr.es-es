---
description: 'Función D3DXVec3Project (D3dx9math.h): proyecta un vector 3D desde el espacio de objetos en el espacio de la pantalla.'
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: Función D3DXVec3Project (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5a9abcb54c883d74bde831570b9df0b40fedfae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115653"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a><span data-ttu-id="10791-103">Función D3DXVec3Project (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="10791-103">D3DXVec3Project function (D3dx9math.h)</span></span>

<span data-ttu-id="10791-104">Proyecta un vector 3D desde el espacio del objeto en el espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="10791-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="10791-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10791-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="10791-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10791-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="10791-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="10791-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="10791-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="10791-109">Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="10791-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="10791-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="10791-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10791-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="10791-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="10791-112">Puntero a la estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.</span><span class="sxs-lookup"><span data-stu-id="10791-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="10791-113">*pViewport* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="10791-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10791-114">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="10791-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="10791-115">Puntero a una [**estructura D3DVIEWPORT9,**](d3dviewport9.md) que representa la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="10791-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="10791-116">*pProjection* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="10791-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10791-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="10791-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="10791-118">Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="10791-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="10791-119">*pView* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="10791-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10791-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="10791-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="10791-121">Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz de vistas.</span><span class="sxs-lookup"><span data-stu-id="10791-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="10791-122">*pWorld* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="10791-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10791-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="10791-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="10791-124">Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="10791-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10791-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10791-125">Return value</span></span>

<span data-ttu-id="10791-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="10791-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="10791-127">Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el vector proyectado desde el espacio del objeto al espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="10791-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="10791-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10791-128">Remarks</span></span>

<span data-ttu-id="10791-129">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="10791-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="10791-130">De esta manera, la **función D3DXVec3Project** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="10791-130">In this way, the **D3DXVec3Project** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="10791-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10791-131">Requirements</span></span>



| <span data-ttu-id="10791-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="10791-132">Requirement</span></span> | <span data-ttu-id="10791-133">Value</span><span class="sxs-lookup"><span data-stu-id="10791-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10791-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10791-134">Header</span></span><br/>  | <dl> <span data-ttu-id="10791-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="10791-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="10791-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10791-136">Library</span></span><br/> | <dl> <span data-ttu-id="10791-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="10791-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="10791-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="10791-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10791-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="10791-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="10791-140">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="10791-140">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 





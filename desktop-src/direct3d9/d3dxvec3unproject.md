---
description: Proyecta un vector a partir del espacio de la pantalla en el espacio de objeto.
ms.assetid: 9fd69cae-1d9c-4fae-9e15-8eb9950b4850
title: Función D3DXVec3Unproject (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bab9af4a2c88a3e3b3b7f342b6c7c9cc89ceb66
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362724"
---
# <a name="d3dxvec3unproject-function-d3dx9mathh"></a><span data-ttu-id="b51b2-103">Función D3DXVec3Unproject (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b51b2-103">D3DXVec3Unproject function (D3dx9math.h)</span></span>

<span data-ttu-id="b51b2-104">Proyecta un vector a partir del espacio de la pantalla en el espacio de objeto.</span><span class="sxs-lookup"><span data-stu-id="b51b2-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="b51b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b51b2-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="b51b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b51b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b51b2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b51b2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b51b2-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b51b2-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b51b2-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b51b2-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b51b2-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b51b2-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b51b2-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b51b2-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b51b2-112">Puntero a la estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="b51b2-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b51b2-113">*pViewport* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b51b2-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b51b2-114">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="b51b2-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="b51b2-115">Puntero a una estructura [**D3DVIEWPORT9**](d3dviewport9.md) que representa la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="b51b2-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="b51b2-116">*pProjection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b51b2-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b51b2-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b51b2-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b51b2-118">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="b51b2-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="b51b2-119">*pView* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b51b2-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b51b2-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b51b2-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b51b2-121">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz de la vista.</span><span class="sxs-lookup"><span data-stu-id="b51b2-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="b51b2-122">*pWorld* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b51b2-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b51b2-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b51b2-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b51b2-124">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz universal.</span><span class="sxs-lookup"><span data-stu-id="b51b2-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b51b2-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b51b2-125">Return value</span></span>

<span data-ttu-id="b51b2-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b51b2-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b51b2-127">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el vector proyectado desde el espacio de la pantalla hasta el espacio del objeto.</span><span class="sxs-lookup"><span data-stu-id="b51b2-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="b51b2-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b51b2-128">Remarks</span></span>

<span data-ttu-id="b51b2-129">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="b51b2-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b51b2-130">De esta manera, la función **D3DXVec3Unproject** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="b51b2-130">In this way, the **D3DXVec3Unproject** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b51b2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b51b2-131">Requirements</span></span>



| <span data-ttu-id="b51b2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b51b2-132">Requirement</span></span> | <span data-ttu-id="b51b2-133">Value</span><span class="sxs-lookup"><span data-stu-id="b51b2-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b51b2-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b51b2-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b51b2-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b51b2-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b51b2-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b51b2-136">Library</span></span><br/> | <dl> <span data-ttu-id="b51b2-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b51b2-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b51b2-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b51b2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b51b2-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="b51b2-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b51b2-140">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="b51b2-140">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 





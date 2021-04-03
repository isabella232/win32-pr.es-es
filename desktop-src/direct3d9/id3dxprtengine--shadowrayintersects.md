---
description: Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla. Normalmente se usa para determinar si un punto determinado está en sombra.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'ID3DXPRTEngine:: ShadowRayIntersects (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083747"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a><span data-ttu-id="abaca-104">ID3DXPRTEngine:: ShadowRayIntersects (método)</span><span class="sxs-lookup"><span data-stu-id="abaca-104">ID3DXPRTEngine::ShadowRayIntersects method</span></span>

<span data-ttu-id="abaca-105">Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla.</span><span class="sxs-lookup"><span data-stu-id="abaca-105">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="abaca-106">Normalmente se usa para determinar si un punto determinado está en sombra.</span><span class="sxs-lookup"><span data-stu-id="abaca-106">Typically used to determine whether a given point is in shadow.</span></span>

## <a name="syntax"></a><span data-ttu-id="abaca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abaca-107">Syntax</span></span>


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a><span data-ttu-id="abaca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abaca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abaca-109">*pRayPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abaca-109">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abaca-110">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="abaca-110">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="abaca-111">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica el punto en el que comienza el rayo.</span><span class="sxs-lookup"><span data-stu-id="abaca-111">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="abaca-112">*pRayDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abaca-112">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abaca-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="abaca-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="abaca-114">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la dirección normalizada del rayo.</span><span class="sxs-lookup"><span data-stu-id="abaca-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abaca-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abaca-115">Return value</span></span>

<span data-ttu-id="abaca-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abaca-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abaca-117">Devuelve **true** si el rayo forma una intersección con la malla actual; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="abaca-117">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="abaca-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abaca-118">Remarks</span></span>

<span data-ttu-id="abaca-119">Use [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para establecer las distancias mínima y máxima de intersección con el rayo.</span><span class="sxs-lookup"><span data-stu-id="abaca-119">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="abaca-120">Este método se ejecuta más rápido que [**ID3DXPRTEngine:: ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="abaca-120">This method executes faster than [**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abaca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abaca-121">Requirements</span></span>



| <span data-ttu-id="abaca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="abaca-122">Requirement</span></span> | <span data-ttu-id="abaca-123">Value</span><span class="sxs-lookup"><span data-stu-id="abaca-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abaca-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abaca-124">Header</span></span><br/>  | <dl> <span data-ttu-id="abaca-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="abaca-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="abaca-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="abaca-126">Library</span></span><br/> | <dl> <span data-ttu-id="abaca-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abaca-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="abaca-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="abaca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abaca-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="abaca-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="abaca-130">**ID3DXPRTEngine::ClosestRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="abaca-130">**ID3DXPRTEngine::ClosestRayIntersects**</span></span>](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[<span data-ttu-id="abaca-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="abaca-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 

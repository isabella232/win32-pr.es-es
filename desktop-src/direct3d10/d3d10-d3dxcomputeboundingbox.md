---
description: 'Función D3DXComputeBoundingBox (D3DX10math.h): calcula un cuadro de límite orientado al eje de coordenadas.'
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: Función D3DXComputeBoundingBox (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a12e7e302fb36ffb8856e6402f110e01bb2afb2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103533"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="bc0a3-103">Función D3DXComputeBoundingBox (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="bc0a3-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="bc0a3-104">Calcula un rectángulo de selección orientado al eje de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="bc0a3-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc0a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc0a3-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="bc0a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc0a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc0a3-107">*pFirstPosition* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bc0a3-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0a3-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc0a3-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bc0a3-109">Puntero a la primera posición.</span><span class="sxs-lookup"><span data-stu-id="bc0a3-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="bc0a3-110">*NumVertices* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bc0a3-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0a3-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc0a3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc0a3-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="bc0a3-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="bc0a3-113">*dwStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bc0a3-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0a3-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc0a3-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc0a3-115">Recuento o número de bytes entre vértices.</span><span class="sxs-lookup"><span data-stu-id="bc0a3-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="bc0a3-116">*pMin* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bc0a3-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0a3-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc0a3-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bc0a3-118">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) que describe la esquina inferior izquierda devuelta del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="bc0a3-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="bc0a3-119">*pMax* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bc0a3-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0a3-120">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc0a3-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bc0a3-121">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) que describe la esquina superior derecha devuelta del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="bc0a3-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc0a3-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc0a3-122">Return value</span></span>

<span data-ttu-id="bc0a3-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc0a3-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc0a3-124">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc0a3-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bc0a3-125">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bc0a3-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0a3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc0a3-126">Requirements</span></span>



| <span data-ttu-id="bc0a3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc0a3-127">Requirement</span></span> | <span data-ttu-id="bc0a3-128">Value</span><span class="sxs-lookup"><span data-stu-id="bc0a3-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0a3-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc0a3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bc0a3-130"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bc0a3-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="bc0a3-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc0a3-131">Library</span></span><br/> | <dl> <span data-ttu-id="bc0a3-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc0a3-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc0a3-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bc0a3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0a3-134">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="bc0a3-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 

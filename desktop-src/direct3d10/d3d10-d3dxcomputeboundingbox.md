---
description: Calcula un cuadro de límite orientado al eje de coordenadas.
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: Función D3DXComputeBoundingBox (D3DX10math. h)
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
ms.openlocfilehash: 9a93eb4a10f6c2b2fd7eda82afcc21158138a1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708015"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="640d5-103">Función D3DXComputeBoundingBox (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="640d5-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="640d5-104">Calcula un cuadro de límite orientado al eje de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="640d5-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="640d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="640d5-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="640d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="640d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="640d5-107">*pFirstPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="640d5-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640d5-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="640d5-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="640d5-109">Puntero a la primera posición.</span><span class="sxs-lookup"><span data-stu-id="640d5-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="640d5-110">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="640d5-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640d5-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="640d5-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="640d5-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="640d5-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="640d5-113">*dwStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="640d5-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640d5-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="640d5-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="640d5-115">Recuento o número de bytes entre los vértices.</span><span class="sxs-lookup"><span data-stu-id="640d5-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="640d5-116">*pMin* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="640d5-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="640d5-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="640d5-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="640d5-118">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que describe la esquina inferior izquierda devuelta del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="640d5-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="640d5-119">*pMax* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="640d5-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="640d5-120">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="640d5-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="640d5-121">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que describe la esquina superior derecha devuelta del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="640d5-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="640d5-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="640d5-122">Return value</span></span>

<span data-ttu-id="640d5-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="640d5-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="640d5-124">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="640d5-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="640d5-125">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="640d5-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="640d5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="640d5-126">Requirements</span></span>



| <span data-ttu-id="640d5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="640d5-127">Requirement</span></span> | <span data-ttu-id="640d5-128">Value</span><span class="sxs-lookup"><span data-stu-id="640d5-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="640d5-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="640d5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="640d5-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="640d5-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="640d5-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="640d5-131">Library</span></span><br/> | <dl> <span data-ttu-id="640d5-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="640d5-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="640d5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="640d5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640d5-134">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="640d5-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 

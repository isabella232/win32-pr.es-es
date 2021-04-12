---
description: Calcula un cuadro de límite orientado al eje de coordenadas.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Función D3DXComputeBoundingBox (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df0376428153cfc02e499c9e26226cce81154023
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280361"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a><span data-ttu-id="cde3a-103">Función D3DXComputeBoundingBox (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="cde3a-103">D3DXComputeBoundingBox function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="cde3a-104">Calcula un cuadro de límite orientado al eje de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="cde3a-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde3a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cde3a-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="cde3a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cde3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cde3a-107">*pFirstPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cde3a-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde3a-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cde3a-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cde3a-109">Puntero a la primera posición.</span><span class="sxs-lookup"><span data-stu-id="cde3a-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="cde3a-110">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cde3a-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde3a-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cde3a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cde3a-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="cde3a-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="cde3a-113">*dwStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cde3a-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde3a-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cde3a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cde3a-115">Recuento o número de bytes entre los vértices.</span><span class="sxs-lookup"><span data-stu-id="cde3a-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="cde3a-116">*pMin* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cde3a-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cde3a-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cde3a-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cde3a-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la esquina inferior izquierda devuelta del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="cde3a-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span> <span data-ttu-id="cde3a-119">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="cde3a-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cde3a-120">*pMax* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cde3a-120">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cde3a-121">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cde3a-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cde3a-122">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que describe la esquina superior derecha devuelta del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="cde3a-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span> <span data-ttu-id="cde3a-123">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="cde3a-123">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cde3a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cde3a-124">Return value</span></span>

<span data-ttu-id="cde3a-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cde3a-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cde3a-126">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cde3a-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cde3a-127">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cde3a-127">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cde3a-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cde3a-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cde3a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cde3a-129">Requirements</span></span>



| <span data-ttu-id="cde3a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde3a-130">Requirement</span></span> | <span data-ttu-id="cde3a-131">Value</span><span class="sxs-lookup"><span data-stu-id="cde3a-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cde3a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cde3a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="cde3a-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cde3a-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cde3a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cde3a-134">Library</span></span><br/> | <dl> <span data-ttu-id="cde3a-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cde3a-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cde3a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="cde3a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde3a-137">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="cde3a-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

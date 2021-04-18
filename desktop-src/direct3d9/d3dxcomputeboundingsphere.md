---
description: Calcula una esfera de límite para la malla.
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: Función D3DXComputeBoundingSphere (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9e6a0c9fb67abe8a98ccf8b3f9b895fd63fc3e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721466"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a><span data-ttu-id="06dea-103">Función D3DXComputeBoundingSphere (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="06dea-103">D3DXComputeBoundingSphere function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="06dea-104">Calcula una esfera de límite para la malla.</span><span class="sxs-lookup"><span data-stu-id="06dea-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="06dea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06dea-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="06dea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06dea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06dea-107">*pFirstPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06dea-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06dea-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="06dea-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="06dea-109">Puntero a la primera posición.</span><span class="sxs-lookup"><span data-stu-id="06dea-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="06dea-110">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06dea-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06dea-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06dea-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06dea-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="06dea-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="06dea-113">*dwStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06dea-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06dea-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06dea-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06dea-115">Número de bytes entre los vectores de posición.</span><span class="sxs-lookup"><span data-stu-id="06dea-115">Number of bytes between position vectors.</span></span> <span data-ttu-id="06dea-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)o [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) para obtener el intervalo de vértice.</span><span class="sxs-lookup"><span data-stu-id="06dea-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md), or [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) to get the vertex stride.</span></span>

</dd> <dt>

<span data-ttu-id="06dea-117">*pCenter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06dea-117">*pCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06dea-118">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="06dea-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="06dea-119">Estructura [**D3DXVECTOR3**](d3dxvector3.md) , que define el centro de coordenadas de la esfera de límite devuelta.</span><span class="sxs-lookup"><span data-stu-id="06dea-119">[**D3DXVECTOR3**](d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="06dea-120">*pRadius* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06dea-120">*pRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06dea-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="06dea-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06dea-122">Radio de la esfera de límite devuelta.</span><span class="sxs-lookup"><span data-stu-id="06dea-122">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06dea-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06dea-123">Return value</span></span>

<span data-ttu-id="06dea-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06dea-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06dea-125">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06dea-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06dea-126">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="06dea-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="06dea-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06dea-127">Requirements</span></span>



| <span data-ttu-id="06dea-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="06dea-128">Requirement</span></span> | <span data-ttu-id="06dea-129">Value</span><span class="sxs-lookup"><span data-stu-id="06dea-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06dea-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06dea-130">Header</span></span><br/>  | <dl> <span data-ttu-id="06dea-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="06dea-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="06dea-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06dea-132">Library</span></span><br/> | <dl> <span data-ttu-id="06dea-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06dea-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06dea-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="06dea-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06dea-135">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="06dea-135">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

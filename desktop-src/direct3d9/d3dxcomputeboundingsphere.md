---
description: 'Función D3DXComputeBoundingSphere (D3DX9Mesh.h): calcula una esfera de límite para la malla.'
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: Función D3DXComputeBoundingSphere (D3DX9Mesh.h)
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
ms.openlocfilehash: dbfccb13dfe15b06de98ddba114cdc62c5f4ec05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115823"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a><span data-ttu-id="91b16-103">Función D3DXComputeBoundingSphere (D3DX9Mesh.h)</span><span class="sxs-lookup"><span data-stu-id="91b16-103">D3DXComputeBoundingSphere function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="91b16-104">Calcula una esfera de límite para la malla.</span><span class="sxs-lookup"><span data-stu-id="91b16-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91b16-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="91b16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91b16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91b16-107">*pFirstPosition* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="91b16-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b16-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="91b16-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="91b16-109">Puntero a la primera posición.</span><span class="sxs-lookup"><span data-stu-id="91b16-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="91b16-110">*NumVertices* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="91b16-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b16-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91b16-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91b16-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="91b16-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="91b16-113">*dwStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="91b16-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b16-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91b16-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91b16-115">Número de bytes entre vectores de posición.</span><span class="sxs-lookup"><span data-stu-id="91b16-115">Number of bytes between position vectors.</span></span> <span data-ttu-id="91b16-116">Use [**GetNumBytesPerVertex,**](id3dxbasemesh--getnumbytespervertex.md) [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)o [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) para obtener el paso de vértice.</span><span class="sxs-lookup"><span data-stu-id="91b16-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md), or [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) to get the vertex stride.</span></span>

</dd> <dt>

<span data-ttu-id="91b16-117">*pCenter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="91b16-117">*pCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91b16-118">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="91b16-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="91b16-119">[**Estructura D3DXVECTOR3,**](d3dxvector3.md) que define el centro de coordenadas de la esfera de límite devuelta.</span><span class="sxs-lookup"><span data-stu-id="91b16-119">[**D3DXVECTOR3**](d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="91b16-120">*pRadius* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="91b16-120">*pRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91b16-121">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="91b16-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="91b16-122">Radio de la esfera de límite devuelta.</span><span class="sxs-lookup"><span data-stu-id="91b16-122">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91b16-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91b16-123">Return value</span></span>

<span data-ttu-id="91b16-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91b16-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91b16-125">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91b16-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="91b16-126">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="91b16-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="91b16-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91b16-127">Requirements</span></span>



| <span data-ttu-id="91b16-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="91b16-128">Requirement</span></span> | <span data-ttu-id="91b16-129">Value</span><span class="sxs-lookup"><span data-stu-id="91b16-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91b16-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91b16-130">Header</span></span><br/>  | <dl> <span data-ttu-id="91b16-131"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="91b16-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="91b16-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91b16-132">Library</span></span><br/> | <dl> <span data-ttu-id="91b16-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="91b16-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91b16-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="91b16-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b16-135">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="91b16-135">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

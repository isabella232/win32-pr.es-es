---
description: Crea un objeto ID3DXPRTEngine que puede generar de forma eficaz simulaciones de transferencia Radiance (PRT) precalculadas de una escena 3D.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: Función D3DXCreatePRTEngine (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547931"
---
# <a name="d3dxcreateprtengine-function"></a><span data-ttu-id="633dc-103">D3DXCreatePRTEngine función)</span><span class="sxs-lookup"><span data-stu-id="633dc-103">D3DXCreatePRTEngine function</span></span>

<span data-ttu-id="633dc-104">Crea un objeto [**ID3DXPRTEngine**](id3dxprtengine.md) que puede generar de forma eficaz simulaciones de transferencia Radiance (PRT) precalculadas de una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="633dc-104">Creates an [**ID3DXPRTEngine**](id3dxprtengine.md) object that can efficiently generate precomputed radiance transfer (PRT) simulations of a 3D scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="633dc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="633dc-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a><span data-ttu-id="633dc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="633dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="633dc-107">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="633dc-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633dc-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="633dc-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="633dc-109">Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de entrada que modela la escena 3D.</span><span class="sxs-lookup"><span data-stu-id="633dc-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object that models the 3D scene.</span></span> <span data-ttu-id="633dc-110">Esta malla debe tener una tabla de atributos en la que los vértices se encuentren en un atributo único.</span><span class="sxs-lookup"><span data-stu-id="633dc-110">This mesh must have an attribute table in which vertices are in a unique attribute.</span></span>

</dd> <dt>

<span data-ttu-id="633dc-111">*pAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="633dc-111">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633dc-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="633dc-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="633dc-113">Puntero opcional a una matriz de tres DWORDs por cada tipo que se va a rellenar con índices de caras adyacentes.</span><span class="sxs-lookup"><span data-stu-id="633dc-113">Optional pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="633dc-114">El número de bytes de esta matriz debe ser al menos ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="633dc-114">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span> <span data-ttu-id="633dc-115">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="633dc-115">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="633dc-116">*ExtractUVs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="633dc-116">*ExtractUVs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633dc-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="633dc-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="633dc-118">Si **es true**, las texturas se usarán para almacenar vectores ALBEDOS o PRT.</span><span class="sxs-lookup"><span data-stu-id="633dc-118">If **TRUE**, textures will be used to store albedos or PRT vectors.</span></span>

</dd> <dt>

<span data-ttu-id="633dc-119">*pBlockerMesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="633dc-119">*pBlockerMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633dc-120">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="633dc-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="633dc-121">Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) opcional que bloquea la escena 3D.</span><span class="sxs-lookup"><span data-stu-id="633dc-121">Pointer to an optional [**ID3DXMesh**](id3dxmesh.md) mesh object that blocks the 3D scene.</span></span> <span data-ttu-id="633dc-122">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="633dc-122">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="633dc-123">*ppEngine* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="633dc-123">*ppEngine* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="633dc-124">Tipo: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**</span><span class="sxs-lookup"><span data-stu-id="633dc-124">Type: **[**LPD3DXPRTENGINE**](id3dxprtengine.md)**</span></span>

<span data-ttu-id="633dc-125">Puntero a un objeto [**ID3DXPRTEngine**](id3dxprtengine.md) de salida.</span><span class="sxs-lookup"><span data-stu-id="633dc-125">Pointer to an output [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="633dc-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="633dc-126">Return value</span></span>

<span data-ttu-id="633dc-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="633dc-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="633dc-128">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="633dc-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="633dc-129">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="633dc-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="633dc-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="633dc-130">Remarks</span></span>

<span data-ttu-id="633dc-131">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) para combinar varias mallas en una sola interfaz de malla.</span><span class="sxs-lookup"><span data-stu-id="633dc-131">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to combine multiple meshes into a single mesh interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="633dc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="633dc-132">Requirements</span></span>



| <span data-ttu-id="633dc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="633dc-133">Requirement</span></span> | <span data-ttu-id="633dc-134">Value</span><span class="sxs-lookup"><span data-stu-id="633dc-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="633dc-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="633dc-135">Header</span></span><br/>  | <dl> <span data-ttu-id="633dc-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="633dc-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="633dc-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="633dc-137">Library</span></span><br/> | <dl> <span data-ttu-id="633dc-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="633dc-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="633dc-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="633dc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633dc-140">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="633dc-140">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 

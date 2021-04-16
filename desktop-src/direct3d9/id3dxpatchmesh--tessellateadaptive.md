---
description: Realiza una teselación adaptativa basada en el criterio de teselación adaptable basado en z.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'ID3DXPatchMesh:: TessellateAdaptive (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670245"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a><span data-ttu-id="ddbdc-103">ID3DXPatchMesh:: TessellateAdaptive (método)</span><span class="sxs-lookup"><span data-stu-id="ddbdc-103">ID3DXPatchMesh::TessellateAdaptive method</span></span>

<span data-ttu-id="ddbdc-104">Realiza una teselación adaptativa basada en el criterio de teselación adaptable basado en z.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-104">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddbdc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddbdc-105">Syntax</span></span>


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="ddbdc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddbdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddbdc-107">*pTrans* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ddbdc-107">*pTrans* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddbdc-108">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="ddbdc-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ddbdc-109">Especifica un vector 4D con puntos con los vértices para obtener la cantidad de teselación adaptable por vértice.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-109">Specifies a 4D vector that is dotted with the vertices to get the per-vertex adaptive tessellation amount.</span></span> <span data-ttu-id="ddbdc-110">Cada borde se Tesela en el valor medio de los niveles de teselación de los dos vértices que conecta.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-110">Each edge is tessellated to the average value of the tessellation levels for the two vertices it connects.</span></span>

</dd> <dt>

<span data-ttu-id="ddbdc-111">*dwMaxTessLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ddbdc-111">*dwMaxTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddbdc-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ddbdc-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ddbdc-113">Límite máximo para la teselación adaptable.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-113">Maximum limit for adaptive tessellation.</span></span> <span data-ttu-id="ddbdc-114">Es el número de vértices introducidos entre los vértices existentes.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-114">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="ddbdc-115">Este valor entero puede oscilar entre 1 y 32, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-115">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="ddbdc-116">*dwMinTessLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ddbdc-116">*dwMinTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddbdc-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ddbdc-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ddbdc-118">Límite mínimo para teselación adaptable.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-118">Minimum limit for adaptive tessellation.</span></span> <span data-ttu-id="ddbdc-119">Es el número de vértices introducidos entre los vértices existentes.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-119">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="ddbdc-120">Este valor entero puede oscilar entre 1 y 32, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-120">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="ddbdc-121">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ddbdc-121">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddbdc-122">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ddbdc-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="ddbdc-123">Malla teselada resultante.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-123">Resulting tessellated mesh.</span></span> <span data-ttu-id="ddbdc-124">Vea [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="ddbdc-124">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddbdc-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddbdc-125">Return value</span></span>

<span data-ttu-id="ddbdc-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ddbdc-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ddbdc-127">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ddbdc-128">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ddbdc-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddbdc-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddbdc-129">Remarks</span></span>

<span data-ttu-id="ddbdc-130">Esta función se ejecutará de forma más eficaz si la malla de revisión se ha optimizado mediante [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="ddbdc-130">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddbdc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddbdc-131">Requirements</span></span>



| <span data-ttu-id="ddbdc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddbdc-132">Requirement</span></span> | <span data-ttu-id="ddbdc-133">Value</span><span class="sxs-lookup"><span data-stu-id="ddbdc-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddbdc-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddbdc-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ddbdc-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddbdc-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ddbdc-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ddbdc-136">Library</span></span><br/> | <dl> <span data-ttu-id="ddbdc-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddbdc-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ddbdc-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddbdc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbdc-139">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="ddbdc-139">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 

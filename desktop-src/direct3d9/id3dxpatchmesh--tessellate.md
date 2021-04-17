---
description: Realiza una teselación uniforme basada en el nivel de teselación.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'ID3DXPatchMesh:: dividirlas (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670264"
---
# <a name="id3dxpatchmeshtessellate-method"></a><span data-ttu-id="19759-103">ID3DXPatchMesh:: dividirlas (método)</span><span class="sxs-lookup"><span data-stu-id="19759-103">ID3DXPatchMesh::Tessellate method</span></span>

<span data-ttu-id="19759-104">Realiza una teselación uniforme basada en el nivel de teselación.</span><span class="sxs-lookup"><span data-stu-id="19759-104">Performs uniform tessellation based on the tessellation level.</span></span>

## <a name="syntax"></a><span data-ttu-id="19759-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19759-105">Syntax</span></span>


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="19759-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19759-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19759-107">*fTessLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19759-107">*fTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19759-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19759-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19759-109">Nivel de teselación.</span><span class="sxs-lookup"><span data-stu-id="19759-109">Tessellation level.</span></span> <span data-ttu-id="19759-110">Es el número de vértices introducidos entre los vértices existentes.</span><span class="sxs-lookup"><span data-stu-id="19759-110">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="19759-111">El intervalo de este parámetro Float es 0 < fTessLevel <= 32.</span><span class="sxs-lookup"><span data-stu-id="19759-111">The range of this float parameter is 0 < fTessLevel <= 32.</span></span>

</dd> <dt>

<span data-ttu-id="19759-112">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19759-112">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19759-113">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="19759-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="19759-114">Malla teselada resultante.</span><span class="sxs-lookup"><span data-stu-id="19759-114">Resulting tessellated mesh.</span></span> <span data-ttu-id="19759-115">Vea [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="19759-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19759-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19759-116">Return value</span></span>

<span data-ttu-id="19759-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19759-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19759-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19759-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19759-119">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="19759-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="19759-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19759-120">Remarks</span></span>

<span data-ttu-id="19759-121">Esta función se ejecutará de forma más eficaz si la malla de revisión se ha optimizado mediante [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="19759-121">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19759-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19759-122">Requirements</span></span>



| <span data-ttu-id="19759-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="19759-123">Requirement</span></span> | <span data-ttu-id="19759-124">Value</span><span class="sxs-lookup"><span data-stu-id="19759-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19759-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19759-125">Header</span></span><br/>  | <dl> <span data-ttu-id="19759-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="19759-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="19759-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19759-127">Library</span></span><br/> | <dl> <span data-ttu-id="19759-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19759-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19759-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="19759-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19759-130">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="19759-130">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 

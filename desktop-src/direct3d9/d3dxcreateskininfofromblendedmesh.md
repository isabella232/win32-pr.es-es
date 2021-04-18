---
description: Crea una malla de máscara desde otra malla.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: Función D3DXCreateSkinInfoFromBlendedMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547926"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a><span data-ttu-id="1c7c9-103">D3DXCreateSkinInfoFromBlendedMesh función)</span><span class="sxs-lookup"><span data-stu-id="1c7c9-103">D3DXCreateSkinInfoFromBlendedMesh function</span></span>

<span data-ttu-id="1c7c9-104">Crea una malla de máscara desde otra malla.</span><span class="sxs-lookup"><span data-stu-id="1c7c9-104">Creates a skin mesh from another mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c7c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c7c9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1c7c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c7c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c7c9-107">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c7c9-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7c9-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1c7c9-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="1c7c9-109">Puntero a un objeto [**ID3DXBaseMesh**](id3dxbasemesh.md) , la malla desde la que se va a crear la malla de máscara.</span><span class="sxs-lookup"><span data-stu-id="1c7c9-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) object, the mesh from which to create the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1c7c9-110">*NumBones* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c7c9-110">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7c9-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c7c9-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c7c9-112">La longitud de la matriz asociada a BoneId.</span><span class="sxs-lookup"><span data-stu-id="1c7c9-112">The length of the array attached to the BoneId.</span></span> <span data-ttu-id="1c7c9-113">Vea [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="1c7c9-113">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c7c9-114">*pBoneCombinationTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c7c9-114">*pBoneCombinationTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7c9-115">Tipo: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***</span><span class="sxs-lookup"><span data-stu-id="1c7c9-115">Type: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md)\***</span></span>

<span data-ttu-id="1c7c9-116">Puntero a una matriz de combinaciones de hueso.</span><span class="sxs-lookup"><span data-stu-id="1c7c9-116">Pointer to an array of bone combinations.</span></span> <span data-ttu-id="1c7c9-117">Vea [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="1c7c9-117">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c7c9-118">*ppSkinInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c7c9-118">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7c9-119">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c7c9-119">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="1c7c9-120">Dirección de un puntero a una interfaz [**ID3DXSkinInfo**](id3dxskininfo.md) que representa el objeto de malla de máscara creado.</span><span class="sxs-lookup"><span data-stu-id="1c7c9-120">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c7c9-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c7c9-121">Return value</span></span>

<span data-ttu-id="1c7c9-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c7c9-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c7c9-123">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1c7c9-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1c7c9-124">Si se produce un error en la función, el valor devuelto puede ser el siguiente: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1c7c9-124">If the function fails, the return value can be the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c7c9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c7c9-125">Requirements</span></span>



| <span data-ttu-id="1c7c9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c7c9-126">Requirement</span></span> | <span data-ttu-id="1c7c9-127">Value</span><span class="sxs-lookup"><span data-stu-id="1c7c9-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c7c9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c7c9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1c7c9-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c7c9-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1c7c9-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c7c9-130">Library</span></span><br/> | <dl> <span data-ttu-id="1c7c9-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c7c9-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c7c9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c7c9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c7c9-133">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="1c7c9-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

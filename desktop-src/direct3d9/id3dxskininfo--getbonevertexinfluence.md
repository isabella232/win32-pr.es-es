---
description: Recupera el factor de mezcla y el vértice afectados por una influencia del hueso especificada.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'ID3DXSkinInfo:: GetBoneVertexInfluence (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362414"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a><span data-ttu-id="05c27-103">ID3DXSkinInfo:: GetBoneVertexInfluence (método)</span><span class="sxs-lookup"><span data-stu-id="05c27-103">ID3DXSkinInfo::GetBoneVertexInfluence method</span></span>

<span data-ttu-id="05c27-104">Recupera el factor de mezcla y el vértice afectados por una influencia del hueso especificada.</span><span class="sxs-lookup"><span data-stu-id="05c27-104">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c27-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05c27-105">Syntax</span></span>


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
);
```



## <a name="parameters"></a><span data-ttu-id="05c27-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05c27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05c27-107">*boneNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05c27-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c27-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05c27-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05c27-109">Índice del hueso.</span><span class="sxs-lookup"><span data-stu-id="05c27-109">Index of the bone.</span></span> <span data-ttu-id="05c27-110">Debe estar comprendido entre 0 y el número de huesos.</span><span class="sxs-lookup"><span data-stu-id="05c27-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="05c27-111">*influenceNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05c27-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c27-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05c27-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05c27-113">Índice de la matriz de influencia del hueso especificado.</span><span class="sxs-lookup"><span data-stu-id="05c27-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="05c27-114">*pWeight* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="05c27-114">*pWeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="05c27-115">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="05c27-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="05c27-116">Puntero al factor de combinación influenciado por influenceNum.</span><span class="sxs-lookup"><span data-stu-id="05c27-116">Pointer to the blend factor influenced by influenceNum.</span></span>

</dd> <dt>

<span data-ttu-id="05c27-117">*pVertexNum* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="05c27-117">*pVertexNum* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="05c27-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="05c27-118">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="05c27-119">Puntero al vértice influido por influenceNum.</span><span class="sxs-lookup"><span data-stu-id="05c27-119">Pointer to the vertex influenced by influenceNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05c27-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05c27-120">Return value</span></span>

<span data-ttu-id="05c27-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="05c27-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="05c27-122">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="05c27-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="05c27-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="05c27-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c27-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c27-124">Requirements</span></span>



| <span data-ttu-id="05c27-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c27-125">Requirement</span></span> | <span data-ttu-id="05c27-126">Value</span><span class="sxs-lookup"><span data-stu-id="05c27-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05c27-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05c27-127">Header</span></span><br/>  | <dl> <span data-ttu-id="05c27-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="05c27-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="05c27-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05c27-129">Library</span></span><br/> | <dl> <span data-ttu-id="05c27-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05c27-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05c27-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="05c27-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c27-132">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="05c27-132">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="05c27-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="05c27-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="05c27-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="05c27-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="05c27-135">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="05c27-135">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 

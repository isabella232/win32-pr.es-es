---
description: Recupera el índice de la influencia del hueso que afecta a un solo vértice.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'ID3DXSkinInfo:: FindBoneVertexInfluenceIndex (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717546"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a><span data-ttu-id="392aa-103">ID3DXSkinInfo:: FindBoneVertexInfluenceIndex (método)</span><span class="sxs-lookup"><span data-stu-id="392aa-103">ID3DXSkinInfo::FindBoneVertexInfluenceIndex method</span></span>

<span data-ttu-id="392aa-104">Recupera el índice de la influencia del hueso que afecta a un solo vértice.</span><span class="sxs-lookup"><span data-stu-id="392aa-104">Retrieves the index of the bone influence affecting a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="392aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="392aa-105">Syntax</span></span>


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="392aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="392aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="392aa-107">*boneNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="392aa-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="392aa-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="392aa-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="392aa-109">Índice del hueso.</span><span class="sxs-lookup"><span data-stu-id="392aa-109">Index of the bone.</span></span> <span data-ttu-id="392aa-110">Debe estar comprendido entre 0 y el número de huesos.</span><span class="sxs-lookup"><span data-stu-id="392aa-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="392aa-111">*vertexNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="392aa-111">*vertexNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="392aa-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="392aa-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="392aa-113">Índice del vértice del que se va a buscar la influencia del hueso.</span><span class="sxs-lookup"><span data-stu-id="392aa-113">Index of the vertex for which the bone influence is to be found.</span></span> <span data-ttu-id="392aa-114">Debe estar entre 0 y el número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="392aa-114">Must be between 0 and the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="392aa-115">*pInfluenceIndex* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="392aa-115">*pInfluenceIndex* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="392aa-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="392aa-116">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="392aa-117">Puntero al índice de la influencia del hueso que afecta a vertexNum.</span><span class="sxs-lookup"><span data-stu-id="392aa-117">Pointer to the index of the bone influence that affects vertexNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="392aa-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="392aa-118">Return value</span></span>

<span data-ttu-id="392aa-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="392aa-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="392aa-120">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="392aa-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="392aa-121">Si el hueso especificado no influye en el vértice dado, \_ se devuelve el valor false.</span><span class="sxs-lookup"><span data-stu-id="392aa-121">If the specified bone does not influence the given vertex, S\_FALSE is returned.</span></span> <span data-ttu-id="392aa-122">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="392aa-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="392aa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="392aa-123">Requirements</span></span>



| <span data-ttu-id="392aa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="392aa-124">Requirement</span></span> | <span data-ttu-id="392aa-125">Value</span><span class="sxs-lookup"><span data-stu-id="392aa-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="392aa-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="392aa-126">Header</span></span><br/>  | <dl> <span data-ttu-id="392aa-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="392aa-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="392aa-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="392aa-128">Library</span></span><br/> | <dl> <span data-ttu-id="392aa-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="392aa-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="392aa-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="392aa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="392aa-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="392aa-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="392aa-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="392aa-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="392aa-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="392aa-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="392aa-134">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="392aa-134">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 

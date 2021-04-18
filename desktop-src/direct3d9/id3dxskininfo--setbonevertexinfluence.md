---
description: Establece un valor de influencia de un hueso en un solo vértice.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'ID3DXSkinInfo:: SetBoneVertexInfluence (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707720"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a><span data-ttu-id="ae2fa-103">ID3DXSkinInfo:: SetBoneVertexInfluence (método)</span><span class="sxs-lookup"><span data-stu-id="ae2fa-103">ID3DXSkinInfo::SetBoneVertexInfluence method</span></span>

<span data-ttu-id="ae2fa-104">Establece un valor de influencia de un hueso en un solo vértice.</span><span class="sxs-lookup"><span data-stu-id="ae2fa-104">Sets an influence value of a bone on a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae2fa-105">Syntax</span></span>


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a><span data-ttu-id="ae2fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae2fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae2fa-107">*boneNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae2fa-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2fa-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae2fa-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae2fa-109">Índice del hueso.</span><span class="sxs-lookup"><span data-stu-id="ae2fa-109">Index of the bone.</span></span> <span data-ttu-id="ae2fa-110">Debe estar comprendido entre 0 y el número de huesos.</span><span class="sxs-lookup"><span data-stu-id="ae2fa-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="ae2fa-111">*influenceNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae2fa-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2fa-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae2fa-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae2fa-113">Índice de la matriz de influencia del hueso especificado.</span><span class="sxs-lookup"><span data-stu-id="ae2fa-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="ae2fa-114">*peso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ae2fa-114">*weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2fa-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae2fa-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae2fa-116">Factor de mezcla de la influencia del hueso especificada.</span><span class="sxs-lookup"><span data-stu-id="ae2fa-116">Blend factor of the specified bone influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae2fa-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae2fa-117">Return value</span></span>

<span data-ttu-id="ae2fa-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae2fa-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae2fa-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae2fa-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ae2fa-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ae2fa-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2fa-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae2fa-121">Requirements</span></span>



| <span data-ttu-id="ae2fa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae2fa-122">Requirement</span></span> | <span data-ttu-id="ae2fa-123">Value</span><span class="sxs-lookup"><span data-stu-id="ae2fa-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2fa-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae2fa-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ae2fa-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2fa-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ae2fa-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae2fa-126">Library</span></span><br/> | <dl> <span data-ttu-id="ae2fa-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae2fa-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ae2fa-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae2fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2fa-129">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="ae2fa-129">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="ae2fa-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="ae2fa-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="ae2fa-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="ae2fa-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="ae2fa-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="ae2fa-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 

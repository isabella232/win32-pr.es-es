---
description: Obtiene los vértices y pesos que un hueso influye.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'ID3DXSkinInfo:: GetBoneInfluence (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717545"
---
# <a name="id3dxskininfogetboneinfluence-method"></a><span data-ttu-id="38acd-103">ID3DXSkinInfo:: GetBoneInfluence (método)</span><span class="sxs-lookup"><span data-stu-id="38acd-103">ID3DXSkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="38acd-104">Obtiene los vértices y pesos que un hueso influye.</span><span class="sxs-lookup"><span data-stu-id="38acd-104">Gets the vertices and weights that a bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="38acd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38acd-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="38acd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38acd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38acd-107">*Hueso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="38acd-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38acd-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38acd-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38acd-109">Número del hueso.</span><span class="sxs-lookup"><span data-stu-id="38acd-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="38acd-110">*vértices* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="38acd-110">*vertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38acd-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38acd-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38acd-112">Obtiene la matriz de vértices influida en un hueso.</span><span class="sxs-lookup"><span data-stu-id="38acd-112">Get the array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="38acd-113">*pesos* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="38acd-113">*weights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38acd-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38acd-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38acd-115">Obtiene la matriz de pesos influida por un hueso.</span><span class="sxs-lookup"><span data-stu-id="38acd-115">Get the array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38acd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38acd-116">Return value</span></span>

<span data-ttu-id="38acd-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38acd-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38acd-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38acd-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38acd-119">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="38acd-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="38acd-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38acd-120">Remarks</span></span>

<span data-ttu-id="38acd-121">Use [**ID3DXSkinInfo:: GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) para averiguar el número de vértices que influyen en el hueso.</span><span class="sxs-lookup"><span data-stu-id="38acd-121">Use [**ID3DXSkinInfo::GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="38acd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38acd-122">Requirements</span></span>



| <span data-ttu-id="38acd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="38acd-123">Requirement</span></span> | <span data-ttu-id="38acd-124">Value</span><span class="sxs-lookup"><span data-stu-id="38acd-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38acd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38acd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="38acd-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="38acd-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="38acd-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38acd-127">Library</span></span><br/> | <dl> <span data-ttu-id="38acd-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38acd-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38acd-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="38acd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38acd-130">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="38acd-130">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="38acd-131">**ID3DXSkinInfo::SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="38acd-131">**ID3DXSkinInfo::SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 

---
description: Establece el valor de influencia de un hueso.
ms.assetid: c6dc8a33-8f5c-47d0-8637-a2492b1e3089
title: 'ID3DXSkinInfo:: SetBoneInfluence (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16ed3514c986dee89f964074d18a646bcf3a1249
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717543"
---
# <a name="id3dxskininfosetboneinfluence-method"></a><span data-ttu-id="62a17-103">ID3DXSkinInfo:: SetBoneInfluence (método)</span><span class="sxs-lookup"><span data-stu-id="62a17-103">ID3DXSkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="62a17-104">Establece el valor de influencia de un hueso.</span><span class="sxs-lookup"><span data-stu-id="62a17-104">Sets the influence value for a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a17-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62a17-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in]       DWORD Bone,
  [in]       DWORD numInfluences,
  [in] const DWORD *vertices,
  [in] const FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="62a17-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62a17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a17-107">*Hueso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62a17-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a17-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62a17-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62a17-109">Número del hueso.</span><span class="sxs-lookup"><span data-stu-id="62a17-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="62a17-110">*numInfluences* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62a17-110">*numInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a17-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62a17-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62a17-112">Número de influencias.</span><span class="sxs-lookup"><span data-stu-id="62a17-112">Number of influences.</span></span>

</dd> <dt>

<span data-ttu-id="62a17-113">*vértices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62a17-113">*vertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a17-114">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="62a17-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="62a17-115">Matriz de vértices influida por un hueso.</span><span class="sxs-lookup"><span data-stu-id="62a17-115">The array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="62a17-116">*pesos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62a17-116">*weights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a17-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="62a17-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="62a17-118">Matriz de pesos influida por un hueso.</span><span class="sxs-lookup"><span data-stu-id="62a17-118">The array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a17-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62a17-119">Return value</span></span>

<span data-ttu-id="62a17-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62a17-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62a17-121">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62a17-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="62a17-122">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="62a17-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a17-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62a17-123">Requirements</span></span>



| <span data-ttu-id="62a17-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a17-124">Requirement</span></span> | <span data-ttu-id="62a17-125">Value</span><span class="sxs-lookup"><span data-stu-id="62a17-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62a17-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62a17-126">Header</span></span><br/>  | <dl> <span data-ttu-id="62a17-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="62a17-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="62a17-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62a17-128">Library</span></span><br/> | <dl> <span data-ttu-id="62a17-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62a17-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62a17-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="62a17-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a17-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="62a17-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="62a17-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="62a17-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> <dt>

[<span data-ttu-id="62a17-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="62a17-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)
</dt> </dl>

 

 

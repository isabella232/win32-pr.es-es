---
description: Establece la influencia mínima del hueso. Los valores de influencia más pequeños se omiten.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'ID3DXSkinInfo:: SetMinBoneInfluence (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03e3aeeed31a58231644784ba5070bc9422f7820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717538"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a><span data-ttu-id="aec85-104">ID3DXSkinInfo:: SetMinBoneInfluence (método)</span><span class="sxs-lookup"><span data-stu-id="aec85-104">ID3DXSkinInfo::SetMinBoneInfluence method</span></span>

<span data-ttu-id="aec85-105">Establece la influencia mínima del hueso.</span><span class="sxs-lookup"><span data-stu-id="aec85-105">Sets the minimum bone influence.</span></span> <span data-ttu-id="aec85-106">Los valores de influencia más pequeños se omiten.</span><span class="sxs-lookup"><span data-stu-id="aec85-106">Influence values smaller than this are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec85-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aec85-107">Syntax</span></span>


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a><span data-ttu-id="aec85-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aec85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aec85-109">*MinInfl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aec85-109">*MinInfl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec85-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aec85-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aec85-111">Valor de influencia mínimo.</span><span class="sxs-lookup"><span data-stu-id="aec85-111">Minimum influence value.</span></span> <span data-ttu-id="aec85-112">Los valores de influencia más pequeños se omiten.</span><span class="sxs-lookup"><span data-stu-id="aec85-112">Influence values smaller than this are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aec85-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aec85-113">Return value</span></span>

<span data-ttu-id="aec85-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aec85-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aec85-115">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aec85-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aec85-116">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="aec85-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec85-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aec85-117">Requirements</span></span>



| <span data-ttu-id="aec85-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aec85-118">Requirement</span></span> | <span data-ttu-id="aec85-119">Value</span><span class="sxs-lookup"><span data-stu-id="aec85-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aec85-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aec85-120">Header</span></span><br/>  | <dl> <span data-ttu-id="aec85-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="aec85-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="aec85-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aec85-122">Library</span></span><br/> | <dl> <span data-ttu-id="aec85-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aec85-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aec85-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="aec85-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec85-125">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="aec85-125">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="aec85-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="aec85-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 

---
description: Obtiene la matriz de desplazamiento del hueso.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'ID3DXSkinInfo:: GetBoneOffsetMatrix (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362418"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a><span data-ttu-id="354c2-103">ID3DXSkinInfo:: GetBoneOffsetMatrix (método)</span><span class="sxs-lookup"><span data-stu-id="354c2-103">ID3DXSkinInfo::GetBoneOffsetMatrix method</span></span>

<span data-ttu-id="354c2-104">Obtiene la matriz de desplazamiento del hueso.</span><span class="sxs-lookup"><span data-stu-id="354c2-104">Gets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="354c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="354c2-105">Syntax</span></span>


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="354c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="354c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354c2-107">*Hueso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="354c2-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="354c2-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="354c2-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="354c2-109">Número del hueso.</span><span class="sxs-lookup"><span data-stu-id="354c2-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354c2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="354c2-110">Return value</span></span>

<span data-ttu-id="354c2-111">Tipo: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="354c2-111">Type: **[**LPD3DXMATRIX**](d3dxmatrix.md)**</span></span>

<span data-ttu-id="354c2-112">Devuelve un puntero a la matriz de desplazamiento del hueso.</span><span class="sxs-lookup"><span data-stu-id="354c2-112">Returns a pointer to the bone offset matrix.</span></span> <span data-ttu-id="354c2-113">No libere este puntero.</span><span class="sxs-lookup"><span data-stu-id="354c2-113">Do not free this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="354c2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="354c2-114">Requirements</span></span>



| <span data-ttu-id="354c2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="354c2-115">Requirement</span></span> | <span data-ttu-id="354c2-116">Value</span><span class="sxs-lookup"><span data-stu-id="354c2-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="354c2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="354c2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="354c2-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="354c2-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="354c2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="354c2-119">Library</span></span><br/> | <dl> <span data-ttu-id="354c2-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="354c2-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="354c2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="354c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="354c2-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="354c2-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="354c2-123">**SetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="354c2-123">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[<span data-ttu-id="354c2-124">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="354c2-124">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 

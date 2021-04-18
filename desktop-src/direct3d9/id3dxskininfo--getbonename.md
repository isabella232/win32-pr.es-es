---
description: Obtiene el nombre del hueso, del índice del hueso.
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'ID3DXSkinInfo:: GetBoneName (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0566d423d277dc3f39f36f8c1fda297ec917eb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707723"
---
# <a name="id3dxskininfogetbonename-method"></a><span data-ttu-id="afd52-103">ID3DXSkinInfo:: GetBoneName (método)</span><span class="sxs-lookup"><span data-stu-id="afd52-103">ID3DXSkinInfo::GetBoneName method</span></span>

<span data-ttu-id="afd52-104">Obtiene el nombre del hueso, del índice del hueso.</span><span class="sxs-lookup"><span data-stu-id="afd52-104">Gets the bone name, from the bone index.</span></span>

## <a name="syntax"></a><span data-ttu-id="afd52-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afd52-105">Syntax</span></span>


```C++
LPCSTR GetBoneName(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="afd52-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afd52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd52-107">*Hueso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="afd52-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd52-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="afd52-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="afd52-109">Número del hueso.</span><span class="sxs-lookup"><span data-stu-id="afd52-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afd52-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afd52-110">Return value</span></span>

<span data-ttu-id="afd52-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="afd52-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="afd52-112">Devuelve el nombre del hueso.</span><span class="sxs-lookup"><span data-stu-id="afd52-112">Returns the bone name.</span></span> <span data-ttu-id="afd52-113">No libere esta cadena.</span><span class="sxs-lookup"><span data-stu-id="afd52-113">Do not free this string.</span></span>

## <a name="requirements"></a><span data-ttu-id="afd52-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afd52-114">Requirements</span></span>



| <span data-ttu-id="afd52-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="afd52-115">Requirement</span></span> | <span data-ttu-id="afd52-116">Value</span><span class="sxs-lookup"><span data-stu-id="afd52-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afd52-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afd52-117">Header</span></span><br/>  | <dl> <span data-ttu-id="afd52-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="afd52-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="afd52-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afd52-119">Library</span></span><br/> | <dl> <span data-ttu-id="afd52-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afd52-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="afd52-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="afd52-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd52-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="afd52-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="afd52-123">**ID3DXSkinInfo::SetBoneName**</span><span class="sxs-lookup"><span data-stu-id="afd52-123">**ID3DXSkinInfo::SetBoneName**</span></span>](id3dxskininfo--setbonename.md)
</dt> <dt>

[<span data-ttu-id="afd52-124">**ID3DXSkinInfo::GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="afd52-124">**ID3DXSkinInfo::GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 

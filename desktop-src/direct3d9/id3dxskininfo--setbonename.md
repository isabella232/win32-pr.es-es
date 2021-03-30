---
description: Establece el nombre del hueso.
ms.assetid: 2eecddb8-4efa-41a3-be83-7404047a9857
title: 'ID3DXSkinInfo:: SetBoneName (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c9190c12eac21963d116f60d5a7aa09f97db796
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280233"
---
# <a name="id3dxskininfosetbonename-method"></a><span data-ttu-id="db9ee-103">ID3DXSkinInfo:: SetBoneName (método)</span><span class="sxs-lookup"><span data-stu-id="db9ee-103">ID3DXSkinInfo::SetBoneName method</span></span>

<span data-ttu-id="db9ee-104">Establece el nombre del hueso.</span><span class="sxs-lookup"><span data-stu-id="db9ee-104">Sets the bone name.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9ee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db9ee-105">Syntax</span></span>


```C++
HRESULT SetBoneName(
  [in] DWORD  Bone,
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="db9ee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db9ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9ee-107">*Hueso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db9ee-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9ee-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db9ee-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db9ee-109">Número de hueso</span><span class="sxs-lookup"><span data-stu-id="db9ee-109">Bone number</span></span>

</dd> <dt>

<span data-ttu-id="db9ee-110">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db9ee-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9ee-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db9ee-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db9ee-112">Nombre del hueso</span><span class="sxs-lookup"><span data-stu-id="db9ee-112">Bone name</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9ee-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db9ee-113">Return value</span></span>

<span data-ttu-id="db9ee-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db9ee-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db9ee-115">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db9ee-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db9ee-116">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="db9ee-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9ee-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db9ee-117">Remarks</span></span>

<span data-ttu-id="db9ee-118">[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)devuelve los nombres de los huesos.</span><span class="sxs-lookup"><span data-stu-id="db9ee-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db9ee-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db9ee-119">Requirements</span></span>



| <span data-ttu-id="db9ee-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="db9ee-120">Requirement</span></span> | <span data-ttu-id="db9ee-121">Value</span><span class="sxs-lookup"><span data-stu-id="db9ee-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db9ee-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db9ee-122">Header</span></span><br/>  | <dl> <span data-ttu-id="db9ee-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="db9ee-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="db9ee-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db9ee-124">Library</span></span><br/> | <dl> <span data-ttu-id="db9ee-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db9ee-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db9ee-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="db9ee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9ee-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="db9ee-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="db9ee-128">**ID3DXSkinInfo::GetBoneName**</span><span class="sxs-lookup"><span data-stu-id="db9ee-128">**ID3DXSkinInfo::GetBoneName**</span></span>](id3dxskininfo--getbonename.md)
</dt> </dl>

 

 

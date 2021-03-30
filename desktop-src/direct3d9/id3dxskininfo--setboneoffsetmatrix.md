---
description: Establece la matriz de desplazamiento del hueso.
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'ID3DXSkinInfo:: SetBoneOffsetMatrix (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 283d36bb68e33cfa0e2349bab304b0cdde7ef77e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820914"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a><span data-ttu-id="d3b06-103">ID3DXSkinInfo:: SetBoneOffsetMatrix (método)</span><span class="sxs-lookup"><span data-stu-id="d3b06-103">ID3DXSkinInfo::SetBoneOffsetMatrix method</span></span>

<span data-ttu-id="d3b06-104">Establece la matriz de desplazamiento del hueso.</span><span class="sxs-lookup"><span data-stu-id="d3b06-104">Sets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b06-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3b06-105">Syntax</span></span>


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a><span data-ttu-id="d3b06-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3b06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b06-107">*Hueso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3b06-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b06-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3b06-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3b06-109">Número del hueso.</span><span class="sxs-lookup"><span data-stu-id="d3b06-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="d3b06-110">*pBoneTransform* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3b06-110">*pBoneTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b06-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3b06-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d3b06-112">Puntero a la matriz de desplazamiento del hueso.</span><span class="sxs-lookup"><span data-stu-id="d3b06-112">Pointer to the bone offset matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b06-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3b06-113">Return value</span></span>

<span data-ttu-id="d3b06-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3b06-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3b06-115">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d3b06-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d3b06-116">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d3b06-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3b06-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3b06-117">Remarks</span></span>

<span data-ttu-id="d3b06-118">[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)devuelve los nombres de los huesos.</span><span class="sxs-lookup"><span data-stu-id="d3b06-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b06-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3b06-119">Requirements</span></span>



| <span data-ttu-id="d3b06-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3b06-120">Requirement</span></span> | <span data-ttu-id="d3b06-121">Value</span><span class="sxs-lookup"><span data-stu-id="d3b06-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b06-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3b06-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d3b06-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3b06-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d3b06-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3b06-124">Library</span></span><br/> | <dl> <span data-ttu-id="d3b06-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3b06-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3b06-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3b06-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b06-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="d3b06-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="d3b06-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="d3b06-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 

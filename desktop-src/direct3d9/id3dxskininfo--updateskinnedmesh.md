---
description: Aplica los aspectos de software a los vértices de destino en función de las matrices actuales.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'ID3DXSkinInfo:: UpdateSkinnedMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717539"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a><span data-ttu-id="fdde0-103">ID3DXSkinInfo:: UpdateSkinnedMesh (método)</span><span class="sxs-lookup"><span data-stu-id="fdde0-103">ID3DXSkinInfo::UpdateSkinnedMesh method</span></span>

<span data-ttu-id="fdde0-104">Aplica los aspectos de software a los vértices de destino en función de las matrices actuales.</span><span class="sxs-lookup"><span data-stu-id="fdde0-104">Applies software skinning to the target vertices based on the current matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdde0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdde0-105">Syntax</span></span>


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a><span data-ttu-id="fdde0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdde0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdde0-107">*pBoneTransforms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdde0-107">*pBoneTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdde0-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fdde0-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fdde0-109">Matriz de transformación del hueso.</span><span class="sxs-lookup"><span data-stu-id="fdde0-109">Bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fdde0-110">*pBoneInvTransposeTransforms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdde0-110">*pBoneInvTransposeTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdde0-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fdde0-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fdde0-112">Transposición inversa de la matriz de transformación del hueso.</span><span class="sxs-lookup"><span data-stu-id="fdde0-112">Inverse transpose of the bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fdde0-113">*pVerticesSrc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdde0-113">*pVerticesSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdde0-114">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdde0-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdde0-115">Puntero al búfer que contiene los vértices de origen.</span><span class="sxs-lookup"><span data-stu-id="fdde0-115">Pointer to the buffer containing the source vertices.</span></span>

</dd> <dt>

<span data-ttu-id="fdde0-116">*pVerticesDst* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdde0-116">*pVerticesDst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdde0-117">Tipo: **[ **PVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdde0-117">Type: **[**PVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdde0-118">Puntero al búfer que contiene los vértices de destino.</span><span class="sxs-lookup"><span data-stu-id="fdde0-118">Pointer to the buffer containing the destination vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdde0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdde0-119">Return value</span></span>

<span data-ttu-id="fdde0-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fdde0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fdde0-121">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fdde0-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fdde0-122">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fdde0-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdde0-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fdde0-123">Remarks</span></span>

<span data-ttu-id="fdde0-124">Cuando se usa para enmascarar vértices con dos elementos de posición, este método enmascara el elemento de segunda posición con el inverso del hueso en lugar del propio hueso.</span><span class="sxs-lookup"><span data-stu-id="fdde0-124">When used to skin vertices with two position elements, this method skins the second position element with the inverse of the bone instead of the bone itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdde0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdde0-125">Requirements</span></span>



| <span data-ttu-id="fdde0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdde0-126">Requirement</span></span> | <span data-ttu-id="fdde0-127">Value</span><span class="sxs-lookup"><span data-stu-id="fdde0-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdde0-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdde0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fdde0-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdde0-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fdde0-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fdde0-130">Library</span></span><br/> | <dl> <span data-ttu-id="fdde0-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdde0-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fdde0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdde0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdde0-133">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="fdde0-133">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 

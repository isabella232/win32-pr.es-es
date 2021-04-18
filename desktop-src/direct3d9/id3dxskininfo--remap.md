---
description: Actualiza la información de influencia del hueso para que coincida con los vértices después de reordenar. Se debe llamar a este método si el búfer de vértices de destino se ha reordenado externamente.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'ID3DXSkinInfo:: reasignar (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698174"
---
# <a name="id3dxskininforemap-method"></a><span data-ttu-id="866bd-104">ID3DXSkinInfo:: reasignar (método)</span><span class="sxs-lookup"><span data-stu-id="866bd-104">ID3DXSkinInfo::Remap method</span></span>

<span data-ttu-id="866bd-105">Actualiza la información de influencia del hueso para que coincida con los vértices después de reordenar.</span><span class="sxs-lookup"><span data-stu-id="866bd-105">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="866bd-106">Se debe llamar a este método si el búfer de vértices de destino se ha reordenado externamente.</span><span class="sxs-lookup"><span data-stu-id="866bd-106">This method should be called if the target vertex buffer has been reordered externally.</span></span>

## <a name="syntax"></a><span data-ttu-id="866bd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="866bd-107">Syntax</span></span>


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="866bd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="866bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="866bd-109">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="866bd-109">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866bd-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="866bd-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="866bd-111">Número de vértices que se van a reasignar.</span><span class="sxs-lookup"><span data-stu-id="866bd-111">Number of vertices to remap.</span></span>

</dd> <dt>

<span data-ttu-id="866bd-112">*pVertexRemap* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="866bd-112">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866bd-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="866bd-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="866bd-114">Matriz de DWORD cuya longitud se especifica mediante NumVertices.</span><span class="sxs-lookup"><span data-stu-id="866bd-114">Array of DWORDS whose length is specified by NumVertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="866bd-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="866bd-115">Return value</span></span>

<span data-ttu-id="866bd-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="866bd-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="866bd-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="866bd-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="866bd-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="866bd-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="866bd-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="866bd-119">Remarks</span></span>

<span data-ttu-id="866bd-120">Cada elemento de pVertexRemap especifica el índice de vértice anterior para esa posición.</span><span class="sxs-lookup"><span data-stu-id="866bd-120">Each element in pVertexRemap specifies the previous vertex index for that position.</span></span> <span data-ttu-id="866bd-121">Por ejemplo, si un vértice estaba en la posición 3 pero se ha reasignado a la posición 5, el quinto elemento de pVertexRemap debe contener 3.</span><span class="sxs-lookup"><span data-stu-id="866bd-121">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap should contain 3.</span></span> <span data-ttu-id="866bd-122">Se puede usar la matriz de reasignación de vértices devuelta por [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) .</span><span class="sxs-lookup"><span data-stu-id="866bd-122">The vertex remap array returned by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) can be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="866bd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="866bd-123">Requirements</span></span>



| <span data-ttu-id="866bd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="866bd-124">Requirement</span></span> | <span data-ttu-id="866bd-125">Value</span><span class="sxs-lookup"><span data-stu-id="866bd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="866bd-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="866bd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="866bd-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="866bd-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="866bd-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="866bd-128">Library</span></span><br/> | <dl> <span data-ttu-id="866bd-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="866bd-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="866bd-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="866bd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866bd-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="866bd-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 

---
description: Cambiar los vértices afectados por los huesos.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'ID3DX10SkinInfo:: RemapVertices (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718225"
---
# <a name="id3dx10skininforemapvertices-method"></a><span data-ttu-id="c5e5b-103">ID3DX10SkinInfo:: RemapVertices (método)</span><span class="sxs-lookup"><span data-stu-id="c5e5b-103">ID3DX10SkinInfo::RemapVertices method</span></span>

<span data-ttu-id="c5e5b-104">Cambiar los vértices afectados por los huesos.</span><span class="sxs-lookup"><span data-stu-id="c5e5b-104">Change which vertices are influenced by which bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e5b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5e5b-105">Syntax</span></span>


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="c5e5b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5e5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e5b-107">*NewVertexCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5e5b-107">*NewVertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e5b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5e5b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5e5b-109">Nuevo número de vértices.</span><span class="sxs-lookup"><span data-stu-id="c5e5b-109">The new number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="c5e5b-110">*pVertexRemap* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5e5b-110">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e5b-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5e5b-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c5e5b-112">Puntero a una matriz de índices de vértices, que describen la reasignación.</span><span class="sxs-lookup"><span data-stu-id="c5e5b-112">A pointer to an array of vertex indices, which describe the remapping.</span></span> <span data-ttu-id="c5e5b-113">Por ejemplo, suponga que SkinInfo contiene algunos vértices, de modo que bone0 se asigna a V0, bone1 a V1 y bone2 a V2, y se especifica array con 2, 1, 0 para pBoneRemap.</span><span class="sxs-lookup"><span data-stu-id="c5e5b-113">For example, say SkinInfo contains some vertices such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="c5e5b-114">Esto hará que bone0 se asigne a V2, bone1 a V1 y bone2 a v0.</span><span class="sxs-lookup"><span data-stu-id="c5e5b-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e5b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5e5b-115">Return value</span></span>

<span data-ttu-id="c5e5b-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5e5b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5e5b-117">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5e5b-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c5e5b-118">Si se produce un error en el método, el valor devuelto puede ser: E \_ OUTOFMEMORY o e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="c5e5b-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e5b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5e5b-119">Requirements</span></span>



| <span data-ttu-id="c5e5b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e5b-120">Requirement</span></span> | <span data-ttu-id="c5e5b-121">Value</span><span class="sxs-lookup"><span data-stu-id="c5e5b-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e5b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5e5b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c5e5b-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5e5b-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5e5b-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5e5b-124">Library</span></span><br/> | <dl> <span data-ttu-id="c5e5b-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5e5b-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5e5b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5e5b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e5b-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="c5e5b-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="c5e5b-128">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="c5e5b-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

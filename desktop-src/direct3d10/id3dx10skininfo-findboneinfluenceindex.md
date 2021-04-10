---
description: Busque el índice que indica dónde se encuentra un vértice determinado en la lista de vértices influida de un hueso determinado.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: 'ID3DX10SkinInfo:: FindBoneInfluenceIndex (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280413"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a><span data-ttu-id="a824e-103">ID3DX10SkinInfo:: FindBoneInfluenceIndex (método)</span><span class="sxs-lookup"><span data-stu-id="a824e-103">ID3DX10SkinInfo::FindBoneInfluenceIndex method</span></span>

<span data-ttu-id="a824e-104">Busque el índice que indica dónde se encuentra un vértice determinado en la lista de vértices influida de un hueso determinado.</span><span class="sxs-lookup"><span data-stu-id="a824e-104">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a824e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a824e-105">Syntax</span></span>


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="a824e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a824e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a824e-107">*BoneIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a824e-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a824e-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a824e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a824e-109">Índice que especifica un hueso existente.</span><span class="sxs-lookup"><span data-stu-id="a824e-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="a824e-110">Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="a824e-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="a824e-111">*VertexIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a824e-111">*VertexIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a824e-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a824e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a824e-113">Índice del vértice en el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="a824e-113">The index of the vertex in the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a824e-114">*pInfluenceIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a824e-114">*pInfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a824e-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a824e-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a824e-116">Índice del vértice en la lista de vértices influidos del hueso.</span><span class="sxs-lookup"><span data-stu-id="a824e-116">The index of the vertex in the bone's list of influenced vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a824e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a824e-117">Return value</span></span>

<span data-ttu-id="a824e-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a824e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a824e-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a824e-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a824e-120">Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="a824e-120">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="a824e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a824e-121">Requirements</span></span>



| <span data-ttu-id="a824e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a824e-122">Requirement</span></span> | <span data-ttu-id="a824e-123">Value</span><span class="sxs-lookup"><span data-stu-id="a824e-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a824e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a824e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a824e-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a824e-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a824e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a824e-126">Library</span></span><br/> | <dl> <span data-ttu-id="a824e-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a824e-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a824e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a824e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a824e-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="a824e-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="a824e-130">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="a824e-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

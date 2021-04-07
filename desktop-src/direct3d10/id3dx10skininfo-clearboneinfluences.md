---
description: Borre la lista de vértices de un hueso a los que influye.
ms.assetid: 1ba6f43a-1f85-4057-b0ed-247cc38d4932
title: 'ID3DX10SkinInfo:: ClearBoneInfluences (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.ClearBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6f161ba400b684b12d6b0a091abb1fa452d476b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003826"
---
# <a name="id3dx10skininfoclearboneinfluences-method"></a><span data-ttu-id="d166c-103">ID3DX10SkinInfo:: ClearBoneInfluences (método)</span><span class="sxs-lookup"><span data-stu-id="d166c-103">ID3DX10SkinInfo::ClearBoneInfluences method</span></span>

<span data-ttu-id="d166c-104">Borre la lista de vértices de un hueso a los que influye.</span><span class="sxs-lookup"><span data-stu-id="d166c-104">Clear a bone's list of vertices that it influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="d166c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d166c-105">Syntax</span></span>


```C++
HRESULT ClearBoneInfluences(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a><span data-ttu-id="d166c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d166c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d166c-107">*BoneIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d166c-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d166c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d166c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d166c-109">Índice que especifica un hueso existente.</span><span class="sxs-lookup"><span data-stu-id="d166c-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="d166c-110">Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="d166c-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d166c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d166c-111">Return value</span></span>

<span data-ttu-id="d166c-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d166c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d166c-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d166c-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d166c-114">Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d166c-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="d166c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d166c-115">Requirements</span></span>



| <span data-ttu-id="d166c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d166c-116">Requirement</span></span> | <span data-ttu-id="d166c-117">Value</span><span class="sxs-lookup"><span data-stu-id="d166c-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d166c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d166c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d166c-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d166c-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d166c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d166c-120">Library</span></span><br/> | <dl> <span data-ttu-id="d166c-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d166c-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d166c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d166c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d166c-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="d166c-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="d166c-124">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="d166c-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

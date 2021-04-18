---
description: Obtiene el número de vértices a los que afecta un hueso determinado.
ms.assetid: e92361ea-4269-4d63-a8d1-560a486b6563
title: 'ID3DX10SkinInfo:: GetBoneInfluenceCount (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluenceCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ad6ddc6ebc80c51e07b7ff0c887371fd45fd42b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718231"
---
# <a name="id3dx10skininfogetboneinfluencecount-method"></a><span data-ttu-id="88459-103">ID3DX10SkinInfo:: GetBoneInfluenceCount (método)</span><span class="sxs-lookup"><span data-stu-id="88459-103">ID3DX10SkinInfo::GetBoneInfluenceCount method</span></span>

<span data-ttu-id="88459-104">Obtiene el número de vértices a los que afecta un hueso determinado.</span><span class="sxs-lookup"><span data-stu-id="88459-104">Get the number of vertices that a given bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="88459-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88459-105">Syntax</span></span>


```C++
UINT GetBoneInfluenceCount(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a><span data-ttu-id="88459-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88459-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88459-107">*BoneIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88459-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88459-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88459-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="88459-109">Índice que especifica un hueso existente.</span><span class="sxs-lookup"><span data-stu-id="88459-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="88459-110">Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="88459-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88459-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88459-111">Return value</span></span>

<span data-ttu-id="88459-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88459-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="88459-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="88459-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="88459-114">Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="88459-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="88459-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88459-115">Requirements</span></span>



| <span data-ttu-id="88459-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="88459-116">Requirement</span></span> | <span data-ttu-id="88459-117">Value</span><span class="sxs-lookup"><span data-stu-id="88459-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88459-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88459-118">Header</span></span><br/>  | <dl> <span data-ttu-id="88459-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="88459-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="88459-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88459-120">Library</span></span><br/> | <dl> <span data-ttu-id="88459-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88459-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88459-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="88459-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88459-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="88459-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="88459-124">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="88459-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

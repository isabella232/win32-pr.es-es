---
description: Establece la cantidad de influencia que un hueso determinado tiene sobre un vértice determinado.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'ID3DX10SkinInfo:: SetBoneInfluence (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d136ddf4491a2a00c029422512c671a5439ba47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718359"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a><span data-ttu-id="3aa54-103">ID3DX10SkinInfo:: SetBoneInfluence (método)</span><span class="sxs-lookup"><span data-stu-id="3aa54-103">ID3DX10SkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="3aa54-104">Establece la cantidad de influencia que un hueso determinado tiene sobre un vértice determinado.</span><span class="sxs-lookup"><span data-stu-id="3aa54-104">Set the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa54-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3aa54-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a><span data-ttu-id="3aa54-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3aa54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa54-107">*BoneIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3aa54-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa54-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3aa54-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3aa54-109">Índice que especifica un hueso existente.</span><span class="sxs-lookup"><span data-stu-id="3aa54-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="3aa54-110">Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="3aa54-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="3aa54-111">*InfluenceIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3aa54-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa54-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3aa54-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3aa54-113">Índice de la lista de vértices del hueso a la que influye.</span><span class="sxs-lookup"><span data-stu-id="3aa54-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="3aa54-114">*Peso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3aa54-114">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa54-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3aa54-115">Type: **float**</span></span>

<span data-ttu-id="3aa54-116">La cantidad de influencia, entre 0 y 1, que tiene el hueso en el vértice.</span><span class="sxs-lookup"><span data-stu-id="3aa54-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa54-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3aa54-117">Return value</span></span>

<span data-ttu-id="3aa54-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3aa54-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3aa54-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3aa54-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3aa54-120">Si se produce un error en el método, el valor devuelto puede ser E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="3aa54-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa54-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa54-121">Requirements</span></span>



| <span data-ttu-id="3aa54-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa54-122">Requirement</span></span> | <span data-ttu-id="3aa54-123">Value</span><span class="sxs-lookup"><span data-stu-id="3aa54-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa54-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3aa54-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3aa54-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aa54-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3aa54-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3aa54-126">Library</span></span><br/> | <dl> <span data-ttu-id="3aa54-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3aa54-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa54-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3aa54-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa54-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="3aa54-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="3aa54-130">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="3aa54-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

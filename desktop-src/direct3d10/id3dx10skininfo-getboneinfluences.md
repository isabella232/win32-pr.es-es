---
description: Obtiene una lista de vértices a los que afecta un hueso determinado y una lista de la cantidad de influencia que tiene el hueso en cada vértice.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'ID3DX10SkinInfo:: GetBoneInfluences (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280514"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a><span data-ttu-id="066ba-103">ID3DX10SkinInfo:: GetBoneInfluences (método)</span><span class="sxs-lookup"><span data-stu-id="066ba-103">ID3DX10SkinInfo::GetBoneInfluences method</span></span>

<span data-ttu-id="066ba-104">Obtiene una lista de vértices a los que afecta un hueso determinado y una lista de la cantidad de influencia que tiene el hueso en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="066ba-104">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="066ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="066ba-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a><span data-ttu-id="066ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="066ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="066ba-107">*BoneIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="066ba-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066ba-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="066ba-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="066ba-109">Índice que especifica un hueso existente.</span><span class="sxs-lookup"><span data-stu-id="066ba-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="066ba-110">Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="066ba-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="066ba-111">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="066ba-111">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066ba-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="066ba-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="066ba-113">Desplazamiento desde la parte superior de la lista de vértices influidos por el hueso.</span><span class="sxs-lookup"><span data-stu-id="066ba-113">An offset from the top of the bone's list of influenced vertices.</span></span> <span data-ttu-id="066ba-114">Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span><span class="sxs-lookup"><span data-stu-id="066ba-114">This must be between 0 and the value returned by [**ID3DX10SkinInfo::GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span></span>

</dd> <dt>

<span data-ttu-id="066ba-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="066ba-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066ba-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="066ba-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="066ba-117">El número de índices y pesos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="066ba-117">The number of indices and weights to retrieve.</span></span> <span data-ttu-id="066ba-118">Debe estar comprendido entre 0 y el valor devuelto por ID3DX10SkinInfo:: GetBoneInfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="066ba-118">Must be between 0 and the value returned by ID3DX10SkinInfo::GetBoneInfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="066ba-119">*pDestIndices* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="066ba-119">*pDestIndices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="066ba-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="066ba-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="066ba-121">Una lista de índices en el búfer de vértices, cada uno de los cuales representa un vértice influido por el hueso.</span><span class="sxs-lookup"><span data-stu-id="066ba-121">A list of indices into the vertex buffer, each one representing a vertex influenced by the bone.</span></span> <span data-ttu-id="066ba-122">Estos valores corresponden a los valores de pDestWeights, de modo que pDestIndices \[ i se \] corresponda con pDestWeights \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="066ba-122">These values correspond to the values in pDestWeights, such that pDestIndices\[i\] corresponds to pDestWeights\[i\].</span></span>

</dd> <dt>

<span data-ttu-id="066ba-123">*pDestWeights* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="066ba-123">*pDestWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="066ba-124">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="066ba-124">Type: **float\***</span></span>

<span data-ttu-id="066ba-125">Una lista de la cantidad de influencia que tiene el hueso en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="066ba-125">A list of the amount of influence the bone has on each vertex.</span></span> <span data-ttu-id="066ba-126">Estos valores corresponden a los valores de pDestIndices, de modo que pDestWeights \[ i se \] corresponda con pDestIndices \[ i \] . f</span><span class="sxs-lookup"><span data-stu-id="066ba-126">These values correspond to the values in pDestIndices, such that pDestWeights\[i\] corresponds to pDestIndices\[i\].f</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="066ba-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="066ba-127">Return value</span></span>

<span data-ttu-id="066ba-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="066ba-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="066ba-129">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="066ba-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="066ba-130">Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG o e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="066ba-130">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="066ba-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="066ba-131">Requirements</span></span>



| <span data-ttu-id="066ba-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="066ba-132">Requirement</span></span> | <span data-ttu-id="066ba-133">Value</span><span class="sxs-lookup"><span data-stu-id="066ba-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="066ba-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="066ba-134">Header</span></span><br/>  | <dl> <span data-ttu-id="066ba-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="066ba-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="066ba-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="066ba-136">Library</span></span><br/> | <dl> <span data-ttu-id="066ba-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="066ba-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="066ba-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="066ba-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="066ba-139">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="066ba-139">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="066ba-140">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="066ba-140">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

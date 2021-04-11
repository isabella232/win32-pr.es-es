---
description: Permite que un hueso existente afecte a un grupo de vértices y defina la influencia que tenga el hueso en cada vértice.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'ID3DX10SkinInfo:: AddBoneInfluences (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280336"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a><span data-ttu-id="2fc1c-103">ID3DX10SkinInfo:: AddBoneInfluences (método)</span><span class="sxs-lookup"><span data-stu-id="2fc1c-103">ID3DX10SkinInfo::AddBoneInfluences method</span></span>

<span data-ttu-id="2fc1c-104">Permite que un hueso existente afecte a un grupo de vértices y defina la influencia que tenga el hueso en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-104">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc1c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fc1c-105">Syntax</span></span>


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="2fc1c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fc1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc1c-107">*BoneIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fc1c-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc1c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fc1c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fc1c-109">Índice que especifica un hueso existente.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="2fc1c-110">Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="2fc1c-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fc1c-111">*InfluenceCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fc1c-111">*InfluenceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc1c-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fc1c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fc1c-113">Número de vértices que se van a agregar a la influencia del hueso.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-113">Number of vertices to add to the bone's influence.</span></span>

</dd> <dt>

<span data-ttu-id="2fc1c-114">*pIndices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fc1c-114">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc1c-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2fc1c-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2fc1c-116">Puntero a una matriz de índices de vértice.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-116">Pointer to an array of vertex indices.</span></span> <span data-ttu-id="2fc1c-117">Cada miembro de esta matriz tiene un miembro correspondiente en pWeights, de modo que pIndices \[ i se \] corresponde con pWeights \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="2fc1c-117">Each member of this array has a corresponding member in pWeights, such that pIndices\[i\] corresponds to pWeights\[i\].</span></span> <span data-ttu-id="2fc1c-118">El valor correspondiente en pWeights \[ \] determinará la cantidad de influencia que BoneIndex tendrá en el vértice indexado por pIndices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="2fc1c-118">The corresponding value in pWeights\[i\] determines how much influence BoneIndex will have on the vertex indexed by pIndices\[i\].</span></span> <span data-ttu-id="2fc1c-119">El tamaño de la matriz pIndices debe ser igual o mayor que InfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-119">The size of the pIndices array must be equal to or greater than InfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="2fc1c-120">*pWeights* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fc1c-120">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc1c-121">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="2fc1c-121">Type: **float\***</span></span>

<span data-ttu-id="2fc1c-122">Puntero a una matriz de pesos del hueso.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-122">Pointer to an array of bone weights.</span></span> <span data-ttu-id="2fc1c-123">Cada miembro de esta matriz tiene un miembro correspondiente en pIndices, de modo que pWeights \[ i se \] corresponde con pIndices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="2fc1c-123">Each member of this array has a corresponding member in pIndices, such that pWeights\[i\] corresponds to pIndices\[i\].</span></span> <span data-ttu-id="2fc1c-124">Cada valor de pWeights se encuentra entre 0 y 1, y define la cantidad de influencia que tiene el hueso en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-124">Each value in pWeights is between 0 and 1 and defines the amount of influence the bone has over each vertex.</span></span> <span data-ttu-id="2fc1c-125">El tamaño de pWeights debe ser igual o mayor que InfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-125">The size of pWeights must be equal to or greater than InfluenceCount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc1c-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fc1c-126">Return value</span></span>

<span data-ttu-id="2fc1c-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2fc1c-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2fc1c-128">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2fc1c-129">Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG o e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2fc1c-129">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fc1c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fc1c-130">Requirements</span></span>



| <span data-ttu-id="2fc1c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fc1c-131">Requirement</span></span> | <span data-ttu-id="2fc1c-132">Value</span><span class="sxs-lookup"><span data-stu-id="2fc1c-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc1c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fc1c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="2fc1c-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fc1c-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fc1c-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fc1c-135">Library</span></span><br/> | <dl> <span data-ttu-id="2fc1c-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fc1c-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fc1c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fc1c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc1c-138">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="2fc1c-138">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="2fc1c-139">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="2fc1c-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

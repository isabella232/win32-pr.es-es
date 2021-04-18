---
description: Cambiar los huesos influyen en los vértices.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'ID3DX10SkinInfo:: RemapBones (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718226"
---
# <a name="id3dx10skininforemapbones-method"></a><span data-ttu-id="d4b04-103">ID3DX10SkinInfo:: RemapBones (método)</span><span class="sxs-lookup"><span data-stu-id="d4b04-103">ID3DX10SkinInfo::RemapBones method</span></span>

<span data-ttu-id="d4b04-104">Cambiar los huesos influyen en los vértices.</span><span class="sxs-lookup"><span data-stu-id="d4b04-104">Change which bones influence which vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b04-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4b04-105">Syntax</span></span>


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a><span data-ttu-id="d4b04-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4b04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b04-107">*NewBoneCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4b04-107">*NewBoneCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4b04-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4b04-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4b04-109">Nuevo número de huesos.</span><span class="sxs-lookup"><span data-stu-id="d4b04-109">The new number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="d4b04-110">*pBoneRemap* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4b04-110">*pBoneRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4b04-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4b04-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d4b04-112">Puntero a una matriz de índices de hueso, que describen la reasignación.</span><span class="sxs-lookup"><span data-stu-id="d4b04-112">A pointer to an array of bone indices, which describe the remapping.</span></span> <span data-ttu-id="d4b04-113">Por ejemplo, suponga que SkinInfo contiene algunos huesos, de modo que bone0 se asigna a V0, bone1 a V1 y bone2 a V2, y se especifica array con 2, 1, 0 para pBoneRemap.</span><span class="sxs-lookup"><span data-stu-id="d4b04-113">For example, say SkinInfo contains some bones such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="d4b04-114">Esto hará que bone0 se asigne a V2, bone1 a V1 y bone2 a v0.</span><span class="sxs-lookup"><span data-stu-id="d4b04-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4b04-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4b04-115">Return value</span></span>

<span data-ttu-id="d4b04-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4b04-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4b04-117">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4b04-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d4b04-118">Si se produce un error en el método, el valor devuelto puede ser: E \_ OUTOFMEMORY o e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d4b04-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b04-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4b04-119">Requirements</span></span>



| <span data-ttu-id="d4b04-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4b04-120">Requirement</span></span> | <span data-ttu-id="d4b04-121">Value</span><span class="sxs-lookup"><span data-stu-id="d4b04-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b04-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4b04-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d4b04-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4b04-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4b04-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4b04-124">Library</span></span><br/> | <dl> <span data-ttu-id="d4b04-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4b04-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b04-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4b04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b04-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="d4b04-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="d4b04-128">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="d4b04-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

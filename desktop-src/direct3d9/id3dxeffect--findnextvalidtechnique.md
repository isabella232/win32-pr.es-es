---
description: Busca la siguiente técnica válida, empezando por la técnica después de la técnica especificada.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'ID3DXEffect:: FindNextValidTechnique (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424412"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a><span data-ttu-id="8adc8-103">ID3DXEffect:: FindNextValidTechnique (método)</span><span class="sxs-lookup"><span data-stu-id="8adc8-103">ID3DXEffect::FindNextValidTechnique method</span></span>

<span data-ttu-id="8adc8-104">Busca la siguiente técnica válida, empezando por la técnica después de la técnica especificada.</span><span class="sxs-lookup"><span data-stu-id="8adc8-104">Searches for the next valid technique, starting at the technique after the specified technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="8adc8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8adc8-105">Syntax</span></span>


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="8adc8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8adc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8adc8-107">*hTechnique* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8adc8-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8adc8-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8adc8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8adc8-109">Identificador único de una técnica.</span><span class="sxs-lookup"><span data-stu-id="8adc8-109">Unique identifier to a technique.</span></span> <span data-ttu-id="8adc8-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8adc8-110">See [Handles (Direct3D 9)](handles.md).</span></span> <span data-ttu-id="8adc8-111">Especifique **null** para este parámetro para buscar la primera técnica válida.</span><span class="sxs-lookup"><span data-stu-id="8adc8-111">Specify **NULL** for this parameter to find the first valid technique.</span></span>

</dd> <dt>

<span data-ttu-id="8adc8-112">*pTechnique* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8adc8-112">*pTechnique* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8adc8-113">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span><span class="sxs-lookup"><span data-stu-id="8adc8-113">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span></span>

<span data-ttu-id="8adc8-114">Puntero a un identificador de la técnica siguiente.</span><span class="sxs-lookup"><span data-stu-id="8adc8-114">Pointer to an identifier for the next technique.</span></span> <span data-ttu-id="8adc8-115">Se devuelve **null** si se trata de la última técnica.</span><span class="sxs-lookup"><span data-stu-id="8adc8-115">**NULL** is returned if this is the last technique.</span></span> <span data-ttu-id="8adc8-116">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8adc8-116">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8adc8-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8adc8-117">Return value</span></span>

<span data-ttu-id="8adc8-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8adc8-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8adc8-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8adc8-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8adc8-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8adc8-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8adc8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8adc8-121">Requirements</span></span>



| <span data-ttu-id="8adc8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8adc8-122">Requirement</span></span> | <span data-ttu-id="8adc8-123">Value</span><span class="sxs-lookup"><span data-stu-id="8adc8-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8adc8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8adc8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8adc8-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8adc8-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8adc8-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8adc8-126">Library</span></span><br/> | <dl> <span data-ttu-id="8adc8-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8adc8-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8adc8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8adc8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8adc8-129">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="8adc8-129">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="8adc8-130">**D3DXTECHNIQUE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8adc8-130">**D3DXTECHNIQUE\_DESC**</span></span>](d3dxtechnique-desc.md)
</dt> <dt>

[<span data-ttu-id="8adc8-131">**ID3DXEffect::ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="8adc8-131">**ID3DXEffect::ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 





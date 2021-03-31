---
description: Determina si la técnica utiliza un parámetro.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'ID3DXEffect:: IsParameterUsed (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6cbe4783a9ad5b618f05941eae08af4c15be0512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157148"
---
# <a name="id3dxeffectisparameterused-method"></a><span data-ttu-id="5051d-103">ID3DXEffect:: IsParameterUsed (método)</span><span class="sxs-lookup"><span data-stu-id="5051d-103">ID3DXEffect::IsParameterUsed method</span></span>

<span data-ttu-id="5051d-104">Determina si la técnica utiliza un parámetro.</span><span class="sxs-lookup"><span data-stu-id="5051d-104">Determines if a parameter is used by the technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="5051d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5051d-105">Syntax</span></span>


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="5051d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5051d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5051d-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5051d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5051d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5051d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5051d-109">Identificador único del parámetro.</span><span class="sxs-lookup"><span data-stu-id="5051d-109">Unique identifier for the parameter.</span></span> <span data-ttu-id="5051d-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5051d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5051d-111">*hTechnique* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5051d-111">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5051d-112">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5051d-112">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5051d-113">Identificador único de la técnica.</span><span class="sxs-lookup"><span data-stu-id="5051d-113">Unique identifier for the technique.</span></span> <span data-ttu-id="5051d-114">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5051d-114">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5051d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5051d-115">Return value</span></span>

<span data-ttu-id="5051d-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5051d-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5051d-117">Devuelve **true** si se utiliza el parámetro y devuelve **false** si no se utiliza el parámetro.</span><span class="sxs-lookup"><span data-stu-id="5051d-117">Returns **TRUE** if the parameter is being used and returns **FALSE** if the parameter is not being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5051d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5051d-118">Requirements</span></span>



| <span data-ttu-id="5051d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5051d-119">Requirement</span></span> | <span data-ttu-id="5051d-120">Value</span><span class="sxs-lookup"><span data-stu-id="5051d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5051d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5051d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5051d-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5051d-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5051d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5051d-123">Library</span></span><br/> | <dl> <span data-ttu-id="5051d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5051d-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5051d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5051d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5051d-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="5051d-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 

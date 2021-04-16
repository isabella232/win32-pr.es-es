---
description: Obtiene el identificador de un paso.
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'ID3DXBaseEffect:: GetPass (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5db5c5da16a65b53b6e266886ee6ab8472dc3246
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424519"
---
# <a name="id3dxbaseeffectgetpass-method"></a><span data-ttu-id="00ca8-103">ID3DXBaseEffect:: GetPass (método)</span><span class="sxs-lookup"><span data-stu-id="00ca8-103">ID3DXBaseEffect::GetPass method</span></span>

<span data-ttu-id="00ca8-104">Obtiene el identificador de un paso.</span><span class="sxs-lookup"><span data-stu-id="00ca8-104">Gets the handle of a pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ca8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00ca8-105">Syntax</span></span>


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="00ca8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00ca8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ca8-107">*hTechnique* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00ca8-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca8-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="00ca8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="00ca8-109">Identificador de la técnica primaria.</span><span class="sxs-lookup"><span data-stu-id="00ca8-109">Handle of the parent technique.</span></span> <span data-ttu-id="00ca8-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="00ca8-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="00ca8-111">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="00ca8-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca8-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00ca8-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00ca8-113">Índice para el paso.</span><span class="sxs-lookup"><span data-stu-id="00ca8-113">Index for the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ca8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00ca8-114">Return value</span></span>

<span data-ttu-id="00ca8-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="00ca8-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="00ca8-116">Devuelve el identificador del paso especificado dentro de la técnica especificada, o **null** si el índice no era válido.</span><span class="sxs-lookup"><span data-stu-id="00ca8-116">Returns the handle of the specified pass inside the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="00ca8-117">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="00ca8-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00ca8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00ca8-118">Requirements</span></span>



| <span data-ttu-id="00ca8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00ca8-119">Requirement</span></span> | <span data-ttu-id="00ca8-120">Value</span><span class="sxs-lookup"><span data-stu-id="00ca8-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ca8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00ca8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="00ca8-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="00ca8-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="00ca8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00ca8-123">Library</span></span><br/> | <dl> <span data-ttu-id="00ca8-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00ca8-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="00ca8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="00ca8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ca8-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="00ca8-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

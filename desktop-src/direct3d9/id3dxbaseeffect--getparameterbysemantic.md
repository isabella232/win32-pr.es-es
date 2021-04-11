---
description: Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su semántica con una búsqueda que no distinga mayúsculas de minúsculas.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'ID3DXBaseEffect:: GetParameterBySemantic (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362775"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a><span data-ttu-id="2d55b-103">ID3DXBaseEffect:: GetParameterBySemantic (método)</span><span class="sxs-lookup"><span data-stu-id="2d55b-103">ID3DXBaseEffect::GetParameterBySemantic method</span></span>

<span data-ttu-id="2d55b-104">Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su semántica con una búsqueda que no distinga mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2d55b-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its semantic with a case-insensitive search.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d55b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d55b-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a><span data-ttu-id="2d55b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d55b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d55b-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d55b-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d55b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2d55b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2d55b-109">Identificador del parámetro o **null** para los parámetros de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="2d55b-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="2d55b-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2d55b-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d55b-111">*pSemantic* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d55b-111">*pSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d55b-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d55b-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d55b-113">Cadena que contiene el nombre semántico.</span><span class="sxs-lookup"><span data-stu-id="2d55b-113">String containing the semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d55b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d55b-114">Return value</span></span>

<span data-ttu-id="2d55b-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2d55b-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2d55b-116">Devuelve el identificador del primer parámetro que coincide con la semántica especificada, o **null** si no se encontró la semántica.</span><span class="sxs-lookup"><span data-stu-id="2d55b-116">Returns the handle of the first parameter that matches the specified semantic, or **NULL** if the semantic was not found.</span></span> <span data-ttu-id="2d55b-117">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2d55b-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d55b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d55b-118">Requirements</span></span>



| <span data-ttu-id="2d55b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d55b-119">Requirement</span></span> | <span data-ttu-id="2d55b-120">Value</span><span class="sxs-lookup"><span data-stu-id="2d55b-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d55b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d55b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2d55b-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d55b-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2d55b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d55b-123">Library</span></span><br/> | <dl> <span data-ttu-id="2d55b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d55b-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2d55b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d55b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d55b-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2d55b-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

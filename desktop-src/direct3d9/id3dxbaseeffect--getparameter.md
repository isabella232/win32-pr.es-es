---
description: Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'ID3DXBaseEffect:: GetParameter (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083806"
---
# <a name="id3dxbaseeffectgetparameter-method"></a><span data-ttu-id="0aa41-103">ID3DXBaseEffect:: GetParameter (método)</span><span class="sxs-lookup"><span data-stu-id="0aa41-103">ID3DXBaseEffect::GetParameter method</span></span>

<span data-ttu-id="0aa41-104">Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="0aa41-104">Gets the handle of a top-level parameter or a structure member parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0aa41-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="0aa41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0aa41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa41-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa41-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa41-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0aa41-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0aa41-109">Identificador del parámetro o **null** para los parámetros de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="0aa41-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="0aa41-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0aa41-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0aa41-111">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0aa41-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa41-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0aa41-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0aa41-113">Índice del parámetro.</span><span class="sxs-lookup"><span data-stu-id="0aa41-113">Parameter index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa41-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0aa41-114">Return value</span></span>

<span data-ttu-id="0aa41-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0aa41-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0aa41-116">Devuelve el identificador del parámetro especificado, o **null** si el índice no era válido.</span><span class="sxs-lookup"><span data-stu-id="0aa41-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="0aa41-117">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0aa41-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa41-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa41-118">Requirements</span></span>



| <span data-ttu-id="0aa41-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa41-119">Requirement</span></span> | <span data-ttu-id="0aa41-120">Value</span><span class="sxs-lookup"><span data-stu-id="0aa41-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa41-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aa41-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0aa41-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aa41-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0aa41-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0aa41-123">Library</span></span><br/> | <dl> <span data-ttu-id="0aa41-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0aa41-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0aa41-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aa41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa41-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0aa41-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

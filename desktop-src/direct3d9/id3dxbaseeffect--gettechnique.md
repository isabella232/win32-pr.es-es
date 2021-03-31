---
description: Obtiene el identificador de una técnica.
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: 'ID3DXBaseEffect:: GetTechnique (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f0c82c301a48eb939d182062240c4dba6d3fc63
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157252"
---
# <a name="id3dxbaseeffectgettechnique-method"></a><span data-ttu-id="d87d2-103">ID3DXBaseEffect:: GetTechnique (método)</span><span class="sxs-lookup"><span data-stu-id="d87d2-103">ID3DXBaseEffect::GetTechnique method</span></span>

<span data-ttu-id="d87d2-104">Obtiene el identificador de una técnica.</span><span class="sxs-lookup"><span data-stu-id="d87d2-104">Gets the handle of a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="d87d2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d87d2-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="d87d2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d87d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d87d2-107">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d87d2-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d87d2-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d87d2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d87d2-109">Índice de técnica.</span><span class="sxs-lookup"><span data-stu-id="d87d2-109">Technique index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d87d2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d87d2-110">Return value</span></span>

<span data-ttu-id="d87d2-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d87d2-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d87d2-112">Devuelve el identificador de la técnica especificada, o **null** si el índice no era válido.</span><span class="sxs-lookup"><span data-stu-id="d87d2-112">Returns the handle of the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="d87d2-113">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d87d2-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d87d2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d87d2-114">Requirements</span></span>



| <span data-ttu-id="d87d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d87d2-115">Requirement</span></span> | <span data-ttu-id="d87d2-116">Value</span><span class="sxs-lookup"><span data-stu-id="d87d2-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d87d2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d87d2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d87d2-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d87d2-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d87d2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d87d2-119">Library</span></span><br/> | <dl> <span data-ttu-id="d87d2-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d87d2-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d87d2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d87d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87d2-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="d87d2-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

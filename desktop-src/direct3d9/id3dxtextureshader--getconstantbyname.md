---
description: Obtiene una constante buscando su nombre.
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: 'ID3DXTextureShader:: GetConstantByName (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a285da2fa3179f91d34eda8d9ce1f622c86df15b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708031"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a><span data-ttu-id="d9745-103">ID3DXTextureShader:: GetConstantByName (método)</span><span class="sxs-lookup"><span data-stu-id="d9745-103">ID3DXTextureShader::GetConstantByName method</span></span>

<span data-ttu-id="d9745-104">Obtiene una constante buscando su nombre.</span><span class="sxs-lookup"><span data-stu-id="d9745-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9745-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9745-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="d9745-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9745-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9745-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9745-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9745-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d9745-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d9745-109">[Identificador](handles.md) de la estructura de datos primaria.</span><span class="sxs-lookup"><span data-stu-id="d9745-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="d9745-110">Si la constante es un parámetro de nivel superior (no hay ninguna estructura de datos primaria), use **null**.</span><span class="sxs-lookup"><span data-stu-id="d9745-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d9745-111">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9745-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9745-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9745-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9745-113">Cadena que contiene el nombre de la constante.</span><span class="sxs-lookup"><span data-stu-id="d9745-113">A string containing the name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9745-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9745-114">Return value</span></span>

<span data-ttu-id="d9745-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d9745-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d9745-116">Devuelve un identificador único a la constante.</span><span class="sxs-lookup"><span data-stu-id="d9745-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9745-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9745-117">Requirements</span></span>



| <span data-ttu-id="d9745-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9745-118">Requirement</span></span> | <span data-ttu-id="d9745-119">Value</span><span class="sxs-lookup"><span data-stu-id="d9745-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9745-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9745-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d9745-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9745-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d9745-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9745-122">Library</span></span><br/> | <dl> <span data-ttu-id="d9745-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9745-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d9745-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9745-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9745-125">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d9745-125">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 

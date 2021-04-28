---
description: 'Método ID3DXTextureShader::GetConstant: obtiene una constante mediante la búsqueda de su índice.'
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: Método ID3DXTextureShader::GetConstant (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117673"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="e7b49-103">Método ID3DXTextureShader::GetConstant</span><span class="sxs-lookup"><span data-stu-id="e7b49-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="e7b49-104">Obtiene una constante mediante la búsqueda de su índice.</span><span class="sxs-lookup"><span data-stu-id="e7b49-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7b49-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="e7b49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7b49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b49-107">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e7b49-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b49-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e7b49-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e7b49-109">Identificador [de](handles.md) la estructura de datos primaria.</span><span class="sxs-lookup"><span data-stu-id="e7b49-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="e7b49-110">Si la constante es un parámetro de nivel superior (no hay ninguna estructura de datos primaria), use **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e7b49-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7b49-111">*Índice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e7b49-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b49-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7b49-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7b49-113">Índice de base cero de la constante.</span><span class="sxs-lookup"><span data-stu-id="e7b49-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b49-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7b49-114">Return value</span></span>

<span data-ttu-id="e7b49-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e7b49-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e7b49-116">Devuelve un identificador único a la constante.</span><span class="sxs-lookup"><span data-stu-id="e7b49-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b49-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7b49-117">Remarks</span></span>

<span data-ttu-id="e7b49-118">Para obtener una constante de una matriz de constantes, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="e7b49-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b49-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7b49-119">Requirements</span></span>



| <span data-ttu-id="e7b49-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b49-120">Requirement</span></span> | <span data-ttu-id="e7b49-121">Value</span><span class="sxs-lookup"><span data-stu-id="e7b49-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b49-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7b49-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e7b49-123"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b49-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e7b49-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7b49-124">Library</span></span><br/> | <dl> <span data-ttu-id="e7b49-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7b49-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e7b49-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e7b49-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b49-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e7b49-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 

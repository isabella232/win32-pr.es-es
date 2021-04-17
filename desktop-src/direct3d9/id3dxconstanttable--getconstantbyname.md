---
description: Obtiene una constante buscando su nombre.
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: 'ID3DXConstantTable:: GetConstantByName (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3df4fc2cf44e035daf208d5dd14602e89b528ed1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698284"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="58fb6-103">ID3DXConstantTable:: GetConstantByName (método)</span><span class="sxs-lookup"><span data-stu-id="58fb6-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="58fb6-104">Obtiene una constante buscando su nombre.</span><span class="sxs-lookup"><span data-stu-id="58fb6-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="58fb6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58fb6-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="58fb6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58fb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58fb6-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58fb6-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb6-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="58fb6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="58fb6-109">Identificador único de la estructura de datos primaria.</span><span class="sxs-lookup"><span data-stu-id="58fb6-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="58fb6-110">Si la constante es un parámetro de nivel superior (no hay ninguna estructura de datos primaria), use **null**.</span><span class="sxs-lookup"><span data-stu-id="58fb6-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="58fb6-111">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58fb6-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb6-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58fb6-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58fb6-113">Nombre de la constante.</span><span class="sxs-lookup"><span data-stu-id="58fb6-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58fb6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58fb6-114">Return value</span></span>

<span data-ttu-id="58fb6-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="58fb6-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="58fb6-116">Devuelve un identificador único a la constante.</span><span class="sxs-lookup"><span data-stu-id="58fb6-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="58fb6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58fb6-117">Requirements</span></span>



| <span data-ttu-id="58fb6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="58fb6-118">Requirement</span></span> | <span data-ttu-id="58fb6-119">Value</span><span class="sxs-lookup"><span data-stu-id="58fb6-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="58fb6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58fb6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="58fb6-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="58fb6-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="58fb6-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58fb6-122">Library</span></span><br/> | <dl> <span data-ttu-id="58fb6-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58fb6-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="58fb6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="58fb6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58fb6-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="58fb6-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 

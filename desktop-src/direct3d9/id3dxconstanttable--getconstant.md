---
description: Obtiene una constante mediante la búsqueda de su índice.
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: 'ID3DXConstantTable:: GetConstant (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4ab7318dc4a05f586db77817653e7df59ef6083
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698285"
---
# <a name="id3dxconstanttablegetconstant-method"></a><span data-ttu-id="fab07-103">ID3DXConstantTable:: GetConstant (método)</span><span class="sxs-lookup"><span data-stu-id="fab07-103">ID3DXConstantTable::GetConstant method</span></span>

<span data-ttu-id="fab07-104">Obtiene una constante mediante la búsqueda de su índice.</span><span class="sxs-lookup"><span data-stu-id="fab07-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab07-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fab07-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="fab07-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fab07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab07-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fab07-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab07-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fab07-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fab07-109">Identificador único de la estructura de datos primaria.</span><span class="sxs-lookup"><span data-stu-id="fab07-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="fab07-110">Si la constante es un parámetro de nivel superior (no hay ninguna estructura de datos primaria), use **null**.</span><span class="sxs-lookup"><span data-stu-id="fab07-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fab07-111">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fab07-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fab07-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fab07-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fab07-113">Índice de base cero de la constante.</span><span class="sxs-lookup"><span data-stu-id="fab07-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fab07-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fab07-114">Return value</span></span>

<span data-ttu-id="fab07-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fab07-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fab07-116">Devuelve un identificador único a la constante.</span><span class="sxs-lookup"><span data-stu-id="fab07-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="fab07-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fab07-117">Remarks</span></span>

<span data-ttu-id="fab07-118">Para obtener una constante de una matriz de constantes, use [**ID3DXConstantTable:: GetConstantElement**](id3dxconstanttable--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="fab07-118">To get a constant from an array of constants, use [**ID3DXConstantTable::GetConstantElement**](id3dxconstanttable--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fab07-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fab07-119">Requirements</span></span>



| <span data-ttu-id="fab07-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab07-120">Requirement</span></span> | <span data-ttu-id="fab07-121">Value</span><span class="sxs-lookup"><span data-stu-id="fab07-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fab07-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fab07-122">Header</span></span><br/>  | <dl> <span data-ttu-id="fab07-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fab07-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fab07-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fab07-124">Library</span></span><br/> | <dl> <span data-ttu-id="fab07-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fab07-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fab07-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="fab07-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab07-127">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="fab07-127">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 

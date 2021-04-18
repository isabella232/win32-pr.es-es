---
description: Obtiene una constante de una matriz de constantes. Una matriz se compone de elementos.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'ID3DXConstantTable:: GetConstantElement (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718256"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a><span data-ttu-id="0baf7-104">ID3DXConstantTable:: GetConstantElement (método)</span><span class="sxs-lookup"><span data-stu-id="0baf7-104">ID3DXConstantTable::GetConstantElement method</span></span>

<span data-ttu-id="0baf7-105">Obtiene una constante de una matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="0baf7-105">Gets a constant from an array of constants.</span></span> <span data-ttu-id="0baf7-106">Una matriz se compone de elementos.</span><span class="sxs-lookup"><span data-stu-id="0baf7-106">An array is made up of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="0baf7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0baf7-107">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="0baf7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0baf7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0baf7-109">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0baf7-109">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0baf7-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0baf7-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0baf7-111">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="0baf7-111">Unique identifier to the array of constants.</span></span> <span data-ttu-id="0baf7-112">Este valor no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="0baf7-112">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0baf7-113">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0baf7-113">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0baf7-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0baf7-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0baf7-115">Índice de base cero del elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="0baf7-115">Zero-based index of the element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0baf7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0baf7-116">Return value</span></span>

<span data-ttu-id="0baf7-117">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0baf7-117">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0baf7-118">Devuelve un identificador único a la constante del elemento.</span><span class="sxs-lookup"><span data-stu-id="0baf7-118">Returns a unique identifier to the element constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="0baf7-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0baf7-119">Remarks</span></span>

<span data-ttu-id="0baf7-120">Para obtener una constante que no forma parte de una matriz, use [**ID3DXConstantTable:: GetConstant**](id3dxconstanttable--getconstant.md) o [**ID3DXConstantTable:: GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span><span class="sxs-lookup"><span data-stu-id="0baf7-120">To get a constant that is not part of an array, use [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) or [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0baf7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0baf7-121">Requirements</span></span>



| <span data-ttu-id="0baf7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0baf7-122">Requirement</span></span> | <span data-ttu-id="0baf7-123">Value</span><span class="sxs-lookup"><span data-stu-id="0baf7-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0baf7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0baf7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0baf7-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0baf7-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0baf7-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0baf7-126">Library</span></span><br/> | <dl> <span data-ttu-id="0baf7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0baf7-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0baf7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0baf7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0baf7-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0baf7-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 

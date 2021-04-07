---
description: Obtiene un puntero a una matriz de descripciones constantes en la tabla Constant.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'ID3DXConstantTable:: GetConstantDesc (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003838"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a><span data-ttu-id="fb020-103">ID3DXConstantTable:: GetConstantDesc (método)</span><span class="sxs-lookup"><span data-stu-id="fb020-103">ID3DXConstantTable::GetConstantDesc method</span></span>

<span data-ttu-id="fb020-104">Obtiene un puntero a una matriz de descripciones constantes en la tabla Constant.</span><span class="sxs-lookup"><span data-stu-id="fb020-104">Gets a pointer to an array of constant descriptions in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb020-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb020-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="fb020-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb020-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb020-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb020-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb020-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fb020-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fb020-109">Identificador único de una constante.</span><span class="sxs-lookup"><span data-stu-id="fb020-109">Unique identifier to a constant.</span></span> <span data-ttu-id="fb020-110">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fb020-110">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb020-111">*pDesc* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fb020-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb020-112">Tipo: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb020-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="fb020-113">Devuelve un puntero a una matriz de descripciones.</span><span class="sxs-lookup"><span data-stu-id="fb020-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="fb020-114">Vea [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="fb020-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb020-115">*pCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fb020-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb020-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb020-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fb020-117">La entrada proporcionada debe ser el tamaño máximo de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fb020-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="fb020-118">El resultado es el número de elementos que se rellenan en la matriz cuando la función devuelve.</span><span class="sxs-lookup"><span data-stu-id="fb020-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb020-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb020-119">Return value</span></span>

<span data-ttu-id="fb020-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb020-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb020-121">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb020-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb020-122">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="fb020-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb020-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb020-123">Remarks</span></span>

<span data-ttu-id="fb020-124">**ID3DXConstantTable:: GetConstantDesc** devolverá a veces una [**\_ Descripción de D3DXCONSTANT**](d3dxconstant-desc.md) con un \_ recuento de registros de 0.</span><span class="sxs-lookup"><span data-stu-id="fb020-124">**ID3DXConstantTable::GetConstantDesc** will sometimes return a [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md) with a Register\_Count of 0.</span></span> <span data-ttu-id="fb020-125">Esto ocurrirá cuando una constante aparezca en más de un conjunto de registros, \_ pero no en el conjunto de registros asignado.</span><span class="sxs-lookup"><span data-stu-id="fb020-125">This will happen with a constant appears in more than one Register\_Set but does not have space in that register set allocated.</span></span>

<span data-ttu-id="fb020-126">Dado que una muestra puede aparecer más de una vez en una tabla de constantes, este método puede devolver una matriz de descripciones, cada una con un índice de registro diferente.</span><span class="sxs-lookup"><span data-stu-id="fb020-126">Because a sampler can appear more than once in a constant table, this method can return an array of descriptions, each one with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb020-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb020-127">Requirements</span></span>



| <span data-ttu-id="fb020-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb020-128">Requirement</span></span> | <span data-ttu-id="fb020-129">Value</span><span class="sxs-lookup"><span data-stu-id="fb020-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb020-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb020-130">Header</span></span><br/>  | <dl> <span data-ttu-id="fb020-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb020-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fb020-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb020-132">Library</span></span><br/> | <dl> <span data-ttu-id="fb020-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb020-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fb020-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb020-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb020-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="fb020-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="fb020-136">**ID3DXConstantTable::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="fb020-136">**ID3DXConstantTable::GetDesc**</span></span>](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 

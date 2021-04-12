---
description: Obtiene el identificador de un parámetro de elemento de matriz.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'ID3DXBaseEffect:: GetParameterElement (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362774"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a><span data-ttu-id="52325-103">ID3DXBaseEffect:: GetParameterElement (método)</span><span class="sxs-lookup"><span data-stu-id="52325-103">ID3DXBaseEffect::GetParameterElement method</span></span>

<span data-ttu-id="52325-104">Obtiene el identificador de un parámetro de elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="52325-104">Get the handle of an array element parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="52325-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52325-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a><span data-ttu-id="52325-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52325-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52325-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52325-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52325-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="52325-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="52325-109">Identificador de la matriz.</span><span class="sxs-lookup"><span data-stu-id="52325-109">Handle of the array.</span></span> <span data-ttu-id="52325-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="52325-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="52325-111">*ElementIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52325-111">*ElementIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52325-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52325-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52325-113">Índice del elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="52325-113">Array element index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52325-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52325-114">Return value</span></span>

<span data-ttu-id="52325-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="52325-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="52325-116">Devuelve el identificador del parámetro especificado, o **null** si HParameter o ElementIndex no son válidos.</span><span class="sxs-lookup"><span data-stu-id="52325-116">Returns the handle of the specified parameter, or **NULL** if either hParameter or ElementIndex is invalid.</span></span> <span data-ttu-id="52325-117">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="52325-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52325-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52325-118">Remarks</span></span>

<span data-ttu-id="52325-119">Este método se usa para obtener un elemento de un parámetro que es una matriz.</span><span class="sxs-lookup"><span data-stu-id="52325-119">This method is used to get an element of a parameter that is an array.</span></span>

## <a name="requirements"></a><span data-ttu-id="52325-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52325-120">Requirements</span></span>



| <span data-ttu-id="52325-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="52325-121">Requirement</span></span> | <span data-ttu-id="52325-122">Value</span><span class="sxs-lookup"><span data-stu-id="52325-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="52325-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52325-123">Header</span></span><br/>  | <dl> <span data-ttu-id="52325-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="52325-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="52325-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52325-125">Library</span></span><br/> | <dl> <span data-ttu-id="52325-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52325-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="52325-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="52325-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52325-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="52325-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 

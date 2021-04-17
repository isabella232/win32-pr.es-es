---
description: Devuelve el índice de muestra.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: 'ID3DXConstantTable:: GetSamplerIndex (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f803b6e129ac20b8a22ed2393ab941698c02d3d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718255"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a><span data-ttu-id="bd69c-103">ID3DXConstantTable:: GetSamplerIndex (método)</span><span class="sxs-lookup"><span data-stu-id="bd69c-103">ID3DXConstantTable::GetSamplerIndex method</span></span>

<span data-ttu-id="bd69c-104">Devuelve el índice de muestra.</span><span class="sxs-lookup"><span data-stu-id="bd69c-104">Returns the sampler index.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd69c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd69c-105">Syntax</span></span>


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a><span data-ttu-id="bd69c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd69c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd69c-107">*hConstant* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bd69c-107">*hConstant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd69c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bd69c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bd69c-109">Identificador de muestra.</span><span class="sxs-lookup"><span data-stu-id="bd69c-109">The sampler handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd69c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd69c-110">Return value</span></span>

<span data-ttu-id="bd69c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd69c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd69c-112">Devuelve el número de índice de muestra de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="bd69c-112">Returns the sampler index number from the constant table.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd69c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd69c-113">Requirements</span></span>



| <span data-ttu-id="bd69c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd69c-114">Requirement</span></span> | <span data-ttu-id="bd69c-115">Value</span><span class="sxs-lookup"><span data-stu-id="bd69c-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd69c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd69c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bd69c-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd69c-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bd69c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd69c-118">Library</span></span><br/> | <dl> <span data-ttu-id="bd69c-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd69c-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bd69c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd69c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd69c-121">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="bd69c-121">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 

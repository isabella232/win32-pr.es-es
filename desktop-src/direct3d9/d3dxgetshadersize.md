---
description: Devuelve el tamaño del código de byte del sombreador, en bytes.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: Función D3DXGetShaderSize (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717756"
---
# <a name="d3dxgetshadersize-function"></a><span data-ttu-id="28751-103">D3DXGetShaderSize función)</span><span class="sxs-lookup"><span data-stu-id="28751-103">D3DXGetShaderSize function</span></span>

<span data-ttu-id="28751-104">Devuelve el tamaño del código de byte del sombreador, en bytes.</span><span class="sxs-lookup"><span data-stu-id="28751-104">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="28751-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28751-105">Syntax</span></span>


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="28751-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28751-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28751-107">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28751-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28751-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="28751-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="28751-109">Puntero a la secuencia DWORD de la función.</span><span class="sxs-lookup"><span data-stu-id="28751-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28751-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28751-110">Return value</span></span>

<span data-ttu-id="28751-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28751-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28751-112">Devuelve el tamaño del código de byte del sombreador, en bytes.</span><span class="sxs-lookup"><span data-stu-id="28751-112">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="28751-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28751-113">Requirements</span></span>



| <span data-ttu-id="28751-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="28751-114">Requirement</span></span> | <span data-ttu-id="28751-115">Value</span><span class="sxs-lookup"><span data-stu-id="28751-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28751-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28751-116">Header</span></span><br/>  | <dl> <span data-ttu-id="28751-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="28751-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="28751-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28751-118">Library</span></span><br/> | <dl> <span data-ttu-id="28751-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28751-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="28751-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="28751-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28751-121">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="28751-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 

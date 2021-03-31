---
description: Devuelve la versión del sombreador del sombreador compilado.
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: Función D3DXGetShaderVersion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157184"
---
# <a name="d3dxgetshaderversion-function"></a><span data-ttu-id="f81b4-103">D3DXGetShaderVersion función)</span><span class="sxs-lookup"><span data-stu-id="f81b4-103">D3DXGetShaderVersion function</span></span>

<span data-ttu-id="f81b4-104">Devuelve la versión del sombreador del sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="f81b4-104">Returns the shader version of the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="f81b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f81b4-105">Syntax</span></span>


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="f81b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f81b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f81b4-107">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f81b4-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81b4-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f81b4-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f81b4-109">Puntero a la secuencia DWORD de la función.</span><span class="sxs-lookup"><span data-stu-id="f81b4-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f81b4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f81b4-110">Return value</span></span>

<span data-ttu-id="f81b4-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f81b4-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f81b4-112">Devuelve la versión del sombreador del sombreador dado, o cero si la función de sombreador es **null**.</span><span class="sxs-lookup"><span data-stu-id="f81b4-112">Returns the shader version of the given shader, or zero if the shader function is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f81b4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f81b4-113">Requirements</span></span>



| <span data-ttu-id="f81b4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f81b4-114">Requirement</span></span> | <span data-ttu-id="f81b4-115">Value</span><span class="sxs-lookup"><span data-stu-id="f81b4-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f81b4-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f81b4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f81b4-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f81b4-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f81b4-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f81b4-118">Library</span></span><br/> | <dl> <span data-ttu-id="f81b4-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f81b4-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f81b4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f81b4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f81b4-121">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="f81b4-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 

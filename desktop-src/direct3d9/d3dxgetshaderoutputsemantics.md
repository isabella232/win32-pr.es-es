---
description: Obtiene la semántica de todos los elementos de salida del sombreador.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: Función D3DXGetShaderOutputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547894"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a><span data-ttu-id="27875-103">D3DXGetShaderOutputSemantics función)</span><span class="sxs-lookup"><span data-stu-id="27875-103">D3DXGetShaderOutputSemantics function</span></span>

<span data-ttu-id="27875-104">Obtiene la semántica de todos los elementos de salida del sombreador.</span><span class="sxs-lookup"><span data-stu-id="27875-104">Get the semantics for all shader output elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="27875-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27875-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="27875-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27875-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27875-107">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27875-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27875-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="27875-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="27875-109">Puntero a la secuencia DWORD de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="27875-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="27875-110">*pSemantics* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27875-110">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27875-111">Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="27875-111">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="27875-112">Puntero a una matriz de estructuras [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="27875-112">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="27875-113">La función rellenará esta matriz con la semántica de cada elemento de salida al que hace referencia el sombreador.</span><span class="sxs-lookup"><span data-stu-id="27875-113">The function will fill this array with the semantics for each output element referenced by the shader.</span></span> <span data-ttu-id="27875-114">Se supone que esta matriz contiene al menos elementos MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="27875-114">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="27875-115">Sin embargo, si se llama a **D3DXGetShaderOutputSemantics** con PSemantics = **null** , se devolverá el número de elementos necesarios para pCount.</span><span class="sxs-lookup"><span data-stu-id="27875-115">However, calling **D3DXGetShaderOutputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="27875-116">*pCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="27875-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27875-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="27875-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="27875-118">Devuelve el número de elementos de pSemantics.</span><span class="sxs-lookup"><span data-stu-id="27875-118">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27875-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27875-119">Return value</span></span>

<span data-ttu-id="27875-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="27875-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="27875-121">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="27875-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="27875-122">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="27875-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="27875-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27875-123">Requirements</span></span>



| <span data-ttu-id="27875-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="27875-124">Requirement</span></span> | <span data-ttu-id="27875-125">Value</span><span class="sxs-lookup"><span data-stu-id="27875-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="27875-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27875-126">Header</span></span><br/>  | <dl> <span data-ttu-id="27875-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="27875-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="27875-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27875-128">Library</span></span><br/> | <dl> <span data-ttu-id="27875-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27875-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="27875-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="27875-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27875-131">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="27875-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 

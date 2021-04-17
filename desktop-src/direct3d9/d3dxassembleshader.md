---
description: Ensamble un sombreador.
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: Función D3DXAssembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7268d394021c7dc1be665f8ed8781a827d1fcdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698294"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="54d61-103">D3DXAssembleShader función)</span><span class="sxs-lookup"><span data-stu-id="54d61-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="54d61-104">Ensamble un sombreador.</span><span class="sxs-lookup"><span data-stu-id="54d61-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54d61-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataLen,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="54d61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54d61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d61-107">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54d61-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d61-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54d61-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54d61-109">Puntero a un búfer de memoria que contiene los datos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="54d61-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="54d61-110">*SrcDataLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54d61-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d61-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54d61-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54d61-112">Longitud de los datos del efecto, en bytes.</span><span class="sxs-lookup"><span data-stu-id="54d61-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="54d61-113">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54d61-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d61-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="54d61-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="54d61-115">Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** .</span><span class="sxs-lookup"><span data-stu-id="54d61-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="54d61-116">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="54d61-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54d61-117">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54d61-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d61-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="54d61-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="54d61-119">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="54d61-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="54d61-120">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="54d61-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="54d61-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="54d61-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d61-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54d61-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54d61-123">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="54d61-123">Compile options identified by various flags.</span></span> <span data-ttu-id="54d61-124">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="54d61-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="54d61-125">Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="54d61-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="54d61-126">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="54d61-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54d61-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="54d61-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="54d61-128">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="54d61-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="54d61-129">Este búfer contiene el código del sombreador compilado, así como cualquier información de la tabla de símbolos y de depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="54d61-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="54d61-130">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="54d61-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54d61-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="54d61-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="54d61-132">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="54d61-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="54d61-133">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="54d61-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="54d61-134">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="54d61-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d61-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54d61-135">Return value</span></span>

<span data-ttu-id="54d61-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54d61-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54d61-137">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54d61-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="54d61-138">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="54d61-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="54d61-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54d61-139">Requirements</span></span>



| <span data-ttu-id="54d61-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="54d61-140">Requirement</span></span> | <span data-ttu-id="54d61-141">Value</span><span class="sxs-lookup"><span data-stu-id="54d61-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54d61-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54d61-142">Header</span></span><br/>  | <dl> <span data-ttu-id="54d61-143"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="54d61-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="54d61-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54d61-144">Library</span></span><br/> | <dl> <span data-ttu-id="54d61-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54d61-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="54d61-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="54d61-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d61-147">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="54d61-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="54d61-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="54d61-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="54d61-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="54d61-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 

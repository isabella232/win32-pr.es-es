---
description: 'Función D3DXAssembleShader: ensamblar un sombreador.'
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: Función D3DXAssembleShader (D3DX9Shader.h)
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
ms.openlocfilehash: 891281ebc3db970ca61132fe49ba98531ca1d879
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116053"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="d37c9-103">Función D3DXAssembleShader</span><span class="sxs-lookup"><span data-stu-id="d37c9-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="d37c9-104">Ensamblar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="d37c9-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d37c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d37c9-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d37c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d37c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d37c9-107">*pSrcData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d37c9-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37c9-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d37c9-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d37c9-109">Puntero a un búfer de memoria que contiene los datos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d37c9-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="d37c9-110">*SrcDataLen* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d37c9-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37c9-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d37c9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d37c9-112">Longitud de los datos del efecto, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d37c9-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d37c9-113">*pDefines* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d37c9-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37c9-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="d37c9-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="d37c9-115">Matriz **terminada en NULL** opcional de estructuras [**D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="d37c9-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="d37c9-116">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="d37c9-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d37c9-117">*pInclude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d37c9-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37c9-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="d37c9-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="d37c9-119">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include.</span><span class="sxs-lookup"><span data-stu-id="d37c9-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="d37c9-120">Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.</span><span class="sxs-lookup"><span data-stu-id="d37c9-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="d37c9-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="d37c9-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37c9-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d37c9-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d37c9-123">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="d37c9-123">Compile options identified by various flags.</span></span> <span data-ttu-id="d37c9-124">El compilador HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d37c9-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="d37c9-125">Consulte [D3DXSHADER Flags (Marcas de D3DXSHADER)](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d37c9-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="d37c9-126">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d37c9-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d37c9-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d37c9-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d37c9-128">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="d37c9-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="d37c9-129">Este búfer contiene el código del sombreador compilado, así como cualquier información de tabla de símbolos y depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="d37c9-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="d37c9-130">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d37c9-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d37c9-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d37c9-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d37c9-132">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="d37c9-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="d37c9-133">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="d37c9-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="d37c9-134">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="d37c9-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d37c9-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d37c9-135">Return value</span></span>

<span data-ttu-id="d37c9-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d37c9-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d37c9-137">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d37c9-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d37c9-138">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d37c9-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d37c9-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d37c9-139">Requirements</span></span>



| <span data-ttu-id="d37c9-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d37c9-140">Requirement</span></span> | <span data-ttu-id="d37c9-141">Value</span><span class="sxs-lookup"><span data-stu-id="d37c9-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d37c9-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d37c9-142">Header</span></span><br/>  | <dl> <span data-ttu-id="d37c9-143"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="d37c9-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d37c9-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d37c9-144">Library</span></span><br/> | <dl> <span data-ttu-id="d37c9-145"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d37c9-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d37c9-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d37c9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d37c9-147">Funciones de sombreador</span><span class="sxs-lookup"><span data-stu-id="d37c9-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="d37c9-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="d37c9-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="d37c9-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="d37c9-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 

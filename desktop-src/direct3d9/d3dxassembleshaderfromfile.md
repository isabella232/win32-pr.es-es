---
description: 'Función D3DXAssembleShaderFromFile: ensamblar un sombreador.'
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: Función D3DXAssembleShaderFromFile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91aaf2924638b1db5b0e8ec0782b90fa964a9543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116033"
---
# <a name="d3dxassembleshaderfromfile-function"></a><span data-ttu-id="7251f-103">Función D3DXAssembleShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="7251f-103">D3DXAssembleShaderFromFile function</span></span>

<span data-ttu-id="7251f-104">Ensamblar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="7251f-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="7251f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7251f-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="7251f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7251f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7251f-107">*pSrcFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7251f-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7251f-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7251f-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7251f-109">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="7251f-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="7251f-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="7251f-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7251f-111">De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="7251f-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="7251f-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7251f-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7251f-113">*pDefines* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7251f-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7251f-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="7251f-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="7251f-115">Matriz **terminada en NULL** opcional de estructuras [**D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="7251f-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="7251f-116">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7251f-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7251f-117">*pInclude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7251f-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7251f-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="7251f-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="7251f-119">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include.</span><span class="sxs-lookup"><span data-stu-id="7251f-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="7251f-120">Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.</span><span class="sxs-lookup"><span data-stu-id="7251f-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="7251f-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7251f-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7251f-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7251f-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7251f-123">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="7251f-123">Compile options identified by various flags.</span></span> <span data-ttu-id="7251f-124">El compilador HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7251f-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="7251f-125">Consulte [D3DXSHADER Flags (Marcas de D3DXSHADER)](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7251f-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="7251f-126">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7251f-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7251f-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7251f-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7251f-128">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="7251f-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="7251f-129">Este búfer contiene el código del sombreador compilado, así como cualquier información de tabla de símbolos y depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="7251f-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="7251f-130">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7251f-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7251f-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7251f-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7251f-132">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="7251f-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="7251f-133">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="7251f-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="7251f-134">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7251f-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7251f-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7251f-135">Return value</span></span>

<span data-ttu-id="7251f-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7251f-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7251f-137">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7251f-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7251f-138">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7251f-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7251f-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7251f-139">Remarks</span></span>

<span data-ttu-id="7251f-140">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="7251f-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7251f-141">Si se define Unicode, la llamada de función se resuelve en D3DXAssembleShaderFromFileW.</span><span class="sxs-lookup"><span data-stu-id="7251f-141">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromFileW.</span></span> <span data-ttu-id="7251f-142">De lo contrario, la llamada de función se resuelve en D3DXAssembleShaderFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="7251f-142">Otherwise, the function call resolves to D3DXAssembleShaderFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7251f-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7251f-143">Requirements</span></span>



| <span data-ttu-id="7251f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7251f-144">Requirement</span></span> | <span data-ttu-id="7251f-145">Value</span><span class="sxs-lookup"><span data-stu-id="7251f-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7251f-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7251f-146">Header</span></span><br/>  | <dl> <span data-ttu-id="7251f-147"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="7251f-147"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7251f-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7251f-148">Library</span></span><br/> | <dl> <span data-ttu-id="7251f-149"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7251f-149"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7251f-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7251f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7251f-151">Funciones de sombreador</span><span class="sxs-lookup"><span data-stu-id="7251f-151">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="7251f-152">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="7251f-152">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="7251f-153">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="7251f-153">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 

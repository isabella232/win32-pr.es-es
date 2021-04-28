---
description: 'Función D3DXAssembleShaderFromResource: ensamblar un sombreador.'
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: Función D3DXAssembleShaderFromResource (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78df978201df37269b7d33058effc16eadc9d16f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116023"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="b3bb8-103">Función D3DXAssembleShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="b3bb8-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="b3bb8-104">Ensamblar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3bb8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3bb8-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="b3bb8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3bb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3bb8-107">*hSrcModule* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b3bb8-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3bb8-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3bb8-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3bb8-109">Identificador de un módulo que contiene la descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="b3bb8-110">Si este parámetro es **NULL,** se usará el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb8-111">*pSrcResource* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b3bb8-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3bb8-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3bb8-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3bb8-113">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="b3bb8-114">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b3bb8-115">De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="b3bb8-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb8-117">*pDefines* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b3bb8-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3bb8-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3bb8-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="b3bb8-119">Matriz **opcional terminada** en NULL de estructuras [**D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="b3bb8-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="b3bb8-120">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="b3bb8-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb8-121">*pInclude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b3bb8-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3bb8-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="b3bb8-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="b3bb8-123">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="b3bb8-124">Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb8-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b3bb8-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3bb8-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3bb8-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3bb8-127">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-127">Compile options identified by various flags.</span></span> <span data-ttu-id="b3bb8-128">El compilador HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="b3bb8-129">Consulte [D3DXSHADER Flags (Marcas de D3DXSHADER)](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb8-130">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b3bb8-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3bb8-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3bb8-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b3bb8-132">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="b3bb8-133">Este búfer contiene el código del sombreador compilado, así como cualquier información de tabla de símbolos y depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb8-134">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b3bb8-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3bb8-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3bb8-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b3bb8-136">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="b3bb8-137">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="b3bb8-138">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="b3bb8-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3bb8-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3bb8-139">Return value</span></span>

<span data-ttu-id="b3bb8-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3bb8-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3bb8-141">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b3bb8-142">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3bb8-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3bb8-143">Remarks</span></span>

<span data-ttu-id="b3bb8-144">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b3bb8-145">Si se define Unicode, la llamada a la función se resuelve en D3DXAssembleShaderFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="b3bb8-146">De lo contrario, la llamada de función se resuelve en D3DXAssembleShaderFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="b3bb8-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3bb8-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3bb8-147">Requirements</span></span>



| <span data-ttu-id="b3bb8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3bb8-148">Requirement</span></span> | <span data-ttu-id="b3bb8-149">Value</span><span class="sxs-lookup"><span data-stu-id="b3bb8-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3bb8-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3bb8-150">Header</span></span><br/>  | <dl> <span data-ttu-id="b3bb8-151"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb8-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b3bb8-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3bb8-152">Library</span></span><br/> | <dl> <span data-ttu-id="b3bb8-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb8-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b3bb8-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b3bb8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3bb8-155">Funciones de sombreador</span><span class="sxs-lookup"><span data-stu-id="b3bb8-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="b3bb8-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="b3bb8-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="b3bb8-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="b3bb8-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 

---
description: 'Función D3DXCompileShaderFromFile: compile un archivo de sombreador.'
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: Función D3DXCompileShaderFromFile (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4392a3c36b31deb4071c215ad9b41e7f40c21ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115853"
---
# <a name="d3dxcompileshaderfromfile-function"></a><span data-ttu-id="a8bba-103">Función D3DXCompileShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="a8bba-103">D3DXCompileShaderFromFile function</span></span>

<span data-ttu-id="a8bba-104">Compile un archivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8bba-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="a8bba-105">En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos Fxc.exe o usar la API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)</span><span class="sxs-lookup"><span data-stu-id="a8bba-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a8bba-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8bba-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromFile(
  _In_        LPCTSTR             pSrcFile,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="a8bba-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8bba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8bba-108">*pSrcFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a8bba-108">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bba-109">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8bba-109">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8bba-110">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="a8bba-110">Pointer to a string that specifies the filename.</span></span>

</dd> <dt>

<span data-ttu-id="a8bba-111">*pDefines* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a8bba-111">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bba-112">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8bba-112">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="a8bba-113">Matriz **opcional terminada** en NULL de estructuras [**D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="a8bba-113">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="a8bba-114">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8bba-114">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a8bba-115">*pInclude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a8bba-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bba-116">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="a8bba-116">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="a8bba-117">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include.</span><span class="sxs-lookup"><span data-stu-id="a8bba-117">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="a8bba-118">Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.</span><span class="sxs-lookup"><span data-stu-id="a8bba-118">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="a8bba-119">*pFunctionName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a8bba-119">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bba-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8bba-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8bba-121">Puntero a la función de punto de entrada del sombreador donde comienza la ejecución.</span><span class="sxs-lookup"><span data-stu-id="a8bba-121">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="a8bba-122">*pProfile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a8bba-122">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bba-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8bba-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8bba-124">Puntero a un perfil de sombreador que determina el conjunto de instrucciones del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8bba-124">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="a8bba-125">Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obtener una lista de los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="a8bba-125">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="a8bba-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a8bba-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bba-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8bba-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8bba-128">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="a8bba-128">Compile options identified by various flags.</span></span> <span data-ttu-id="a8bba-129">El compilador HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a8bba-129">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="a8bba-130">Consulte [D3DXSHADER Flags (Marcas de D3DXSHADER)](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a8bba-130">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="a8bba-131">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a8bba-131">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bba-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8bba-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a8bba-133">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="a8bba-133">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="a8bba-134">Este búfer contiene el código del sombreador compilado, así como cualquier información de tabla de símbolos y depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="a8bba-134">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="a8bba-135">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a8bba-135">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bba-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8bba-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a8bba-137">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="a8bba-137">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="a8bba-138">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="a8bba-138">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="a8bba-139">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8bba-139">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a8bba-140">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a8bba-140">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8bba-141">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8bba-141">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="a8bba-142">Devuelve una [**interfaz ID3DXConstantTable,**](id3dxconstanttable.md) que se puede usar para tener acceso a las constantes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8bba-142">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="a8bba-143">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8bba-143">This value can be **NULL**.</span></span> <span data-ttu-id="a8bba-144">Si compila la aplicación como una dirección grande (es decir, usa la opción del vinculador /LARGEADDRESSAWARE para controlar direcciones de más de 2 GB), no puede usar este parámetro y debe establecerlo en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8bba-144">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="a8bba-145">En su lugar, debe usar la función [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar la tabla shader-constant incrustada dentro del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8bba-145">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="a8bba-146">En esta **llamada D3DXGetShaderConstantTableEx,** debe pasar la marca **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parámetro *Flags* para especificar el acceso a hasta 4 GB de espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="a8bba-146">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8bba-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8bba-147">Return value</span></span>

<span data-ttu-id="a8bba-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8bba-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8bba-149">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8bba-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a8bba-150">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ NOTIMPL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a8bba-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="a8bba-151">Se \_ devuelve E NOTIMPL si usa sombreadores 1.1 (frente a \_ \_ 1 1 y ps \_ \_ 1 1).</span><span class="sxs-lookup"><span data-stu-id="a8bba-151">E\_NOTIMPL is returned if you're using 1.1 shaders (vs\_1\_1 and ps\_1\_1).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8bba-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8bba-152">Requirements</span></span>



| <span data-ttu-id="a8bba-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8bba-153">Requirement</span></span> | <span data-ttu-id="a8bba-154">Value</span><span class="sxs-lookup"><span data-stu-id="a8bba-154">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bba-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8bba-155">Header</span></span><br/>  | <dl> <span data-ttu-id="a8bba-156"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="a8bba-156"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a8bba-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8bba-157">Library</span></span><br/> | <dl> <span data-ttu-id="a8bba-158"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8bba-158"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a8bba-159">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8bba-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bba-160">Funciones de sombreador</span><span class="sxs-lookup"><span data-stu-id="a8bba-160">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="a8bba-161">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="a8bba-161">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="a8bba-162">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="a8bba-162">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 

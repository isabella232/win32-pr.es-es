---
description: 'Función D3DXCompileShader: compile un archivo de sombreador.'
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: Función D3DXCompileShader (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1f5e5f0f30714ed001438235e124341b8ce4d35
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115863"
---
# <a name="d3dxcompileshader-function"></a><span data-ttu-id="65609-103">Función D3DXCompileShader</span><span class="sxs-lookup"><span data-stu-id="65609-103">D3DXCompileShader function</span></span>

<span data-ttu-id="65609-104">Compile un archivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="65609-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="65609-105">En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos Fxc.exe o usar la API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)</span><span class="sxs-lookup"><span data-stu-id="65609-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="65609-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65609-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
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



## <a name="parameters"></a><span data-ttu-id="65609-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65609-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65609-108">*pSrcData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65609-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-109">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65609-109">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65609-110">Puntero a una cadena que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="65609-110">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="65609-111">*srcDataLen* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65609-111">*srcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65609-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65609-113">Longitud de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="65609-113">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="65609-114">*pDefines* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65609-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-115">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="65609-115">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="65609-116">Matriz **opcional terminada** en NULL de estructuras [**D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="65609-116">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="65609-117">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="65609-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="65609-118">*pInclude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65609-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-119">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="65609-119">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="65609-120">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include.</span><span class="sxs-lookup"><span data-stu-id="65609-120">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="65609-121">Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.</span><span class="sxs-lookup"><span data-stu-id="65609-121">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="65609-122">*pFunctionName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65609-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65609-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65609-124">Puntero a una cadena que contiene el nombre de la función de punto de entrada del sombreador donde comienza la ejecución.</span><span class="sxs-lookup"><span data-stu-id="65609-124">Pointer to a string that contains the name of the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="65609-125">*pProfile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65609-125">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-126">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65609-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65609-127">Puntero a un perfil de sombreador que determina el conjunto de instrucciones del sombreador.</span><span class="sxs-lookup"><span data-stu-id="65609-127">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="65609-128">Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obtener una lista de los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="65609-128">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="65609-129">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="65609-129">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65609-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65609-131">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="65609-131">Compile options identified by various flags.</span></span> <span data-ttu-id="65609-132">El compilador HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="65609-132">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="65609-133">Consulte [D3DXSHADER Flags (Marcas de D3DXSHADER)](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="65609-133">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="65609-134">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65609-134">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="65609-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="65609-136">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="65609-136">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="65609-137">Este búfer contiene el código del sombreador compilado, así como cualquier información de tabla de símbolos y depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="65609-137">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="65609-138">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65609-138">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-139">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="65609-139">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="65609-140">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="65609-140">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="65609-141">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="65609-141">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="65609-142">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="65609-142">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="65609-143">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65609-143">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65609-144">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="65609-144">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="65609-145">Devuelve una [**interfaz ID3DXConstantTable,**](id3dxconstanttable.md) que se puede usar para tener acceso a las constantes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="65609-145">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="65609-146">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="65609-146">This value can be **NULL**.</span></span> <span data-ttu-id="65609-147">Si compila la aplicación como una dirección grande (es decir, usa la opción del vinculador /LARGEADDRESSAWARE para controlar direcciones de más de 2 GB), no puede usar este parámetro y debe establecerlo en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="65609-147">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="65609-148">En su lugar, debe usar la función [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar la tabla shader-constant incrustada dentro del sombreador.</span><span class="sxs-lookup"><span data-stu-id="65609-148">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="65609-149">En esta **llamada D3DXGetShaderConstantTableEx,** debe pasar la marca **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parámetro *Flags* para especificar el acceso a hasta 4 GB de espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="65609-149">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65609-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65609-150">Return value</span></span>

<span data-ttu-id="65609-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65609-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65609-152">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65609-152">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="65609-153">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="65609-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="65609-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65609-154">Requirements</span></span>



| <span data-ttu-id="65609-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="65609-155">Requirement</span></span> | <span data-ttu-id="65609-156">Value</span><span class="sxs-lookup"><span data-stu-id="65609-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65609-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65609-157">Header</span></span><br/>  | <dl> <span data-ttu-id="65609-158"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="65609-158"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="65609-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65609-159">Library</span></span><br/> | <dl> <span data-ttu-id="65609-160"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="65609-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="65609-161">Consulte también</span><span class="sxs-lookup"><span data-stu-id="65609-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65609-162">Funciones de sombreador</span><span class="sxs-lookup"><span data-stu-id="65609-162">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="65609-163">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="65609-163">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="65609-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="65609-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 

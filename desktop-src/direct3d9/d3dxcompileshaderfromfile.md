---
description: Compilar un archivo de sombreador.
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: Función D3DXCompileShaderFromFile (D3DX9Shader. h)
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
ms.openlocfilehash: 865241142fa13ec9d34826bfe334c30b38ca78d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718268"
---
# <a name="d3dxcompileshaderfromfile-function"></a><span data-ttu-id="01579-103">D3DXCompileShaderFromFile función)</span><span class="sxs-lookup"><span data-stu-id="01579-103">D3DXCompileShaderFromFile function</span></span>

<span data-ttu-id="01579-104">Compilar un archivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="01579-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="01579-105">En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="01579-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="01579-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01579-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="01579-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01579-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01579-108">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01579-108">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01579-109">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01579-109">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01579-110">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="01579-110">Pointer to a string that specifies the filename.</span></span>

</dd> <dt>

<span data-ttu-id="01579-111">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01579-111">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01579-112">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="01579-112">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="01579-113">Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** .</span><span class="sxs-lookup"><span data-stu-id="01579-113">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="01579-114">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="01579-114">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="01579-115">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01579-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01579-116">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="01579-116">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="01579-117">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="01579-117">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="01579-118">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="01579-118">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="01579-119">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01579-119">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01579-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01579-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01579-121">Puntero a la función de punto de entrada del sombreador en la que comienza la ejecución.</span><span class="sxs-lookup"><span data-stu-id="01579-121">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="01579-122">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01579-122">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01579-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01579-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01579-124">Puntero a un perfil de sombreador que determina el conjunto de instrucciones del sombreador.</span><span class="sxs-lookup"><span data-stu-id="01579-124">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="01579-125">Vea [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obtener una lista de los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="01579-125">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="01579-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="01579-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01579-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01579-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01579-128">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="01579-128">Compile options identified by various flags.</span></span> <span data-ttu-id="01579-129">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="01579-129">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="01579-130">Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="01579-130">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="01579-131">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="01579-131">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01579-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="01579-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="01579-133">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="01579-133">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="01579-134">Este búfer contiene el código del sombreador compilado, así como cualquier información de la tabla de símbolos y de depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="01579-134">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="01579-135">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="01579-135">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01579-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="01579-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="01579-137">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="01579-137">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="01579-138">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="01579-138">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="01579-139">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="01579-139">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="01579-140">*ppConstantTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="01579-140">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01579-141">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="01579-141">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="01579-142">Devuelve una interfaz [**ID3DXConstantTable**](id3dxconstanttable.md) , que se puede usar para tener acceso a las constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="01579-142">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="01579-143">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="01579-143">This value can be **NULL**.</span></span> <span data-ttu-id="01579-144">Si compila la aplicación como compatible con direcciones grandes (es decir, usa la opción del vinculador/LARGEADDRESSAWARE para controlar direcciones de más de 2 GB), no puede utilizar este parámetro y debe establecerlo en **null**.</span><span class="sxs-lookup"><span data-stu-id="01579-144">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="01579-145">En su lugar, debe usar la función [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar la tabla de constantes del sombreador que está incrustada en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="01579-145">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="01579-146">En esta llamada a **D3DXGetShaderConstantTableEx** , debe pasar la marca **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parámetro *Flags* para especificar que se tenga acceso a un máximo de 4 GB de espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="01579-146">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01579-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01579-147">Return value</span></span>

<span data-ttu-id="01579-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01579-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01579-149">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="01579-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="01579-150">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ NOTIMPL, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="01579-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="01579-151">\_Se devuelve E NOTIMPL si está utilizando sombreadores 1,1 (vs \_ 1 \_ 1 y PS \_ 1 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="01579-151">E\_NOTIMPL is returned if you're using 1.1 shaders (vs\_1\_1 and ps\_1\_1).</span></span>

## <a name="requirements"></a><span data-ttu-id="01579-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01579-152">Requirements</span></span>



| <span data-ttu-id="01579-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="01579-153">Requirement</span></span> | <span data-ttu-id="01579-154">Value</span><span class="sxs-lookup"><span data-stu-id="01579-154">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01579-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01579-155">Header</span></span><br/>  | <dl> <span data-ttu-id="01579-156"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="01579-156"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="01579-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01579-157">Library</span></span><br/> | <dl> <span data-ttu-id="01579-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01579-158"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="01579-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="01579-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01579-160">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="01579-160">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="01579-161">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="01579-161">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="01579-162">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="01579-162">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 

---
description: Compilar un archivo de sombreador.
ms.assetid: e944ae61-0c27-4795-8381-0ec9b3d8c3f4
title: Función D3DXCompileShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1bbb48fa2932eecb82c1c45d303d7afb948fa4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678812"
---
# <a name="d3dxcompileshaderfromresource-function"></a><span data-ttu-id="0d4fc-103">D3DXCompileShaderFromResource función)</span><span class="sxs-lookup"><span data-stu-id="0d4fc-103">D3DXCompileShaderFromResource function</span></span>

<span data-ttu-id="0d4fc-104">Compilar un archivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="0d4fc-105">En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="0d4fc-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0d4fc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d4fc-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromResource(
  _In_        HMODULE             hSrcModule,
  _In_        LPCSTR              pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="0d4fc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d4fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d4fc-108">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-108">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-109">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fc-109">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d4fc-110">Identificador de un módulo que contiene la descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-110">Handle to a module containing the effect description.</span></span> <span data-ttu-id="0d4fc-111">Si este parámetro es **null**, se usará el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-111">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fc-112">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-112">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fc-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d4fc-114">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-114">Pointer to a string that specifies the resource name.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fc-115">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-116">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="0d4fc-116">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="0d4fc-117">Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** .</span><span class="sxs-lookup"><span data-stu-id="0d4fc-117">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="0d4fc-118">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-118">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fc-119">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-120">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fc-120">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="0d4fc-121">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-121">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="0d4fc-122">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-122">If this value is **NULL**, \#includes will either be honored when compiling from a file, or will error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fc-123">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-123">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-124">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fc-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d4fc-125">Puntero a la función de punto de entrada del sombreador en la que comienza la ejecución.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-125">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fc-126">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-127">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fc-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d4fc-128">Puntero a un perfil de sombreador que determina el conjunto de instrucciones del sombreador.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-128">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="0d4fc-129">Vea [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obtener una lista de los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-129">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fc-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fc-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d4fc-132">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-132">Compile options identified by various flags.</span></span> <span data-ttu-id="0d4fc-133">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="0d4fc-134">Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-134">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fc-135">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-135">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d4fc-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0d4fc-137">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-137">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="0d4fc-138">Este búfer contiene el código del sombreador compilado, así como cualquier información de la tabla de símbolos y de depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-138">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fc-139">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d4fc-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0d4fc-141">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-141">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="0d4fc-142">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-142">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="0d4fc-143">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-143">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fc-144">*ppConstantTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d4fc-144">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fc-145">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d4fc-145">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="0d4fc-146">Devuelve una interfaz [**ID3DXConstantTable**](id3dxconstanttable.md) , que se puede usar para tener acceso a las constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-146">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="0d4fc-147">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-147">This value can be **NULL**.</span></span> <span data-ttu-id="0d4fc-148">Si compila la aplicación como compatible con direcciones grandes (es decir, usa la opción del vinculador/LARGEADDRESSAWARE para controlar direcciones de más de 2 GB), no puede utilizar este parámetro y debe establecerlo en **null**.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-148">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="0d4fc-149">En su lugar, debe usar la función [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar la tabla de constantes del sombreador que está incrustada en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-149">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="0d4fc-150">En esta llamada a **D3DXGetShaderConstantTableEx** , debe pasar la marca **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parámetro *Flags* para especificar que se tenga acceso a un máximo de 4 GB de espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-150">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d4fc-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d4fc-151">Return value</span></span>

<span data-ttu-id="0d4fc-152">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d4fc-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d4fc-153">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0d4fc-154">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0d4fc-154">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4fc-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d4fc-155">Requirements</span></span>



| <span data-ttu-id="0d4fc-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d4fc-156">Requirement</span></span> | <span data-ttu-id="0d4fc-157">Value</span><span class="sxs-lookup"><span data-stu-id="0d4fc-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4fc-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d4fc-158">Header</span></span><br/>  | <dl> <span data-ttu-id="0d4fc-159"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fc-159"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0d4fc-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d4fc-160">Library</span></span><br/> | <dl> <span data-ttu-id="0d4fc-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fc-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0d4fc-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d4fc-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d4fc-163">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="0d4fc-163">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="0d4fc-164">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="0d4fc-164">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="0d4fc-165">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="0d4fc-165">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> </dl>

 

 

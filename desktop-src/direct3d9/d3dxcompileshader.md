---
description: Compilar un archivo de sombreador.
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: Función D3DXCompileShader (D3DX9Shader. h)
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
ms.openlocfilehash: 65dd9f74280abe7ee2fe427a4772b14b88742e97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362545"
---
# <a name="d3dxcompileshader-function"></a><span data-ttu-id="72f91-103">D3DXCompileShader función)</span><span class="sxs-lookup"><span data-stu-id="72f91-103">D3DXCompileShader function</span></span>

<span data-ttu-id="72f91-104">Compilar un archivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="72f91-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="72f91-105">En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="72f91-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="72f91-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72f91-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="72f91-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72f91-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72f91-108">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f91-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-109">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72f91-109">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72f91-110">Puntero a una cadena que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="72f91-110">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="72f91-111">*srcDataLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f91-111">*srcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72f91-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72f91-113">Longitud de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="72f91-113">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="72f91-114">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f91-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-115">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="72f91-115">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="72f91-116">Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** .</span><span class="sxs-lookup"><span data-stu-id="72f91-116">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="72f91-117">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="72f91-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="72f91-118">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f91-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-119">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="72f91-119">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="72f91-120">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="72f91-120">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="72f91-121">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="72f91-121">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="72f91-122">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f91-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72f91-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72f91-124">Puntero a una cadena que contiene el nombre de la función del punto de entrada del sombreador en el que comienza la ejecución.</span><span class="sxs-lookup"><span data-stu-id="72f91-124">Pointer to a string that contains the name of the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="72f91-125">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f91-125">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-126">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72f91-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72f91-127">Puntero a un perfil de sombreador que determina el conjunto de instrucciones del sombreador.</span><span class="sxs-lookup"><span data-stu-id="72f91-127">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="72f91-128">Vea [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obtener una lista de los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="72f91-128">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="72f91-129">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="72f91-129">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72f91-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72f91-131">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="72f91-131">Compile options identified by various flags.</span></span> <span data-ttu-id="72f91-132">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="72f91-132">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="72f91-133">Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="72f91-133">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="72f91-134">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="72f91-134">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="72f91-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="72f91-136">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="72f91-136">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="72f91-137">Este búfer contiene el código del sombreador compilado, así como cualquier información de la tabla de símbolos y de depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="72f91-137">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="72f91-138">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="72f91-138">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-139">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="72f91-139">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="72f91-140">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="72f91-140">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="72f91-141">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="72f91-141">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="72f91-142">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="72f91-142">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="72f91-143">*ppConstantTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="72f91-143">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72f91-144">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="72f91-144">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="72f91-145">Devuelve una interfaz [**ID3DXConstantTable**](id3dxconstanttable.md) , que se puede usar para tener acceso a las constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="72f91-145">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="72f91-146">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="72f91-146">This value can be **NULL**.</span></span> <span data-ttu-id="72f91-147">Si compila la aplicación como compatible con direcciones grandes (es decir, usa la opción del vinculador/LARGEADDRESSAWARE para controlar direcciones de más de 2 GB), no puede utilizar este parámetro y debe establecerlo en **null**.</span><span class="sxs-lookup"><span data-stu-id="72f91-147">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="72f91-148">En su lugar, debe usar la función [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar la tabla de constantes del sombreador que está incrustada en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="72f91-148">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="72f91-149">En esta llamada a **D3DXGetShaderConstantTableEx** , debe pasar la marca **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parámetro *Flags* para especificar que se tenga acceso a un máximo de 4 GB de espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="72f91-149">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72f91-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72f91-150">Return value</span></span>

<span data-ttu-id="72f91-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="72f91-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="72f91-152">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="72f91-152">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="72f91-153">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="72f91-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f91-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72f91-154">Requirements</span></span>



| <span data-ttu-id="72f91-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="72f91-155">Requirement</span></span> | <span data-ttu-id="72f91-156">Value</span><span class="sxs-lookup"><span data-stu-id="72f91-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f91-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72f91-157">Header</span></span><br/>  | <dl> <span data-ttu-id="72f91-158"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f91-158"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="72f91-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72f91-159">Library</span></span><br/> | <dl> <span data-ttu-id="72f91-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72f91-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="72f91-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="72f91-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f91-162">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="72f91-162">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="72f91-163">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="72f91-163">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="72f91-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="72f91-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 

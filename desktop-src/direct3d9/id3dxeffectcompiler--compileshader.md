---
description: Compila un sombreador a partir de un efecto que contiene una o más funciones.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'ID3DXEffectCompiler:: CompileShader (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 375646202e102623053c179398329ad2286e6c1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707973"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="772e4-103">ID3DXEffectCompiler:: CompileShader (método)</span><span class="sxs-lookup"><span data-stu-id="772e4-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="772e4-104">Compila un sombreador a partir de un efecto que contiene una o más funciones.</span><span class="sxs-lookup"><span data-stu-id="772e4-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="772e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="772e4-105">Syntax</span></span>


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="772e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="772e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="772e4-107">*hFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="772e4-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e4-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="772e4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="772e4-109">Identificador único de la función que se va a compilar.</span><span class="sxs-lookup"><span data-stu-id="772e4-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="772e4-110">Este valor no debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="772e4-110">This value must not be **NULL**.</span></span> <span data-ttu-id="772e4-111">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="772e4-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="772e4-112">*pTarget* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="772e4-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e4-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="772e4-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="772e4-114">Puntero a un perfil de sombreador que determina el conjunto de instrucciones del sombreador.</span><span class="sxs-lookup"><span data-stu-id="772e4-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="772e4-115">Vea [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obtener una lista de los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="772e4-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="772e4-116">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="772e4-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e4-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="772e4-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="772e4-118">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="772e4-118">Compile options identified by various flags.</span></span> <span data-ttu-id="772e4-119">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="772e4-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="772e4-120">Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="772e4-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="772e4-121">*ppShader* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="772e4-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="772e4-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="772e4-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="772e4-123">Búfer que contiene el sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="772e4-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="772e4-124">El sombreador del compilador es una matriz de DWORDs.</span><span class="sxs-lookup"><span data-stu-id="772e4-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="772e4-125">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="772e4-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="772e4-126">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="772e4-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="772e4-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="772e4-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="772e4-128">Búfer que contiene al menos el primer mensaje de error de compilación que se produjo.</span><span class="sxs-lookup"><span data-stu-id="772e4-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="772e4-129">Esto incluye los errores del compilador y los errores de compilación de lenguaje de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="772e4-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="772e4-130">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="772e4-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="772e4-131">*ppConstantTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="772e4-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="772e4-132">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="772e4-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="772e4-133">Devuelve una interfaz [**ID3DXConstantTable**](id3dxconstanttable.md) , que se puede usar para tener acceso a las constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="772e4-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="772e4-134">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="772e4-134">This value can be **NULL**.</span></span> <span data-ttu-id="772e4-135">Si compila la aplicación como compatible con direcciones grandes (es decir, usa la opción del vinculador/LARGEADDRESSAWARE para controlar direcciones de más de 2 GB), no puede utilizar este parámetro y debe establecerlo en **null**.</span><span class="sxs-lookup"><span data-stu-id="772e4-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="772e4-136">En su lugar, debe usar la función [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar la tabla de constantes del sombreador que está incrustada en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="772e4-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="772e4-137">En esta llamada a **D3DXGetShaderConstantTableEx** , debe pasar la marca **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parámetro *Flags* para especificar que se tenga acceso a un máximo de 4 GB de espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="772e4-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="772e4-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="772e4-138">Return value</span></span>

<span data-ttu-id="772e4-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="772e4-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="772e4-140">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="772e4-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="772e4-141">Si los argumentos no son válidos, el método devolverá D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="772e4-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="772e4-142">Si se produce un error en el método, el valor devuelto será E \_ producirá un error.</span><span class="sxs-lookup"><span data-stu-id="772e4-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="772e4-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="772e4-143">Remarks</span></span>

<span data-ttu-id="772e4-144">Los destinos se pueden especificar para los sombreadores de vértices, los sombreadores de píxeles y las funciones de relleno de textura.</span><span class="sxs-lookup"><span data-stu-id="772e4-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



|                       |                                                                       |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="772e4-145">Destinos del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="772e4-145">Vertex shader targets</span></span> | <span data-ttu-id="772e4-146">vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ SW, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="772e4-146">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="772e4-147">Destinos del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="772e4-147">Pixel shader targets</span></span>  | <span data-ttu-id="772e4-148">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, PS \_ 2 \_ 0, PS \_ 2 \_ SW, PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="772e4-148">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="772e4-149">Destinos de relleno de textura</span><span class="sxs-lookup"><span data-stu-id="772e4-149">Texture fill targets</span></span>  | <span data-ttu-id="772e4-150">TX \_ 0, TX \_ 1</span><span class="sxs-lookup"><span data-stu-id="772e4-150">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="772e4-151">Este método compila un sombreador a partir de una función escrita en un lenguaje de tipo C.</span><span class="sxs-lookup"><span data-stu-id="772e4-151">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="772e4-152">Para obtener más información, vea [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="772e4-152">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="772e4-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="772e4-153">Requirements</span></span>



| <span data-ttu-id="772e4-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="772e4-154">Requirement</span></span> | <span data-ttu-id="772e4-155">Value</span><span class="sxs-lookup"><span data-stu-id="772e4-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="772e4-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="772e4-156">Header</span></span><br/>  | <dl> <span data-ttu-id="772e4-157"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="772e4-157"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="772e4-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="772e4-158">Library</span></span><br/> | <dl> <span data-ttu-id="772e4-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="772e4-159"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="772e4-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="772e4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772e4-161">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="772e4-161">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="772e4-162">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="772e4-162">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 

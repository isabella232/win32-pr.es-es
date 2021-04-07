---
description: Tenga en cuenta que, en lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API D3DCompile. Compilar un sombreador o un efecto que se carga en la memoria.
ms.assetid: c6458d82-a649-402c-8180-5b7320f9fdb0
title: Función D3DX10CompileFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: fbb4a716df4a893ea122e7badfd6faad536aacce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003939"
---
# <a name="d3dx10compilefrommemory-function"></a><span data-ttu-id="74b28-104">D3DX10CompileFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="74b28-104">D3DX10CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="74b28-105">En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="74b28-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="74b28-106">Compilar un sombreador o un efecto que se carga en la memoria.</span><span class="sxs-lookup"><span data-stu-id="74b28-106">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b28-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74b28-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="74b28-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74b28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74b28-109">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74b28-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74b28-111">Puntero al sombreador en la memoria.</span><span class="sxs-lookup"><span data-stu-id="74b28-111">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-112">*SrcDataLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-112">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-113">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74b28-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74b28-114">Tamaño del sombreador en la memoria.</span><span class="sxs-lookup"><span data-stu-id="74b28-114">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-115">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74b28-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74b28-117">Nombre del archivo que contiene el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="74b28-117">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-118">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-119">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="74b28-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="74b28-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="74b28-120">Optional.</span></span> <span data-ttu-id="74b28-121">Puntero a una matriz de definiciones de macro (vea la [**\_ \_ macro del sombreador de D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="74b28-121">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="74b28-122">La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0.</span><span class="sxs-lookup"><span data-stu-id="74b28-122">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="74b28-123">Si no se usa, establezca *pDefines* en **null**.</span><span class="sxs-lookup"><span data-stu-id="74b28-123">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-124">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-125">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="74b28-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="74b28-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="74b28-126">Optional.</span></span> <span data-ttu-id="74b28-127">Puntero a una interfaz de [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para administrar archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="74b28-127">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="74b28-128">Si se establece en **null** , se producirá un error de compilación si un sombreador contiene un \# include.</span><span class="sxs-lookup"><span data-stu-id="74b28-128">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-129">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-129">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-130">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74b28-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74b28-131">Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="74b28-131">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="74b28-132">Al compilar un efecto, **D3DX10CompileFromMemory** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="74b28-132">When you compile an effect, **D3DX10CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-133">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-133">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-134">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74b28-134">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74b28-135">Cadena que especifica el modelo de sombreador; puede ser cualquier perfil en el modelo de sombreador [2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), el [modelo de sombreador 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o el [modelo de sombreador 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="74b28-135">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="74b28-136">*Flags1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-137">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74b28-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74b28-138">[Marcas de compilación del sombreador](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="74b28-138">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="74b28-139">*Flags2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-140">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74b28-140">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74b28-141">[Marcas de compilación de efectos](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="74b28-141">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="74b28-142">Al compilar un sombreador y no un archivo de efectos, **D3DX10CompileFromMemory** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="74b28-142">When you compile a shader and not an effect file, **D3DX10CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-143">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-144">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="74b28-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="74b28-145">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="74b28-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="74b28-146">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="74b28-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-147">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="74b28-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-148">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="74b28-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="74b28-149">Puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene el sombreador compilado, así como cualquier información de depuración y de tabla de símbolos incrustada.</span><span class="sxs-lookup"><span data-stu-id="74b28-149">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-150">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="74b28-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-151">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="74b28-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="74b28-152">Un puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene una lista de errores y advertencias que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="74b28-152">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="74b28-153">Estos errores y advertencias son idénticos a los resultados de depuración de un depurador.</span><span class="sxs-lookup"><span data-stu-id="74b28-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-154">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="74b28-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-155">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="74b28-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="74b28-156">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="74b28-156">A pointer to the return value.</span></span> <span data-ttu-id="74b28-157">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="74b28-157">May be **NULL**.</span></span> <span data-ttu-id="74b28-158">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="74b28-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74b28-159">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74b28-159">Return value</span></span>

<span data-ttu-id="74b28-160">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74b28-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74b28-161">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="74b28-161">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74b28-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74b28-162">Requirements</span></span>



| <span data-ttu-id="74b28-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="74b28-163">Requirement</span></span> | <span data-ttu-id="74b28-164">Value</span><span class="sxs-lookup"><span data-stu-id="74b28-164">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b28-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74b28-165">Header</span></span><br/> | <dl> <span data-ttu-id="74b28-166"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="74b28-166"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74b28-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="74b28-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b28-168">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="74b28-168">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

---
description: Tenga en cuenta que, en lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API D3DCompile. Compilar un sombreador o un efecto desde un recurso.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: Función D3DX10CompileFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717682"
---
# <a name="d3dx10compilefromresource-function"></a><span data-ttu-id="33841-104">D3DX10CompileFromResource función)</span><span class="sxs-lookup"><span data-stu-id="33841-104">D3DX10CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="33841-105">En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="33841-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="33841-106">Compilar un sombreador o un efecto desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="33841-106">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="33841-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33841-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="33841-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33841-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33841-109">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-109">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-110">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33841-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33841-111">Identificador del módulo de recursos que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="33841-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="33841-112">HMODULE se puede obtener con la [función GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="33841-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="33841-113">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33841-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33841-115">Nombre del recurso que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="33841-115">Name of the resource containing the shader.</span></span> <span data-ttu-id="33841-116">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="33841-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="33841-117">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="33841-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="33841-118">*pSrcFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-119">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33841-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33841-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="33841-120">Optional.</span></span> <span data-ttu-id="33841-121">Nombre del archivo de efectos, que solo se usa para los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="33841-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="33841-122">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="33841-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33841-123">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-124">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="33841-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="33841-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="33841-125">Optional.</span></span> <span data-ttu-id="33841-126">Puntero a una matriz de definiciones de macro (vea la [**\_ \_ macro del sombreador de D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="33841-126">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="33841-127">La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0.</span><span class="sxs-lookup"><span data-stu-id="33841-127">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="33841-128">Si no se usa, establezca *pDefines* en **null**.</span><span class="sxs-lookup"><span data-stu-id="33841-128">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33841-129">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-130">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="33841-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="33841-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="33841-131">Optional.</span></span> <span data-ttu-id="33841-132">Puntero a una interfaz de [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para administrar archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="33841-132">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="33841-133">Si se establece en **null** , se producirá un error de compilación si un sombreador contiene un \# include.</span><span class="sxs-lookup"><span data-stu-id="33841-133">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="33841-134">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-134">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-135">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33841-135">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33841-136">Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="33841-136">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="33841-137">Al compilar un efecto, **D3DX10CompileFromResource** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="33841-137">When you compile an effect, **D3DX10CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="33841-138">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-138">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-139">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33841-139">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33841-140">Cadena que especifica el modelo de sombreador; puede ser cualquier perfil en el modelo de sombreador [2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), el [modelo de sombreador 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o el [modelo de sombreador 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="33841-140">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="33841-141">*Flags1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-141">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-142">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33841-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33841-143">[Marcas de compilación del sombreador](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="33841-143">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="33841-144">*Flags2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-144">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-145">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33841-145">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33841-146">[Marcas de compilación de efectos](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="33841-146">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="33841-147">Al compilar un sombreador y no un archivo de efectos, **D3DX10CompileFromResource** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="33841-147">When you compile a shader and not an effect file, **D3DX10CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="33841-148">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33841-148">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-149">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="33841-149">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="33841-150">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="33841-150">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="33841-151">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="33841-151">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="33841-152">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="33841-152">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-153">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="33841-153">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="33841-154">Puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene el sombreador compilado, así como cualquier información de depuración y de tabla de símbolos incrustada.</span><span class="sxs-lookup"><span data-stu-id="33841-154">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="33841-155">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="33841-155">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-156">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="33841-156">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="33841-157">Un puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene una lista de errores y advertencias que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="33841-157">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="33841-158">Estos errores y advertencias son idénticos a los resultados de depuración de un depurador.</span><span class="sxs-lookup"><span data-stu-id="33841-158">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="33841-159">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="33841-159">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33841-160">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="33841-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="33841-161">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="33841-161">A pointer to the return value.</span></span> <span data-ttu-id="33841-162">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="33841-162">May be **NULL**.</span></span> <span data-ttu-id="33841-163">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="33841-163">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33841-164">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33841-164">Return value</span></span>

<span data-ttu-id="33841-165">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33841-165">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33841-166">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="33841-166">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33841-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33841-167">Requirements</span></span>



| <span data-ttu-id="33841-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="33841-168">Requirement</span></span> | <span data-ttu-id="33841-169">Value</span><span class="sxs-lookup"><span data-stu-id="33841-169">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33841-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33841-170">Header</span></span><br/> | <dl> <span data-ttu-id="33841-171"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="33841-171"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33841-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="33841-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33841-173">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="33841-173">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

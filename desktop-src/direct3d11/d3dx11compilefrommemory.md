---
title: Función D3DX11CompileFromMemory (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API D3DCompile. Compilar un sombreador o un efecto que se carga en la memoria.
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- Función D3DX11CompileFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987031"
---
# <a name="d3dx11compilefrommemory-function"></a><span data-ttu-id="ac7e0-106">D3DX11CompileFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="ac7e0-106">D3DX11CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="ac7e0-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="ac7e0-108">En lugar de usar esta función, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="ac7e0-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="ac7e0-109">Compilar un sombreador o un efecto que se carga en la memoria.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-109">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac7e0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac7e0-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="ac7e0-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac7e0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac7e0-112">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ac7e0-114">Puntero al sombreador en la memoria.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-114">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-115">*SrcDataLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-115">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-116">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ac7e0-117">Tamaño del sombreador en la memoria.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-117">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-118">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-119">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ac7e0-120">Nombre del archivo que contiene el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-120">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-121">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-122">Tipo: **[**D3D10 de \_ sombreador \_ const**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="ac7e0-122">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="ac7e0-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-123">Optional.</span></span> <span data-ttu-id="ac7e0-124">Puntero a una matriz de definiciones de macro (vea [**D3D10 \_ Shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="ac7e0-124">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="ac7e0-125">La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-125">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="ac7e0-126">Si no se usa, establezca *pDefines* en **null**.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-126">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-127">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-127">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-128">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-128">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="ac7e0-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-129">Optional.</span></span> <span data-ttu-id="ac7e0-130">Puntero a una interfaz para controlar archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-130">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="ac7e0-131">Si se establece en **null** , se producirá un error de compilación si un sombreador contiene un \# include.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-131">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-132">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-132">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-133">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ac7e0-134">Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-134">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="ac7e0-135">Al compilar un efecto, **D3DX11CompileFromMemory** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-135">When you compile an effect, **D3DX11CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-136">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-136">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-137">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-137">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ac7e0-138">Cadena que especifica el modelo de sombreador; puede ser cualquier perfil del modelo de sombreador 2, el modelo de sombreador 3, el modelo de sombreador 4 o el modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-138">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="ac7e0-139">El perfil también puede ser para el tipo de efecto (por ejemplo, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="ac7e0-139">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-140">*Flags1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-140">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-141">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-141">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ac7e0-142">Marcas de [**compilación**](/windows/desktop/direct3dhlsl/d3dcompile-constants)del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-142">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-143">*Flags2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-143">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-144">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-144">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ac7e0-145">[**Marcas de compilación**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)de efectos.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-145">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="ac7e0-146">Al compilar un sombreador y no un archivo de efectos, **D3DX11CompileFromMemory** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-146">When you compile a shader and not an effect file, **D3DX11CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-147">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-147">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-148">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="ac7e0-148">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="ac7e0-149">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="ac7e0-149">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="ac7e0-150">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-150">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-151">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-151">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-152">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ac7e0-152">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ac7e0-153">Puntero a la memoria que contiene el sombreador compilado, así como cualquier información de depuración incrustada y de tabla de símbolos.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-153">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-154">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-154">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-155">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ac7e0-155">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ac7e0-156">Puntero a la memoria que contiene una lista de errores y advertencias que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-156">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="ac7e0-157">Estos errores y advertencias son idénticos a los resultados de depuración de un depurador.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-157">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="ac7e0-158">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac7e0-158">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7e0-159">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="ac7e0-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="ac7e0-160">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-160">A pointer to the return value.</span></span> <span data-ttu-id="ac7e0-161">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-161">May be **NULL**.</span></span> <span data-ttu-id="ac7e0-162">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-162">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac7e0-163">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac7e0-163">Return value</span></span>

<span data-ttu-id="ac7e0-164">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac7e0-165">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ac7e0-165">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="ac7e0-166">**D3DX11CompileFromMemory** devuelve E \_ INVALIDARG si proporciona un valor distinto de **null** al parámetro *pHResult* cuando se proporciona **null** al parámetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="ac7e0-166">**D3DX11CompileFromMemory** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="ac7e0-167">Para obtener más información sobre esta situación, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-167">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac7e0-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac7e0-168">Remarks</span></span>

<span data-ttu-id="ac7e0-169">Para obtener más información sobre **D3DX11CompileFromMemory**, consulte [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="ac7e0-169">For more information about **D3DX11CompileFromMemory**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="ac7e0-170">Debe proporcionar un **valor null** al parámetro *pHResult* si también proporciona **null** al parámetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="ac7e0-170">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="ac7e0-171">De lo contrario, no se puede crear un sombreador posteriormente mediante el código del sombreador compilado que **D3DX11CompileFromMemory** devuelve en la memoria a la que apunta el parámetro *ppShader* .</span><span class="sxs-lookup"><span data-stu-id="ac7e0-171">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromMemory** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="ac7e0-172">Para crear un sombreador a partir del código de sombreador compatible, llame a uno de los siguientes métodos de interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="ac7e0-172">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="ac7e0-173">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-173">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="ac7e0-174">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-174">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="ac7e0-175">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-175">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="ac7e0-176">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-176">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="ac7e0-177">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-177">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="ac7e0-178">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-178">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="ac7e0-179">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="ac7e0-179">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="ac7e0-180">Además, si se proporciona un valor distinto de **null** a *pHResult* cuando se proporciona **null** a *pPump*, **D3DX11CompileFromMemory** devuelve el código de \_ error E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="ac7e0-180">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromMemory** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac7e0-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac7e0-181">Requirements</span></span>



| <span data-ttu-id="ac7e0-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac7e0-182">Requirement</span></span> | <span data-ttu-id="ac7e0-183">Value</span><span class="sxs-lookup"><span data-stu-id="ac7e0-183">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac7e0-184">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac7e0-184">Header</span></span><br/>  | <dl> <span data-ttu-id="ac7e0-185"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac7e0-185"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="ac7e0-186">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac7e0-186">Library</span></span><br/> | <dl> <span data-ttu-id="ac7e0-187"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac7e0-187"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ac7e0-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac7e0-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac7e0-189">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="ac7e0-189">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 


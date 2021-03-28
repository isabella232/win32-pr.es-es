---
title: Función D3DX11CompileFromResource (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar funciones de recursos y, a continuación, compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API de D3DCompile. Compilar un sombreador o un efecto desde un recurso.
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- Función D3DX11CompileFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26eeb825a1d3b6bcda9f77eae24c99c3cec168b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003900"
---
# <a name="d3dx11compilefromresource-function"></a><span data-ttu-id="9527d-106">D3DX11CompileFromResource función)</span><span class="sxs-lookup"><span data-stu-id="9527d-106">D3DX11CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="9527d-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="9527d-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="9527d-108">En lugar de usar esta función, se recomienda usar funciones de [recursos](/windows/desktop/menurc/resources-functions)y, a continuación, compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API de [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="9527d-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="9527d-109">Compilar un sombreador o un efecto desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="9527d-109">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9527d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9527d-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
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



## <a name="parameters"></a><span data-ttu-id="9527d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9527d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9527d-112">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-113">Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9527d-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9527d-114">Identificador del módulo de recursos que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="9527d-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="9527d-115">HMODULE se puede obtener con la [función GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="9527d-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="9527d-116">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9527d-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9527d-118">Nombre del recurso que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="9527d-118">Name of the resource containing the shader.</span></span> <span data-ttu-id="9527d-119">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="9527d-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="9527d-120">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="9527d-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="9527d-121">*pSrcFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-122">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9527d-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9527d-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9527d-123">Optional.</span></span> <span data-ttu-id="9527d-124">Nombre del archivo de efectos, que solo se usa para los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="9527d-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="9527d-125">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="9527d-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9527d-126">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-127">Tipo: **[**D3D10 de \_ sombreador \_ const**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="9527d-127">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="9527d-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9527d-128">Optional.</span></span> <span data-ttu-id="9527d-129">Puntero a una matriz de definiciones de macro (vea [**D3D10 \_ Shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="9527d-129">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="9527d-130">La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0.</span><span class="sxs-lookup"><span data-stu-id="9527d-130">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="9527d-131">Si no se usa, establezca *pDefines* en **null**.</span><span class="sxs-lookup"><span data-stu-id="9527d-131">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9527d-132">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-132">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-133">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9527d-133">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="9527d-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9527d-134">Optional.</span></span> <span data-ttu-id="9527d-135">Puntero a una interfaz para controlar archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="9527d-135">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="9527d-136">Si se establece en **null** , se producirá un error de compilación si un sombreador contiene un \# include.</span><span class="sxs-lookup"><span data-stu-id="9527d-136">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="9527d-137">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-137">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-138">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9527d-138">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9527d-139">Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9527d-139">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="9527d-140">Al compilar un efecto, **D3DX11CompileFromResource** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="9527d-140">When you compile an effect, **D3DX11CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="9527d-141">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-141">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-142">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9527d-142">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9527d-143">Cadena que especifica el modelo de sombreador; puede ser cualquier perfil del modelo de sombreador 2, el modelo de sombreador 3, el modelo de sombreador 4 o el modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="9527d-143">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="9527d-144">El perfil también puede ser para el tipo de efecto (por ejemplo, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="9527d-144">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="9527d-145">*Flags1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-145">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-146">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9527d-146">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9527d-147">Marcas de [**compilación**](/windows/desktop/direct3dhlsl/d3dcompile-constants)del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9527d-147">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="9527d-148">*Flags2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-148">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-149">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9527d-149">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9527d-150">[**Marcas de compilación**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)de efectos.</span><span class="sxs-lookup"><span data-stu-id="9527d-150">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="9527d-151">Al compilar un sombreador y no un archivo de efectos, **D3DX11CompileFromResource** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="9527d-151">When you compile a shader and not an effect file, **D3DX11CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="9527d-152">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9527d-152">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-153">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="9527d-153">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="9527d-154">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="9527d-154">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="9527d-155">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="9527d-155">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="9527d-156">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9527d-156">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-157">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9527d-157">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9527d-158">Puntero a la memoria que contiene el sombreador compilado, así como cualquier información de depuración incrustada y de tabla de símbolos.</span><span class="sxs-lookup"><span data-stu-id="9527d-158">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="9527d-159">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9527d-159">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-160">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9527d-160">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9527d-161">Puntero a la memoria que contiene una lista de errores y advertencias que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="9527d-161">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="9527d-162">Estos errores y advertencias son idénticos a los resultados de depuración de un depurador.</span><span class="sxs-lookup"><span data-stu-id="9527d-162">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="9527d-163">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9527d-163">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9527d-164">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="9527d-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="9527d-165">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="9527d-165">A pointer to the return value.</span></span> <span data-ttu-id="9527d-166">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="9527d-166">May be **NULL**.</span></span> <span data-ttu-id="9527d-167">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9527d-167">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9527d-168">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9527d-168">Return value</span></span>

<span data-ttu-id="9527d-169">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9527d-169">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9527d-170">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9527d-170">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="9527d-171">**D3DX11CompileFromResource** devuelve E \_ INVALIDARG si proporciona un valor distinto de **null** al parámetro *pHResult* cuando se proporciona **null** al parámetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="9527d-171">**D3DX11CompileFromResource** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="9527d-172">Para obtener más información sobre esta situación, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9527d-172">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="9527d-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9527d-173">Remarks</span></span>

<span data-ttu-id="9527d-174">Para obtener más información sobre **D3DX11CompileFromResource**, consulte [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="9527d-174">For more information about **D3DX11CompileFromResource**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="9527d-175">Debe proporcionar un **valor null** al parámetro *pHResult* si también proporciona **null** al parámetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="9527d-175">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="9527d-176">De lo contrario, no se puede crear un sombreador posteriormente mediante el código del sombreador compilado que **D3DX11CompileFromResource** devuelve en la memoria a la que apunta el parámetro *ppShader* .</span><span class="sxs-lookup"><span data-stu-id="9527d-176">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromResource** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="9527d-177">Para crear un sombreador a partir del código de sombreador compatible, llame a uno de los siguientes métodos de interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="9527d-177">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="9527d-178">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="9527d-178">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="9527d-179">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="9527d-179">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="9527d-180">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="9527d-180">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="9527d-181">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="9527d-181">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="9527d-182">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="9527d-182">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="9527d-183">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="9527d-183">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="9527d-184">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="9527d-184">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="9527d-185">Además, si se proporciona un valor distinto de **null** a *pHResult* cuando se proporciona **null** a *pPump*, **D3DX11CompileFromResource** devuelve el código de \_ error E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="9527d-185">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromResource** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9527d-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9527d-186">Requirements</span></span>



| <span data-ttu-id="9527d-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="9527d-187">Requirement</span></span> | <span data-ttu-id="9527d-188">Value</span><span class="sxs-lookup"><span data-stu-id="9527d-188">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9527d-189">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9527d-189">Header</span></span><br/>  | <dl> <span data-ttu-id="9527d-190"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="9527d-190"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="9527d-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9527d-191">Library</span></span><br/> | <dl> <span data-ttu-id="9527d-192"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9527d-192"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9527d-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="9527d-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9527d-194">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="9527d-194">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 


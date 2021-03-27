---
title: Función D3DX11CompileFromFile (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API D3DCompileFromFile. Compilar un sombreador o un efecto desde un archivo.
ms.assetid: 91a1a339-50da-4f86-9b55-6af246a60482
keywords:
- Función D3DX11CompileFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c9194eb54652304c220e5a4de0ee12a26ea1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157220"
---
# <a name="d3dx11compilefromfile-function"></a><span data-ttu-id="2ddb1-106">D3DX11CompileFromFile función)</span><span class="sxs-lookup"><span data-stu-id="2ddb1-106">D3DX11CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="2ddb1-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="2ddb1-108">En lugar de usar esta función, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="2ddb1-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) API.</span></span>

 

<span data-ttu-id="2ddb1-109">Compilar un sombreador o un efecto desde un archivo.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-109">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ddb1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ddb1-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="2ddb1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ddb1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddb1-112">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ddb1-114">Nombre del archivo que contiene el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-114">The name of the file that contains the shader code.</span></span> <span data-ttu-id="2ddb1-115">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2ddb1-116">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-117">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-118">Tipo: **[**D3D10 de \_ sombreador \_ const**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="2ddb1-118">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="2ddb1-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-119">Optional.</span></span> <span data-ttu-id="2ddb1-120">Puntero a una matriz de definiciones de macro (vea [**D3D10 \_ Shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="2ddb1-120">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="2ddb1-121">La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-121">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="2ddb1-122">Si no se usa, establezca *pDefines* en **null**.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-122">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-123">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-124">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-124">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="2ddb1-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-125">Optional.</span></span> <span data-ttu-id="2ddb1-126">Puntero a una interfaz para controlar archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-126">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="2ddb1-127">Si se establece en **null** , se producirá un error de compilación si un sombreador contiene un \# include.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-127">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-128">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-128">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-129">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-129">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ddb1-130">Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-130">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="2ddb1-131">Al compilar un efecto, **D3DX11CompileFromFile** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-131">When you compile an effect, **D3DX11CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-132">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-132">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-133">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ddb1-134">Cadena que especifica el modelo de sombreador; puede ser cualquier perfil del modelo de sombreador 2, el modelo de sombreador 3, el modelo de sombreador 4 o el modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-134">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="2ddb1-135">El perfil también puede ser para el tipo de efecto (por ejemplo, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="2ddb1-135">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-136">*Flags1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-137">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-137">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ddb1-138">Marcas de [**compilación**](/windows/desktop/direct3dhlsl/d3dcompile-constants)del sombreador.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-138">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-139">*Flags2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-140">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-140">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ddb1-141">[**Marcas de compilación**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)de efectos.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-141">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="2ddb1-142">Al compilar un sombreador y no un archivo de efectos, **D3DX11CompileFromFile** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-142">When you compile a shader and not an effect file, **D3DX11CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-143">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-144">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ddb1-144">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="2ddb1-145">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="2ddb1-145">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="2ddb1-146">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-147">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-148">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="2ddb1-148">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="2ddb1-149">Puntero a la memoria que contiene el sombreador compilado, así como cualquier información de depuración incrustada y de tabla de símbolos.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-149">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-150">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-151">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="2ddb1-151">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="2ddb1-152">Puntero a la memoria que contiene una lista de errores y advertencias que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-152">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="2ddb1-153">Estos errores y advertencias son idénticos a los resultados de depuración de un depurador.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="2ddb1-154">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2ddb1-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddb1-155">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="2ddb1-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="2ddb1-156">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-156">A pointer to the return value.</span></span> <span data-ttu-id="2ddb1-157">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-157">May be **NULL**.</span></span> <span data-ttu-id="2ddb1-158">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ddb1-159">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ddb1-159">Return value</span></span>

<span data-ttu-id="2ddb1-160">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ddb1-161">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2ddb1-161">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="2ddb1-162">**D3DX11CompileFromFile** devuelve E \_ INVALIDARG si proporciona un valor distinto de **null** al parámetro *pHResult* cuando se proporciona **null** al parámetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="2ddb1-162">**D3DX11CompileFromFile** returns E\_INVALIDARG if you supply a non-**NULL** value to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="2ddb1-163">Para obtener más información sobre esta situación, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-163">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ddb1-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ddb1-164">Remarks</span></span>

<span data-ttu-id="2ddb1-165">Para obtener más información sobre **D3DX11CompileFromFile**, consulte [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="2ddb1-165">For more information about **D3DX11CompileFromFile**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="2ddb1-166">Debe proporcionar un **valor null** al parámetro *pHResult* si también proporciona **null** al parámetro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="2ddb1-166">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="2ddb1-167">De lo contrario, no se puede crear un sombreador mediante el código del sombreador compilado que **D3DX11CompileFromFile** devuelve en la memoria a la que apunta el parámetro *ppShader* .</span><span class="sxs-lookup"><span data-stu-id="2ddb1-167">Otherwise, you cannot create a shader by using the compiled shader code that **D3DX11CompileFromFile** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="2ddb1-168">Para crear un sombreador a partir del código de sombreador compatible, llame a uno de los siguientes métodos de interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="2ddb1-168">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="2ddb1-169">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-169">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="2ddb1-170">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-170">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="2ddb1-171">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-171">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="2ddb1-172">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-172">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="2ddb1-173">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-173">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="2ddb1-174">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-174">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="2ddb1-175">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="2ddb1-175">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="2ddb1-176">Además, si se proporciona un valor distinto de **null** a *pHResult* cuando se proporciona **null** a *pPump*, **D3DX11CompileFromFile** devuelve el código de \_ error E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="2ddb1-176">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromFile** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddb1-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ddb1-177">Requirements</span></span>



| <span data-ttu-id="2ddb1-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ddb1-178">Requirement</span></span> | <span data-ttu-id="2ddb1-179">Value</span><span class="sxs-lookup"><span data-stu-id="2ddb1-179">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddb1-180">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ddb1-180">Header</span></span><br/>  | <dl> <span data-ttu-id="2ddb1-181"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ddb1-181"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="2ddb1-182">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ddb1-182">Library</span></span><br/> | <dl> <span data-ttu-id="2ddb1-183"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ddb1-183"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2ddb1-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ddb1-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddb1-185">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="2ddb1-185">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 


---
description: Tenga en cuenta que, en lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API D3DCompile. Compilar un sombreador o un efecto desde un archivo.
ms.assetid: b0ca0b6a-3ff0-49ee-83de-14c4686a7104
title: Función D3DX10CompileFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 571f8123a9834c95ecca6043c3495fb18fbaca47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718441"
---
# <a name="d3dx10compilefromfile-function"></a><span data-ttu-id="1928e-104">D3DX10CompileFromFile función)</span><span class="sxs-lookup"><span data-stu-id="1928e-104">D3DX10CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="1928e-105">En lugar de usar esta función heredada, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar la API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="1928e-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="1928e-106">Compilar un sombreador o un efecto desde un archivo.</span><span class="sxs-lookup"><span data-stu-id="1928e-106">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1928e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1928e-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="1928e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1928e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1928e-109">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1928e-109">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-110">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1928e-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1928e-111">Nombre del archivo que contiene el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1928e-111">The name of the file that contains the shader code.</span></span> <span data-ttu-id="1928e-112">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="1928e-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1928e-113">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1928e-113">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="1928e-114">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1928e-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-115">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="1928e-115">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="1928e-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1928e-116">Optional.</span></span> <span data-ttu-id="1928e-117">Puntero a una matriz de definiciones de macro (vea la [**\_ \_ macro del sombreador de D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="1928e-117">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="1928e-118">La última estructura de la matriz actúa como terminador y debe tener todos los miembros establecidos en 0.</span><span class="sxs-lookup"><span data-stu-id="1928e-118">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="1928e-119">Si no se usa, establezca *pDefines* en **null**.</span><span class="sxs-lookup"><span data-stu-id="1928e-119">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1928e-120">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1928e-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-121">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1928e-121">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="1928e-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1928e-122">Optional.</span></span> <span data-ttu-id="1928e-123">Puntero a una interfaz de [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) para administrar archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="1928e-123">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="1928e-124">Si se establece en **null** , se producirá un error de compilación si un sombreador contiene un \# include.</span><span class="sxs-lookup"><span data-stu-id="1928e-124">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="1928e-125">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1928e-125">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-126">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1928e-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1928e-127">Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1928e-127">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="1928e-128">Al compilar un efecto, **D3DX10CompileFromFile** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="1928e-128">When you compile an effect, **D3DX10CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="1928e-129">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1928e-129">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-130">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1928e-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1928e-131">Cadena que especifica el modelo de sombreador; puede ser cualquier perfil en el modelo de sombreador [2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), el [modelo de sombreador 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o el [modelo de sombreador 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="1928e-131">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="1928e-132">*Flags1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1928e-132">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-133">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1928e-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1928e-134">[Marcas de compilación del sombreador](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="1928e-134">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="1928e-135">*Flags2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1928e-135">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-136">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1928e-136">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1928e-137">[Marcas de compilación de efectos](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1928e-137">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="1928e-138">Al compilar un sombreador y no un archivo de efectos, **D3DX10CompileFromFile** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="1928e-138">When you compile a shader and not an effect file, **D3DX10CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="1928e-139">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1928e-139">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-140">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="1928e-140">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="1928e-141">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="1928e-141">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="1928e-142">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="1928e-142">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="1928e-143">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1928e-143">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-144">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1928e-144">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1928e-145">Puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene el sombreador compilado, así como cualquier información de depuración y de tabla de símbolos incrustada.</span><span class="sxs-lookup"><span data-stu-id="1928e-145">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="1928e-146">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1928e-146">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-147">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1928e-147">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1928e-148">Un puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) que contiene una lista de errores y advertencias que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="1928e-148">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="1928e-149">Estos errores y advertencias son idénticos a los resultados de depuración de un depurador.</span><span class="sxs-lookup"><span data-stu-id="1928e-149">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="1928e-150">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1928e-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1928e-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="1928e-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="1928e-152">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1928e-152">A pointer to the return value.</span></span> <span data-ttu-id="1928e-153">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1928e-153">May be **NULL**.</span></span> <span data-ttu-id="1928e-154">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1928e-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1928e-155">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1928e-155">Return value</span></span>

<span data-ttu-id="1928e-156">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1928e-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1928e-157">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1928e-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1928e-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1928e-158">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1928e-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1928e-159">Requirements</span></span>



| <span data-ttu-id="1928e-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="1928e-160">Requirement</span></span> | <span data-ttu-id="1928e-161">Value</span><span class="sxs-lookup"><span data-stu-id="1928e-161">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1928e-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1928e-162">Header</span></span><br/> | <dl> <span data-ttu-id="1928e-163"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="1928e-163"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1928e-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="1928e-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1928e-165">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="1928e-165">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

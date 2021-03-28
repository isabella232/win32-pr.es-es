---
title: Función D3DX11CreateAsyncCompilerProcessor (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un procesador de datos asincrónico para un sombreador.
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- Función D3DX11CreateAsyncCompilerProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533e487e65640b8c17a0ff8d061388e8b5a6c0f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998563"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a><span data-ttu-id="3fef4-106">D3DX11CreateAsyncCompilerProcessor función)</span><span class="sxs-lookup"><span data-stu-id="3fef4-106">D3DX11CreateAsyncCompilerProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="3fef4-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="3fef4-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="3fef4-108">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3fef4-108">See Remarks.</span></span>

 

<span data-ttu-id="3fef4-109">Cree un procesador de datos asincrónico para un sombreador.</span><span class="sxs-lookup"><span data-stu-id="3fef4-109">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fef4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fef4-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="3fef4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fef4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fef4-112">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3fef4-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3fef4-114">Cadena que contiene el nombre de archivo del sombreador.</span><span class="sxs-lookup"><span data-stu-id="3fef4-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="3fef4-115">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-116">Tipo: **D3D11 de \_ sombreador \_ \* const**</span><span class="sxs-lookup"><span data-stu-id="3fef4-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="3fef4-117">Una matriz terminada en NULL de macros de sombreador; Establezca este **valor en NULL** para no especificar ninguna macro.</span><span class="sxs-lookup"><span data-stu-id="3fef4-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="3fef4-118">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-119">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3fef4-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="3fef4-120">Puntero a una interfaz de inclusión.</span><span class="sxs-lookup"><span data-stu-id="3fef4-120">A pointer to an include interface.</span></span> <span data-ttu-id="3fef4-121">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3fef4-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3fef4-122">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-123">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3fef4-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3fef4-124">Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="3fef4-124">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="3fef4-125">Al compilar un efecto, **D3DX11CreateAsyncCompilerProcessor** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="3fef4-125">When you compile an effect, **D3DX11CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it..</span></span>

</dd> <dt>

<span data-ttu-id="3fef4-126">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-127">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3fef4-127">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3fef4-128">Una cadena que especifica el perfil del sombreador o el modelo de sombreador; puede ser cualquier perfil del modelo de sombreador 2, el modelo de sombreador 3, el modelo de sombreador 4 o el modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="3fef4-128">A string that specifies the shader profile or shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="3fef4-129">El perfil también puede ser para el tipo de efecto (por ejemplo, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="3fef4-129">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="3fef4-130">*Flags1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-130">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-131">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3fef4-131">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3fef4-132">Marcas de compilación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="3fef4-132">Shader compile flags.</span></span>

</dd> <dt>

<span data-ttu-id="3fef4-133">*Flags2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-133">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-134">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3fef4-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3fef4-135">Marcas de compilación de efectos.</span><span class="sxs-lookup"><span data-stu-id="3fef4-135">Effect compile flags.</span></span> <span data-ttu-id="3fef4-136">Al compilar un sombreador y no un archivo de efectos, **D3DX11CreateAsyncCompilerProcessor** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro que no es de puntero en cero si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="3fef4-136">When you compile a shader and not an effect file, **D3DX11CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="3fef4-137">*ppCompiledShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-137">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-138">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3fef4-138">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3fef4-139">Dirección de un puntero al efecto compilado.</span><span class="sxs-lookup"><span data-stu-id="3fef4-139">Address of a pointer to the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="3fef4-140">*ppErrorBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-140">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-141">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3fef4-141">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3fef4-142">Dirección de un puntero para compilar errores.</span><span class="sxs-lookup"><span data-stu-id="3fef4-142">Address of a pointer to compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="3fef4-143">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3fef4-143">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fef4-144">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3fef4-144">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="3fef4-145">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="3fef4-145">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fef4-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fef4-146">Return value</span></span>

<span data-ttu-id="3fef4-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3fef4-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3fef4-148">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3fef4-148">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3fef4-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fef4-149">Remarks</span></span>

<span data-ttu-id="3fef4-150">No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="3fef4-150">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="3fef4-151">En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="3fef4-151">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="3fef4-152">En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3fef4-152">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fef4-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fef4-153">Requirements</span></span>



| <span data-ttu-id="3fef4-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fef4-154">Requirement</span></span> | <span data-ttu-id="3fef4-155">Value</span><span class="sxs-lookup"><span data-stu-id="3fef4-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fef4-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fef4-156">Header</span></span><br/>  | <dl> <span data-ttu-id="3fef4-157"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fef4-157"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="3fef4-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fef4-158">Library</span></span><br/> | <dl> <span data-ttu-id="3fef4-159"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fef4-159"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3fef4-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fef4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fef4-161">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="3fef4-161">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 


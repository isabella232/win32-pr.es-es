---
description: Cree un procesador de datos asincrónico para un sombreador.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: Función D3DX10CreateAsyncCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fa6a558efd56917832da3280df2aad4ac400def
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280281"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a><span data-ttu-id="77933-103">D3DX10CreateAsyncCompilerProcessor función)</span><span class="sxs-lookup"><span data-stu-id="77933-103">D3DX10CreateAsyncCompilerProcessor function</span></span>

<span data-ttu-id="77933-104">Cree un procesador de datos asincrónico para un sombreador.</span><span class="sxs-lookup"><span data-stu-id="77933-104">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="77933-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77933-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="77933-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77933-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77933-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77933-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77933-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77933-109">Cadena que contiene el nombre de archivo del sombreador.</span><span class="sxs-lookup"><span data-stu-id="77933-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="77933-110">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77933-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-111">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="77933-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="77933-112">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="77933-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="77933-113">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77933-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="77933-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="77933-115">Un puntero a una interfaz de inclusión (consulte la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="77933-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="77933-116">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="77933-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="77933-117">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77933-117">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77933-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77933-119">Nombre de la función del punto de entrada del sombreador en el que comienza la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="77933-119">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="77933-120">Al compilar un efecto, **D3DX10CreateAsyncCompilerProcessor** omite *pFunctionName*; se recomienda establecer *pFunctionName* en **null** porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="77933-120">When you compile an effect, **D3DX10CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="77933-121">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77933-121">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-122">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77933-122">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77933-123">Una cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) o el modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="77933-123">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="77933-124">*Flags1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77933-124">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77933-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77933-126">[Marcas de compilación del sombreador](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="77933-126">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="77933-127">*Flags2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77933-127">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77933-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77933-129">[Marcas de compilación de efectos](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="77933-129">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="77933-130">Al compilar un sombreador y no un archivo de efectos, **D3DX10CreateAsyncCompilerProcessor** omite *Flags2*; se recomienda establecer *Flags2* en cero porque es una buena práctica de programación establecer un parámetro de puntero en **null** si la función llamada no lo va a usar.</span><span class="sxs-lookup"><span data-stu-id="77933-130">When you compile a shader and not an effect file, **D3DX10CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="77933-131">*ppCompiledShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="77933-131">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-132">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="77933-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="77933-133">Dirección de un puntero al efecto compilado (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="77933-133">Address of a pointer to the compiled effect (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="77933-134">*ppErrorBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="77933-134">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-135">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="77933-135">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="77933-136">Dirección de un puntero para compilar errores (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="77933-136">Address of a pointer to compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="77933-137">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="77933-137">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77933-138">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="77933-138">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="77933-139">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="77933-139">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77933-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77933-140">Return value</span></span>

<span data-ttu-id="77933-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77933-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77933-142">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="77933-142">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77933-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77933-143">Requirements</span></span>



| <span data-ttu-id="77933-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="77933-144">Requirement</span></span> | <span data-ttu-id="77933-145">Value</span><span class="sxs-lookup"><span data-stu-id="77933-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="77933-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77933-146">Header</span></span><br/> | <dl> <span data-ttu-id="77933-147"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="77933-147"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77933-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="77933-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77933-149">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="77933-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

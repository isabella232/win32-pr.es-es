---
description: Compilar un sombreador y crear un procesador de datos de forma asincrónica.
ms.assetid: 842db48b-51a7-4f32-8ea6-44247f2619b0
title: Función D3DX10CreateAsyncShaderCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 2a1cd663827cc32b868c9c6c9b74fbc3c21b8ee6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424363"
---
# <a name="d3dx10createasyncshadercompilerprocessor-function"></a><span data-ttu-id="0b0ae-103">D3DX10CreateAsyncShaderCompilerProcessor función)</span><span class="sxs-lookup"><span data-stu-id="0b0ae-103">D3DX10CreateAsyncShaderCompilerProcessor function</span></span>

<span data-ttu-id="0b0ae-104">Compilar un sombreador y crear un procesador de datos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="0b0ae-104">Compile a shader and create a data processor asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b0ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b0ae-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="0b0ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b0ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b0ae-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b0ae-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0ae-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b0ae-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b0ae-109">Cadena que contiene el nombre de archivo del sombreador.</span><span class="sxs-lookup"><span data-stu-id="0b0ae-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="0b0ae-110">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b0ae-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0ae-111">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="0b0ae-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="0b0ae-112">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="0b0ae-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="0b0ae-113">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b0ae-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0ae-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0b0ae-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="0b0ae-115">Un puntero a una interfaz de inclusión (vea la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="0b0ae-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="0b0ae-116">*pFunctionName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b0ae-116">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0ae-117">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b0ae-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b0ae-118">Nombre de la función de punto de entrada para el sombreador.</span><span class="sxs-lookup"><span data-stu-id="0b0ae-118">Name of the entry point function for the shader.</span></span>

</dd> <dt>

<span data-ttu-id="0b0ae-119">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b0ae-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0ae-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b0ae-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b0ae-121">Una cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) o el modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0b0ae-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="0b0ae-122">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0b0ae-122">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0ae-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b0ae-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b0ae-124">Opciones de compilación de HLSL (consulte [marcas de sombreador](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="0b0ae-124">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0b0ae-125">*ppCompiledShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0b0ae-125">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0ae-126">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="0b0ae-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="0b0ae-127">Dirección de un puntero al sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="0b0ae-127">Address of a pointer to the compiled shader.</span></span> <span data-ttu-id="0b0ae-128">Consulte la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="0b0ae-128">See [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="0b0ae-129">*ppErrorBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0b0ae-129">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0ae-130">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="0b0ae-130">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="0b0ae-131">Dirección de un puntero a un búfer que contiene errores de compilación (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="0b0ae-131">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="0b0ae-132">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0b0ae-132">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0ae-133">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0b0ae-133">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="0b0ae-134">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="0b0ae-134">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b0ae-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b0ae-135">Return value</span></span>

<span data-ttu-id="0b0ae-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b0ae-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b0ae-137">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0b0ae-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b0ae-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b0ae-138">Requirements</span></span>



| <span data-ttu-id="0b0ae-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b0ae-139">Requirement</span></span> | <span data-ttu-id="0b0ae-140">Value</span><span class="sxs-lookup"><span data-stu-id="0b0ae-140">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0ae-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b0ae-141">Header</span></span><br/> | <dl> <span data-ttu-id="0b0ae-142"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b0ae-142"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b0ae-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b0ae-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b0ae-144">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="0b0ae-144">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

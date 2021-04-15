---
description: Cree un procesador de datos para un sombreador de forma asincrónica.
ms.assetid: f5521e55-5f20-422d-979e-98b70efd3b13
title: Función D3DX10CreateAsyncShaderPreprocessProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderPreprocessProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 14afdb899d99b7c0278d3042fbc9a108f446c692
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708023"
---
# <a name="d3dx10createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="ab17f-103">D3DX10CreateAsyncShaderPreprocessProcessor función)</span><span class="sxs-lookup"><span data-stu-id="ab17f-103">D3DX10CreateAsyncShaderPreprocessProcessor function</span></span>

<span data-ttu-id="ab17f-104">Cree un procesador de datos para un sombreador de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ab17f-104">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab17f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab17f-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="ab17f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab17f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab17f-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab17f-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab17f-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab17f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab17f-109">Cadena que contiene el nombre de archivo del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ab17f-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="ab17f-110">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab17f-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab17f-111">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="ab17f-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="ab17f-112">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="ab17f-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="ab17f-113">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab17f-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab17f-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ab17f-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="ab17f-115">Un puntero a una interfaz de inclusión (vea la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="ab17f-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="ab17f-116">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab17f-116">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab17f-117">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ab17f-117">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ab17f-118">Dirección de un puntero a un búfer que contiene el texto ASCII del sombreador (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="ab17f-118">Address of a pointer to a buffer that contains the ASCII text of the shader (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="ab17f-119">*ppErrorBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab17f-119">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab17f-120">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ab17f-120">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ab17f-121">Dirección de un puntero a un búfer que contiene errores de compilación (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="ab17f-121">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="ab17f-122">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab17f-122">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab17f-123">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ab17f-123">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="ab17f-124">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="ab17f-124">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab17f-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab17f-125">Return value</span></span>

<span data-ttu-id="ab17f-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab17f-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab17f-127">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ab17f-127">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab17f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab17f-128">Requirements</span></span>



| <span data-ttu-id="ab17f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab17f-129">Requirement</span></span> | <span data-ttu-id="ab17f-130">Value</span><span class="sxs-lookup"><span data-stu-id="ab17f-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab17f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab17f-131">Header</span></span><br/> | <dl> <span data-ttu-id="ab17f-132"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab17f-132"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab17f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab17f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab17f-134">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="ab17f-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

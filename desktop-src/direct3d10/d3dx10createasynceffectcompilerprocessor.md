---
description: Cree un procesador de datos asincrónicos para un efecto.
ms.assetid: 90a0dcd1-e495-4068-9f28-e2645370b984
title: Función D3DX10CreateAsyncEffectCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 9e1e5716228537d505adc4f48179ec7027b57198
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718280"
---
# <a name="d3dx10createasynceffectcompilerprocessor-function"></a><span data-ttu-id="3343e-103">D3DX10CreateAsyncEffectCompilerProcessor función)</span><span class="sxs-lookup"><span data-stu-id="3343e-103">D3DX10CreateAsyncEffectCompilerProcessor function</span></span>

<span data-ttu-id="3343e-104">Cree un procesador de datos asincrónicos para un efecto.</span><span class="sxs-lookup"><span data-stu-id="3343e-104">Create an asynchronous-data processor for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="3343e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3343e-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="3343e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3343e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3343e-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3343e-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3343e-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3343e-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3343e-109">Cadena que contiene el nombre de archivo del efecto.</span><span class="sxs-lookup"><span data-stu-id="3343e-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="3343e-110">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3343e-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3343e-111">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="3343e-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="3343e-112">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="3343e-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="3343e-113">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3343e-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3343e-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3343e-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="3343e-115">Un puntero a una interfaz de inclusión (consulte la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="3343e-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="3343e-116">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3343e-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3343e-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3343e-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3343e-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3343e-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3343e-119">[Opciones de compilación de HLSL](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3343e-119">[HLSL compile options](d3d10-graphics-reference-effect-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3343e-120">*FXFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3343e-120">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3343e-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3343e-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3343e-122">[Opciones de compilación de efectos](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="3343e-122">[Effect compile options](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="3343e-123">*ppCompiledShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3343e-123">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3343e-124">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3343e-124">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3343e-125">Dirección de un puntero a búfer (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene el efecto compilado.</span><span class="sxs-lookup"><span data-stu-id="3343e-125">Address of a pointer to buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="3343e-126">*ppErrorBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3343e-126">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3343e-127">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3343e-127">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3343e-128">Dirección de un puntero a un búfer (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="3343e-128">Address of a pointer to a buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="3343e-129">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3343e-129">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3343e-130">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3343e-130">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="3343e-131">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="3343e-131">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3343e-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3343e-132">Return value</span></span>

<span data-ttu-id="3343e-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3343e-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3343e-134">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3343e-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3343e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3343e-135">Requirements</span></span>



| <span data-ttu-id="3343e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3343e-136">Requirement</span></span> | <span data-ttu-id="3343e-137">Value</span><span class="sxs-lookup"><span data-stu-id="3343e-137">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3343e-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3343e-138">Header</span></span><br/> | <dl> <span data-ttu-id="3343e-139"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="3343e-139"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3343e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3343e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3343e-141">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="3343e-141">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

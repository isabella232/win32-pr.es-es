---
description: Cree un procesador de datos asincrónico para un bloque de memoria.
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: Función D3DX10CreateAsyncEffectPoolCreateProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280378"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a><span data-ttu-id="1f510-103">D3DX10CreateAsyncEffectPoolCreateProcessor función)</span><span class="sxs-lookup"><span data-stu-id="1f510-103">D3DX10CreateAsyncEffectPoolCreateProcessor function</span></span>

<span data-ttu-id="1f510-104">Cree un procesador de datos asincrónico para un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="1f510-104">Create an asynchronous-data processor for a memory pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f510-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f510-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="1f510-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f510-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f510-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f510-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f510-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f510-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f510-109">Cadena que contiene el nombre de archivo del efecto.</span><span class="sxs-lookup"><span data-stu-id="1f510-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="1f510-110">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f510-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f510-111">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="1f510-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="1f510-112">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="1f510-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="1f510-113">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f510-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f510-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1f510-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="1f510-115">Un puntero a una interfaz de inclusión (vea la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="1f510-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="1f510-116">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f510-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f510-117">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f510-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f510-118">Una cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) o el modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1f510-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="1f510-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1f510-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f510-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f510-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f510-121">Opciones de compilación de HLSL (consulte [marcas de sombreador](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="1f510-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1f510-122">*FXFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f510-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f510-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f510-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f510-124">Opciones de compilación de efectos (vea [marcas de compilación y efectos](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="1f510-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1f510-125">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f510-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f510-126">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="1f510-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="1f510-127">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará los recursos.</span><span class="sxs-lookup"><span data-stu-id="1f510-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="1f510-128">*ppErrorBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1f510-128">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f510-129">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1f510-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1f510-130">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de compilación del efecto, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="1f510-130">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="1f510-131">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1f510-131">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f510-132">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1f510-132">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="1f510-133">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="1f510-133">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f510-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f510-134">Return value</span></span>

<span data-ttu-id="1f510-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f510-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f510-136">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1f510-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f510-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f510-137">Requirements</span></span>



| <span data-ttu-id="1f510-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f510-138">Requirement</span></span> | <span data-ttu-id="1f510-139">Value</span><span class="sxs-lookup"><span data-stu-id="1f510-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f510-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f510-140">Header</span></span><br/> | <dl> <span data-ttu-id="1f510-141"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f510-141"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f510-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f510-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f510-143">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="1f510-143">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

---
description: Cree un grupo de efectos de forma asincrónica.
ms.assetid: 50c55751-26de-4002-9a89-8e5ab59dda79
title: Función D3DX10CreateAsyncEffectCreateProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 573efc51214031afe66f6cfd552bbda634d15142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717680"
---
# <a name="d3dx10createasynceffectcreateprocessor-function"></a><span data-ttu-id="84152-103">D3DX10CreateAsyncEffectCreateProcessor función)</span><span class="sxs-lookup"><span data-stu-id="84152-103">D3DX10CreateAsyncEffectCreateProcessor function</span></span>

<span data-ttu-id="84152-104">Cree un grupo de efectos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="84152-104">Create an effect pool asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="84152-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84152-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _In_        ID3D10EffectPool     *pPool,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="84152-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84152-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84152-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84152-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84152-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84152-109">Cadena que contiene el nombre de archivo del efecto.</span><span class="sxs-lookup"><span data-stu-id="84152-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="84152-110">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84152-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-111">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="84152-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="84152-112">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="84152-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="84152-113">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84152-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="84152-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="84152-115">Un puntero a una interfaz de inclusión (vea la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="84152-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="84152-116">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84152-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-117">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84152-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84152-118">Una cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md) o el modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="84152-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="84152-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="84152-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84152-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84152-121">Opciones de compilación de HLSL (consulte [marcas de sombreador](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="84152-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="84152-122">*FXFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84152-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84152-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84152-124">Opciones de compilación de efectos (vea [marcas de compilación y efectos](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="84152-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="84152-125">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84152-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-126">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="84152-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="84152-127">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará los recursos.</span><span class="sxs-lookup"><span data-stu-id="84152-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="84152-128">*pPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84152-128">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-129">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="84152-129">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="84152-130">Un puntero a un grupo de efectos (vea la [**interfaz ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) para compartir variables entre efectos.</span><span class="sxs-lookup"><span data-stu-id="84152-130">A pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="84152-131">*ppErrorBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="84152-131">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-132">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="84152-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="84152-133">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de compilación del efecto, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="84152-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="84152-134">*ppProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="84152-134">*ppProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84152-135">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="84152-135">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="84152-136">La dirección de un puntero al procesador de datos asincrónicos (consulte la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="84152-136">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84152-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84152-137">Return value</span></span>

<span data-ttu-id="84152-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84152-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84152-139">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="84152-139">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84152-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84152-140">Requirements</span></span>



| <span data-ttu-id="84152-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="84152-141">Requirement</span></span> | <span data-ttu-id="84152-142">Value</span><span class="sxs-lookup"><span data-stu-id="84152-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84152-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84152-143">Header</span></span><br/> | <dl> <span data-ttu-id="84152-144"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="84152-144"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84152-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="84152-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84152-146">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="84152-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

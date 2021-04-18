---
description: Cree un grupo de efectos a partir de un efecto en la memoria.
ms.assetid: 634bcb23-a73f-4493-b805-e2aa5420fa2a
title: Función D3DX10CreateEffectPoolFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 7dc93b7e73f336e75432debfe9bde6659ea4707c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721448"
---
# <a name="d3dx10createeffectpoolfrommemory-function"></a><span data-ttu-id="c5819-103">D3DX10CreateEffectPoolFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="c5819-103">D3DX10CreateEffectPoolFromMemory function</span></span>

<span data-ttu-id="c5819-104">Cree un grupo de efectos a partir de un efecto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="c5819-104">Create an effect pool from an effect in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5819-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5819-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="c5819-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5819-107">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5819-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5819-109">Puntero al efecto.</span><span class="sxs-lookup"><span data-stu-id="c5819-109">A pointer to the effect.</span></span>

</dd> <dt>

<span data-ttu-id="c5819-110">*DATALENGTH* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-111">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5819-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5819-112">Tamaño del efecto.</span><span class="sxs-lookup"><span data-stu-id="c5819-112">The size of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="c5819-113">*pSrcFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-114">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5819-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5819-115">Nombre del archivo de efectos.</span><span class="sxs-lookup"><span data-stu-id="c5819-115">The name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="c5819-116">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-117">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="c5819-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="c5819-118">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="c5819-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="c5819-119">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-120">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="c5819-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="c5819-121">Un puntero a una interfaz de inclusión (consulte la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="c5819-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="c5819-122">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c5819-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c5819-123">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-124">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5819-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5819-125">Cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)o el modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c5819-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="c5819-126">*HLSLFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5819-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5819-128">Opciones de compilación de HLSL (vea [D3D10 ( \_ constantes del sombreador](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="c5819-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c5819-129">*FXFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5819-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5819-131">Opciones de compilación de efectos (vea [marcas de compilación y efectos](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="c5819-131">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c5819-132">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-133">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="c5819-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="c5819-134">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará los recursos.</span><span class="sxs-lookup"><span data-stu-id="c5819-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="c5819-135">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5819-135">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-136">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5819-136">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="c5819-137">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="c5819-137">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="c5819-138">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="c5819-138">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="c5819-139">*ppEffectPool* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c5819-139">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-140">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="c5819-140">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="c5819-141">Dirección de un puntero al grupo de efectos (vea la [**interfaz ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="c5819-141">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="c5819-142">*ppErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c5819-142">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-143">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c5819-143">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c5819-144">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de compilación del efecto, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="c5819-144">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="c5819-145">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c5819-145">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5819-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c5819-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c5819-147">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c5819-147">A pointer to the return value.</span></span> <span data-ttu-id="c5819-148">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c5819-148">May be **NULL**.</span></span> <span data-ttu-id="c5819-149">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c5819-149">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5819-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5819-150">Return value</span></span>

<span data-ttu-id="c5819-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5819-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5819-152">Devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c5819-152">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5819-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5819-153">Requirements</span></span>



| <span data-ttu-id="c5819-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5819-154">Requirement</span></span> | <span data-ttu-id="c5819-155">Value</span><span class="sxs-lookup"><span data-stu-id="c5819-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5819-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5819-156">Header</span></span><br/> | <dl> <span data-ttu-id="c5819-157"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5819-157"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5819-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5819-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5819-159">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="c5819-159">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

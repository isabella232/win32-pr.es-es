---
description: Cree un grupo de efectos a partir de un recurso.
ms.assetid: 594ab788-fd96-4ea9-ad93-ef02fefa5d61
title: Función D3DX10CreateEffectPoolFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fccc9c399a4573440318b92d1157738589da8a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721447"
---
# <a name="d3dx10createeffectpoolfromresource-function"></a><span data-ttu-id="a0f3f-103">D3DX10CreateEffectPoolFromResource función)</span><span class="sxs-lookup"><span data-stu-id="a0f3f-103">D3DX10CreateEffectPoolFromResource function</span></span>

<span data-ttu-id="a0f3f-104">Cree un grupo de efectos a partir de un recurso.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-104">Create an effect pool from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f3f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0f3f-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _In_        ID3D10EffectPool   **ppEffectPool,
  _In_        ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="a0f3f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0f3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f3f-107">*hModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f3f-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f3f-109">Identificador del módulo de recursos que contiene el efecto.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="a0f3f-110">HMODULE se puede obtener con la [función GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="a0f3f-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-111">*pResourceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f3f-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f3f-113">Nombre del recurso en hModule.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-113">The name of the resource in hModule.</span></span> <span data-ttu-id="a0f3f-114">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a0f3f-115">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-116">*pSrcFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-117">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f3f-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f3f-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-118">Optional.</span></span> <span data-ttu-id="a0f3f-119">Nombre del archivo de efectos, que solo se usa para los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="a0f3f-120">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-121">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-122">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="a0f3f-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="a0f3f-123">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-124">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-125">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="a0f3f-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="a0f3f-126">Un puntero a una interfaz de inclusión (consulte la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="a0f3f-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="a0f3f-127">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-128">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-129">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f3f-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f3f-130">Cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)o el modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-131">*HLSLFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f3f-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f3f-133">Opciones de compilación de HLSL (vea [D3D10 ( \_ constantes del sombreador](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="a0f3f-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-134">*FXFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f3f-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f3f-136">Opciones de compilación de efectos (vea [marcas de compilación y efectos](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="a0f3f-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-137">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-138">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="a0f3f-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="a0f3f-139">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará los recursos.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-140">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-140">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-141">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0f3f-141">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="a0f3f-142">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="a0f3f-142">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="a0f3f-143">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-143">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-144">*ppEffectPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-144">*ppEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-145">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="a0f3f-145">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="a0f3f-146">Dirección de un puntero al grupo de efectos (vea la [**interfaz ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="a0f3f-146">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-147">*ppErrors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-147">*ppErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-148">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a0f3f-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a0f3f-149">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de compilación del efecto, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-149">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="a0f3f-150">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a0f3f-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3f-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a0f3f-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a0f3f-152">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-152">A pointer to the return value.</span></span> <span data-ttu-id="a0f3f-153">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-153">May be **NULL**.</span></span> <span data-ttu-id="a0f3f-154">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a0f3f-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f3f-155">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0f3f-155">Return value</span></span>

<span data-ttu-id="a0f3f-156">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0f3f-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0f3f-157">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a0f3f-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f3f-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0f3f-158">Requirements</span></span>



| <span data-ttu-id="a0f3f-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f3f-159">Requirement</span></span> | <span data-ttu-id="a0f3f-160">Value</span><span class="sxs-lookup"><span data-stu-id="a0f3f-160">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f3f-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0f3f-161">Header</span></span><br/> | <dl> <span data-ttu-id="a0f3f-162"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f3f-162"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f3f-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0f3f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f3f-164">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="a0f3f-164">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

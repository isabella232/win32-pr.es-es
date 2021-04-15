---
description: Cree un efecto a partir de la memoria.
ms.assetid: 6903a695-bb87-45fe-9913-25beeaf17233
title: Función D3DX10CreateEffectFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 03cbbc70e633f8289f99e094602cb1a912b711c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707945"
---
# <a name="d3dx10createeffectfrommemory-function"></a><span data-ttu-id="8e1ec-103">D3DX10CreateEffectFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="8e1ec-103">D3DX10CreateEffectFromMemory function</span></span>

<span data-ttu-id="8e1ec-104">Cree un efecto a partir de la memoria.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-104">Create an effect from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1ec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e1ec-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="8e1ec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e1ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e1ec-107">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e1ec-109">Puntero al efecto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-109">Pointer to the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-110">*DATALENGTH* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-111">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e1ec-112">Tamaño del efecto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-112">Size of the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-113">*pSrcFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-114">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e1ec-115">Nombre del archivo de efectos en la memoria.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-115">Name of the effect file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-116">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-117">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="8e1ec-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="8e1ec-118">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-119">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-120">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="8e1ec-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="8e1ec-121">Un puntero a una interfaz de inclusión (consulte la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="8e1ec-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="8e1ec-122">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-123">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-124">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e1ec-125">Cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)o el modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-126">*HLSLFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e1ec-128">Opciones de compilación de HLSL (vea [D3D10 ( \_ constantes del sombreador](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="8e1ec-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-129">*FXFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e1ec-131">Opciones de compilación de efectos (vea [ \_ constantes Effect D3D10](d3d10-effect.md)).</span><span class="sxs-lookup"><span data-stu-id="8e1ec-131">Effect compile options (see [D3D10\_EFFECT Constants](d3d10-effect.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-132">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-133">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="8e1ec-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="8e1ec-134">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará los recursos.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-135">*pEffectPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-135">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-136">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="8e1ec-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="8e1ec-137">Puntero a un grupo de efectos (vea la [**interfaz ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) para compartir variables entre efectos.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-137">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-138">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-138">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-139">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e1ec-139">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="8e1ec-140">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="8e1ec-140">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="8e1ec-141">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-141">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-142">*ppEffect* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-143">Tipo: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="8e1ec-143">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="8e1ec-144">Dirección de un puntero al efecto (vea la [**interfaz ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) que se crea.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-144">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-145">*ppErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-145">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-146">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="8e1ec-146">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="8e1ec-147">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de compilación del efecto, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-147">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-148">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-148">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-149">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="8e1ec-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="8e1ec-150">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-150">A pointer to the return value.</span></span> <span data-ttu-id="8e1ec-151">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-151">May be **NULL**.</span></span> <span data-ttu-id="8e1ec-152">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-152">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e1ec-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e1ec-153">Return value</span></span>

<span data-ttu-id="8e1ec-154">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e1ec-155">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8e1ec-155">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1ec-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e1ec-156">Requirements</span></span>



| <span data-ttu-id="8e1ec-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e1ec-157">Requirement</span></span> | <span data-ttu-id="8e1ec-158">Value</span><span class="sxs-lookup"><span data-stu-id="8e1ec-158">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1ec-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e1ec-159">Header</span></span><br/> | <dl> <span data-ttu-id="8e1ec-160"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e1ec-160"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1ec-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e1ec-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1ec-162">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="8e1ec-162">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

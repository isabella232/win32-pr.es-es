---
description: Cree un efecto a partir de un archivo.
ms.assetid: 1418857e-bda1-4ffb-bbb9-dfa3709313b1
title: Función D3DX10CreateEffectFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 60bc52e5b149a2fa69cc4a16f12900b12ab81db8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718425"
---
# <a name="d3dx10createeffectfromfile-function"></a><span data-ttu-id="91215-103">D3DX10CreateEffectFromFile función)</span><span class="sxs-lookup"><span data-stu-id="91215-103">D3DX10CreateEffectFromFile function</span></span>

<span data-ttu-id="91215-104">Cree un efecto a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="91215-104">Create an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="91215-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91215-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromFile(
  _In_        LPCTSTR            pFileName,
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



## <a name="parameters"></a><span data-ttu-id="91215-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91215-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91215-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91215-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91215-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91215-109">Nombre del archivo de efectos ASCII.</span><span class="sxs-lookup"><span data-stu-id="91215-109">Name of the ASCII effect file.</span></span> <span data-ttu-id="91215-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="91215-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="91215-111">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="91215-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="91215-112">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91215-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-113">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="91215-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="91215-114">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="91215-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="91215-115">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91215-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-116">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="91215-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="91215-117">Un puntero a una interfaz de inclusión (consulte la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="91215-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="91215-118">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="91215-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="91215-119">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91215-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91215-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91215-121">Cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)o el modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="91215-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="91215-122">*HLSLFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91215-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91215-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91215-124">Opciones de compilación de HLSL (vea [D3D10 ( \_ constantes del sombreador](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="91215-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="91215-125">*FXFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91215-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91215-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91215-127">Opciones de compilación de efectos (vea [marcas de compilación y efectos](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="91215-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="91215-128">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91215-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-129">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="91215-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="91215-130">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará los recursos.</span><span class="sxs-lookup"><span data-stu-id="91215-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="91215-131">*pEffectPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91215-131">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-132">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="91215-132">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="91215-133">Puntero a un grupo de efectos (vea la [**interfaz ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) para compartir variables entre efectos.</span><span class="sxs-lookup"><span data-stu-id="91215-133">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="91215-134">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91215-134">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-135">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="91215-135">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="91215-136">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="91215-136">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="91215-137">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="91215-137">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="91215-138">*ppEffect* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="91215-138">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-139">Tipo: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="91215-139">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="91215-140">Dirección de un puntero al efecto (vea la [**interfaz ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) que se crea.</span><span class="sxs-lookup"><span data-stu-id="91215-140">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="91215-141">*ppErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="91215-141">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-142">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="91215-142">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="91215-143">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de compilación del efecto, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="91215-143">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="91215-144">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="91215-144">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91215-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="91215-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="91215-146">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="91215-146">A pointer to the return value.</span></span> <span data-ttu-id="91215-147">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="91215-147">May be **NULL**.</span></span> <span data-ttu-id="91215-148">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="91215-148">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91215-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91215-149">Return value</span></span>

<span data-ttu-id="91215-150">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91215-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91215-151">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="91215-151">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91215-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91215-152">Requirements</span></span>



| <span data-ttu-id="91215-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="91215-153">Requirement</span></span> | <span data-ttu-id="91215-154">Value</span><span class="sxs-lookup"><span data-stu-id="91215-154">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91215-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91215-155">Header</span></span><br/> | <dl> <span data-ttu-id="91215-156"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="91215-156"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91215-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="91215-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91215-158">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="91215-158">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

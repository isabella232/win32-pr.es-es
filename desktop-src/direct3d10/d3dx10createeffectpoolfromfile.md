---
description: Cree un grupo de efectos a partir de un archivo de efectos.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: Función D3DX10CreateEffectPoolFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 418ea287b9bbf2021f3b2e5379b209cf87745a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721449"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a><span data-ttu-id="99c19-103">D3DX10CreateEffectPoolFromFile función)</span><span class="sxs-lookup"><span data-stu-id="99c19-103">D3DX10CreateEffectPoolFromFile function</span></span>

<span data-ttu-id="99c19-104">Cree un grupo de efectos a partir de un archivo de efectos.</span><span class="sxs-lookup"><span data-stu-id="99c19-104">Create an effect pool from an effect file.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c19-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99c19-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
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



## <a name="parameters"></a><span data-ttu-id="99c19-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99c19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c19-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c19-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99c19-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99c19-109">El nombre de archivo del efecto.</span><span class="sxs-lookup"><span data-stu-id="99c19-109">The effect filename.</span></span> <span data-ttu-id="99c19-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="99c19-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="99c19-111">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="99c19-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="99c19-112">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c19-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-113">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="99c19-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="99c19-114">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="99c19-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="99c19-115">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c19-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-116">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="99c19-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="99c19-117">Un puntero a una interfaz de inclusión (consulte la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="99c19-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="99c19-118">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="99c19-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="99c19-119">*pProfile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c19-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99c19-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99c19-121">Cadena que especifica el [Perfil del sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)o el modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="99c19-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="99c19-122">*HLSLFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c19-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99c19-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99c19-124">Opciones de compilación de HLSL (vea [D3D10 ( \_ constantes del sombreador](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="99c19-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="99c19-125">*FXFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c19-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99c19-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99c19-127">Opciones de compilación de efectos (vea [marcas de compilación y efectos](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="99c19-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="99c19-128">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c19-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-129">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="99c19-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="99c19-130">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará los recursos.</span><span class="sxs-lookup"><span data-stu-id="99c19-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="99c19-131">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c19-131">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-132">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="99c19-132">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="99c19-133">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="99c19-133">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="99c19-134">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="99c19-134">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="99c19-135">*ppEffectPool* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="99c19-135">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-136">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="99c19-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="99c19-137">Dirección de un puntero al grupo de efectos (vea la [**interfaz ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="99c19-137">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="99c19-138">*ppErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="99c19-138">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-139">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="99c19-139">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="99c19-140">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de compilación del efecto, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="99c19-140">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="99c19-141">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="99c19-141">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99c19-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="99c19-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="99c19-143">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="99c19-143">A pointer to the return value.</span></span> <span data-ttu-id="99c19-144">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="99c19-144">May be **NULL**.</span></span> <span data-ttu-id="99c19-145">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="99c19-145">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c19-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99c19-146">Return value</span></span>

<span data-ttu-id="99c19-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99c19-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99c19-148">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="99c19-148">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="99c19-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99c19-149">Remarks</span></span>

<span data-ttu-id="99c19-150">En este ejemplo se crea un grupo de efectos a partir del efecto utilizado en el [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="99c19-150">This example creates an effect pool from the effect used in the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a><span data-ttu-id="99c19-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99c19-151">Requirements</span></span>



| <span data-ttu-id="99c19-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="99c19-152">Requirement</span></span> | <span data-ttu-id="99c19-153">Value</span><span class="sxs-lookup"><span data-stu-id="99c19-153">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c19-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99c19-154">Header</span></span><br/> | <dl> <span data-ttu-id="99c19-155"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="99c19-155"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99c19-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="99c19-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c19-157">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="99c19-157">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

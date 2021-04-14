---
description: Tenga en cuenta que, en lugar de usar esta función heredada, se recomienda usar la API de D3DPreprocess. Cree un sombreador a partir de un recurso sin compilarlo.
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: Función D3DX10PreprocessShaderFromResource (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 81a9f272cb0769d4313a4375f98bdc25b9e403e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424539"
---
# <a name="d3dx10preprocessshaderfromresource-function"></a><span data-ttu-id="32be9-104">D3DX10PreprocessShaderFromResource función)</span><span class="sxs-lookup"><span data-stu-id="32be9-104">D3DX10PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="32be9-105">En lugar de usar esta función heredada, se recomienda usar la API de [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="32be9-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="32be9-106">Cree un sombreador a partir de un recurso sin compilarlo.</span><span class="sxs-lookup"><span data-stu-id="32be9-106">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="32be9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32be9-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="32be9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32be9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32be9-109">*hModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32be9-109">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32be9-110">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32be9-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32be9-111">Identificador del módulo de recursos que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="32be9-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="32be9-112">HMODULE se puede obtener con la [función GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="32be9-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="32be9-113">*pResourceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32be9-113">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32be9-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32be9-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32be9-115">Nombre del recurso en el servidor hModule que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="32be9-115">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="32be9-116">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="32be9-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="32be9-117">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="32be9-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="32be9-118">*pSrcFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32be9-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32be9-119">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32be9-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32be9-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="32be9-120">Optional.</span></span> <span data-ttu-id="32be9-121">Nombre del archivo de efectos, que solo se usa para los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="32be9-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="32be9-122">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="32be9-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="32be9-123">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32be9-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32be9-124">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="32be9-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="32be9-125">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="32be9-125">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="32be9-126">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32be9-126">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32be9-127">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="32be9-127">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="32be9-128">Un puntero a una interfaz de inclusión (vea la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="32be9-128">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="32be9-129">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32be9-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32be9-130">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="32be9-130">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="32be9-131">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="32be9-131">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="32be9-132">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="32be9-132">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="32be9-133">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32be9-133">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32be9-134">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="32be9-134">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="32be9-135">Puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene el sombreador sin compilar.</span><span class="sxs-lookup"><span data-stu-id="32be9-135">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="32be9-136">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32be9-136">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32be9-137">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="32be9-137">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="32be9-138">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de creación de efectos, si los hubiera.</span><span class="sxs-lookup"><span data-stu-id="32be9-138">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32be9-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32be9-139">Return value</span></span>

<span data-ttu-id="32be9-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="32be9-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="32be9-141">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="32be9-141">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32be9-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32be9-142">Requirements</span></span>



| <span data-ttu-id="32be9-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="32be9-143">Requirement</span></span> | <span data-ttu-id="32be9-144">Value</span><span class="sxs-lookup"><span data-stu-id="32be9-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32be9-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32be9-145">Header</span></span><br/>  | <dl> <span data-ttu-id="32be9-146"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="32be9-146"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="32be9-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32be9-147">Library</span></span><br/> | <dl> <span data-ttu-id="32be9-148"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32be9-148"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32be9-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="32be9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32be9-150">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="32be9-150">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

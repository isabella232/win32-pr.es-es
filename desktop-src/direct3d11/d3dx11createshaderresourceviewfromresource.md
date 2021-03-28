---
title: Función D3DX11CreateShaderResourceViewFromResource (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda que use las funciones de recursos y, a continuación, la biblioteca DirectXTK (Runtime), CreateXXXTextureFromMemory (donde XXX es DDS o WIC) Biblioteca DirectXTex (Tools), LoadFromXXXMemory (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de código fuente común para juegos) y CreateShaderResourceView crear una vista de recursos de sombreador a partir de un recurso.
ms.assetid: 64620e6d-fc0d-4411-8744-d9d8ffe6ccb8
keywords:
- Función D3DX11CreateShaderResourceViewFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb374bd569cb58451461a7fe269c58c200895b7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998520"
---
# <a name="d3dx11createshaderresourceviewfromresource-function"></a><span data-ttu-id="fcfb3-105">D3DX11CreateShaderResourceViewFromResource función)</span><span class="sxs-lookup"><span data-stu-id="fcfb3-105">D3DX11CreateShaderResourceViewFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="fcfb3-106">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="fcfb3-107">En lugar de usar esta función, se recomienda usar funciones de [recursos](/windows/desktop/menurc/resources-functions)y, a continuación:</span><span class="sxs-lookup"><span data-stu-id="fcfb3-107">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then these:</span></span>
>
> -   <span data-ttu-id="fcfb3-108">Biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMMEMORY** (donde xxx es DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="fcfb3-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="fcfb3-109">Biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (herramientas), **LOADFROMXXXMEMORY** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego **CreateShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="fcfb3-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="fcfb3-110">Cree una vista de recursos del sombreador desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-110">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcfb3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcfb3-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromResource(
  _In_  ID3D11Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="fcfb3-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcfb3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcfb3-113">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcfb3-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcfb3-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="fcfb3-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="fcfb3-115">Un puntero al dispositivo (vea [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará el recurso.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="fcfb3-116">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcfb3-116">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcfb3-117">Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fcfb3-117">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fcfb3-118">Identificador del módulo de recursos que contiene la vista de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-118">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="fcfb3-119">HMODULE se puede obtener con la [función GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="fcfb3-119">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="fcfb3-120">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcfb3-120">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcfb3-121">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fcfb3-121">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fcfb3-122">Nombre de la vista de recursos del sombreador en hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-122">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="fcfb3-123">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-123">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fcfb3-124">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-124">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="fcfb3-125">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcfb3-125">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcfb3-126">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcfb3-126">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="fcfb3-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-127">Optional.</span></span> <span data-ttu-id="fcfb3-128">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-128">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="fcfb3-129">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcfb3-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcfb3-130">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcfb3-130">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="fcfb3-131">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="fcfb3-131">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="fcfb3-132">Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-132">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="fcfb3-133">*ppShaderResourceView* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fcfb3-133">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcfb3-134">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="fcfb3-134">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="fcfb3-135">Dirección de un puntero a la vista de recursos del sombreador (vea [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="fcfb3-135">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="fcfb3-136">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fcfb3-136">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcfb3-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="fcfb3-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="fcfb3-138">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-138">A pointer to the return value.</span></span> <span data-ttu-id="fcfb3-139">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-139">May be **NULL**.</span></span> <span data-ttu-id="fcfb3-140">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="fcfb3-140">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcfb3-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcfb3-141">Return value</span></span>

<span data-ttu-id="fcfb3-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcfb3-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcfb3-143">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fcfb3-143">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcfb3-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcfb3-144">Requirements</span></span>



| <span data-ttu-id="fcfb3-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcfb3-145">Requirement</span></span> | <span data-ttu-id="fcfb3-146">Value</span><span class="sxs-lookup"><span data-stu-id="fcfb3-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcfb3-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcfb3-147">Header</span></span><br/>  | <dl> <span data-ttu-id="fcfb3-148"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcfb3-148"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fcfb3-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcfb3-149">Library</span></span><br/> | <dl> <span data-ttu-id="fcfb3-150"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcfb3-150"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fcfb3-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcfb3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcfb3-152">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="fcfb3-152">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 


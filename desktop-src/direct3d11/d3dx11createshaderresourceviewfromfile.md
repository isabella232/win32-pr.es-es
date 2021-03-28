---
title: Función D3DX11CreateShaderResourceViewFromFile (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar esta biblioteca DirectXTK (Runtime), CreateXXXTextureFromFile (donde XXX es DDS o WIC) DirectXTex Library (Tools), LoadFromXXXFile (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de código fuente común para juegos) y CreateShaderResourceView crear una vista de recursos de sombreador a partir de un archivo.
ms.assetid: c6a23503-f511-49dc-a0dc-19932cf8f313
keywords:
- Función D3DX11CreateShaderResourceViewFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05e7d710b0b379f3027591c2ff9e52c2fdd0d7a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362669"
---
# <a name="d3dx11createshaderresourceviewfromfile-function"></a><span data-ttu-id="c7a30-105">D3DX11CreateShaderResourceViewFromFile función)</span><span class="sxs-lookup"><span data-stu-id="c7a30-105">D3DX11CreateShaderResourceViewFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="c7a30-106">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="c7a30-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="c7a30-107">En lugar de usar esta función, se recomienda usar estas:</span><span class="sxs-lookup"><span data-stu-id="c7a30-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="c7a30-108">Biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMFILE** (donde xxx es DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="c7a30-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="c7a30-109">Biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (herramientas), **LOADFROMXXXFILE** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego **CreateShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="c7a30-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="c7a30-110">Cree una vista de recursos del sombreador a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="c7a30-110">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a30-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7a30-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="c7a30-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7a30-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7a30-113">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7a30-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a30-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="c7a30-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="c7a30-115">Un puntero al dispositivo (vea [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará el recurso.</span><span class="sxs-lookup"><span data-stu-id="c7a30-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="c7a30-116">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7a30-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a30-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7a30-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c7a30-118">Nombre del archivo que contiene la vista de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="c7a30-118">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="c7a30-119">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="c7a30-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c7a30-120">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c7a30-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="c7a30-121">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7a30-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a30-122">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7a30-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="c7a30-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c7a30-123">Optional.</span></span> <span data-ttu-id="c7a30-124">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="c7a30-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="c7a30-125">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7a30-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a30-126">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7a30-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="c7a30-127">Puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="c7a30-127">Pointer to a thread-pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="c7a30-128">Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.</span><span class="sxs-lookup"><span data-stu-id="c7a30-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="c7a30-129">*ppShaderResourceView* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c7a30-129">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a30-130">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="c7a30-130">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="c7a30-131">Dirección de un puntero a la vista de recursos del sombreador (vea [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="c7a30-131">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="c7a30-132">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c7a30-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a30-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c7a30-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c7a30-134">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c7a30-134">A pointer to the return value.</span></span> <span data-ttu-id="c7a30-135">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c7a30-135">May be **NULL**.</span></span> <span data-ttu-id="c7a30-136">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c7a30-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7a30-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7a30-137">Return value</span></span>

<span data-ttu-id="c7a30-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7a30-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7a30-139">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c7a30-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7a30-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7a30-140">Remarks</span></span>

<span data-ttu-id="c7a30-141">Para obtener una lista de formatos de imagen compatibles, consulte [**\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="c7a30-141">For a list of supported image formats, see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7a30-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7a30-142">Requirements</span></span>



| <span data-ttu-id="c7a30-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7a30-143">Requirement</span></span> | <span data-ttu-id="c7a30-144">Value</span><span class="sxs-lookup"><span data-stu-id="c7a30-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a30-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7a30-145">Header</span></span><br/>  | <dl> <span data-ttu-id="c7a30-146"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7a30-146"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c7a30-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7a30-147">Library</span></span><br/> | <dl> <span data-ttu-id="c7a30-148"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7a30-148"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c7a30-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7a30-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a30-150">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="c7a30-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 


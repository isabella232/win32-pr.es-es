---
title: Función D3DX11CreateShaderResourceViewFromMemory (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar esta biblioteca DirectXTK (Runtime), CreateXXXTextureFromMemory (donde XXX es DDS o WIC) DirectXTex Library (Tools), LoadFromXXXMemory (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de código fuente común para juegos) y CreateShaderResourceView crear una vista de recursos de sombreador a partir de un archivo en memoria.
ms.assetid: fd75b187-2c9c-403c-8327-c312c4cda238
keywords:
- Función D3DX11CreateShaderResourceViewFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0730fafdeb85cc22944f282eaaf556a1cdb12d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998521"
---
# <a name="d3dx11createshaderresourceviewfrommemory-function"></a><span data-ttu-id="90bc6-105">D3DX11CreateShaderResourceViewFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="90bc6-105">D3DX11CreateShaderResourceViewFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="90bc6-106">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="90bc6-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="90bc6-107">En lugar de usar esta función, se recomienda usar estas:</span><span class="sxs-lookup"><span data-stu-id="90bc6-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="90bc6-108">Biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMMEMORY** (donde xxx es DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="90bc6-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="90bc6-109">Biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (herramientas), **LOADFROMXXXMEMORY** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego **CreateShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="90bc6-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="90bc6-110">Cree una vista de recursos del sombreador desde un archivo en la memoria.</span><span class="sxs-lookup"><span data-stu-id="90bc6-110">Create a shader-resource view from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="90bc6-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90bc6-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromMemory(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="90bc6-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90bc6-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90bc6-113">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90bc6-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90bc6-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="90bc6-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="90bc6-115">Un puntero al dispositivo (vea [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará el recurso.</span><span class="sxs-lookup"><span data-stu-id="90bc6-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="90bc6-116">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90bc6-116">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90bc6-117">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="90bc6-117">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="90bc6-118">Puntero al archivo en memoria que contiene la vista de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="90bc6-118">Pointer to the file in memory that contains the shader-resource view.</span></span>

</dd> <dt>

<span data-ttu-id="90bc6-119">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90bc6-119">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90bc6-120">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="90bc6-120">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="90bc6-121">Tamaño del archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="90bc6-121">Size of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="90bc6-122">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90bc6-122">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90bc6-123">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="90bc6-123">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="90bc6-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="90bc6-124">Optional.</span></span> <span data-ttu-id="90bc6-125">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="90bc6-125">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="90bc6-126">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90bc6-126">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90bc6-127">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="90bc6-127">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="90bc6-128">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="90bc6-128">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="90bc6-129">Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.</span><span class="sxs-lookup"><span data-stu-id="90bc6-129">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="90bc6-130">*ppShaderResourceView* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90bc6-130">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90bc6-131">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="90bc6-131">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="90bc6-132">Dirección de un puntero a la vista de recursos del sombreador recién creada.</span><span class="sxs-lookup"><span data-stu-id="90bc6-132">Address of a pointer to the newly created shader resource view.</span></span> <span data-ttu-id="90bc6-133">Vea [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="90bc6-133">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="90bc6-134">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90bc6-134">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90bc6-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="90bc6-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="90bc6-136">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="90bc6-136">A pointer to the return value.</span></span> <span data-ttu-id="90bc6-137">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="90bc6-137">May be **NULL**.</span></span> <span data-ttu-id="90bc6-138">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="90bc6-138">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90bc6-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90bc6-139">Return value</span></span>

<span data-ttu-id="90bc6-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90bc6-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90bc6-141">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="90bc6-141">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90bc6-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90bc6-142">Requirements</span></span>



| <span data-ttu-id="90bc6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="90bc6-143">Requirement</span></span> | <span data-ttu-id="90bc6-144">Value</span><span class="sxs-lookup"><span data-stu-id="90bc6-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90bc6-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90bc6-145">Header</span></span><br/>  | <dl> <span data-ttu-id="90bc6-146"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="90bc6-146"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="90bc6-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90bc6-147">Library</span></span><br/> | <dl> <span data-ttu-id="90bc6-148"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90bc6-148"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="90bc6-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="90bc6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90bc6-150">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="90bc6-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 


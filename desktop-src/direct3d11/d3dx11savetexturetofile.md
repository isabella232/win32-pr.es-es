---
title: Función D3DX11SaveTextureToFile (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, CaptureTexture then SaveToXXXFile (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos. Para el escenario simplificado de creación de una captura de pantalla a partir de una textura de destino de representación, se recomienda usar la biblioteca DirectXTK, SaveDDSTextureToFile o SaveWICTextureToFile. Guardar una textura en un archivo.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- Función D3DX11SaveTextureToFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986989"
---
# <a name="d3dx11savetexturetofile-function"></a><span data-ttu-id="449c8-107">D3DX11SaveTextureToFile función)</span><span class="sxs-lookup"><span data-stu-id="449c8-107">D3DX11SaveTextureToFile function</span></span>

> [!Note]  
> <span data-ttu-id="449c8-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="449c8-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="449c8-109">En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** then **SAVETOXXXFILE** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.</span><span class="sxs-lookup"><span data-stu-id="449c8-109">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="449c8-110">Para el escenario simplificado de creación de una captura de pantalla a partir de una textura de destino de representación, se recomienda usar la biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SaveDDSTextureToFile** o **SaveWICTextureToFile**.</span><span class="sxs-lookup"><span data-stu-id="449c8-110">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SaveDDSTextureToFile** or **SaveWICTextureToFile**.</span></span>

 

<span data-ttu-id="449c8-111">Guardar una textura en un archivo.</span><span class="sxs-lookup"><span data-stu-id="449c8-111">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="449c8-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="449c8-112">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="449c8-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="449c8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="449c8-114">*pContext*</span><span class="sxs-lookup"><span data-stu-id="449c8-114">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="449c8-115">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="449c8-115">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="449c8-116">Un puntero a un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="449c8-116">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="449c8-117">*pSrcTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="449c8-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="449c8-118">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="449c8-118">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="449c8-119">Puntero a la textura que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="449c8-119">Pointer to the texture to be saved.</span></span> <span data-ttu-id="449c8-120">Vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="449c8-120">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="449c8-121">*DestFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="449c8-121">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="449c8-122">Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="449c8-122">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="449c8-123">El formato con el que se guardará la textura (consulte [**\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="449c8-123">The format the texture will be saved as (see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)).</span></span> <span data-ttu-id="449c8-124">D3DX11 \_ IFF \_ es el formato preferido, ya que es la única opción que admite todos los formatos en [**el \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="449c8-124">D3DX11\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="449c8-125">*pDestFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="449c8-125">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="449c8-126">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="449c8-126">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="449c8-127">Nombre del archivo de salida de destino en el que se guardará la textura.</span><span class="sxs-lookup"><span data-stu-id="449c8-127">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="449c8-128">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="449c8-128">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="449c8-129">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="449c8-129">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="449c8-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="449c8-130">Return value</span></span>

<span data-ttu-id="449c8-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="449c8-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="449c8-132">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md); Use el valor devuelto para ver si se admite *DestFormat* .</span><span class="sxs-lookup"><span data-stu-id="449c8-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="449c8-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="449c8-133">Remarks</span></span>

<span data-ttu-id="449c8-134">**D3DX11SaveTextureToFile** escribe la estructura del [**encabezado DDS adicional \_ \_ DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) para la textura de entrada solo si es necesario (por ejemplo, porque la textura de entrada está en formato RGB estándar (sRGB)).</span><span class="sxs-lookup"><span data-stu-id="449c8-134">**D3DX11SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="449c8-135">Si **D3DX11SaveTextureToFile** escribe la estructura **del \_ encabezado \_ DDS DXT10** , establece el miembro **DwFourCC** de la estructura [**de \_ PIXELFORMAT de DDS**](/windows/desktop/direct3ddds/dds-pixelformat) para la textura en **contenido DX10** para indicar el prescense del **encabezado \_ DDS \_ DXT10** encabezado extendido.</span><span class="sxs-lookup"><span data-stu-id="449c8-135">If **D3DX11SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="449c8-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="449c8-136">Requirements</span></span>



| <span data-ttu-id="449c8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="449c8-137">Requirement</span></span> | <span data-ttu-id="449c8-138">Value</span><span class="sxs-lookup"><span data-stu-id="449c8-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="449c8-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="449c8-139">Header</span></span><br/>  | <dl> <span data-ttu-id="449c8-140"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="449c8-140"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="449c8-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="449c8-141">Library</span></span><br/> | <dl> <span data-ttu-id="449c8-142"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="449c8-142"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="449c8-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="449c8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="449c8-144">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="449c8-144">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 


---
description: Guardar una textura en un archivo.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Función D3DX10SaveTextureToFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698450"
---
# <a name="d3dx10savetexturetofile-function"></a><span data-ttu-id="f251d-103">D3DX10SaveTextureToFile función)</span><span class="sxs-lookup"><span data-stu-id="f251d-103">D3DX10SaveTextureToFile function</span></span>

<span data-ttu-id="f251d-104">Guardar una textura en un archivo.</span><span class="sxs-lookup"><span data-stu-id="f251d-104">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f251d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f251d-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="f251d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f251d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f251d-107">*pSrcTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f251d-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f251d-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="f251d-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="f251d-109">Puntero a la textura que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="f251d-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="f251d-110">Consulte la [**interfaz ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="f251d-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="f251d-111">*DestFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f251d-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f251d-112">Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="f251d-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="f251d-113">El formato con el que se guardará la textura (consulte [**\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="f251d-113">The format the texture will be saved as (see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)).</span></span> <span data-ttu-id="f251d-114">D3DX10 \_ IFF \_ es el formato preferido, ya que es la única opción que admite todos los formatos en [**el \_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f251d-114">D3DX10\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="f251d-115">*pDestFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f251d-115">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f251d-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f251d-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f251d-117">Nombre del archivo de salida de destino en el que se guardará la textura.</span><span class="sxs-lookup"><span data-stu-id="f251d-117">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="f251d-118">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="f251d-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f251d-119">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f251d-119">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f251d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f251d-120">Return value</span></span>

<span data-ttu-id="f251d-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f251d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f251d-122">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md). Use el valor devuelto para ver si se admite *DestFormat* .</span><span class="sxs-lookup"><span data-stu-id="f251d-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="f251d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f251d-123">Remarks</span></span>

<span data-ttu-id="f251d-124">**D3DX10SaveTextureToFile** escribe la estructura del [**encabezado DDS adicional \_ \_ DXT10**](../direct3ddds/dds-header-dxt10.md) para la textura de entrada solo si es necesario (por ejemplo, porque la textura de entrada está en formato RGB estándar (sRGB)).</span><span class="sxs-lookup"><span data-stu-id="f251d-124">**D3DX10SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](../direct3ddds/dds-header-dxt10.md) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="f251d-125">Si **D3DX10SaveTextureToFile** escribe la estructura **del \_ encabezado \_ DDS DXT10** , establece el miembro **DwFourCC** de la estructura [**de \_ PIXELFORMAT de DDS**](../direct3ddds/dds-pixelformat.md) para la textura en **contenido DX10** para indicar el prescense del **encabezado \_ DDS \_ DXT10** encabezado extendido.</span><span class="sxs-lookup"><span data-stu-id="f251d-125">If **D3DX10SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="f251d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f251d-126">Requirements</span></span>



| <span data-ttu-id="f251d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f251d-127">Requirement</span></span> | <span data-ttu-id="f251d-128">Value</span><span class="sxs-lookup"><span data-stu-id="f251d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f251d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f251d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f251d-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f251d-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f251d-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f251d-131">Library</span></span><br/> | <dl> <span data-ttu-id="f251d-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f251d-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f251d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f251d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f251d-134">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="f251d-134">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="f251d-135">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="f251d-135">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

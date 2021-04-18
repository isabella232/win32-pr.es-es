---
title: D3DX11_IMAGE_LOAD_INFO estructura (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas. | D3DX11_IMAGE_LOAD_INFO estructura (D3DX11tex. h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO estructura de Direct3D 11
- Puntero de estructura de LPD3DX11_IMAGE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987205"
---
# <a name="d3dx11_image_load_info-structure"></a><span data-ttu-id="8f9af-107">\_Estructura de \_ información de carga de imagen de D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="8f9af-107">D3DX11\_IMAGE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="8f9af-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="8f9af-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="8f9af-109">Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas.</span><span class="sxs-lookup"><span data-stu-id="8f9af-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="8f9af-110">Un valor de D3DX11 \_ predeterminado para cualquiera de estos parámetros hará que D3DX use automáticamente el valor del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="8f9af-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9af-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f9af-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="8f9af-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f9af-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f9af-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="8f9af-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-115">Ancho de destino de la textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-115">The target width of the texture.</span></span> <span data-ttu-id="8f9af-116">Si el ancho real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este ancho de destino.</span><span class="sxs-lookup"><span data-stu-id="8f9af-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-117">**Height**</span><span class="sxs-lookup"><span data-stu-id="8f9af-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-119">Alto de destino de la textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-119">The target height of the texture.</span></span> <span data-ttu-id="8f9af-120">Si el alto real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este alto de destino.</span><span class="sxs-lookup"><span data-stu-id="8f9af-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-121">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="8f9af-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-123">Profundidad de la textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-123">The depth of the texture.</span></span> <span data-ttu-id="8f9af-124">Esto solo se aplica a las texturas de volumen.</span><span class="sxs-lookup"><span data-stu-id="8f9af-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-125">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="8f9af-125">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-127">Nivel de mipmap de resolución más alto de la textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-127">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="8f9af-128">Si es mayor que 0, después de que se cargue la textura, FirstMipLevel se asignará al nivel 0 del mipmap.</span><span class="sxs-lookup"><span data-stu-id="8f9af-128">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-129">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="8f9af-129">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-131">Número máximo de niveles de mipmap en la textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-131">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="8f9af-132">Vea los comentarios de [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="8f9af-132">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="8f9af-133">El uso del valor predeterminado de 0 o D3DX11 hará que \_ se cree una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="8f9af-133">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-134">**Uso**</span><span class="sxs-lookup"><span data-stu-id="8f9af-134">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-135">Tipo: **[ **\_ uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-135">Type: **[**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-136">La forma en que se va a usar el recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-136">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="8f9af-137">Vea [**\_ uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="8f9af-137">See [**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-138">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="8f9af-138">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-139">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-139">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-140">Fases de canalización a las que se puede enlazar la textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-140">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="8f9af-141">Vea [**D3D11 \_ BIND \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="8f9af-141">See [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-142">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="8f9af-142">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-143">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-144">Los permisos de acceso que tendrá la CPU para el recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-144">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="8f9af-145">Consulte [**\_ marca de \_ acceso \_ de CPU de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="8f9af-145">See [**D3D11\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-146">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="8f9af-146">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-147">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-147">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-148">Propiedades de recursos misceláneas (consulte la [**marca D3D11 de \_ recursos \_ varios \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="8f9af-148">Miscellaneous resource properties (see [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-149">**Format**</span><span class="sxs-lookup"><span data-stu-id="8f9af-149">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-150">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-151">Una enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) que indica el formato en el que estará la textura después de cargarse.</span><span class="sxs-lookup"><span data-stu-id="8f9af-151">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration indicating the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-152">**Filtrar**</span><span class="sxs-lookup"><span data-stu-id="8f9af-152">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-153">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-153">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-154">Filtre la textura mediante el filtro especificado (solo cuando se remuestre).</span><span class="sxs-lookup"><span data-stu-id="8f9af-154">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="8f9af-155">Vea [**D3DX11 \_ Filter \_ Flag**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="8f9af-155">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-156">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="8f9af-156">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-157">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f9af-157">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-158">Filtre los niveles de textura de MIP mediante el filtro especificado (solo si se generan mapas MIP).</span><span class="sxs-lookup"><span data-stu-id="8f9af-158">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="8f9af-159">Los valores válidos son D3DX11 \_ Filter \_ None, D3DX11 Filter \_ \_ Point, D3DX11 \_ Filter \_ linear o D3DX11 \_ Filter \_ Triangle.</span><span class="sxs-lookup"><span data-stu-id="8f9af-159">Valid values are D3DX11\_FILTER\_NONE, D3DX11\_FILTER\_POINT, D3DX11\_FILTER\_LINEAR, or D3DX11\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="8f9af-160">Vea [**D3DX11 \_ Filter \_ Flag**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="8f9af-160">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f9af-161">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="8f9af-161">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8f9af-162">Tipo: **[ **\_ \_ información de imagen de D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f9af-162">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="8f9af-163">Información sobre la imagen original.</span><span class="sxs-lookup"><span data-stu-id="8f9af-163">Information about the original image.</span></span> <span data-ttu-id="8f9af-164">Consulte [**la \_ \_ información**](d3dx11-image-info.md)de la imagen de D3DX11.</span><span class="sxs-lookup"><span data-stu-id="8f9af-164">See [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md).</span></span> <span data-ttu-id="8f9af-165">Se puede obtener con [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="8f9af-165">Can be obtained with [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f9af-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f9af-166">Remarks</span></span>

<span data-ttu-id="8f9af-167">Al inicializar la estructura, puede establecer cualquier miembro en D3DX11 \_ default y D3DX lo inicializará con un valor predeterminado de la textura de origen cuando se cargue la textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-167">When initializing the structure, you may set any member to D3DX11\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="8f9af-168">Esta estructura la pueden usar las API que:</span><span class="sxs-lookup"><span data-stu-id="8f9af-168">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="8f9af-169">Cree recursos, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) y [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="8f9af-169">Create resources, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="8f9af-170">Cree procesadores de datos, como [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) o [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="8f9af-170">Create data processors, such as [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) or [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span></span>

<span data-ttu-id="8f9af-171">Los valores predeterminados son:</span><span class="sxs-lookup"><span data-stu-id="8f9af-171">The default values are:</span></span>


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



<span data-ttu-id="8f9af-172">Este es un breve ejemplo que usa esta estructura para proporcionar el formato de píxel al cargar una textura.</span><span class="sxs-lookup"><span data-stu-id="8f9af-172">Here is a brief example that uses this structure to supply the pixel format when loading a texture.</span></span> <span data-ttu-id="8f9af-173">Para obtener el código completo, consulte HDRFormats10. cpp en el [ejemplo HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="8f9af-173">For the complete code, see HDRFormats10.cpp in [HDRToneMappingCS11 Sample](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span></span>


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a><span data-ttu-id="8f9af-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f9af-174">Requirements</span></span>



| <span data-ttu-id="8f9af-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f9af-175">Requirement</span></span> | <span data-ttu-id="8f9af-176">Value</span><span class="sxs-lookup"><span data-stu-id="8f9af-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9af-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f9af-177">Header</span></span><br/> | <dl> <span data-ttu-id="8f9af-178"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f9af-178"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f9af-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f9af-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9af-180">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="8f9af-180">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 


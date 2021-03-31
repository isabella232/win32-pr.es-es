---
description: Usar texturas comprimidas (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Usar texturas comprimidas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806853"
---
# <a name="using-compressed-textures-direct3d-9"></a><span data-ttu-id="bc3dd-103">Usar texturas comprimidas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc3dd-103">Using Compressed Textures (Direct3D 9)</span></span>

## <a name="determining-support-for-compressed-textures"></a><span data-ttu-id="bc3dd-104">Determinar la compatibilidad con las texturas comprimidas</span><span class="sxs-lookup"><span data-stu-id="bc3dd-104">Determining Support for Compressed Textures</span></span>

<span data-ttu-id="bc3dd-105">Para probar el adaptador, especifique cualquier formato de píxel que use DXT1, DXT2, DXT3, DXT4 o DXT5.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-105">To test the adapter, specify any pixel format that uses the DXT1, DXT2, DXT3, DXT4, or DXT5.</span></span> <span data-ttu-id="bc3dd-106">Si [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) devuelve D3D \_ OK, el dispositivo puede crear textura directamente desde una superficie de textura comprimida que use ese formato.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-106">If [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) returns D3D\_OK, the device can create texture directly from a compressed texture surface that uses that format.</span></span> <span data-ttu-id="bc3dd-107">Si es así, puede usar superficies de textura comprimidas directamente con Direct3D llamando al método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="bc3dd-107">If so, you can use compressed texture surfaces directly with Direct3D by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="bc3dd-108">En el ejemplo de código siguiente se muestra cómo determinar si el adaptador admite un formato de textura comprimido.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-108">The following code example shows how to determine if the adapter supports a compressed texture format.</span></span>


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



<span data-ttu-id="bc3dd-109">Si el dispositivo no admite la texturización desde superficies de textura comprimidas, todavía puede almacenar los datos de textura en una superficie de formato comprimido, pero debe convertir las texturas comprimidas en un formato admitido antes de que se puedan usar para la texturización.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-109">If the device does not support texturing from compressed texture surfaces, you can still store texture data in a compressed format surface, but you must convert any compressed textures to a supported format before they can be used for texturing.</span></span>

## <a name="creating-compressed-textures"></a><span data-ttu-id="bc3dd-110">Crear texturas comprimidas</span><span class="sxs-lookup"><span data-stu-id="bc3dd-110">Creating Compressed Textures</span></span>

<span data-ttu-id="bc3dd-111">Después de crear un dispositivo que admita un formato de textura comprimido en el adaptador, puede crear un recurso de textura comprimido.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-111">After creating a device that supports a compressed texture format on the adapter, you can create a compressed texture resource.</span></span> <span data-ttu-id="bc3dd-112">Llame a [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) y especifique un formato de textura comprimido para el parámetro de formato.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-112">Call [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) and specify a compressed texture format for the Format parameter.</span></span>

<span data-ttu-id="bc3dd-113">Antes de cargar una imagen en un objeto de textura, recupere un puntero a la superficie de textura mediante una llamada al método [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) .</span><span class="sxs-lookup"><span data-stu-id="bc3dd-113">Before loading an image into a texture object, retrieve a pointer to the texture surface by calling the [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) method.</span></span>

<span data-ttu-id="bc3dd-114">Ahora puede usar cualquier función D3DXLoadSurfacexxx para cargar una imagen en la superficie que se ha recuperado mediante [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span><span class="sxs-lookup"><span data-stu-id="bc3dd-114">Now you can use any D3DXLoadSurfacexxx function to load an image to the surface that was retrieved by using [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span></span> <span data-ttu-id="bc3dd-115">Estas funciones controlan la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-115">These functions handle conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="bc3dd-116">Puede crear y convertir archivos de textura comprimida (DDS) mediante el editor de texturas de DirectX (Dxtex.exe) suministrado con el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-116">You can create and convert compressed texture (DDS) files using the DirectX Texture Editor (Dxtex.exe) supplied with the DirectX SDK.</span></span> <span data-ttu-id="bc3dd-117">Puede obtener Dxtex.exe y obtener información sobre él desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-117">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="bc3dd-118">Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="bc3dd-118">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="bc3dd-119">La ventaja de este comportamiento es que una aplicación puede copiar el contenido de una superficie comprimida en un archivo sin calcular la cantidad de almacenamiento necesaria para una superficie de un ancho y un alto determinados en el formato específico.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-119">The advantage of this behavior is that an application can copy the contents of a compressed surface to a file without calculating how much storage is required for a surface of a particular width and height in the specific format.</span></span>

<span data-ttu-id="bc3dd-120">En la tabla siguiente se muestran los cinco tipos de texturas comprimidas.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-120">The following table shows the five types of compressed textures.</span></span> <span data-ttu-id="bc3dd-121">Para obtener más información sobre cómo se almacenan los datos, vea [formatos de textura comprimidos (Direct3D 9)](compressed-texture-formats.md).</span><span class="sxs-lookup"><span data-stu-id="bc3dd-121">For more information about how the data is stored, see [Compressed Texture Formats (Direct3D 9)](compressed-texture-formats.md).</span></span> <span data-ttu-id="bc3dd-122">Solo necesitará esta información si está escribiendo sus propias rutinas de compresión.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-122">You only need this information if you are writing your own compression routines.</span></span>



| <span data-ttu-id="bc3dd-123">FOURCC</span><span class="sxs-lookup"><span data-stu-id="bc3dd-123">FOURCC</span></span> | <span data-ttu-id="bc3dd-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc3dd-124">Description</span></span>        | <span data-ttu-id="bc3dd-125">¿Alfa premultiplicado?</span><span class="sxs-lookup"><span data-stu-id="bc3dd-125">Alpha premultiplied?</span></span> |
|--------|--------------------|----------------------|
| <span data-ttu-id="bc3dd-126">DXT1</span><span class="sxs-lookup"><span data-stu-id="bc3dd-126">DXT1</span></span>   | <span data-ttu-id="bc3dd-127">Alfa opaco/1 bit</span><span class="sxs-lookup"><span data-stu-id="bc3dd-127">Opaque/1-bit alpha</span></span> | <span data-ttu-id="bc3dd-128">N/D</span><span class="sxs-lookup"><span data-stu-id="bc3dd-128">N/A</span></span>                  |
| <span data-ttu-id="bc3dd-129">DXT2</span><span class="sxs-lookup"><span data-stu-id="bc3dd-129">DXT2</span></span>   | <span data-ttu-id="bc3dd-130">Alfa explícito</span><span class="sxs-lookup"><span data-stu-id="bc3dd-130">Explicit alpha</span></span>     | <span data-ttu-id="bc3dd-131">Sí</span><span class="sxs-lookup"><span data-stu-id="bc3dd-131">Yes</span></span>                  |
| <span data-ttu-id="bc3dd-132">DXT3</span><span class="sxs-lookup"><span data-stu-id="bc3dd-132">DXT3</span></span>   | <span data-ttu-id="bc3dd-133">Alfa explícito</span><span class="sxs-lookup"><span data-stu-id="bc3dd-133">Explicit alpha</span></span>     | <span data-ttu-id="bc3dd-134">No</span><span class="sxs-lookup"><span data-stu-id="bc3dd-134">No</span></span>                   |
| <span data-ttu-id="bc3dd-135">DXT4</span><span class="sxs-lookup"><span data-stu-id="bc3dd-135">DXT4</span></span>   | <span data-ttu-id="bc3dd-136">Alfa interpolado</span><span class="sxs-lookup"><span data-stu-id="bc3dd-136">Interpolated alpha</span></span> | <span data-ttu-id="bc3dd-137">Sí</span><span class="sxs-lookup"><span data-stu-id="bc3dd-137">Yes</span></span>                  |
| <span data-ttu-id="bc3dd-138">DXT5</span><span class="sxs-lookup"><span data-stu-id="bc3dd-138">DXT5</span></span>   | <span data-ttu-id="bc3dd-139">Alfa interpolado</span><span class="sxs-lookup"><span data-stu-id="bc3dd-139">Interpolated alpha</span></span> | <span data-ttu-id="bc3dd-140">No</span><span class="sxs-lookup"><span data-stu-id="bc3dd-140">No</span></span>                   |



 

<span data-ttu-id="bc3dd-141">Cuando se transfieren datos de un formato nonpremultiplied a un formato premultiplicado, Direct3D escala los colores en función de los valores alfa.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-141">When you transfer data from a nonpremultiplied format to a premultiplied format, Direct3D scales the colors based on the alpha values.</span></span> <span data-ttu-id="bc3dd-142">No se admite la transferencia de datos a partir de un formato premultiplicado a un formato nonpremultiplied.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-142">Transferring data from a premultiplied format to a nonpremultiplied format is not supported.</span></span> <span data-ttu-id="bc3dd-143">Si intenta transferir datos de un origen alfa premultiplicado a un destino Alfa nonpremultiplied, el método devuelve D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-143">If you try to transfer data from a premultiplied alpha source to a nonpremultiplied alpha destination, the method returns D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="bc3dd-144">Si se transfieren datos de un origen alfa premultiplicado a un destino que no tiene alfa, los componentes de color de origen, que se han escalado por alfa, se copian tal cual.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-144">If you transfer data from a premultiplied alpha source to a destination that has no alpha, the source color components, which have been scaled by alpha, are copied as is.</span></span>

## <a name="decompressing-compressed-texture-surfaces"></a><span data-ttu-id="bc3dd-145">Descomprimir superficies de textura comprimidas</span><span class="sxs-lookup"><span data-stu-id="bc3dd-145">Decompressing Compressed Texture Surfaces</span></span>

<span data-ttu-id="bc3dd-146">Al igual que con la compresión de una superficie de textura, la descompresión de una textura comprimida se realiza a través de los servicios de copia de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-146">As with compressing a texture surface, decompressing a compressed texture is performed through Direct3D copying services.</span></span>

<span data-ttu-id="bc3dd-147">Para copiar una superficie de textura comprimida en una superficie de textura sin comprimir, utilice la función [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span><span class="sxs-lookup"><span data-stu-id="bc3dd-147">To copy a compressed texture surface to a uncompressed texture surface, use the function [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span></span> <span data-ttu-id="bc3dd-148">Esta función controla la compresión hacia y desde superficies comprimidas y sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="bc3dd-148">This functions handles compression to and from compressed and uncompressed surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc3dd-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc3dd-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc3dd-150">Recursos de textura comprimidos</span><span class="sxs-lookup"><span data-stu-id="bc3dd-150">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 

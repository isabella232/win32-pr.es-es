---
title: Desempaquetar y empaquetar DXGI_FORMAT para la edición de In-Place imagen
description: El \_ archivo D3DX DXGIFormatConvert. INL contiene funciones de conversión de formato en línea que puede usar en el sombreador de cálculo o en el sombreador de píxeles en el hardware de Direct3D 11.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04f3729bbeda5b0677da9d52e595e621523ff2d1
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187906"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a><span data-ttu-id="f0c0a-103">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="f0c0a-103">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>

<span data-ttu-id="f0c0a-104">El \_ archivo D3DX DXGIFormatConvert. INL contiene funciones de conversión de formato en línea que puede usar en el sombreador de cálculo o en el sombreador de píxeles en el hardware de Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-104">The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="f0c0a-105">Puede usar estas funciones en la aplicación para leer y escribir simultáneamente en una textura.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-105">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="f0c0a-106">Es decir, puede realizar la edición en contexto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-106">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="f0c0a-107">Para usar estas funciones de conversión de formato en línea, incluya el \_ archivo D3DX DXGIFormatConvert. INL en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-107">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>

> <span data-ttu-id="f0c0a-108">El \_ encabezado de D3DX DXGIFormatConvert. INL se incluye en el SDK de DirectX heredado.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-108">The D3DX\_DXGIFormatConvert.inl header ships in the legacy DirectX SDK.</span></span> <span data-ttu-id="f0c0a-109">También se incluye en el paquete NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) .</span><span class="sxs-lookup"><span data-stu-id="f0c0a-109">It is also included in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package.</span></span>

<span data-ttu-id="f0c0a-110">La vista de acceso desordenado de Direct3D 11 (UAV) de un recurso Texture1D, Texture2D o Texture3D admite lecturas y escrituras de acceso aleatorio en la memoria desde un sombreador de cálculo o un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-110">Direct3D 11's Unordered Access View (UAV) of a Texture1D, Texture2D, or Texture3D resource supports random access reads and writes to memory from a compute shader or pixel shader.</span></span> <span data-ttu-id="f0c0a-111">Sin embargo, Direct3D 11 admite simultáneamente la lectura y la escritura en el formato de estilo DXGI \_ \_ R32 \_ uint Texture.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-111">However, Direct3D 11 supports simultaneously both reading from and writing to only the DXGI\_FORMAT\_R32\_UINT texture format.</span></span> <span data-ttu-id="f0c0a-112">Por ejemplo, Direct3D 11 no admite simultáneamente la lectura y la escritura en otros formatos más útiles, como el formato de DXGI \_ \_ R8G8B8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-112">For example, Direct3D 11 does not support simultaneously both reading from and writing to other, more useful formats, such as DXGI\_FORMAT\_R8G8B8A8\_UNORM.</span></span> <span data-ttu-id="f0c0a-113">Solo se puede usar un UAV para el acceso aleatorio de escritura a otros formatos, o solo se puede usar un sombreador Vista de recursos (SRV) para el acceso aleatorio leído de otros formatos.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-113">You can use only a UAV to random access write to such other formats, or you can use only a Shader Resource View (SRV) to random access read from such other formats.</span></span> <span data-ttu-id="f0c0a-114">El hardware de conversión de formato no está disponible para leer y escribir en otros formatos simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-114">Format conversion hardware is not available to simultaneously both read from and write to such other formats.</span></span>

<span data-ttu-id="f0c0a-115">Sin embargo, todavía puede leer simultáneamente y escribir en otros formatos mediante la conversión de la textura al \_ \_ formato dxgi R32 \_ uint Texture al crear un UAV, siempre que el formato original del recurso admita la conversión al \_ formato dxgi \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-115">However, you can still simultaneously both read from and write to such other formats by casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, as long as the original format of the resource supports casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="f0c0a-116">La mayoría de los formatos de elementos de 32 bits por elemento admiten la conversión al formato de DXGI \_ \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-116">Most 32 bit per element formats support casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="f0c0a-117">Al convertir la textura en el formato de DXGI \_ formato \_ R32 \_ uint cuando se crea un UAV, se pueden realizar de forma simultánea lecturas y escrituras en la textura siempre que el sombreador realice el desempaquetado manual de formato en la lectura y el empaquetado en la escritura.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-117">By casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, you can then simultaneous perform reads and writes to the texture as long as the shader performs manual format unpacking on read and packing on write.</span></span>

<span data-ttu-id="f0c0a-118">La ventaja de convertir la textura en el formato de DXGI \_ \_ R32 \_ uint Texture es que, más adelante, puede usar el formato adecuado (por ejemplo, DXGI \_ format \_ R16G16 \_ float) con otras vistas en la misma textura, como vistas de destino de representación (RTVs) o SRVs.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-118">The benefit of casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format is that later on you can use the appropriate format (for example, DXGI\_FORMAT\_R16G16\_FLOAT) with other views on the same texture, such as Render Target Views (RTVs) or SRVs.</span></span> <span data-ttu-id="f0c0a-119">Por lo tanto, el hardware puede realizar el desempaquetado y paquete de formato automático típico, puede realizar el filtrado de texturas, y así sucesivamente donde no haya limitaciones de hardware.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-119">Therefore, the hardware can perform the typical automatic format unpack and pack, can perform texture filtering, and so on where there are no hardware limitations.</span></span>

<span data-ttu-id="f0c0a-120">En el escenario siguiente se requiere que una aplicación realice la siguiente secuencia de acciones para realizar la edición de imágenes en contexto.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-120">The following scenario requires that an application take the following sequence of actions to perform in-place image editing.</span></span>

<span data-ttu-id="f0c0a-121">Supongamos que desea crear una textura en la que puede usar un sombreador de píxeles o un sombreador de cálculo para realizar la edición en contexto y desea almacenar los datos de textura en un formato descendiente de uno de los siguientes formatos sin tipo:</span><span class="sxs-lookup"><span data-stu-id="f0c0a-121">Suppose you want to make a texture on which you can use a pixel shader or compute shader to perform in-place editing, and you want the texture data to be stored in a format that is a descendant of one of the following TYPELESS formats:</span></span>

-   <span data-ttu-id="f0c0a-122">\_Formato de \_ DXGI \_ sin tipo R10G10B10A2</span><span class="sxs-lookup"><span data-stu-id="f0c0a-122">DXGI\_FORMAT\_R10G10B10A2\_TYPELESS</span></span>
-   <span data-ttu-id="f0c0a-123">\_Formato de \_ DXGI \_ sin tipo R8G8B8A8</span><span class="sxs-lookup"><span data-stu-id="f0c0a-123">DXGI\_FORMAT\_R8G8B8A8\_TYPELESS</span></span>
-   <span data-ttu-id="f0c0a-124">\_Formato de \_ DXGI \_ sin tipo B8G8R8A8</span><span class="sxs-lookup"><span data-stu-id="f0c0a-124">DXGI\_FORMAT\_B8G8R8A8\_TYPELESS</span></span>
-   <span data-ttu-id="f0c0a-125">\_Formato de \_ DXGI \_ sin tipo B8G8R8X8</span><span class="sxs-lookup"><span data-stu-id="f0c0a-125">DXGI\_FORMAT\_B8G8R8X8\_TYPELESS</span></span>
-   <span data-ttu-id="f0c0a-126">\_Formato de \_ DXGI \_ sin tipo R16G16</span><span class="sxs-lookup"><span data-stu-id="f0c0a-126">DXGI\_FORMAT\_R16G16\_TYPELESS</span></span>

<span data-ttu-id="f0c0a-127">Por ejemplo, el formato de DXGI \_ formato \_ R10G10B10A2 \_ UNORM es un descendiente del formato \_ dxgi \_ \_ sin tipo R10G10B10A2.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-127">For example, the DXGI\_FORMAT\_R10G10B10A2\_UNORM format is a descendant of the DXGI\_FORMAT\_R10G10B10A2\_TYPELESS format.</span></span> <span data-ttu-id="f0c0a-128">Por lo tanto \_ , \_ el formato de DXGI R10G10B10A2 \_ UNORM admite el patrón de uso que se describe en la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-128">Therefore, DXGI\_FORMAT\_R10G10B10A2\_UNORM supports the usage pattern that is described in the following sequence.</span></span> <span data-ttu-id="f0c0a-129">Los formatos que descienden del formato de DXGI \_ \_ R32 \_ sin tipo, como dxgi \_ format \_ R32 \_ float, se admiten de forma trivial sin necesidad de ninguna ayuda de conversión de formato que se describe en la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-129">Formats that descend from DXGI\_FORMAT\_R32\_TYPELESS, such as DXGI\_FORMAT\_R32\_FLOAT, are trivially supported without requiring any of the format conversion help that is described in the following sequence.</span></span>

<span data-ttu-id="f0c0a-130">**Para realizar la edición de imágenes en contexto**</span><span class="sxs-lookup"><span data-stu-id="f0c0a-130">**To perform in-place image editing**</span></span>

1.  <span data-ttu-id="f0c0a-131">Cree una textura con el formato dependiente sin tipos que se especifica en el escenario anterior, junto con las marcas de enlace necesarias, como D3D11 \_ enlace \_ Unordered \_ Access \| D3D11 \_ Binder \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f0c0a-131">Create a texture with the appropriate TYPELESS-dependent format that is specified in the previous scenario together with the required bind flags, such as D3D11\_BIND\_UNORDERED\_ACCESS \| D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
2.  <span data-ttu-id="f0c0a-132">Para la edición de imágenes en contexto, cree un UAV con el formato de DXGI \_ formato \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-132">For in-place image editing, create a UAV with the DXGI\_FORMAT\_R32\_UINT format.</span></span> <span data-ttu-id="f0c0a-133">La API de Direct3D 11 normalmente no permite la conversión entre "familias" de formato diferente.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-133">The Direct3D 11 API typically does not allow casting between different format "families."</span></span> <span data-ttu-id="f0c0a-134">Sin embargo, la API de Direct3D 11 realiza una excepción con el formato de DXGI \_ format \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-134">However, the Direct3D 11 API makes an exception with the DXGI\_FORMAT\_R32\_UINT format.</span></span>
3.  <span data-ttu-id="f0c0a-135">En el sombreador de cálculo o el sombreador de píxeles, use las funciones adecuadas de paquete de formato insertado y desempaquetado que se proporcionan en el \_ archivo D3DX DXGIFormatConvert. INL.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-135">In the compute shader or pixel shader, use the appropriate inline format pack and unpack functions that are provided in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="f0c0a-136">Por ejemplo, supongamos que el \_ formato \_ de dxgi R32 \_ uint UAV de la textura realmente contiene \_ \_ \_ datos con formato de dxgi R10G10B10A2 UNORM.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-136">For example, suppose the DXGI\_FORMAT\_R32\_UINT UAV of the texture really holds DXGI\_FORMAT\_R10G10B10A2\_UNORM-formatted data.</span></span> <span data-ttu-id="f0c0a-137">Una vez que la aplicación Lee un uint de UAV en el sombreador, debe llamar a la función siguiente para desempaquetar el formato de textura:</span><span class="sxs-lookup"><span data-stu-id="f0c0a-137">After the application reads a uint from the UAV into the shader, it must call the following function to unpack the texture format:</span></span>

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    <span data-ttu-id="f0c0a-138">Después, para escribir en el UAV en el mismo sombreador, la aplicación llama a la función siguiente para empaquetar los datos del sombreador en un valor uint que la aplicación puede escribir en UAV:</span><span class="sxs-lookup"><span data-stu-id="f0c0a-138">Then, to write to the UAV in the same shader, the application calls the following function to pack shader data into a uint that the application can write to the UAV:</span></span>

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  <span data-ttu-id="f0c0a-139">A continuación, la aplicación puede crear otras vistas, como SRVs, con el formato requerido.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-139">The application can then create other views, such as SRVs, with the required format.</span></span> <span data-ttu-id="f0c0a-140">Por ejemplo, la aplicación puede crear un SRV con el formato de DXGI \_ formato \_ R10G10B10A2 \_ UNORM si el recurso se creó como \_ formato de dxgi \_ R10G10B10A2 \_ sin tipo.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-140">For example, the application can create a SRV with the DXGI\_FORMAT\_R10G10B10A2\_UNORM format if the resource was created as DXGI\_FORMAT\_R10G10B10A2\_TYPELESS.</span></span> <span data-ttu-id="f0c0a-141">Cuando un sombreador accede a ese SRV, el hardware puede realizar la conversión automática de tipos como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-141">When a shader accesses that SRV, the hardware can perform automatic type conversion as usual.</span></span>

> [!Note]  
> <span data-ttu-id="f0c0a-142">Si el sombreador debe escribir solo en un UAV o leer como un SRV, no es necesario ninguno de estos trabajos de conversión porque puede usar UAVs o SRVs totalmente tipados.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-142">If the shader must write only to a UAV, or read as an SRV, none of this conversion work is needed because you can use fully typed UAVs or SRVs.</span></span> <span data-ttu-id="f0c0a-143">Las funciones de conversión de formato proporcionadas en D3DX \_ DXGIFormatConvert. INL solo son útiles si desea realizar operaciones de lectura y escritura simultáneas en una UAV de una textura.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-143">The format conversion functions provided in D3DX\_DXGIFormatConvert.inl are potentially useful only if you want to perform simultaneous reading from and writing to a UAV of a texture.</span></span>

 

<span data-ttu-id="f0c0a-144">A continuación se muestra la lista de funciones de conversión de formato que se incluyen en el \_ archivo D3DX DXGIFormatConvert. INL.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-144">The following is the list of format conversion functions that are included in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="f0c0a-145">Estas funciones se clasifican por el formato de DXGI \_ que desempaquetan y empaquetan.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-145">These functions are categorized by the DXGI\_FORMAT that they unpack and pack.</span></span> <span data-ttu-id="f0c0a-146">Cada uno de los formatos admitidos desciende de uno de los formatos sin tipo enumerados en el escenario anterior y admite la conversión al formato de DXGI \_ \_ R32 \_ uint como UAV.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-146">Each of the supported formats descends from one of the TYPELESS formats listed in the preceding scenario and supports casting to DXGI\_FORMAT\_R32\_UINT as a UAV.</span></span>

<dl> <dt>

<span data-ttu-id="f0c0a-147"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>Formato de DXGI \_ \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f0c0a-147"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-148"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>Formato de DXGI \_ \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="f0c0a-148"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-149"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f0c0a-149"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-150"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="f0c0a-150"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="f0c0a-151">La \_ función de tipo inexacto usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-151">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="f0c0a-152">La función alternativa utiliza una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión de punto flotante de SRGB->exacta.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-152">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="f0c0a-153"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="f0c0a-153"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-154"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="f0c0a-154"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-155"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="f0c0a-155"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-156"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f0c0a-156"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-157"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="f0c0a-157"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="f0c0a-158">La \_ función de tipo inexacto usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-158">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="f0c0a-159">La función alternativa utiliza una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión de punto flotante de SRGB->exacta.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-159">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="f0c0a-160"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f0c0a-160"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-161"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="f0c0a-161"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="f0c0a-162">La \_ función de tipo inexacto usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-162">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="f0c0a-163">La función alternativa utiliza una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión de punto flotante de SRGB->exacta.</span><span class="sxs-lookup"><span data-stu-id="f0c0a-163">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="f0c0a-164"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>Formato de DXGI \_ \_ R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="f0c0a-164"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI\_FORMAT\_R16G16\_FLOAT</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-165"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>Formato de DXGI \_ \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="f0c0a-165"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI\_FORMAT\_R16G16\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-166"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>Formato de DXGI \_ \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="f0c0a-166"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI\_FORMAT\_R16G16\_UINT</span></span>
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-167"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>Formato de DXGI \_ \_ R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="f0c0a-167"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI\_FORMAT\_R16G16\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="f0c0a-168"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>Formato de DXGI \_ \_ R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="f0c0a-168"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI\_FORMAT\_R16G16\_SINT</span></span>
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f0c0a-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f0c0a-169">Related Topics</span></span>

[<span data-ttu-id="f0c0a-170">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="f0c0a-170">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="f0c0a-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f0c0a-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0c0a-172">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="f0c0a-172">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 





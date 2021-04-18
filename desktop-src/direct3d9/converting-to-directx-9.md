---
description: Se cambiaron las siguientes características en Microsoft Direct3D 9. Si usa estas características, consulte los cambios que se enumeran a continuación para ayudarle a migrar la aplicación a Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Convertir a Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714861"
---
# <a name="converting-to-direct3d-9"></a><span data-ttu-id="feab0-104">Convertir a Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="feab0-104">Converting to Direct3D 9</span></span>

<span data-ttu-id="feab0-105">Se cambiaron las siguientes características en Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="feab0-105">The following features were changed in Microsoft Direct3D 9.</span></span> <span data-ttu-id="feab0-106">Si usa estas características, consulte los cambios que se enumeran a continuación para ayudarle a migrar la aplicación a Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="feab0-106">If you are using these features, see the changes listed below to help you port your application to Direct3D 9.</span></span>

-   [<span data-ttu-id="feab0-107">BaseVertexIndex cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-107">BaseVertexIndex Changes</span></span>](#basevertexindex-changes)
-   [<span data-ttu-id="feab0-108">CreateImageSurface cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-108">CreateImageSurface Changes</span></span>](#createimagesurface-changes)
-   [<span data-ttu-id="feab0-109">D3DENUM \_ sin \_ cambios en el nivel de WHQL \_</span><span class="sxs-lookup"><span data-stu-id="feab0-109">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>](/windows)
-   [<span data-ttu-id="feab0-110">Crear cambios de recursos</span><span class="sxs-lookup"><span data-stu-id="feab0-110">Create Resource Changes</span></span>](#create-resource-changes)
-   [<span data-ttu-id="feab0-111">EnumAdapterModes cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-111">EnumAdapterModes Changes</span></span>](#enumadaptermodes-changes)
-   [<span data-ttu-id="feab0-112">Cambios de Get/SetStreamSource \_</span><span class="sxs-lookup"><span data-stu-id="feab0-112">Get/SetStreamSource\_Changes</span></span>](#getsetstreamsource-changes)
-   [<span data-ttu-id="feab0-113">Cambios de calidad de muestreo múltiple</span><span class="sxs-lookup"><span data-stu-id="feab0-113">Multisampling Quality Changes</span></span>](#multisampling-quality-changes)
-   [<span data-ttu-id="feab0-114">ResourceManagerDiscardBytes cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-114">ResourceManagerDiscardBytes Changes</span></span>](#resourcemanagerdiscardbytes-changes)
-   [<span data-ttu-id="feab0-115">SetSoftwareVertexProcessing cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-115">SetSoftwareVertexProcessing Changes</span></span>](#setsoftwarevertexprocessing-changes)
-   [<span data-ttu-id="feab0-116">Cambios de la muestra de textura</span><span class="sxs-lookup"><span data-stu-id="feab0-116">Texture Sampler Changes</span></span>](#texture-sampler-changes)
-   [<span data-ttu-id="feab0-117">Cambios en la declaración de vértices</span><span class="sxs-lookup"><span data-stu-id="feab0-117">Vertex Declaration Changes</span></span>](#vertex-declaration-changes)
-   [<span data-ttu-id="feab0-118">Intervalos \_ y \_ cambios de SwapEffects \_</span><span class="sxs-lookup"><span data-stu-id="feab0-118">Intervals,\_and\_SwapEffects\_Changes</span></span>](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a><span data-ttu-id="feab0-119">BaseVertexIndex cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-119">BaseVertexIndex Changes</span></span>

<span data-ttu-id="feab0-120">En DirectX 8. x, IDirect3DDevice8:: SetIndices requería un puntero al búfer de índice y un BaseVertexIndex para la posición inicial en el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="feab0-120">In DirectX 8.x, IDirect3DDevice8::SetIndices required a pointer to the index buffer and a BaseVertexIndex for the starting position in the vertex buffer.</span></span> <span data-ttu-id="feab0-121">Una aplicación que procesa por lotes objetos diferentes en el búfer de vértices tenía que cambiar el búfer de índice (o realizar una llamada a IDirect3DDevice8:: SetIndices) antes de llamar a IDirect3DDevice8::D rawIndexedPrimitive.</span><span class="sxs-lookup"><span data-stu-id="feab0-121">An application batching different objects into the vertex buffer had to switch the index buffer (or make a call to IDirect3DDevice8::SetIndices) before calling IDirect3DDevice8::DrawIndexedPrimitive.</span></span>

<span data-ttu-id="feab0-122">En Direct3D 9, la posición inicial en el búfer de vértices, *BaseVertexIndex*, se ha pasado a IDirect3DDevice9::D rawindexedprimitive y su tipo de datos ha cambiado de DWORD a int.</span><span class="sxs-lookup"><span data-stu-id="feab0-122">In Direct3D 9, the starting position in the vertex buffer, *BaseVertexIndex*, has been moved to IDirect3DDevice9::DrawIndexedPrimitive, and its data type changed from a DWORD to an INT.</span></span>


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a><span data-ttu-id="feab0-123">CreateImageSurface cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-123">CreateImageSurface Changes</span></span>

<span data-ttu-id="feab0-124">IDirect3DDevice8:: CreateImageSurface ha cambiado el nombre de [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span><span class="sxs-lookup"><span data-stu-id="feab0-124">IDirect3DDevice8::CreateImageSurface was renamed [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span></span> <span data-ttu-id="feab0-125">Se ha agregado un parámetro adicional que toma un tipo D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="feab0-125">An additional parameter that takes a D3DPOOL type was added.</span></span> <span data-ttu-id="feab0-126">D3DPOOL \_ Scratch devolverá una superficie que tiene características idénticas a una superficie creada por IDirect3DDevice8:: CreateImageSurface.</span><span class="sxs-lookup"><span data-stu-id="feab0-126">D3DPOOL\_SCRATCH will return a surface that has identical characteristics to a surface created by IDirect3DDevice8::CreateImageSurface.</span></span> <span data-ttu-id="feab0-127">D3DPOOL \_ default es el grupo adecuado para su uso con [**StretchRect**](/windows/desktop/api) y [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span><span class="sxs-lookup"><span data-stu-id="feab0-127">D3DPOOL\_DEFAULT is the appropriate pool for use with [**StretchRect**](/windows/desktop/api) and [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span></span>

## <a name="d3denum_no_whql_level-changes"></a><span data-ttu-id="feab0-128">D3DENUM \_ sin \_ cambios en el nivel de WHQL \_</span><span class="sxs-lookup"><span data-stu-id="feab0-128">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>

<span data-ttu-id="feab0-129">Ahora, las aplicaciones tienen que solicitar explícitamente los laboratorios de calidad de hardware de Microsoft Windows (WHQL), ya que la respuesta tarda un tiempo relativamente largo (unos segundos).</span><span class="sxs-lookup"><span data-stu-id="feab0-129">Applications now have to explicitly ask for the Microsoft Windows Hardware Quality Labs (WHQL) because the response takes relatively long (a few seconds).</span></span> <span data-ttu-id="feab0-130">D3DENUM \_ no se ha \_ \_ quitado el nivel de WHQL y se ha agregado el nivel de WHQL de D3DENUM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="feab0-130">D3DENUM\_NO\_WHQL\_LEVEL has been removed and D3DENUM\_WHQL\_LEVEL has been added.</span></span>

## <a name="create-resource-changes"></a><span data-ttu-id="feab0-131">Crear cambios de recursos</span><span class="sxs-lookup"><span data-stu-id="feab0-131">Create Resource Changes</span></span>

<span data-ttu-id="feab0-132">Se ha agregado un identificador a varios métodos y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="feab0-132">A handle has been added to several methods and should be set to **NULL**.</span></span> <span data-ttu-id="feab0-133">Los métodos afectados incluyen:</span><span class="sxs-lookup"><span data-stu-id="feab0-133">The methods affected include:</span></span>

-   [<span data-ttu-id="feab0-134">**CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="feab0-134">**CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="feab0-135">**CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="feab0-135">**CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [<span data-ttu-id="feab0-136">**CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="feab0-136">**CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="feab0-137">**CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="feab0-137">**CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [<span data-ttu-id="feab0-138">**CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="feab0-138">**CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [<span data-ttu-id="feab0-139">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="feab0-139">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [<span data-ttu-id="feab0-140">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="feab0-140">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="feab0-141">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="feab0-141">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a><span data-ttu-id="feab0-142">EnumAdapterModes cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-142">EnumAdapterModes Changes</span></span>

<span data-ttu-id="feab0-143">[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) Now toma D3DFORMAT.</span><span class="sxs-lookup"><span data-stu-id="feab0-143">The [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) now takes a D3DFORMAT.</span></span>


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



<span data-ttu-id="feab0-144">El formato admite un conjunto expandido de modos de presentación.</span><span class="sxs-lookup"><span data-stu-id="feab0-144">The format supports an expanding set of display modes.</span></span> <span data-ttu-id="feab0-145">Para proteger las aplicaciones de los formatos que no se inventaron cuando se envió la aplicación, la aplicación debe indicar a Direct3D el formato de los modos de presentación que se deben enumerar.</span><span class="sxs-lookup"><span data-stu-id="feab0-145">To protect applications from enumerating formats that were not invented when the application shipped, the application must tell Direct3D the format for the display modes that should be enumerated.</span></span> <span data-ttu-id="feab0-146">La matriz de modos de presentación resultante solo variará en función del ancho, el alto y la frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="feab0-146">The resulting array of display modes will differ only by width, height, and refresh rate.</span></span>

<span data-ttu-id="feab0-147">La aplicación especifica un formato de píxel y la enumeración está restringida a los modos de presentación que coinciden exactamente con el formato.</span><span class="sxs-lookup"><span data-stu-id="feab0-147">The application specifies a pixel format and the enumeration is restricted to those display modes that exactly match the format.</span></span> <span data-ttu-id="feab0-148">A continuación se muestra una lista de los formatos permitidos:</span><span class="sxs-lookup"><span data-stu-id="feab0-148">The following is a list of the allowed formats:</span></span>

-   <span data-ttu-id="feab0-149">D3DFMT \_ A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="feab0-149">D3DFMT\_A1R5G5B5</span></span>
-   <span data-ttu-id="feab0-150">D3DFMT \_ A2B10G10R10</span><span class="sxs-lookup"><span data-stu-id="feab0-150">D3DFMT\_A2B10G10R10</span></span>
-   <span data-ttu-id="feab0-151">D3DFMT \_ A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="feab0-151">D3DFMT\_A8R8G8B8</span></span>
-   <span data-ttu-id="feab0-152">D3DFMT \_ R5G6B5</span><span class="sxs-lookup"><span data-stu-id="feab0-152">D3DFMT\_R5G6B5</span></span>
-   <span data-ttu-id="feab0-153">D3DFMT \_ X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="feab0-153">D3DFMT\_X1R5G5B5</span></span>
-   <span data-ttu-id="feab0-154">D3DFMT \_ X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="feab0-154">D3DFMT\_X8R8G8B8</span></span>

<span data-ttu-id="feab0-155">La enumeración es equivalente para las versiones alfa y no Alpha del mismo formato.</span><span class="sxs-lookup"><span data-stu-id="feab0-155">Enumeration is equivalent for alpha and nonalpha versions of the same format.</span></span> <span data-ttu-id="feab0-156">El formato devuelto siempre se rellenará con el mismo formato proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="feab0-156">The returned Format will always be filled with the same format supplied by the application.</span></span>

<span data-ttu-id="feab0-157">Este método trata 565 y 555 como equivalente y devuelve la versión correcta en el formato.</span><span class="sxs-lookup"><span data-stu-id="feab0-157">This method treats 565 and 555 as equivalent, and returns the correct version in the Format.</span></span> <span data-ttu-id="feab0-158">La diferencia solo se produce cuando la aplicación bloquea el búfer de reserva y hay una marca explícita que la aplicación debe establecer para lograrlo.</span><span class="sxs-lookup"><span data-stu-id="feab0-158">The difference comes into play only when the application locks the back buffer, and there is an explicit flag that the application must set in order to accomplish this.</span></span>

## <a name="getsetstreamsource-changes"></a><span data-ttu-id="feab0-159">Cambios de Get/SetStreamSource</span><span class="sxs-lookup"><span data-stu-id="feab0-159">Get/SetStreamSource Changes</span></span>

<span data-ttu-id="feab0-160">Se ha agregado un parámetro a los métodos [**GetStreamSource**](/windows/desktop/api) y [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) .</span><span class="sxs-lookup"><span data-stu-id="feab0-160">One parameter has been added to the [**GetStreamSource**](/windows/desktop/api) and [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) methods.</span></span> <span data-ttu-id="feab0-161">El desplazamiento es el número de bytes entre el principio de la secuencia y el principio de los datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="feab0-161">The offset is the number of bytes between the beginning of the stream and the beginning of the vertex data.</span></span> <span data-ttu-id="feab0-162">Se mide en bytes.</span><span class="sxs-lookup"><span data-stu-id="feab0-162">It is measured in bytes.</span></span> <span data-ttu-id="feab0-163">Esto permite que la canalización admita desplazamientos de flujo.</span><span class="sxs-lookup"><span data-stu-id="feab0-163">This enables the pipeline to support stream offsets.</span></span> <span data-ttu-id="feab0-164">Para averiguar si el dispositivo admite desplazamientos de flujo, consulte D3DDEVCAPS2 \_ STREAMOFFSET.</span><span class="sxs-lookup"><span data-stu-id="feab0-164">To find out if the device supports stream offsets, see D3DDEVCAPS2\_STREAMOFFSET.</span></span>


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a><span data-ttu-id="feab0-165">Cambios de calidad de muestreo múltiple</span><span class="sxs-lookup"><span data-stu-id="feab0-165">Multisampling Quality Changes</span></span>

<span data-ttu-id="feab0-166">Anteriormente, solo había una \_ enumeración de tipo D3DMULTISAMPLE.</span><span class="sxs-lookup"><span data-stu-id="feab0-166">Previously, there was only the D3DMULTISAMPLE\_TYPE enumeration.</span></span> <span data-ttu-id="feab0-167">Direct3D 9 conserva esta enumeración y agrega la idea de un nivel de calidad para cada elemento de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="feab0-167">Direct3D 9 retains this enumeration and adds the idea of a quality level for each element of the enumeration.</span></span> <span data-ttu-id="feab0-168">El nivel de calidad indica un equilibrio entre la calidad visual y el rendimiento indicando el número de muestras Enmascarables (en el sentido de D3DRS \_ MULTISAMPLEMASK).</span><span class="sxs-lookup"><span data-stu-id="feab0-168">The quality level indicates a trade-off between visual quality and performance by indicating the number of maskable samples (in the sense of D3DRS\_MULTISAMPLEMASK).</span></span>

<span data-ttu-id="feab0-169">Una aplicación debe elegir el número de ejemplos Enmascarables que requiera y, a continuación, consultar pQualityLevels.</span><span class="sxs-lookup"><span data-stu-id="feab0-169">An application should choose how many maskable samples it requires, and then consult pQualityLevels.</span></span> <span data-ttu-id="feab0-170">Si es distinto de cero, este valor indica el número de niveles de calidad que la aplicación puede pasar a las distintas funciones de creación a través de MultiSampleQuality.</span><span class="sxs-lookup"><span data-stu-id="feab0-170">If nonzero, this value indicates the number of quality levels the application can pass to the various creation functions through MultiSampleQuality.</span></span> <span data-ttu-id="feab0-171">Dado que los controladores exponen todos los esquemas de ejemplo múltiple como niveles de calidad en D3DMULTISAMPLE \_ no enmascarable, puede enumerar todos los esquemas de muestreo múltiple disponibles a través de este tipo si la aplicación no necesita enmascarar los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="feab0-171">Because drivers expose all their multisample schemes as quality levels at D3DMULTISAMPLE\_NONMASKABLE, you can enumerate all available multisampling schemes through this one type if your application does not need to mask samples.</span></span>

<span data-ttu-id="feab0-172">Se ha \_ retirado el bit de Cap de STRETCHBLTMULTISAMPLE de D3DPRASTERCAPS.</span><span class="sxs-lookup"><span data-stu-id="feab0-172">The D3DPRASTERCAPS\_STRETCHBLTMULTISAMPLE caps bit has been retired.</span></span> <span data-ttu-id="feab0-173">Este bit se usa para indicar que el método de muestreo múltiple no admitía máscaras de escritura y no se podía activar y desactivar entre [**BeginScene**](/windows/desktop/api) y [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span><span class="sxs-lookup"><span data-stu-id="feab0-173">This bit used to mean that the multisampling method did not support write masks, and could not be toggled on and off between [**BeginScene**](/windows/desktop/api) and [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span></span> <span data-ttu-id="feab0-174">Estos métodos no Enmascarables ahora se exponen a través de D3DMULTISAMPLE no \_ enmascarable.</span><span class="sxs-lookup"><span data-stu-id="feab0-174">Such nonmaskable methods are now exposed through D3DMULTISAMPLE\_NONMASKABLE.</span></span>


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



<span data-ttu-id="feab0-175">Existe un máximo diferente para cada número de muestras Enmascarables.</span><span class="sxs-lookup"><span data-stu-id="feab0-175">There is a different maximum for each number of maskable samples.</span></span> <span data-ttu-id="feab0-176">Por ejemplo, \_ los ejemplos de D3DMULTISAMPLE 4 \_ podrían tener tres niveles de calidad, mientras que los de D3DMULTISAMPLE \_ 2 \_ pueden tener solo uno.</span><span class="sxs-lookup"><span data-stu-id="feab0-176">For example, D3DMULTISAMPLE\_4\_SAMPLES might have three levels of quality, while D3DMULTISAMPLE\_2\_SAMPLES might have only one.</span></span> <span data-ttu-id="feab0-177">Hay ocho niveles de calidad como máximo para cada número de muestras Enmascarables (el controlador no puede expresar más).</span><span class="sxs-lookup"><span data-stu-id="feab0-177">There are at most eight levels of quality for each number of maskable samples (the driver is not allowed to express more).</span></span> <span data-ttu-id="feab0-178">La calidad oscila entre cero y ( \* pQualityLevels-1).</span><span class="sxs-lookup"><span data-stu-id="feab0-178">The quality ranges from zero to (\*pQualityLevels - 1).</span></span>

## <a name="resourcemanagerdiscardbytes-changes"></a><span data-ttu-id="feab0-179">ResourceManagerDiscardBytes cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-179">ResourceManagerDiscardBytes Changes</span></span>

<span data-ttu-id="feab0-180">ResourceManagerDiscardBytes se ha reemplazado por IDirect3DDevice9:: EvictManagedResources.</span><span class="sxs-lookup"><span data-stu-id="feab0-180">ResourceManagerDiscardBytes has been replaced by IDirect3DDevice9::EvictManagedResources.</span></span> <span data-ttu-id="feab0-181">Puede expulsar todos los recursos, tanto Direct3D como los recursos de controlador.</span><span class="sxs-lookup"><span data-stu-id="feab0-181">It can evict all resources, both Direct3D and driver resources.</span></span>

<span data-ttu-id="feab0-182">Ahora se consulta al administrador de recursos cuando un recurso (ya sea administrado o no administrado) produce un error en la creación porque no hay suficiente memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="feab0-182">The resource manager is now consulted when a resource (whether managed or nonmanaged) fails creation because there is insufficient video memory.</span></span> <span data-ttu-id="feab0-183">Se pedirá automáticamente al administrador que libere suficientes recursos para que la creación se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="feab0-183">The manager will automatically be asked to free enough resources for the creation to succeed.</span></span> <span data-ttu-id="feab0-184">En DirectX 8,0, no se trata de un proceso automatizado.</span><span class="sxs-lookup"><span data-stu-id="feab0-184">In DirectX 8.0, this was not an automated process.</span></span>

## <a name="setsoftwarevertexprocessing-changes"></a><span data-ttu-id="feab0-185">SetSoftwareVertexProcessing cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-185">SetSoftwareVertexProcessing Changes</span></span>

<span data-ttu-id="feab0-186">Una aplicación puede crear un dispositivo en modo mixto para usar el procesamiento de vértices de software y hardware.</span><span class="sxs-lookup"><span data-stu-id="feab0-186">An application can create a mixed-mode device to use software and hardware vertex processing.</span></span>

<span data-ttu-id="feab0-187">Para cambiar entre los dos modos de procesamiento de vértices en DirectX 8. x, llame a IDirect3DDevice8:: SetRenderState.</span><span class="sxs-lookup"><span data-stu-id="feab0-187">To switch between the two vertex processing modes in DirectX 8.x, call IDirect3DDevice8::SetRenderState.</span></span> <span data-ttu-id="feab0-188">Esto se ha sustituido por [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) para facilitar los problemas causados por los bloques de estado.</span><span class="sxs-lookup"><span data-stu-id="feab0-188">This has been replaced with [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) to ease problems caused by state blocks.</span></span> <span data-ttu-id="feab0-189">Este nuevo método no está registrado por los bloques de estado.</span><span class="sxs-lookup"><span data-stu-id="feab0-189">This new method is not recorded by state blocks.</span></span>

## <a name="texture-sampler-changes"></a><span data-ttu-id="feab0-190">Cambios de la muestra de textura</span><span class="sxs-lookup"><span data-stu-id="feab0-190">Texture Sampler Changes</span></span>

<span data-ttu-id="feab0-191">Direct3D 9 admite hasta dieciséis superficies de textura en un solo paso mediante el modelo de sombreador de píxeles 2 \_ 0; sin embargo, el número de coordenadas de textura permanece limitado a ocho.</span><span class="sxs-lookup"><span data-stu-id="feab0-191">Direct3D 9 supports up to sixteen texture surfaces in one pass using the pixel shader 2\_0 model; however, the number of texture coordinates remains limited to eight.</span></span> <span data-ttu-id="feab0-192">El estado de la fase de textura está asociado a las superficies, los conjuntos de coordenadas, el procesamiento de vértices y el procesamiento de píxeles.</span><span class="sxs-lookup"><span data-stu-id="feab0-192">Texture stage state is associated with surfaces, coordinate sets, vertex processing, and pixel processing.</span></span> <span data-ttu-id="feab0-193">Para administrar estas diferencias en tiempo de compilación, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) se ha dividido en dos métodos:</span><span class="sxs-lookup"><span data-stu-id="feab0-193">To manage these differences at compile time, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) has been broken into two methods:</span></span>

-   <span data-ttu-id="feab0-194">IDirect3DDevice9:: SetTextureStageState se seguirá usando para el estado de coordenadas de textura, como los modos de ajuste y la generación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="feab0-194">IDirect3DDevice9::SetTextureStageState will still be used for texture coordinate state, such as wrap modes and texture coordinate generation.</span></span>
-   <span data-ttu-id="feab0-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) se ha agregado y ahora se usará para filtrar, colocar en mosaicos, adfijar, MIPLOD, etc.</span><span class="sxs-lookup"><span data-stu-id="feab0-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) has been added and will now be used for filtering, tiling, clamping, MIPLOD, and so forth.</span></span> <span data-ttu-id="feab0-196">Esto funcionará para hasta dieciséis muestreadores.</span><span class="sxs-lookup"><span data-stu-id="feab0-196">This will work for up to sixteen samplers.</span></span>

### <a name="settexturestagestate-changes"></a><span data-ttu-id="feab0-197">SetTextureStageState cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-197">SetTextureStageState Changes</span></span>

<span data-ttu-id="feab0-198">IDirect3DDevice9:: SetTextureStageState ahora establece los siguientes Estados:</span><span class="sxs-lookup"><span data-stu-id="feab0-198">IDirect3DDevice9::SetTextureStageState now sets the following states:</span></span>

-   <span data-ttu-id="feab0-199">Estado de procesamiento de vértice de función fija.</span><span class="sxs-lookup"><span data-stu-id="feab0-199">Fixed function vertex processing state.</span></span> <span data-ttu-id="feab0-200">Este estado controla la manipulación de las coordenadas de textura D3DTSS \_ TEXTURETRANSFORMFLAGS y D3DTSS \_ TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="feab0-200">This state controls the manipulation of texture coordinates D3DTSS\_TEXTURETRANSFORMFLAGS and D3DTSS\_TEXCOORDINDEX.</span></span> <span data-ttu-id="feab0-201">Se pueden establecer hasta ocho de cada uno (dado que se admiten ocho coordenadas de textura siempre).</span><span class="sxs-lookup"><span data-stu-id="feab0-201">Up to eight of each can be set (because eight texture coordinates are always supported).</span></span> <span data-ttu-id="feab0-202">D3DTSS \_ TEXCOORDINDEX es un estado de procesamiento de vértice de función fijo.</span><span class="sxs-lookup"><span data-stu-id="feab0-202">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="feab0-203">Si se usa un sombreador de vértices programable, se omite este estado.</span><span class="sxs-lookup"><span data-stu-id="feab0-203">If a programmable vertex shader is used, this state is ignored.</span></span>
-   <span data-ttu-id="feab0-204">Estado del sombreador de píxeles de función fija (el TextureStageState heredado).</span><span class="sxs-lookup"><span data-stu-id="feab0-204">Fixed function pixel shader state (the legacy TextureStageState).</span></span>

    -   <span data-ttu-id="feab0-205">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="feab0-205">D3DTSS\_ALPHAARG0</span></span>
    -   <span data-ttu-id="feab0-206">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="feab0-206">D3DTSS\_ALPHAARG1</span></span>
    -   <span data-ttu-id="feab0-207">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="feab0-207">D3DTSS\_ALPHAARG2</span></span>
    -   <span data-ttu-id="feab0-208">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="feab0-208">D3DTSS\_ALPHAOP</span></span>
    -   <span data-ttu-id="feab0-209">D3DTSS \_ BUMPENVLOFFSET</span><span class="sxs-lookup"><span data-stu-id="feab0-209">D3DTSS\_BUMPENVLOFFSET</span></span>
    -   <span data-ttu-id="feab0-210">D3DTSS \_ BUMPENVLSCALE</span><span class="sxs-lookup"><span data-stu-id="feab0-210">D3DTSS\_BUMPENVLSCALE</span></span>
    -   <span data-ttu-id="feab0-211">D3DTSS \_ BUMPENVMAT00</span><span class="sxs-lookup"><span data-stu-id="feab0-211">D3DTSS\_BUMPENVMAT00</span></span>
    -   <span data-ttu-id="feab0-212">D3DTSS \_ BUMPENVMAT01</span><span class="sxs-lookup"><span data-stu-id="feab0-212">D3DTSS\_BUMPENVMAT01</span></span>
    -   <span data-ttu-id="feab0-213">D3DTSS \_ BUMPENVMAT10</span><span class="sxs-lookup"><span data-stu-id="feab0-213">D3DTSS\_BUMPENVMAT10</span></span>
    -   <span data-ttu-id="feab0-214">D3DTSS \_ BUMPENVMAT11</span><span class="sxs-lookup"><span data-stu-id="feab0-214">D3DTSS\_BUMPENVMAT11</span></span>
    -   <span data-ttu-id="feab0-215">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="feab0-215">D3DTSS\_COLORARG0</span></span>
    -   <span data-ttu-id="feab0-216">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="feab0-216">D3DTSS\_COLORARG1</span></span>
    -   <span data-ttu-id="feab0-217">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="feab0-217">D3DTSS\_COLORARG2</span></span>
    -   <span data-ttu-id="feab0-218">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="feab0-218">D3DTSS\_COLOROP</span></span>
    -   <span data-ttu-id="feab0-219">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="feab0-219">D3DTSS\_RESULTARG</span></span>

    <span data-ttu-id="feab0-220">El número de Estados de sombreador de píxeles de función fija que se pueden establecer es menor o igual que el número representado por MaxTextureBlendStages.</span><span class="sxs-lookup"><span data-stu-id="feab0-220">The number of fixed function pixel shader states that can be set is less than or equal to the number represented by MaxTextureBlendStages.</span></span>

<span data-ttu-id="feab0-221">El número de muestras de textura disponibles para la aplicación viene determinado por la versión del sombreador de píxeles, como se indica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="feab0-221">The number of texture samplers available to the application is determined by the pixel shader version, as indicated in the following table.</span></span>



| <span data-ttu-id="feab0-222">Nombre</span><span class="sxs-lookup"><span data-stu-id="feab0-222">Name</span></span>                    | <span data-ttu-id="feab0-223">Number</span><span class="sxs-lookup"><span data-stu-id="feab0-223">Number</span></span>                                                         |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="feab0-224">PS \_ 1 \_ 1 a PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="feab0-224">ps\_1\_1 to ps\_1\_3</span></span>    | <span data-ttu-id="feab0-225">4 muestras de texturas</span><span class="sxs-lookup"><span data-stu-id="feab0-225">4 texture samplers</span></span>                                             |
| <span data-ttu-id="feab0-226">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="feab0-226">ps\_1\_4</span></span>                | <span data-ttu-id="feab0-227">6 muestras de texturas</span><span class="sxs-lookup"><span data-stu-id="feab0-227">6 texture samplers</span></span>                                             |
| <span data-ttu-id="feab0-228">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="feab0-228">ps\_2\_0</span></span>                | <span data-ttu-id="feab0-229">16 muestras de texturas</span><span class="sxs-lookup"><span data-stu-id="feab0-229">16 texture samplers</span></span>                                            |
| <span data-ttu-id="feab0-230">canalización de funciones fijas</span><span class="sxs-lookup"><span data-stu-id="feab0-230">fixed function pipeline</span></span> | <span data-ttu-id="feab0-231">Muestras de textura de MaxTextureBlendStages/MaxSimultaneousTextures</span><span class="sxs-lookup"><span data-stu-id="feab0-231">MaxTextureBlendStages/MaxSimultaneousTextures texture samplers</span></span> |



 

<span data-ttu-id="feab0-232">Los dispositivos que admiten la asignación de desplazamiento en Direct3D 9 serán compatibles con una muestra adicional (D3DDMAPSAMPLER), que muestrea los mapas de desplazamiento en la unidad del teselador.</span><span class="sxs-lookup"><span data-stu-id="feab0-232">Devices that support displacement mapping in Direct3D 9 will support an additional sampler (D3DDMAPSAMPLER), which samples the displacement maps in the tessellator unit.</span></span>

### <a name="setsamplerstate-changes"></a><span data-ttu-id="feab0-233">SetSamplerState cambios</span><span class="sxs-lookup"><span data-stu-id="feab0-233">SetSamplerState Changes</span></span>

<span data-ttu-id="feab0-234">IDirect3DDevice9:: SetSamplerState establece el estado de la muestra (incluido el usado en la unidad del teselador en los mapas de desplazamiento de ejemplo).</span><span class="sxs-lookup"><span data-stu-id="feab0-234">IDirect3DDevice9::SetSamplerState sets the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="feab0-235">Se les ha cambiado el nombre con un \_ prefijo D3DSAMP para habilitar la detección de errores en tiempo de compilación al migrar desde DirectX 8. x.</span><span class="sxs-lookup"><span data-stu-id="feab0-235">These have been renamed with a D3DSAMP\_ prefix to enable compile-time error detection when porting from DirectX 8.x.</span></span> <span data-ttu-id="feab0-236">Los Estados incluyen:</span><span class="sxs-lookup"><span data-stu-id="feab0-236">The states include:</span></span>

-   <span data-ttu-id="feab0-237">D3DSAMP \_ ADDRESSU</span><span class="sxs-lookup"><span data-stu-id="feab0-237">D3DSAMP\_ADDRESSU</span></span>
-   <span data-ttu-id="feab0-238">D3DSAMP \_ ADDRESSV</span><span class="sxs-lookup"><span data-stu-id="feab0-238">D3DSAMP\_ADDRESSV</span></span>
-   <span data-ttu-id="feab0-239">D3DSAMP \_ ADDRESSW</span><span class="sxs-lookup"><span data-stu-id="feab0-239">D3DSAMP\_ADDRESSW</span></span>
-   <span data-ttu-id="feab0-240">D3DSAMP \_ BORDERCOLOR</span><span class="sxs-lookup"><span data-stu-id="feab0-240">D3DSAMP\_BORDERCOLOR</span></span>
-   <span data-ttu-id="feab0-241">D3DSAMP \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="feab0-241">D3DSAMP\_MAGFILTER</span></span>
-   <span data-ttu-id="feab0-242">D3DSAMP \_ MAXANISOTROPY</span><span class="sxs-lookup"><span data-stu-id="feab0-242">D3DSAMP\_MAXANISOTROPY</span></span>
-   <span data-ttu-id="feab0-243">D3DSAMP \_ MAXMIPLEVEL</span><span class="sxs-lookup"><span data-stu-id="feab0-243">D3DSAMP\_MAXMIPLEVEL</span></span>
-   <span data-ttu-id="feab0-244">D3DSAMP \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="feab0-244">D3DSAMP\_MINFILTER</span></span>
-   <span data-ttu-id="feab0-245">D3DSAMP \_ MIPFILTER</span><span class="sxs-lookup"><span data-stu-id="feab0-245">D3DSAMP\_MIPFILTER</span></span>
-   <span data-ttu-id="feab0-246">D3DSAMP \_ MIPMAPLODBIAS</span><span class="sxs-lookup"><span data-stu-id="feab0-246">D3DSAMP\_MIPMAPLODBIAS</span></span>

## <a name="vertex-declaration-changes"></a><span data-ttu-id="feab0-247">Cambios en la declaración de vértices</span><span class="sxs-lookup"><span data-stu-id="feab0-247">Vertex Declaration Changes</span></span>

<span data-ttu-id="feab0-248">Las declaraciones de vértices ahora se desacoplan de la creación del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="feab0-248">Vertex declarations are now decoupled from vertex shader creation.</span></span> <span data-ttu-id="feab0-249">Las declaraciones de vértices ahora usan una interfaz del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="feab0-249">Vertex declarations now use a Component Object Model (COM) interface.</span></span>

<span data-ttu-id="feab0-250">Para DirectX 8. x, las declaraciones de vértices están asociadas a los sombreadores de vértices.</span><span class="sxs-lookup"><span data-stu-id="feab0-250">For DirectX 8.x, vertex declarations are tied to vertex shaders.</span></span>

-   <span data-ttu-id="feab0-251">Para la canalización de función fija, llame a [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) con el código de formato de vértice flexible (FVF) del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="feab0-251">For the fixed function pipeline, call [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) with the flexible vertex format (FVF) code of the vertex buffer.</span></span>
-   <span data-ttu-id="feab0-252">Para los sombreadores de vértices, llame a IDirect3DDevice9:: SetVertexShader con un identificador a un sombreador de vértices creado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="feab0-252">For vertex shaders, call IDirect3DDevice9::SetVertexShader with a handle to a previously create vertex shader.</span></span> <span data-ttu-id="feab0-253">El sombreador incluye una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="feab0-253">The shader includes a vertex declaration.</span></span>

<span data-ttu-id="feab0-254">En Direct3D 9, las declaraciones de vértices se desacoplan de los sombreadores de vértices y se pueden usar con la canalización de función fija o con los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="feab0-254">For Direct3D 9, vertex declarations are decoupled from vertex shaders and they can be used with either the fixed function pipeline or with shaders.</span></span>

-   <span data-ttu-id="feab0-255">Para la canalización de función fija, no es necesario llamar a IDirect3DDevice9:: SetVertexShader.</span><span class="sxs-lookup"><span data-stu-id="feab0-255">For the fixed function pipeline, there is no need to call IDirect3DDevice9::SetVertexShader.</span></span> <span data-ttu-id="feab0-256">Sin embargo, si desea cambiar a la canalización de función fija y ha usado previamente un sombreador de vértices, llame a IDirect3DDevice9:: SetVertexShader (**null**).</span><span class="sxs-lookup"><span data-stu-id="feab0-256">If, however, you want to switch to the fixed function pipeline and have previously used a vertex shader, call IDirect3DDevice9::SetVertexShader(**NULL**).</span></span> <span data-ttu-id="feab0-257">Una vez hecho esto, deberá llamar a [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) para declarar el código FVF.</span><span class="sxs-lookup"><span data-stu-id="feab0-257">When this is done, you will still need to call [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) to declare the FVF code.</span></span>
-   <span data-ttu-id="feab0-258">Al usar sombreadores de vértices, llame a IDirect3DDevice9:: SetVertexShader con el objeto de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="feab0-258">When using vertex shaders, call IDirect3DDevice9::SetVertexShader with the vertex shader object.</span></span> <span data-ttu-id="feab0-259">Además, llame a IDirect3DDevice9:: SetFVF para configurar una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="feab0-259">Additionally, call IDirect3DDevice9::SetFVF to set up a vertex declaration.</span></span> <span data-ttu-id="feab0-260">Usa la información implícita en el FVF.</span><span class="sxs-lookup"><span data-stu-id="feab0-260">This uses the information implicit in the FVF.</span></span> <span data-ttu-id="feab0-261">Se puede llamar a [**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) en lugar de IDirect3DDevice9:: SetFVF porque admite declaraciones de vértices que no se pueden expresar con un FVF.</span><span class="sxs-lookup"><span data-stu-id="feab0-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) can be called in place of IDirect3DDevice9::SetFVF because it supports vertex declarations that cannot be expressed with an FVF.</span></span>

## <a name="intervals-and-swapeffects-changes"></a><span data-ttu-id="feab0-262">Intervalos y cambios de SwapEffects</span><span class="sxs-lookup"><span data-stu-id="feab0-262">Intervals, and SwapEffects Changes</span></span>

<span data-ttu-id="feab0-263">Se realizaron varios cambios para ofrecer al usuario más control sobre la frecuencia de actualización del monitor, la velocidad de presentación y el dibujo del búfer frontal frente al de búfer.</span><span class="sxs-lookup"><span data-stu-id="feab0-263">Several changes were made to give the user more control over monitor refresh rate, presentation rate, and front-buffer versus back-buffer drawing.</span></span> <span data-ttu-id="feab0-264">Los pasos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="feab0-264">They are as follows:</span></span>

-   <span data-ttu-id="feab0-265">Se ha quitado un efecto de intercambio, D3DSWAPEFFECT \_ Copy \_ VSYNC y una velocidad de presentación, D3DPRESENT \_ rate \_ Unlimited.</span><span class="sxs-lookup"><span data-stu-id="feab0-265">Removed one swap effect, D3DSWAPEFFECT\_COPY\_VSYNC, and one presentation rate, D3DPRESENT\_RATE\_UNLIMITED.</span></span>
-   <span data-ttu-id="feab0-266">Se ha cambiado el nombre de \_ los parámetros D3DPRESENT. FullScreen \_ PresentationInterval a PresentationIntervals.</span><span class="sxs-lookup"><span data-stu-id="feab0-266">Renamed D3DPRESENT\_PARAMETERS.FullScreen\_PresentationInterval to PresentationIntervals.</span></span>
-   <span data-ttu-id="feab0-267">Se ha agregado el intervalo de D3DPRESENT \_ \_ inmediato, lo que significa que la presentación no está sincronizada con la sincronización vertical. Como en DirectX 8. x, D3DPRESENT \_ Interval \_ default se define como cero y es equivalente a D3DPRESENT \_ Interval \_ One.</span><span class="sxs-lookup"><span data-stu-id="feab0-267">Added D3DPRESENT\_INTERVAL\_IMMEDIATE, which means that the presentation is not synchronized with the vertical sync. As in DirectX 8.x, D3DPRESENT\_INTERVAL\_DEFAULT is defined as zero and is equivalent to D3DPRESENT\_INTERVAL\_ONE.</span></span> <span data-ttu-id="feab0-268">D3DPRESENT \_ Interval \_ default es una comodidad para inicializar \_ los parámetros de D3DPRESENT en cero.</span><span class="sxs-lookup"><span data-stu-id="feab0-268">D3DPRESENT\_INTERVAL\_DEFAULT is a convenience for initializing D3DPRESENT\_PARAMETERS to zero.</span></span>

<span data-ttu-id="feab0-269">Para obtener una explicación detallada de los modos y los intervalos que se admiten, vea D3DPRESENT.</span><span class="sxs-lookup"><span data-stu-id="feab0-269">For a detailed explanation of the modes and the intervals that are supported, see D3DPRESENT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="feab0-270">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="feab0-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feab0-271">Gráficos de Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="feab0-271">Direct3D 9 Graphics</span></span>](dx9-graphics.md)
</dt> </dl>

 

 

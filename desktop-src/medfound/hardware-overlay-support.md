---
description: Describe cómo usar superposiciones de hardware en Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Compatibilidad con la superposición de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcae33cdf55de59bdcd074829d52b4c1c43ea5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715446"
---
# <a name="hardware-overlay-support"></a><span data-ttu-id="a0adc-103">Compatibilidad con la superposición de hardware</span><span class="sxs-lookup"><span data-stu-id="a0adc-103">Hardware Overlay Support</span></span>

<span data-ttu-id="a0adc-104">Una superposición de hardware es un área dedicada de memoria de vídeo que se puede superponer en la superficie principal.</span><span class="sxs-lookup"><span data-stu-id="a0adc-104">A hardware overlay is a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="a0adc-105">No se realiza ninguna copia cuando se muestra la superposición.</span><span class="sxs-lookup"><span data-stu-id="a0adc-105">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="a0adc-106">La operación de superposición se realiza en el hardware, sin modificar los datos en la superficie principal.</span><span class="sxs-lookup"><span data-stu-id="a0adc-106">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

<span data-ttu-id="a0adc-107">El uso de superposiciones de hardware para la reproducción de vídeo era habitual en versiones anteriores de Windows, ya que las superposiciones son eficientes para el contenido de vídeo con una velocidad de fotogramas alta.</span><span class="sxs-lookup"><span data-stu-id="a0adc-107">The use of hardware overlays for video playback was common in earlier versions of Windows, because overlays are efficient for video content with a high frame rate.</span></span> <span data-ttu-id="a0adc-108">A partir de Windows 7, Direct3D 9 admite superposiciones de hardware.</span><span class="sxs-lookup"><span data-stu-id="a0adc-108">Starting in Windows 7, Direct3D 9 supports hardware overlays.</span></span> <span data-ttu-id="a0adc-109">Esta compatibilidad está pensada principalmente para la reproducción de vídeo y difiere en algunos aspectos de las API de DirectDraw anteriores:</span><span class="sxs-lookup"><span data-stu-id="a0adc-109">This support is intended primarily for video playback, and differs in some respects from earlier DirectDraw APIs:</span></span>

-   <span data-ttu-id="a0adc-110">La superposición no se puede reducir, reflejar o Desentrelazar.</span><span class="sxs-lookup"><span data-stu-id="a0adc-110">The overlay cannot be shrunk, mirrored, or deinterlaced.</span></span>
-   <span data-ttu-id="a0adc-111">No se admiten las claves de color de origen ni la combinación alfa.</span><span class="sxs-lookup"><span data-stu-id="a0adc-111">Source color keys and alpha blending are not supported.</span></span>
-   <span data-ttu-id="a0adc-112">Las superposiciones se pueden ajustar si el hardware de superposición lo admite.</span><span class="sxs-lookup"><span data-stu-id="a0adc-112">Overlays can be stretched if the overlay hardware supports it.</span></span> <span data-ttu-id="a0adc-113">De lo contrario, no se admite la ampliación.</span><span class="sxs-lookup"><span data-stu-id="a0adc-113">Otherwise, stretching is not supported.</span></span> <span data-ttu-id="a0adc-114">En la práctica, no todos los controladores de gráficos admiten la ampliación.</span><span class="sxs-lookup"><span data-stu-id="a0adc-114">In practice, not all graphics drivers support stretching.</span></span>
-   <span data-ttu-id="a0adc-115">Cada dispositivo admite como máximo una superposición.</span><span class="sxs-lookup"><span data-stu-id="a0adc-115">Each device supports at most one overlay.</span></span>
-   <span data-ttu-id="a0adc-116">La superposición se realiza mediante una clave de color de destino, pero el tiempo de ejecución de Direct3D selecciona automáticamente el color y dibuja el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="a0adc-116">Overlay is performed using a destination color key, but the Direct3D runtime automatically selects the color and draws the destination rectangle.</span></span> <span data-ttu-id="a0adc-117">Direct3D realiza automáticamente el seguimiento de la posición de la ventana y actualiza la posición de la superposición cada vez que se llama a **PresentEx** .</span><span class="sxs-lookup"><span data-stu-id="a0adc-117">Direct3D automatically tracks the position of the window and updates the overlay position whenever the **PresentEx** is called.</span></span>

### <a name="creating-a-hardware-overlay-surface"></a><span data-ttu-id="a0adc-118">Crear una superficie de superposición de hardware</span><span class="sxs-lookup"><span data-stu-id="a0adc-118">Creating a Hardware Overlay Surface</span></span>

<span data-ttu-id="a0adc-119">Para consultar la compatibilidad con la superposición, llame a **IDirect3D9:: GetDeviceCaps**.</span><span class="sxs-lookup"><span data-stu-id="a0adc-119">To query for overlay support, call **IDirect3D9::GetDeviceCaps**.</span></span> <span data-ttu-id="a0adc-120">Si el controlador admite la superposición de hardware, la marca de **\_ superposición D3DCAPS** se establece en **D3DCAPS9. Elemento Cap** .</span><span class="sxs-lookup"><span data-stu-id="a0adc-120">If the driver supports hardware overlay, the **D3DCAPS\_OVERLAY** flag is set in the **D3DCAPS9.Caps** member.</span></span>

<span data-ttu-id="a0adc-121">Para averiguar si un formato de superposición específico es compatible con un modo de presentación determinado, llame a [**IDirect3D9ExOverlayExtension:: CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span><span class="sxs-lookup"><span data-stu-id="a0adc-121">To find out whether a specific overlay format is supported for a given display mode, call [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span></span>

<span data-ttu-id="a0adc-122">Para crear la superposición, llame a **IDirect3D9Ex:: CreateDeviceEx** y especifique el efecto de intercambio de **\_ superposición D3DSWAPEFFECT** .</span><span class="sxs-lookup"><span data-stu-id="a0adc-122">To create the overlay, call **IDirect3D9Ex::CreateDeviceEx** and specify the **D3DSWAPEFFECT\_OVERLAY** swap effect.</span></span> <span data-ttu-id="a0adc-123">Si el hardware lo admite, el búfer de reserva puede utilizar un formato que no sea RGB.</span><span class="sxs-lookup"><span data-stu-id="a0adc-123">The back buffer can use a non-RGB format if the hardware supports it.</span></span>

<span data-ttu-id="a0adc-124">Las superficies superpuestas tienen las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="a0adc-124">Overlay surfaces have the following limitations:</span></span>

-   <span data-ttu-id="a0adc-125">La aplicación no puede crear más de una cadena de intercambio de superposición.</span><span class="sxs-lookup"><span data-stu-id="a0adc-125">The application cannot create more than one overlay swap chain.</span></span>
-   <span data-ttu-id="a0adc-126">La superposición debe usarse en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="a0adc-126">The overlay must be used in windowed mode.</span></span> <span data-ttu-id="a0adc-127">No se puede usar en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="a0adc-127">It cannot be used in fullscreen mode.</span></span>
-   <span data-ttu-id="a0adc-128">El efecto de intercambio de superposición debe usarse con la interfaz **IDirect3DDevice9Ex** .</span><span class="sxs-lookup"><span data-stu-id="a0adc-128">The overlay swap effect must be used with the **IDirect3DDevice9Ex** interface.</span></span> <span data-ttu-id="a0adc-129">No es compatible con **IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="a0adc-129">It is not supported for **IDirect3DDevice9**.</span></span>
-   <span data-ttu-id="a0adc-130">No se puede usar el muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="a0adc-130">Multisampling cannot be used.</span></span>
-   <span data-ttu-id="a0adc-131">No se admiten las marcas **D3DPRESENT \_ DONOTFLIP** y **D3DPRESENT \_ FLIPRESTART** .</span><span class="sxs-lookup"><span data-stu-id="a0adc-131">The **D3DPRESENT\_DONOTFLIP** and **D3DPRESENT\_FLIPRESTART** flags are not supported.</span></span>
-   <span data-ttu-id="a0adc-132">Las estadísticas de presentación no están disponibles para la superficie superpuesta.</span><span class="sxs-lookup"><span data-stu-id="a0adc-132">Presentation statistics are not available for the overlay surface.</span></span>

<span data-ttu-id="a0adc-133">Si el hardware no admite la expansión, se recomienda crear una cadena de intercambio tan grande como el modo de presentación, de modo que se pueda cambiar el tamaño de la ventana a cualquier dimensión.</span><span class="sxs-lookup"><span data-stu-id="a0adc-133">If the hardware does not support stretching, it is recommended to create a swap chain as large as the display mode, so that the window can be resized to any dimensions.</span></span> <span data-ttu-id="a0adc-134">Volver a crear la cadena de intercambio no es una manera óptima de controlar el cambio de tamaño de la ventana, ya que puede provocar artefactos de representación graves.</span><span class="sxs-lookup"><span data-stu-id="a0adc-134">Recreating the swap chain is not an optimal way to handle resizing the window, because it can cause severe rendering artifacts.</span></span> <span data-ttu-id="a0adc-135">Además, debido a la forma en que la GPU administra la memoria de superposición, la recreación de la cadena de intercambio puede provocar que una aplicación se quede sin memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a0adc-135">Also, because of the way the GPU manages the overlay memory, recreating the swap chain can potentially cause an application to run out of video memory.</span></span>

### <a name="new-d3dpresent_parameters-flags"></a><span data-ttu-id="a0adc-136">Nuevas marcas de parámetros de D3DPRESENT \_</span><span class="sxs-lookup"><span data-stu-id="a0adc-136">New D3DPRESENT\_PARAMETERS Flags</span></span>

<span data-ttu-id="a0adc-137">Se definen los siguientes marcadores de **\_ parámetros de D3DPRESENT** para crear superposiciones.</span><span class="sxs-lookup"><span data-stu-id="a0adc-137">The following **D3DPRESENT\_PARAMETERS** flags are defined for creating overlays.</span></span>



| <span data-ttu-id="a0adc-138">Marca</span><span class="sxs-lookup"><span data-stu-id="a0adc-138">Flag</span></span>                                      | <span data-ttu-id="a0adc-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0adc-139">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0adc-140">**D3DPRESENTFLAG \_ superposición \_ LIMITEDRGB**</span><span class="sxs-lookup"><span data-stu-id="a0adc-140">**D3DPRESENTFLAG\_OVERLAY\_LIMITEDRGB**</span></span>   | <span data-ttu-id="a0adc-141">El intervalo RGB es 16 – 235.</span><span class="sxs-lookup"><span data-stu-id="a0adc-141">The RGB range is 16–235.</span></span> <span data-ttu-id="a0adc-142">El valor predeterminado es 0 – 255.</span><span class="sxs-lookup"><span data-stu-id="a0adc-142">The default is 0–255.</span></span> <br/> <span data-ttu-id="a0adc-143">Requiere la funcionalidad de **\_ LIMITEDRANGERGB de D3DOVERLAYCAPS** .</span><span class="sxs-lookup"><span data-stu-id="a0adc-143">Requires the **D3DOVERLAYCAPS\_LIMITEDRANGERGB** capability.</span></span><br/>                                                 |
| <span data-ttu-id="a0adc-144">**D3DPRESENTFLAG de BT709 de la \_ superposición \_ YCbCr \_**</span><span class="sxs-lookup"><span data-stu-id="a0adc-144">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_BT709**</span></span> | <span data-ttu-id="a0adc-145">Los colores YUV usan la definición de BT. 709.</span><span class="sxs-lookup"><span data-stu-id="a0adc-145">YUV colors use the BT.709 definition.</span></span> <span data-ttu-id="a0adc-146">El valor predeterminado es BT. 601.</span><span class="sxs-lookup"><span data-stu-id="a0adc-146">The default is BT.601.</span></span> <br/> <span data-ttu-id="a0adc-147">Requiere la **funcionalidad \_ \_ BT709 de YCbCr D3DOVERLAYCAPS** .</span><span class="sxs-lookup"><span data-stu-id="a0adc-147">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT709** capability.</span></span><br/>                                      |
| <span data-ttu-id="a0adc-148">**D3DPRESENTFLAG de xvYCC de la \_ superposición \_ YCbCr \_**</span><span class="sxs-lookup"><span data-stu-id="a0adc-148">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_xvYCC**</span></span> | <span data-ttu-id="a0adc-149">Generar los datos mediante YCbCr extendido (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="a0adc-149">Output the data by using extended YCbCr (xvYCC).</span></span><br/> <span data-ttu-id="a0adc-150">Requiere la funcionalidad **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** o **D3DOVERLAYCAPS \_ YCbCr \_ BT709 \_ xvYCC** .</span><span class="sxs-lookup"><span data-stu-id="a0adc-150">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT601\_xvYCC** or **D3DOVERLAYCAPS\_YCbCr\_BT709\_xvYCC** capability.</span></span><br/> |



 

### <a name="using-hardware-overlays"></a><span data-ttu-id="a0adc-151">Usar superposiciones de hardware</span><span class="sxs-lookup"><span data-stu-id="a0adc-151">Using Hardware Overlays</span></span>

<span data-ttu-id="a0adc-152">Para mostrar la superficie de superposición, la aplicación llama a **IDirect3DDevice9Ex::P resentex**.</span><span class="sxs-lookup"><span data-stu-id="a0adc-152">To display the overlay surface, the application calls **IDirect3DDevice9Ex::PresentEx**.</span></span> <span data-ttu-id="a0adc-153">El tiempo de ejecución de Direct3D dibuja automáticamente la clave de color de destino.</span><span class="sxs-lookup"><span data-stu-id="a0adc-153">The Direct3D runtime automatically draws the destination color key.</span></span>

<span data-ttu-id="a0adc-154">Las siguientes marcas de **PresentEx** se definen para las superposiciones.</span><span class="sxs-lookup"><span data-stu-id="a0adc-154">The following **PresentEx** flags are defined for overlays.</span></span>



| <span data-ttu-id="a0adc-155">Marca</span><span class="sxs-lookup"><span data-stu-id="a0adc-155">Flag</span></span>                              | <span data-ttu-id="a0adc-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0adc-156">Description</span></span>                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0adc-157">**D3DPRESENT \_ UPDATECOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="a0adc-157">**D3DPRESENT\_UPDATECOLORKEY**</span></span>    | <span data-ttu-id="a0adc-158">Establezca esta marca si la composición de Administrador de ventanas de escritorio (DWM) está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="a0adc-158">Set this flag if Desktop Window Manager (DWM) composition is disabled.</span></span> <span data-ttu-id="a0adc-159">Esta marca hace que Direct3D vuelva a dibujar la clave de color.</span><span class="sxs-lookup"><span data-stu-id="a0adc-159">This flag causes Direct3D to redraw the color key.</span></span><br/> <span data-ttu-id="a0adc-160">Si DWM está habilitado, esta marca no es necesaria, porque Direct3D dibuja la clave de color una vez en la superficie que DWM usa para la redirección.</span><span class="sxs-lookup"><span data-stu-id="a0adc-160">If DWM is enabled, this flag is not required, because Direct3D draws the color key once on the surface that DWM uses for redirection.</span></span><br/> |
| <span data-ttu-id="a0adc-161">**D3DPRESENT \_ HIDEOVERLAY**</span><span class="sxs-lookup"><span data-stu-id="a0adc-161">**D3DPRESENT\_HIDEOVERLAY**</span></span>       | <span data-ttu-id="a0adc-162">Oculta la superposición.</span><span class="sxs-lookup"><span data-stu-id="a0adc-162">Hides the overlay.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a0adc-163">**D3DPRESENT \_ UPDATEOVERLAYONLY**</span><span class="sxs-lookup"><span data-stu-id="a0adc-163">**D3DPRESENT\_UPDATEOVERLAYONLY**</span></span> | <span data-ttu-id="a0adc-164">Actualiza la superposición sin cambiar el contenido.</span><span class="sxs-lookup"><span data-stu-id="a0adc-164">Updates the overlay without changing the contents.</span></span><br/> <span data-ttu-id="a0adc-165">Esta marca es útil si la ventana se mueve mientras el vídeo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="a0adc-165">This flag is useful if the window moves while the video is paused.</span></span><br/>                                                                                                                                           |



 

<span data-ttu-id="a0adc-166">Una aplicación debe estar preparada para controlar los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="a0adc-166">An application should be prepared to handle the following cases:</span></span>

-   <span data-ttu-id="a0adc-167">Si otra aplicación está usando la superposición, **PresentEx** devuelve **D3DERR \_ NOTAVAILABLE**.</span><span class="sxs-lookup"><span data-stu-id="a0adc-167">If another application is using the overlay, **PresentEx** returns **D3DERR\_NOTAVAILABLE**.</span></span>
-   <span data-ttu-id="a0adc-168">Si la ventana se mueve a otro monitor, la aplicación debe volver a crear la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="a0adc-168">If the window is moved to another monitor, the application must recreate the swap chain.</span></span> <span data-ttu-id="a0adc-169">De lo contrario, si la aplicación llama a **PresentEx** para mostrar la superposición en un monitor diferente, **PresentEx** devuelve **D3DERR \_ INVALIDDEVICE**.</span><span class="sxs-lookup"><span data-stu-id="a0adc-169">Otherwise, if the application calls **PresentEx** to display the overlay on a different monitor, **PresentEx** returns **D3DERR\_INVALIDDEVICE**.</span></span>
-   <span data-ttu-id="a0adc-170">Si cambia el modo de presentación, Direct3D intenta restaurar la superposición.</span><span class="sxs-lookup"><span data-stu-id="a0adc-170">If the display mode changes, Direct3D attempts to restore the overlay.</span></span> <span data-ttu-id="a0adc-171">Si el nuevo modo no admite la superposición, **PresentEx** devuelve **D3DERR \_ UNSUPPORTEDOVERLAY**.</span><span class="sxs-lookup"><span data-stu-id="a0adc-171">If the new mode does not support the overlay, **PresentEx** returns **D3DERR\_UNSUPPORTEDOVERLAY**.</span></span>

### <a name="example-code"></a><span data-ttu-id="a0adc-172">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0adc-172">Example Code</span></span>

<span data-ttu-id="a0adc-173">En el ejemplo siguiente se muestra cómo crear una superficie de superposición.</span><span class="sxs-lookup"><span data-stu-id="a0adc-173">The following example shows how to create an overlay surface.</span></span>


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a0adc-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0adc-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0adc-175">API de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a0adc-175">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 





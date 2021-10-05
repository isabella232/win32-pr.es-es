---
title: Ejemplos de código de cadena de intercambio de composición
description: Colección de ejemplos de código que muestran varios escenarios de cadena de intercambio de composición.
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 5dccd8df84111bb41a894a7ddb6da77c27b4f742
ms.sourcegitcommit: b1f058e2360e54c07cb988a3204ec33f47889122
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2021
ms.locfileid: "129454661"
---
# <a name="composition-swapchain-code-examples"></a>Ejemplos de código de cadena de intercambio de composición

En estos ejemplos de código se [usa Windows bibliotecas de implementación de implementación (WIL).](https://github.com/Microsoft/wil) Una manera cómoda de instalar WIL es ir  a Visual Studio, hacer clic en Project \> **Administrar paquetes NuGet...** Examinar, escribir o pegar \>  **Microsoft.Windows. ImplementationLibrary** en el cuadro de búsqueda, seleccione el  elemento en los resultados de la búsqueda y, a continuación, haga clic en Instalar para instalar el paquete para ese proyecto.

## <a name="example-1mdashcreating-a-presentation-manager-on-systems-that-support-the-composition-swapchain-api"></a>Ejemplo &mdash; 1: Creación de un administrador de presentación en sistemas que admiten la API de cadena de intercambio de composición

Como se mencionó, la API de cadena de intercambio de composición requiere controladores admitidos para funcionar. En el ejemplo siguiente se muestra cómo la aplicación puede crear un administrador de presentación si el sistema admite la API. Esto se muestra como una `TryCreate` función de estilo que devuelve el administrador de presentación solo si se admite la API. Esta función también muestra cómo crear correctamente un dispositivo Direct3D para crear un administrador de presentación.

### <a name="c-example"></a>Ejemplo de C++

```cpp
bool TryCreatePresentationManager(
    _In_ bool requestDirectPresentation,
    _Out_ ID3D11Device** ppD3DDevice,
    _Outptr_opt_result_maybenull_ IPresentationManager **ppPresentationManager)
{
    // Null the presentation manager and Direct3D device initially
    *ppD3DDevice = nullptr;
    *ppPresentationManager = nullptr;

    // Direct3D device creation flags. The composition swapchain API requires that applications disable internal
    // driver threading optimizations, as these optimizations are incompatible with the
    // composition swapchain API. If this flag is not present, then the API will fail the call to create the
    // presentation factory.
    UINT deviceCreationFlags =
        D3D11_CREATE_DEVICE_BGRA_SUPPORT |
        D3D11_CREATE_DEVICE_SINGLETHREADED |
        D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS;

    // Create the Direct3D device.
    com_ptr_failfast<ID3D11DeviceContext> d3dDeviceContext;
    FAIL_FAST_IF_FAILED(D3D11CreateDevice(
        nullptr,                   // No adapter
        D3D_DRIVER_TYPE_HARDWARE,  // Hardware device
        nullptr,                   // No module
        deviceCreationFlags,       // Device creation flags
        nullptr, 0,                // Highest available feature level
        D3D11_SDK_VERSION,         // API version
        ppD3DDevice,               // Resulting interface pointer
        nullptr,                   // Actual feature level
        &d3dDeviceContext));       // Device context

    // Call the composition swapchain API export to create the presentation factory.
    com_ptr_failfast<IPresentationFactory> presentationFactory;
    FAIL_FAST_IF_FAILED(CreatePresentationFactory(
        (*ppD3DDevice),
        IID_PPV_ARGS(&presentationFactory)));

    // Determine whether the system is capable of supporting the composition swapchain API based
    // on the capability that's reported by the presentation factory. If your application
    // wants direct presentation (that is, presentation without the need for DWM to
    // compose, using MPO or iflip), then we query for direct presentation support.
    bool isSupportedOnSystem;
    if (requestDirectPresentation)
    {
        isSupportedOnSystem = presentationFactory->IsPresentationSupportedWithIndependentFlip();
    }
    else
    {
        isSupportedOnSystem = presentationFactory->IsPresentationSupported();
    }

    // Create the presentation manager if it is supported on the current system.
    if (isSupportedOnSystem)
    {
        FAIL_FAST_IF_FAILED(presentationFactory->CreatePresentationManager(ppPresentationManager));
    }

    return isSupportedOnSystem;
}
```

## <a name="example-2mdashcreating-a-presentation-manager-and-presentation-surface"></a>Ejemplo &mdash; 2: Creación de un administrador de presentación y una superficie de presentación

En el ejemplo siguiente se muestra cómo la aplicación crearía un administrador de presentación y una superficie de presentación para enlazar a un objeto visual en un árbol visual. Los ejemplos posteriores mostrarán cómo enlazar la superficie de presentación a los árboles visuales [**DirectComposition**](/windows/win32/directcomp/directcomposition-portal) [**y Windows.UI.Composition.**](/uwp/api/windows.ui.composition)

### <a name="c-example-dcompositiongettargetstatistics"></a>Ejemplo de C++ (DCompositionGetTargetStatistics)

```cpp
bool MakePresentationManagerAndPresentationSurface(
    _Out_ ID3D11Device** ppD3dDevice,
    _Out_ IPresentationManager** ppPresentationManager,
    _Out_ IPresentationSurface** ppPresentationSurface,
    _Out_ unique_handle& compositionSurfaceHandle)
{
    // Null the output pointers initially.
    *ppD3dDevice = nullptr;
    *ppPresentationManager = nullptr;
    *ppPresentationSurface = nullptr;
    compositionSurfaceHandle.reset();

    com_ptr_failfast<IPresentationManager> presentationManager;
    com_ptr_failfast<IPresentationSurface> presentationSurface;
    com_ptr_failfast<ID3D11Device> d3d11Device;

    // Call the function we defined previously to create a Direct3D device and presentation manager, if
    // the system supports it.
    if (TryCreatePresentationManager(
        true, // Request presentation with independent flip.
        &d3d11Device,
        &presentationManager) == false)
    {
        // Return 'false' out of the call if the composition swapchain API is unsupported. Assume the caller
        // will handle this somehow, such as by falling back to DXGI.
        return false;
    }

    // Use DirectComposition to create a composition surface handle.
    FAIL_FAST_IF_FAILED(DCompositionCreateSurfaceHandle(
        COMPOSITIONOBJECT_ALL_ACCESS,
        nullptr,
        compositionSurfaceHandle.addressof()));

    // Create presentation surface bound to the composition surface handle.
    FAIL_FAST_IF_FAILED(presentationManager->CreatePresentationSurface(
        compositionSurfaceHandle.get(),
        presentationSurface.addressof()));

    // Return the Direct3D device, presentation manager, and presentation surface to the caller for future
    // use.
    *ppD3dDevice = d3d11Device.detach();
    *ppPresentationManager = presentationManager.detach();
    *ppPresentationSurface = presentationSurface.detach();

    // Return 'true' out of the call if the composition swapchain API is supported and we were able to
    // create a presentation manager.
    return true;
}
```

## <a name="example-3mdashbinding-a-presentation-surface-to-a-windowsuicomposition-surface-brush"></a>Ejemplo 3 &mdash; Enlace de una superficie de presentación a un pincel de superficie Windows.UI.Composition

En el ejemplo siguiente se muestra cómo la aplicación enlazaría un identificador de superficie de composición enlazado a una superficie de presentación, como se creó en el ejemplo anterior, a un pincel de superficie [**Windows.UI.Composition**](/uwp/api/windows.ui.composition) *(WinComp),* que luego se puede enlazar a un objeto visual sprite en el árbol visual de la aplicación.

### <a name="c-example"></a>Ejemplo de C++

```cpp
void BindPresentationSurfaceHandleToWinCompTree(
    _In_ ICompositor * pCompositor,
    _In_ ISpriteVisual * pVisualToBindTo, // The sprite visual we want to bind to.
    _In_ unique_handle& compositionSurfaceHandle)
{
    // QI an interop compositor from the passed compositor.
    com_ptr_failfast<ICompositorInterop> compositorInterop;
    FAIL_FAST_IF_FAILED(pCompositor->QueryInterface(IID_PPV_ARGS(&compositorInterop)));

    // Create a composition surface for the presentation surface's composition surface handle.
    com_ptr_failfast<ICompositionSurface> compositionSurface;
    FAIL_FAST_IF_FAILED(compositorInterop->CreateCompositionSurfaceForHandle(
        compositionSurfaceHandle.get(),
        &compositionSurface));

    // Create a composition surface brush, and bind the surface to it.
    com_ptr_failfast<ICompositionSurfaceBrush> surfaceBrush;
    FAIL_FAST_IF_FAILED(pCompositor->CreateSurfaceBrush(&surfaceBrush));
    FAIL_FAST_IF_FAILED(surfaceBrush->put_Surface(compositionSurface.get()));

    // Bind the brush to the visual.
    auto brush = surfaceBrush.query<ICompositionBrush>();
    FAIL_FAST_IF_FAILED(pVisualToBindTo->put_Brush(brush.get()));
}
```

## <a name="example-4mdashbinding-a-presentation-surface-to-a-directcomposition-visual"></a>Ejemplo 4 &mdash; Enlace de una superficie de presentación a un objeto visual DirectComposition

En el ejemplo siguiente se muestra cómo la aplicación enlazaría una superficie de presentación a un objeto visual DirectComposition *(DComp)* en un árbol visual.

### <a name="c-example"></a>Ejemplo de C++

```cpp
void BindPresentationSurfaceHandleToDCompTree(
    _In_ IDCompositionDevice* pDCompDevice,
    _In_ IDCompositionVisual* pVisualToBindTo,
    _In_ unique_handle& compositionSurfaceHandle) // The composition surface handle that was
                                                  // passed to CreatePresentationSurface.
{
    // Create a DComp surface to wrap the presentation surface.
    com_ptr_failfast<IUnknown> dcompSurface;
    FAIL_FAST_IF_FAILED(pDCompDevice->CreateSurfaceFromHandle(
        compositionSurfaceHandle.get(),
        &dcompSurface));

    // Bind the presentation surface to the visual.
    FAIL_FAST_IF_FAILED(pVisualToBindTo->SetContent(dcompSurface.get()));
}
```

## <a name="example-5mdashsetting-alpha-mode-and-color-space-on-a-presentation-surface"></a>Ejemplo 5 &mdash; Establecimiento del modo alfa y el espacio de color en una superficie de presentación

En el ejemplo siguiente se muestra cómo la aplicación establecería el modo alfa y el espacio de color en una superficie de presentación. El modo alfa describe si se debe interpretar o no el canal alfa de la textura y cómo. El espacio de colores describe el espacio de color al que hacen referencia los píxeles de textura.

Todas las actualizaciones de propiedades como estas surtendrán efecto como parte del siguiente presente de la aplicación y surtendrán efecto de forma atómica junto con las actualizaciones de búfer que forman parte de ese presente. Un presente también puede, si la aplicación lo desea, no actualizar ningún búfer en absoluto y, en su lugar, constar solo de actualizaciones de propiedades. Las superficies de presentación cuyos búferes no se actualizan en un presente determinado permanecen enlazadas al búfer al que estaban enlazados antes de ese presente.

### <a name="c-example"></a>Ejemplo de C++

```cpp
void SetAlphaModeAndColorSpace(
    _In_ IPresentationSurface* pPresentationSurface)
{
    // Set alpha mode.
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetAlphaMode(DXGI_ALPHA_MODE_IGNORE));

    // Set color space to full RGB.
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetColorSpace(DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709));
}
```

## <a name="example-6mdashsetting-letterboxing-margins-on-a-presentation-surface"></a>Ejemplo 6 &mdash; Establecimiento de márgenes de letterboxing en una superficie de presentación

En el ejemplo siguiente se muestra cómo la aplicación especificaría los márgenes de letterboxing en una superficie de presentación. La conversión letterboxing se usa para rellenar un área especificada fuera del propio contenido de la superficie, para tener en cuenta las distintas relaciones de aspecto entre el contenido y el dispositivo de visualización en el que se muestra. Un buen ejemplo de  esto son las barras negras que a menudo son visibles por encima y por debajo del contenido al ver en un equipo una película con formato para pantallas de pantalla ancha. La API de intercambio de composición permite especificar los márgenes dentro de los cuales se representa la aplicación de letterboxing en estos casos.

Actualmente, las áreas de letterboxing siempre se rellenan con negro opaco.

Como contenido de árbol visual, la superficie de presentación existe en el espacio de coordenadas de su objeto visual host. Con el formato letterboxing presente, el origen del espacio de coordenadas del objeto visual se corresponde con la parte superior izquierda de la caja de letras. Es decir, el propio búfer existe desplazamiento en el espacio de coordenadas del objeto visual. Los límites se calculan como el tamaño del búfer más el tamaño de la caja de letras.

A continuación se muestra dónde existen el búfer y el letterboxing en el espacio de coordenadas visual y cómo se calculan los límites.

![Márgenes de letterboxing](images/letterboxing-margins.png)

Por último, si la transformación aplicada a una superficie de presentación viene con un desplazamiento, el área no cubierta por el búfer o el letterboxing se considera fuera de los límites del contenido y se trata como transparente de forma similar a como se trata cualquier otro contenido de árbol visual fuera de los &mdash; límites de contenido.

### <a name="letterboxing-and-transform-interaction"></a>Interacción de transformación y letterboxing

Con el fin de proporcionar tamaños de margen de conversión letterboxing coherentes independientemente de la escala que la aplicación aplique a un búfer para rellenar algún área de contenido, DWM intentará representar los márgenes en un tamaño coherente independientemente de la escala, pero teniendo en cuenta el resultado de la transformación que se ha aplicado a la superficie de presentación.

Dicho de otro modo, los márgenes de letterboxing se aplican técnicamente antes de aplicar la transformación de la superficie de presentación, pero compensan cualquier escala que pueda formar parte de esa transformación. Es decir, la transformación de la superficie de presentación se deconstruye en dos componentes, la parte de la transformación que se escala y el resto &mdash; de la transformación.

![Interacción de transformación y letterboxing 1](images/letterboxing-and-transform-interaction-1.png)

Por ejemplo, con márgenes de letterboxing de 100 px y sin ninguna transformación aplicada a la superficie de presentación, el búfer resultante se representará sin escala y los márgenes de letterboxing tendrán 100 px de ancho.

![Interacción de transformación y letterboxing 2](images/letterboxing-and-transform-interaction-2.png)

Otro ejemplo, con márgenes de letterboxing de 100 px y una transformación de escala de 2 veces aplicada en la superficie de presentación, el búfer resultante se representará con una escala de dos veces y los márgenes de letterboxing que se ven en la pantalla seguirán siendo de 100 px en todos los tamaños.

![Interacción de transformación y letterboxing 3](images/letterboxing-and-transform-interaction-3.png)

Otro ejemplo, con una transformación de rotación de 45 grados, los márgenes de letterboxing resultantes aparecerán a 100 px y los márgenes de letterboxing se girarán con el búfer.

![Interacción de transformación y letterboxing 4](images/letterboxing-and-transform-interaction-4.png)

Otro ejemplo, con una transformación de escala 2x y rotación de 45 grados, la imagen se girará y escalará, y los márgenes de letterboxing también tendrán 100 px de ancho y se girarán con el búfer.

![Interacción de transformación y letterboxing 5](images/letterboxing-and-transform-interaction-5.png)

Si una transformación de escala no se puede extraer de forma inequívoca de la transformación que la aplicación aplica a la superficie de presentación, como si la escala X o Y resultante es 0, los márgenes de conversión de letras se representarán con toda la transformación aplicada y no intentaremos compensar la escala.

![Interacción de transformación y letterboxing 6](images/letterboxing-and-transform-interaction-6.png)

### <a name="c-example"></a>Ejemplo de C++

```cpp
 void SetContentLayoutAndFill(
    _In_ IPresentationSurface* pPresentationSurface)
{
    // Set layout properties. Each layout property is described below.

    // The source RECT describes the area from the bound buffer that will be sampled from. The
    // RECT is in source texture coordinates. Below we indicate that we'll sample from a
    // 100x100 area on the source texture.
    RECT sourceRect;
    sourceRect.left = 0;
    sourceRect.top = 0;
    sourceRect.right = 100;
    sourceRect.bottom = 100;
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetSourceRect(&sourceRect));

    // The presentation transform defines how the source rect will be transformed when
    // rendering the buffer. In this case, we indicate we want to scale it 2x in both
    // width and height, and we also want to offset it 50 pixels to the right.
    PresentationTransform transform = { 0 };
    transform.M11 = 2.0f; // X scale 2x
    transform.M22 = 2.0f; // Y scale 2x
    transform.M31 = 50.0f; // X offset 50px
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetTransform(&transform));

    // The letterboxing parameters describe how to letterbox the content. Letterboxing
    // is commonly used to fill area not covered by video/surface content when scaling to
    // an aspect ration that doesn't match the aspect ratio of the surface itself. For
    // example, when viewing content formatted for the theater on a 1080p home screen, one
    // can typically see black "bars" on the top and bottom of the video, covering the space
    // on screen that wasn't covered by the video due to the differing aspect ratios of the
    // content and the display device. The composition swapchain API allows the user to specify
    // letterboxing margins, which describe the number of pixels to surround the surface
    // content with on screen. In this case, surround the top and bottom of our content with
    // 100 pixel tall letterboxing.
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetLetterboxingMargins(
        0.0f,
        100.0f,
        0.0f,
        100.0f));
}
```

## <a name="example-7mdashsetting-content-restrictions-on-a-presentation-surface"></a>Ejemplo 7 &mdash; Establecimiento de restricciones de contenido en una superficie de presentación

En el ejemplo siguiente se muestra cómo la aplicación impediría que otras aplicaciones leyesen el contenido de la superficie de presentación (de tecnologías como PrintScreen, DDA, Capture API, etc.) para fines de contenido protegido. También se muestra cómo limitar la presentación de una superficie de presentación a una única salida DXGI.

Si la lectura de contenido está deshabilitada, cuando la aplicación intente volver a leer, la imagen capturada contendrá negro opaco en lugar de la superficie de presentación. Si una superficie de presentación está limitada a [**una IDXGIOutput,**](/windows/win32/api/dxgi/nn-dxgi-idxgioutput)aparecerá como negro opaco en todas las demás salidas.

### <a name="c-example"></a>Ejemplo de C++

```cpp
void SetContentRestrictions(
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ IDXGIOutput* pOutputToRestrictTo)
{
    // Disable readback of the surface via printscreen, bitblt, etc.
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetDisableReadback(true));

    // Restrict display of surface to only the passed output.
    FAIL_FAST_IF_FAILED(pPresentationSurface->RestrictToOutput(pOutputToRestrictTo));
}
```

## <a name="example-8mdashadding-presentation-buffers-to-a-presentation-manager"></a>Ejemplo &mdash; 8: Adición de búferes de presentación a un administrador de presentación

En el ejemplo siguiente se muestra cómo la aplicación asignaría un conjunto de texturas de Direct3D y las agregaría al administrador de presentación para usarlas como búferes de presentación, que se pueden presentar a las superficies de presentación.

Como se mencionó, no hay ninguna restricción en torno al número de administradores de presentación con los que se puede registrar una textura. Sin embargo, en la mayoría de los casos de uso normales, una textura solo se registrará en un único administrador de presentación.

Tenga en cuenta también que, dado que la API acepta identificadores de búfer compartidos como moneda al registrar texturas como búferes de presentación en el administrador de presentación, y dado que DXGI puede crear varios búferes compartidos para una sola textura2D, es técnicamente posible que la aplicación cree varios identificadores de búfer compartido para una sola textura y los registre con el administrador de presentación.  básicamente tener el efecto de agregar el mismo búfer más de una vez. Esto no se recomienda, ya que interrumpirá los mecanismos de sincronización que proporciona el administrador de presentación, ya que dos búferes de presentación a los que se realiza un seguimiento único se corresponderán realmente con la misma textura. Puesto que se trata de una API avanzada y, como en realidad es bastante difícil en la implementación detectar este caso cuando se produce, la API no intenta validar este escenario.

### <a name="c-example"></a>Ejemplo de C++

```cpp
void AddBuffersToPresentationManager(
    _In_ ID3D11Device* pD3D11Device, // The backing Direct3D device
    _In_ IPresentationManager* pPresentationManager, // Previously-made presentation manager
    _In_ UINT bufferWidth, // The width of the buffers to add
    _In_ UINT bufferHeight, // The height of the buffers to add
    _In_ UINT numberOfBuffersToAdd, // The number of buffers to add to the presentation manager
    _Out_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures, // Array of textures returned
    _Out_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers) // Array of presentation buffers returned
{
    // Clear the returned vectors initially.
    textures.clear();
    presentationBuffers.clear();

    // Add the desired buffers to the presentation manager.
    for (UINT i = 0; i < numberOfBuffersToAdd; i++)
    {
        com_ptr_failfast<ID3D11Texture2D> texture;
        com_ptr_failfast<IPresentationBuffer> presentationBuffer;

        // Call our helper to make a new buffer of the desired type.
        AddNewPresentationBuffer(
            pD3D11Device,
            pPresentationManager,
            bufferWidth,
            bufferHeight,
            &texture,
            &presentationBuffer);

        // Track our buffers in our own set of vectors.
        textures.push_back(texture);
        presentationBuffers.push_back(presentationBuffer);
    }
}

void AddNewPresentationBuffer(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ UINT bufferWidth,
    _In_ UINT bufferHeight,
    _Out_ ID3D11Texture2D** ppTexture2D,
    _Out_ IPresentationBuffer** ppPresentationBuffer)
{
    com_ptr_failfast<ID3D11Texture2D> texture2D;
    unique_handle sharedResourceHandle;

    // Create a shared Direct3D texture and handle with the passed attributes.
    MakeD3D11Texture(
        pD3D11Device,
        bufferWidth,
        bufferHeight,
        &texture2D,
        out_param(sharedResourceHandle));

    // Add the texture2D to the presentation manager, and get back a presentation buffer.
    com_ptr_failfast<IPresentationBuffer> presentationBuffer;
    FAIL_FAST_IF_FAILED(pPresentationManager->AddBufferFromSharedHandle(
        sharedResourceHandle.get(),
        &presentationBuffer));

    // Return back the texture and buffer presentation buffer.
    *ppTexture2D = texture2D.detach();
    *ppPresentationBuffer = presentationBuffer.detach();
}

void MakeD3D11Texture(
    _In_ ID3D11Device* pD3D11Device,
    _In_ UINT textureWidth,
    _In_ UINT textureHeight,
    _Out_ ID3D11Texture2D** ppTexture2D,
    _Out_ HANDLE* sharedResourceHandle)
{
    D3D11_TEXTURE2D_DESC textureDesc = {};

    // Width and height can be anything within max texture size of the adapter backing the Direct3D
    // device.
    textureDesc.Width = textureWidth;
    textureDesc.Height = textureHeight;

    // MipLevels and ArraySize must be 1.
    textureDesc.MipLevels = 1;
    textureDesc.ArraySize = 1;

    // Format can be one of the following:
    //   DXGI_FORMAT_B8G8R8A8_UNORM
    //   DXGI_FORMAT_R8G8B8A8_UNORM
    //   DXGI_FORMAT_R16G16B16A16_FLOAT
    //   DXGI_FORMAT_R10G10B10A2_UNORM
    //   DXGI_FORMAT_NV12
    //   DXGI_FORMAT_YUY2
    //   DXGI_FORMAT_420_OPAQUE
    // For this 
    textureDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;

    // SampleDesc count and quality must be 1 and 0 respectively.
    textureDesc.SampleDesc.Count = 1;
    textureDesc.SampleDesc.Quality = 0;

    // Usage must be D3D11_USAGE_DEFAULT.
    textureDesc.Usage = D3D11_USAGE_DEFAULT;

    // BindFlags must include D3D11_BIND_SHADER_RESOURCE for RGB textures, and D3D11_BIND_DECODER
    // for YUV textures. For RGB textures, it is likely your application will want to specify
    // D3D11_BIND_RENDER_TARGET in order to render to it.
    textureDesc.BindFlags =
        D3D11_BIND_SHADER_RESOURCE |
        D3D11_BIND_RENDER_TARGET;

    // MiscFlags should include D3D11_RESOURCE_MISC_SHARED and D3D11_RESOURCE_MISC_SHARED_NTHANDLE,
    // and might also include D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE if your application wishes to
    // qualify for MPO and iflip. If D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE is not provided, then the
    // content will not qualify for MPO or iflip, but can still be composed by DWM
    textureDesc.MiscFlags =
        D3D11_RESOURCE_MISC_SHARED |
        D3D11_RESOURCE_MISC_SHARED_NTHANDLE |
        D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE;

    // CPUAccessFlags must be 0.
    textureDesc.CPUAccessFlags = 0;

    // Use Direct3D to create a texture 2D matching the desired attributes.
    com_ptr_failfast<ID3D11Texture2D> texture2D;
    FAIL_FAST_IF_FAILED(pD3D11Device->CreateTexture2D(&textureDesc, nullptr, &texture2D));

    // Create a shared handle for the texture2D.
    unique_handle sharedBufferHandle;
    auto dxgiResource = texture2D.query<IDXGIResource1>();
    FAIL_FAST_IF_FAILED(dxgiResource->CreateSharedHandle(
        nullptr,
        GENERIC_ALL,
        nullptr,
        &sharedBufferHandle));

    // Return the handle to the caller.
    *ppTexture2D = texture2D.detach();
    *sharedResourceHandle = sharedBufferHandle.release();
}
```

## <a name="example-9mdashremoving-presentation-buffers-from-a-presentation-manager-and-object-lifetime"></a>Ejemplo &mdash; 9: Eliminación de búferes de presentación de un administrador de presentación y duración de objetos

Quitar un búfer de presentación del administrador de presentación es tan sencillo como liberar el objeto IPresentationBuffer en un recuento de referencias 0. Sin embargo, cuando esto sucede, no significa necesariamente que se pueda liberar el búfer de presentación. Puede haber casos en los que un búfer todavía esté en uso, como si ese búfer de presentación está visible en pantalla o tiene presentaciones pendientes que hacen referencia a él.

En resumen, el administrador de presentación realizará un seguimiento de cómo la aplicación usa cada búfer de forma directa e indirecta. Realizará un seguimiento de los búferes que se muestran, los que están pendientes y los búferes de referencia, y realizará un seguimiento interno de todo este estado para asegurarse de que un búfer no se libera o anula el registro realmente hasta que realmente ya no está en uso.

Una buena manera de pensar en la duración del búfer es que, si la aplicación libera un IPresentationBuffer, le está contando a la API que ya no usará ese búfer en futuras llamadas. La API de intercambio de composición realizará un seguimiento de esto, así como de cualquier otra manera en que se esté utilizando el búfer, y liberará completamente el búfer solo cuando sea completamente seguro hacerlo.

En resumen, la aplicación debe liberar un IPresentationBuffer cuando haya terminado con él y saber que la API de intercambio de composición liberará completamente el búfer cuando se hayan completado también todos los demás &mdash; usos. [](/windows/win32/api/presentation/nn-presentation-ipresentationbuffer)

A continuación se muestra una ilustración de los conceptos anteriores.

![Eliminación de búferes de presentación](images/removing-presentation-buffers.png)

En este ejemplo, tenemos un administrador de presentación con dos búferes de presentación. El búfer 1 tiene tres referencias que lo mantienen activo.

* La aplicación contiene un **IPresentationBuffer que** hace referencia a él.
* Interna de la API, se almacena como búfer enlazado actual de la superficie de presentación, ya que fue el último búfer enlazado a la aplicación, que luego presentó.
* También hay un presente pendiente en la cola actual que pretende mostrar el búfer 1 en la superficie de presentación.

El búfer 1 también mantiene una referencia en su asignación de textura de Direct3D correspondiente. La aplicación también tiene un [**ID3D11Texture2D que**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) hace referencia a esa asignación.

El búfer 2 no tiene más referencias pendientes del lado de la aplicación, ni la asignación de textura a la que hace referencia, pero el búfer 2 se mantiene activo porque es lo que la superficie de presentación muestra actualmente en pantalla. Cuando se procesa Present 1 y el búfer 1 se muestra en pantalla en su lugar, el búfer 2 no tendrá más referencias y se liberará, liberando a su vez su referencia en su asignación de Textura2D de Direct3D.

### <a name="c-example"></a>Ejemplo de C++

```cpp
void ReleasePresentationManagerBuffersExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager)
{
    com_ptr_failfast<ID3D11Texture2D> texture2D;
    com_ptr_failfast<IPresentationBuffer> newBuffer;

    // Create a new texture/presentation buffer.
    AddNewPresentationBuffer(
        pD3D11Device,
        pPresentationManager,
        200, // Buffer width
        200, // Buffer height
        &texture2D,
        &newBuffer);

    // Release the IPresentationBuffer. This indicates that we have no more intention to use it
    // from the application side. However, if we have any presents outstanding that reference
    // the buffer, it will be kept alive internally and released when all outstanding presents
    // have been retired.
    newBuffer.reset();

    // When the presentation buffer is truly released internally, it will in turn release its
    // reference on the texture2D which it corresponds to. Your application must also release
    // its own references to the texture2D for it to be released.
    texture2D.reset();
}
```

## <a name="example-10mdashresizing-buffers-in-a-presentation-manager"></a>Ejemplo 10: &mdash; Tamaño de búferes en un administrador de presentación

En el ejemplo siguiente se muestra cómo la aplicación realizaría un cambio *de tamaño de* los búferes de presentación. Por ejemplo, si un servicio de streaming de películas transmite 480p pero decide cambiar los formatos a 1080p debido a la disponibilidad de un ancho de banda de red elevado, le gustaría volver a clasificar sus búferes de 480p a 1080p para que pudiera empezar a presentar contenido de 1080p.

En DXGI, esto se conoce como una operación *de cambio de* tamaño. DXGI reosigna todos los búferes de forma atómica, lo que es costoso y puede producir problemas en la pantalla. En el ejemplo siguiente se describe cómo lograr el cambio de tamaño atómico a la par que DXGI en la API de cadena de intercambio de composición. En un ejemplo posterior se muestra  cómo realizar un cambio de tamaño de forma escalonada, espaciado horizontalmente la reasignación entre varios presentaciones, con lo que se consigue un mejor rendimiento que un cambio de tamaño de cadena de intercambio atómico.

### <a name="c-example"></a>Ejemplo de C++

```cpp
void ResizePresentationManagerBuffersExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager) // Previously-made presentation manager.
{
    // Vectors representing the IPresentationBuffer and ID3D11Texture2D collections.
    vector<com_ptr_failfast<ID3D11Texture2D>> textures;
    vector<com_ptr_failfast<IPresentationBuffer>> presentationBuffers;

    // Add 6 50x50 buffers to the presentation manager. See previous example for definition of
    // this function.
    AddBuffersToPresentationManager(
        pD3D11Device,
        pPresentationManager,
        50, // Buffer width
        50, // Buffer height
        6, // Number of buffers
        textures,
        presentationBuffers);

    // Release all the buffers we just added. The presentation buffers internally will be released
    // when any other references are also removed (outstanding presents, display references, etc.).
    textures.clear();
    presentationBuffers.clear();

    // Add 6 new 100x100 buffers to the presentation manager to replace the
    // old ones we just removed.
    AddBuffersToPresentationManager(
        pD3D11Device,
        pPresentationManager,
        100, // Buffer width
        100, // Buffer height
        6, // Number of buffers
        textures,
        presentationBuffers);
}
```

## <a name="example-11mdashsynchronizing-presentation-using-buffer-available-events-and-handling-presentation-manager-lost-events"></a>Ejemplo 11: Sincronización de la presentación mediante eventos disponibles del búfer y control de eventos perdidos &mdash; del administrador de presentación

Si la aplicación va a emitir un presente que implica un búfer de presentación que se ha usado en un presente anterior, debe asegurarse de que el presente anterior está completo para representar y presentar de nuevo el búfer de presentación. La API de cadena de intercambio de composición proporciona un par de mecanismos diferentes para facilitar esta sincronización. El más sencillo es el evento disponible de un búfer de *presentación,* que es un objeto de evento NT  que se  señala cuando un búfer está disponible para su uso (es decir, todos los presentaciones anteriores han entrado en el estado de retirada o retirada) y sin signo en caso contrario. En este ejemplo se muestra cómo usar los eventos disponibles del búfer para seleccionar los búferes disponibles que se deben presentar. También se muestra cómo  escuchar errores de pérdida de dispositivos que son equivalentes a la pérdida de dispositivos DXGI y requieren una recreación del administrador de presentación.

### <a name="presentation-manager-lost-errors"></a>Errores perdidos del administrador de presentación

Un administrador de presentación puede perderse si encuentra un error internamente del que no se puede recuperar. La aplicación debe destruir un administrador de presentación perdido y crear uno nuevo para usarlo en su lugar. Cuando se pierde un administrador de presentación, dejará de aceptar más presentaciones. Cualquier intento de llamar a **Present en** un administrador de presentación perdido devolverá **PRESENTATION_ERROR_LOST**. Sin embargo, todos los demás métodos funcionarán con normalidad. Esto es para asegurarse de que  la aplicación solo necesita comprobar si hay PRESENTATION_ERROR_LOST en las llamadas actuales y no necesita prever ni controlar los errores perdidos en cada llamada API. Si la aplicación desea comprobar o recibir una notificación de errores perdidos fuera de una llamada actual, puede usar el evento perdido devuelto por [**IPresentationManager::GetLostEvent**](/windows/win32/api/presentation/nf-presentation-ipresentationmanager-getlostevent).

### <a name="present-queue-and-timing"></a>Cola y control de tiempo presentes

Los presentaciones emitidos por el administrador de presentación pueden especificar una hora específica de destino. Esta hora de destino es la hora ideal en la que el sistema intentará mostrar el presente. Dado que las pantallas se actualizan a una cadencia finita, es poco probable que el presente se muestre con precisión en el momento especificado, pero se mostrará lo más cerca posible del tiempo.

Esta hora de destino es una hora relativa del sistema o el tiempo que el sistema se ha estado ejecutando desde que se ha activado, en unidades de cientos de nanosegundos. Una manera fácil de calcular la hora actual es consultar el valor actual de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC), dividirlo por la frecuencia QPC del sistema y multiplicarlo por 10 000 000. Los límites de redondeo y precisión se reservan, lo que calculará la hora actual en las unidades aplicables. El sistema también podría obtener la hora actual llamando a [**MfGetSystemTime**](/windows/win32/api/mfidl/nf-mfidl-mfgetsystemtime)o [**QueryInterruptTimePrecise.**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)

Una vez conocida la hora actual, la aplicación normalmente emitirá presentaciones con desplazamientos crecientes con respecto a la hora actual.

Independientemente de la hora de destino, los presentaciones siempre se procesan en orden de cola. Aunque un presente tenga como destino una hora anterior a la anterior, no se procesará hasta que se procese ese presente anterior. Básicamente, esto significa que cualquier presente que no tiene como destino una hora posterior a la anterior invalidará ese presente anterior. También significa que si la aplicación quiere emitir un presente lo antes *posible,* simplemente no puede establecer una hora de destino (en cuyo caso la hora de destino seguiría siendo la que era para el último presente) o establecer una hora de destino de 0. Ambos tendrían el mismo efecto. Si la aplicación no desea esperar a que se completen los presentaciones anteriores para que se realice un nuevo presente, deberá cancelar los presentaciones anteriores. En un ejemplo futuro se describe cómo hacerlo.

![Presentar cola y tiempo](images/present-queue-and-timing.png)

**T=3s:** present 1, 2, 3 all ready, and 3, being the last present, wins out. **T=4s:** present 4, 5, 6 all ready, and 6, being the last present, wins out.

En el diagrama anterior se muestra un ejemplo de los presentaciones pendientes en la cola actual. Present 1 tiene como destino un tiempo de 3 s. Por lo tanto, no se llevará a cabo ningún presente hasta 3s. Sin embargo, present 2 tiene como destino una hora anterior, 2s y present 3 targets 3s también. Por lo tanto, en el momento 3s, los presenta 1, 2 y 3 se completarán, y present 3 será el presente para que su efecto sea real. A continuación, el siguiente presente, 4, se satisfacerá en 4 s, pero inmediatamente se reemplazará por Present 5, que tiene como destino 0s, y Present 6, que no tiene ningún tiempo de destino establecido. Tanto 5 como 6 efectivos tienen efecto *lo antes posible.*

### <a name="c-example"></a>Ejemplo de C++

```cpp
bool SimpleEventSynchronizationExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Build an array of events that we can wait on to perform various actions in our work loop.
    vector<unique_event> waitEvents;

    // The lost event will be the first event in our list. This is an event that signifies that
    // something went wrong in the system (due to extreme conditions such as memory pressure, or
    // driver issues) that indicate that the presentation manager has been lost, and should no
    // longer be used, and instead should be recreated.
    unique_event lostEvent;
    pPresentationManager->GetLostEvent(&lostEvent);
    waitEvents.emplace_back(std::move(lostEvent));

    // Add each buffer's available event to the list of events we will be waiting on.
    for (UINT bufferIndex = 0; bufferIndex < presentationBuffers.size(); bufferIndex++)
    {
        unique_event availableEvent;
        presentationBuffers[bufferIndex]->GetAvailableEvent(&availableEvent);
        waitEvents.emplace_back(std::move(availableEvent));
    }

    // Iterate for 120 presents.
    constexpr UINT numberOfPresents = 120;
    for (UINT onPresent = 0; onPresent < numberOfPresents; onPresent++)
    {
        // Advance our present time 1/10th of a second in the future. Note the API accepts
        // time in 100ns units, or 1/1e7 of a second, meaning that 1 million units correspond to
        // 1/10th of a second.
        presentTime.value += 1'000'000;

        // Wait for the lost event or an available buffer. Since WaitForMultipleObjects prioritizes
        // lower-indexed events, it is recommended to put any higher importance events (like the
        // lost event) first, and then follow up with buffer available events.
        DWORD waitResult = WaitForMultipleObjects(
            static_cast<UINT>(waitEvents.size()),
            reinterpret_cast<HANDLE*>(waitEvents.data()),
            FALSE,
            INFINITE);

        // Failfast if the wait hit an error.
        FAIL_FAST_IF((waitResult - WAIT_OBJECT_0) >= waitEvents.size());

        // Our lost event was the first event in the array. If this is signaled, the caller
        // should recreate the presentation manager. This is very similar to how Direct3D devices
        // can be lost. Assume our caller knows to handle this return value appropriately.
        if (waitResult == WAIT_OBJECT_0)
        {
            return false;
        }

        // Otherwise, compute the buffer corresponding to the available event that was signaled.
        UINT bufferIndex = waitResult - (WAIT_OBJECT_0 + 1);

        // Draw red to that buffer
        DrawColorToSurface(
            pD3D11Device,
            textures[bufferIndex],
            1.0f, // red
            0.0f, // green
            0.0f); // blue

        // Bind the presentation buffer to the presentation surface. Changes in this binding will take
        // effect on the next present, and the binding persists across presents. That is, any number
        // of subsequent presents will imply this binding until it is changed. It is completely fine
        // to only update buffers for a subset of the presentation surfaces owned by a presentation
        // manager on a given present - the implication is that it simply didn't update.
        //
        // Similarly, note that if your application were to call SetBuffer on the same presentation
        // surface multiple times without calling present, this is fine. The policy is last writer
        // wins.
        //
        // Your application may present without first binding a presentation surface to a buffer.
        // The result will be that presentation surface will simply have no content on screen,
        // similar to how DComp and WinComp surfaces appear in a tree before they are rendered to.
        // In that case system content will show through where the buffer would have been.
        //
        // Your application may also set a 'null' buffer binding after previously having bound a
        // buffer and present - the end result is the same as if your application had presented
        // without ever having set the content.
        pPresentationSurface->SetBuffer(presentationBuffers[bufferIndex].get());

        // Present at the targeted time. Note that a present can target only a single time. If an
        // application wants to updates two buffers at two different times, then it must present
        // two times.
        //
        // Presents are always processed in queue order. A present will not take effect before any
        // previous present in the queue, even if it targets an earlier time. In such a case, when
        // the previous present is processed, the next present will also be processed immediately,
        // and override that previous present.
        //
        // For this reason, if your application wishes to present "now" or "early as possible", then
        // it can simply present, without setting a target time. The implied target time will be 0,
        // and the new present will override the previous present.
        //
        // If your application wants to present truly "now", and not wait for previous presents in the
        // queue to be processed, then it will need to cancel previous presents. A future example
        // demonstrates how to do this.
        //
        // Your application will receive PRESENTATION_ERROR_LOST if it attempts to Present a lost
        // presentation manager. This is the only call that will return such an error. A lost
        // presentation manager functions normally in every other case, so applications need only
        // to handle this error at the time they call Present.
        pPresentationManager->SetTargetTime(presentTime);
        HRESULT hrPresent = pPresentationManager->Present();
        if (hrPresent == PRESENTATION_ERROR_LOST)
        {
            // Our presentation manager has been lost. Return 'false' to the caller to indicate that
            // the presentation manager should be recreated.
            return false;
        }
        else
        {
            FAIL_FAST_IF_FAILED(hrPresent);
        }
    }

    return true;
}

void DrawColorToSurface(
    _In_ ID3D11Device* pD3D11Device,
    _In_ const com_ptr_failfast<ID3D11Texture2D>& texture2D,
    _In_ float redValue,
    _In_ float greenValue,
    _In_ float blueValue)
{
    com_ptr_failfast<ID3D11DeviceContext> D3DDeviceContext;
    com_ptr_failfast<ID3D11RenderTargetView> renderTargetView;

    // Get the immediate context from the D3D11 device.
    pD3D11Device->GetImmediateContext(&D3DDeviceContext);

    // Create a render target view of the passed texture.
    auto resource = texture2D.query<ID3D11Resource>();
    FAIL_FAST_IF_FAILED(pD3D11Device->CreateRenderTargetView(
        resource.get(),
        nullptr,
        renderTargetView.addressof()));

    // Clear the texture with the specified color.
    float clearColor[4] = { redValue, greenValue, blueValue, 1.0f }; // red, green, blue, alpha
    D3DDeviceContext->ClearRenderTargetView(renderTargetView.get(), clearColor);
}
```

## <a name="example-12mdashadvanced-synchronizationmdashthrottling-workflow-to-the-size-of-the-outstanding-present-queue-using-present-synchronization-fences-and-handling-presentation-manager-lost-events"></a>Ejemplo 12 Flujo de trabajo de limitación de sincronización avanzada al tamaño de la cola actual pendiente mediante barreras de sincronización actuales y control de eventos perdidos del &mdash; &mdash; administrador de presentación

En el ejemplo siguiente se muestra cómo la aplicación puede enviar un gran número de presentaciones para el futuro y, a continuación, se queda en suspensión hasta que el número de presentaciones que todavía están pendientes se reduce a una cantidad específica. Los marcos como Windows Media Foundation limitar esta manera para minimizar el número de reactivaciones de CPU que se producen, a la vez que se garantiza que la cola actual no se agota (lo que impediría una reproducción fluida y provocaría un problema). Esto tiene el efecto de minimizar el uso de energía de CPU durante el flujo de trabajo de presentación. La aplicación pondrá en cola el número máximo de presentaciones (en función del número de búferes de presentación que haya asignado) y, a continuación, se suspensión hasta justo antes de que se agote la cola actual para rellenar la cola.

### <a name="c-example"></a>Ejemplo de C++

```cpp
bool FenceSynchronizationExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Get present retiring fence.
    com_ptr_failfast<ID3D11Fence> presentRetiringFence;
    FAIL_FAST_IF_FAILED(pPresentationManager->GetPresentRetiringFence(
        IID_PPV_ARGS(&presentRetiringFence)));

    // Get the lost event to query before presentation.
    unique_event lostEvent;
    pPresentationManager->GetLostEvent(&lostEvent);

    // Create an event to synchronize to our queue depth with. We'll use Direct3D to signal this event
    // when our synchronization fence indicates reaching a specific present.
    unique_event presentQueueSyncEvent;
    presentQueueSyncEvent.create(EventOptions::ManualReset);

    // Cycle the present queue 10 times.
    constexpr UINT numberOfPresentRefillCycles = 10;
    for (UINT onRefillCycle = 0; onRefillCycle < numberOfPresentRefillCycles; onRefillCycle++)
    {
        // Fill up presents for all presentation buffers. We compare the presentation manager's
        // next present ID to the present confirmed fence's value to figure out how
        // far ahead we are. We stop when we've issued presents for all buffers.
        while ((pPresentationManager->GetNextPresentId() -
                presentRetiringFence->GetCompletedValue()) < presentationBuffers.size())
        {
            // Present buffers in cyclical pattern. We can figure out the current buffer to
            // present by taking the modulo of the next present ID by the number of buffers. Note that the
            // first present of a presentation manager always has a present ID of 1 and increments by 1 on
            // each subsequent present. A present ID of 0 is conceptually meant to indicate that "no
            // presents have taken place yet".
            UINT bufferIndex = static_cast<UINT>(
                pPresentationManager->GetNextPresentId() % presentationBuffers.size());

            // Assert that the passed buffer is tracked as available for presentation. Because we throttle
            // based on the total number of buffers, this should always be true.
            NT_ASSERT(presentationBuffers[bufferIndex]->IsAvailable());

            // Advance our present time 1/10th of a second in the future.
            presentTime.value += 1'000'000;

            // Draw red to the texture.
            DrawColorToSurface(
                pD3D11Device,
                textures[bufferIndex],
                1.0f, // red
                0.0f, // green
                0.0f); // blue

            // Bind the presentation buffer to the presentation surface.
            pPresentationSurface->SetBuffer(presentationBuffers[bufferIndex].get());

            // Present at the targeted time.
            pPresentationManager->SetTargetTime(presentTime);
            HRESULT hrPresent = pPresentationManager->Present();
            if (hrPresent == PRESENTATION_ERROR_LOST)
            {
                // Our presentation manager has been lost. Return 'false' to the caller to indicate that
                // the presentation manager should be recreated.
                return false;
            }
            else
            {
                FAIL_FAST_IF_FAILED(hrPresent);
            }
        };

        // Now that the buffer is full, go to sleep until the present queue has been drained to
        // the desired queue depth. To figure out the appropriate present to wake on, we subtract
        // the desired wake queue depth from the presentation manager's last present ID. We
        // use Direct3D's SetEventOnCompletion to signal our wait event when that particular present
        // is retiring, and then wait on that event. Note that the semantic of SetEventOnCompletion
        // is such that even if we happen to call it after the fence has already reached the
        // requested value, the event will be set immediately.
        constexpr UINT wakeOnQueueDepth = 2;
        presentQueueSyncEvent.ResetEvent();
        FAIL_FAST_IF_FAILED(presentRetiringFence->SetEventOnCompletion(
            pPresentationManager->GetNextPresentId() - 1 - wakeOnQueueDepth,
            presentQueueSyncEvent.get()));

        HANDLE waitHandles[] = { lostEvent.get(), presentQueueSyncEvent.get() };
        DWORD waitResult = WaitForMultipleObjects(
            ARRAYSIZE(waitHandles),
            waitHandles,
            FALSE,
            INFINITE);

        // Failfast if we hit an error during our wait.
        FAIL_FAST_IF((waitResult - WAIT_OBJECT_0) >= ARRAYSIZE(waitHandles));

        if (waitResult == WAIT_OBJECT_0)
        {
            // The lost event was signaled - return 'false' to the caller to indicate that
            // the presentation manager was lost.
            return false;
        }

        // Iterate into another refill cycle.
    }

    return true;
}
```

## <a name="example-13mdashvsync-interrupts-and-hardware-flip-queue-support"></a>Ejemplo 13 &mdash; Interrupciones de VSync y compatibilidad con la cola de volteo de hardware

Junto con esta API se ha introducido una nueva forma de administración de la cola de volteo denominada cola de volteo de *hardware,* lo que básicamente permite que el hardware de GPU administre los presenta completamente independientemente de la CPU. La principal ventaja de esto es la eficiencia energética. Cuando no es necesario que la CPU esté implicada en el proceso de presentación, se dibuja menos potencia.

La desventaja de que el identificador de GPU se presente de forma independiente es que el estado de la CPU ya no se puede reflejar inmediatamente cuando se muestran los presentes. Los conceptos de api de intercambio de composición, como los eventos disponibles del búfer, las barreras de sincronización y las estadísticas actuales, no se actualizarán inmediatamente. En su lugar, la GPU solo actualizará periódicamente el estado de la CPU en cuanto a los presentaciones que se han mostrado. Esto significa que los comentarios a las aplicaciones sobre el estado actual tendrán una latencia.

Normalmente, a la aplicación le importará cuando se muestran algunos presentes, pero no tanto de otros. Por ejemplo, si se presenta el problema 10 de la aplicación, puede decidir que quiere saber cuándo se muestra el 8, para que pueda empezar a rellenar de nuevo la cola actual. En este caso, el único presente del que realmente desea recibir comentarios es el 8. No tiene previsto hacer nada cuando se muestran 1-7 o 9.

Si presenta el estado de la CPU de actualización depende de si el hardware de GPU está configurado para generar una interrupción de VSync cuando se muestra ese presente. Esta interrupción de VSync activa la CPU si aún no está activa y, a su vez, la CPU ejecuta código de nivel de kernel especial para actualizarse en los presentaciones que se han producido en la GPU desde la última vez que se comprobó, actualizando a su vez los mecanismos de comentarios, como los eventos disponibles del búfer, la barrera de retirada actual y las estadísticas presentes.

Para permitir que la aplicación indique explícitamente qué presentaciones deben emitir una interrupción de VSync, el administrador de presentación expone un método [**IPresentationManager::ForceVSyncInterrupt,**](/windows/win32/api/presentation/nf-presentation-ipresentationmanager-forcevsyncinterrupt) que especifica si los presentaciones posteriores deben emitir una interrupción de VSync. Esta configuración se aplica a todos los futuros presentes hasta que se cambie, de forma muy parecido a [**IPresentationManager::SetTargetTime**](/windows/win32/api/presentation/nf-presentation-ipresentationmanager-settargettime) e [**IPresentationManager::SetPreferredPresentDuration**](/windows/win32/api/presentation/nf-presentation-ipresentationmanager-setpreferredpresentduration).

Si esta configuración está habilitada en un presente determinado, el hardware notificará inmediatamente a la CPU cuando se muestra ese presente, con más potencia, pero asegurándose de que la CPU se notifica inmediatamente cuando se produce un presente para permitir que las aplicaciones respondan lo antes posible. Si esta configuración está deshabilitada en un presente determinado, el sistema podrá aplazar la actualización de la CPU cuando se muestra el presente ahorrando energía, pero aplazando los &mdash; comentarios.

Normalmente, la aplicación no forzará la interrupción de VSync para los presentaciones, excepto un presente con el que desea sincronizarse. En el ejemplo anterior, dado que la aplicación quería reactivar cuando se mostró el número 8 presente para rellenar su cola actual, solicitaría que presente 8 señale una interrupción de VSync, pero presenta 1-7 y present 9 no. 

De forma predeterminada, si la aplicación no configura esta opción, el administrador de presentación siempre señalará la interrupción de VSync cuando se muestra cada presente. Las aplicaciones que no están interesadas en el uso de energía, o que no son conscientes de la compatibilidad con la cola de volteo de hardware, simplemente no pueden llamar a **ForceVSyncInterrupt** y se garantizará que se sincronicen correctamente como resultado. Las aplicaciones que son conscientes de la compatibilidad con la cola de volteo de hardware pueden controlar explícitamente esta configuración para mejorar la eficacia de energía.

A continuación se muestra un diagrama que describe el comportamiento de la API con respecto a la configuración de interrupción de VSync.

![Interrupciones de VSync](images/vsync-interrupts.png)

### <a name="c-example"></a>Ejemplo de C++

```cpp
bool ForceVSyncInterruptPresentsExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Get present retiring fence.
    com_ptr_failfast<ID3D11Fence> presentRetiringFence;
    FAIL_FAST_IF_FAILED(pPresentationManager->GetPresentRetiringFence(
        IID_PPV_ARGS(&presentRetiringFence)));

    // Get the lost event to query before presentation.
    unique_event lostEvent;
    pPresentationManager->GetLostEvent(&lostEvent);

    // Create an event to synchronize to our queue depth with. We will use Direct3D to signal this event
    // when our synchronization fence indicates reaching a specific present.
    unique_event presentQueueSyncEvent;
    presentQueueSyncEvent.create(EventOptions::ManualReset);

    // Issue 10 presents, and wake when the present queue is 2 entries deep (which happens when
    // present 7 is retiring).
    constexpr UINT wakeOnQueueDepth = 2;
    constexpr UINT numberOfPresents = 10;
    const UINT presentIdToWakeOn = numberOfPresents - 1 - wakeOnQueueDepth;
    while (pPresentationManager->GetNextPresentId() <= numberOfPresents)
    {
        UINT bufferIndex = static_cast<UINT>(
            pPresentationManager->GetNextPresentId() % presentationBuffers.size());

        // Advance our present time 1/10th of a second in the future.
        presentTime.value += 1'000'000;

        // Draw red to the texture.
        DrawColorToSurface(
            pD3D11Device,
            textures[bufferIndex],
            1.0f, // red
            0.0f, // green
            0.0f); // blue

        // Bind the presentation buffer to the presentation surface.
        pPresentationSurface->SetBuffer(presentationBuffers[bufferIndex].get());

        // Present at the targeted time.
        pPresentationManager->SetTargetTime(presentTime);

        // If this present is not going to retire the present that we want to wake on when it is shown, then
        // we don't need immediate updates to buffer available events, present retiring fence, or present
        // statistics. As such, we can mark it as not requiring a VSync interrupt, to allow for greater
        // power efficiency on machines with hardware flip queue support.
        bool forceVSyncInterrupt = (pPresentationManager->GetNextPresentId() == (presentIdToWakeOn + 1));
        pPresentationManager->ForceVSyncInterrupt(forceVSyncInterrupt);

        HRESULT hrPresent = pPresentationManager->Present();
        if (hrPresent == PRESENTATION_ERROR_LOST)
        {
            // Our presentation manager has been lost. Return 'false' to the caller to indicate that
            // the presentation manager should be recreated.
            return false;
        }
        else
        {
            FAIL_FAST_IF_FAILED(hrPresent);
        }
    }

    // Now that the buffer is full, go to sleep until presentIdToWakeOn has begun retiring. We
    // configured the subsequent present to force a VSync interrupt when it is shown, which will ensure
    // this wait is completed immediately.
    presentQueueSyncEvent.ResetEvent();
    FAIL_FAST_IF_FAILED(presentRetiringFence->SetEventOnCompletion(
        presentIdToWakeOn,
        presentQueueSyncEvent.get()));

    HANDLE waitHandles[] = { lostEvent.get(), presentQueueSyncEvent.get() };
    DWORD waitResult = WaitForMultipleObjects(
        ARRAYSIZE(waitHandles),
        waitHandles,
        FALSE,
        INFINITE);

    // Failfast if we hit an error during our wait.
    FAIL_FAST_IF((waitResult - WAIT_OBJECT_0) >= ARRAYSIZE(waitHandles));

    if (waitResult == WAIT_OBJECT_0)
    {
        // The lost event was signaled - return 'false' to the caller to indicate that
        // the presentation manager was lost.
        return false;
    }

    return true;
}
```

## <a name="example-14mdashcanceling-presents-scheduled-for-the-future"></a>Ejemplo 14: &mdash; Cancelación de presentaciones programadas para el futuro

Las aplicaciones multimedia que se presentan en cola profundamente para el futuro pueden decidir cancelar los presentaciones que han emitido previamente. Esto puede ocurrir, por ejemplo, si la aplicación reproduce un vídeo, ha emitido un gran número de fotogramas para el futuro y el usuario decide pausar la reproducción de vídeo. En este caso, la aplicación querrá quedarse con el marco actual y cancelar los fotogramas futuros que aún no se hayan poner en cola. Esto también puede ocurrir si una aplicación multimedia decide mover la reproducción a un punto diferente del vídeo. En este caso, la aplicación querrá cancelar todos los presentaciones que aún no se han puesto en cola para la posición anterior en el vídeo y reemplazarlos por presentaciones para la nueva posición. En este caso, después de cancelar los presentaciones anteriores, la aplicación puede emitir nuevos presentaciones en el futuro correspondientes al nuevo punto del vídeo.

### <a name="c-example"></a>Ejemplo de C++

```cpp
void PresentCancelExample(
    _In_ IPresentationManager* pPresentationManager,
    _In_ UINT64 firstPresentIDToCancelFrom)

{
    // Assume we've issued a number of presents in the future. Something happened in the app, and
    // we want to cancel the issued presents that occur after a specified time or present ID. This
    // may happen, for example, when the user pauses playback from inside a media application. The
    // application will want to cancel all presents posted targeting beyond the pause time. The
    // cancel will apply to all previously posted presents whose present IDs are at least
    // 'firstPresentIDToCancelFrom'. Note that Present IDs are always unique, and never recycled,
    // so even if a present is canceled, no subsequent present will ever reuse its present ID.
    //
    // Also note that if some presents we attempt to cancel can't be canceled because they've
    // already started queueing, then no error will be returned, they simply won't be canceled as
    // requested. Cancelation takes a "best effort" approach.
    FAIL_FAST_IF_FAILED(pPresentationManager->CancelPresentsFrom(firstPresentIDToCancelFrom));

    // In the case where the media application scrubbed to a different position in the video, it may now
    // choose to issue new presents to replace the ones canceled. This is not illustrated here, but
    // previous examples that demonstrate presentation show how this may be achieved.
}
```

## <a name="example-15mdashstaggered-buffer-resize-operation-for-improved-performance"></a>Ejemplo 15 Operación &mdash; de cambio de tamaño de búfer escalonado para mejorar el rendimiento

En este ejemplo se muestra cómo la aplicación puede escalonar el tamaño del búfer para mejorar el rendimiento sobre DXGI. Recuerde el ejemplo de cambio de tamaño anterior, en el que un cliente del servicio de streaming de películas desea cambiar la resolución de reproducción de 720p a 1080p. En DXGI, la aplicación realizaría una operación de cambio de tamaño en la cadena de intercambio DXGI, que desecharía de forma atómica todos los búferes anteriores, y reasignaría todos los nuevos búferes de 1080p a la vez y los agregaría a la cadena de intercambio. Este tipo de cambio de tamaño atómico de los búferes es costoso y tiene el potencial de tardar mucho tiempo y provocar problemas. La nueva API proporciona un control más preciso sobre los búferes de presentación individuales. Por lo tanto, los búferes se pueden reasignar y reemplazar uno a uno en varios presentaciones para dividir la carga de trabajo a lo largo del tiempo. Esto tiene menos impacto en cualquiera de los presentes y es mucho menos probable que cause problemas. Básicamente, para un administrador de presentación con n búferes de presentación, para los "n" presentes, la aplicación puede quitar un búfer de presentación antiguo con el tamaño anterior, asignar un nuevo búfer de presentación con el nuevo tamaño y presentarlo. Después de que se presente "n", todos los búferes tendrán el nuevo tamaño.

### <a name="c-example"></a>Ejemplo de C++

```cpp
bool StaggeredResizeExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>> textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>> presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Assume textures/presentationBuffers vector contains 10 100x100 buffers, and we want to resize
    // our swapchain to 200x200. Instead of reallocating 10 200x200 buffers all at once,
    // like DXGI does today, we can stagger the reallocation across multiple presents. For
    // each present, we can allocate one buffer at the new size, and replace one old buffer
    // at the old size with the new one at the new size. After 10 presents, we will have
    // reallocated all our buffers, and we will have done so in a manner that's much less
    // likely to produce delays or glitches.
    constexpr UINT numberOfBuffers = 10;
    for (UINT bufferIndex = 0; bufferIndex < numberOfBuffers; bufferIndex++)
    {
        // Advance our present time 1/10th of a second in the future.
        presentTime.value += 1'000'000;

        // Release the old texture/presentation buffer at the presented index.
        auto& replacedTexture = textures[bufferIndex];
        auto& replacedPresentationBuffer = presentationBuffers[bufferIndex];
        replacedTexture.reset();
        replacedPresentationBuffer.reset();

        // Create a new texture/presentation buffer in its place.
        AddNewPresentationBuffer(
            pD3D11Device,
            pPresentationManager,
            200, // Buffer width
            200, // Buffer height
            &replacedTexture,
            &replacedPresentationBuffer);

        // Draw red to the new texture.
        DrawColorToSurface(
            pD3D11Device,
            replacedTexture,
            1.0f, // red
            0.0f, // green
            0.0f); // blue

        // Bind the presentation buffer to the presentation surface.
        pPresentationSurface->SetBuffer(replacedPresentationBuffer.get());

        // Present at the targeted time.
        pPresentationManager->SetTargetTime(presentTime);
        HRESULT hrPresent = pPresentationManager->Present();
        if (hrPresent == PRESENTATION_ERROR_LOST)
        {
            // Our presentation manager has been lost. Return 'false' to the caller to indicate that
            // the presentation manager should be recreated.
            return false;
        }
        else
        {
            FAIL_FAST_IF_FAILED(hrPresent);
        }
    }

    return true;
}
```

## <a name="example-16mdashreading-and-processing-present-statistics"></a>Ejemplo 16: &mdash; Lectura y procesamiento de estadísticas presentes

Los informes de API presentan estadísticas para cada presente que se envía. En un nivel alto, las estadísticas presentes son un mecanismo de comentarios que describe cómo el sistema procesó o mostró un presente determinado. Hay diferentes tipos de estadísticas que la aplicación puede registrar para recibir y la infraestructura de estadísticas de la propia API está pensada para ser ampliable, por lo que se pueden agregar más tipos de estadísticas en el futuro. Esta API describe cómo volver a leer las estadísticas y describe los tipos de estadísticas definidos hoy en día y qué información transmiten en un nivel alto.

### <a name="c-example"></a>Ejemplo de C++

```cpp
// This is an identifier we'll assign to our presentation surface that will be used to reference that
// presentation surface in statistics. This is to avoid referring to a presentation surface by pointer
// in a statistics structure, which has unclear refcounting and lifetime semantics.
static constexpr UINT_PTR myPresentedContentTag = 12345;

bool StatisticsExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Register to receive 3 types of statistics.
    FAIL_FAST_IF_FAILED(pPresentationManager->EnablePresentStatisticsKind(
        PresentStatisticsKind_CompositionFrame,
        true));
    FAIL_FAST_IF_FAILED(pPresentationManager->EnablePresentStatisticsKind(
        PresentStatisticsKind_PresentStatus,
        true));
    FAIL_FAST_IF_FAILED(pPresentationManager->EnablePresentStatisticsKind(
        PresentStatisticsKind_IndependentFlipFrame,
        true));

    // Stats come back referencing specific presentation surfaces. We assign 'tags' to presentation
    // surfaces in the API that statistics will use to reference the presentation surface in a
    // statistic.
    pPresentationSurface->SetTag(myPresentedContentTag);

    // Build an array of events that we can wait on.
    vector<unique_event> waitEvents;

    // The lost event will be the first event in our list. This is an event that signifies that
    // something went wrong in the system (due to extreme conditions like memory pressure, or
    // driver issues) that indicate that the presentation manager has been lost, and should no
    // longer be used, and instead should be recreated.
    unique_event lostEvent;
    FAIL_FAST_IF_FAILED(pPresentationManager->GetLostEvent(&lostEvent));
    waitEvents.emplace_back(std::move(lostEvent));

    // The statistics event will be the second event in our list. This event will be signaled
    // by the presentation manager when there are statistics to read back.
    unique_event statisticsEvent;
    FAIL_FAST_IF_FAILED(pPresentationManager->GetPresentStatisticsAvailableEvent(&statisticsEvent));
    waitEvents.emplace_back(std::move(statisticsEvent));

    // Add each buffer's available event to the list of events we will be waiting on.
    for (UINT bufferIndex = 0; bufferIndex < presentationBuffers.size(); bufferIndex++)
    {
        unique_event availableEvent;
        presentationBuffers[bufferIndex]->GetAvailableEvent(&availableEvent);
        waitEvents.emplace_back(std::move(availableEvent));
    }

    // Iterate our workflow 120 times.
    constexpr UINT iterationCount = 120;
    for (UINT i = 0; i < iterationCount; i++)
    {
        // Wait for an event to be signaled.
        DWORD waitResult = WaitForMultipleObjects(
            static_cast<UINT>(waitEvents.size()),
            reinterpret_cast<HANDLE*>(waitEvents.data()),
            FALSE,
            INFINITE);

        // Failfast if the wait hit an error.
        FAIL_FAST_IF((waitResult - WAIT_OBJECT_0) >= waitEvents.size());

        // Our lost event was the first event in the array. If this is signaled, then the caller
        // should recreate the presentation manager. This is very similar to how Direct3D devices
        // can be lost. Assume our caller knows to handle this return value appropriately.
        if (waitResult == WAIT_OBJECT_0)
        {
            return false;
        }

        // The second event in the array is the statistics event. If this event is signaled,
        // read and process our statistics.
        if (waitResult == (WAIT_OBJECT_0 + 1))
        {
            StatisticsExample_ProcessStatistics(pPresentationManager);
        }
        // Otherwise, the event corresponds to a buffer available event that is signaled.
        // Compute the buffer for the available event that was signaled and present a
        // frame.
        else
        {
            DWORD bufferIndex = waitResult - (WAIT_OBJECT_0 + 2);

            // Draw red to the texture.
            DrawColorToSurface(
                pD3D11Device,
                textures[bufferIndex],
                1.0f, // red
                0.0f, // green
                0.0f); // blue

            // Bind the texture to the presentation surface.
            pPresentationSurface->SetBuffer(presentationBuffers[bufferIndex].get());

            // Advance our present time 1/10th of a second in the future.
            presentTime.value += 1'000'000;

            // Present at the targeted time.
            pPresentationManager->SetTargetTime(presentTime);
            HRESULT hrPresent = pPresentationManager->Present();
            if (hrPresent == PRESENTATION_ERROR_LOST)
            {
                // Our presentation manager has been lost. Return 'false' to the caller to indicate that
                // the presentation manager should be recreated.
                return false;
            }
            else
            {
                FAIL_FAST_IF_FAILED(hrPresent);
            }
        }
    }

    return true;
}

void StatisticsExample_ProcessStatistics(
    _In_ IPresentationManager* pPresentationManager)
{
    // Dequeue a single present statistics item. This will return the item
    // and pop it off the queue of statistics.
    com_ptr_failfast<IPresentStatistics> presentStatisticsItem;
    pPresentationManager->GetNextPresentStatistics(&presentStatisticsItem);

    // Read back the present ID this corresponds to.
    UINT64 presentId = presentStatisticsItem->GetPresentId();
    UNREFERENCED_PARAMETER(presentId);

    // Switch on the type of statistic this item corresponds to.
    switch (presentStatisticsItem->GetKind())
    {
        case PresentStatisticsKind_PresentStatus:
        {
            // Present status statistics describe whether a given present was queued for display,
            // skipped due to some future present being a better candidate to display on a given
            // frame, or canceled via the API.
            auto presentStatusStatistics = presentStatisticsItem.query<IPresentStatusStatistics>();

            // Read back the status
            PresentStatus status = presentStatusStatistics->GetPresentStatus();
            UNREFERENCED_PARAMETER(status);

            // Possible values for status:
            //   PresentStatus_Queued
            //   PresentStatus_Skipped
            //   PresentStatus_Canceled;

            // Depending on the status returned, your application can adjust their workflow
            // accordingly. For example, if your application sees that a large percentage of their
            // presents are skipped, it means they are presenting more frames than the system can
            // display. In such a case, your application might decided to lower the rate at which
            // you present frames.
        }
        break;

        case PresentStatisticsKind_CompositionFrame:
        {
            // Composition frame statistics describe how a given present was used in a DWM frame.
            // It includes information such as which monitors displayed the present, whether the
            // present was composed or directly scanned out via an MPO plane, and rendering
            // properties such as what transforms were applied to the rendering. Composition
            // frame statistics are not issued for iflip presents - only for presents issued by the
            // compositor. iflip presents have their own type of statistic (described next).
            auto compositionFrameStatistics =
                presentStatisticsItem.query<ICompositionFramePresentStatistics>();

            // Stats should come back for the present statistics item that we tagged earlier.
            NT_ASSERT(compositionFrameStatistics->GetContentTag() == myPresentedContentTag);

            // The composition frame ID indicates the DWM frame ID that the present was used
            // in.
            CompositionFrameId frameId = compositionFrameStatistics->GetCompositionFrameId();

            // Get the display instance array to indicate which displays showed the present. Each
            // instance of the presentation surface will have an entry in this array. For example,
            // if your application adds the same presentation surface to four different visuals in the
            // visual tree, then each instance in the tree will have an entry in the display instance
            // array. Similarly, if the presentation surface shows up on multiple monitors, then each
            // monitor instance will be accounted for in the display instance array that is
            // returned.
            //
            // Note that the pointer returned from GetDisplayInstanceArray is valid for the
            // lifetime of the ICompositionFramePresentStatistics. Your application must not attempt
            // to read this pointer after the ICompositionFramePresentStatistics has been released
            // to a refcount of 0.
            UINT displayInstanceArrayCount;
            const CompositionFrameDisplayInstance* pDisplayInstances;
            compositionFrameStatistics->GetDisplayInstanceArray(
                &displayInstanceArrayCount,
                &pDisplayInstances);

            for (UINT i = 0; i < displayInstanceArrayCount; i++)
            {
                const auto& displayInstance = pDisplayInstances[i];

                // The following are fields that are available in a display instance.

                // The LUID, VidPnSource, and unique ID of the output and its owning
                // adapter. The unique ID will be bumped when a LUID/VidPnSource is
                // recycled. Applications should use the unique ID to determine when
                // this happens so that they don't try and correlate stats from one
                // monitor with another.
                displayInstance.outputAdapterLUID;
                displayInstance.outputVidPnSourceId;
                displayInstance.outputUniqueId;

                // The instanceKind field indicates how the present was used. It
                // indicates that the present was composed (rendered to DWM's backbuffer),
                // scanned out (via MPO/DFlip) or composed to an intermediate buffer by DWM
                // for effects.
                displayInstance.instanceKind;

                // The finalTransform field indicates the transform at which the present was
                // shown in world space. It will include all ancestor visual transforms and
                // can be used to know how it was rendered in the global visual tree.
                displayInstance.finalTransform;

                // The requiredCrossAdapterCopy field indicates whether or not we needed to
                // copy your application's buffer to a different adapter in order to display
                // it. Applications should use this to determine whether or not they should
                // reallocate their buffers onto a different adapter for better performance.
                displayInstance.requiredCrossAdapterCopy;

                // The colorSpace field indicates the colorSpace of the output that the
                // present was rendered to.
                displayInstance.colorSpace;

                // For example, if your application sees that the finalTransform is scaling your
                // content by 2x, you might elect to pre-render that scale into your presentation
                // surface, and then add a 1/2 scale. At which point, the finalTransform should
                // be 1x, and some MPO hardware will be more likely to MPO a presentation surface
                // with a 1x scale applied, since some hardware has a maximum they are able to
                // scale in an MPO plane. Similarly, if your application's content is being scaled
                // down on screen, you may wish to simply render its content at a
                // smaller scale to conserve resources, and apply an enlargement transform.
            }

            // Additionally, we can use the CompositionFrameId reported by the statistic
            // to query timing-related information about that specific frame via the new
            // composition timing API, such as when that frame showed up on screen.
            // Note this is achieved using a separate API from the composition swapchain API, but
            // using the composition frame ID reported in the composition swapchain API to
            // properly specify which frame your application wants timing information from.
            COMPOSITION_FRAME_TARGET_STATS frameTargetStats;
            COMPOSITION_TARGET_STATS targetStats[4];
            frameTargetStats.targetCount = ARRAYSIZE(targetStats);
            frameTargetStats.targetStats = targetStats;

            // Specify the frameId that we got from stats in order to pass to the call
            // below and retrieve timing information about that frame.
            frameTargetStats.frameId = frameId;
            FAIL_FAST_IF_FAILED(DCompositionGetTargetStatistics(1, &frameTargetStats));

            // If the frameTargetStats comes back with a 0 frameId, it means the frame isn't
            // part of statistics. This might mean that it has expired out of
            // DCompositionGetTargetStatistics history, but that call keeps a history buffer
            // roughly equivalent to ~5 seconds worth of frame history, so if your application
            // is processing statistics from the presentation manager relatively regularly,
            // by all accounts it shouldn't worry about DCompositionGetTargetStatistics
            // history expiring. The more likely scenario when this occurs is that it's too
            // early, and that this frame isn't part of statistics YET. In that case, your application
            // should defer processing for this frame, and try again later. For the purposes
            // if sample brevity, we don't bother trying again here. A good method to use would
            // be to add this present info to a list of presents that we haven't gotten target
            // statistics for yet, and try again for all presents in that list any time we get
            // a new PresentStatisticsKind_CompositionFrame for a future frame.
            if (frameTargetStats.frameId == frameId)
            {
                // The targetCount will represent the count of outputs the given frame
                // applied to.
                frameTargetStats.targetCount;

                // The targetTime corresponds to the wall clock QPC time DWM was
                // targeting for the frame.
                frameTargetStats.targetTime;

                for (UINT i = 0; i < frameTargetStats.targetCount; i++)
                {
                    const auto& targetStat = frameTargetStats.targetStats[i];

                    // The present time corresponds to the targeted present time of the composition
                    // frame.
                    targetStat.presentTime;

                    // The target ID corresponds to the LUID/VidPnSourceId/Unique ID for the given
                    // target.
                    targetStat.targetId;

                    // The completedStats convey information about the time a compositor frame was
                    // completed, which marks the time any of its associated composition swapchain API
                    // presents entered the displayed state. In particular, your application might wish
                    // to use the 'time' to know if a present showed at a time it expected.
                    targetStat.completedStats.presentCount;
                    targetStat.completedStats.refreshCount;
                    targetStat.completedStats.time;

                    // There is various other timing statistics information conveyed by
                    // DCompositionGetTargetStatistics.
                }
            }
        }
        break;

        case PresentStatisticsKind_IndependentFlipFrame:
        {
            // Independent flip frame statistics describe a present that was shown via
            // independent flip.
            auto independentFlipFrameStatistics =
                presentStatisticsItem.query<IIndependentFlipFramePresentStatistics>();

            // Stats should come back for the present statistics item that we tagged earlier.
            NT_ASSERT(independentFlipFrameStatistics->GetContentTag() == myPresentedContentTag);

            // The driver-approved present duration describes the custom present duration that was
            // approved by the driver and applied during the present. This is how, for example, media
            // will know whether or not they got 24hz mode for their content if they requested it.
            independentFlipFrameStatistics->GetPresentDuration();

            // The displayed time is the time the present was confirmed to have been shown
            // on screen.
            independentFlipFrameStatistics->GetDisplayedTime();

            // The adapter LUID/VidpnSource ID describe the output on which the present took
            // place. Unlike the composition statistic above, we don't report a unique ID here
            // because a monitor recycle would kick the presentation out of iflip.
            independentFlipFrameStatistics->GetOutputAdapterLUID();
            independentFlipFrameStatistics->GetOutputVidPnSourceId();
        }
        break;
    }
}
```

## <a name="example-17mdashusing-an-abstraction-layer-to-present-using-either-the-new-composition-swapchain-api-or-dxgi-from-your-application"></a>Ejemplo 17: uso de una capa de abstracción para presentar mediante la nueva API de intercambio de composición &mdash; o DXGI de la aplicación

Dados los requisitos superiores del sistema o del controlador de la nueva API de intercambio de composición, es posible que la aplicación quiera usar DXGI en casos en los que no se admite la nueva API. Afortunadamente, es bastante fácil introducir una capa de abstracción que use cualquier API disponible para realizar la presentación. En el ejemplo siguiente se muestra cómo lograr esto.

### <a name="c-example"></a>Ejemplo de C++

```cpp
// A base class presentation provider. We'll provide implementations using both DXGI and the new
// composition swapchain API, which the example will use based on what's supported.
class PresentationProvider
{
public:
    virtual void GetBackBuffer(
        _Out_ ID3D11Texture2D** ppBackBuffer) = 0;

    virtual void Present(
        _In_ SystemInterruptTime presentationTime) = 0;

    virtual bool ReadStatistics(
        _Out_ UINT* pPresentCount,
        _Out_ UINT64* pSyncQPCTime) = 0;

    virtual ID3D11Device* GetD3D11DeviceNoRef()
    {
        return m_d3dDevice.get();
    }

protected:
    com_ptr_failfast<ID3D11Device> m_d3dDevice;
};

// An implementation of PresentationProvider using a DXGI swapchain to provide presentation
// functionality.
class DXGIProvider :
    public PresentationProvider
{
public:
    DXGIProvider(
        _In_ UINT width,
        _In_ UINT height,
        _In_ UINT bufferCount)
    {
        com_ptr_failfast<IDXGIAdapter> dxgiAdapter;
        com_ptr_failfast<IDXGIFactory7> dxgiFactory;
        com_ptr_failfast<IDXGISwapChain1> dxgiSwapchain;
        com_ptr_failfast<ID3D11DeviceContext> d3dDeviceContext;

        // Direct3D device creation flags.
        UINT deviceCreationFlags =
            D3D11_CREATE_DEVICE_BGRA_SUPPORT |
            D3D11_CREATE_DEVICE_SINGLETHREADED;

        // Create the Direct3D device.
        FAIL_FAST_IF_FAILED(D3D11CreateDevice(
            nullptr,                   // No adapter
            D3D_DRIVER_TYPE_HARDWARE,  // Hardware device
            nullptr,                   // No module
            deviceCreationFlags,       // Device creation flags
            nullptr, 0,                // Highest available feature level
            D3D11_SDK_VERSION,         // API version
            &m_d3dDevice,              // Resulting interface pointer
            nullptr,                   // Actual feature level
            &d3dDeviceContext));       // Device context

        // Make our way from the Direct3D device to the DXGI factory.
        auto dxgiDevice = m_d3dDevice.query<IDXGIDevice>();
        FAIL_FAST_IF_FAILED(dxgiDevice->GetParent(IID_PPV_ARGS(&dxgiAdapter)));
        FAIL_FAST_IF_FAILED(dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory)));

        // Create a swapchain matching the desired parameters.
        DXGI_SWAP_CHAIN_DESC1 desc = {};
        desc.Width = width;
        desc.Height = height;
        desc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        desc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        desc.SampleDesc.Count = 1;
        desc.SampleDesc.Quality = 0;
        desc.BufferCount = bufferCount;
        desc.Scaling = DXGI_SCALING_STRETCH;
        desc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
        desc.AlphaMode = DXGI_ALPHA_MODE_PREMULTIPLIED;
        FAIL_FAST_IF_FAILED(dxgiFactory->CreateSwapChainForComposition(
            m_d3dDevice.get(),
            &desc,
            nullptr,
            &dxgiSwapchain));

        // Store the swapchain.
        dxgiSwapchain.query_to(&m_swapchain);
    }

    void GetBackBuffer(
        _Out_ ID3D11Texture2D** ppBackBuffer) override
    {
        // Get the backbuffer directly from the swapchain.
        FAIL_FAST_IF_FAILED(m_swapchain->GetBuffer(
            m_swapchain->GetCurrentBackBufferIndex(),
            IID_PPV_ARGS(ppBackBuffer)));
    }

    void Present(
        _In_ SystemInterruptTime presentationTime) override
    {
        // Convert the passed presentation time to a present interval. The implementation is
        // not provided here, as there's a great deal of complexity around computing this
        // most accurately, but it essentially boils down to taking the time from now and
        // figuring out the number of vblanks that corresponds to that time duration.
        UINT vblankIntervals = ComputePresentIntervalFromTime(presentationTime);

        // Issue a present to the swapchain. If we wanted to allow for a time to be specified,
        // code here could convert the time to a present duration, which could be passed here.
        FAIL_FAST_IF_FAILED(m_swapchain->Present(vblankIntervals, 0));
    }

    bool ReadStatistics(
        _Out_ UINT* pPresentCount,
        _Out_ UINT64* pSyncQPCTime) override
    {
        // Zero our output parameters initially.
        *pPresentCount = 0;
        *pSyncQPCTime = 0;

        // Grab frame statistics from the swapchain.
        DXGI_FRAME_STATISTICS frameStatistics;
        FAIL_FAST_IF_FAILED(m_swapchain->GetFrameStatistics(&frameStatistics));

        // If the statistics have changed since our last read, then return the new information
        // to the caller.
        bool hasNewStats = false;
        if (frameStatistics.PresentCount > m_lastPresentCount)
        {
            m_lastPresentCount = frameStatistics.PresentCount;
            hasNewStats = true;
            *pPresentCount = frameStatistics.PresentCount;
            *pSyncQPCTime = frameStatistics.SyncQPCTime.QuadPart;
        }

        return hasNewStats;
    }

private:
    com_ptr_failfast<IDXGISwapChain4> m_swapchain;
    UINT m_lastPresentCount = 0;
};

// An implementation of PresentationProvider using the composition swapchain API to provide
// presentation functionality.
class PresentationAPIProvider :
    public PresentationProvider
{
public:
    PresentationAPIProvider(
        _In_ UINT width,
        _In_ UINT height,
        _In_ UINT bufferCount)
    {
        // Create the presentation manager and presentation surface using the function defined in a
        // previous example.
        MakePresentationManagerAndPresentationSurface(
            &m_d3dDevice,
            &m_presentationManager,
            &m_presentationSurface,
            m_presentationSurfaceHandle);

        // Register for present statistics.
        FAIL_FAST_IF_FAILED(m_presentationManager->EnablePresentStatisticsKind(
            PresentStatisticsKind_CompositionFrame,
            true));

        // Get the statistics event from the presentation manager.
        FAIL_FAST_IF_FAILED(m_presentationManager->GetPresentStatisticsAvailableEvent(
            &m_statisticsAvailableEvent));

        // Create and register the specified number of presentation buffers.
        for (UINT i = 0; i < bufferCount; i++)
        {
            com_ptr_failfast<ID3D11Texture2D> texture;
            com_ptr_failfast<IPresentationBuffer> presentationBuffer;
            AddNewPresentationBuffer(
                m_d3dDevice.get(),
                m_presentationManager.get(),
                width,
                height,
                &texture,
                &presentationBuffer);

            // Add the new presentation buffer and texture to our array.
            m_textures.push_back(texture);
            m_presentationBuffers.push_back(presentationBuffer);

            // Store the available event for the presentation buffer.
            unique_event availableEvent;
            FAIL_FAST_IF_FAILED(presentationBuffer->GetAvailableEvent(&availableEvent));
            m_bufferAvailableEvents.emplace_back(std::move(availableEvent));
        }
    }

    void GetBackBuffer(
        _Out_ ID3D11Texture2D** ppBackBuffer) override
    {
        // Query an available backbuffer using our available events.
        DWORD waitIndex = WaitForMultipleObjects(
            static_cast<UINT>(m_bufferAvailableEvents.size()),
            reinterpret_cast<HANDLE*>(m_bufferAvailableEvents.data()),
            FALSE,
            INFINITE);
        UINT bufferIndex = waitIndex - WAIT_OBJECT_0;

        // Set the backbuffer to be the next presentation buffer.
        FAIL_FAST_IF_FAILED(m_presentationSurface->SetBuffer(m_presentationBuffers[bufferIndex].get()));

        // Return the backbuffer to the caller.
        m_textures[bufferIndex].query_to(ppBackBuffer);
    }

    void Present(
        _In_ SystemInterruptTime presentationTime) override
    {
        // Present at the targeted time.
        m_presentationManager->SetTargetTime(presentationTime);
        HRESULT hrPresent = m_presentationManager->Present();
        if (hrPresent == PRESENTATION_ERROR_LOST)
        {
            // Our presentation manager has been lost. See previous examples regarding how to handle this.
            return;
        }
        else
        {
            FAIL_FAST_IF_FAILED(hrPresent);
        }
    }

    bool ReadStatistics(
        _Out_ UINT* pPresentCount,
        _Out_ UINT64* pSyncQPCTime) override
    {
        // Zero our out parameters initially.
        *pPresentCount = 0;
        *pSyncQPCTime = 0;

        bool hasNewStats = false;

        // Peek at the statistics available event state to see if we've got new statistics.
        while (WaitForSingleObject(m_statisticsAvailableEvent.get(), 0) == WAIT_OBJECT_0)
        {
            // Pop a statistics item to process.
            com_ptr_failfast<IPresentStatistics> statisticsItem;
            FAIL_FAST_IF_FAILED(m_presentationManager->GetNextPresentStatistics(
                &statisticsItem));

            // If this is a composition frame stat, process it.
            if (statisticsItem->GetKind() == PresentStatisticsKind_CompositionFrame)
            {
                // We've got new stats to report.
                hasNewStats = true;

                // Convert to composition frame statistic item.
                auto frameStatisticsItem = statisticsItem.query<ICompositionFramePresentStatistics>();

                // Query DirectComposition's target statistics API to determine the completed time.
                COMPOSITION_FRAME_TARGET_STATS frameTargetStats;
                COMPOSITION_TARGET_STATS targetStats[4];
                frameTargetStats.targetCount = ARRAYSIZE(targetStats);
                frameTargetStats.targetStats = targetStats;
                // Specify the frameId we got from stats in order to pass to the call
                // below and retrieve timing information about that frame.
                frameTargetStats.frameId = frameStatisticsItem->GetCompositionFrameId();
                FAIL_FAST_IF_FAILED(DCompositionGetTargetStatistics(1, &frameTargetStats));

                // Return the statistics information for the first target.
                *pPresentCount = static_cast<UINT>(frameStatisticsItem->GetPresentId());
                *pSyncQPCTime = frameTargetStats.targetStats[0].completedStats.time;

                // Note that there's a much richer variety of statistics information in the new
                // API that can be used to infer much more than is possible with DXGI frame
                // statistics.
            }
        }

        return hasNewStats;
    }

    static bool IsSupportedOnSystem()
    {
        // Direct3D device creation flags. The composition swapchain API requires that applications disable internal
        // driver threading optimizations, as these optimizations break synchronization of the API.
        // If this flag isn't present, then the API will fail the call to create the presentation factory.
        UINT deviceCreationFlags =
            D3D11_CREATE_DEVICE_BGRA_SUPPORT |
            D3D11_CREATE_DEVICE_SINGLETHREADED |
            D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS;

        // Create the Direct3D device.
        com_ptr_failfast<ID3D11Device> d3dDevice;
        com_ptr_failfast<ID3D11DeviceContext> d3dDeviceContext;
        FAIL_FAST_IF_FAILED(D3D11CreateDevice(
            nullptr,                   // No adapter
            D3D_DRIVER_TYPE_HARDWARE,  // Hardware device
            nullptr,                   // No module
            deviceCreationFlags,       // Device creation flags
            nullptr, 0,                // Highest available feature level
            D3D11_SDK_VERSION,         // API version
            &d3dDevice,                // Resulting interface pointer
            nullptr,                   // Actual feature level
            &d3dDeviceContext));       // Device context

        // Call the composition swapchain API export to create the presentation factory.
        com_ptr_failfast<IPresentationFactory> presentationFactory;
        FAIL_FAST_IF_FAILED(CreatePresentationFactory(
            d3dDevice.get(),
            IID_PPV_ARGS(&presentationFactory)));

        // Now determine whether the system is capable of supporting the composition swapchain API based
        // on the capability that's reported by the presentation factory.
        return presentationFactory->IsPresentationSupported();
    }

private:
    com_ptr_failfast<IPresentationManager> m_presentationManager;
    com_ptr_failfast<IPresentationSurface> m_presentationSurface;
    vector<com_ptr_failfast<ID3D11Texture2D>> m_textures;
    vector<com_ptr_failfast<IPresentationBuffer>> m_presentationBuffers;
    vector<unique_event> m_bufferAvailableEvents;
    unique_handle m_presentationSurfaceHandle;
    unique_event m_statisticsAvailableEvent;
};

void DXGIOrPresentationAPIExample()
{
    // Get the current system time. We'll base our 'PresentAt' time on this result.
    SystemInterruptTime currentTime;
    QueryInterruptTimePrecise(&currentTime.value);

    // Track a time we'll be presenting at below. Default to the current time, then increment by
    // 1/10th of a second every present.
    auto presentTime = currentTime;

    // Allocate a presentation provider using the composition swapchain API if it is supported;
    // otherwise fall back to DXGI.
    unique_ptr<PresentationProvider> presentationProvider;
    if (PresentationAPIProvider::IsSupportedOnSystem())
    {
        presentationProvider = std::make_unique<PresentationAPIProvider>(
            500, // Buffer width
            500, // Buffer height
            6);  // Number of buffers
    }
    else
    {
        // System doesn't support the composition swapchain API. Fall back to DXGI.
        presentationProvider = std::make_unique<DXGIProvider>(
            500, // Buffer width
            500, // Buffer height
            6);  // Number of buffers
    }

    // Present 50 times.
    constexpr UINT numPresents = 50;
    for (UINT i = 0; i < 50; i++)
    {
        // Advance our present time 1/10th of a second in the future.
        presentTime.value += 1'000'000;

        // Call the presentation provider to get a backbuffer to render to.
        com_ptr_failfast<ID3D11Texture2D> backBuffer;
        presentationProvider->GetBackBuffer(&backBuffer);

        // Render to the backbuffer.
        DrawColorToSurface(
            presentationProvider->GetD3D11DeviceNoRef(),
            backBuffer,
            1.0f, // red
            0.0f, // green
            0.0f); // blue

        // Present the backbuffer.
        presentationProvider->Present(presentTime);

        // Process statistics.
        bool hasNewStats;
        UINT64 presentTime;
        UINT presentCount;
        hasNewStats = presentationProvider->ReadStatistics(
            &presentCount,
            &presentTime);
        if (hasNewStats)
        {
            // Process these statistics however your application wishes.
        }
    }
}
```

## <a name="related-topics"></a>Temas relacionados

* [Cadena de intercambio de composición](comp-swapchain-portal.md)

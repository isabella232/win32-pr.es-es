---
description: Describe cómo usar superposiciones de hardware en Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Compatibilidad con la superposición de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcae33cdf55de59bdcd074829d52b4c1c43ea5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581069"
---
# <a name="hardware-overlay-support"></a>Compatibilidad con la superposición de hardware

Una superposición de hardware es un área dedicada de memoria de vídeo que se puede superponer en la superficie principal. No se realiza ninguna copia cuando se muestra la superposición. La operación de superposición se realiza en hardware, sin modificar los datos de la superficie principal.

El uso de superposiciones de hardware para la reproducción de vídeo era común en versiones anteriores de Windows, ya que las superposiciones son eficaces para el contenido de vídeo con una alta velocidad de fotogramas. A partir Windows 7, Direct3D 9 admite superposiciones de hardware. Esta compatibilidad está pensada principalmente para la reproducción de vídeo y difiere en algunos aspectos de las API anteriores de DirectDraw:

-   La superposición no se puede acotar, reflejar o desenlazar.
-   No se admiten las claves de color de origen ni la combinación alfa.
-   Las superposiciones se pueden extender si el hardware de superposición lo admite. De lo contrario, no se admite el stretching. En la práctica, no todos los controladores de gráficos admiten el stretching.
-   Cada dispositivo admite como máximo una superposición.
-   La superposición se realiza mediante una clave de color de destino, pero el tiempo de ejecución de Direct3D selecciona automáticamente el color y dibuja el rectángulo de destino. Direct3D realiza un seguimiento automático de la posición de la ventana y actualiza la posición de superposición cada vez que se llama a **PresentEx.**

### <a name="creating-a-hardware-overlay-surface"></a>Creación de una superficie de superposición de hardware

Para consultar la compatibilidad con la superposición, llame **a IDirect3D9::GetDeviceCaps**. Si el controlador admite la superposición de hardware, la marca OVERLAY de **\_ D3DCAPS** se establece en **D3DCAPS9. Miembro Caps.**

Para averiguar si se admite un formato de superposición específico para un modo de presentación determinado, llame a [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).

Para crear la superposición, llame a **IDirect3D9Ex::CreateDeviceEx** y especifique el efecto de intercambio **D3DSWAPEFFECT \_ OVERLAY.** El búfer de reserva puede usar un formato no RGB si el hardware lo admite.

Las superficies superpuestas tienen las siguientes limitaciones:

-   La aplicación no puede crear más de una cadena de intercambio de superposición.
-   La superposición debe usarse en modo de ventana. No se puede usar en modo de pantalla completa.
-   El efecto de intercambio de superposición debe usarse con la **interfaz IDirect3DDevice9Ex.** No se admite para **IDirect3DDevice9.**
-   No se puede usar multimuestreo.
-   No se admiten las marcas **D3DPRESENT \_ DONOTFLIP** y **D3DPRESENT \_ FLIPRESTART.**
-   Las estadísticas de presentación no están disponibles para la superficie superpuesta.

Si el hardware no admite el ajuste, se recomienda crear una cadena de intercambio tan grande como el modo de presentación, para que la ventana pueda cambiar de tamaño a cualquier dimensión. Volver a crear la cadena de intercambio no es una manera óptima de controlar el cambio de tamaño de la ventana, ya que puede provocar artefactos de representación graves. Además, debido a la forma en que la GPU administra la memoria superpuesta, volver a crear la cadena de intercambio puede provocar que una aplicación se queme de la memoria de vídeo.

### <a name="new-d3dpresent_parameters-flags"></a>Nuevas marcas de parámetros D3DPRESENT \_

Las siguientes **marcas \_ de parámetros D3DPRESENT** se definen para crear superposiciones.



| Marca                                      | Descripción                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENTFLAG \_ OVERLAY \_ LIMITEDRGB**   | El intervalo RGB es de 16 a 235. El valor predeterminado es de 0 a 255. <br/> Requiere la **funcionalidad D3DOVERLAYCAPS \_ LIMITEDRANGERGB.**<br/>                                                 |
| **D3DPRESENTFLAG \_ OVERLAY \_ YCbCr \_ BT709** | Los colores YUV usan la definición BT.709. El valor predeterminado es BT.601. <br/> Requiere la **funcionalidad D3DOVERLAYCAPS \_ YCbCr \_ BT709.**<br/>                                      |
| **D3DPRESENTFLAG \_ OVERLAY \_ YCbCr \_ scryCC** | Generación de los datos mediante YCbCr extendido (sipYCC).<br/> Requiere la **funcionalidad D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ trasACC** o **D3DOVERLAYCAPS \_ YCbCr \_ BT709. \_**<br/> |



 

### <a name="using-hardware-overlays"></a>Uso de superposiciones de hardware

Para mostrar la superficie superpuesta, la aplicación llama a **IDirect3DDevice9Ex::P resentEx**. El tiempo de ejecución de Direct3D dibuja automáticamente la clave de color de destino.

Las siguientes **marcas PresentEx** se definen para las superposiciones.



| Marca                              | Descripción                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENT \_ UPDATECOLORKEY**    | Establezca esta marca si Administrador de ventanas de escritorio composición (DWM) está deshabilitada. Esta marca hace que Direct3D vuelva a dibujar la clave de color.<br/> Si DWM está habilitado, esta marca no es necesaria, ya que Direct3D dibuja la clave de color una vez en la superficie que DWM usa para el redireccionamiento.<br/> |
| **D3DPRESENT \_ HIDEOVERLAY**       | Oculta la superposición.                                                                                                                                                                                                                                                                    |
| **D3DPRESENT \_ UPDATEOVERLAYONLY** | Actualiza la superposición sin cambiar el contenido.<br/> Esta marca es útil si la ventana se mueve mientras el vídeo está en pausa.<br/>                                                                                                                                           |



 

Una aplicación debe estar preparada para controlar los casos siguientes:

-   Si otra aplicación usa la superposición, **PresentEx** devuelve **D3DERR \_ NOTAVAILABLE.**
-   Si la ventana se mueve a otro monitor, la aplicación debe volver a crear la cadena de intercambio. De lo contrario, si la aplicación llama a **PresentEx** para mostrar la superposición en un monitor diferente, **PresentEx** devuelve **D3DERR \_ INVALIDDEVICE**.
-   Si cambia el modo de presentación, Direct3D intenta restaurar la superposición. Si el nuevo modo no admite la superposición, **PresentEx** devuelve **D3DERR \_ UNSUPPORTEDOVERLAY**.

### <a name="example-code"></a>Código de ejemplo

En el ejemplo siguiente se muestra cómo crear una superficie superpuesta.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 





---
title: Mostrar correctamente en una pantalla de PPP alta
description: Describe cómo crear una ventana que se muestra correctamente en pantallas de alta ppp.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b3e82951dfa77e6f61c661b87064dad5cb9f08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995537"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a>Mostrar correctamente en una pantalla de PPP alta

Aunque Direct2D soluciona muchos problemas con un alto nivel de PPP, hay dos pasos que debe seguir para asegurarse de que la aplicación funciona correctamente en pantallas de alta PPP:

-   [Paso 1: usar el PPP del sistema al crear ventanas](#step-1-use-the-system-dpi-when-creating-windows)
-   [Paso 2: declarar que la aplicación es compatible con PPP](#step-2-declare-that-the-application-is-dpi-aware)
-   [Temas relacionados](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Paso 1: usar el PPP del sistema al crear ventanas

La interfaz [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) proporciona el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar los PPP del sistema. Proporciona las dimensiones horizontal y vertical de la pantalla en puntos por pulgada (PPP). Para usar estos valores para establecer el ancho de una ventana, use la siguiente fórmula:

<*PPP* >  \* horizontal  < *ancho*, en píxeles>/<*valores de PPP horizontales predeterminados*>

... donde *PPP horizontal* es el valor recuperado por [**GETDESKTOPDPI**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) y el *PPP horizontal predeterminado* es 96. La fórmula es similar para el tamaño vertical:

<*PPP* >  \* vertical  < *alto*, en píxeles>/<*PPP vertical predeterminado*>

... donde *DPI vertical* es el valor recuperado por el método [**GETDESKTOPDPI**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) y el *PPP vertical predeterminado* es 96.

En el código siguiente se usa el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar el PPP del sistema y, a continuación, se crea una ventana de 640 × 480, escalada a PPP del sistema.


```C++
        // Because the CreateWindow function takes its size in pixels,
        // obtain the system DPI and use it to scale the window size.
        FLOAT dpiX, dpiY;

        // The factory returns the current system DPI. This is also the value it will use
        // to create its own windows.
        m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


        // Create the window.
        m_hwnd = CreateWindow(
            L"D2DDemoApp",
            L"Direct2D Demo App",
            WS_OVERLAPPEDWINDOW,
            CW_USEDEFAULT,
            CW_USEDEFAULT,
            static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
            static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
            NULL,
            NULL,
            HINST_THISCOMPONENT,
            this
            );
```



> [!Note]
>
> A partir de Windows 8, puede usar la clase [**Windows:: Graphics::D de la:D isplayproperties:**](/uwp/api/Windows.Graphics.Display.DisplayProperties) para obtener el PPP del sistema.

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Paso 2: declarar que la aplicación está DPI-Aware

Cuando una aplicación se declara para que sea compatible con PPP, es una instrucción que especifica que la aplicación se comporta bien con valores de PPP de hasta 200 ppp. En Windows Vista y Windows 7, cuando está habilitada la virtualización de PPP, se escalan las aplicaciones que no reconocen los PPP y las aplicaciones reciben datos virtualizados de las API del sistema, como la función [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Para declarar que la aplicación es compatible con PPP, complete los pasos siguientes.

1.  Cree un archivo denominado DeclareDPIAware. manifest.
2.  Copie el siguiente código XML en el archivo y guárdelo:
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  En el archivo. vcproj del proyecto, agregue la entrada siguiente dentro de cada elemento de configuración en VisualStudioProject/Configurations:
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct2D y High-PPP](direct2d-and-high-dpi.md)
</dt> </dl>

 

 
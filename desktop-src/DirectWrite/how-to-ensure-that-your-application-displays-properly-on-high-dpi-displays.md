---
title: Cómo asegurarse de que la aplicación se muestre correctamente en pantallas de alta PPP (DirectWrite)
description: Describe cómo crear una ventana que se muestra correctamente en pantallas de alta ppp.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317eb3379963cec600ab9bac7deb3778f0874e59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359168"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>Cómo asegurarse de que la aplicación se muestre correctamente en pantallas de alta resolución de PPP

Aunque [DirectWrite](direct-write-portal.md) soluciona muchos problemas con un alto nivel de PPP, hay dos pasos que debe seguir para asegurarse de que la aplicación funciona correctamente en pantallas de alta PPP:

-   [Paso 1: usar el PPP del sistema al crear ventanas](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [GDI](#gdi)
-   [Paso 2: declarar que la aplicación es compatible con PPP](#step-2-declare-that-the-application-is-dpi-aware)
-   [Temas relacionados](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Paso 1: usar el PPP del sistema al crear ventanas

Esto se puede hacer mediante [Direct2D](../direct2d/direct2d-portal.md) o mediante [GDI](../gdi/windows-gdi.md).

### <a name="direct2d"></a>Direct2D

La interfaz [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) proporciona el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar los PPP del sistema. Proporciona las dimensiones horizontal y vertical de la pantalla en puntos por pulgada (PPP). Para usar estos valores para establecer el ancho de una ventana, use la siguiente fórmula:

<*PPP* >  \* horizontal  < *ancho*, en píxeles>/<*valores de PPP horizontales predeterminados*>

... donde *PPP horizontal* es el valor recuperado por GetDpi y el *PPP horizontal predeterminado* es 96. La fórmula es similar para el tamaño vertical:

<*PPP* >  \* vertical  < *alto*, en píxeles>/<*PPP vertical predeterminado*>

... donde *DPI vertical* es el valor recuperado por el método [**GETDESKTOPDPI**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) y el *PPP vertical predeterminado* es 96.

En el código siguiente se usa el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para crear una ventana de 640 x 480, escalada a PPP del sistema. (En el código siguiente, *m \_ spD2DFactory* es un puntero inteligente a una instancia de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) ).


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



### <a name="gdi"></a>GDI

[GDI](interoperating-with-gdi.md) proporciona la función [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para recuperar información del dispositivo. Puede recuperar información de PPP pasando los valores de índice de *LOGPIXELSX* y *LOGPIXELSY* . La fórmula para determinar el tamaño horizontal y vertical de una ventana es la misma que con el ejemplo de [Direct2D](../direct2d/direct2d-portal.md) anterior.

En el código siguiente se usa la función [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para crear una ventana de 640 x 480, escalada a PPP del sistema.


```C++
FLOAT dpiX, dpiY;

HDC screen = GetDC(0);
dpiX = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSX));
dpiY = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSY));
ReleaseDC(0, screen);

hWnd = CreateWindow(
         TEXT("DirectWriteApp"),
         TEXT("DirectWrite Demo App"),
         WS_OVERLAPPEDWINDOW,
         CW_USEDEFAULT,
         CW_USEDEFAULT,
         static_cast<INT>(dpiX * 640.f / 96.f),
         static_cast<INT>(dpiY * 480.f / 96.f),
         NULL,
         NULL,
         hInstance,
         NULL
         );
```



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Paso 2: declarar que la aplicación está DPI-Aware

Cuando una aplicación se declara para que sea compatible con PPP, es una instrucción que especifica que la aplicación se comporta bien con valores de PPP de hasta 200 ppp. En Windows Vista y Windows 7, cuando está habilitada la virtualización de PPP, se escalan las aplicaciones que no reconocen los PPP y las aplicaciones reciben datos virtualizados de las API del sistema, como la función [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) . Para declarar que la aplicación es compatible con PPP, complete los pasos siguientes.

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

[Direct2D y High-PPP](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 
---
title: Cómo asegurarse de que la aplicación se muestra correctamente en pantallas de valores altos de PPP (DirectWrite)
description: Describe cómo asegurarse de que la aplicación crea una ventana que se muestra correctamente en pantallas con valores altos de PPP.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71166d312fe666644c683fe2ece7dd3ced59f765
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406428"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>Cómo asegurarse de que la aplicación se muestra correctamente en pantallas con valores altos de PPP

Aunque [DirectWrite](direct-write-portal.md) soluciona muchos problemas de valores altos de PPP, hay dos pasos que debe seguir para asegurarse de que la aplicación funciona correctamente en pantallas con valores altos de PPP:

-   [Paso 1: Usar el valor de PPP del sistema al crear Windows](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [Gdi](#gdi)
-   [Paso 2: Declarar que la aplicación es compatible con PPP](#step-2-declare-that-the-application-is-dpi-aware)
-   [Temas relacionados](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Paso 1: Usar el valor de PPP del sistema al crear Windows

Esto se puede hacer mediante [Direct2D](../direct2d/direct2d-portal.md) o mediante [GDI.](../gdi/windows-gdi.md)

### <a name="direct2d"></a>Direct2D

La [**interfaz ID2D1Factory proporciona**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar el ppp del sistema. Proporciona las dimensiones horizontal y vertical de la pantalla en puntos por pulgada (PPP). Para usar estos valores para establecer el ancho de una ventana, use la siguiente fórmula:

<*PPP horizontal* >  \*  < *width*, en píxeles> /<*ppp horizontal predeterminado*>

... donde *PPP horizontal* es el valor retrived by GetDpi y el valor predeterminado de PPP *horizontal* es 96. La fórmula es similar para el tamaño vertical:

<*PPP vertical* >  \*  < *height*, en píxeles>/<*ppp vertical predeterminado*>

... donde *PPP vertical* es el valor recuperado por el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) y *el valor predeterminado de PPP vertical* es 96.

El código siguiente usa el [**método GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para crear una ventana de 640 x 480, escalada a ppp del sistema. (En el código siguiente, *m \_ spD2DFactory* es un puntero inteligente a una [**instancia de ID2D1Factory).**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)


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

[GDI](interoperating-with-gdi.md) proporciona la [**función GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para recuperar información del dispositivo. Puede recuperar información de PPP pasando los valores de índice *LOGPIXELSX* *y LOGPIXELSY.* La fórmula para determinar el tamaño horizontal y vertical de una ventana es la misma que con el [ejemplo de Direct2D](../direct2d/direct2d-portal.md) anterior.

El código siguiente usa la [**función GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para crear una ventana de 640 x 480, escalada a ppp del sistema.


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Paso 2: Declarar que la aplicación está DPI-Aware

Cuando una aplicación se declara compatible con PPP, es una instrucción que especifica que la aplicación se comporta bien en la configuración de PPP de hasta 200 PPP. En Windows Vista y Windows 7, cuando se habilita la virtualización de PPP, las aplicaciones que no tienen reconocimiento de PPP se escalan y las aplicaciones reciben datos virtualizados de las API del sistema, como la [**función GetSystemMetric.**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) Para declarar que la aplicación es compatible con PPP, complete los pasos siguientes.

1.  Cree un archivo denominado DeclareDPIAware.manifest.
2.  Copie el siguiente xml en el archivo y guárdelo:
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  En el archivo .vcproj del proyecto, agregue la siguiente entrada dentro de cada elemento Configuration en VisualStudioProject/Configurations:
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct2D y valores altos de PPP](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 
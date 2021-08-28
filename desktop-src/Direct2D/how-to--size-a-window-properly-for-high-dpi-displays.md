---
title: Mostrar correctamente en una pantalla con valores altos de PPP
description: Describe los pasos para crear una ventana para la aplicación que se muestre correctamente en pantallas con valores altos de PPP.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8ebc6a7621623307d9b2cfd953a5fa3f3387fbacb3faeb345375d925044cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259965"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a>Mostrar correctamente en una pantalla con valores altos de PPP

Aunque Direct2D soluciona muchos problemas de valores altos de PPP, hay dos pasos que debe seguir para asegurarse de que la aplicación funciona correctamente en pantallas con valores altos de PPP:

-   [Paso 1: Usar el valor de PPP del sistema al crear Windows](#step-1-use-the-system-dpi-when-creating-windows)
-   [Paso 2: Declarar que la aplicación es compatible con PPP](#step-2-declare-that-the-application-is-dpi-aware)
-   [Temas relacionados](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Paso 1: Usar el valor de PPP del sistema al crear Windows

La [**interfaz ID2D1Factory proporciona**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar el ppp del sistema. Proporciona las dimensiones horizontal y vertical de la pantalla en puntos por pulgada (PPP). Para usar estos valores para establecer el ancho de una ventana, use la siguiente fórmula:

<*PPP horizontal* >  \*  < *width*, en píxeles> /<*ppp horizontal predeterminado*>

... donde *PPP horizontal* es el valor retrived by [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) y *el valor predeterminado de PPP horizontal* es 96. La fórmula es similar para el tamaño vertical:

<*PPP vertical* >  \*  < *height*, en píxeles> o <*ppp vertical predeterminado*>

... donde *PPP vertical* es el valor recuperado por el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) y *el valor predeterminado de PPP vertical* es 96.

El código siguiente usa el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar el VALOR DE PPP del sistema y, a continuación, crea una ventana 640 × 480, escalada a ppp del sistema.


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
> A partir Windows 8, puede usar la [**clase Windows::Graphics::D isplay::D isplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) para obtener el valor de PPP del sistema.

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Paso 2: Declarar que la aplicación está DPI-Aware

Cuando una aplicación se declara compatible con PPP, es una instrucción que especifica que la aplicación se comporta bien en la configuración de PPP de hasta 200 PPP. En Windows Vista y Windows 7, cuando se habilita la virtualización de PPP, se escalan las aplicaciones que no tienen reconocimiento de PPP y las aplicaciones reciben datos virtualizados de las API del sistema, como la [**función GetSystemMetric.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Para declarar que la aplicación es compatible con PPP, complete los pasos siguientes.

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

[Direct2D y valores altos de PPP](direct2d-and-high-dpi.md)
</dt> </dl>

 

 
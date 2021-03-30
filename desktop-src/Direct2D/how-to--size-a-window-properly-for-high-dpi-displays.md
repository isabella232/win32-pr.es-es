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
# <a name="displaying-properly-on-a-high-dpi-display"></a><span data-ttu-id="9694d-103">Mostrar correctamente en una pantalla de PPP alta</span><span class="sxs-lookup"><span data-stu-id="9694d-103">Displaying properly on a high-DPI display</span></span>

<span data-ttu-id="9694d-104">Aunque Direct2D soluciona muchos problemas con un alto nivel de PPP, hay dos pasos que debe seguir para asegurarse de que la aplicación funciona correctamente en pantallas de alta PPP:</span><span class="sxs-lookup"><span data-stu-id="9694d-104">Although Direct2D addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="9694d-105">Paso 1: usar el PPP del sistema al crear ventanas</span><span class="sxs-lookup"><span data-stu-id="9694d-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
-   [<span data-ttu-id="9694d-106">Paso 2: declarar que la aplicación es compatible con PPP</span><span class="sxs-lookup"><span data-stu-id="9694d-106">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="9694d-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9694d-107">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="9694d-108">Paso 1: usar el PPP del sistema al crear ventanas</span><span class="sxs-lookup"><span data-stu-id="9694d-108">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="9694d-109">La interfaz [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) proporciona el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar los PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="9694d-109">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="9694d-110">Proporciona las dimensiones horizontal y vertical de la pantalla en puntos por pulgada (PPP).</span><span class="sxs-lookup"><span data-stu-id="9694d-110">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="9694d-111">Para usar estos valores para establecer el ancho de una ventana, use la siguiente fórmula:</span><span class="sxs-lookup"><span data-stu-id="9694d-111">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="9694d-112"><*PPP* >  \* horizontal  < *ancho*, en píxeles>/<*valores de PPP horizontales predeterminados*></span><span class="sxs-lookup"><span data-stu-id="9694d-112"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="9694d-113">... donde *PPP horizontal* es el valor recuperado por [**GETDESKTOPDPI**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) y el *PPP horizontal predeterminado* es 96.</span><span class="sxs-lookup"><span data-stu-id="9694d-113">...where *horizontal DPI* is the value retrived by [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="9694d-114">La fórmula es similar para el tamaño vertical:</span><span class="sxs-lookup"><span data-stu-id="9694d-114">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="9694d-115"><*PPP* >  \* vertical  < *alto*, en píxeles>/<*PPP vertical predeterminado*></span><span class="sxs-lookup"><span data-stu-id="9694d-115"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="9694d-116">... donde *DPI vertical* es el valor recuperado por el método [**GETDESKTOPDPI**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) y el *PPP vertical predeterminado* es 96.</span><span class="sxs-lookup"><span data-stu-id="9694d-116">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="9694d-117">En el código siguiente se usa el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar el PPP del sistema y, a continuación, se crea una ventana de 640 × 480, escalada a PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="9694d-117">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to retrieve the system DPI and then creates a 640 × 480 window, scaled to the system DPI.</span></span>


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
> <span data-ttu-id="9694d-118">A partir de Windows 8, puede usar la clase [**Windows:: Graphics::D de la:D isplayproperties:**](/uwp/api/Windows.Graphics.Display.DisplayProperties) para obtener el PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="9694d-118">Starting with Windows 8, you can use the [**Windows::Graphics::Display::DisplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) class to get the system DPI.</span></span>

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="9694d-119">Paso 2: declarar que la aplicación está DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="9694d-119">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="9694d-120">Cuando una aplicación se declara para que sea compatible con PPP, es una instrucción que especifica que la aplicación se comporta bien con valores de PPP de hasta 200 ppp.</span><span class="sxs-lookup"><span data-stu-id="9694d-120">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="9694d-121">En Windows Vista y Windows 7, cuando está habilitada la virtualización de PPP, se escalan las aplicaciones que no reconocen los PPP y las aplicaciones reciben datos virtualizados de las API del sistema, como la función [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="9694d-121">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="9694d-122">Para declarar que la aplicación es compatible con PPP, complete los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9694d-122">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="9694d-123">Cree un archivo denominado DeclareDPIAware. manifest.</span><span class="sxs-lookup"><span data-stu-id="9694d-123">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="9694d-124">Copie el siguiente código XML en el archivo y guárdelo:</span><span class="sxs-lookup"><span data-stu-id="9694d-124">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="9694d-125">En el archivo. vcproj del proyecto, agregue la entrada siguiente dentro de cada elemento de configuración en VisualStudioProject/Configurations:</span><span class="sxs-lookup"><span data-stu-id="9694d-125">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="9694d-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9694d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9694d-127">Direct2D y High-PPP</span><span class="sxs-lookup"><span data-stu-id="9694d-127">Direct2D and High-DPI</span></span>](direct2d-and-high-dpi.md)
</dt> </dl>

 

 
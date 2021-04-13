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
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a><span data-ttu-id="0a171-103">Cómo asegurarse de que la aplicación se muestre correctamente en pantallas de alta resolución de PPP</span><span class="sxs-lookup"><span data-stu-id="0a171-103">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>

<span data-ttu-id="0a171-104">Aunque [DirectWrite](direct-write-portal.md) soluciona muchos problemas con un alto nivel de PPP, hay dos pasos que debe seguir para asegurarse de que la aplicación funciona correctamente en pantallas de alta PPP:</span><span class="sxs-lookup"><span data-stu-id="0a171-104">Although [DirectWrite](direct-write-portal.md) addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="0a171-105">Paso 1: usar el PPP del sistema al crear ventanas</span><span class="sxs-lookup"><span data-stu-id="0a171-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
    -   [<span data-ttu-id="0a171-106">Direct2D</span><span class="sxs-lookup"><span data-stu-id="0a171-106">Direct2D</span></span>](#direct2d)
    -   [<span data-ttu-id="0a171-107">GDI</span><span class="sxs-lookup"><span data-stu-id="0a171-107">GDI</span></span>](#gdi)
-   [<span data-ttu-id="0a171-108">Paso 2: declarar que la aplicación es compatible con PPP</span><span class="sxs-lookup"><span data-stu-id="0a171-108">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="0a171-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a171-109">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="0a171-110">Paso 1: usar el PPP del sistema al crear ventanas</span><span class="sxs-lookup"><span data-stu-id="0a171-110">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="0a171-111">Esto se puede hacer mediante [Direct2D](../direct2d/direct2d-portal.md) o mediante [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="0a171-111">This can be done by using [Direct2D](../direct2d/direct2d-portal.md) or by using [GDI](../gdi/windows-gdi.md).</span></span>

### <a name="direct2d"></a><span data-ttu-id="0a171-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="0a171-112">Direct2D</span></span>

<span data-ttu-id="0a171-113">La interfaz [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) proporciona el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar los PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="0a171-113">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="0a171-114">Proporciona las dimensiones horizontal y vertical de la pantalla en puntos por pulgada (PPP).</span><span class="sxs-lookup"><span data-stu-id="0a171-114">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="0a171-115">Para usar estos valores para establecer el ancho de una ventana, use la siguiente fórmula:</span><span class="sxs-lookup"><span data-stu-id="0a171-115">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="0a171-116"><*PPP* >  \* horizontal  < *ancho*, en píxeles>/<*valores de PPP horizontales predeterminados*></span><span class="sxs-lookup"><span data-stu-id="0a171-116"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="0a171-117">... donde *PPP horizontal* es el valor recuperado por GetDpi y el *PPP horizontal predeterminado* es 96.</span><span class="sxs-lookup"><span data-stu-id="0a171-117">...where *horizontal DPI* is the value retrived by GetDpi and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="0a171-118">La fórmula es similar para el tamaño vertical:</span><span class="sxs-lookup"><span data-stu-id="0a171-118">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="0a171-119"><*PPP* >  \* vertical  < *alto*, en píxeles>/<*PPP vertical predeterminado*></span><span class="sxs-lookup"><span data-stu-id="0a171-119"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="0a171-120">... donde *DPI vertical* es el valor recuperado por el método [**GETDESKTOPDPI**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) y el *PPP vertical predeterminado* es 96.</span><span class="sxs-lookup"><span data-stu-id="0a171-120">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="0a171-121">En el código siguiente se usa el método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para crear una ventana de 640 x 480, escalada a PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="0a171-121">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to create a 640 x 480 window, scaled to the system DPI.</span></span> <span data-ttu-id="0a171-122">(En el código siguiente, *m \_ spD2DFactory* es un puntero inteligente a una instancia de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) ).</span><span class="sxs-lookup"><span data-stu-id="0a171-122">(In the following code, *m\_spD2DFactory* is a smart pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) instance.)</span></span>


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



### <a name="gdi"></a><span data-ttu-id="0a171-123">GDI</span><span class="sxs-lookup"><span data-stu-id="0a171-123">GDI</span></span>

<span data-ttu-id="0a171-124">[GDI](interoperating-with-gdi.md) proporciona la función [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para recuperar información del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a171-124">[GDI](interoperating-with-gdi.md) provides the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function for retrieving device information.</span></span> <span data-ttu-id="0a171-125">Puede recuperar información de PPP pasando los valores de índice de *LOGPIXELSX* y *LOGPIXELSY* .</span><span class="sxs-lookup"><span data-stu-id="0a171-125">You can retrieve DPI information by passing the *LOGPIXELSX* and *LOGPIXELSY* index values.</span></span> <span data-ttu-id="0a171-126">La fórmula para determinar el tamaño horizontal y vertical de una ventana es la misma que con el ejemplo de [Direct2D](../direct2d/direct2d-portal.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="0a171-126">The formula for determining the horizontal and vertical size of a window is the same as with the [Direct2D](../direct2d/direct2d-portal.md) example above.</span></span>

<span data-ttu-id="0a171-127">En el código siguiente se usa la función [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para crear una ventana de 640 x 480, escalada a PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="0a171-127">The following code uses the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function to create a 640 x 480 window, scaled to the system DPI.</span></span>


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="0a171-128">Paso 2: declarar que la aplicación está DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="0a171-128">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="0a171-129">Cuando una aplicación se declara para que sea compatible con PPP, es una instrucción que especifica que la aplicación se comporta bien con valores de PPP de hasta 200 ppp.</span><span class="sxs-lookup"><span data-stu-id="0a171-129">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="0a171-130">En Windows Vista y Windows 7, cuando está habilitada la virtualización de PPP, se escalan las aplicaciones que no reconocen los PPP y las aplicaciones reciben datos virtualizados de las API del sistema, como la función [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="0a171-130">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="0a171-131">Para declarar que la aplicación es compatible con PPP, complete los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="0a171-131">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="0a171-132">Cree un archivo denominado DeclareDPIAware. manifest.</span><span class="sxs-lookup"><span data-stu-id="0a171-132">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="0a171-133">Copie el siguiente código XML en el archivo y guárdelo:</span><span class="sxs-lookup"><span data-stu-id="0a171-133">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="0a171-134">En el archivo. vcproj del proyecto, agregue la entrada siguiente dentro de cada elemento de configuración en VisualStudioProject/Configurations:</span><span class="sxs-lookup"><span data-stu-id="0a171-134">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="0a171-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a171-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a171-136">Direct2D y High-PPP</span><span class="sxs-lookup"><span data-stu-id="0a171-136">Direct2D and High-DPI</span></span>](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 
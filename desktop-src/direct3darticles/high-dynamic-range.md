---
title: Uso de DirectX con pantallas de alto rango dinámico y color avanzado
description: En este tema se proporciona información general técnica sobre la representación de contenido de Direct3D 11 y Direct3D 12 de rango dinámico alto en una pantalla de HDR10 con compatibilidad con el color avanzado de Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104565393"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a><span data-ttu-id="383ae-103">Usar DirectX con altas pantallas de rango dinámico y color avanzado</span><span class="sxs-lookup"><span data-stu-id="383ae-103">Using DirectX with high dynamic range Displays and Advanced Color</span></span>

<span data-ttu-id="383ae-104">En este tema se proporciona información general técnica sobre la salida de contenido de Direct3D 11 y Direct3D 12 de rango dinámico alto (HDR) a una pantalla de HDR10 con compatibilidad con el color avanzado de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="383ae-104">This topic provides a technical overview of outputting high dynamic range (HDR) Direct3D 11 and Direct3D 12 content to an HDR10 display using Windows 10 advanced color support.</span></span> <span data-ttu-id="383ae-105">Resume algunas diferencias conceptuales clave entre la salida a las pantallas de HDR10 en comparación con las pantallas del intervalo dinámico estándar tradicional (SDR).</span><span class="sxs-lookup"><span data-stu-id="383ae-105">It summarizes some key conceptual differences between outputting to HDR10 displays as compared to traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="383ae-106">También se tratan los requisitos técnicos clave de la aplicación para admitir correctamente el color avanzado de Windows, así como recomendaciones y prácticas recomendadas.</span><span class="sxs-lookup"><span data-stu-id="383ae-106">It also covers the key technical requirements for your app to properly support Windows advanced color, as well as recommendations and best practices.</span></span>

## <a name="introduction"></a><span data-ttu-id="383ae-107">Introducción</span><span class="sxs-lookup"><span data-stu-id="383ae-107">Introduction</span></span>

<span data-ttu-id="383ae-108">Windows 10 admite HDR y otras pantallas de color avanzadas, que proporcionan una fidelidad de color significativamente mayor que las pantallas de SDR tradicionales.</span><span class="sxs-lookup"><span data-stu-id="383ae-108">Windows 10 supports HDR and other advanced color displays, which provide significantly higher color fidelity than traditional SDR displays.</span></span> <span data-ttu-id="383ae-109">Puede usar Direct3D, Direct2D y otras API de gráficos para representar el contenido HDR en una visualización compatible.</span><span class="sxs-lookup"><span data-stu-id="383ae-109">You can use Direct3D, Direct2D and other graphics APIs to render HDR content to a capable display.</span></span>

<span data-ttu-id="383ae-110">Windows Advanced color hace referencia a varias tecnologías relacionadas, introducidas por primera vez con la versión 1703 de Windows 10, que proporcionan compatibilidad con las pantallas que superan las capacidades de color de las pantallas tradicionales de rango dinámico estándar (SDR).</span><span class="sxs-lookup"><span data-stu-id="383ae-110">Windows advanced color refers to several related technologies, first introduced with Windows 10 version 1703, that provide support for displays that exceed the color capabilities of traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="383ae-111">A continuación se describen las tres principales capacidades extendidas.</span><span class="sxs-lookup"><span data-stu-id="383ae-111">The three major extended capabilities are described below.</span></span> <span data-ttu-id="383ae-112">El tipo más común de presentación de color avanzada, HDR10, admite las tres capacidades extendidas.</span><span class="sxs-lookup"><span data-stu-id="383ae-112">The most common type of advanced color display, HDR10, supports all three extended capabilities.</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="383ae-113">Alto rango dinámico</span><span class="sxs-lookup"><span data-stu-id="383ae-113">High dynamic range</span></span>

<span data-ttu-id="383ae-114">El intervalo dinámico hace referencia a la diferencia entre la luminancia máxima y mínima de una escena. a menudo se mide en nits (candelas por centímetro cuadrado).</span><span class="sxs-lookup"><span data-stu-id="383ae-114">Dynamic range refers to the difference between the maximum and minimum luminance in a scene; this is often measured in nits (candelas per square centimeter).</span></span> <span data-ttu-id="383ae-115">Las escenas del mundo real, como este atardecer, a menudo tienen intervalos dinámicos de 10 pedidos de magnitud de luminancia; el ojo humano puede discernir un rango incluso mayor después de la adaptación.</span><span class="sxs-lookup"><span data-stu-id="383ae-115">Real world scenes, such as this sunset, often have dynamic ranges of 10 orders of magnitude of luminance; the human eye can discern an even greater range after adaptation.</span></span>

![imagen de una puesta de sol con brillo y puntos más oscuros de la escena etiquetada](images/HDR-HDR.jpg)

<span data-ttu-id="383ae-117">Desde Direct3D 9, los motores de gráficos han podido representar internamente sus escenas con este nivel de fidelidad físicamente precisa.</span><span class="sxs-lookup"><span data-stu-id="383ae-117">Ever since Direct3D 9, graphics engines have been able to internally render their scenes with this level of physically accurate fidelity.</span></span> <span data-ttu-id="383ae-118">Sin embargo, una pantalla de intervalo dinámico estándar típica solo puede reproducir un poco más de 3 órdenes de magnitud de luminancia y, por lo tanto, cualquier contenido representado por HDR debe ser tonemapped (comprimido) en el intervalo limitado de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-118">However, a typical standard dynamic range display can reproduce only a little more than 3 orders of magnitude of luminance, and therefore any HDR-rendered content had to be tonemapped (compressed) into the limited range of the display.</span></span> <span data-ttu-id="383ae-119">En las nuevas pantallas HDR, incluidas las que cumplen con el estándar HDR10 (BT. 2100), se interrumpe esta limitación.</span><span class="sxs-lookup"><span data-stu-id="383ae-119">New HDR displays, including those that comply with the HDR10 (BT.2100) standard, break through this limitation.</span></span>

### <a name="wide-color-gamut-with-automatic-system-color-management"></a><span data-ttu-id="383ae-120">Gama de colores anchos con administración automática del color del sistema</span><span class="sxs-lookup"><span data-stu-id="383ae-120">Wide color gamut with automatic system color management</span></span>

<span data-ttu-id="383ae-121">La gama de colores hace referencia al intervalo y la saturación de los matices que puede reproducir una pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-121">Color gamut refers to the range and saturation of hues that a display can reproduce.</span></span> <span data-ttu-id="383ae-122">El color natural más saturado que el ojo humano puede percibir es puro, luz monocromática, como lo que genera un láser.</span><span class="sxs-lookup"><span data-stu-id="383ae-122">The most saturated natural color the human eye can perceive is pure, monochromatic light such as what is produced by a laser.</span></span> <span data-ttu-id="383ae-123">Sin embargo, las pantallas de consumidor estándar a menudo pueden reproducir colores solo dentro de la gama sRGB, que solo representa aproximadamente el 35% de todos los colores que perciben los usuarios.</span><span class="sxs-lookup"><span data-stu-id="383ae-123">However, mainstream consumer displays can often reproduce colors only within the sRGB gamut, which represents only about 35% of all human-perceivable colors.</span></span> <span data-ttu-id="383ae-124">El diagrama siguiente es una representación del "raíz espectral" humano o de todos los colores perceptibles (en un nivel de luminancia determinado), donde el triángulo más pequeño es la gama sRGB.</span><span class="sxs-lookup"><span data-stu-id="383ae-124">The diagram below is a representation of the human "spectral locus", or all perceivable colors (at a given luminance level), where the smaller triangle is the sRGB gamut.</span></span>

![diagrama de la gama raíz y sRGB humana](images/HDR-WCG.jpg)

<span data-ttu-id="383ae-126">En el extremo superior, las pantallas de PC profesionales tienen gamas de colores que son mucho más grandes que sRGB, como Adobe RGB y D65-P3.</span><span class="sxs-lookup"><span data-stu-id="383ae-126">High end, professional PC displays have long supported color gamuts that are significantly wider than sRGB, such as Adobe RGB and D65-P3.</span></span> <span data-ttu-id="383ae-127">Y estas pantallas de gama ancha son cada vez más comunes.</span><span class="sxs-lookup"><span data-stu-id="383ae-127">And these wide gamut displays are becoming more common.</span></span> <span data-ttu-id="383ae-128">Sin embargo, antes del color avanzado, Windows no realizaba ninguna administración de color de nivel de sistema para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="383ae-128">However, prior to advanced color, Windows didn't perform any system-level color management for applications.</span></span> <span data-ttu-id="383ae-129">Esto significaba que si una aplicación de DirectX se representara, por ejemplo, un rojo o RGB puro (1.0, 0,0, 0,0) a su cadena de intercambio, Windows simplemente escanearía el rojo más saturado que podía reproducir la pantalla, independientemente de cuál sea la gama de colores real de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-129">This meant that if a DirectX app rendered, for example, a pure red or RGB(1.0, 0.0, 0.0) to its swap chain, then Windows would simply scan out the most saturated red that the display could reproduce, regardless of what the actual color gamut of the display was.</span></span>

<span data-ttu-id="383ae-130">Las aplicaciones que necesitan una precisión de color alta podrían consultar las capacidades de color de la pantalla (por ejemplo, mediante perfiles de ICC) y realizar su propia administración de color en proceso para dirigirse correctamente a la gama de colores de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-130">Apps that needed high color accuracy could query the color capabilities of the display (for example, using ICC profiles), and perform their own in-process color management to correctly target the display's color gamut.</span></span> <span data-ttu-id="383ae-131">Sin embargo, la gran mayoría de las aplicaciones y el contenido visual suponen que la pantalla es sRGB y que dependen del sistema operativo para cumplir esta suposición.</span><span class="sxs-lookup"><span data-stu-id="383ae-131">However, the vast majority of apps and visual content assume that the display is sRGB, and they rely on the operating system to fulfill this assumption.</span></span>

<span data-ttu-id="383ae-132">Windows Advanced color agrega administración automática del color de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="383ae-132">Windows advanced color adds automatic system-level color management.</span></span> <span data-ttu-id="383ae-133">El Administrador de ventanas de escritorio (DWM) es el compositor de Windows.</span><span class="sxs-lookup"><span data-stu-id="383ae-133">The Desktop Window Manager (DWM) is Windows' compositor.</span></span> <span data-ttu-id="383ae-134">Cuando se habilita el color avanzado, DWM realiza una conversión de color explícita desde el ColorSpace del contenido visual de la aplicación a un espacio de colores de composición canónico, que es scRGB.</span><span class="sxs-lookup"><span data-stu-id="383ae-134">When advanced color is enabled, the DWM performs an explicit color conversion from the app visual content's colorspace to a canonical composition color space, which is scRGB.</span></span> <span data-ttu-id="383ae-135">A continuación, Windows convierte el contenido de fotogramas compuesto en el espacio de colores nativo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-135">Windows then color-converts the composed framebuffer content to the display's native color space.</span></span> <span data-ttu-id="383ae-136">De esta manera, el contenido sRGB tradicional obtiene automáticamente un comportamiento con precisión del color, mientras que las aplicaciones avanzadas para el color pueden aprovechar las capacidades de color completo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-136">In this way, traditional sRGB content automatically gets color-accurate behavior, while advanced color-aware apps can take advantage of the full color capabilities of the display.</span></span>

### <a name="deep-precisionbit-depth"></a><span data-ttu-id="383ae-137">Profundidad de profundidad y profundidad de bits</span><span class="sxs-lookup"><span data-stu-id="383ae-137">Deep precision/bit depth</span></span>

<span data-ttu-id="383ae-138">La precisión numérica, o la profundidad de bits, se refiere a representar o distinguir entre colores similares pero distintos sin bandas ni artefactos.</span><span class="sxs-lookup"><span data-stu-id="383ae-138">Numerical precision, or bit depth, refers to representing or distinguishing between similar but distinct colors without banding nor artifacts.</span></span> <span data-ttu-id="383ae-139">El equipo estándar muestra la compatibilidad con 8 bits por canal de color, mientras que el ojo humano requiere al menos 10-12 bits de precisión para evitar distorsiones perceptibles, sin tener que recurrir a técnicas como el tramado o en función de las condiciones de visualización.</span><span class="sxs-lookup"><span data-stu-id="383ae-139">Mainstream PC displays support 8 bits per color channel, while the human eye requires at least 10-12 bits of precision to avoid perceivable distortions, without resorting to techniques such as dithering or depending on viewing conditions.</span></span>

![imagen de Windmills en una simulación de 2 bits por canal de color frente a 8 bits por canal](images/HDR-bitdepth.jpg)

<span data-ttu-id="383ae-141">Antes del color avanzado, las aplicaciones con ventana restringida de DWM solo envían contenido a 8 bits por canal de color, aunque la pantalla admita una profundidad de bits más alta.</span><span class="sxs-lookup"><span data-stu-id="383ae-141">Prior to advanced color, the DWM restricted windowed apps to output content at only 8 bits per color channel, even if the display supported a higher bit depth.</span></span> <span data-ttu-id="383ae-142">Cuando se habilita el color avanzado, el DWM realiza su composición mediante el punto flotante de media precisión IEEE (FP16), lo que elimina los cuellos de botella y permite que se use la precisión completa de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-142">When advanced color is enabled, the DWM performs its composition using IEEE half-precision floating point (FP16), eliminating any bottlenecks, and allowing the full precision of the display to be used.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="383ae-143">Requisitos del sistema</span><span class="sxs-lookup"><span data-stu-id="383ae-143">System Requirements</span></span>

### <a name="operating-system-os"></a><span data-ttu-id="383ae-144">Sistema operativo (SO)</span><span class="sxs-lookup"><span data-stu-id="383ae-144">Operating system (OS)</span></span>

<span data-ttu-id="383ae-145">La compatibilidad con el color avanzado se incluyó por primera vez con Windows 10, versión 1703, y se ha mejorado significativamente con cada actualización.</span><span class="sxs-lookup"><span data-stu-id="383ae-145">Advanced color support first shipped with Windows 10, version 1703, and it has been significantly improved with each update.</span></span> <span data-ttu-id="383ae-146">En este tema se da por supuesto que la aplicación está dirigida a Windows 10, versión 1903 o posterior.</span><span class="sxs-lookup"><span data-stu-id="383ae-146">This topic assumes that your app is targeting Windows 10, version 1903, or later.</span></span>

### <a name="display"></a><span data-ttu-id="383ae-147">Pantalla</span><span class="sxs-lookup"><span data-stu-id="383ae-147">Display</span></span>

<span data-ttu-id="383ae-148">Para aprovechar el alto rango dinámico, debe tener una pantalla que admita el estándar HDR10.</span><span class="sxs-lookup"><span data-stu-id="383ae-148">To take advantage of high dynamic range, you must have a display that supports the HDR10 standard.</span></span> <span data-ttu-id="383ae-149">Windows funciona mejor con las pantallas que tienen la [certificación VESA DisplayHDR](https://displayhdr.org/).</span><span class="sxs-lookup"><span data-stu-id="383ae-149">Windows works best with displays that are [VESA DisplayHDR certified](https://displayhdr.org/).</span></span>

### <a name="graphics-processor-gpu"></a><span data-ttu-id="383ae-150">Procesador de gráficos (GPU)</span><span class="sxs-lookup"><span data-stu-id="383ae-150">Graphics processor (GPU)</span></span>

<span data-ttu-id="383ae-151">Se requiere una GPU reciente.</span><span class="sxs-lookup"><span data-stu-id="383ae-151">A recent GPU is required.</span></span> <span data-ttu-id="383ae-152">Para admitir pantallas de HDR10, Windows 10 requiere una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="383ae-152">To support HDR10 displays, Windows 10 requires one of the following.</span></span>

* <span data-ttu-id="383ae-153">NVIDIA GeForce 1000 series (Pascal) o posterior</span><span class="sxs-lookup"><span data-stu-id="383ae-153">Nvidia GeForce 1000 series (Pascal), or newer</span></span>
* <span data-ttu-id="383ae-154">AMD Radeon serie 400 (Polaris) o versiones más recientes</span><span class="sxs-lookup"><span data-stu-id="383ae-154">AMD Radeon RX 400 series (Polaris), or newer</span></span>
* <span data-ttu-id="383ae-155">Serie de Intel Core 7 seleccionada (Kaby Lake) o posterior</span><span class="sxs-lookup"><span data-stu-id="383ae-155">Selected Intel Core 7 series (Kaby Lake), or newer</span></span>

<span data-ttu-id="383ae-156">Tenga en cuenta que se aplican requisitos de hardware adicionales en función de los escenarios, incluida la aceleración de códecs de hardware (HEVC de 10 bits, VP9 de 10 bits, etc.) y la compatibilidad con PlayReady (SL3000).</span><span class="sxs-lookup"><span data-stu-id="383ae-156">Note that additional hardware requirements apply depending on the scenarios, including hardware codec acceleration (10 bit HEVC, 10 bit VP9, etc.) and PlayReady support (SL3000).</span></span> <span data-ttu-id="383ae-157">Póngase en contacto con su proveedor de GPU para obtener información más específica.</span><span class="sxs-lookup"><span data-stu-id="383ae-157">Contact your GPU vendor for more specific information.</span></span>

### <a name="graphics-driver-wddm"></a><span data-ttu-id="383ae-158">Controlador de gráficos (WDDM)</span><span class="sxs-lookup"><span data-stu-id="383ae-158">Graphics driver (WDDM)</span></span>

<span data-ttu-id="383ae-159">Se recomienda encarecidamente el controlador de gráficos más reciente disponible, ya sea desde Windows Update o desde el sitio web del fabricante de la GPU o del equipo.</span><span class="sxs-lookup"><span data-stu-id="383ae-159">The latest available graphics driver is strongly recommended, either from Windows Update or from the GPU vendor or PC manufacturer's website.</span></span> <span data-ttu-id="383ae-160">En Windows 10, versión 1903 y versiones posteriores, se recomiendan controladores que admitan como mínimo Windows Display Driver Model (WDDM), versión 2,6.</span><span class="sxs-lookup"><span data-stu-id="383ae-160">For Windows 10, version 1903, and later, we recommend drivers that support at least Windows Display Driver Model (WDDM) version 2.6.</span></span>

## <a name="supported-rendering-apis"></a><span data-ttu-id="383ae-161">API de representación compatibles</span><span class="sxs-lookup"><span data-stu-id="383ae-161">Supported rendering APIs</span></span>

<span data-ttu-id="383ae-162">Windows 10 admite una amplia variedad de plataformas y API de representación.</span><span class="sxs-lookup"><span data-stu-id="383ae-162">Windows 10 supports a wide variety of rendering APIs and frameworks.</span></span> <span data-ttu-id="383ae-163">En esencia, la compatibilidad con colores avanzada se basa en la aplicación para realizar una presentación moderna con las API de nivel visual o DXGI.</span><span class="sxs-lookup"><span data-stu-id="383ae-163">Advanced color support fundamentally relies on your app being able to perform modern presentation using either DXGI or the Visual Layer APIs.</span></span>

* [<span data-ttu-id="383ae-164">Infraestructura de gráficos de DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="383ae-164">DirectX Graphics Infrastructure (DXGI)</span></span>](../direct3ddxgi/dx-graphics-dxgi.md)
* [<span data-ttu-id="383ae-165">Capa visual (Windows. UI. Composition)</span><span class="sxs-lookup"><span data-stu-id="383ae-165">Visual Layer (Windows.UI.Composition)</span></span>](/windows/uwp/composition/visual-layer)

<span data-ttu-id="383ae-166">Por lo tanto, todas las API de representación que pueden generar resultados en uno de estos métodos de presentación pueden admitir el color avanzado.</span><span class="sxs-lookup"><span data-stu-id="383ae-166">Therefore, any rendering API that can output to one of these presentations methods can support advanced color.</span></span> <span data-ttu-id="383ae-167">Esto incluye pero no se limita a ello.</span><span class="sxs-lookup"><span data-stu-id="383ae-167">This includes but is not limited to these.</span></span>

* [<span data-ttu-id="383ae-168">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="383ae-168">Direct3D 11</span></span>](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [<span data-ttu-id="383ae-169">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="383ae-169">Direct3D 12</span></span>](../direct3d12/direct3d-12-graphics.md)
* [<span data-ttu-id="383ae-170">Direct2D</span><span class="sxs-lookup"><span data-stu-id="383ae-170">Direct2D</span></span>](../direct2d/direct2d-portal.md)
* [<span data-ttu-id="383ae-171">Win2D</span><span class="sxs-lookup"><span data-stu-id="383ae-171">Win2D</span></span>](https://github.com/Microsoft/Win2D)
  * <span data-ttu-id="383ae-172">Requiere el uso de las API de **CanvasSwapChain** o **CanvasSwapChainPanel** de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="383ae-172">Requires using the lower level **CanvasSwapChain** or **CanvasSwapChainPanel** APIs.</span></span>
* [<span data-ttu-id="383ae-173">**Windows.UI.Input.Inking**</span><span class="sxs-lookup"><span data-stu-id="383ae-173">**Windows.UI.Input.Inking**</span></span>](/uwp/api/Windows.UI.Input.Inking)
  * <span data-ttu-id="383ae-174">Admite la representación de tinta seca personalizada mediante DirectX.</span><span class="sxs-lookup"><span data-stu-id="383ae-174">Supports custom dry ink rendering using DirectX.</span></span>
* [<span data-ttu-id="383ae-175">XAML</span><span class="sxs-lookup"><span data-stu-id="383ae-175">XAML</span></span>](/windows/uwp/xaml-platform/)
  * <span data-ttu-id="383ae-176">Admite la reproducción de vídeos HDR mediante **MediaPlayerElement**.</span><span class="sxs-lookup"><span data-stu-id="383ae-176">Supports playback of HDR videos using **MediaPlayerElement**.</span></span>
  * <span data-ttu-id="383ae-177">Admite el descodificación de imágenes JPEG XR mediante el elemento de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="383ae-177">Supports decode of JPEG XR images using **Image** element.</span></span>
  * <span data-ttu-id="383ae-178">Admite la interoperabilidad de DirectX mediante **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="383ae-178">Supports DirectX interop using **SwapChainPanel**.</span></span>

## <a name="handling-dynamic-display-capabilities"></a><span data-ttu-id="383ae-179">Controlar las capacidades de visualización dinámica</span><span class="sxs-lookup"><span data-stu-id="383ae-179">Handling dynamic display capabilities</span></span>

<span data-ttu-id="383ae-180">Windows 10 es compatible con una amplia gama de pantallas avanzadas de uso de color, desde paneles integrados con eficacia energética hasta monitores y televisores de juegos de gama alta.</span><span class="sxs-lookup"><span data-stu-id="383ae-180">Windows 10 supports an enormous range of advanced color-capable displays, from power-efficient integrated panels to high end gaming monitors and TVs.</span></span> <span data-ttu-id="383ae-181">Los usuarios de Windows esperan que la aplicación controle sin problemas todas estas variaciones, incluidas las pantallas de SDR existentes.</span><span class="sxs-lookup"><span data-stu-id="383ae-181">Windows users expect that your app will seamlessly handle all of these variations, including ubiquitous existing SDR displays.</span></span>

<span data-ttu-id="383ae-182">Windows 10 proporciona control sobre las funcionalidades de color avanzado y HDR al usuario.</span><span class="sxs-lookup"><span data-stu-id="383ae-182">Windows 10 provides control over HDR and advanced color capabilities to the user.</span></span> <span data-ttu-id="383ae-183">La aplicación debe detectar la configuración de la pantalla actual y responder dinámicamente a cualquier cambio en la capacidad.</span><span class="sxs-lookup"><span data-stu-id="383ae-183">Your app must detect the current display's configuration, and respond dynamically to any changes in capability.</span></span> <span data-ttu-id="383ae-184">Esto puede ocurrir por muchas razones, por ejemplo, porque el usuario ha habilitado o deshabilitado una característica, o ha desplazado la aplicación entre distintas pantallas o ha cambiado el estado de energía del sistema.</span><span class="sxs-lookup"><span data-stu-id="383ae-184">This could occur for many reasons, for example, because the user enabled or disabled a feature, or moved the app between different displays, or the system's power state changed.</span></span>

### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="383ae-185">Aplicaciones de la Plataforma universal de Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="383ae-185">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="383ae-186">Si va a escribir una aplicación para UWP, independientemente de la API de representación de gráficos que esté usando, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) para obtener funcionalidades de visualización.</span><span class="sxs-lookup"><span data-stu-id="383ae-186">If you're writing a UWP app, regardless of the graphics rendering API you're using, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get display capabilities.</span></span> <span data-ttu-id="383ae-187">Obtenga una instancia de **AdvancedColorInfo** de [**DisplayInformation:: GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span><span class="sxs-lookup"><span data-stu-id="383ae-187">Obtain an instance of **AdvancedColorInfo** from [**DisplayInformation::GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span></span>

<span data-ttu-id="383ae-188">Para comprobar qué tipo de color avanzado está activo actualmente, use la propiedad [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) .</span><span class="sxs-lookup"><span data-stu-id="383ae-188">To check what advanced color kind is currently active, use the [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) property.</span></span> <span data-ttu-id="383ae-189">En Windows 10, versión 1903 y versiones posteriores, devuelve uno de los tres valores posibles: **SDR**, **WCG** o **HDR**.</span><span class="sxs-lookup"><span data-stu-id="383ae-189">In Windows 10, version 1903, and later, this returns one of three possible values: **SDR**, **WCG**, or **HDR**.</span></span> <span data-ttu-id="383ae-190">Esta es la propiedad más importante que se va a comprobar y debe configurar la canalización de representación y presentación en respuesta a la clase activa.</span><span class="sxs-lookup"><span data-stu-id="383ae-190">This is the most important property to check, and you should configure your render and presentation pipeline in response to the active kind.</span></span>

<span data-ttu-id="383ae-191">Para comprobar qué tipos de color avanzado se admiten, pero no necesariamente activos, llame a [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span><span class="sxs-lookup"><span data-stu-id="383ae-191">To check what advanced color kinds are supported, but not necessarily active, call [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span></span> <span data-ttu-id="383ae-192">Puede usar esta información, por ejemplo, para solicitar al usuario que vaya a la aplicación de configuración de Windows para que pueda habilitar HDR o WCG.</span><span class="sxs-lookup"><span data-stu-id="383ae-192">You could use this information, for example, to prompt the user to navigate to the Windows Settings app so that they can enable HDR or WCG.</span></span>

<span data-ttu-id="383ae-193">Los demás miembros de **AdvancedColorInfo** proporcionan información cuantitativa sobre el volumen de color físico del panel (luminancia y crominancia), que corresponde a los metadatos de HDR estáticos de SMPTE St. 2086.</span><span class="sxs-lookup"><span data-stu-id="383ae-193">The other members of **AdvancedColorInfo** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="383ae-194">Debe usar esta información para configurar la asignación de gama y tonemapping HDR de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="383ae-194">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="383ae-195">Para controlar los cambios en las capacidades de color avanzadas, Regístrese para el evento [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) .</span><span class="sxs-lookup"><span data-stu-id="383ae-195">To handle changes in advanced color capabilities, register for the [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) event.</span></span> <span data-ttu-id="383ae-196">Este evento se desencadena si algún parámetro de las funciones de color avanzadas de la pantalla cambia por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="383ae-196">This event is raised if any parameter of the display's advanced color capabilities changes for any reason.</span></span>

<span data-ttu-id="383ae-197">Controle este evento mediante la obtención de una nueva instancia de **AdvancedColorInfo** y la comprobación de los valores que han cambiado.</span><span class="sxs-lookup"><span data-stu-id="383ae-197">Handle this event by obtaining a new instance of **AdvancedColorInfo**, and checking which values have changed.</span></span>

### <a name="desktop-win32-directx-apps"></a><span data-ttu-id="383ae-198">Aplicaciones DirectX de escritorio (Win32)</span><span class="sxs-lookup"><span data-stu-id="383ae-198">Desktop (Win32) DirectX apps</span></span>

<span data-ttu-id="383ae-199">Si está escribiendo una aplicación de Win32 y usa DirectX para representar, use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) para obtener funcionalidades de visualización.</span><span class="sxs-lookup"><span data-stu-id="383ae-199">If you're writing a Win32 app, and using DirectX to render, then use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get display capabilities.</span></span> <span data-ttu-id="383ae-200">Obtenga una instancia de este struct a través de [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span><span class="sxs-lookup"><span data-stu-id="383ae-200">Obtain an instance of this struct via [**IDXGIOutput6::GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span></span>

<span data-ttu-id="383ae-201">Para comprobar qué tipo de color avanzado está activo actualmente, use la propiedad **ColorSpace** , que es de tipo [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), y contiene uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="383ae-201">To check what advanced color kind is currently active, use the **ColorSpace** property, which is of type [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), and contains one of the following values:</span></span>

* <span data-ttu-id="383ae-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span><span class="sxs-lookup"><span data-stu-id="383ae-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span></span>
* <span data-ttu-id="383ae-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span><span class="sxs-lookup"><span data-stu-id="383ae-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span></span>

> [!Note]
> <span data-ttu-id="383ae-204">Otros tipos de color avanzados, como WCG, se tratan como SDR por DXGI.</span><span class="sxs-lookup"><span data-stu-id="383ae-204">Other advanced color kinds such as WCG are treated as SDR by DXGI.</span></span> <span data-ttu-id="383ae-205">No se puede usar DXGI para identificar una presentación de WCG.</span><span class="sxs-lookup"><span data-stu-id="383ae-205">You can't use DXGI to identify a WCG display.</span></span>

> [!Note]
> <span data-ttu-id="383ae-206">DXGI no permite comprobar qué tipos de color avanzado se admiten, pero no activos en este momento.</span><span class="sxs-lookup"><span data-stu-id="383ae-206">DXGI doesn't let you check what advanced color kinds are supported but not active at the moment.</span></span>

<span data-ttu-id="383ae-207">La mayoría de los demás miembros de **DXGI_OUTPUT_DESC1** proporcionan información cuantitativa sobre el volumen de color físico del panel (luminancia y crominancia), que corresponde a los metadatos de HDR estáticos de SMPTE St. 2086.</span><span class="sxs-lookup"><span data-stu-id="383ae-207">Most of the other members of **DXGI_OUTPUT_DESC1** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="383ae-208">Debe usar esta información para configurar la asignación de gama y tonemapping HDR de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="383ae-208">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="383ae-209">Las aplicaciones Win32 no tienen un mecanismo nativo para responder a los cambios en la funcionalidad de color avanzada.</span><span class="sxs-lookup"><span data-stu-id="383ae-209">Win32 apps don't have a native mechanism to respond to advanced color capability changes.</span></span> <span data-ttu-id="383ae-210">En su lugar, si la aplicación usa un bucle de representación, debe consultar [**IDXGIFactory1:: IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) con cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="383ae-210">Instead, if your app uses a render loop, then you should query [**IDXGIFactory1::IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) with each frame.</span></span> <span data-ttu-id="383ae-211">Si informa de **false**, debe obtener un nuevo **DXGI_OUTPUT_DESC1** y comprobar los valores que han cambiado.</span><span class="sxs-lookup"><span data-stu-id="383ae-211">If it reports **FALSE**, then you should obtain a new **DXGI_OUTPUT_DESC1**, and check which values have changed.</span></span>

<span data-ttu-id="383ae-212">Además, el bombeo de mensajes de Win32 debe controlar el mensaje de [**WM_SIZE**](../winmsg/wm-size.md) , lo que indica que la aplicación puede haberse desplazado entre distintas pantallas.</span><span class="sxs-lookup"><span data-stu-id="383ae-212">In addition, your Win32 message pump should handle the [**WM_SIZE**](../winmsg/wm-size.md) message, which indicates that your app may have moved between different displays.</span></span>

> [!Note]
> <span data-ttu-id="383ae-213">Para obtener una nueva **DXGI_OUTPUT_DESC1**, debe obtener la pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="383ae-213">To obtain a new **DXGI_OUTPUT_DESC1**, you must obtain the current display.</span></span> <span data-ttu-id="383ae-214">Sin embargo, no debe llamar a **IDXGISwapChain:: GetContainingOutput**.</span><span class="sxs-lookup"><span data-stu-id="383ae-214">However, you should not call **IDXGISwapChain::GetContainingOutput**.</span></span> <span data-ttu-id="383ae-215">Esto se debe a que las cadenas de intercambio devolverán una salida de DXGI obsoleta una vez que **DXGIFactory:: IsCurrent** es false y volver a crear la cadena de intercambio para obtener una salida actual genera una pantalla negra temporal.</span><span class="sxs-lookup"><span data-stu-id="383ae-215">This is because swap chains will return a stale DXGI output once **DXGIFactory::IsCurrent** is false, and recreating the swap chain to get a current output results in a temporary black screen.</span></span> <span data-ttu-id="383ae-216">En su lugar, se recomienda enumerar los límites de todas las salidas de DXGI y determinar cuál de ellas tiene la mayor intersección con los límites de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="383ae-216">Instead, we recommend that you enumerate through the bounds of all DXGI outputs, and determine which one has the greatest intersection with your app window's bounds.</span></span>

<span data-ttu-id="383ae-217">El siguiente ejemplo de código procede del [repositorio DirectX-Graphics-samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="383ae-217">The following code example comes from the [DirectX-Graphics-Samples repository](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span>

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a><span data-ttu-id="383ae-218">Configuración de la cadena de intercambio de DirectX</span><span class="sxs-lookup"><span data-stu-id="383ae-218">Setting up Your DirectX swap chain</span></span>

<span data-ttu-id="383ae-219">Una vez que haya determinado que la pantalla admite actualmente capacidades de color avanzadas, configure la cadena de intercambio como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="383ae-219">Once you have determined that the display currently supports advanced color capabilities, configure your swap chain as follows.</span></span>

### <a name="use-a-flip-presentation-model-effect"></a><span data-ttu-id="383ae-220">Usar un efecto de modelo de presentación Flip</span><span class="sxs-lookup"><span data-stu-id="383ae-220">Use a flip presentation model effect</span></span>

<span data-ttu-id="383ae-221">Al crear la cadena de intercambio mediante **CreateSwapChainFor [HWND | Composición |** Los métodos de CoreWindow], debe usar el modelo de volteo de DXGI seleccionando la opción **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** o **DXGI_SWAP_EFFECT_FLIP_DISCARD** , que hace que la cadena de intercambio sea válida para el procesamiento de color avanzado de DWM y varias optimizaciones de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="383ae-221">When creating your swap chain using the **CreateSwapChainFor[Hwnd|Composition|CoreWindow]** methods, you must use the DXGI flip model by selecting either the **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** or **DXGI_SWAP_EFFECT_FLIP_DISCARD** option, which makes your swap chain eligible for advanced color processing from DWM and various fullscreen optimizations.</span></span> <span data-ttu-id="383ae-222">Para obtener más información, consulte el tema para obtener el [mejor rendimiento, use DXGI Flip Model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .</span><span class="sxs-lookup"><span data-stu-id="383ae-222">For more information, refer to the [For best performance, use DXGI flip model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) topic.</span></span>

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a><span data-ttu-id="383ae-223">Opción 1.</span><span class="sxs-lookup"><span data-stu-id="383ae-223">Option 1.</span></span> <span data-ttu-id="383ae-224">Usar el formato de píxel de FP16 y el espacio de colores scRGB</span><span class="sxs-lookup"><span data-stu-id="383ae-224">Use FP16 pixel format and scRGB color space</span></span>

<span data-ttu-id="383ae-225">Windows 10 admite dos combinaciones principales de formato de píxeles y espacio de colores para el color avanzado.</span><span class="sxs-lookup"><span data-stu-id="383ae-225">Windows 10 supports two main combinations of pixel format and color space for advanced color.</span></span> <span data-ttu-id="383ae-226">Seleccione una en función de los requisitos específicos de su aplicación.</span><span class="sxs-lookup"><span data-stu-id="383ae-226">Select one based on your app's specific requirements.</span></span>

<span data-ttu-id="383ae-227">En el caso de las aplicaciones de uso general, al crear la cadena de intercambio, se recomienda especificar [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="383ae-227">For general-purpose apps, when creating your swap chain we recommend specifying [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="383ae-228">Esto también se conoce como *FP16* en el [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="383ae-228">That's also known as *FP16* in your [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="383ae-229">De forma predeterminada, una cadena de intercambio creada con un formato de píxel de punto flotante se trata como si usara el espacio de colores [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) , que también se conoce como *ScRGB*.</span><span class="sxs-lookup"><span data-stu-id="383ae-229">By default, a swap chain created with a floating point pixel format is treated as if it uses the [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) color space, which is also known as *scRGB*.</span></span>

<span data-ttu-id="383ae-230">Esta combinación proporciona el intervalo numérico y la precisión para especificar casi cualquier color físicamente posible y realizar un procesamiento arbitrario que incluye la combinación.</span><span class="sxs-lookup"><span data-stu-id="383ae-230">This combination provides you with the numeric range and precision to specify almost any physically possible color, and perform arbitrary processing including blending.</span></span> <span data-ttu-id="383ae-231">Además, si está usando Direct2D, Win2D o Windows. UI. Composition, esta es la única combinación admitida para cualquier cadena de intercambio o destino intermedio que contenga contenido de color avanzado.</span><span class="sxs-lookup"><span data-stu-id="383ae-231">In addition, if you're using Direct2D, Win2D, or Windows.UI.Composition, then this is the only supported combination for any swap chain or intermediate target that contains advanced color content.</span></span> 

<span data-ttu-id="383ae-232">La principal desventaja de esta opción es que consume 64 bits por píxel, que duplica el ancho de banda de la GPU y el consumo de memoria en comparación con los formatos del píxel de SDR de UINT8 tradicionales.</span><span class="sxs-lookup"><span data-stu-id="383ae-232">The main tradeoff of this option is that it consumes 64 bits per pixel, which doubles GPU bandwidth and memory consumption compared to the traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="383ae-233">Además, scRGB usa valores numéricos que están fuera del intervalo normalizado [0, 1] para representar colores que están fuera de la gama de sRGB y/o superior a 80 Nits de luminancia.</span><span class="sxs-lookup"><span data-stu-id="383ae-233">In addition, scRGB uses numeric values that are outside the normalized [0, 1] range to represent colors that are outside the sRGB gamut and/or greater than 80 nits of luminance.</span></span> <span data-ttu-id="383ae-234">Por ejemplo, scRGB (1,0, 1,0, 1,0) codifica el blanco D65 estándar en 80 Nits; sin embargo, scRGB (12,5, 12,5, 12,5) codifica el mismo blanco de D65 en unos 1000 Nits.</span><span class="sxs-lookup"><span data-stu-id="383ae-234">For example, scRGB (1.0, 1.0, 1.0) encodes the standard D65 white at 80 nits; but scRGB (12.5, 12.5, 12.5) encodes the same D65 white at a much brighter 1000 nits.</span></span> <span data-ttu-id="383ae-235">Algunas operaciones de gráficos requieren un intervalo numérico normalizado y debe modificar la operación o volver a normalizar los valores de color.</span><span class="sxs-lookup"><span data-stu-id="383ae-235">Some graphics operations require a normalized numeric range, and you must either modify the operation, or re-normalize color values.</span></span>

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a><span data-ttu-id="383ae-236">Opción 2: usar el formato de píxel UINT10/RGB10 y el espacio de colores HDR10/BT. 2100</span><span class="sxs-lookup"><span data-stu-id="383ae-236">Option 2: Use UINT10/RGB10 pixel format and HDR10/BT.2100 color space</span></span>

<span data-ttu-id="383ae-237">En el caso de las aplicaciones que consumen contenido codificado en HDR10, como reproductores multimedia o aplicaciones que se espera que se usen principalmente en escenarios de pantalla completa, como juegos, al crear la cadena de intercambio, debería considerar la posibilidad de especificar [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) en [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="383ae-237">For apps that consume HDR10-encoded content, such as media players, or apps that are expected to be used mainly in fullscreen scenarios such as games, when creating your swap chain you should consider specifying [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="383ae-238">De forma predeterminada, esto se trata como si se usara el espacio de color sRGB; por lo tanto, debe llamar explícitamente a [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)y establecer como espacio de colores [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), también conocido como HDR10/BT. 2100.</span><span class="sxs-lookup"><span data-stu-id="383ae-238">By default, this is treated as using the sRGB color space; therefore, you must explicitly call [**IDXGISwapChain3::SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1), and set as your color space [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), also known as HDR10/BT.2100.</span></span>

<span data-ttu-id="383ae-239">Esta combinación tiene restricciones más rigurosas que FP16.</span><span class="sxs-lookup"><span data-stu-id="383ae-239">This combination has more stringent restrictions than FP16.</span></span> <span data-ttu-id="383ae-240">Solo se puede usar con Direct3D 11 o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="383ae-240">You can use this only with Direct3D 11 or Direct3D 12.</span></span> <span data-ttu-id="383ae-241">Además, UINT10/HDR10 tiene limitaciones como un formato intermedio porque usa la función ST. 2084 EOTF ("gamma"), que es muy no lineal y está optimizada como un formato de conexión, y porque solo ofrece 2 bits de alfa.</span><span class="sxs-lookup"><span data-stu-id="383ae-241">In addition, UINT10/HDR10 has limitations as an intermediate format because it uses the ST.2084 EOTF ("gamma" function), which is highly nonlinear, and optimized as a wire format, and because it offers only 2 bits of alpha.</span></span>

<span data-ttu-id="383ae-242">Sin embargo, esta combinación puede ofrecer optimizaciones de rendimiento eficaces cuando se usa en la salida final de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="383ae-242">However, this combination can offer powerful performance optimizations when used in your app's final output.</span></span> <span data-ttu-id="383ae-243">Consume los mismos 32 bits por píxel que los formatos tradicionales de inglés UINT8 SDR.</span><span class="sxs-lookup"><span data-stu-id="383ae-243">It consumes the same 32 bits per pixel as traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="383ae-244">Además, en ciertos escenarios de pantalla completa, el sistema operativo puede optimizar el rendimiento mediante el análisis directo de la superficie HDR10.</span><span class="sxs-lookup"><span data-stu-id="383ae-244">In addition, in certain fullscreen scenarios, the OS can optimize performance by directly scanning out the HDR10 surface.</span></span>

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a><span data-ttu-id="383ae-245">Usar una cadena de intercambio de color avanzada cuando la pantalla está en modo SDR</span><span class="sxs-lookup"><span data-stu-id="383ae-245">Using an advanced color swap chain when the display is in SDR mode</span></span>

<span data-ttu-id="383ae-246">Puede usar una cadena de intercambio de color avanzada incluso si la pantalla no es compatible con algunas o todas las funciones de color avanzadas que requiere el contenido.</span><span class="sxs-lookup"><span data-stu-id="383ae-246">You can use an advanced color swap chain even if the display doesn't support some or all of the advanced color capabilities your content requires.</span></span> <span data-ttu-id="383ae-247">En estos casos, el Administrador de ventanas de escritorio (DWM) downconvert el contenido para ajustarse a las capacidades de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-247">In those cases, the Desktop Window Manager (DWM) will downconvert your content to fit the display's capabilities.</span></span> <span data-ttu-id="383ae-248">En Windows 10, versión 1903 y versiones posteriores, realizará el recorte numérico; por ejemplo, si se representa en una cadena de intercambio de FP16 scRGB, se recorta todo lo que se encuentra fuera del intervalo numérico [0, 1].</span><span class="sxs-lookup"><span data-stu-id="383ae-248">In Windows 10, version 1903, and later, it will perform numeric clipping; for example, if you render to an FP16 scRGB swap chain, then everything outside of the [0, 1] numeric range is clipped.</span></span>

<span data-ttu-id="383ae-249">Este comportamiento de downconversion también se producirá si la ventana de la aplicación abarca dos o más pantallas con distintas capacidades de color avanzadas.</span><span class="sxs-lookup"><span data-stu-id="383ae-249">This downconversion behavior will also occur if your app window is straddling two or more displays with differing advanced color capabilities.</span></span> <span data-ttu-id="383ae-250">**AdvancedColorInfo** y **IDXGIOutput6** se abstraen para informar únicamente de las características de la presentación "principal" (definidas como la pantalla que contiene el centro de la ventana).</span><span class="sxs-lookup"><span data-stu-id="383ae-250">**AdvancedColorInfo** and **IDXGIOutput6** are abstracted to report only the "main" display's characteristics (defined as the display containing the center of the window).</span></span>

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a><span data-ttu-id="383ae-251">Representar correctamente el contenido de SDR con el nivel blanco de referencia de SDR</span><span class="sxs-lookup"><span data-stu-id="383ae-251">Correctly render SDR content with SDR reference white level</span></span>

<span data-ttu-id="383ae-252">En muchos escenarios, la aplicación querrá representar el contenido de SDR y HDR; por ejemplo, la representación de subtítulos o controles de transporte sobre el vídeo HDR o la interfaz de usuario en una escena de juego.</span><span class="sxs-lookup"><span data-stu-id="383ae-252">In many scenarios, your app will want to render both SDR and HDR content; for example, rendering subtitles or transport controls over HDR video, or UI into a game scene.</span></span> <span data-ttu-id="383ae-253">Es importante comprender el concepto de *nivel blanco de referencia de SDR* para asegurarse de que el contenido de SDR tiene un aspecto correcto en una pantalla HDR.</span><span class="sxs-lookup"><span data-stu-id="383ae-253">It is important to understand the concept of *SDR reference white level* to ensure that your SDR content looks correct on an HDR display.</span></span>

<span data-ttu-id="383ae-254">Windows trata el contenido de HDR como _referencia de la escena_, lo que significa que un valor de color determinado se debe mostrar en un nivel de luminancia específico; por ejemplo, scRGB (1,0, 1,0, 1,0) y HDR10 (497, 497, 497) codifican exactamente el blanco D65 en la luminancia de 80 Nits.</span><span class="sxs-lookup"><span data-stu-id="383ae-254">Windows treats HDR content as _scene-referred_, meaning that a particular color value should be displayed at a specific luminance level; for example, scRGB (1.0, 1.0, 1.0) and HDR10 (497, 497, 497) both encode exactly D65 white at 80 nits luminance.</span></span> <span data-ttu-id="383ae-255">Mientras tanto, el contenido de SDR tradicionalmente se ha _remitido_ (o se ha remitido a la presentación), lo que significa que su luminancia se deja al usuario o al dispositivo. por ejemplo sRGB (1,0, 1,0, 1,0) codifica el blanco D65 como en los ejemplos de HDR, pero con la luminancia máxima para la que esté configurada la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-255">Meanwhile, SDR content traditionally has been _output-referred_ (or display-referred), meaning that its luminance is left up to the user or the device; for example sRGB (1.0, 1.0, 1.0) encodes D65 white as in the HDR examples, but at whatever maximum luminance the display is configured for.</span></span> <span data-ttu-id="383ae-256">Windows permite al usuario ajustar el _nivel blanco de referencia de SDR_ a sus preferencias; Esta es la luminancia que Windows representará sRGB (1,0, 1,0, 1,0) en.</span><span class="sxs-lookup"><span data-stu-id="383ae-256">Windows allows the user to adjust the _SDR reference white level_ to their preference; this is the luminance that Windows will render sRGB (1.0, 1.0, 1.0) at.</span></span> <span data-ttu-id="383ae-257">En los monitores de encabezado de los equipos de escritorio, los niveles blancos de referencia de SDR normalmente se establecen en unos 200 Nits.</span><span class="sxs-lookup"><span data-stu-id="383ae-257">On desktop HDR monitors, SDR reference white levels are typically set to around 200 nits.</span></span>

> [!Note]
> <span data-ttu-id="383ae-258">En una pantalla que admita un control de brillo, como en un equipo portátil, Windows también ajustará la luminancia del contenido HDR (con referencia a la escena) para que coincida con el nivel de brillo deseado del usuario, pero esto es invisible para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="383ae-258">On a display that supports a brightness control, such as on a laptop, Windows will also adjust the luminance of HDR (scene-referred) content to match the user's desired brightness level, but this is invisible to the app.</span></span> <span data-ttu-id="383ae-259">A menos que esté intentando garantizar la reproducción de la señal HDR con precisión de bits, por lo general puede pasarlo por alto.</span><span class="sxs-lookup"><span data-stu-id="383ae-259">Unless you're trying to guarantee bit-accurate reproduction of the HDR signal, you can generally ignore this.</span></span>

<span data-ttu-id="383ae-260">Si la aplicación siempre representa SDR y HDR para separar superficies y se basa en la composición del sistema operativo, Windows realizará automáticamente el ajuste correcto para aumentar el contenido de SDR al nivel de blanco deseado.</span><span class="sxs-lookup"><span data-stu-id="383ae-260">If your app always renders SDR and HDR to separate surfaces, and relies on OS composition, then Windows will automatically perform the correct adjustment to boost SDR content to the desired white level.</span></span> <span data-ttu-id="383ae-261">Por ejemplo, si la aplicación usa XAML y representa el contenido HDR en su propio **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="383ae-261">For example, if your app uses XAML and renders HDR content to its own **SwapChainPanel**.</span></span>

<span data-ttu-id="383ae-262">Sin embargo, si la aplicación realiza su propia composición de contenido de SDR y HDR en una sola superficie, es el responsable de realizar el ajuste de nivel blanco de referencia de SDR usted mismo.</span><span class="sxs-lookup"><span data-stu-id="383ae-262">However, if your app performs its own composition of SDR and HDR content into a single surface, then you're responsible for performing the SDR reference white level adjustment yourself.</span></span> <span data-ttu-id="383ae-263">En caso contrario, es posible que el contenido de SDR parezca demasiado tenue suponiendo condiciones típicas de visualización del escritorio.</span><span class="sxs-lookup"><span data-stu-id="383ae-263">Otherwise the SDR content might appear too dim assuming typical desktop viewing conditions.</span></span> <span data-ttu-id="383ae-264">En primer lugar, debe obtener el nivel de documento de referencia de SDR actual y, después, debe ajustar los valores de color de cualquier contenido de SDR que esté representando.</span><span class="sxs-lookup"><span data-stu-id="383ae-264">First, you must obtain the current SDR reference white level, and then you must adjust the color values of any SDR content you're rendering.</span></span>

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a><span data-ttu-id="383ae-265">Paso 1.</span><span class="sxs-lookup"><span data-stu-id="383ae-265">Step 1.</span></span> <span data-ttu-id="383ae-266">Obtención del nivel blanco actual de referencia de SDR</span><span class="sxs-lookup"><span data-stu-id="383ae-266">Obtain the current SDR reference white level</span></span>

<span data-ttu-id="383ae-267">Actualmente, solo las aplicaciones UWP pueden obtener el nivel de blanco de referencia de SDR actual a través de [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span><span class="sxs-lookup"><span data-stu-id="383ae-267">Currently, only UWP apps can obtain the current SDR reference white level via [**AdvancedColorInfo.SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span></span> <span data-ttu-id="383ae-268">Esta API requiere un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="383ae-268">This API requires a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

### <a name="step-2-adjust-color-values-of-sdr-content"></a><span data-ttu-id="383ae-269">Paso 2.</span><span class="sxs-lookup"><span data-stu-id="383ae-269">Step 2.</span></span> <span data-ttu-id="383ae-270">Ajustar los valores de color del contenido de SDR</span><span class="sxs-lookup"><span data-stu-id="383ae-270">Adjust color values of SDR content</span></span>

<span data-ttu-id="383ae-271">Windows define el nivel blanco nominal o predeterminado de referencia en 80 Nits; por lo tanto, si tuviera que representar un blanco estándar sRGB (1,0, 1,0, 1,0) en una cadena de intercambio de FP16, se volvería a producir con una luminancia de 80 Nits.</span><span class="sxs-lookup"><span data-stu-id="383ae-271">Windows defines the nominal, or default, reference white level at 80 nits; therefore if you were to render a standard sRGB (1.0, 1.0, 1.0) white to an FP16 swap chain, it would be reproduced at 80 nits luminance.</span></span> <span data-ttu-id="383ae-272">Para que coincida con el nivel de blanco de referencia definido por el usuario real, debe ajustar el contenido de SDR desde 80 Nits hasta el nivel especificado a través de **AdvancedColorInfo. SdrWhiteLevelInNits**.</span><span class="sxs-lookup"><span data-stu-id="383ae-272">In order to match the actual user-defined reference white level, you must adjust SDR content from 80 nits to the level specified via **AdvancedColorInfo.SdrWhiteLevelInNits**.</span></span>

<span data-ttu-id="383ae-273">Si va a representar con FP16 y ScRGB, o cualquier espacio de colores que use gamma lineal (1,0), puede multiplicar el valor de color de SDR por _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_.</span><span class="sxs-lookup"><span data-stu-id="383ae-273">If you're rendering using FP16 and scRGB, or any color space that uses linear (1.0) gamma, then you can simply multiply the SDR color value by _AdvancedColorInfo.SdrWhiteLevelInNits_ / _80_.</span></span> <span data-ttu-id="383ae-274">Si utiliza Direct2D, hay una constante predefinida [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), que tiene un valor de 80.</span><span class="sxs-lookup"><span data-stu-id="383ae-274">If you're using Direct2D, there is a predefined constant [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), which has a value of 80.</span></span>

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

<span data-ttu-id="383ae-275">Si está representando mediante un espacio de colores de gamma no lineal como HDR10, la realización del ajuste de nivel blanco de SDR es más compleja. Si está escribiendo su propio sombreador de píxeles, considere la posibilidad de convertir en gamma lineal para aplicar el ajuste.</span><span class="sxs-lookup"><span data-stu-id="383ae-275">If you're rendering using a nonlinear gamma color space such as HDR10, then performing SDR white level adjustment is more complex; if you're writing your own pixel shader you should consider converting into linear gamma to apply the adjustment.</span></span>

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a><span data-ttu-id="383ae-276">Adaptación del contenido de HDR a las capacidades de la pantalla mediante tonemapping</span><span class="sxs-lookup"><span data-stu-id="383ae-276">Adapt HDR content to the display's capabilities using tonemapping</span></span>

<span data-ttu-id="383ae-277">Las pantallas de color avanzado y HDR varían en gran medida en función de sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="383ae-277">HDR and advanced color displays vary greatly in terms of their capabilities.</span></span> <span data-ttu-id="383ae-278">Por ejemplo, la luminancia mínima y máxima y la gama de colores son capaces de reproducir.</span><span class="sxs-lookup"><span data-stu-id="383ae-278">For example, the minimum and maximum luminance and the color gamut they are capable of reproducing.</span></span> <span data-ttu-id="383ae-279">En muchos casos, el contenido de HDR contendrá colores que superan las capacidades de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-279">In many cases, your HDR content will contain colors that exceed the display's capabilities.</span></span> <span data-ttu-id="383ae-280">Para obtener la mejor calidad de imagen, es importante que realice tonemappings HDR, con lo que comprime en esencia el intervalo de colores para ajustarse a la pantalla, al mismo tiempo que se conserva la intención visual del contenido.</span><span class="sxs-lookup"><span data-stu-id="383ae-280">For the best image quality it is important for you to perform HDR tonemapping, essentially compressing the range of colors to fit the display while best preserving the visual intent of the content.</span></span>

<span data-ttu-id="383ae-281">El parámetro único más importante para adaptarse es la luminancia máxima, también conocido como MaxCLL (nivel de luz de contenido); los tonemappers más sofisticados también adaptarán la luminancia mínima (MinCLL) y/o los primarios de color.</span><span class="sxs-lookup"><span data-stu-id="383ae-281">The most important single parameter to adapt for is max luminance, also known as MaxCLL (content light level); more sophisticated tonemappers will also adapt min luminance (MinCLL) and/or color primaries.</span></span>

### <a name="step-1-get-the-displays-color-volume-capabilities"></a><span data-ttu-id="383ae-282">Paso 1.</span><span class="sxs-lookup"><span data-stu-id="383ae-282">Step 1.</span></span> <span data-ttu-id="383ae-283">Obtención de las capacidades de volumen de color de la pantalla</span><span class="sxs-lookup"><span data-stu-id="383ae-283">Get the display's color volume capabilities</span></span>

#### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="383ae-284">Aplicaciones de la Plataforma universal de Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="383ae-284">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="383ae-285">Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) para obtener el volumen de color de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-285">Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get the display's color volume.</span></span>

#### <a name="win32-desktop-directx-apps"></a><span data-ttu-id="383ae-286">Win32 (escritorio) aplicaciones DirectX</span><span class="sxs-lookup"><span data-stu-id="383ae-286">Win32 (desktop) DirectX apps</span></span>

<span data-ttu-id="383ae-287">Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) para obtener el volumen de color de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="383ae-287">Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get the display's color volume.</span></span>

### <a name="step-2-get-the-contents-color-volume-information"></a><span data-ttu-id="383ae-288">Paso 2.</span><span class="sxs-lookup"><span data-stu-id="383ae-288">Step 2.</span></span> <span data-ttu-id="383ae-289">Obtención de la información de volumen de color del contenido</span><span class="sxs-lookup"><span data-stu-id="383ae-289">Get the content's color volume information</span></span>

<span data-ttu-id="383ae-290">En función de dónde provenga el contenido de HDR, hay varias formas posibles de determinar la luminancia y la información de la gama de colores.</span><span class="sxs-lookup"><span data-stu-id="383ae-290">Depending on where your HDR content came from, there are multiple potential ways to determine its luminance and color gamut information.</span></span> <span data-ttu-id="383ae-291">Algunos archivos de imagen y vídeo HDR contienen metadatos SMPTE ST. 2086.</span><span class="sxs-lookup"><span data-stu-id="383ae-291">Certain HDR video and image files contain SMPTE ST.2086 metadata.</span></span> <span data-ttu-id="383ae-292">Si el contenido se representó dinámicamente, es posible que pueda extraer información de la escena de las fases de representación internas, por ejemplo, la fuente de luz más brillante de una escena.</span><span class="sxs-lookup"><span data-stu-id="383ae-292">If your content was rendered dynamically, then you may be able to extract scene information from the internal rendering stages, for example the brightest light source in a scene.</span></span>

<span data-ttu-id="383ae-293">Una solución más general pero costosamente costosa es ejecutar un histograma u otro paso de análisis en el fotograma representado.</span><span class="sxs-lookup"><span data-stu-id="383ae-293">A more general but computationally expensive solution is to run a histogram or other analysis pass on the rendered frame.</span></span> <span data-ttu-id="383ae-294">El [ejemplo de SDK de imágenes de color avanzado de direct2d](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) muestra cómo hacerlo con Direct2D; a continuación se incluyen los fragmentos de código más relevantes:</span><span class="sxs-lookup"><span data-stu-id="383ae-294">The [Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) demonstrates how to do this using Direct2D; the most relevant code snippets are included below:</span></span>

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a><span data-ttu-id="383ae-295">Paso 3.</span><span class="sxs-lookup"><span data-stu-id="383ae-295">Step 3.</span></span> <span data-ttu-id="383ae-296">Realización de la operación HDR tonemapping</span><span class="sxs-lookup"><span data-stu-id="383ae-296">Perform the HDR tonemapping operation</span></span>

<span data-ttu-id="383ae-297">Tonemapping es intrínsecamente un proceso de pérdida y se puede optimizar para una serie de métricas perceptuales o objetivas, por lo que no hay un algoritmo estándar.</span><span class="sxs-lookup"><span data-stu-id="383ae-297">Tonemapping is inherently a lossy process, and can be optimized for a number of perceptual or objective metrics, so there is no one standard algorithm.</span></span> <span data-ttu-id="383ae-298">Windows proporciona un [efecto tonemapper de HDR](../direct2d/hdr-tone-map-effect.md) integrado como parte de Direct2D y en la canalización de reproducción de vídeo HDR Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="383ae-298">Windows provides a built-in [HDR tonemapper effect](../direct2d/hdr-tone-map-effect.md) as part of Direct2D as well as in the Media Foundation HDR video playback pipeline.</span></span> <span data-ttu-id="383ae-299">Entre otros algoritmos de uso común se incluyen las ACE filme, Reinhard y ITU-R BT. 2390-3 EETF (función de transferencia eléctrica eléctrica).</span><span class="sxs-lookup"><span data-stu-id="383ae-299">Some other commonly used algorithms include ACES Filmic, Reinhard, and ITU-R BT.2390-3 EETF (electrical-electrical transfer function).</span></span>

<span data-ttu-id="383ae-300">A continuación se muestra un operador Reinhard tonemapper simplificado.</span><span class="sxs-lookup"><span data-stu-id="383ae-300">A simplified Reinhard tonemapper operator is shown below.</span></span>

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a><span data-ttu-id="383ae-301">Captura de contenido de HDR y WCG</span><span class="sxs-lookup"><span data-stu-id="383ae-301">Capturing HDR and WCG content</span></span>

<span data-ttu-id="383ae-302">Las API que admiten la especificación de formatos de píxeles, como las del espacio de nombres [**Windows. Graphics. Capture**](/uwp/api/windows.graphics.capture) y el método [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , proporcionan la capacidad de capturar contenido HDR y WCG sin perder información de píxeles.</span><span class="sxs-lookup"><span data-stu-id="383ae-302">APIs that support specifying pixel formats, such as those in the [**Windows.Graphics.Capture**](/uwp/api/windows.graphics.capture) namespace, and the [**IDXGIOutput5::DuplicateOutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) method, provide the capability to capture HDR and WCG content without losing pixel information.</span></span> <span data-ttu-id="383ae-303">Tenga en cuenta que después de adquirir los marcos de contenido, se requiere un procesamiento adicional.</span><span class="sxs-lookup"><span data-stu-id="383ae-303">Note that after acquiring content frames, additional processing is required.</span></span> <span data-ttu-id="383ae-304">Por ejemplo, la asignación de tonos HDR a SDR (por ejemplo, copia de pantalla de SDR para el uso compartido de Internet) y almacenamiento de contenido con el formato correcto (por ejemplo, JPEG XR).</span><span class="sxs-lookup"><span data-stu-id="383ae-304">For example, HDR-to-SDR tone mapping (for example, SDR screenshot copy for Internet sharing) and content saving with proper format (for example, JPEG XR).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="383ae-305">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="383ae-305">Additional resources</span></span>

* <span data-ttu-id="383ae-306">*Uso de la representación de HDR con el kit de herramientas de DirectX* para DirectX [11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span><span class="sxs-lookup"><span data-stu-id="383ae-306">*Using HDR Rendering with the DirectX Tool Kit* for [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering) / [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span></span> <span data-ttu-id="383ae-307">Tutorial sobre cómo agregar compatibilidad con HDR a una aplicación de DirectX mediante el kit de herramientas de DirectX (DirectXTK).</span><span class="sxs-lookup"><span data-stu-id="383ae-307">Walkthrough of how to add HDR support to a DirectX app using the DirectX Tool Kit (DirectXTK).</span></span>
* <span data-ttu-id="383ae-308">[Ejemplo de SDK de imágenes de color avanzadas de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span><span class="sxs-lookup"><span data-stu-id="383ae-308">[Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span></span> <span data-ttu-id="383ae-309">Ejemplo de SDK de UWP que implementa un visor de imágenes HDR y WCG avanzado compatible con el color mediante Direct2D.</span><span class="sxs-lookup"><span data-stu-id="383ae-309">UWP SDK sample implementing an advanced color-aware HDR and WCG image viewer using Direct2D.</span></span> <span data-ttu-id="383ae-310">Muestra el abanico completo de procedimientos recomendados para las aplicaciones UWP, como la respuesta a la visualización de cambios en la funcionalidad y el ajuste del nivel blanco de SDR.</span><span class="sxs-lookup"><span data-stu-id="383ae-310">Demonstrates the full range of best practices for UWP apps, including responding to display capability changes and adjusting for SDR white level.</span></span>
* <span data-ttu-id="383ae-311">[Ejemplo de escritorio de encabezado de Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="383ae-311">[Direct3D 12 HDR desktop sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span> <span data-ttu-id="383ae-312">Ejemplo de SDK de escritorio que implementa una escena de HDR de Direct3D 12 básica.</span><span class="sxs-lookup"><span data-stu-id="383ae-312">Desktop SDK sample implementing a basic Direct3D 12 HDR scene.</span></span>
* <span data-ttu-id="383ae-313">[Ejemplo de UWP de Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="383ae-313">[Direct3D 12 HDR UWP sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span></span> <span data-ttu-id="383ae-314">Equivalente a UWP del ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="383ae-314">UWP equivalent of the above sample.</span></span>
* <span data-ttu-id="383ae-315">[Ejemplo de PC SimpleHDR de Xbox ATG](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span><span class="sxs-lookup"><span data-stu-id="383ae-315">[Xbox ATG SimpleHDR PC sample](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span></span> <span data-ttu-id="383ae-316">Ejemplo de SDK de escritorio que implementa una escena de HDR de Direct3D 11 básica.</span><span class="sxs-lookup"><span data-stu-id="383ae-316">Desktop SDK sample implementing a basic Direct3D 11 HDR scene.</span></span>

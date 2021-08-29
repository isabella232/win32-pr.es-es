---
title: Uso de DirectX con pantallas de alto rango dinámico y color avanzado
description: En este tema se proporciona información técnica sobre la representación de contenido de direct3D 11 y Direct3D 12 de alto rango dinámico en una pantalla DE HDR10 Windows 10 compatibilidad avanzada con colores.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 8577d9737bd1f5f22f5e550dbcef503151c84dc1a147cf510820b589283b4990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120575"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a>Uso de DirectX con un rango dinámico alto Muestra y Color avanzado

En este tema se proporciona información técnica sobre cómo generar contenido de alto rango dinámico (HDR) Direct3D 11 y Direct3D 12 en una pantalla DE HDR10 Windows 10 compatibilidad avanzada con colores. En él se resumen algunas diferencias conceptuales clave entre la salida y las pantallas de HDR10 en comparación con las pantallas de intervalo dinámico estándar (SDR) tradicionales. También se tratan los requisitos técnicos clave para que la aplicación admita correctamente Windows color avanzado, así como recomendaciones y procedimientos recomendados.

## <a name="introduction"></a>Introducción

Windows 10 compatibilidad con HDR y otras pantallas de color avanzadas, que proporcionan una fidelidad de color significativamente mayor que las pantallas SDR tradicionales. Puede usar Direct3D, Direct2D y otras API de gráficos para representar el contenido DE HDR en una pantalla compatible.

Windows color avanzado hace referencia a varias tecnologías relacionadas, introducidas por primera vez con la versión 1703 de Windows 10, que proporcionan compatibilidad con pantallas que superan las funcionalidades de color de las pantallas de intervalo dinámico estándar (SDR) tradicionales. A continuación se describen las tres principales funcionalidades extendidas. El tipo más común de pantalla de color avanzada, HDR10, admite las tres funcionalidades extendidas.

### <a name="high-dynamic-range"></a>Alto intervalo dinámico

El intervalo dinámico hace referencia a la diferencia entre la luminosidad máxima y mínima de una escena; a menudo se mide en nits (candelas por cent centrón cuadrado). Las escenas del mundo real, como esta puesta de sol, suelen tener intervalos dinámicos de 10 órdenes de magnitud de luminosidad; el ojo humano puede distinguir un intervalo aún mayor después de la adaptación.

![imagen de una puesta de sol con brillo y puntos más oscuros en la escena etiquetados](images/HDR-HDR.jpg)

Desde Direct3D 9, los motores gráficos han podido representar internamente sus escenas con este nivel de fidelidad físicamente precisa. Sin embargo, una pantalla de intervalo dinámico estándar típica solo puede reproducir un poco más de 3 órdenes de magnitud de la luminosidad y, por tanto, cualquier contenido representado por HDR se tenía que recortar (comprimir) en el intervalo limitado de la pantalla. Las nuevas pantallas de HDR, incluidas las que cumplen con el estándar HDR10 (BT.2100), interrumpirán esta limitación.

### <a name="wide-color-gamut-with-automatic-system-color-management"></a>Amplia gama de colores con administración automática del color del sistema

La gama de colores hace referencia al intervalo y la saturación de los matiz que puede reproducir una pantalla. El color natural más saturado que puede percibir el ojo humano es la luz monocromática pura, como la que produce un rayo. Sin embargo, las pantallas de consumidor estándar a menudo pueden reproducir colores solo dentro de la gama sRGB, que representa solo aproximadamente el 35 % de todos los colores que se pueden obtener por el usuario. El diagrama siguiente es una representación del "locus espectral" humano o de todos los colores que se pueden percibir (en un nivel de luminosidad determinado), donde el triángulo más pequeño es la gama sRGB.

![diagrama del locus espectral humano y la gama sRGB](images/HDR-WCG.jpg)

Las pantallas de equipos profesionales de gama alta tienen gamas de colores largas admitidas que son significativamente más anchas que sRGB, como Adobe RGB y D65-P3. Y estas pantallas de gama amplia son cada vez más comunes. Sin embargo, antes del color avanzado, Windows no realizaba ninguna administración de colores de nivel de sistema para las aplicaciones. Esto significaba que si una aplicación de DirectX representara, por ejemplo, un rojo puro o RGB (1.0, 0.0, 0.0) en su cadena de intercambio, Windows simplemente examinaría el rojo más saturado que la pantalla podría reproducir, independientemente de cuál fuera la gama de color real de la pantalla.

Las aplicaciones que necesitaban una alta precisión de color podrían consultar las funcionalidades de color de la pantalla (por ejemplo, mediante perfiles DE TASA) y realizar su propia administración de colores en proceso para dirigirse correctamente a la gama de colores de la pantalla. Sin embargo, la gran mayoría de las aplicaciones y el contenido visual asumen que la pantalla es sRGB y dependen del sistema operativo para cumplir esta suposición.

Windows el color avanzado agrega administración automática de colores de nivel de sistema. El Administrador de ventanas de escritorio (DWM) es Windows compositor. Cuando el color avanzado está habilitado, DWM realiza una conversión de color explícita del espacio de colores del contenido visual de la aplicación a un espacio de colores de composición canónica, que es scRGB. Windows a continuación, convierte el contenido del búfer de fotogramas compuesto en el espacio de color nativo de la pantalla. De esta manera, el contenido tradicional de sRGB obtiene automáticamente un comportamiento preciso del color, mientras que las aplicaciones avanzadas que conocen el color pueden aprovechar todas las funcionalidades de color de la pantalla.

### <a name="deep-precisionbit-depth"></a>Profundidad de precisión/profundidad de bits

La precisión numérica, o profundidad de bits, hace referencia a representar o distinguir entre colores similares pero distintos sin bandas ni artefactos. El equipo estándar muestra compatibilidad con 8 bits por canal de color, mientras que el ojo humano requiere al menos entre 10 y 12 bits de precisión para evitar distorsión perceptible, sin recurrir a técnicas como la dithering o en función de las condiciones de visualización.

![imagen de los proyectos de viento en un canal simulado de 2 bits por canal de color frente a 8 bits por canal](images/HDR-bitdepth.jpg)

Antes del color avanzado, las aplicaciones con ventanas restringidas de DWM solo generaban contenido de 8 bits por canal de color, incluso si la pantalla admite una profundidad de bits más alta. Cuando el color avanzado está habilitado, DWM realiza su composición mediante el punto flotante de precisión media IEEE (FP16), lo que elimina los cuellos de botella y permite usar la precisión completa de la pantalla.

## <a name="system-requirements"></a>Requisitos del sistema

### <a name="operating-system-os"></a>Sistema operativo (SO)

La compatibilidad de color avanzada se incluye Windows 10, versión 1703, y se ha mejorado significativamente con cada actualización. En este tema se supone que la aplicación tiene como destino Windows 10, versión 1903 o posterior.

### <a name="display"></a>Mostrar

Para aprovechar el alto rango dinámico, debe tener una pantalla que admita el estándar HDR10. Windows funciona mejor con pantallas que tienen la certificación [VESA DisplayHDR.](https://displayhdr.org/)

### <a name="graphics-processor-gpu"></a>Procesador de gráficos (GPU)

Se requiere una GPU reciente. Para admitir las pantallas DE HDR10, Windows 10 requiere una de las siguientes opciones.

* Serie Nvidia GeForce 1000 (Pascal) o posterior
* Serie AMD Radeon RX 400 (Ría) o posterior
* Serie Intel Core 7 seleccionada (Lake Deserción) o posterior

Tenga en cuenta que se aplican requisitos de hardware adicionales en función de los escenarios, incluida la aceleración de códecs de hardware (HEVC de 10 bits, VP9 de 10 bits, etc.) y la compatibilidad con PlayReady (SL3000). Póngase en contacto con el proveedor de GPU para obtener información más específica.

### <a name="graphics-driver-wddm"></a>Controlador de gráficos (WDDM)

Se recomienda encarecidamente el controlador de gráficos más reciente disponible, ya sea desde Windows Update o desde el sitio web del fabricante de GPU o del equipo. Por Windows 10, versión 1903 y posteriores, se recomiendan controladores que admitan al menos Windows Display Driver Model (WDDM) versión 2.6.

## <a name="supported-rendering-apis"></a>API de representación admitidas

Windows 10 admite una amplia variedad de plataformas y API de representación. La compatibilidad con colores avanzados se basa fundamentalmente en que la aplicación pueda realizar una presentación moderna mediante DXGI o las API de capa visual.

* [Infraestructura de gráficos de DirectX (DXGI)](../direct3ddxgi/dx-graphics-dxgi.md)
* [Capa visual (Windows.UI.Composition)](/windows/uwp/composition/visual-layer)

Por lo tanto, cualquier API de representación que pueda generarse en uno de estos métodos de presentaciones puede admitir el color avanzado. Esto incluye pero no se limita a estos.

* [Direct3D 11](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [Direct3D 12](../direct3d12/direct3d-12-graphics.md)
* [Direct2D](../direct2d/direct2d-portal.md)
* [Win2D](https://github.com/Microsoft/Win2D)
  * Requiere el uso de las API **CanvasSwapChain** o **CanvasSwapChainPanel de** nivel inferior.
* [**Windows.UI.Input.Inking**](/uwp/api/Windows.UI.Input.Inking)
  * Admite la representación personalizada de lápiz sin procesar mediante DirectX.
* [XAML](/windows/uwp/xaml-platform/)
  * Admite la reproducción de vídeos DE HDR **mediante MediaPlayerElement**.
  * Admite la descodificación de imágenes JPEG XR mediante **el elemento Image.**
  * Admite la interoperabilidad de DirectX **mediante SwapChainPanel**.

## <a name="handling-dynamic-display-capabilities"></a>Control de las funcionalidades de visualización dinámica

Windows 10 admite una gran variedad de pantallas avanzadas con capacidad de color, desde paneles integrados de bajo consumo hasta monitores y televisores de juegos de gama alta. Windows usuarios esperan que la aplicación controle sin problemas todas estas variaciones, incluidas las omnipresentes pantallas SDR existentes.

Windows 10 proporciona control sobre HDR y funcionalidades avanzadas de color al usuario. La aplicación debe detectar la configuración de la pantalla actual y responder dinámicamente a los cambios en la funcionalidad. Esto puede ocurrir por muchas razones, por ejemplo, porque el usuario habilitó o deshabilitó una característica, o movió la aplicación entre diferentes pantallas o el estado de energía del sistema cambió.

### <a name="universal-windows-platform-uwp-apps"></a>Aplicaciones de la Plataforma universal de Windows (UWP)

Si va a escribir una aplicación para UWP, independientemente de la API de representación de gráficos que use, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) para obtener funcionalidades de visualización. Obtenga una instancia de **AdvancedColorInfo** de [**DisplayInformation::GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).

Para comprobar qué tipo de color avanzado está activo actualmente, use la [**propiedad CurrentAdvancedColorKind.**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) En Windows 10, versión 1903 y posteriores, devuelve uno de los tres valores posibles: **SDR,** **WCG** o **HDR.** Esta es la propiedad más importante que se debe comprobar y debe configurar la canalización de presentación y representación en respuesta al tipo activo.

Para comprobar qué tipos de colores avanzados se admiten, pero no necesariamente activos, llame a [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable). Puede usar esta información, por ejemplo, para pedir al usuario que vaya a la aplicación Windows Configuración para que pueda habilitar HDR o WCG.

Los demás miembros de **AdvancedColorInfo** proporcionan información cuantitativa sobre el volumen de color físico del panel (luminosidad y chrominance), correspondiente a los metadatos estáticos de SMPTE ST.2086 DE HDR. Debe usar esta información para configurar la asignación de colores y de gamas de HDR de la aplicación.

Para controlar los cambios en las funcionalidades de color avanzadas, regístrese para el [**evento AdvancedColorInfoChanged.**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) Este evento se genera si cualquier parámetro de las funcionalidades de color avanzadas de la pantalla cambia por cualquier motivo.

Para controlar este evento, obtenga una nueva instancia de **AdvancedColorInfo** y comprueba qué valores han cambiado.

### <a name="desktop-win32-directx-apps"></a>Aplicaciones DirectX de escritorio (Win32)

Si va a escribir una aplicación Win32 y usa [](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) DirectX para representarla, use DXGI_OUTPUT_DESC1 para obtener funcionalidades de visualización. Obtenga una instancia de este struct a través [**de IDXGIOutput6::GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).

Para comprobar qué tipo de color avanzado está activo actualmente, use la propiedad **ColorSpace,** que es de tipo [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)y contiene uno de los valores siguientes:

* **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR
* **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR

> [!Note]
> DXGI trata otros tipos de colores avanzados, como WCG, como SDR. No se puede usar DXGI para identificar una pantalla wcg.

> [!Note]
> DXGI no permite comprobar qué tipos de colores avanzados se admiten pero no están activos en este momento.

La mayoría de los demás miembros de **DXGI_OUTPUT_DESC1** proporcionan información cuantitativa sobre el volumen de color físico del panel (luminosidad y chrominance), correspondiente a los metadatos estáticos de SMPTE ST.2086 DE HDR. Debe usar esta información para configurar la asignación de colores y de gamas de HDR de la aplicación.

Las aplicaciones Win32 no tienen un mecanismo nativo para responder a cambios avanzados de funcionalidad de color. En su lugar, si la aplicación usa un bucle de representación, debe consultar [**IDXGIFactory1::IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) con cada fotograma. Si notifica **FALSE**, debe obtener una nueva DXGI_OUTPUT_DESC1 **y** comprobar qué valores han cambiado.

Además, el bombeo de mensajes Win32 debe controlar el mensaje WM_SIZE, lo que indica que la aplicación puede haber cambiado entre diferentes pantallas. [](../winmsg/wm-size.md)

> [!Note]
> Para obtener un nuevo **DXGI_OUTPUT_DESC1**, debe obtener la presentación actual. Sin embargo, no debe llamar a **IDXGISwapChain::GetContainingOutput**. Esto se debe a que las cadenas de intercambio devolverán una salida DXGI obsoleta una vez **que DXGIFactory::IsCurrent** sea false y volver a crear la cadena de intercambio para obtener una salida actual da como resultado una pantalla negra temporal. En su lugar, se recomienda enumerar a través de los límites de todas las salidas DXGI y determinar cuál tiene la mayor intersección con los límites de la ventana de la aplicación.

El ejemplo de código siguiente procede del [repositorio DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).

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

## <a name="setting-up-your-directx-swap-chain"></a>Configuración de la cadena de intercambio de DirectX

Una vez que haya determinado que la pantalla admite actualmente funcionalidades de color avanzadas, configure la cadena de intercambio como se muestra a continuación.

### <a name="use-a-flip-presentation-model-effect"></a>Uso de un efecto de modelo de presentación de volteo

Al crear la cadena de intercambio mediante **CreateSwapChainFor[Hwnd| Composición| CoreWindow]** Métodos, debe usar el modelo de volteo DXGI seleccionando la opción **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** o **DXGI_SWAP_EFFECT_FLIP_DISCARD,** lo que hace que la cadena de intercambio sea apta para el procesamiento de color avanzado de DWM y varias optimizaciones de pantalla completa. Para obtener más información, consulte el [tema For best performance, use DXGI flip model (Para](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) obtener el mejor rendimiento, use DXGI flip model).

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a>Opción 1. Uso del formato de píxel FP16 y el espacio de colores scRGB

Windows 10 admite dos combinaciones principales de formato de píxel y espacio de color para el color avanzado. Seleccione uno en función de los requisitos específicos de la aplicación.

En el caso de las aplicaciones de uso general, al crear la cadena de intercambio, se recomienda especificar [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Esto también se conoce como *FP16* en la [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). De forma predeterminada, una cadena de intercambio creada con un formato de píxel de punto flotante se trata como si usara el espacio [**de**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) color DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709, que también se conoce como *scRGB.*

Esta combinación proporciona el intervalo numérico y la precisión para especificar casi cualquier color físicamente posible y realizar un procesamiento arbitrario, incluida la combinación. Además, si usa Direct2D, Win2D o Windows.UI.Composition, esta es la única combinación admitida para cualquier cadena de intercambio o destino intermedio que contenga contenido de color avanzado. 

La principal diferencia de esta opción es que consume 64 bits por píxel, lo que duplica el ancho de banda de GPU y el consumo de memoria en comparación con los formatos de píxeles SDR de UINT8 tradicionales. Además, scRGB usa valores numéricos que están fuera del intervalo normalizado [0, 1] para representar colores que están fuera de la gama sRGB o superiores a 80 nits de luminosidad. Por ejemplo, scRGB (1.0, 1.0, 1.0) codifica el estándar D65 blanco a 80 nits; pero scRGB (12.5, 12.5, 12.5) codifica el mismo D65 blanco a una velocidad de 1000 nits mucho más brillante. Algunas operaciones de gráficos requieren un intervalo numérico normalizado y debe modificar la operación o volver a normalizar los valores de color.

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a>Opción 2: Usar el formato de píxel UINT10/RGB10 y el espacio de colores HDR10/BT.2100

En el caso de las aplicaciones que consumen contenido codificado con HDR10, como reproductores multimedia o aplicaciones que se espera que se utilicen principalmente en escenarios de pantalla completa como juegos, al crear la cadena de intercambio, debe considerar la posibilidad de especificar [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) en [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). De forma predeterminada, esto se trata como si usara el espacio de colores sRGB; Por lo tanto, debe llamar explícitamente a [**IDXGISwapChain3::SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)y establecer como espacio de color [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), también conocido como HDR10/BT.2100.

Esta combinación tiene restricciones más estrictas que FP16. Solo puede usarlo con Direct3D 11 o Direct3D 12. Además, UINT10/HDR10 tiene limitaciones como formato intermedio porque usa la función ST.2084 EOTF ("gamma"), que es altamente no lineal y está optimizada como formato de conexión, y porque solo ofrece 2 bits de alfa.

Sin embargo, esta combinación puede ofrecer eficaces optimizaciones de rendimiento cuando se usa en la salida final de la aplicación. Consume los mismos 32 bits por píxel que los formatos de píxel SDR de UINT8 tradicionales. Además, en determinados escenarios de pantalla completa, el sistema operativo puede optimizar el rendimiento analizando directamente la superficie de HDR10.

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a>Uso de una cadena de intercambio de colores avanzada cuando la pantalla está en modo SDR

Puede usar una cadena de intercambio de colores avanzada incluso si la pantalla no admite algunas o todas las funcionalidades de color avanzadas que requiere el contenido. En esos casos, el Administrador de ventanas de escritorio (DWM) revierte el contenido para ajustarlo a las funcionalidades de la pantalla. En Windows 10, versión 1903 y posteriores, realizará un recorte numérico; Por ejemplo, si se representa en una cadena de intercambio fp16 scRGB, se recorta todo lo que está fuera del intervalo numérico [0, 1].

Este comportamiento de inversión a la baja también se producirá si la ventana de la aplicación está desasoyendo dos o más pantallas con distintas funcionalidades de color avanzadas. **AdvancedColorInfo** e **IDXGIOutput6** se abstraen para notificar solo las características de la pantalla "principal" (definida como la pantalla que contiene el centro de la ventana).

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a>Representación correcta del contenido de SDR con el nivel de blanco de referencia de SDR

En muchos escenarios, la aplicación querrá representar contenido SDR y HDR. por ejemplo, la representación de subtítulos o controles de transporte a través de vídeo o interfaz de usuario de HDR en una escena de juego. Es importante comprender el concepto de nivel de blanco de referencia *de SDR* para asegurarse de que el contenido de SDR tiene un aspecto correcto en una pantalla de HDR.

Windows el contenido de HDR como al que se hace referencia a la _escena,_ lo que significa que un valor de color determinado debe mostrarse en un nivel de luminosidad específico; por ejemplo, scRGB (1.0, 1.0, 1.0) y HDR10 (497, 497, 497) codifican exactamente D65 blanco a 80 nits de luminosidad. Mientras tanto, el contenido de SDR tradicionalmente se ha hecho referencia a la salida _(o_ se hace referencia a la pantalla), lo que significa que su luminosidad se deja al usuario o al dispositivo. Por ejemplo, sRGB (1.0, 1.0, 1.0) codifica D65 en blanco como en los ejemplos de HDR, pero en cualquier luminosidad máxima para la que esté configurada la pantalla. Windows permite al usuario ajustar el nivel de blanco de referencia _de SDR a_ sus preferencias; esta es la luminosidad que Windows representará sRGB (1.0, 1.0, 1.0) en . En los monitores HDR de escritorio, los niveles de blanco de referencia de SDR suelen establecerse en aproximadamente 200 nits.

> [!Note]
> En una pantalla que admite un control de brillo, como en un portátil, Windows también ajustará la luminosidad del contenido de HDR (referencia a la escena) para que coincida con el nivel de brillo deseado del usuario, pero esto es invisible para la aplicación. A menos que esté intentando garantizar la reproducción bit-precisa de la señal HDR, generalmente puede omitir esto.

Si la aplicación siempre representa SDR y HDR en superficies independientes y se basa en la composición del sistema operativo, Windows realizará automáticamente el ajuste correcto para aumentar el contenido SDR al nivel de blanco deseado. Por ejemplo, si la aplicación usa XAML y representa contenido DE HDR en su propio **SwapChainPanel**.

Sin embargo, si la aplicación realiza su propia composición de contenido SDR y HDR en una sola superficie, usted es responsable de realizar el ajuste de nivel de blanco de referencia de SDR usted mismo. De lo contrario, el contenido de SDR podría parecer demasiado tenue suponiendo condiciones de visualización de escritorio típicas. En primer lugar, debe obtener el nivel de blanco de referencia SDR actual y, a continuación, debe ajustar los valores de color de cualquier contenido de SDR que se va a representar.

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a>Paso 1. Obtener el nivel de blanco de referencia de SDR actual

Actualmente, solo las aplicaciones para UWP pueden obtener el nivel de blanco de referencia de SDR actual a través [**de AdvancedColorInfo.SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits). Esta API requiere una [**instancia de CoreWindow.**](/uwp/api/Windows.UI.Core.CoreWindow)

### <a name="step-2-adjust-color-values-of-sdr-content"></a>Paso 2. Ajuste de los valores de color del contenido de SDR

Windows define el nivel de blanco de referencia nominal o predeterminado en 80 nits; por lo tanto, si representara un sRGB estándar (1.0, 1.0, 1.0) en blanco en una cadena de intercambio FP16, se reproduciría a 80 nits de luminosidad. Para que coincida con el nivel blanco de referencia real definido por el usuario, debe ajustar el contenido de SDR de 80 nits al nivel especificado a través de **AdvancedColorInfo.SdrWhiteLevelInNits**.

Si va a representar mediante FP16 y scRGB, o cualquier espacio de color que use gamma lineal (1,0), simplemente puede multiplicar el valor de color de SDR por _AdvancedColorInfo.SdrWhiteLevelInNits_  /  _80._ Si usa Direct2D, hay una constante [**predefinida D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), que tiene un valor de 80.

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

Si va a representar con un espacio de color gamma no lineal como HDR10, es más complejo realizar el ajuste de nivel de blanco de SDR. si está escribiendo su propio sombreador de píxeles, debe considerar la posibilidad de convertir en gamma lineal para aplicar el ajuste.

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a>Adaptación del contenido de HDR a las funcionalidades de la pantalla mediante la combinación de tono

Las pantallas de color avanzado y HDR varían considerablemente en términos de sus capacidades. Por ejemplo, la luminosidad mínima y máxima y la gama de colores que son capaces de reproducir. En muchos casos, el contenido de HDR contendrá colores que superan las funcionalidades de la pantalla. Para obtener la mejor calidad de imagen, es importante realizar el ajuste de tono DE HDR, comprimiendo básicamente el intervalo de colores para ajustarse a la pantalla, a la vez que se conserva mejor la intención visual del contenido.

El parámetro único más importante para adaptarse es la luminosidad máxima, también conocida como MaxCLL (nivel de luz de contenido); Los tonemappers más sofisticados también adaptarán la luminosidad mínima (MinCLL) o las primarias de color.

### <a name="step-1-get-the-displays-color-volume-capabilities"></a>Paso 1. Obtener las funcionalidades de volumen de color de la pantalla

#### <a name="universal-windows-platform-uwp-apps"></a>Aplicaciones de la Plataforma universal de Windows (UWP)

Use [**AdvancedColorInfo para**](/uwp/api/windows.graphics.display.advancedcolorinfo) obtener el volumen de color de la pantalla.

#### <a name="win32-desktop-directx-apps"></a>Aplicaciones DirectX win32 (escritorio)

Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) para obtener el volumen de color de la pantalla.

### <a name="step-2-get-the-contents-color-volume-information"></a>Paso 2. Obtener la información del volumen de color del contenido

Dependiendo de dónde provenía el contenido de HDR, hay varias maneras posibles de determinar su información de luminosidad y gama de colores. Algunos archivos de imagen y vídeo DE HDR contienen metadatos SMPTE ST.2086. Si el contenido se representó dinámicamente, es posible que pueda extraer información de la escena de las fases de representación internas, por ejemplo, la fuente de luz más brillante de una escena.

Una solución más general pero costosa computacionalmente es ejecutar un histograma u otro paso de análisis en el marco representado. En [el ejemplo del SDK de imágenes de color avanzadas de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) se muestra cómo hacerlo mediante Direct2D. a continuación se incluyen los fragmentos de código más relevantes:

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

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a>Paso 3. Realización de la operación de combinación de tono de HDR

La optimización de tono es inherentemente un proceso con pérdida y se puede optimizar para una serie de métricas perceptuales u objetivo, por lo que no hay ningún algoritmo estándar. Windows proporciona un efecto [tonemapper de HDR](../direct2d/hdr-tone-map-effect.md) integrado como parte de Direct2D, así como en la canalización de reproducción de vídeo de Media Foundation HDR. Algunos otros algoritmos usados habitualmente incluyen ACES Películasic, Reinhard e ITU-R BT.2390-3 EETF (función de transferencia eléctrica).

A continuación se muestra un operador de tonemapper Reinhard simplificado.

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

## <a name="capturing-hdr-and-wcg-content"></a>Captura de contenido de HDR y WCG

API que admiten la especificación de formatos de píxel, como los del [**Windows. El**](/uwp/api/windows.graphics.capture) espacio de nombres Graphics.Capture y el método [**IDXGIOutput5::D uplicateOutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) proporcionan la capacidad de capturar contenido DE HDR y WCG sin perder información de píxeles. Tenga en cuenta que después de adquirir fotogramas de contenido, se requiere un procesamiento adicional. Por ejemplo, la asignación de tono de HDR a SDR (por ejemplo, la copia de captura de pantalla de SDR para el uso compartido de Internet) y el guardado de contenido con el formato adecuado (por ejemplo, JPEG XR).

## <a name="additional-resources"></a>Recursos adicionales

* *Usar la representación de HDR con el Kit de herramientas de DirectX* [para DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12.](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering) Tutorial sobre cómo agregar compatibilidad con HDR a una aplicación DirectX mediante el Kit de herramientas de DirectX (DirectXTK).
* [Ejemplo de SDK de imágenes de color avanzadas de Direct2D.](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) Ejemplo del SDK de UWP que implementa un visor avanzado de imágenes DE HDR y WCG con compatibilidad con colores con Direct2D. Muestra toda la gama de procedimientos recomendados para aplicaciones para UWP, incluida la respuesta a los cambios de funcionalidad de visualización y el ajuste para el nivel blanco de SDR.
* [Ejemplo de escritorio DE DIRECT3D 12 HDR](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR). Ejemplo de SDK de escritorio que implementa una escena básica de Direct3D 12 HDR.
* [Ejemplo de UWP de Direct3D 12 HDR](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR). Equivalente de UWP del ejemplo anterior.
* [Ejemplo de PC SimpleHDR de Xbox ATG](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC). Ejemplo de SDK de escritorio que implementa una escena básica de Direct3D 11 HDR.

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
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a>Usar DirectX con altas pantallas de rango dinámico y color avanzado

En este tema se proporciona información general técnica sobre la salida de contenido de Direct3D 11 y Direct3D 12 de rango dinámico alto (HDR) a una pantalla de HDR10 con compatibilidad con el color avanzado de Windows 10. Resume algunas diferencias conceptuales clave entre la salida a las pantallas de HDR10 en comparación con las pantallas del intervalo dinámico estándar tradicional (SDR). También se tratan los requisitos técnicos clave de la aplicación para admitir correctamente el color avanzado de Windows, así como recomendaciones y prácticas recomendadas.

## <a name="introduction"></a>Introducción

Windows 10 admite HDR y otras pantallas de color avanzadas, que proporcionan una fidelidad de color significativamente mayor que las pantallas de SDR tradicionales. Puede usar Direct3D, Direct2D y otras API de gráficos para representar el contenido HDR en una visualización compatible.

Windows Advanced color hace referencia a varias tecnologías relacionadas, introducidas por primera vez con la versión 1703 de Windows 10, que proporcionan compatibilidad con las pantallas que superan las capacidades de color de las pantallas tradicionales de rango dinámico estándar (SDR). A continuación se describen las tres principales capacidades extendidas. El tipo más común de presentación de color avanzada, HDR10, admite las tres capacidades extendidas.

### <a name="high-dynamic-range"></a>Alto rango dinámico

El intervalo dinámico hace referencia a la diferencia entre la luminancia máxima y mínima de una escena. a menudo se mide en nits (candelas por centímetro cuadrado). Las escenas del mundo real, como este atardecer, a menudo tienen intervalos dinámicos de 10 pedidos de magnitud de luminancia; el ojo humano puede discernir un rango incluso mayor después de la adaptación.

![imagen de una puesta de sol con brillo y puntos más oscuros de la escena etiquetada](images/HDR-HDR.jpg)

Desde Direct3D 9, los motores de gráficos han podido representar internamente sus escenas con este nivel de fidelidad físicamente precisa. Sin embargo, una pantalla de intervalo dinámico estándar típica solo puede reproducir un poco más de 3 órdenes de magnitud de luminancia y, por lo tanto, cualquier contenido representado por HDR debe ser tonemapped (comprimido) en el intervalo limitado de la pantalla. En las nuevas pantallas HDR, incluidas las que cumplen con el estándar HDR10 (BT. 2100), se interrumpe esta limitación.

### <a name="wide-color-gamut-with-automatic-system-color-management"></a>Gama de colores anchos con administración automática del color del sistema

La gama de colores hace referencia al intervalo y la saturación de los matices que puede reproducir una pantalla. El color natural más saturado que el ojo humano puede percibir es puro, luz monocromática, como lo que genera un láser. Sin embargo, las pantallas de consumidor estándar a menudo pueden reproducir colores solo dentro de la gama sRGB, que solo representa aproximadamente el 35% de todos los colores que perciben los usuarios. El diagrama siguiente es una representación del "raíz espectral" humano o de todos los colores perceptibles (en un nivel de luminancia determinado), donde el triángulo más pequeño es la gama sRGB.

![diagrama de la gama raíz y sRGB humana](images/HDR-WCG.jpg)

En el extremo superior, las pantallas de PC profesionales tienen gamas de colores que son mucho más grandes que sRGB, como Adobe RGB y D65-P3. Y estas pantallas de gama ancha son cada vez más comunes. Sin embargo, antes del color avanzado, Windows no realizaba ninguna administración de color de nivel de sistema para las aplicaciones. Esto significaba que si una aplicación de DirectX se representara, por ejemplo, un rojo o RGB puro (1.0, 0,0, 0,0) a su cadena de intercambio, Windows simplemente escanearía el rojo más saturado que podía reproducir la pantalla, independientemente de cuál sea la gama de colores real de la pantalla.

Las aplicaciones que necesitan una precisión de color alta podrían consultar las capacidades de color de la pantalla (por ejemplo, mediante perfiles de ICC) y realizar su propia administración de color en proceso para dirigirse correctamente a la gama de colores de la pantalla. Sin embargo, la gran mayoría de las aplicaciones y el contenido visual suponen que la pantalla es sRGB y que dependen del sistema operativo para cumplir esta suposición.

Windows Advanced color agrega administración automática del color de nivel de sistema. El Administrador de ventanas de escritorio (DWM) es el compositor de Windows. Cuando se habilita el color avanzado, DWM realiza una conversión de color explícita desde el ColorSpace del contenido visual de la aplicación a un espacio de colores de composición canónico, que es scRGB. A continuación, Windows convierte el contenido de fotogramas compuesto en el espacio de colores nativo de la pantalla. De esta manera, el contenido sRGB tradicional obtiene automáticamente un comportamiento con precisión del color, mientras que las aplicaciones avanzadas para el color pueden aprovechar las capacidades de color completo de la pantalla.

### <a name="deep-precisionbit-depth"></a>Profundidad de profundidad y profundidad de bits

La precisión numérica, o la profundidad de bits, se refiere a representar o distinguir entre colores similares pero distintos sin bandas ni artefactos. El equipo estándar muestra la compatibilidad con 8 bits por canal de color, mientras que el ojo humano requiere al menos 10-12 bits de precisión para evitar distorsiones perceptibles, sin tener que recurrir a técnicas como el tramado o en función de las condiciones de visualización.

![imagen de Windmills en una simulación de 2 bits por canal de color frente a 8 bits por canal](images/HDR-bitdepth.jpg)

Antes del color avanzado, las aplicaciones con ventana restringida de DWM solo envían contenido a 8 bits por canal de color, aunque la pantalla admita una profundidad de bits más alta. Cuando se habilita el color avanzado, el DWM realiza su composición mediante el punto flotante de media precisión IEEE (FP16), lo que elimina los cuellos de botella y permite que se use la precisión completa de la pantalla.

## <a name="system-requirements"></a>Requisitos del sistema

### <a name="operating-system-os"></a>Sistema operativo (SO)

La compatibilidad con el color avanzado se incluyó por primera vez con Windows 10, versión 1703, y se ha mejorado significativamente con cada actualización. En este tema se da por supuesto que la aplicación está dirigida a Windows 10, versión 1903 o posterior.

### <a name="display"></a>Pantalla

Para aprovechar el alto rango dinámico, debe tener una pantalla que admita el estándar HDR10. Windows funciona mejor con las pantallas que tienen la [certificación VESA DisplayHDR](https://displayhdr.org/).

### <a name="graphics-processor-gpu"></a>Procesador de gráficos (GPU)

Se requiere una GPU reciente. Para admitir pantallas de HDR10, Windows 10 requiere una de las siguientes opciones.

* NVIDIA GeForce 1000 series (Pascal) o posterior
* AMD Radeon serie 400 (Polaris) o versiones más recientes
* Serie de Intel Core 7 seleccionada (Kaby Lake) o posterior

Tenga en cuenta que se aplican requisitos de hardware adicionales en función de los escenarios, incluida la aceleración de códecs de hardware (HEVC de 10 bits, VP9 de 10 bits, etc.) y la compatibilidad con PlayReady (SL3000). Póngase en contacto con su proveedor de GPU para obtener información más específica.

### <a name="graphics-driver-wddm"></a>Controlador de gráficos (WDDM)

Se recomienda encarecidamente el controlador de gráficos más reciente disponible, ya sea desde Windows Update o desde el sitio web del fabricante de la GPU o del equipo. En Windows 10, versión 1903 y versiones posteriores, se recomiendan controladores que admitan como mínimo Windows Display Driver Model (WDDM), versión 2,6.

## <a name="supported-rendering-apis"></a>API de representación compatibles

Windows 10 admite una amplia variedad de plataformas y API de representación. En esencia, la compatibilidad con colores avanzada se basa en la aplicación para realizar una presentación moderna con las API de nivel visual o DXGI.

* [Infraestructura de gráficos de DirectX (DXGI)](../direct3ddxgi/dx-graphics-dxgi.md)
* [Capa visual (Windows. UI. Composition)](/windows/uwp/composition/visual-layer)

Por lo tanto, todas las API de representación que pueden generar resultados en uno de estos métodos de presentación pueden admitir el color avanzado. Esto incluye pero no se limita a ello.

* [Direct3D 11](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [Direct3D 12](../direct3d12/direct3d-12-graphics.md)
* [Direct2D](../direct2d/direct2d-portal.md)
* [Win2D](https://github.com/Microsoft/Win2D)
  * Requiere el uso de las API de **CanvasSwapChain** o **CanvasSwapChainPanel** de nivel inferior.
* [**Windows.UI.Input.Inking**](/uwp/api/Windows.UI.Input.Inking)
  * Admite la representación de tinta seca personalizada mediante DirectX.
* [XAML](/windows/uwp/xaml-platform/)
  * Admite la reproducción de vídeos HDR mediante **MediaPlayerElement**.
  * Admite el descodificación de imágenes JPEG XR mediante el elemento de **imagen** .
  * Admite la interoperabilidad de DirectX mediante **SwapChainPanel**.

## <a name="handling-dynamic-display-capabilities"></a>Controlar las capacidades de visualización dinámica

Windows 10 es compatible con una amplia gama de pantallas avanzadas de uso de color, desde paneles integrados con eficacia energética hasta monitores y televisores de juegos de gama alta. Los usuarios de Windows esperan que la aplicación controle sin problemas todas estas variaciones, incluidas las pantallas de SDR existentes.

Windows 10 proporciona control sobre las funcionalidades de color avanzado y HDR al usuario. La aplicación debe detectar la configuración de la pantalla actual y responder dinámicamente a cualquier cambio en la capacidad. Esto puede ocurrir por muchas razones, por ejemplo, porque el usuario ha habilitado o deshabilitado una característica, o ha desplazado la aplicación entre distintas pantallas o ha cambiado el estado de energía del sistema.

### <a name="universal-windows-platform-uwp-apps"></a>Aplicaciones de la Plataforma universal de Windows (UWP)

Si va a escribir una aplicación para UWP, independientemente de la API de representación de gráficos que esté usando, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) para obtener funcionalidades de visualización. Obtenga una instancia de **AdvancedColorInfo** de [**DisplayInformation:: GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).

Para comprobar qué tipo de color avanzado está activo actualmente, use la propiedad [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) . En Windows 10, versión 1903 y versiones posteriores, devuelve uno de los tres valores posibles: **SDR**, **WCG** o **HDR**. Esta es la propiedad más importante que se va a comprobar y debe configurar la canalización de representación y presentación en respuesta a la clase activa.

Para comprobar qué tipos de color avanzado se admiten, pero no necesariamente activos, llame a [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable). Puede usar esta información, por ejemplo, para solicitar al usuario que vaya a la aplicación de configuración de Windows para que pueda habilitar HDR o WCG.

Los demás miembros de **AdvancedColorInfo** proporcionan información cuantitativa sobre el volumen de color físico del panel (luminancia y crominancia), que corresponde a los metadatos de HDR estáticos de SMPTE St. 2086. Debe usar esta información para configurar la asignación de gama y tonemapping HDR de la aplicación.

Para controlar los cambios en las capacidades de color avanzadas, Regístrese para el evento [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) . Este evento se desencadena si algún parámetro de las funciones de color avanzadas de la pantalla cambia por cualquier motivo.

Controle este evento mediante la obtención de una nueva instancia de **AdvancedColorInfo** y la comprobación de los valores que han cambiado.

### <a name="desktop-win32-directx-apps"></a>Aplicaciones DirectX de escritorio (Win32)

Si está escribiendo una aplicación de Win32 y usa DirectX para representar, use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) para obtener funcionalidades de visualización. Obtenga una instancia de este struct a través de [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).

Para comprobar qué tipo de color avanzado está activo actualmente, use la propiedad **ColorSpace** , que es de tipo [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), y contiene uno de los valores siguientes:

* **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR
* **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR

> [!Note]
> Otros tipos de color avanzados, como WCG, se tratan como SDR por DXGI. No se puede usar DXGI para identificar una presentación de WCG.

> [!Note]
> DXGI no permite comprobar qué tipos de color avanzado se admiten, pero no activos en este momento.

La mayoría de los demás miembros de **DXGI_OUTPUT_DESC1** proporcionan información cuantitativa sobre el volumen de color físico del panel (luminancia y crominancia), que corresponde a los metadatos de HDR estáticos de SMPTE St. 2086. Debe usar esta información para configurar la asignación de gama y tonemapping HDR de la aplicación.

Las aplicaciones Win32 no tienen un mecanismo nativo para responder a los cambios en la funcionalidad de color avanzada. En su lugar, si la aplicación usa un bucle de representación, debe consultar [**IDXGIFactory1:: IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) con cada fotograma. Si informa de **false**, debe obtener un nuevo **DXGI_OUTPUT_DESC1** y comprobar los valores que han cambiado.

Además, el bombeo de mensajes de Win32 debe controlar el mensaje de [**WM_SIZE**](../winmsg/wm-size.md) , lo que indica que la aplicación puede haberse desplazado entre distintas pantallas.

> [!Note]
> Para obtener una nueva **DXGI_OUTPUT_DESC1**, debe obtener la pantalla actual. Sin embargo, no debe llamar a **IDXGISwapChain:: GetContainingOutput**. Esto se debe a que las cadenas de intercambio devolverán una salida de DXGI obsoleta una vez que **DXGIFactory:: IsCurrent** es false y volver a crear la cadena de intercambio para obtener una salida actual genera una pantalla negra temporal. En su lugar, se recomienda enumerar los límites de todas las salidas de DXGI y determinar cuál de ellas tiene la mayor intersección con los límites de la ventana de la aplicación.

El siguiente ejemplo de código procede del [repositorio DirectX-Graphics-samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).

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

Una vez que haya determinado que la pantalla admite actualmente capacidades de color avanzadas, configure la cadena de intercambio como se indica a continuación.

### <a name="use-a-flip-presentation-model-effect"></a>Usar un efecto de modelo de presentación Flip

Al crear la cadena de intercambio mediante **CreateSwapChainFor [HWND | Composición |** Los métodos de CoreWindow], debe usar el modelo de volteo de DXGI seleccionando la opción **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** o **DXGI_SWAP_EFFECT_FLIP_DISCARD** , que hace que la cadena de intercambio sea válida para el procesamiento de color avanzado de DWM y varias optimizaciones de pantalla completa. Para obtener más información, consulte el tema para obtener el [mejor rendimiento, use DXGI Flip Model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a>Opción 1. Usar el formato de píxel de FP16 y el espacio de colores scRGB

Windows 10 admite dos combinaciones principales de formato de píxeles y espacio de colores para el color avanzado. Seleccione una en función de los requisitos específicos de su aplicación.

En el caso de las aplicaciones de uso general, al crear la cadena de intercambio, se recomienda especificar [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Esto también se conoce como *FP16* en el [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). De forma predeterminada, una cadena de intercambio creada con un formato de píxel de punto flotante se trata como si usara el espacio de colores [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) , que también se conoce como *ScRGB*.

Esta combinación proporciona el intervalo numérico y la precisión para especificar casi cualquier color físicamente posible y realizar un procesamiento arbitrario que incluye la combinación. Además, si está usando Direct2D, Win2D o Windows. UI. Composition, esta es la única combinación admitida para cualquier cadena de intercambio o destino intermedio que contenga contenido de color avanzado. 

La principal desventaja de esta opción es que consume 64 bits por píxel, que duplica el ancho de banda de la GPU y el consumo de memoria en comparación con los formatos del píxel de SDR de UINT8 tradicionales. Además, scRGB usa valores numéricos que están fuera del intervalo normalizado [0, 1] para representar colores que están fuera de la gama de sRGB y/o superior a 80 Nits de luminancia. Por ejemplo, scRGB (1,0, 1,0, 1,0) codifica el blanco D65 estándar en 80 Nits; sin embargo, scRGB (12,5, 12,5, 12,5) codifica el mismo blanco de D65 en unos 1000 Nits. Algunas operaciones de gráficos requieren un intervalo numérico normalizado y debe modificar la operación o volver a normalizar los valores de color.

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a>Opción 2: usar el formato de píxel UINT10/RGB10 y el espacio de colores HDR10/BT. 2100

En el caso de las aplicaciones que consumen contenido codificado en HDR10, como reproductores multimedia o aplicaciones que se espera que se usen principalmente en escenarios de pantalla completa, como juegos, al crear la cadena de intercambio, debería considerar la posibilidad de especificar [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) en [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). De forma predeterminada, esto se trata como si se usara el espacio de color sRGB; por lo tanto, debe llamar explícitamente a [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)y establecer como espacio de colores [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), también conocido como HDR10/BT. 2100.

Esta combinación tiene restricciones más rigurosas que FP16. Solo se puede usar con Direct3D 11 o Direct3D 12. Además, UINT10/HDR10 tiene limitaciones como un formato intermedio porque usa la función ST. 2084 EOTF ("gamma"), que es muy no lineal y está optimizada como un formato de conexión, y porque solo ofrece 2 bits de alfa.

Sin embargo, esta combinación puede ofrecer optimizaciones de rendimiento eficaces cuando se usa en la salida final de la aplicación. Consume los mismos 32 bits por píxel que los formatos tradicionales de inglés UINT8 SDR. Además, en ciertos escenarios de pantalla completa, el sistema operativo puede optimizar el rendimiento mediante el análisis directo de la superficie HDR10.

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a>Usar una cadena de intercambio de color avanzada cuando la pantalla está en modo SDR

Puede usar una cadena de intercambio de color avanzada incluso si la pantalla no es compatible con algunas o todas las funciones de color avanzadas que requiere el contenido. En estos casos, el Administrador de ventanas de escritorio (DWM) downconvert el contenido para ajustarse a las capacidades de la pantalla. En Windows 10, versión 1903 y versiones posteriores, realizará el recorte numérico; por ejemplo, si se representa en una cadena de intercambio de FP16 scRGB, se recorta todo lo que se encuentra fuera del intervalo numérico [0, 1].

Este comportamiento de downconversion también se producirá si la ventana de la aplicación abarca dos o más pantallas con distintas capacidades de color avanzadas. **AdvancedColorInfo** y **IDXGIOutput6** se abstraen para informar únicamente de las características de la presentación "principal" (definidas como la pantalla que contiene el centro de la ventana).

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a>Representar correctamente el contenido de SDR con el nivel blanco de referencia de SDR

En muchos escenarios, la aplicación querrá representar el contenido de SDR y HDR; por ejemplo, la representación de subtítulos o controles de transporte sobre el vídeo HDR o la interfaz de usuario en una escena de juego. Es importante comprender el concepto de *nivel blanco de referencia de SDR* para asegurarse de que el contenido de SDR tiene un aspecto correcto en una pantalla HDR.

Windows trata el contenido de HDR como _referencia de la escena_, lo que significa que un valor de color determinado se debe mostrar en un nivel de luminancia específico; por ejemplo, scRGB (1,0, 1,0, 1,0) y HDR10 (497, 497, 497) codifican exactamente el blanco D65 en la luminancia de 80 Nits. Mientras tanto, el contenido de SDR tradicionalmente se ha _remitido_ (o se ha remitido a la presentación), lo que significa que su luminancia se deja al usuario o al dispositivo. por ejemplo sRGB (1,0, 1,0, 1,0) codifica el blanco D65 como en los ejemplos de HDR, pero con la luminancia máxima para la que esté configurada la pantalla. Windows permite al usuario ajustar el _nivel blanco de referencia de SDR_ a sus preferencias; Esta es la luminancia que Windows representará sRGB (1,0, 1,0, 1,0) en. En los monitores de encabezado de los equipos de escritorio, los niveles blancos de referencia de SDR normalmente se establecen en unos 200 Nits.

> [!Note]
> En una pantalla que admita un control de brillo, como en un equipo portátil, Windows también ajustará la luminancia del contenido HDR (con referencia a la escena) para que coincida con el nivel de brillo deseado del usuario, pero esto es invisible para la aplicación. A menos que esté intentando garantizar la reproducción de la señal HDR con precisión de bits, por lo general puede pasarlo por alto.

Si la aplicación siempre representa SDR y HDR para separar superficies y se basa en la composición del sistema operativo, Windows realizará automáticamente el ajuste correcto para aumentar el contenido de SDR al nivel de blanco deseado. Por ejemplo, si la aplicación usa XAML y representa el contenido HDR en su propio **SwapChainPanel**.

Sin embargo, si la aplicación realiza su propia composición de contenido de SDR y HDR en una sola superficie, es el responsable de realizar el ajuste de nivel blanco de referencia de SDR usted mismo. En caso contrario, es posible que el contenido de SDR parezca demasiado tenue suponiendo condiciones típicas de visualización del escritorio. En primer lugar, debe obtener el nivel de documento de referencia de SDR actual y, después, debe ajustar los valores de color de cualquier contenido de SDR que esté representando.

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a>Paso 1. Obtención del nivel blanco actual de referencia de SDR

Actualmente, solo las aplicaciones UWP pueden obtener el nivel de blanco de referencia de SDR actual a través de [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits). Esta API requiere un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

### <a name="step-2-adjust-color-values-of-sdr-content"></a>Paso 2. Ajustar los valores de color del contenido de SDR

Windows define el nivel blanco nominal o predeterminado de referencia en 80 Nits; por lo tanto, si tuviera que representar un blanco estándar sRGB (1,0, 1,0, 1,0) en una cadena de intercambio de FP16, se volvería a producir con una luminancia de 80 Nits. Para que coincida con el nivel de blanco de referencia definido por el usuario real, debe ajustar el contenido de SDR desde 80 Nits hasta el nivel especificado a través de **AdvancedColorInfo. SdrWhiteLevelInNits**.

Si va a representar con FP16 y ScRGB, o cualquier espacio de colores que use gamma lineal (1,0), puede multiplicar el valor de color de SDR por _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_. Si utiliza Direct2D, hay una constante predefinida [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), que tiene un valor de 80.

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

Si está representando mediante un espacio de colores de gamma no lineal como HDR10, la realización del ajuste de nivel blanco de SDR es más compleja. Si está escribiendo su propio sombreador de píxeles, considere la posibilidad de convertir en gamma lineal para aplicar el ajuste.

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a>Adaptación del contenido de HDR a las capacidades de la pantalla mediante tonemapping

Las pantallas de color avanzado y HDR varían en gran medida en función de sus capacidades. Por ejemplo, la luminancia mínima y máxima y la gama de colores son capaces de reproducir. En muchos casos, el contenido de HDR contendrá colores que superan las capacidades de la pantalla. Para obtener la mejor calidad de imagen, es importante que realice tonemappings HDR, con lo que comprime en esencia el intervalo de colores para ajustarse a la pantalla, al mismo tiempo que se conserva la intención visual del contenido.

El parámetro único más importante para adaptarse es la luminancia máxima, también conocido como MaxCLL (nivel de luz de contenido); los tonemappers más sofisticados también adaptarán la luminancia mínima (MinCLL) y/o los primarios de color.

### <a name="step-1-get-the-displays-color-volume-capabilities"></a>Paso 1. Obtención de las capacidades de volumen de color de la pantalla

#### <a name="universal-windows-platform-uwp-apps"></a>Aplicaciones de la Plataforma universal de Windows (UWP)

Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) para obtener el volumen de color de la pantalla.

#### <a name="win32-desktop-directx-apps"></a>Win32 (escritorio) aplicaciones DirectX

Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) para obtener el volumen de color de la pantalla.

### <a name="step-2-get-the-contents-color-volume-information"></a>Paso 2. Obtención de la información de volumen de color del contenido

En función de dónde provenga el contenido de HDR, hay varias formas posibles de determinar la luminancia y la información de la gama de colores. Algunos archivos de imagen y vídeo HDR contienen metadatos SMPTE ST. 2086. Si el contenido se representó dinámicamente, es posible que pueda extraer información de la escena de las fases de representación internas, por ejemplo, la fuente de luz más brillante de una escena.

Una solución más general pero costosamente costosa es ejecutar un histograma u otro paso de análisis en el fotograma representado. El [ejemplo de SDK de imágenes de color avanzado de direct2d](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) muestra cómo hacerlo con Direct2D; a continuación se incluyen los fragmentos de código más relevantes:

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

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a>Paso 3. Realización de la operación HDR tonemapping

Tonemapping es intrínsecamente un proceso de pérdida y se puede optimizar para una serie de métricas perceptuales o objetivas, por lo que no hay un algoritmo estándar. Windows proporciona un [efecto tonemapper de HDR](../direct2d/hdr-tone-map-effect.md) integrado como parte de Direct2D y en la canalización de reproducción de vídeo HDR Media Foundation. Entre otros algoritmos de uso común se incluyen las ACE filme, Reinhard y ITU-R BT. 2390-3 EETF (función de transferencia eléctrica eléctrica).

A continuación se muestra un operador Reinhard tonemapper simplificado.

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

Las API que admiten la especificación de formatos de píxeles, como las del espacio de nombres [**Windows. Graphics. Capture**](/uwp/api/windows.graphics.capture) y el método [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , proporcionan la capacidad de capturar contenido HDR y WCG sin perder información de píxeles. Tenga en cuenta que después de adquirir los marcos de contenido, se requiere un procesamiento adicional. Por ejemplo, la asignación de tonos HDR a SDR (por ejemplo, copia de pantalla de SDR para el uso compartido de Internet) y almacenamiento de contenido con el formato correcto (por ejemplo, JPEG XR).

## <a name="additional-resources"></a>Recursos adicionales

* *Uso de la representación de HDR con el kit de herramientas de DirectX* para DirectX [11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering). Tutorial sobre cómo agregar compatibilidad con HDR a una aplicación de DirectX mediante el kit de herramientas de DirectX (DirectXTK).
* [Ejemplo de SDK de imágenes de color avanzadas de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages). Ejemplo de SDK de UWP que implementa un visor de imágenes HDR y WCG avanzado compatible con el color mediante Direct2D. Muestra el abanico completo de procedimientos recomendados para las aplicaciones UWP, como la respuesta a la visualización de cambios en la funcionalidad y el ajuste del nivel blanco de SDR.
* [Ejemplo de escritorio de encabezado de Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR). Ejemplo de SDK de escritorio que implementa una escena de HDR de Direct3D 12 básica.
* [Ejemplo de UWP de Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR). Equivalente a UWP del ejemplo anterior.
* [Ejemplo de PC SimpleHDR de Xbox ATG](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC). Ejemplo de SDK de escritorio que implementa una escena de HDR de Direct3D 11 básica.

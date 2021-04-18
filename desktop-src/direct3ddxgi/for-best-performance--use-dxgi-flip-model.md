---
description: En este tema se proporcionan instrucciones para desarrolladores sobre cómo maximizar el rendimiento y la eficacia en la pila de presentaciones en versiones modernas de Windows.
ms.assetid: B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1
title: Para obtener el mejor rendimiento, use DXGI Flip Model
ms.topic: article
ms.date: 05/31/2018
ms.custom: RS5
ms.openlocfilehash: 2a1e671c03f468fd62b0b5bad0f008f84e62ca3c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705199"
---
# <a name="for-best-performance-use-dxgi-flip-model"></a>Para obtener el mejor rendimiento, use DXGI Flip Model

En este tema se proporcionan instrucciones para desarrolladores sobre cómo maximizar el rendimiento y la eficacia en la pila de presentaciones en versiones modernas de Windows. Recoge dónde está el [modelo de volteo de DXGI](dxgi-flip-model.md), [DirectX 12: modos de presentación en Windows 10 (vídeo)](https://www.youtube.com/watch?v=E3wTajGZOsA)y [mejoras en la presentación en Windows 10: una mirada rápida (vídeo)](https://www.youtube.com/watch?v=nUZVV_mssWQ) .

## <a name="call-to-action"></a>Llamada a la acción

Si sigue usando el efecto de **intercambio de dxgi, \_ \_ \_ descarte** o **efecto de intercambio de dxgi \_ \_ \_ secuencial** (también conocido como el modelo de presentación de "BLT", es el momento de detenerse.

Cambiar al **efecto de intercambio de dxgi \_ \_ \_ volteo \_** del efecto de intercambio de dxgi o secuencial **\_ \_ \_ Flip \_ descartar** (también conocido como el modelo Flip) proporcionará un mejor rendimiento y un menor consumo de energía, y proporcionará un conjunto de características más completo. (Consulte [ \_ \_ enumeración de efectos de intercambio de DXGI](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) para obtener más información sobre estos valores).

El modelo de volteo se presenta hasta el momento en que el modo de ventana es realmente equivalente o mejor en comparación con el modo clásico de "pantalla completa". De hecho, es posible que desee volver a considerar si la aplicación realmente necesita un modo exclusivo de pantalla completa, ya que las ventajas de una ventana sin borde del modelo de volteo incluyen un cambio de Alt-Tab más rápido y una mejor integración con las características modernas de pantalla.

¿Por qué se aplican ahora? Antes de la actualización del 2018 de abril, el modelo de BLT podría dar lugar a una interrupción visible cuando se usa en configuraciones de GPU híbridas, que a menudo se encuentran en equipos portátiles de tecnología avanzada (consulte [KB 3158621](https://support.microsoft.com/help/3158621/hybrid-graphics-and-vsync-results-in-graphic-tearing-in-some-games-and)). En la actualización del 2018 de abril, este corte se ha solucionado, a costa de algún trabajo adicional. Si está llevando a cabo BLT en alta framerate a través de GPU híbridas, especialmente en resoluciones altas como 4K, este trabajo adicional puede afectar al rendimiento general. Para mantener el mejor rendimiento en estos sistemas, cambie desde BLT al modelo Flip Present. Además, considere la posibilidad de reducir la resolución de su intercambio, especialmente si no es el punto principal de interacción con el usuario (como suele ser el caso de las ventanas de la vista previa de VR).

## <a name="a-brief-history"></a>Un breve historial

¿Qué es el modelo Flip? ¿Cuál es la alternativa?

Antes de Windows 7, la única manera de presentar contenido desde D3D era "BLT" o copiarlo en una superficie que era propiedad de la ventana o la pantalla. A partir del efecto de intercambio de D3D9's FLIPEX, que llega a DXGI a través del \_ efecto Flip Sequential swap en Windows 8, hemos desarrollado una manera más eficaz de poner el contenido en pantalla compartiendo directamente con el compositor de escritorio, con copias mínimas. Consulte [modelo de volteo de DXGI](dxgi-flip-model.md) para obtener información general de alto nivel de la tecnología.

Esta optimización es posible gracias a DWM (Administrador de ventanas de escritorio), que es el compositor que controla el escritorio de Windows.

## <a name="when-should-i-use-the-blt-model"></a>¿Cuándo debo usar el modelo BLT?

Hay una parte de la funcionalidad que el modelo de volteo no proporciona: la capacidad de tener varias API diferentes que producen contenido, que se agrupan en el mismo **hWnd** en la actualidad. Un ejemplo de esto sería usar D3D para dibujar el fondo de una ventana y, a continuación, [Windows GDI](/windows/desktop/gdi/windows-gdi) para dibujar algo encima, o bien dos API de gráficos diferentes, o dos intercambio de la misma API, para generar fotogramas alternativos. Si no necesita interoperabilidad de nivel **hWnd** entre componentes de gráficos, no necesita el modelo BLT.

Hay una segunda parte de la funcionalidad que no se proporcionó en el diseño del modelo Flip original, pero que ahora está disponible, que es la capacidad de presentar en una velocidad de fotogramas no limitada. En el caso de una aplicación que usa el intervalo de sincronización 0, no se recomienda cambiar al modelo de volteo a menos que esté disponible la API [IDXGIFactory5:: CheckFeatureSupport](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) y que los informes de compatibilidad con la **característica de DXGI \_ \_ presente \_ permitan el \_ recorte**. Esta característica es casi ubicua en las versiones recientes de Windows 10 y en el hardware moderno.

## <a name="directflip"></a>DirectFlip

Si ha observado [DirectX 12: modos de presentación en Windows 10](https://www.youtube.com/watch?v=E3wTajGZOsA), verá hablar acerca de "Direct Flip" y "volteo independiente". Estas son las optimizaciones que están habilitadas para las aplicaciones que usan Flip Model intercambio. En función de la configuración de la ventana y del búfer, es posible omitir completamente la composición del escritorio y enviar directamente los marcos de la aplicación a la pantalla, de la misma manera que lo hace el modo de pantalla completa.

Estos días, estas optimizaciones pueden participar en uno de tres escenarios, en orden de funcionalidad creciente:

1.  **DirectFlip**: los búferes de intercambio coinciden con las dimensiones de la pantalla y su región de cliente de ventana cubre la pantalla. En lugar de usar el intercambio de DWM para mostrarse en la pantalla, se usa la aplicación intercambio.
2.  **DirectFlip con el panel de instalador**: la región de cliente de Windows cubre la pantalla y los búferes de intercambio se encuentran dentro de un factor de escala dependiente del hardware (por ejemplo, de 0,25 x a 4x) de la pantalla. El hardware scanout de GPU se usa para escalar el búfer mientras lo envía a la pantalla.
3.  **DirectFlip con superposición de varios planos (MPO)**: los búferes intercambio se encuentran dentro de algún factor de escala dependiente del hardware de las dimensiones de la ventana. DWM puede reservar un plano de scanout de hardware dedicado para su aplicación, que luego se analiza y se ajusta potencialmente a una subregión alfa combinada de la pantalla.

Con el modelo de volteo de ventanas, la aplicación puede consultar la compatibilidad de hardware para diferentes escenarios de DirectFlip e implementar diferentes tipos de escalado dinámico mediante el uso de [IDXGIOutput6:: CheckHardwareCompositionSupport](/windows/desktop/api/DXGI1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport). Es importante tener en cuenta que si se usan los instaladores de los paneles, es posible que el cursor sufra efectos secundarios de ajuste, lo que se indica a través de la **\_ \_ marca de \_ compatibilidad con \_ \_ \_ la composición de hardware de DXGI**.

Una vez que el intercambio ha sido "DirectFlipped", el DWM puede entrar en suspensión y reactivarse cuando algo cambia fuera de la aplicación. Los fotogramas de la aplicación se envían directamente a la pantalla, de forma independiente, con la misma eficacia que el modo de pantalla completa. Este es el "volteo independiente" y puede participar en todos los escenarios anteriores. Si el contenido de un escritorio se incluye en la parte superior, el DWM puede realizar una transición sin problemas al modo compuesto, "recomponer" de forma eficaz el contenido que se encuentra en la parte superior de la aplicación antes de voltearlo, o aprovechar MPO para mantener el modo de volteo independiente.

Consulte la herramienta [PresentMon](https://github.com/GameTechDev/PresentMon) para obtener información sobre el uso de la versión anterior.

## <a name="what-else-is-new-in-the-flip-model"></a>¿Qué más es nuevo en el modelo de volteo?

Además de las mejoras anteriores, que se aplican a intercambio estándar sin nada especial, hay varias características disponibles para el uso de las aplicaciones de Flip Model:

-   Disminución de latencia mediante **el \_ \_ objeto de \_ \_ \_ \_ espera \_ de trama** de la cadena de intercambio de DXGI. En el modo de volteo independiente, puede reducir hasta un fotograma de latencia en las versiones recientes de Windows, con una reserva estable al mínimo posible cuando se crea.
    -   ADVERTENCIA: se ha producido un problema que dio un mínimo de dos marcos de latencia en la actualización de aniversario de Windows 10 y versiones anteriores. Consulte [este tema del Foro](https://www.gamedev.net/forums/topic/686507-windows-10-dx12-low-latency-tearing-free-rendering/) para obtener más información. Esto se ha corregido en la actualización de Fall Creator.
-   **DXGI \_ Efecto de intercambio \_ \_ Flip \_ discard** permite un modo de "composición inversa" de Direct Flip, lo que da lugar a un trabajo menos general para mostrar el escritorio. DWM puede hacer garabatos en los búferes de la aplicación y enviarlos a la pantalla, en lugar de realizar una copia completa en su propio intercambio.
-   **DXGI \_ El \_ marcador de cadena de intercambio \_ permitir el \_ \_ recorte** puede habilitar una latencia incluso menor que el objeto que se puede esperar, incluso en una ventana de sistemas con compatibilidad con superposición de varios planos.
-   Las aplicaciones tienen control sobre el escalado de contenido que se produce durante el redimensionamiento de las ventanas, mediante la propiedad de [ \_ escala de DXGI](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling) establecida durante la creación de intercambio.
-   El contenido en formatos HDR (R10G10B10A2 \_ UNORM o R16G16B16A16 \_ float) no se fija a menos que esté compuesto por un escritorio SDR.
-   Las estadísticas presentes están disponibles en el modo de ventana.
-   Existe una mayor compatibilidad con el modelo de aplicación de UWP (Plataforma universal de Windows) y DX12, ya que solo son compatibles con el modelo de volteo.

## <a name="what-do-i-have-to-do-to-use-the-flip-model"></a>¿Qué tengo que hacer para usar el modelo de volteo?

Flip Model intercambio tiene algunos requisitos adicionales sobre BLT intercambio:

1.  El número de búferes debe ser al menos 2.
2.  Después de las llamadas [presentes](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) , el búfer de reserva debe volver a enlazarse explícitamente al contexto inmediato de D3D11 antes de que se pueda volver a usar.
3.  Después de llamar a [SetFullscreenState](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate), la aplicación debe llamar a [ResizeBuffers](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) antes de **presentar**.
4.  Los intercambio de MSAA (suavizado de contorno de muestreo múltiple) no se admiten directamente en el modelo Flip, por lo que la aplicación deberá realizar una resolución de MSAA antes de emitir el **presente**.

## <a name="how-to-choose-the-right-rendering-and-presentation-resolutions"></a>Cómo elegir las resoluciones de representación y presentación correctas

El patrón tradicional para aplicaciones en el pasado ha sido proporcionar al usuario una lista de resoluciones entre las que elegir cuando el usuario selecciona el modo de pantalla completa exclusiva. Con la capacidad de las pantallas modernas para empezar a escalar el contenido sin problemas, considere la posibilidad de proporcionar a los usuarios la capacidad de elegir una resolución de representación para el escalado de rendimiento, independientemente de la resolución de salida, e incluso en el modo de ventana. Además, las aplicaciones deben aprovechar **IDXGIOutput6:: CheckHardwareCompositionSupport** para determinar si es necesario escalar el contenido antes de presentarlo, o bien si deben permitir que el hardware realice el escalado para ellos.

Es posible que sea necesario migrar el contenido de una GPU a otra como parte de la operación presente o de composición. Esto suele ser cierto en equipos portátiles de varias GPU o sistemas con GPU externas conectadas. Dado que estas configuraciones son más comunes y, a medida que las pantallas de alta resolución son más comunes, el costo de presentar una intercambio de resolución completa aumenta. Si el destino de su intercambio no es el punto principal de interacción con el usuario, como suele ser el caso de los títulos de VR que presentan una vista previa 2D de la escena de VR en una ventana secundaria, considere la posibilidad de usar una intercambio de resolución inferior para minimizar la cantidad de ancho de banda que se debe transferir a través de diferentes GPU.

## <a name="other-considerations"></a>Otras consideraciones

La primera vez que pida a la GPU que escriba en el búfer de reserva de intercambio es el tiempo que la GPU se pondrá en espera para que el búfer esté disponible. Siempre que sea posible, retrasar este punto en el fotograma como sea posible.

 

 

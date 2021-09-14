---
description: En este tema se proporcionan instrucciones para desarrolladores sobre cómo maximizar el rendimiento y la eficacia en la pila de presentación en versiones modernas de Windows.
ms.assetid: B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1
title: Para obtener el mejor rendimiento, use el modelo de volteo DXGI.
ms.topic: article
ms.date: 05/31/2018
ms.custom: RS5
ms.openlocfilehash: 2a1e671c03f468fd62b0b5bad0f008f84e62ca3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360847"
---
# <a name="for-best-performance-use-dxgi-flip-model"></a>Para obtener el mejor rendimiento, use el modelo de volteo DXGI.

En este tema se proporcionan instrucciones para desarrolladores sobre cómo maximizar el rendimiento y la eficacia en la pila de presentación en versiones modernas de Windows. Recoge el modelo de volteo [DXGI,](dxgi-flip-model.md) [DirectX 12:](https://www.youtube.com/watch?v=E3wTajGZOsA)Modos de presentación en Windows 10 (vídeo) y Mejoras de presentación en Windows 10: Una apariencia [temprana (vídeo)](https://www.youtube.com/watch?v=nUZVV_mssWQ) dejados.

## <a name="call-to-action"></a>Llamada a la acción

Si sigue usando **DXGI \_ SWAP EFFECT \_ \_ DISCARD** o **DXGI SWAP EFFECT \_ \_ \_ SEQUENTIAL** (también es decir, el modelo "blt" actual), es el momento de detenerse.

Cambio a **DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL** o **DXGI SWAP EFFECT FLIP \_ \_ \_ \_ DISCARD** (también es decir, el modelo de volteo) proporcionará un mejor rendimiento, un menor uso de energía y proporcionará un conjunto más completo de características. (Consulte [enumeración DXGI \_ SWAP \_ EFFECT](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) para obtener más información sobre estos valores).

Los presentaciones de modelo de volteo van tan lejos como hacer que el modo de ventana sea equivalente o mejor en comparación con el modo clásico "pantalla completa exclusiva". De hecho, es posible que quiera replantearse si la aplicación realmente necesita un modo exclusivo de pantalla completa, ya que las ventajas de una ventana sin borde del modelo de volteo incluyen una conmutación de Alt-Tab más rápida y una mejor integración con características de pantalla modernas.

¿Por qué se aplican ahora? Antes de la actualización de abril de 2018, el modelo blt presentaba un desgarro visible cuando se usaba en configuraciones de GPU híbridas, que a menudo se encontraban en equipos portátiles de gama alta (consulte [KB 3158621](https://support.microsoft.com/help/3158621/hybrid-graphics-and-vsync-results-in-graphic-tearing-in-some-games-and)). En la actualización de abril de 2018, se ha corregido este desgarro, a costa de algún trabajo adicional. Si va a realizar presentaciones con velocidades de fotogramas elevadas en GPU híbridas, especialmente en resoluciones altas como 4K, este trabajo adicional puede afectar al rendimiento general. Para mantener el mejor rendimiento en estos sistemas, cambie del modelo blt al modelo actual de volteo. Además, considere la posibilidad de reducir la resolución de la cadena de intercambio, especialmente si no es el punto principal de interacción del usuario (como suele ser el caso de las ventanas de vista previa de VR).

## <a name="a-brief-history"></a>Un breve historial

¿Qué es el modelo flip? ¿Cuál es la alternativa?

Antes de Windows 7, la única manera de presentar contenido de D3D era "blt" o copiarlo en una superficie que era propiedad de la ventana o pantalla. A partir del efecto de intercambio FLIPEX de D3D9 y la llegada a DXGI a través del efecto de intercambio FLIP SEQUENTIAL en Windows 8, hemos desarrollado una manera más eficaz de colocar contenido en pantalla al compartirlo directamente con el compositor de escritorio, con copias \_ mínimas. Consulte [Modelo de volteo DXGI](dxgi-flip-model.md) para obtener información general de alto nivel de la tecnología.

Esta optimización es posible gracias a DWM (Administrador de ventanas de escritorio), que es el compositor que dirige el Windows escritorio.

## <a name="when-should-i-use-the-blt-model"></a>¿Cuándo debo usar el modelo blt?

Hay una parte de la funcionalidad que el modelo de volteo no proporciona: la capacidad de tener varias API diferentes que producen contenido, que se capa a su vez en el mismo **HWND,** de forma presente por presente. Un ejemplo de esto sería usar D3D para dibujar un fondo de ventana y, Windows continuación, [un GDI](/windows/desktop/gdi/windows-gdi) para dibujar algo en la parte superior, o usar dos API de gráficos diferentes, o dos cadenas de intercambio de la misma API, para generar fotogramas alternos. Si no necesita interoperabilidad **de nivel HWND** entre componentes de gráficos, no necesita el modelo blt.

Hay una segunda parte de funcionalidad que no se proporcionó en el diseño original del modelo de volteo, pero que ahora está disponible, que es la capacidad de presentarse en una velocidad de fotogramas no limitada. En el caso de una aplicación que usa el intervalo de sincronización 0, no se recomienda cambiar al modelo de volteo a menos que la API [IDXGIFactory5::CheckFeatureSupport](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) esté disponible e informe de la compatibilidad con **DXGI \_ FEATURE PRESENT ALLOW \_ \_ \_ TEARING**. Esta característica es casi ubicua en las versiones recientes de Windows 10 y en hardware moderno.

## <a name="directflip"></a>DirectFlip

Si ha visto [DirectX 12: Modos](https://www.youtube.com/watch?v=E3wTajGZOsA)de presentación en Windows 10 , verá hablar sobre "Direct Flip" y "Independent Flip". Se trata de optimizaciones que están habilitadas para las aplicaciones que usan cadenas de intercambio de modelos de volteo. En función de la configuración de la ventana y del búfer, es posible omitir la composición del escritorio por completo y enviar directamente marcos de aplicación a la pantalla, de la misma manera que lo hace la pantalla completa exclusiva.

En estos días, estas optimizaciones pueden participar en uno de tres escenarios, con el fin de aumentar la funcionalidad:

1.  **DirectFlip:** los búferes de la cadena de intercambio coinciden con las dimensiones de la pantalla y la región cliente de la ventana cubre la pantalla. En lugar de usar la cadena de intercambio DWM para mostrarla en la pantalla, se usa la cadena de intercambio de aplicaciones.
2.  **DirectFlip con fitters** del panel: la región de cliente de la ventana cubre la pantalla y los búferes de la cadena de intercambio están dentro de algún factor de escalado dependiente del hardware (por ejemplo, de 0,25x a 4x) de la pantalla. El hardware de examen de GPU se usa para escalar el búfer mientras se envía a la pantalla.
3.  **DirectFlip con superposición de** varios plano (MPO): los búferes de cadena de intercambio están dentro de algún factor de escalado dependiente del hardware de las dimensiones de la ventana. DwM puede reservar un plano de examen de hardware dedicado para la aplicación, que luego se analiza y se extiende potencialmente a una sub-región de mezcla alfa de la pantalla.

Con el modelo de volteo de ventana, la aplicación puede consultar la compatibilidad de hardware para distintos escenarios de DirectFlip e implementar diferentes tipos de escalado dinámico mediante el uso de [IDXGIOutput6::CheckHardwareCompositionSupport.](/windows/desktop/api/DXGI1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport) Una advertencia que hay que tener en cuenta es que si se usan los fitters del panel, es posible que el cursor sufra efectos secundarios de extensión, que se indican a través de **DXGI \_ HARDWARE COMPOSITION SUPPORT FLAG CURSOR \_ \_ \_ \_ \_ STRETCHED**.

Una vez que la cadena de intercambio ha sido "DirectFlipped", dwm puede entrar en suspensión y solo reactivar cuando algo cambia fuera de la aplicación. Los marcos de aplicación se envían directamente a la pantalla, de forma independiente, con la misma eficacia que la pantalla completa exclusiva. Se trata de "Flip independiente" y puede participar en todos los escenarios anteriores. Si hay otros contenidos de escritorio encima, dwm puede realizar la transición sin problemas al modo compuesto, "componer" eficazmente el contenido encima de la aplicación antes de voltearlo, o bien aprovechar MPO para mantener el modo de volteo independiente.

Consulte la herramienta [PresentMon](https://github.com/GameTechDev/PresentMon) para obtener información sobre cuál de los anteriores se usó.

## <a name="what-else-is-new-in-the-flip-model"></a>¿Qué más hay de nuevo en el modelo de volteo?

Además de las mejoras anteriores, que se aplican a las cadenas de intercambio estándar sin nada especial, hay varias características disponibles para que las aplicaciones de modelo flip usen:

-   Reducir la latencia mediante **DXGI \_ SWAP CHAIN FLAG FRAME \_ \_ \_ \_ LATENCY \_ WAITABLE \_ OBJECT**. Cuando está en el modo de inversión independiente, puede llegar a un fotograma de latencia en las versiones recientes de Windows, con una reserva correcta al mínimo posible cuando se compone.
    -   Advertencia: hubo un problema que dio un mínimo de dos fotogramas de latencia en la actualización de aniversario Windows 10 anterior. Consulte [este tema del foro](https://www.gamedev.net/forums/topic/686507-windows-10-dx12-low-latency-tearing-free-rendering/) para obtener más información. Esto se ha corregido en Fall Creator's Update.
-   **DXGI \_ SWAP \_ EFFECT FLIP DISCARD \_ \_ habilita** un modo de "composición inversa" de volteo directo, lo que da como resultado un trabajo menos general para mostrar el escritorio. DwM puede suscribirse en los búferes de la aplicación y enviarlos a la pantalla, en lugar de realizar una copia completa en sus propias cadenas de intercambio.
-   **DXGI \_ SWAP \_ CHAIN FLAG ALLOW \_ \_ \_ TEARING** puede permitir una latencia incluso menor que el objeto que se puede esperar, incluso en una ventana en sistemas con compatibilidad con superposición de varios planos.
-   Las aplicaciones tienen control sobre el escalado de contenido que se produce durante el cambio de tamaño de la ventana, mediante la [propiedad DXGI \_ SCALING](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling) establecida durante la creación de la cadena de intercambio.
-   El contenido en formatos HDR (R10G10B10A2 UNORM o \_ R16G16B16A16 FLOAT) no se fija a menos que esté compuesto por un escritorio \_ SDR.
-   Las estadísticas presentes están disponibles en modo de ventana.
-   Hay una mayor compatibilidad con el modelo de aplicación de UWP (Plataforma Windows universal) y DX12, ya que solo son compatibles con el modelo flip.

## <a name="what-do-i-have-to-do-to-use-the-flip-model"></a>¿Qué tengo que hacer para usar el modelo flip?

Las cadenas de intercambio de modelos de volteo tienen algunos requisitos adicionales sobre las cadenas de intercambio blt:

1.  El número de búferes debe ser al menos 2.
2.  Después [de llamar](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) a Present, el búfer de reserva debe volver a enlazarse explícitamente al contexto inmediato D3D11 antes de poder volver a usarse.
3.  Después de llamar [a SetFullscreenState](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate), la aplicación debe llamar a [ResizeBuffers](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) antes de **present**.
4.  Las cadenas de intercambio de MSAA (suavizado de alias multiejemplo) no se admiten directamente en el modelo de volteo, por lo que la aplicación deberá realizar una resolución de MSAA antes de emitir **present**.

## <a name="how-to-choose-the-right-rendering-and-presentation-resolutions"></a>Cómo elegir las resoluciones de presentación y representación correctas

El patrón tradicional para las aplicaciones en el pasado ha sido proporcionar al usuario una lista de resoluciones entre las que elegir cuando el usuario selecciona el modo de pantalla completa exclusivo. Con la capacidad de las pantallas modernas de empezar a escalar contenido sin problemas, considere la posibilidad de proporcionar a los usuarios la capacidad de elegir una resolución de representación para el escalado del rendimiento, independiente de una resolución de salida e incluso en modo de ventana. Además, las aplicaciones deben aprovechar **IDXGIOutput6::CheckHardwareCompositionSupport** para determinar si necesitan escalar el contenido antes de presentarlo, o si deben permitir que el hardware realice el escalado para ellas.

Es posible que el contenido tenga que migrarse de una GPU a otra como parte de la operación actual o de composición. Esto suele ser así en equipos portátiles con varias GPU o sistemas con GPU externas conectadas. A medida que estas configuraciones se hacen más comunes y a medida que las pantallas de alta resolución se vuelven más comunes, aumenta el costo de presentar una cadena de intercambio de resolución completa. Si el destino de la cadena de intercambio no es el punto principal de interacción del usuario, como suele ser el caso de los títulos vr que presentan una vista previa 2D de la escena de realidad virtual en una ventana secundaria, considere la posibilidad de usar una cadena de intercambio de resolución inferior para minimizar la cantidad de ancho de banda que debe transferirse entre diferentes GPU.

## <a name="other-considerations"></a>Otras consideraciones

La primera vez que pida a la GPU que escriba en el búfer de reserva de la cadena de intercambio es el tiempo que la GPU se detendrán a la espera de que el búfer esté disponible. Cuando sea posible, retrase este punto lo más lejos posible en el marco.

 

 

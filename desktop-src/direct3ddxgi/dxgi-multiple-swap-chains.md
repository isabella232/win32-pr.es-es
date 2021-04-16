---
description: Para mejorar el rendimiento, es posible que desee crear más de una cadena de intercambio por dispositivo de representación de Direct3D.
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: Mejorar el rendimiento con varias cadenas de intercambio por dispositivo de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e356434521054bc13b553c8ae3d6e43d8d98ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495221"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>Mejorar el rendimiento con varias cadenas de intercambio por dispositivo de representación

Para mejorar el rendimiento, es posible que desee crear más de una cadena de intercambio por dispositivo de representación de Direct3D. Use este enfoque para ahorrar memoria que se requiere mediante la creación de dispositivos adicionales o para reducir la cantidad de tiempo de representación que se va a representar en cadenas de intercambio individuales por dispositivo por separado, o bien para ahorrar memoria y reducir el tiempo de representación.

-   [Escenarios de aplicaciones con varias cadenas de intercambio por dispositivo](#app-scenarios-with-multiple-swap-chains-per-device)
-   [Administración de varias cadenas de intercambio por dispositivo](#managing-multiple-swap-chains-per-device)
    -   [Establecer la latencia máxima de fotogramas](#setting-maximum-frame-latency)
    -   [Usar Flip Model con varias cadenas de intercambio por dispositivo](#using-flip-model-with-multiple-swap-chains-per-device)
-   [Temas relacionados](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>Escenarios de aplicaciones con varias cadenas de intercambio por dispositivo

Considere la posibilidad de usar varias cadenas cuando la escena de la aplicación se compone de objetos de visualización independientes que se representan y actualizan de forma independiente. Por ejemplo, la aplicación ha cambiado constantemente la animación, como vídeo en un lado y texto desplazable en otro lado. Para ahorrar memoria que normalmente tendría que crear un dispositivo adicional y facilitar el uso compartido de contenido entre las dos cadenas de intercambio, puede crear ambas cadenas de intercambio asociadas al mismo dispositivo de representación de Direct3D. Use una cadena de intercambio para la animación y una cadena de intercambio para el texto. Un ejemplo común de este escenario es una aplicación de Direct3D que también usa la API de [DirectComposition](../directcomp/directcomposition-portal.md) .

Otro escenario es cuando desea ahorrar tiempo de representación estableciendo varios destinos de representación en varias cadenas de intercambio simultáneamente. Por ejemplo, supongamos que desea representar una escena compleja con una gran cantidad de texturas y geometría, como coches de carreras en una pista, y desea que la ventana de la aplicación muestre las vistas de los reflejos trasero y lateral en dos ventanas de visualización que se representan mediante dos cadenas de intercambio. Si establece las cadenas de intercambio múltiples como destinos de representación, no es necesario que la aplicación Repita los tiempos de representación en cada cadena de intercambio por separado.

## <a name="managing-multiple-swap-chains-per-device"></a>Administración de varias cadenas de intercambio por dispositivo

Siga las instrucciones de esta sección para administrar varias cadenas de intercambio que cree para un único dispositivo de representación de Direct3D.

### <a name="setting-maximum-frame-latency"></a>Establecer la latencia máxima de fotogramas

Use el método [**IDXGIDevice1:: SetMaximumFrameLatency**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) para establecer el número máximo de operaciones presentes que el sistema operativo puede poner en cola para su representación en la pantalla. Este número máximo es por dispositivo de representación de Direct3D en lugar de por cadena de intercambio. Por lo tanto, para asegurarse de que el sistema operativo muestra las operaciones presentes en el intervalo de VSYNC deseado, se recomienda no establecer la latencia máxima de fotogramas en 1 al crear varias cadenas de intercambio de modelo de volteo o bitblt por dispositivo y cuando se representará más de una de esas cadenas de intercambio para cada fotograma. Como norma general, si envía de forma confiable solo 2 operaciones de presentación por fotograma entre todas las cadenas de intercambio del mismo dispositivo, puede establecer la latencia máxima de fotogramas en 2. Si no puede enviar y contar de forma confiable las operaciones presentes por fotograma, puede usar [estadísticas presentes](dxgi-flip-model.md) para realizar el seguimiento cuando el sistema operativo muestra las operaciones presentes.

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>Usar Flip Model con varias cadenas de intercambio por dispositivo

Siga estas directrices cuando use el [modelo de volteo de DXGI](dxgi-flip-model.md) con varias cadenas de intercambio que cree para un único dispositivo de representación de Direct3D.

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>Establecer como destino intervalos de VSYNC específicos con las operaciones presentes de cada cadena de intercambio

Cuando cree dos o más cadenas de intercambio de modelo de volteo por dispositivo, preste atención a las diferencias de visualización al administrar la secuencia de estado del dispositivo y la secuencia de llamadas al método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) de todas las cadenas de intercambio. Para asegurarse de que el sistema operativo muestra la operación de presentación de cada cadena de intercambio en el intervalo de VSYNC deseado, se recomienda asegurarse de que el número de operaciones presentes en cola sea siempre al menos uno menos que el número de búferes de reserva de la cadena de intercambio con el menor número de búferes de reserva.

### <a name="flip-model-swap-chains-with-two-buffers"></a>Voltear cadenas de intercambio de modelo con dos búferes

La aplicación puede tener como destino intervalos de VSYNC específicos cuando el número de operaciones presentes en cola es menor o igual que el número de búferes de reserva: 1. Además, debe usar o representar en cada cadena de intercambio por separado y, a continuación, terminar el uso de cada cadena de intercambio con una operación Present. Por lo tanto, cuando se envía cada operación present para una cadena de intercambio de dos búferes de cambio de modelo, se alcanza el umbral para el número de búferes de reserva en los que se debe prestar atención especial si se desea que la aplicación tenga como destino intervalos de VSYNC específicos.

En el caso de las cadenas de intercambio de búfer 2, para dirigirse a intervalos de VSYNC específicos, debe asegurarse de que el sistema operativo termine de mostrar la operación de presentación de cada cadena de intercambio antes de representarla al siguiente búfer. Se recomienda finalizar la configuración de la vista de destino de representación y otro estado de representación, siguiente representación y, a continuación, llamar a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para cada uno de los dos búferes de una cadena de intercambio antes de hacer lo mismo con otra cadena de intercambio. Cuando se trabaja con dos o más cadenas de intercambio, es necesario restablecer el destino de representación y el estado de representación en el dispositivo para cada cadena de intercambio. La ventaja de este enfoque es evitar el caso en el que una o varias de las operaciones presentes de la cadena de intercambio pierden el intervalo de VSYNC previsto. En el primer ejemplo, aplicación con cambio de animación y texto, como se describe en [escenarios de aplicaciones con varias cadenas de intercambio por dispositivo](#app-scenarios-with-multiple-swap-chains-per-device), al establecer como destino los intervalos presentes específicos, se garantiza que cuando la animación se actualice en una ventana de visualización, el texto correspondiente representado por una cadena de intercambio independiente también se muestra al mismo tiempo en otra ventana de visualización. Si la aplicación necesita tener como destino intervalos de VSYNC específicos, debe seguir esta guía.

En este diagrama se muestra un ejemplo del flujo de código de representación y presentación de la cadena de intercambio en una aplicación con dos cadenas de intercambio de modelo de volteo cada una con dos búferes. En este caso, debe tener como destino un intervalo presente específico para cada operación Present.

![Ilustración del modelo de volteo con dos búferes](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>Reducir el tiempo de representación al establecer simultáneamente varias cadenas de intercambio como destinos de representación

En el segundo ejemplo, los automóviles de carreras de una pista, tal y como se describe en [escenarios de aplicaciones con varias cadenas de intercambio por dispositivo](#app-scenarios-with-multiple-swap-chains-per-device), puede que le interese desasociar los intervalos de sincronización de transacciones presentes específicos de destino con el ahorro de tiempo de representación que obtiene estableciendo varios destinos de representación en todas las cadenas de intercambio simultáneamente. En este caso, establezca varios destinos de representación simultáneamente, represente la escena en cada cadena de intercambio y, a continuación, llame a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) en cada cadena de intercambio que se use en la escena. La ventaja de este enfoque es reducir el tiempo de representación. La limitación de este enfoque es que las operaciones presentes de la cadena de intercambio simultánea no pueden tener como destino la misma VSYNC cuando se usan cadenas de intercambio de búfer 2. Por ejemplo, el sistema operativo no mostrará el contenido de los reflejos de la vista lateral del coche de carreras hasta 1 VSYNC después de que el mismo contenido se vea en el reflejo de la vista posterior del coche de carreras.

En este diagrama se muestra un ejemplo del flujo de código de representación y presentación de la cadena de intercambio en una aplicación con dos cadenas de intercambio de modelo de volteo, cada una con dos búferes de longitud. En este tipo de ejemplo, se guardan los tiempos de representación en las cadenas de intercambio 1 y 2 para los búferes A y C. Pero no puede sincronizar los intervalos de VSYNC en los que se muestran las operaciones presentes para los búferes A y C. Este patrón se repite para el fotograma 2.

![Ilustración de la configuración simultánea de varias cadenas de intercambio como destinos de representación](images/multi-swap-chains-as-render-targets.png)

Para evitar que falte el intervalo de VSYNC previsto debido a muchas operaciones presentes en cola, puede aumentar el número de búferes de reserva en cada cadena de intercambio. Pero esta técnica usa más memoria de vídeo. Para evitar que falten intervalos de VSYNC de destino, se recomienda mantener siempre el número de operaciones presentes en cola menos que el número de búferes de reserva de la cadena de intercambio con el menor número de búferes de reserva. Al establecer dos cadenas de intercambio como varios destinos de representación, dado que pone en cola dos operaciones presentes simultáneamente en ambas cadenas de intercambio, se recomienda que cree cadenas de intercambio con al menos tres búferes de longitud.

En el diagrama siguiente se muestra un ejemplo del flujo de código de representación y presentación de la cadena de intercambio en una aplicación con dos cadenas de intercambio de modelo de volteo cada una con tres búferes de longitud. En este caso, dado que el número de presentaciones en cola para un fotograma determinado es 2, que es menor que el número de búferes de reserva por cadena de intercambio, la aplicación puede establecer varios destinos de representación y seguir teniendo como destino los mismos intervalos de VSYNC para los búferes A y D en el fotograma 2 y para los búferes de los fotogramas posteriores.

![Ilustración de la configuración simultánea de varias cadenas de intercambio como destinos de representación destino la misma VSYNC](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar la presentación con el modelo de volteo, los rectángulos modificados y las áreas desplazadas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 

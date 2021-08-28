---
description: Para mejorar el rendimiento, puede crear más de una cadena de intercambio por dispositivo de representación de Direct3D.
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: Mejora del rendimiento con varias cadenas de intercambio por dispositivo de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91445660bf9efc59e9e39c88819587dce3960325df0659487eaae67a845a7329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627501"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>Mejora del rendimiento con varias cadenas de intercambio por dispositivo de representación

Para mejorar el rendimiento, puede crear más de una cadena de intercambio por dispositivo de representación de Direct3D. Use este enfoque para ahorrar memoria necesaria mediante la creación de dispositivos adicionales, o para reducir la cantidad de tiempo de representación que se representará en cadenas de intercambio individuales por dispositivo por separado, o para ahorrar memoria y reducir el tiempo de representación.

-   [Escenarios de aplicaciones con varias cadenas de intercambio por dispositivo](#app-scenarios-with-multiple-swap-chains-per-device)
-   [Administración de varias cadenas de intercambio por dispositivo](#managing-multiple-swap-chains-per-device)
    -   [Establecimiento de la latencia máxima de fotogramas](#setting-maximum-frame-latency)
    -   [Uso de un modelo de volteo con varias cadenas de intercambio por dispositivo](#using-flip-model-with-multiple-swap-chains-per-device)
-   [Temas relacionados](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>Escenarios de aplicaciones con varias cadenas de intercambio por dispositivo

Considere la posibilidad de usar varias cadenas cuando la escena de la aplicación consta de objetos de presentación independientes que se representan y actualizan de forma independiente. Por ejemplo, la aplicación tiene animaciones que cambian constantemente, como vídeo en un lado y texto desplazable en otro lado. Para ahorrar memoria que normalmente tendría que crear un dispositivo adicional y facilitar el uso compartido de contenido entre las dos cadenas de intercambio, puede crear ambas cadenas de intercambio asociadas al mismo dispositivo de representación de Direct3D. Use una cadena de intercambio para la animación y una cadena de intercambio para el texto. Un ejemplo común de este escenario es una aplicación direct3D que también usa [DirectComposition](../directcomp/directcomposition-portal.md) API.

Otro escenario es cuando desea ahorrar tiempo de representación estableciendo varios destinos de representación en varias cadenas de intercambio simultáneamente. Por ejemplo, supongamos que quiere representar una escena compleja con muchas texturas y geometría, como automóviles de carreras en una pista, y quiere que la ventana de la aplicación muestre las vistas de los reflejos rear y side en dos ventanas de presentación que se representan mediante dos cadenas de intercambio. Si establece varias cadenas de intercambio como destinos de representación, la aplicación no tiene que repetir los tiempos de representación en cada cadena de intercambio por separado.

## <a name="managing-multiple-swap-chains-per-device"></a>Administración de varias cadenas de intercambio por dispositivo

Use las directrices de esta sección para administrar varias cadenas de intercambio que cree para un único dispositivo de representación de Direct3D.

### <a name="setting-maximum-frame-latency"></a>Establecimiento de la latencia máxima de fotogramas

Use el [**método IDXGIDevice1::SetMaximumFrameLatency**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) para establecer el número máximo de operaciones actuales que el sistema operativo puede poner en cola para su representación en la pantalla. Este número máximo es por dispositivo de representación de Direct3D en lugar de por cadena de intercambio. Por lo tanto, para asegurarse de que el sistema operativo muestra las operaciones actuales en el intervalo vsync previsto, se recomienda no establecer la latencia máxima de fotogramas en 1 al crear varias cadenas de intercambio de modelos de volteo o bit a bit por dispositivo y cuando se represente más de una de esas cadenas de intercambio para cada fotograma. Como regla general, si envía de forma confiable solo 2 operaciones presentes por fotograma entre todas las cadenas de intercambio del mismo dispositivo, puede establecer la latencia máxima de fotogramas en 2. Si no puede enviar y contar de forma confiable las operaciones actuales por fotograma, puede usar las [estadísticas](dxgi-flip-model.md) actuales para realizar un seguimiento de cuándo el sistema operativo muestra las operaciones presentes.

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>Uso de un modelo de volteo con varias cadenas de intercambio por dispositivo

Use estas directrices cuando use el modelo [de volteo DXGI](dxgi-flip-model.md) con varias cadenas de intercambio que cree para un único dispositivo de representación de Direct3D.

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>Destino de intervalos vsync específicos con las operaciones actuales de cada cadena de intercambio

Al crear dos o más cadenas de intercambio de modelos de volteo por dispositivo, preste atención a las diferencias de visualización al administrar la secuencia de estado del dispositivo y la secuencia de llamadas al método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) de todas las cadenas de intercambio. Para asegurarse de que el sistema operativo muestra la operación actual de cada cadena de intercambio en el intervalo vsync previsto, se recomienda asegurarse de que el número de operaciones presentes en cola siempre sea al menos uno menor que el número de búferes de reserva para la cadena de intercambio con el menor número de búferes de reserva.

### <a name="flip-model-swap-chains-with-two-buffers"></a>Voltear cadenas de intercambio de modelos con dos búferes

La aplicación puede tener como destino intervalos de vsync específicos cuando su número de operaciones presentes en cola es menor o igual que el número de búferes de reserva: 1. Además, debe usar o representar en cada cadena de intercambio por separado y, a continuación, finalizar el uso de cada cadena de intercambio con una operación actual. Por lo tanto, cuando se envían todas las operaciones actuales para una cadena de intercambio de modelo de volteo de dos búferes, se alcanza el umbral del número de búferes de reserva, donde debe prestar especial atención si desea que la aplicación tenga como destino intervalos de vsync específicos.

En el caso de las cadenas de intercambio de dos búferes, para dirigirse a intervalos de vsync específicos, debe asegurarse de que el sistema operativo finaliza la presentación de la operación actual de cada cadena de intercambio antes de representarla en el siguiente búfer. Se recomienda terminar de establecer la vista de destino de representación y otro estado de representación, después representar y, a continuación, llamar a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para cada uno de los dos búferes de una cadena de intercambio antes de hacer lo mismo para otra cadena de intercambio. Cuando trabaje con dos o más cadenas de intercambio, deberá restablecer el destino de representación y el estado de representación en el dispositivo para cada cadena de intercambio. La ventaja de este enfoque es evitar el caso en el que una o varias de las operaciones actuales de la cadena de intercambio pierdan su intervalo vsync previsto. En el primer ejemplo, aplicación con animación y texto [cambiantes,](#app-scenarios-with-multiple-swap-chains-per-device)como se describe en Escenarios de aplicación con varias cadenas de intercambio por dispositivo , al dirigirse a intervalos presentes específicos, se garantiza que cuando la animación se actualiza en una ventana de presentación, el texto correspondiente representado por una cadena de intercambio independiente también se muestra al mismo tiempo en otra ventana de presentación. Si la aplicación necesita tener como destino intervalos de vsync específicos, debe seguir estas instrucciones.

En este diagrama se muestra un ejemplo del flujo de código de representación y presentación de la cadena de intercambio en una aplicación con dos cadenas de intercambio de modelos de volteo cada una con dos búferes. En este caso, debe tener como destino un intervalo presente específico para cada operación actual.

![ilustración del modelo de volteo con dos búferes](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>Reducir el tiempo de representación estableciendo simultáneamente varias cadenas de intercambio como destinos de representación

En el segundo ejemplo, los automóviles de carreras en una pista, como se describe en Escenarios de aplicación con varias cadenas de intercambio por dispositivo , puede que desee cambiar el destino de intervalos vsync presentes específicos con el ahorro de tiempo de representación que se obtiene estableciendo varios [destinos](#app-scenarios-with-multiple-swap-chains-per-device)de representación en todas las cadenas de intercambio simultáneamente. En este caso, establezca varios destinos de representación simultáneamente, represente la escena en cada cadena de intercambio y, a continuación, llame a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) en cada cadena de intercambio que se usa en la escena. La ventaja de este enfoque es que reduce el tiempo de representación. La limitación de este enfoque es que las operaciones de presentación de la cadena de intercambio simultánea no pueden tener como destino la misma sincronización virtual cuando se usan cadenas de intercambio de dos búferes. Por ejemplo, el sistema operativo no mostrará el contenido de los reflejos de la vista lateral del coche de carreras hasta 1 vsync después de que se vea el mismo contenido desde el reflejo de la vista trasera del coche de carreras.

En este diagrama se muestra un ejemplo del flujo de código de representación y presentación de la cadena de intercambio en una aplicación con dos cadenas de intercambio de modelo de volteo cada una con dos búferes de longitud. En este tipo de ejemplo, se ahorran tiempos de representación para intercambiar las cadenas 1 y 2 para los búferes A y C. Pero no se pueden sincronizar los intervalos de vsync en los que se muestran las operaciones actuales para los búferes A y C. Este patrón se repite para el fotograma 2.

![ilustración de la configuración simultánea de varias cadenas de intercambio como destinos de representación](images/multi-swap-chains-as-render-targets.png)

Para evitar que falte el intervalo vsync previsto debido a muchas operaciones presentes en cola, puede aumentar el número de búferes de reserva en cada cadena de intercambio. Pero esta técnica usa más memoria de vídeo. Para evitar que falte el destino vsync intervalos, se recomienda mantener siempre el número de operaciones presentes en cola menor que el número de búferes de reserva en la cadena de intercambio con el menor número de búferes de reserva. Al establecer dos cadenas de intercambio como varios destinos de representación, dado que pone en cola dos operaciones presentes simultáneamente en ambas cadenas de intercambio, se recomienda crear cadenas de intercambio con al menos tres búferes de longitud.

En el diagrama siguiente se muestra un ejemplo del flujo de código de representación y presentación de la cadena de intercambio en una aplicación con dos cadenas de intercambio de modelo de volteo cada una con tres búferes de longitud. En este caso, dado que el número de presentaciones en cola para un fotograma determinado es 2, que es menor que el número de búferes de reserva por cadena de intercambio, la aplicación puede establecer varios destinos de representación y seguir teniendo como destino los mismos intervalos de vsync para los búferes A y D del marco 2 y para los búferes en fotogramas posteriores.

![ilustración de la configuración simultánea de varias cadenas de intercambio como destinos de representación que se destinan a la misma sincronización virtual](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora de la presentación con el modelo de volteo, rectángulos sucios y áreas desplazadas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 

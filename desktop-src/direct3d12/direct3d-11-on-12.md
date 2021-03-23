---
title: Direct3D 11 en 12
description: D3D11On12 es un mecanismo por el que los desarrolladores pueden usar interfaces y objetos de D3D11 para impulsar la API de D3D12.
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62816ea0d7d7969cd56e0a9f525b2c412c8da182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549075"
---
# <a name="direct3d-11-on-12"></a>Direct3D 11 en 12

D3D11On12 es un mecanismo por el que los desarrolladores pueden usar interfaces y objetos de D3D11 para impulsar la API de D3D12. D3D11on12 permite que los componentes escritos con D3D11 (por ejemplo, texto y la interfaz de usuario de D2D) funcionen juntos con los componentes escritos como destino de la API de D3D12. D3D11on12 también habilita el traslado incremental de una aplicación de D3D11 a D3D12, ya que permite que partes de la aplicación continúen orientadas a D3D11 para simplificar, mientras que otras se dirigen a D3D12 de rendimiento, a la vez que siempre tienen una representación completa y correcta. D3D11On12 simplifica el uso de técnicas de interoperabilidad para compartir recursos y sincronizar el trabajo entre las dos API.

-   [Inicializando D3D11On12](#initializing-d3d11on12)
-   [Ejemplo de uso](#example-usage)
-   [Información preliminar](#background)
-   [Limpiar](#cleaning-up)
-   [Limitaciones](#limitations)
-   [API](#apis)
-   [Temas relacionados](#related-topics)

## <a name="initializing-d3d11on12"></a>Inicializando D3D11On12

Para empezar a usar D3D11On12, el primer paso es crear un dispositivo D3D12 y una cola de comandos. Estos objetos se proporcionan como entrada para el método de inicialización [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). Puede considerar este método como la creación de un dispositivo D3D11 con el tipo de controlador imaginario D3D \_ \_ tipo \_ 11ON12, donde el controlador D3D11 es responsable de crear objetos y enviar listas de comandos a la API de D3D12.

Una vez que tenga un dispositivo D3D11 y un contexto inmediato, puede `QueryInterface` desactivar el dispositivo para la interfaz [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) . Esta es la interfaz principal que se usa para la interoperabilidad entre D3D11 y D3D12. Para que las listas de comandos D3D11 y el contexto de dispositivo de D3D12 funcionen en los mismos recursos, es necesario crear "recursos ajustados" mediante la API de [**CreateWrappedResource**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) . Este método "promueve" un recurso D3D12 para que sea comprensible en D3D11. Un recurso ajustado comienza en el estado "adquirido", una propiedad que manipulan los métodos [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) y [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) .

## <a name="example-usage"></a>Ejemplo de uso

El uso típico de D3D11On12 sería usar D2D para representar texto o imágenes encima de un búfer de reserva de D3D12. Vea el ejemplo de D3D11On12 para ver el código de ejemplo. Este es un esquema aproximado de los pasos que se deben seguir para ello:

-   Cree un dispositivo D3D12 ([**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)) y una cadena de intercambio D3D12 ([**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) con un [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) como entrada).
-   Cree un dispositivo D3D11On12 con el dispositivo D3D12 y la misma cola de comandos como entrada.
-   Recupere los búferes de retroceso de la cadena de intercambio y cree recursos encapsulados con D3D11 para cada uno de ellos. El estado de entrada utilizado debe ser la última manera en que D3D12 lo usó (por ejemplo, destino de representación \_ ) y el estado de salida debe ser la manera en que D3D12 lo usará una vez finalizada la D3D11 (por ejemplo, presente).
-   Inicialice D2D y proporcione los recursos encapsulados D3D11 a D2D para prepararse para la representación.

A continuación, en cada fotograma, haga lo siguiente:

-   Se representa en el búfer de retroceso de la cadena de intercambio actual mediante una lista de comandos de D3D12 y se ejecuta.
-   Adquirir el recurso encapsulado del búfer de retroceso actual ([**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)).
-   Emita comandos de representación de D2D.
-   Libere el recurso encapsulado ([**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)).
-   Vacíe el contexto inmediato de D3D11.
-   Presente ([**IDXGISwapChain1::P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)).

## <a name="background"></a>Información previa

D3D11On12 funciona sistemáticamente. Cada llamada de API de D3D11 pasa por la validación de tiempo de ejecución típica y hace que sea el controlador. En el nivel de controlador, el controlador 11on12 especial registra el estado y emite las operaciones de representación en las listas de comandos de D3D12. Estas listas de comandos se envían según sea necesario (por ejemplo, una consulta `GetData` o un recurso `Map` podrían requerir que se vacíen los comandos) o como lo solicitó el vaciado. La creación de un objeto D3D11 suele tener como resultado el objeto D3D12 correspondiente que se va a crear. Algunas operaciones de representación de funciones fijas en D3D11 como `GenerateMips` o `DrawAuto` no se admiten en D3D12, por lo que D3D11On12 las emula mediante sombreadores y recursos adicionales.

Para la interoperabilidad, es importante comprender cómo interactúa D3D11On12 con los objetos D3D12 que la aplicación ha creado y proporcionado. Para asegurarse de que el trabajo ocurre en el orden correcto, se debe vaciar el contexto inmediato de D3D11 antes de que se pueda enviar trabajo de D3D12 adicional a esa cola. También es importante asegurarse de que la cola proporcionada a D3D11On12 debe ser drenada en todo momento. Esto significa que, al final, se deben satisfacer todas las esperas de la cola, aunque el subproceso de representación D3D11 se bloquee indefinidamente. Tenga cuidado de no tomar una dependencia en el momento en que D3D11On12 inserta vaciados o esperas, ya que esto puede cambiar con versiones futuras. Además, D3D11On12 realiza un seguimiento de los Estados de los recursos y los manipula por sí solos. La única manera de garantizar la coherencia de las transiciones de estado consiste en usar las API de adquisición y versión para manipular el seguimiento de estado para satisfacer las necesidades de la aplicación.

## <a name="cleaning-up"></a>Limpiar

Para liberar un recurso encapsulado de D3D11On12, es necesario que se produzcan dos cosas en este orden:

-   Todas las referencias al recurso, incluidas las vistas del recurso, deben liberarse.
-   El procesamiento diferido de la destrucción debe realizarse. La manera más sencilla de asegurarse de esto es invocar la API de contexto inmediata `Flush` .

Una vez completados los dos pasos, se debe liberar cualquier referencia tomada por el recurso encapsulado y el recurso D3D12 se convierte exclusivamente en propiedad del componente D3D12. Tenga en cuenta que D3D12 todavía requiere esperar la finalización de la GPU antes de liberar un recurso por completo, por lo que debe asegurarse de mantener una referencia en el recurso antes de realizar los dos pasos anteriores, a menos que ya haya confirmado que la GPU ya no usa el recurso.

Todos los demás recursos u objetos creados por D3D11On12 se limpiarán en el momento adecuado, cuando la GPU haya terminado de usarlos, mediante el mecanismo de destrucción diferida de D3D11's. Sin embargo, si intenta liberar el propio dispositivo D3D11On12 mientras la GPU todavía se está ejecutando, la destrucción puede bloquearse hasta que se complete la GPU.

## <a name="limitations"></a>Limitaciones

El nivel D3D11On12 implementa un subconjunto muy grande de la API D3D11, pero hay algunos huecos conocidos (además de errores en la implementación que pueden causar una representación incorrecta).

A partir de Windows 10, versión 1809 (10,0; Compilación 17763), siempre que D3D11On12 se ejecute en un controlador compatible con el modelo de sombreador 6,0 o posterior, puede ejecutar los sombreadores que usan las interfaces. En versiones anteriores de Windows, la característica de interfaces de sombreador no se implementa en D3D11On12 y, si se intenta usar la característica, se producirán errores y los mensajes de depuración.

A partir de Windows 10, versión 1803 (10,0; Compilación 17134), se admiten cadenas de intercambio en dispositivos D3D11On12. En versiones anteriores de Windows, no lo son.

D3D11On12 no se ha optimizado para el rendimiento. Probablemente habrá una sobrecarga moderada de la CPU en comparación con un controlador D3D11 estándar, una sobrecarga mínima de la GPU y se sabe que la sobrecarga de memoria es significativa. Por lo tanto, no se recomienda usar D3D11On12 para escenas 3D complicadas y, en su lugar, se recomienda para escenas simples o para la representación en 2D.

## <a name="apis"></a>API

Las API que componen el nivel 11on12 se describen en [referencia de 11on12](direct3d-11on12-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[D2D con el tutorial de D3D11on12](d2d-using-d3d11on12.md)
</dt> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Trabajar con Direct3D 11, Direct3D 10 y Direct2D](direct3d-12-interop.md)
</dt> </dl>

 

 
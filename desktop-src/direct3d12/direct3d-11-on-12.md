---
title: Direct3D 11 en 12
description: D3D11On12 es un mecanismo por el que los desarrolladores pueden usar interfaces y objetos D3D11 para impulsar la API D3D12.
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62816ea0d7d7969cd56e0a9f525b2c412c8da182
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249177"
---
# <a name="direct3d-11-on-12"></a>Direct3D 11 en 12

D3D11On12 es un mecanismo por el que los desarrolladores pueden usar interfaces y objetos D3D11 para impulsar la API D3D12. D3D11on12 permite que los componentes escritos mediante D3D11 (por ejemplo, texto D2D e interfaz de usuario) funcionen junto con componentes escritos que tienen como destino la API D3D12. D3D11on12 también permite la porción incremental de una aplicación de D3D11 a D3D12, al permitir que las partes de la aplicación sigan teniendo como destino D3D11 por motivos de simplicidad, mientras que otras tienen como destino D3D12 para el rendimiento, mientras que siempre tienen una representación completa y correcta. D3D11On12 simplifica el uso de técnicas de interoperabilidad para compartir recursos y sincronizar el trabajo entre las dos API.

-   [Inicialización de D3D11On12](#initializing-d3d11on12)
-   [Uso de ejemplo](#example-usage)
-   [Información preliminar](#background)
-   [Limpiar](#cleaning-up)
-   [Limitaciones](#limitations)
-   [API](#apis)
-   [Temas relacionados](#related-topics)

## <a name="initializing-d3d11on12"></a>Inicialización de D3D11On12

Para empezar a usar D3D11On12, el primer paso es crear un dispositivo D3D12 y una cola de comandos. Estos objetos se proporcionan como entrada al método de inicialización [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). Puede pensar en este método como crear un dispositivo D3D11 con el tipo de controlador imaginario D3D \_ DRIVER \_ TYPE 11ON12, donde el controlador D3D11 es responsable de crear objetos y enviar listas de comandos a la \_ API D3D12.

Después de tener un dispositivo D3D11 y un contexto inmediato, puede desactivarlo para la interfaz `QueryInterface` [**ID3D11On12Device.**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) Esta es la interfaz principal que se usa para la interoperabilidad entre D3D11 y D3D12. Para que tanto el contexto de dispositivo D3D11 como las listas de comandos D3D12 funcionen en los mismos recursos, es necesario crear "recursos encapsulados" mediante la API [**CreateWrappedResource.**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) Este método "promueve" un recurso D3D12 para que sea comprensible en D3D11. Un recurso encapsulado se inicia en el estado "adquirido", una propiedad manipulada por los [**métodos AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) y [**ReleaseWrappedResources.**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)

## <a name="example-usage"></a>Ejemplo de uso

El uso típico de D3D11On12 sería usar D2D para representar texto o imágenes sobre un búfer de reserva D3D12. Consulte el ejemplo D3D11On12 para obtener código de ejemplo. Este es un esquema aproximado de los pasos que debe seguir para hacerlo:

-   Cree un dispositivo D3D12 [**(D3D12CreateDevice)**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)y una cadena de intercambio D3D12 [**(CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) con [**un ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) como entrada).
-   Cree un dispositivo D3D11On12 con el dispositivo D3D12 y la misma cola de comandos que la entrada.
-   Recupere los búferes de reserva de la cadena de intercambio y cree recursos encapsulados D3D11 para cada uno de ellos. El estado de entrada usado debe ser la última manera en que D3D12 lo usó (por ejemplo, RENDER TARGET) y el estado de salida debe ser la manera en que D3D12 lo usará una vez que D3D11 haya finalizado (por ejemplo, \_ PRESENT).
-   Inicialice D2D y proporcione los recursos encapsulados D3D11 a D2D para prepararse para la representación.

A continuación, en cada fotograma, haga lo siguiente:

-   Represente en el búfer de reserva de la cadena de intercambio actual mediante una lista de comandos D3D12 y ejecáquelo.
-   Adquiera el recurso encapsulado del búfer de reserva actual ([**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)).
-   Emita comandos de representación D2D.
-   Libere el recurso encapsulado ([**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)).
-   Vacíe el contexto inmediato D3D11.
-   Present ([**IDXGISwapChain1::P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)).

## <a name="background"></a>Fondo

D3D11On12 funciona sistemáticamente. Cada llamada API D3D11 pasa por la validación típica en tiempo de ejecución y llega al controlador. En el nivel de controlador, el controlador especial 11on12 registra el estado y los problemas representan las operaciones en las listas de comandos D3D12. Estas listas de comandos se envían según sea necesario (por ejemplo, una consulta o recurso puede requerir que se vacíe el comando) o según `GetData` `Map` lo solicitado por Flush. La creación de un objeto D3D11 normalmente da como resultado la creación del objeto D3D12 correspondiente. Algunas operaciones de representación de funciones fijas en D3D11 como o no se admiten en D3D12, por lo que `GenerateMips` D3D11On12 las emula mediante sombreadores y recursos `DrawAuto` adicionales.

Para la interoperabilidad, es importante comprender cómo D3D11On12 interactúa con los objetos D3D12 que la aplicación ha creado y proporcionado. Para asegurarse de que el trabajo se produce en el orden correcto, el contexto inmediato D3D11 debe vaciarse antes de que se pueda enviar trabajo adicional D3D12 a esa cola. También es importante asegurarse de que la cola dada a D3D11On12 debe ser purgable en todo momento. Esto significa que las esperas en la cola se deben satisfacer finalmente, incluso si D3D11 representa los bloques de subproceso indefinidamente. Tenga cuidado de no tomar una dependencia cuando D3D11On12 inserte vaciados o esperas, ya que esto puede cambiar con futuras versiones. Además, D3D11On12 realiza un seguimiento y manipula los estados de recursos por sí mismo. La única manera de garantizar la coherencia de las transiciones de estado es usar las API de adquisición/versión para manipular el seguimiento de estado para satisfacer las necesidades de la aplicación.

## <a name="cleaning-up"></a>Limpiar

Para liberar un recurso encapsulado D3D11On12, deben ocurrir dos cosas en este orden:

-   Todas las referencias al recurso, incluidas las vistas del recurso, deben liberarse.
-   Debe realizarse el procesamiento de destrucción diferida. La manera más sencilla de asegurarse de que esto sucede es invocar la API de contexto `Flush` inmediato.

Una vez completados ambos pasos, se deben liberar las referencias realizadas por el recurso encapsulado y el recurso D3D12 pasa a ser propiedad exclusiva del componente D3D12. Tenga en cuenta que D3D12 todavía requiere esperar a la finalización de GPU antes de liberar completamente un recurso, así que asegúrese de contener una referencia en el recurso antes de realizar los dos pasos anteriores, a menos que ya haya confirmado que la GPU ya no usa el recurso.

Todos los demás recursos u objetos creados por D3D11On12 se limpiarán en el momento adecuado, cuando la GPU haya terminado de usarlos, mediante el mecanismo de destrucción diferida de D3D11. Sin embargo, si intenta liberar el propio dispositivo D3D11On12 mientras la GPU todavía se está ejecutando, la destrucción puede bloquearse hasta que se complete la GPU.

## <a name="limitations"></a>Limitaciones

La capa D3D11On12 implementa un subconjunto muy grande de la API D3D11, pero hay algunas lagunas conocidas (además de errores en la implementación que pueden provocar una representación incorrecta).

A partir Windows 10, versión 1809 (10.0; Compilación 17763), siempre y cuando D3D11On12 se ejecute en un controlador que admita El modelo de sombreador 6.0 o posterior, puede ejecutar sombreadores que usen interfaces. En versiones anteriores de Windows, la característica de interfaces de sombreador no se implementa en D3D11On12 y el intento de usar la característica provocará errores y mensajes de depuración.

A partir Windows 10, versión 1803 (10.0; Compilación 17134), las cadenas de intercambio se admiten en dispositivos D3D11On12. En versiones anteriores de Windows, no lo son.

D3D11On12 no se ha optimizado para el rendimiento. Probablemente habrá una sobrecarga de CPU moderada en comparación con un controlador D3D11 estándar, una sobrecarga de GPU mínima y se sabe que hay una sobrecarga de memoria significativa. Por lo tanto, no se recomienda usar D3D11On12 para escenas 3D complicadas y, en su lugar, se recomienda para escenas simples o representación en 2D.

## <a name="apis"></a>API existentes

Las API que son la capa 11on12 se describen en [11on12 Reference (Referencia de 11on12).](direct3d-11on12-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recorrido por D2D con D3D11on12](d2d-using-d3d11on12.md)
</dt> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Trabajar con Direct3D 11, Direct3D 10 y Direct2D](direct3d-12-interop.md)
</dt> </dl>

 

 
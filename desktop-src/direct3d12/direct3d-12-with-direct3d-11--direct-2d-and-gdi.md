---
title: Interoperabilidad de Direct3D 12
description: D3D12 se puede usar para escribir aplicaciones en componentes.
ms.assetid: 51F7E715-82B6-48D8-A06A-CBBEDF6968F5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b5fcfe2adf756c12f034031675d0c3ac5571b44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549180"
---
# <a name="direct3d-12-interop"></a>Interoperabilidad de Direct3D 12

D3D12 se puede usar para escribir aplicaciones en componentes.

-   [Información general sobre interoperabilidad](#interop-overview)
-   [Razones para utilizar la interoperabilidad](#reasons-for-using-interop)
    -   [Compartir una lista de comandos](#sharing-a-command-list)
    -   [Compartir una cola de comandos](#sharing-a-command-queue)
    -   [Uso compartido de primitivas de sincronización](#sharing-sync-primitives)
    -   [Uso compartido de recursos](#sharing-resources)
    -   [Elegir un modelo de interoperabilidad](#choosing-an-interop-model)
-   [API de interoperabilidad](#interop-apis)
-   [Temas relacionados](#related-topics)

## <a name="interop-overview"></a>Información general sobre interoperabilidad

D3D12 puede ser muy eficaz y permitir que las aplicaciones escriban código gráfico con eficacia similar a la consola, pero no todas las aplicaciones deben reinventar la rueda y escribir la totalidad de su motor de representación desde cero. En algunos casos, otro componente o biblioteca ya lo ha hecho mejor, o en otros casos, el rendimiento de una parte del código no es tan importante como su corrección y legibilidad.

En esta sección se tratan las técnicas de interoperabilidad siguientes:

-   D3D12 y D3D12 en el mismo dispositivo
-   D3D12 y D3D12 en dispositivos diferentes
-   D3D12 y cualquier combinación de D3D11, D3D10 o D2D en el mismo dispositivo
-   D3D12 y cualquier combinación de D3D11, D3D10 o D2D en distintos dispositivos
-   D3D12 y GDI, o D3D12 y D3D11 y GDI

## <a name="reasons-for-using-interop"></a>Razones para utilizar la interoperabilidad

Hay varios motivos por los que una aplicación desearía D3D12 Interop con otras API. He aquí algunos ejemplos:

-   Portabilidad incremental: desea migrar una aplicación completa de D3D10 o D3D11 a D3D12, mientras que es funcional en fases intermedias del proceso de portabilidad (para habilitar las pruebas y la depuración).
-   Código de caja negra: se desea dejar una parte determinada de una aplicación tal cual al trasladar el resto del código. Por ejemplo, puede que no sea necesario migrar los elementos de la interfaz de usuario de un juego.
-   Componentes no modificables: necesidad de usar componentes que no pertenecen a la aplicación, que no se escriben en el destino D3D12.
-   Un nuevo componente: no quiere trasladar toda la aplicación, pero desea utilizar un nuevo componente que se escribe mediante D3D12.

Hay cuatro técnicas principales para la interoperabilidad en D3D12:

-   Una aplicación puede elegir proporcionar una lista de comandos abierta a un componente, que registra algunos comandos de representación adicionales en un destino de representación ya enlazado. Esto es equivalente a proporcionar un contexto de dispositivo preparado a otro componente en D3D11 y es ideal para cosas como agregar la interfaz de usuario o el texto a un búfer de reserva ya delimitado.
-   Una aplicación puede elegir proporcionar una cola de comandos a un componente, junto con un recurso de destino deseado. Esto es equivalente a usar las API de [**ClearState**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate) o [**DeviceContextState**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate) en D3D11 para proporcionar un contexto de dispositivo limpio a otro componente. Así es como funcionan los componentes como D2D.
-   Un componente puede optar por un modelo en el que se genera una lista de comandos, potencialmente en paralelo, que la aplicación es responsable de su envío en otro momento. Se debe proporcionar al menos un recurso a través de los límites de los componentes. Esta misma técnica está disponible en D3D11 con contextos aplazados, aunque el rendimiento de D3D12 es más conveniente.
-   Cada componente tiene sus propias colas y dispositivos, y la aplicación y los componentes deben compartir los recursos y la información de sincronización a través de los límites de los componentes. Esto es similar al heredado `ISurfaceQueue` y al [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex)más moderno.

Las diferencias entre estos escenarios son lo que se comparte exactamente entre los límites del componente. Se supone que el dispositivo está compartido, pero, dado que básicamente es sin estado, no es realmente relevante. Los objetos de clave son la lista de comandos, la cola de comandos, los objetos de sincronización y los recursos. Cada una de ellas tiene sus propias complicaciones al compartirlas.

### <a name="sharing-a-command-list"></a>Compartir una lista de comandos

El método más sencillo de interoperabilidad requiere compartir solo una lista de comandos con una parte del motor. Una vez completadas las operaciones de representación, la propiedad de la lista de comandos vuelve al autor de la llamada. Se puede realizar un seguimiento de la propiedad de la lista de comandos a través de la pila. Dado que las listas de comandos tienen un único subproceso, no hay ninguna manera de que una aplicación haga algo único o innovador con esta técnica.

### <a name="sharing-a-command-queue"></a>Compartir una cola de comandos

Probablemente, la técnica más común para varios componentes que comparten un dispositivo en el mismo proceso.

Cuando la cola de comandos es la unidad de uso compartido, debe haber una llamada al componente para que sepa que todas las listas de comandos pendientes deben enviarse inmediatamente a la cola de comandos (y se deben sincronizar las colas de comandos internas). Esto es equivalente a la API de [**vaciado**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) de D3D11 y es la única manera en que la aplicación puede enviar sus propias listas de comandos o sincronizar primitivas.

### <a name="sharing-sync-primitives"></a>Uso compartido de primitivas de sincronización

El patrón esperado para un componente que opera en sus propios dispositivos y/o colas de comandos será aceptar un [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) o un identificador compartido, y un par UInt64 al comenzar su trabajo, en el que se esperará y, a continuación, un segundo ID3D12Fence o identificador compartido, y un par UInt64 que señalará cuando se complete todo el trabajo. Este patrón coincide con la implementación actual de [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex) y el diseño de sincronización de los modelos de relanzamiento de DWM/DXGI.

### <a name="sharing-resources"></a>Uso compartido de recursos

Por el momento, la parte más complicada de escribir una aplicación de D3D12 que aprovecha varios componentes es cómo tratar los recursos que se comparten entre los límites de los componentes. Esto se debe principalmente al concepto de Estados de los recursos. Aunque algunos aspectos del diseño de estado de los recursos están diseñados para tratar la sincronización de la lista de comandos, otros tienen efecto entre las listas de comandos, que afectan al diseño de recursos y a conjuntos válidos de operaciones o características de rendimiento de acceso a los datos de recursos.

Hay dos patrones de tratar con esta complicación, que implican esencialmente un contrato entre los componentes.

-   El contrato puede ser definido por el desarrollador de componentes y documentado. Esto puede ser tan sencillo como "el recurso debe estar en el estado predeterminado cuando se inicia el trabajo y se volverá a poner en el estado predeterminado cuando se realice el trabajo" o podría tener reglas más complicadas para permitir elementos como el uso compartido de un búfer de profundidad sin forzar la resolución de la profundidad intermedia.
-   La aplicación puede definir el contrato en tiempo de ejecución, en el momento en que el recurso se comparte entre los límites de los componentes. Consta de los mismos dos fragmentos de información: el estado en el que estará el recurso cuando el componente empiece a usarlo y el estado en el que el componente debe dejarlo cuando finalice.

### <a name="choosing-an-interop-model"></a>Elegir un modelo de interoperabilidad

Para la mayoría de las aplicaciones D3D12, compartir una cola de comandos es probablemente el modelo ideal. Permite la propiedad completa de la creación y el envío del trabajo, sin la sobrecarga de memoria adicional que supone tener colas redundantes y sin el impacto en el rendimiento de tratar con los primitivos de sincronización de GPU.

El uso compartido de primitivas de sincronización es necesario una vez que los componentes deben tratar las distintas propiedades de la cola, como el tipo o la prioridad, o una vez que el uso compartido debe abarcar los límites del proceso.

Los componentes de terceros no usan ampliamente el uso compartido o la generación de listas de comandos, pero pueden usarse ampliamente en componentes que son internos de un motor de juegos.

## <a name="interop-apis"></a>API de interoperabilidad

El tema [Direct3D 11 en 12](./direct3d-11-on-12.md) le guía por el uso de gran parte de la superficie de API relacionada con los tipos de interoperación descritos en este tema.

Vea también el método [ID3D12Device:: CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle) , que puede usar para compartir las superficies entre las API de gráficos de Windows.

## <a name="related-topics"></a>Temas relacionados

* [Descripción de Direct3D 12](directx-12-getting-started.md)
* [Trabajar con Direct3D 11, Direct3D 10 y Direct2D](direct3d-12-interop.md)
* [Direct3D 11 en 12](./direct3d-11-on-12.md)
---
title: Interoperabilidad de Direct3D 12
description: D3D12 se puede usar para escribir aplicaciones con componentes.
ms.assetid: 51F7E715-82B6-48D8-A06A-CBBEDF6968F5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b5fcfe2adf756c12f034031675d0c3ac5571b44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466341"
---
# <a name="direct3d-12-interop"></a>Interoperabilidad de Direct3D 12

D3D12 se puede usar para escribir aplicaciones con componentes.

-   [Información general sobre interoperabilidad](#interop-overview)
-   [Motivos para usar la interoperabilidad](#reasons-for-using-interop)
    -   [Uso compartido de una lista de comandos](#sharing-a-command-list)
    -   [Uso compartido de una cola de comandos](#sharing-a-command-queue)
    -   [Uso compartido de primitivas de sincronización](#sharing-sync-primitives)
    -   [Uso compartido de recursos](#sharing-resources)
    -   [Elección de un modelo de interoperabilidad](#choosing-an-interop-model)
-   [API de interoperabilidad](#interop-apis)
-   [Temas relacionados](#related-topics)

## <a name="interop-overview"></a>Información general sobre interoperabilidad

D3D12 puede ser muy eficaz y permitir que las aplicaciones escriban código gráfico con eficacia como consola, pero no todas las aplicaciones necesitan volver a inventar la rueda y escribir la totalidad de su motor de representación desde cero. En algunos casos, otro componente o biblioteca ya lo ha hecho mejor o, en otros casos, el rendimiento de una parte del código no es tan crítico como su corrección y legibilidad.

En esta sección se tratan las siguientes técnicas de interoperabilidad:

-   D3D12 y D3D12, en el mismo dispositivo
-   D3D12 y D3D12, en dispositivos diferentes
-   D3D12 y cualquier combinación de D3D11, D3D10 o D2D en el mismo dispositivo
-   D3D12 y cualquier combinación de D3D11, D3D10 o D2D en distintos dispositivos
-   D3D12 y GDI, o D3D12 y D3D11 y GDI

## <a name="reasons-for-using-interop"></a>Motivos para usar la interoperabilidad

Hay varias razones por las que una aplicación desea la interoperabilidad D3D12 con otras API. He aquí algunos ejemplos:

-   Portabilidad incremental: quiere portabilidad de una aplicación completa de D3D10 o D3D11 a D3D12, mientras funciona en fases intermedias del proceso de portabilidad (para habilitar las pruebas y la depuración).
-   Código de caja negra: quiere dejar una parte determinada de una aplicación tal y como está mientras se porte el resto del código. Por ejemplo, es posible que no sea necesario portabilidad de elementos de interfaz de usuario de un juego.
-   Componentes que no se pueden cambiar: es necesario usar componentes que no son propiedad de la aplicación, que no se escriben en D3D12 de destino.
-   Un nuevo componente: no quiere portabilidad de toda la aplicación, sino que quiere usar un nuevo componente que se escribe mediante D3D12.

Hay cuatro técnicas principales para la interoperabilidad en D3D12:

-   Una aplicación puede optar por proporcionar una lista de comandos abierta a un componente, que registra algunos comandos de representación adicionales en un destino de representación ya enlazado. Esto equivale a proporcionar un contexto de dispositivo preparado a otro componente en D3D11 y es excelente para cosas como agregar la interfaz de usuario o el texto a un búfer de reserva ya enlazado.
-   Una aplicación puede optar por proporcionar una cola de comandos a un componente, junto con un recurso de destino deseado. Esto equivale al uso de las API [**ClearState**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate) o [**DeviceContextState**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate) en D3D11 para proporcionar un contexto de dispositivo limpio a otro componente. Así es como funcionan componentes como D2D.
-   Un componente puede optar por un modelo en el que genera una lista de comandos, posiblemente en paralelo, de la que la aplicación es responsable del envío más adelante. Se debe proporcionar al menos un recurso a través de los límites del componente. Esta misma técnica está disponible en D3D11 mediante contextos diferidos, aunque el rendimiento de D3D12 es más deseable.
-   Cada componente tiene sus propias colas o dispositivos, y la aplicación y los componentes deben compartir recursos e información de sincronización a través de los límites de los componentes. Esto es similar al heredado y al `ISurfaceQueue` [**IDXGIKeyedMutex más moderno.**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex)

Las diferencias entre estos escenarios es lo que se comparte exactamente entre los límites del componente. Se supone que el dispositivo se comparte, pero como básicamente no tiene estado, no es realmente relevante. Los objetos clave son la lista de comandos, la cola de comandos, los objetos de sincronización y los recursos. Cada una de ellas tiene sus propias complicaciones al compartirlas.

### <a name="sharing-a-command-list"></a>Uso compartido de una lista de comandos

El método más sencillo de interoperabilidad requiere compartir solo una lista de comandos con una parte del motor. Una vez completadas las operaciones de representación, la propiedad de la lista de comandos vuelve al autor de la llamada. La propiedad de la lista de comandos se puede realizar a través de la pila. Puesto que las listas de comandos son de un solo subproceso, no hay ninguna manera de que una aplicación haga algo único o innovador mediante esta técnica.

### <a name="sharing-a-command-queue"></a>Uso compartido de una cola de comandos

Probablemente la técnica más común para varios componentes que comparten un dispositivo en el mismo proceso.

Cuando la cola de comandos es la unidad de uso compartido, debe haber una llamada al componente para que sepa que todas las listas de comandos pendientes deben enviarse inmediatamente a la cola de comandos (y las colas de comandos internas deben sincronizarse). Esto equivale a la [**API**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) de vaciado D3D11 y es la única manera en que la aplicación puede enviar sus propias listas de comandos o sincronizar primitivas.

### <a name="sharing-sync-primitives"></a>Uso compartido de primitivas de sincronización

El patrón esperado para un componente que opera en sus propios dispositivos o colas de comandos será aceptar un [**identificador ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) o compartido, y un par UINT64 al comenzar su trabajo, que esperará, y un segundo identificador ID3D12Fence o compartido, y un par UINT64 que señalará cuando se complete todo el trabajo. Este patrón coincide con la implementación actual de [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex) y el diseño de sincronización del modelo de volteo DWM/DXGI.

### <a name="sharing-resources"></a>Uso compartido de recursos

Con diferencia, la parte más complicada de escribir una aplicación D3D12 que aprovecha varios componentes es cómo tratar con los recursos que se comparten entre los límites de los componentes. Esto se debe principalmente al concepto de estados de recursos. Aunque algunos aspectos del diseño del estado de los recursos están diseñados para tratar la sincronización entre listas de comandos, otros tienen impacto entre las listas de comandos, lo que afecta al diseño de recursos y a conjuntos válidos de operaciones o características de rendimiento del acceso a los datos de recursos.

Hay dos patrones de tratamiento de esta complicación, que implican básicamente un contrato entre componentes.

-   El desarrollador del componente puede definir el contrato y documentarlo. Esto podría ser tan sencillo como "el recurso debe estar en el estado predeterminado cuando se inicia el trabajo y se volverá a colocar en el estado predeterminado cuando se realiza el trabajo" o podría tener reglas más complicadas para permitir cosas como compartir un búfer de profundidad sin forzar la resolución de profundidad intermedia.
-   La aplicación puede definir el contrato en tiempo de ejecución, en el momento en que el recurso se comparte entre los límites del componente. Consta de los mismos dos fragmentos de información: el estado en el que se encontrará el recurso cuando el componente empiece a usarlo y el estado en el que el componente debe dejarlo cuando finalice.

### <a name="choosing-an-interop-model"></a>Elección de un modelo de interoperabilidad

Para la mayoría de las aplicaciones D3D12, el modelo ideal es compartir una cola de comandos. Permite la propiedad completa de la creación y el envío del trabajo, sin la sobrecarga de memoria adicional de tener colas redundantes y sin el impacto de rendimiento de trabajar con las primitivas de sincronización de GPU.

El uso compartido de primitivas de sincronización es necesario una vez que los componentes tienen que tratar con diferentes propiedades de cola, como tipo o prioridad, o una vez que el uso compartido debe abarcar los límites del proceso.

El uso compartido o la generación de listas de comandos no son ampliamente utilizados externamente por componentes de terceros, pero pueden usarse ampliamente en componentes que son internos de un motor de juego.

## <a name="interop-apis"></a>API de interoperabilidad

El [tema Direct3D 11 on 12](./direct3d-11-on-12.md) le guía a través del uso de gran parte de la superficie de API relacionada con los tipos de interoperación que se describen en este tema.

Vea también el [método ID3D12Device::CreateSharedHandle,](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle) que puede usar para compartir superficies entre Windows API de gráficos.

## <a name="related-topics"></a>Temas relacionados

* [Descripción de Direct3D 12](directx-12-getting-started.md)
* [Trabajar con Direct3D 11, Direct3D 10 y Direct2D](direct3d-12-interop.md)
* [Direct3D 11 en 12](./direct3d-11-on-12.md)
---
title: Aplicaciones Direct2D multiproceso
description: Describe los procedimientos recomendados para crear aplicaciones de Direct2D multiproceso.
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be979b867edd6d36583959c4a595dbd507ca94f
ms.sourcegitcommit: c3243ec4ada05b7faf9d563853cb667ecef825e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "103797242"
---
# <a name="multithreaded-direct2d-apps"></a>Aplicaciones Direct2D multiproceso

Si desarrolla aplicaciones de [direct2d](./direct2d-portal.md) , puede que necesite acceder a los recursos de direct2d desde más de un subproceso. En otros casos, puede que desee usar multithreading para obtener un mejor rendimiento o una mejor capacidad de respuesta (como usar un subproceso para la presentación en pantalla y un subproceso independiente para la representación sin conexión).

En este tema se describen los procedimientos recomendados para desarrollar aplicaciones de [Direct2D](./direct2d-portal.md) multiproceso con poca o ninguna representación de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) . Puede ser difícil realizar un seguimiento de los defectos de software causados por problemas de simultaneidad y resulta útil planear la Directiva de multithreading y seguir las prácticas recomendadas que se describen aquí.

> [!Note]  
> Si tiene acceso a dos recursos de [direct2d](./direct2d-portal.md) creados a partir de dos generadores de direct2d de un solo subproceso, no se producirán conflictos de acceso, siempre que los dispositivos [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) subyacentes y los contextos de dispositivo sean también distintos. Al hablar sobre el "acceso a los recursos de Direct2D" en este artículo, en realidad se entiende el acceso a los recursos de Direct2D creados desde el mismo dispositivo Direct2D, a menos que se indique lo contrario.

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>Desarrollo de aplicaciones Thread-Safe que solo llaman a las API de Direct2D

Puede crear una instancia del generador de [Direct2D](./direct2d-portal.md) multiproceso. Puede usar y compartir un generador multiproceso y todos sus recursos de más de un subproceso, pero los accesos a esos recursos (a través de llamadas de Direct2D) se serializan mediante Direct2D, por lo que no se producen conflictos de acceso. Si la aplicación solo llama a las API de Direct2D, Direct2D realiza automáticamente esta protección en un nivel granular con una sobrecarga mínima. Aquí se muestra el código para crear un generador multiproceso.

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

En la imagen siguiente se muestra cómo [Direct2D](./direct2d-portal.md) serializa dos subprocesos que realizan llamadas solo mediante la API de direct2d.

![diagrama de dos subprocesos serializados.](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>Desarrollo de aplicaciones Thread-Safe Direct2D con llamadas de Direct3D o DXGI mínimas

Es más de lo frecuente que una aplicación de [Direct2D](./direct2d-portal.md) también realiza algunas llamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI. Por ejemplo, un subproceso de presentación se dibujará en Direct2D y, a continuación, se presentará mediante una [**cadena de intercambio de DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

En este caso, garantizar la seguridad para subprocesos es más complicada: algunas llamadas a [Direct2D](./direct2d-portal.md) acceden indirectamente a los recursos de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) subyacentes, a los que otro subproceso llama a la vez a Direct3D o DXGI. Dado que esas llamadas de Direct3D o DXGI están fuera del reconocimiento y el control de Direct2d, tiene que crear un generador de Direct2D multiproceso, pero debe hacer MOR para evitar conflictos de acceso.

En el diagrama siguiente se muestra un conflicto de acceso a los recursos de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) debido a que el subproceso T0 tiene acceso indirectamente a un recurso a través de una llamada de [Direct2D](./direct2d-portal.md) y T2 accediendo al mismo recurso directamente a través de una llamada de Direct3D o DXGI.

> [!Note]  
> La protección de subprocesos que [Direct2D](./direct2d-portal.md) proporciona (el bloqueo azul de esta imagen) no ayuda en este caso.

 

![diagrama de la protección de subprocesos.](images/multi-thread2.png)

Para evitar el conflicto de acceso a los recursos aquí, se recomienda adquirir explícitamente el bloqueo que [Direct2D](./direct2d-portal.md) usa para la sincronización de acceso interno y aplicar ese bloqueo cuando un subproceso necesite realizar llamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI que puedan provocar conflictos de acceso, como se muestra aquí. En concreto, debe tener especial cuidado con el código que usa excepciones o un sistema de salida en tiempo de compilación basado en códigos de retorno HRESULT. Por esta razón, se recomienda usar un patrón RAII (adquisición de recursos) para llamar a los métodos [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) y [**leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) .

> [!Note]  
> Es importante que empareje las llamadas a los métodos [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) y [**leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) ; de lo contrario, la aplicación puede bloquearse.

 

En el código siguiente se muestra un ejemplo de Cuándo se deben bloquear y, a continuación, y desbloquearse en torno a llamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI.


```C++
void MyApp::DrawFromThread2()
{
    // We are accessing Direct3D resources directly without Direct2D's knowledge, so we
    // must manually acquire and apply the Direct2D factory lock.
    ID2D1Multithread* m_D2DMultithread;
    m_D2DFactory->QueryInterface(IID_PPV_ARGS(&m_D2DMultithread));
    m_D2DMultithread->Enter();
    
    // Now it is safe to make Direct3D/DXGI calls, such as IDXGISwapChain::Present
    MakeDirect3DCalls();

    // It is absolutely critical that the factory lock be released upon
    // exiting this function, or else any consequent Direct2D calls will be blocked.
    m_D2DMultithread->Leave();
}
```



> [!Note]  
> Algunas llamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI (especialmente [**IDXGISwapChain::P reenviados**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)) pueden adquirir bloqueos y/o desencadenadores de devoluciones de llamada en el código de la función o el método que realiza la llamada. Debe tener en cuenta esto y asegurarse de que este comportamiento no provoque interbloqueos. Para obtener más información, vea el tema [información general sobre DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) .

 

![diagrama de bloqueo de subprocesos de direct2d y Direct3D.](images/multi-thread3.png)

Cuando se usan los métodos [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) y [**leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) , las llamadas están protegidas por el [Direct2D](./direct2d-portal.md) automático y el bloqueo explícito, por lo que la aplicación no alcanza el conflicto de acceso.

Hay otros enfoques para solucionar este problema. Sin embargo, se recomienda que proteja explícitamente las llamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI con el bloqueo de [Direct2D](./direct2d-portal.md) porque normalmente proporciona un mejor rendimiento, ya que protege la simultaneidad en un nivel mucho más preciso y con una sobrecarga menor en direct2d Cover.

## <a name="ensuring-atomicity-of-stateful-operations"></a>Garantizar la atomicidad de las operaciones con estado

Aunque las características de seguridad para subprocesos de [DirectX](/previous-versions//ee663301(v=vs.85)) pueden ayudar a garantizar que no se realicen dos llamadas de API individuales simultáneamente, también debe asegurarse de que los subprocesos que realizan llamadas API con estado no interfieren entre sí. A continuación se muestra un ejemplo:

1.  Hay dos líneas de texto que se van a representar en la pantalla (por subproceso 0) y fuera de la pantalla (por subproceso 1): la línea \# 1 es "a es mayor" y \# la línea 2 es "a B", que se dibujarán con un pincel negro sólido.
2.  El subproceso 1 dibuja la primera línea de texto.
3.  El subproceso 0 reacciona a una entrada del usuario, actualiza las líneas de texto a "B es menor" y "a", respectivamente, y cambia el color del pincel a rojo sólido para su propio dibujo;
4.  El subproceso 1 continúa dibujando la segunda línea de texto, que ahora es "a", con el pincel de color rojo;
5.  Por último, obtenemos dos líneas de texto en el destino de dibujo fuera de la pantalla: "A es mayor" en negro y "a" en rojo.

![diagrama de subprocesos de pantalla en y sin conexión.](images/multi-thread4.png)

En la fila superior, el subproceso 0 dibuja con las cadenas de texto actuales y el pincel negro actual. El subproceso 1 solo finaliza el dibujo fuera de la pantalla en la mitad superior.

En la fila central, el subproceso 0 responde a la interacción del usuario, actualiza las cadenas de texto y el pincel y, a continuación, actualiza la pantalla. En este momento, el subproceso 1 está bloqueado. En la fila inferior, la representación fuera de la pantalla final después del subproceso 1 reanuda el dibujo de la mitad inferior con un pincel modificado y una cadena de texto alterada.

Para solucionar este problema, se recomienda tener un contexto independiente para cada subproceso, de modo que:

-   Debe crear una copia del contexto de dispositivo para que los recursos mutables (es decir, los recursos que pueden variar durante la presentación o la impresión, como el contenido de texto o el pincel de color sólido en el ejemplo) no cambien al presentar. En este ejemplo, debe mantener una copia de esas dos líneas de texto y el pincel de color antes de dibujar. Al hacerlo, garantiza que cada subproceso tiene contenido completo y coherente para dibujar y presentar.
-   Debe compartir recursos de gran peso (como mapas de bits y gráficos de efectos complejos) que se inicializan una vez y, después, no se modifican en los subprocesos para aumentar el rendimiento.
-   Puede compartir recursos ligeros (como los pinceles de color sólido y formatos de texto) que se inicializan una vez y, después, no se modifican a través de subprocesos o no

## <a name="summary"></a>Resumen

Al desarrollar aplicaciones de [direct2d](./direct2d-portal.md) multiproceso, debe crear un generador de direct2d multiproceso y, a continuación, derivar todos los recursos de direct2d de ese generador. Si un subproceso realiza llamadas [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o dxgi, también debe adquirir explícitamente el bloqueo de Direct2D para proteger esas llamadas de Direct3D o dxgi. Además, debe garantizar la integridad del contexto al tener una copia de los recursos mutables para cada subproceso.

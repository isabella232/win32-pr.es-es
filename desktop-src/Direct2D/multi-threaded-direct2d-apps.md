---
title: Aplicaciones Direct2D multiproceso
description: Describe los procedimientos recomendados para crear aplicaciones Direct2D multiproceso.
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be979b867edd6d36583959c4a595dbd507ca94f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162678"
---
# <a name="multithreaded-direct2d-apps"></a>Aplicaciones Direct2D multiproceso

Si desarrolla aplicaciones [de Direct2D,](./direct2d-portal.md) es posible que tenga que acceder a los recursos de Direct2D desde más de un subproceso. En otros casos, es posible que desee usar multiproceso para obtener un mejor rendimiento o una mejor capacidad de respuesta (por ejemplo, usar un subproceso para la presentación en pantalla y un subproceso independiente para la representación sin conexión).

En este tema se describen los procedimientos recomendados para desarrollar aplicaciones [Direct2D](./direct2d-portal.md) multiproceso con poca o ninguna [representación de Direct3D.](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) Los defectos de software causados por problemas de simultaneidad pueden ser difíciles de realizar y resulta útil planear la directiva multithreading y seguir los procedimientos recomendados que se describen aquí.

> [!Note]  
> Si accede a dos recursos de [Direct2D](./direct2d-portal.md) creados a partir de dos factorías de Direct2D de un solo subproceso diferentes, no se producirán conflictos de acceso, siempre y cuando los dispositivos y contextos de dispositivo de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) subyacentes también sean distintos. Al hablar de "acceso a recursos de Direct2D" en este artículo, significa realmente "acceder a los recursos de Direct2D creados desde el mismo dispositivo Direct2D", a menos que se indique lo contrario.

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>Desarrollo de Thread-Safe que llaman solo a las API de Direct2D

Puede crear una instancia de fábrica [de Direct2D](./direct2d-portal.md) multiproceso. Puede usar y compartir una fábrica multiproceso y todos sus recursos desde más de un subproceso, pero los accesos a esos recursos (a través de llamadas de Direct2D) se serializan mediante Direct2D, por lo que no se producen conflictos de acceso. Si la aplicación llama solo a las API de Direct2D, Dicha protección se realiza automáticamente mediante Direct2D en un nivel granular con una sobrecarga mínima. Código para crear un generador multiproceso aquí.

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

En la imagen siguiente se muestra [cómo Direct2D](./direct2d-portal.md) serializa dos subprocesos que hacen llamadas solo mediante la API de Direct2D.

![diagrama de dos subprocesos serializados.](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>Desarrollar aplicaciones Thread-Safe Direct2D con llamadas mínimas de Direct3D o DXGI

Es más que habitual que una [aplicación de Direct2D](./direct2d-portal.md) también haga algunas [llamadas a Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI. Por ejemplo, un subproceso de presentación se dibujará en Direct2D y, a continuación, se presentará mediante una [**cadena de intercambio DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

En este caso, garantizar la seguridad de subprocesos es más complicado: algunas llamadas de [Direct2D](./direct2d-portal.md) acceden indirectamente a los recursos subyacentes [de Direct3D,](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) a los que podría tener acceso simultáneamente otro subproceso que llama a Direct3D o DXGI. Dado que esas llamadas a Direct3D o DXGI están fuera del conocimiento y el control de Direct2D, debe crear una fábrica de Direct2D multiproceso, pero debe hacer lo mismo para evitar conflictos de acceso.

En el diagrama siguiente se muestra un conflicto de acceso a recursos [de Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) debido a que el subproceso T0 accede indirectamente a un recurso a través de una llamada a [Direct2D](./direct2d-portal.md) y T2 accede al mismo recurso directamente a través de una llamada a Direct3D o DXGI.

> [!Note]  
> La protección de subprocesos [que proporciona Direct2D](./direct2d-portal.md) (el bloqueo azul de esta imagen) no ayuda en este caso.

 

![diagrama de protección de subprocesos.](images/multi-thread2.png)

Para evitar conflictos de acceso a recursos aquí, se recomienda adquirir explícitamente el bloqueo que [Usa Direct2D](./direct2d-portal.md) para la sincronización de acceso interno y aplicar ese bloqueo cuando un subproceso necesite realizar llamadas [a Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI que puedan causar conflictos de acceso, como se muestra aquí. En concreto, debe tener especial cuidado con el código que usa excepciones o un sistema de salida anticipada basado en códigos de retorno HRESULT. Por este motivo, se recomienda usar un patrón RAII (Resource Acquisition Is Initialization) para llamar a los [**métodos Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) [**y Leave.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave)

> [!Note]  
> Es importante emparejar las llamadas a los métodos [**Entrar**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) y [**Salir;**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) de lo contrario, la aplicación puede interbloquear.

 

El código aquí muestra un ejemplo de cuándo bloquear y, a continuación, desbloquear las [llamadas direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI.


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
> Algunas [llamadas Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI (en particular [**IDXGISwapChain::P resent)**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)pueden adquirir bloqueos o desencadenar devoluciones de llamada en el código de la función o método de llamada. Debe tener en cuenta esto y asegurarse de que este comportamiento no provoca interbloqueos. Para obtener más información, vea el [tema Información general de DXGI.](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)

 

![Diagrama de bloqueo de subprocesos direct2d y direct3d.](images/multi-thread3.png)

Cuando se usan [](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) los [**métodos Entrar**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) y Salir, las llamadas están protegidas por [direct2D](./direct2d-portal.md) automático y el bloqueo explícito, por lo que la aplicación no entra en conflicto de acceso.

Hay otros enfoques para evitar este problema. Sin embargo, se recomienda proteger explícitamente las llamadas [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI con el bloqueo [de Direct2D,](./direct2d-portal.md) ya que normalmente proporciona un mejor rendimiento, ya que protege la simultaneidad en un nivel mucho más fino y con una sobrecarga menor bajo la cobertura de Direct2D.

## <a name="ensuring-atomicity-of-stateful-operations"></a>Garantizar la atomicidad de las operaciones con estado

Aunque las características de seguridad para subprocesos de [DirectX](/previous-versions//ee663301(v=vs.85)) pueden ayudar a garantizar que no se realicen dos llamadas API individuales simultáneamente, también debe asegurarse de que los subprocesos que realizan llamadas API con estado no interfieran entre sí. A continuación se muestra un ejemplo:

1.  Hay dos líneas de texto que desea representar en pantalla (por subproceso 0) y fuera de pantalla (por subproceso 1): la línea 1 es "A es mayor" y la línea 2 es \# "que B", ambas se dibujarán con un pincel negro \# sólido.
2.  El subproceso 1 dibuja la primera línea de texto.
3.  El subproceso 0 reacciona a una entrada del usuario, actualiza ambas líneas de texto a "B es más pequeño" y "que A", respectivamente, y cambia el color del pincel a rojo sólido para su propio dibujo;
4.  El subproceso 1 sigue dibujando la segunda línea de texto, que ahora es "que A", con el pincel de color rojo;
5.  Por último, se obtienen dos líneas de texto en el destino de dibujo fuera de la pantalla: "A es mayor" en negro y "que A" en rojo.

![diagrama de subprocesos de la pantalla de inicio y apagado.](images/multi-thread4.png)

En la fila superior, subproceso 0 dibuja con cadenas de texto actuales y el pincel negro actual. El subproceso 1 solo finaliza el dibujo fuera de la pantalla en la mitad superior.

En la fila central, el subproceso 0 responde a la interacción del usuario, actualiza las cadenas de texto y el pincel y, a continuación, actualiza la pantalla. En este momento, el subproceso 1 está bloqueado. En la fila inferior, la representación fuera de pantalla final después del subproceso 1 reanuda el dibujo de la mitad inferior con un pincel modificado y una cadena de texto modificada.

Para solucionar este problema, se recomienda tener un contexto independiente para cada subproceso, de modo que:

-   Debe crear una copia del contexto del dispositivo para que los recursos mutables (es decir, los recursos que pueden variar durante la presentación o impresión, como el contenido de texto o el pincel de color sólido del ejemplo) no cambien al representar. En este ejemplo, debe mantener una copia de esas dos líneas de texto y el pincel de color antes de dibujar. Al hacerlo, garantiza que cada subproceso tiene contenido completo y coherente para dibujar y presentar.
-   Debe compartir recursos de gran peso (como mapas de bits y gráficos de efectos complejos) que se inicializan una vez y, a continuación, nunca se modifican entre subprocesos para aumentar el rendimiento.
-   Puede compartir recursos ligeros (como pinceles de color sólido y formatos de texto) que se inicializan una vez y, a continuación, nunca se modifican entre subprocesos o no.

## <a name="summary"></a>Resumen

Al desarrollar aplicaciones [Direct2D](./direct2d-portal.md) multiproceso, debe crear una factoría direct2D multiproceso y, a continuación, derivar todos los recursos de Direct2D de esa factoría. Si un subproceso va a realizar llamadas a [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) o DXGI, también debe adquirir explícitamente y, a continuación, aplicar el bloqueo de Direct2D para proteger esas llamadas direct3D o DXGI. Además, debe garantizar la integridad del contexto al tener una copia de los recursos mutables para cada subproceso.

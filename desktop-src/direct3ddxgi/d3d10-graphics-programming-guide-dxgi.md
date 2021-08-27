---
description: En este tema se incluyen las siguientes secciones.
ms.assetid: 0522ccbf-e754-470a-8199-004fcbaa927d
title: Información general sobre DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 604787a1b3f747b9d33cc04e249128aede7b7a3e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626141"
---
# <a name="dxgi-overview"></a>Información general sobre DXGI

Microsoft Infraestructura de gráficos de DirectX (DXGI) reconoce que algunas partes de los gráficos evolucionan más lentamente que otras. El objetivo principal de DXGI es administrar tareas de bajo nivel que pueden ser independientes del entorno de ejecución de gráficos de DirectX. DXGI proporciona un marco común para futuros componentes gráficos. El primer componente que aprovecha las ventajas de DXGI es Microsoft Direct3D 10.

En versiones anteriores de Direct3D, las tareas de bajo nivel, como la enumeración de dispositivos de hardware, la presentación de fotogramas representados en una salida, el control de gamma y la administración de una transición a pantalla completa, se incluían en el entorno de ejecución de Direct3D. Estas tareas se implementan ahora en DXGI.

El propósito de DXGI es comunicarse con el controlador de modo kernel y el hardware del sistema, como se muestra en el diagrama siguiente.

![diagrama de la comunicación entre aplicaciones, dxgi y controladores y hardware](images/dxgi-dll.png)

Una aplicación puede acceder directamente a DXGI o llamar a las API de Direct3D en D3D11 \_ 1.h, D3D11.h, D3D10 1.h o D3D10.h, que controla las comunicaciones con \_ DXGI por usted. Es posible que quiera trabajar directamente con DXGI si la aplicación necesita enumerar dispositivos o controlar cómo se presentan los datos a una salida.

En este tema se incluyen las siguientes secciones.

-   [Enumeración de adaptadores](#enumerating-adapters)
    -   [Nueva información sobre la enumeración de adaptadores para Windows 8](#new-info-about-enumerating-adapters-for-windows-8)
-   [Presentación](#presentation)
    -   [Crear una cadena de intercambio](#create-a-swap-chain)
    -   [Cuidado y alimentación de la cadena de intercambio](#care-and-feeding-of-the-swap-chain)
    -   [Control del tamaño de ventana](#handling-window-resizing)
    -   [Elección de la salida y el tamaño de DXGI](#choosing-the-dxgi-output-and-size)
    -   [Depuración en modo Full-Screen depuración](#debugging-in-full-screen-mode)
    -   [Destruir una cadena de intercambio](#destroying-a-swap-chain)
    -   [Uso de un monitor girado](#using-a-rotated-monitor)
    -   [Cambiar modos](#switching-modes)
    -   [Sugerencia de rendimiento a pantalla completa](#full-screen-performance-tip)
    -   [Consideraciones sobre multiproceso](#multithread-considerations)
-   [Respuestas DXGI de DLLMain](#dxgi-responses-from-dllmain)
-   [Cambios de DXGI 1.1](#dxgi-11-changes)
-   [Cambios en DXGI 1.2](#dxgi-12-changes)
-   [Temas relacionados](#related-topics)

Para ver qué formatos son compatibles con el hardware de Direct3D 11:

-   [Compatibilidad con formato DXGI para hardware de nivel 12.1 de características de Direct3D](hardware-support-for-direct3d-12-1-formats.md)
-   [Compatibilidad con formato DXGI para hardware de nivel 12.0 de características de Direct3D](hardware-support-for-direct3d-12-0-formats.md)
-   [Compatibilidad con el formato DXGI para hardware de nivel 11.1 de características de Direct3D](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Compatibilidad con formato DXGI para hardware de nivel 11.0 de características de Direct3D](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Compatibilidad de hardware con formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Compatibilidad de hardware con formatos de Direct3D 10.1](/previous-versions//cc627091(v=vs.85))
-   [Compatibilidad de hardware con formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="enumerating-adapters"></a>Enumeración de adaptadores

Un adaptador es una abstracción del hardware y la funcionalidad de software del equipo. Por lo general, hay muchos adaptadores en la máquina. Algunos dispositivos se implementan en hardware (como la tarjeta de vídeo) y otros se implementan en software (como el rasterizador de referencia de Direct3D). Los adaptadores implementan la funcionalidad utilizada por una aplicación gráfica. En el diagrama siguiente se muestra un sistema con un solo equipo, dos adaptadores (tarjetas de vídeo) y tres monitores de salida.

![diagrama de un equipo con dos tarjetas de vídeo y tres monitores](images/dxgi-terms.png)

Al enumerar estos fragmentos de hardware, DXGI crea una interfaz [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) para cada salida (o monitor) y una interfaz [**IDXGIAdapter2**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2) para cada tarjeta de vídeo (incluso si se trata de una tarjeta de vídeo integrada en una placa base). La enumeración se realiza mediante una llamada de interfaz [**IDXGIFactory,**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) [**IDXGIFactory::EnumAdapters**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-enumadapters), para devolver un conjunto de interfaces [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) que representan el hardware de vídeo.

DXGI 1.1 agregó la [**interfaz IDXGIFactory1.**](/windows/win32/api/DXGI/nn-dxgi-idxgifactory1) [**IDXGIFactory1::EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) devuelve un conjunto de interfaces [**IDXGIAdapter1**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter1) que representa el hardware de vídeo.

Si desea seleccionar funcionalidades específicas de hardware de vídeo al usar las API de Direct3D, se recomienda llamar iterativamente a la función [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) con cada identificador de adaptador y el posible nivel de característica [de](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)hardware . Esta función se realiza correctamente si el adaptador especificado admite el nivel de característica.

### <a name="new-info-about-enumerating-adapters-for-windows-8"></a>Nueva información sobre la enumeración de adaptadores para Windows 8

A partir Windows 8, siempre está presente un adaptador denominado "Controlador de representación básica de Microsoft". Este adaptador tiene un VendorId **de 0x1414** y un DeviceID **de 0x8c**. Este adaptador también tiene el valor [**DXGI \_ ADAPTER FLAG \_ \_ SOFTWARE**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) establecido en el **miembro Flags** de su [**estructura \_ \_ DESC2 del ADAPTADOR DE DXGI.**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_adapter_desc2) Este adaptador es un dispositivo de solo representación que no tiene salidas de pantalla. DXGI nunca devuelve [**DXGI \_ ERROR DEVICE \_ \_ REMOVED**](dxgi-error.md) para este adaptador.

Si el controlador de pantalla de un equipo no funciona o está deshabilitado, el adaptador principal **(NULL)** del equipo también podría denominarse "Controlador de representación básica de Microsoft". Pero este adaptador tiene salidas y no tiene establecido el valor [**DE SOFTWARE DXGI \_ ADAPTER \_ FLAG. \_**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) El sistema operativo y las aplicaciones usan este adaptador de forma predeterminada. Si un controlador de pantalla está instalado o habilitado, las aplicaciones pueden recibir [**DXGI \_ ERROR DEVICE \_ \_ REMOVED**](dxgi-error.md) para este adaptador y, a continuación, deben volver a enumerar los adaptadores.

Cuando el adaptador de pantalla principal de un equipo es el "Adaptador de pantalla básica de Microsoft" (adaptador[WARP),](../direct3d11/overviews-direct3d-11-devices-create-warp.md) ese equipo también tiene un segundo adaptador. Este segundo adaptador es el dispositivo de solo representación que no tiene salidas de pantalla y para el que DXGI nunca devuelve [**DXGI \_ ERROR DEVICE \_ \_ REMOVED**](dxgi-error.md).

Si desea usar WARP para la representación, el proceso u otras tareas de larga duración, se recomienda usar el dispositivo de solo representación. Puede obtener un puntero al dispositivo de solo representación llamando al [**método IDXGIFactory1::EnumAdapters1.**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) También se crea el dispositivo de solo representación cuando se especifica [**D3D \_ DRIVER \_ TYPE \_ WARP**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type) en el parámetro *DriverType* de [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) porque el dispositivo WARP también usa el adaptador WARP de solo representación.

## <a name="presentation"></a>Presentación

El trabajo de la aplicación es representar fotogramas y pedir a DXGI que presente esos fotogramas en la salida. Si la aplicación tiene dos búferes disponibles, puede representar un búfer mientras se presenta otro. La aplicación puede requerir más de dos búferes según el tiempo que se tarda en representar un fotograma o la velocidad de fotogramas deseada para la presentación. El conjunto de búferes creado se denomina cadena de intercambio, como se muestra aquí.

![ilustración de una cadena de intercambio](images/dxgi-swap-chain.png)

-   [Crear una cadena de intercambio](#create-a-swap-chain)
-   [Cuidado y alimentación de la cadena de intercambio](#care-and-feeding-of-the-swap-chain)
-   [Control del tamaño de ventana](#handling-window-resizing)
-   [Elección de la salida y el tamaño de DXGI](#choosing-the-dxgi-output-and-size)
-   [Depuración en modo Full-Screen depuración](#debugging-in-full-screen-mode)
-   [Destruir una cadena de intercambio](#destroying-a-swap-chain)
-   [Uso de un monitor girado](#using-a-rotated-monitor)
-   [Cambiar modos](#switching-modes)
-   [Sugerencia de rendimiento a pantalla completa](#full-screen-performance-tip)
-   [Consideraciones sobre multiproceso](#multithread-considerations)

Una cadena de intercambio tiene un búfer frontal y uno o varios búferes de reserva. Cada aplicación crea su propia cadena de intercambio. Para maximizar la velocidad de presentación de los datos en una salida, casi siempre se crea una cadena de intercambio en la memoria de un subsestado de pantalla, que se muestra en la ilustración siguiente.

![ilustración de un subs sistema de visualización](images/dxgi-adapter.png)

El subs sistema de visualización (que a menudo es una tarjeta de vídeo pero que se podría implementar en una placa base) contiene una GPU, un convertidor de digital a análogo (DAC) y memoria. La cadena de intercambio se asigna dentro de esta memoria para que la presentación sea muy rápida. El subs sistema de visualización presenta los datos del búfer frontal a la salida.

Se configura una cadena de intercambio para dibujar en modo de pantalla completa o en modo de ventana, lo que elimina la necesidad de saber si una salida es de ventana o de pantalla completa. Una cadena de intercambio de modo de pantalla completa puede optimizar el rendimiento cambiando la resolución de pantalla.

### <a name="create-a-swap-chain"></a>Crear una cadena de intercambio

<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10: Direct3D 10 es el primer componente gráfico que usa DXGI. DXGI tiene algunos comportamientos de cadena de intercambio diferentes.<br/>
<ul>
<li>En DXGI, una cadena de intercambio se vincula a una ventana cuando se crea la cadena de intercambio. Este cambio mejora el rendimiento y ahorra memoria. Las versiones anteriores de Direct3D permitían que la cadena de intercambio cambiara la ventana a la que está asociada la cadena de intercambio.</li>
<li>En DXGI, una cadena de intercambio está asociada a un dispositivo de representación durante la creación. El objeto de dispositivo que devuelven las funciones de dispositivo de creación de Direct3D implementa la <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown"><strong>interfaz IUnknown.</strong></a> Puede llamar a <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface para</strong></a> consultar la interfaz <a href="/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgidevice2"><strong>IDXGIDevice2</strong></a> correspondiente del dispositivo. Un cambio en el dispositivo de representación requiere que se vuelva a crear la cadena de intercambio.</li>
<li><p>En DXGI, los efectos de intercambio disponibles se DXGI_SWAP_EFFECT_DISCARD y DXGI_SWAP_EFFECT_SEQUENTIAL. A partir Windows 8 el DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL de intercambio también está disponible. En la tabla siguiente se muestra una asignación de Direct3D 9 a las define el efecto de intercambio DXGI. </p>
<table>
<thead>
<tr class="header">
<th>Efecto de intercambio D3D9</th>
<th>Efecto de intercambio DXGI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DSWAPEFFECT_DISCARD</td>
<td>DXGI_SWAP_EFFECT_DISCARD</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_COPY</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL con 1 búfer</td>
</tr>
<tr class="odd">
<td>D3DSWAPEFFECT_FLIP</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL con 2 o más búferes</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_FLIPEX</td>
<td>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL con 2 o más búferes</td>
</tr>
</tbody>
</table>
<p></p>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



 

Los búferes de una cadena de intercambio se crean en un tamaño determinado y en un formato determinado. La aplicación especifica estos valores (o puede heredar el tamaño de la ventana de destino) en el inicio y, opcionalmente, puede modificarlos a medida que cambia el tamaño de la ventana en respuesta a eventos de programa o entrada del usuario.

Después de crear la cadena de intercambio, normalmente querrá representar imágenes en ella. Este es un fragmento de código que configura un contexto de Direct3D para representarlo en una cadena de intercambio. Este código extrae un búfer de la cadena de intercambio, crea una vista de destino de representación a partir de ese búfer y, a continuación, lo establece en el dispositivo:


```
ID3D11Resource * pBB;
ThrowFailure( pSwapChain->GetBuffer(0, __uuidof(pBB),    
  reinterpret_cast<void**>(&pBB)), "Couldn't get back buffer");
ID3D11RenderTargetView * pView;
ThrowFailure( pD3D11Device->CreateRenderTargetView(pBB, NULL, &pView), 
  "Couldn't create view" );
pD3D11DeviceContext->OMSetRenderTargets(1, &pView, 0);
        
```



Después de que la aplicación represente un marco en un búfer de cadena de intercambio, llame a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). A continuación, la aplicación puede representar la siguiente imagen.

### <a name="care-and-feeding-of-the-swap-chain"></a>Cuidado y alimentación de la cadena de intercambio

Después de representar la imagen, llame a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) y vaya a representar la siguiente imagen. Ese es el alcance de su responsabilidad.

Si anteriormente llamó a [**IDXGIFactory::MakeWindowAssociation**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation), el usuario puede presionar la combinación de teclas Alt-Enter y DXGI realizará la transición de la aplicación entre el modo de ventana y el modo de pantalla completa. **Se recomienda IDXGIFactory::MakeWindowAssociation,** ya que se desea encarecidamente un mecanismo de control estándar para el usuario.

Aunque no tiene que escribir más código del que se ha descrito, algunos pasos sencillos pueden hacer que la aplicación tenga más capacidad de respuesta. La consideración más importante es el cambio de tamaño de los búferes de la cadena de intercambio en respuesta al cambio de tamaño de la ventana de salida. Naturalmente, la mejor ruta de la aplicación es responder a WM SIZE y llamar a \_ [**IDXGISwapChain::ResizeBuffers,**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers)pasando el tamaño contenido en los parámetros del mensaje. Obviamente, este comportamiento hace que la aplicación responda bien al usuario cuando arrastra los bordes de la ventana, pero también es exactamente lo que permite una transición sin problemas a pantalla completa. La ventana recibirá un mensaje WM SIZE cada vez que se produce una transición de este tipo y llamar \_ a **IDXGISwapChain::ResizeBuffers** es la oportunidad de la cadena de intercambio de volver a asignar el almacenamiento de los búferes para una presentación óptima. Este es el motivo por el que la aplicación debe liberar las referencias que tenga en los búferes existentes antes de llamar a **IDXGISwapChain::ResizeBuffers**.

Si no se llama a [**IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) en respuesta al cambio al modo de pantalla completa (de forma natural, en respuesta a WM SIZE), puede impedir la optimización de volteo, donde DXGI puede simplemente intercambiar qué búfer se muestra, en lugar de copiar datos de una pantalla \_ completa.

[**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) le informará si la ventana de salida está totalmente concluida a través de **DXGI \_ STATUS \_ OCCLUDED**. Cuando esto sucede, se recomienda que la aplicación entre en modo de espera (mediante una llamada a **IDXGISwapChain1::P resent1** con **DXGI \_ PRESENT \_ TEST),** ya que los recursos usados para representar el marco se desperdician. El **uso de DXGI PRESENT \_ \_ TEST** impedirá que se presenten datos mientras se sigue realizando la comprobación de oclusión. Una **vez que IDXGISwapChain1::P resent1** devuelve S OK, debe salir del modo en espera; no use el código de retorno para cambiar al modo en espera, ya que puede dejar que la cadena de intercambio no pueda abandonar el modo de pantalla \_ completa.

El entorno de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8, proporciona una cadena de intercambio de modelos de volteo (es decir, una cadena de intercambio que tiene el valor [**de DXGI \_ SWAP EFFECT \_ FLIP \_ \_ SEQUENTIAL**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) establecido en el miembro **SwapEffect** de [**DXGI SWAP CHAIN \_ \_ \_ DESC**](/windows/win32/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) o [**DXGI SWAP CHAIN \_ \_ \_ DESC1).**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Cuando se presentan fotogramas a una salida con una cadena de intercambio de modelos de volteo, DXGI desenlaiza el búfer de reserva de todas las ubicaciones de estado de canalización, como un destino de representación de fusión de salida, que escriben en el búfer de reserva 0. Por lo tanto, se recomienda llamar a [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets) inmediatamente antes de representar en el búfer de reserva. Por ejemplo, no llame a **OMSetRenderTargets** y, a continuación, realice el trabajo del sombreador de proceso que no termina de representarse en el recurso. Para obtener más información sobre las cadenas de intercambio de modelos de volteo y sus ventajas, vea [DXGI Flip Model](dxgi-flip-model.md).

> [!NOTE]  
> En Direct3D 10 y Direct3D 11, no tiene que llamar a [**IDXGISwapChain::GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) para recuperar el búfer de reserva 0 después de llamar a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) porque, para mayor comodidad, las identidades de los búferes de reserva cambian. Esto no sucede en Direct3D 12 y, en su lugar, la aplicación debe realizar un seguimiento manual de los índices de búfer de reserva.

### <a name="handling-window-resizing"></a>Control del tamaño de la ventana

Puede usar el método [**IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) para controlar el cambio de tamaño de la ventana. Antes de llamar a **ResizeBuffers,** debe liberar todas las referencias pendientes a los búferes de la cadena de intercambio. El objeto que normalmente contiene una referencia al búfer de una cadena de intercambio es una vista de destino de representación.

En el código de ejemplo siguiente se muestra cómo llamar [**a ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) desde el controlador WindowProc para los mensajes \_ WM SIZE:


```
    case WM_SIZE:
        if (g_pSwapChain)
        {
            g_pd3dDeviceContext->OMSetRenderTargets(0, 0, 0);

            // Release all outstanding references to the swap chain's buffers.
            g_pRenderTargetView->Release();

            HRESULT hr;
            // Preserve the existing buffer count and format.
            // Automatically choose the width and height to match the client rect for HWNDs.
            hr = g_pSwapChain->ResizeBuffers(0, 0, 0, DXGI_FORMAT_UNKNOWN, 0);
                                            
            // Perform error handling here!

            // Get buffer and create a render-target-view.
            ID3D11Texture2D* pBuffer;
            hr = g_pSwapChain->GetBuffer(0, __uuidof( ID3D11Texture2D),
                                         (void**) &pBuffer );
            // Perform error handling here!

            hr = g_pd3dDevice->CreateRenderTargetView(pBuffer, NULL,
                                                     &g_pRenderTargetView);
            // Perform error handling here!
            pBuffer->Release();

            g_pd3dDeviceContext->OMSetRenderTargets(1, &g_pRenderTargetView, NULL );

            // Set up the viewport.
            D3D11_VIEWPORT vp;
            vp.Width = width;
            vp.Height = height;
            vp.MinDepth = 0.0f;
            vp.MaxDepth = 1.0f;
            vp.TopLeftX = 0;
            vp.TopLeftY = 0;
            g_pd3dDeviceContext->RSSetViewports( 1, &vp );
        }
        return 1;
```



### <a name="choosing-the-dxgi-output-and-size"></a>Elección de la salida y el tamaño de DXGI

De forma predeterminada, DXGI elige la salida que contiene la mayor parte del área de cliente de la ventana. Esta es la única opción disponible para DXGI cuando pasa a pantalla completa en respuesta a alt-entrar. Si la aplicación decide pasar al modo de pantalla completa por sí misma, puede llamar a [**IDXGISwapChain::SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) y pasar un [**valor IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) explícito (o **NULL,** si la aplicación está contenta de dejar que DXGI decida).

Para cambiar el tamaño de la salida mientras está en pantalla completa o en ventanas, se recomienda llamar a [**IDXGISwapChain::ResizeTarget**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget), ya que este método también cambia el tamaño de la ventana de destino. Puesto que se cambia el tamaño de la ventana de destino, el sistema operativo envía **WM \_ SIZE** y el código llamará de forma natural a [**IDXGISwapChain::ResizeBuffers en**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) respuesta. Por lo tanto, es una pérdida de esfuerzo cambiar el tamaño de los búferes y, a continuación, cambiar el tamaño del destino.

### <a name="debugging-in-full-screen-mode"></a>Depuración en modo de pantalla completa

Una cadena de intercambio DXGI se reencadena al modo de pantalla completa solo cuando sea absolutamente necesario. Esto significa que puede depurar una aplicación de pantalla completa mediante varios monitores, siempre y cuando la ventana de depuración no se superponga a la ventana de destino de la cadena de intercambio. Como alternativa, puede evitar el cambio de modo por completo si no establece la **marca DXGI \_ SWAP CHAIN FLAG ALLOW MODE \_ \_ \_ \_ \_ SWITCH.**

Si se permite la conmutación de modo, una cadena de intercambio se deslindrá del modo de pantalla completa cada vez que otra ventana ocluse su ventana de salida. La comprobación de oclusión se realiza durante [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)o mediante un subproceso independiente cuyo propósito es comprobar si la aplicación deja de responder (y ya no llama a **IDXGISwapChain1::P resent1).** Para deshabilitar la capacidad del subproceso independiente de provocar un modificador, establezca la siguiente clave del Registro en cualquier valor distinto de cero.

**HKCU \\ Software \\ Microsoft \\ DXGI \\ DisableFullscreenWatchdog**

### <a name="destroying-a-swap-chain"></a>Destruir una cadena de intercambio

Es posible que no libere una cadena de intercambio en modo de pantalla completa porque puede crear contención de subprocesos (lo que hará que DXGI proste una excepción no continuable). Antes de liberar una cadena de intercambio, cambie primero al modo de ventana (mediante [**IDXGISwapChain::SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)( **FALSE**, **NULL** )) y, a continuación, llame a [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

### <a name="using-a-rotated-monitor"></a>Uso de un monitor girado

Una aplicación no necesita preocuparse por la orientación del monitor, DXGI girará un búfer de cadena de intercambio durante la presentación, si es necesario. Por supuesto, esta rotación adicional puede afectar al rendimiento. Para obtener el mejor rendimiento, haga lo siguiente para encargarse de la rotación en la aplicación:

-   Use la **marca DXGI \_ SWAP CHAIN \_ \_ \_ NONPREROTATED**. Esto notifica a DXGI que la aplicación producirá una imagen girada (por ejemplo, modificando su matriz de proyección). Hay que tener en cuenta que esta marca solo es válida mientras está en modo de pantalla completa.
-   Asigne cada búfer de cadena de intercambio en su tamaño girado. Use [**IDXGIOutput::GetDesc para**](/windows/win32/api/DXGI/nf-dxgi-idxgioutput-getdesc) obtener estos valores, si es necesario.

Al realizar la rotación en la aplicación, DXGI simplemente realizará una copia en lugar de una copia y una rotación.

El entorno de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8, proporciona una cadena de intercambio de modelos de inversión (es decir, una cadena de intercambio que tiene el valor DE FLIP SEQUENTIAL DE [**DXGI \_ SWAP EFFECT \_ \_ \_ FLIP**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) establecido en el miembro **SwapEffect** de [**DXGI SWAP CHAIN \_ \_ \_ DESC1).**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Para maximizar las optimizaciones de presentación disponibles con una cadena de intercambio de modelos de volteo, se recomienda que las aplicaciones orienten el contenido para que coincida con la salida concreta en la que reside el contenido cuando ese contenido ocupa totalmente la salida. Para obtener más información sobre las cadenas de intercambio de modelos de volteo y sus ventajas, vea [DXGI Flip Model](dxgi-flip-model.md).

### <a name="switching-modes"></a>Cambio de modos

La cadena de intercambio DXGI podría cambiar el modo de presentación de una salida al realizar una transición a pantalla completa. Para habilitar el cambio de modo de presentación automática, debe especificar **DXGI \_ SWAP CHAIN FLAG ALLOW MODE \_ \_ \_ \_ \_ SWITCH** en la descripción de la cadena de intercambio. Si el modo de presentación cambia automáticamente, DXGI elegirá el modo más moderado (el tamaño y la resolución no cambiarán, pero la profundidad del color puede). Cambiar el tamaño de los búferes de la cadena de intercambio no provocará un cambio de modo. La cadena de intercambio hace una promesa implícita de que, si elige un búfer de reserva que coincida exactamente con un modo de presentación compatible con la salida de destino, pasará a ese modo de presentación al entrar en el modo de pantalla completa en esa salida. Por lo tanto, puede elegir un modo de presentación eligiendo el tamaño y el formato del búfer de reserva.

### <a name="full-screen-performance-tip"></a>Sugerencia de rendimiento de pantalla completa

Cuando se llama a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) en una aplicación de pantalla completa, la cadena de intercambio invierte (en lugar de blits) el contenido del búfer de reserva en el búfer frontal. Esto requiere que la cadena de intercambio se haya creado mediante un modo de presentación enumerado (especificado en [**DXGI \_ SWAP CHAIN \_ \_ DESC1).**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Si no enumera los modos de presentación o especifica incorrectamente el modo de presentación en la descripción, la cadena de intercambio puede realizar una transferencia de bloque de bits (bitblt) en su lugar. La bitblt provoca una copia de extensión adicional, así como un aumento del uso de memoria de vídeo, y es difícil de detectar. Para evitar este problema, enumere los modos de presentación e inicialice correctamente la descripción de la cadena de intercambio antes de crear la cadena de intercambio. Esto garantizará el máximo rendimiento al voltear en modo de pantalla completa y evitará la sobrecarga de memoria adicional.

### <a name="multithread-considerations"></a>Consideraciones sobre multiproceso

Cuando se usa DXGI en una aplicación con varios subprocesos, debe tener cuidado para evitar la creación de un interbloqueo, donde dos subprocesos diferentes esperan entre sí para completarse. Hay dos situaciones en las que esto puede ocurrir.

-   El subproceso de representación no es el subproceso de la bomba de mensajes.
-   El subproceso que ejecuta una API DXGI no es el mismo subproceso que creó la ventana.

Tenga cuidado de que nunca tenga que esperar el subproceso de suministro de mensajes en el subproceso de representación cuando use cadenas de intercambio de pantalla completa. Por ejemplo, llamar a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (desde el subproceso de representación) puede hacer que el subproceso de representación espere en el subproceso de la bomba de mensajes. Cuando se produce un cambio de modo, este escenario es posible si **Present1** llama a ::SetWindowPos() o ::SetWindowStyle() y cualquiera de estos métodos llama a ::SendMessage(). En este escenario, si el subproceso de bombeo de mensajes tiene una sección crítica que lo protege o si el subproceso de representación está bloqueado, los dos subprocesos se interbloquearán.

Para obtener más información sobre el uso de DXGI con varios subprocesos, [vea Multithreading y DXGI](../direct3d11/overviews-direct3d-11-render-multi-thread-intro.md).

## <a name="dxgi-responses-from-dllmain"></a>Respuestas DXGI de DLLMain

Dado que una función [**DllMain**](../dlls/dllmain.md) no puede garantizar el orden en el que carga y descarga archivos DLL, se recomienda que la función **DllMain** de la aplicación no llame a funciones o métodos de Direct3D o DXGI, incluidas las funciones o métodos que crean o liberan objetos. Si la función **DllMain** de la aplicación llama a un componente determinado, ese componente podría llamar a otro archivo DLL que no está presente en el sistema operativo, lo que hace que el sistema operativo se bloquea. Direct3D y DXGI podrían cargar un conjunto de archivos DLL, normalmente un conjunto de controladores, que difiere de un equipo a otro. Por lo tanto, incluso si la aplicación no se bloquea en los equipos de desarrollo y prueba cuando su función **DllMain** llama a funciones o métodos de Direct3D o DXGI, podría bloquearse cuando se ejecuta en otro equipo.

Para evitar que cree una aplicación que pueda provocar el bloqueo del sistema operativo, DXGI proporciona las siguientes respuestas en las situaciones especificadas:

-   Si la función [**DllMain**](../dlls/dllmain.md) de la aplicación publica su última referencia a un generador DXGI, DXGI genera una excepción.
-   Si la función [**DllMain de**](../dlls/dllmain.md) la aplicación crea un generador DXGI, DXGI devuelve un código de error.

## <a name="dxgi-11-changes"></a>Cambios en DXGI 1.1

Hemos agregado la siguiente funcionalidad en DXGI 1.1.

-   Compatibilidad con superficies compartidas sincronizadas

    Las superficies compartidas sincronizadas para Direct3D 10.1 y Direct3D 11 permiten un uso compartido eficaz de la superficie de lectura y escritura entre varios dispositivos Direct3D (es posible compartir entre dispositivos Direct3D 10 y Direct3D 11). Vea [**IDXGIKeyedMutex::AcquireSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-acquiresync) e [**IDXGIKeyedMutex::ReleaseSync.**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-releasesync)

-   Compatibilidad con colores altos

    Admite el formato UNORM DXGI \_ FORMAT \_ R10G10B10 \_ XR \_ BIAS \_ \_ A2.

-   [**IDXGIDevice1::SetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) e [ **IDXGIDevice1::GetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-getmaximumframelatency)
-   [**IDXGIFactory1::EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) enumera los adaptadores locales sin monitores ni salidas asociados, así como adaptadores con salidas asociadas. El primer adaptador devuelto será el adaptador local en el que se muestra el escritorio principal.
-   Compatibilidad con el formato BGRA

    FORMATO \_ \_ DXGI B8G8R8A8 UNORM y \_ DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB, vea [**IDXGISurface1::GetDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-getdc) e [**IDXGISurface1::ReleaseDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-releasedc).

## <a name="dxgi-12-changes"></a>Cambios en DXGI 1.2

Hemos agregado la siguiente funcionalidad en DXGI 1.2.

-   Cadena de intercambio estéreo
-   [Cadena de intercambio de modelos de volteo](dxgi-flip-model.md)
-   Presentación optimizada (desplazamiento, rectángulos desa desplazamiento y rotación)
-   Sincronización y recursos compartidos mejorados
-   [Duplicación de escritorio](desktop-dup-api.md)
-   Uso optimizado de memoria de vídeo
-   Compatibilidad con formatos de 16 bits por píxel (bpp) (DXGI \_ FORMAT \_ B5G6R5 \_ UNORM, DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM, DXGI \_ FORMAT \_ B4G4R4A4 \_ UNORM)
-   Depuración de API

Para obtener más información sobre DXGI 1.2, vea Mejoras de [DXGI 1.2.](dxgi-1-2-improvements.md)

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)

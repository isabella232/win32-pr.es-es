---
description: En este tema se incluyen las siguientes secciones.
ms.assetid: 0522ccbf-e754-470a-8199-004fcbaa927d
title: Información general sobre DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 324a5be26aade17385a6ab0b7d347015497a2a3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494567"
---
# <a name="dxgi-overview"></a>Información general sobre DXGI

Microsoft DirectX Graphics Infrastructure (DXGI) reconoce que algunas partes de los gráficos evolucionan más lentamente que otras. El objetivo principal de DXGI es administrar tareas de bajo nivel que pueden ser independientes del tiempo de ejecución de gráficos de DirectX. DXGI proporciona un marco común para los componentes de gráficos futuros; el primer componente que aprovecha DXGI es Microsoft Direct3D 10.

En las versiones anteriores de Direct3D, las tareas de bajo nivel, como la enumeración de los dispositivos de hardware, la presentación de fotogramas representados en una salida, el control de gamma y la administración de una transición de pantalla completa se incluían en el tiempo de ejecución de Direct3D. Estas tareas se implementan ahora en DXGI.

El objetivo de DXGI es comunicarse con el controlador de modo kernel y el hardware del sistema, tal como se muestra en el diagrama siguiente.

![diagrama de la comunicación entre aplicaciones, dxgi y controladores y hardware](images/dxgi-dll.png)

Una aplicación puede acceder a la DXGI directamente o llamar a las API de Direct3D en D3D11 \_ 1. h, D3D11. h, D3D10 \_ 1. h o D3D10. h, que controla las comunicaciones con DXGI. Puede que desee trabajar con DXGI directamente si la aplicación necesita enumerar dispositivos o controlar cómo se presentan los datos en una salida.

En este tema se incluyen las siguientes secciones.

-   [Enumerar adaptadores](#enumerating-adapters)
    -   [Nueva información acerca de la enumeración de adaptadores para Windows 8](#new-info-about-enumerating-adapters-for-windows-8)
-   [Presentación](#presentation)
    -   [Crear una cadena de intercambio](#create-a-swap-chain)
    -   [Atención e alimentación de la cadena de intercambio](#care-and-feeding-of-the-swap-chain)
    -   [Control de cambio de tamaño de ventana](#handling-window-resizing)
    -   [Elección del tamaño y la salida de DXGI](#choosing-the-dxgi-output-and-size)
    -   [Depuración en modo de Full-Screen](#debugging-in-full-screen-mode)
    -   [Destruir una cadena de intercambio](#destroying-a-swap-chain)
    -   [Uso de un monitor girado](#using-a-rotated-monitor)
    -   [Cambiar modos](#switching-modes)
    -   [Sugerencia de rendimiento de pantalla completa](#full-screen-performance-tip)
    -   [Consideraciones sobre subprocesos](#multithread-considerations)
-   [Respuestas de DXGI desde DLLMain](#dxgi-responses-from-dllmain)
-   [Cambios en DXGI 1,1](#dxgi-11-changes)
-   [Cambios en DXGI 1,2](#dxgi-12-changes)
-   [Temas relacionados](#related-topics)

Para ver qué formatos son compatibles con el hardware de Direct3D 11:

-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,1](hardware-support-for-direct3d-12-1-formats.md)
-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,0](hardware-support-for-direct3d-12-0-formats.md)
-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,1](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,0](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Compatibilidad de hardware con formatos 10Level9 de Direct3D](/previous-versions//ff471324(v=vs.85))
-   [Compatibilidad de hardware con formatos de Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Compatibilidad de hardware con formatos de Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="enumerating-adapters"></a>Enumerar adaptadores

Un adaptador es una abstracción del hardware y la funcionalidad de software del equipo. Normalmente hay muchos adaptadores en el equipo. Algunos dispositivos se implementan en hardware (como la tarjeta de vídeo) y otros se implementan en software (como el rasterizador de referencia de Direct3D). Los adaptadores implementan la funcionalidad usada por una aplicación gráfica. En el diagrama siguiente se muestra un sistema con un solo equipo, dos adaptadores (tarjetas de vídeo) y tres monitores de salida.

![diagrama de un equipo con dos tarjetas de vídeo y tres monitores](images/dxgi-terms.png)

Al enumerar estos componentes de hardware, DXGI crea una interfaz [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) para cada salida (o monitor) y una interfaz [**IDXGIAdapter2**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2) para cada tarjeta de vídeo (incluso si se trata de una tarjeta de vídeo integrada en una placa base). La enumeración se realiza mediante una llamada de interfaz [**IDXGIFactory**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) , [**IDXGIFactory:: EnumAdapters**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-enumadapters), para devolver un conjunto de interfaces [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) que representan el hardware de vídeo.

DXGI 1,1 agregó la interfaz [**IDXGIFactory1**](/windows/win32/api/DXGI/nn-dxgi-idxgifactory1) . [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) devuelve un conjunto de interfaces [**IDXGIAdapter1**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter1) que representa el hardware de vídeo.

Si desea seleccionar capacidades de hardware de vídeo específicas al usar las API de Direct3D, se recomienda llamar a la función [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) con cada identificador de adaptador y posible nivel de [característica](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)de hardware. Esta función se ejecuta correctamente si el adaptador especificado es compatible con el nivel de característica.

### <a name="new-info-about-enumerating-adapters-for-windows-8"></a>Nueva información acerca de la enumeración de adaptadores para Windows 8

A partir de Windows 8, siempre está presente un adaptador denominado "Microsoft Basic Render driver". Este adaptador tiene un ID. de cuenta de **0x1414** y un ID. de **0x8c**. Este adaptador también tiene establecido el valor de [**\_ \_ \_ software marca de adaptador de dxgi**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) en el miembro **Flags** de la estructura [**\_ \_ DESC2 del adaptador de dxgi**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_adapter_desc2) . Este adaptador es un dispositivo solo de representación que no tiene salidas de presentación. DXGI nunca devuelve un [**dispositivo de error de dxgi \_ \_ \_ quitado**](dxgi-error.md) para este adaptador.

Si el controlador de pantalla de un equipo no funciona o está deshabilitado, el adaptador principal (**null**) del equipo también podría denominarse "controlador de representación básica de Microsoft". Pero este adaptador tiene salidas y no tiene establecido el valor de [**\_ \_ \_ software marca de adaptador de DXGI**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) . El sistema operativo y las aplicaciones usan este adaptador de forma predeterminada. Si un controlador de pantalla está instalado o habilitado, las aplicaciones pueden recibir un [**dispositivo de error de DXGI \_ \_ \_ quitado**](dxgi-error.md) para este adaptador y, después, deben volver a enumerar los adaptadores.

Cuando el adaptador de pantalla principal de un equipo es el "adaptador de pantalla básico de Microsoft[" (adaptador](../direct3d11/overviews-direct3d-11-devices-create-warp.md) de deformación), ese equipo también tiene un segundo adaptador. Este segundo adaptador es el dispositivo de solo representación que no tiene salidas de presentación y para la que DXGI nunca devuelve un [**\_ dispositivo de error de \_ \_ dxgi**](dxgi-error.md).

Si desea usar WARP para la representación, el proceso u otras tareas de ejecución prolongada, se recomienda usar el dispositivo de solo representación. Puede obtener un puntero al dispositivo de solo representación llamando al método [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) . También creará el dispositivo de solo representación Cuando especifique el [**\_ tipo de controlador D3D \_ \_ Warp**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type) en el parámetro *DriverType* de [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) , ya que el dispositivo de deformación también utiliza el adaptador de alabeo de solo representación.

## <a name="presentation"></a>Presentación

El trabajo de la aplicación es representar fotogramas y pedir a DXGI que presente esos fotogramas en la salida. Si la aplicación tiene dos búferes disponibles, puede representar un búfer mientras presenta otro. La aplicación podría requerir más de dos búferes según el tiempo necesario para representar un fotograma o la velocidad de fotogramas deseada para la presentación. El conjunto de búferes creados se denomina cadena de intercambio, como se muestra aquí.

![Ilustración de una cadena de intercambio](images/dxgi-swap-chain.png)

-   [Crear una cadena de intercambio](#create-a-swap-chain)
-   [Atención e alimentación de la cadena de intercambio](#care-and-feeding-of-the-swap-chain)
-   [Control de cambio de tamaño de ventana](#handling-window-resizing)
-   [Elección del tamaño y la salida de DXGI](#choosing-the-dxgi-output-and-size)
-   [Depuración en modo de Full-Screen](#debugging-in-full-screen-mode)
-   [Destruir una cadena de intercambio](#destroying-a-swap-chain)
-   [Uso de un monitor girado](#using-a-rotated-monitor)
-   [Cambiar modos](#switching-modes)
-   [Sugerencia de rendimiento de pantalla completa](#full-screen-performance-tip)
-   [Consideraciones sobre subprocesos](#multithread-considerations)

Una cadena de intercambio tiene un búfer frontal y uno o más búferes de reserva. Cada aplicación crea su propia cadena de intercambio. Para maximizar la velocidad de la presentación de los datos en una salida, casi siempre se crea una cadena de intercambio en la memoria de un subsistema de pantalla, que se muestra en la siguiente ilustración.

![Ilustración de un subsistema de presentación](images/dxgi-adapter.png)

El subsistema de pantalla (que suele ser una tarjeta de vídeo, pero que se puede implementar en una placa base) contiene una GPU, un convertidor digital a analógico (DAC) y una memoria. La cadena de intercambio se asigna en esta memoria para agilizar la presentación. El subsistema de visualización presenta los datos en el búfer frontal a la salida.

Una cadena de intercambio está configurada para dibujarse en el modo de pantalla completa o en ventanas; de esta forma, se elimina la necesidad de saber si una salida está en ventana o en pantalla completa. Una cadena de intercambio en modo de pantalla completa puede optimizar el rendimiento cambiando la resolución de pantalla.

### <a name="create-a-swap-chain"></a>Crear una cadena de intercambio

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10: Direct3D 10 es el primer componente de gráficos para usar DXGI. DXGI tiene distintos comportamientos de cadena de intercambio.<br/>
<ul>
<li>En DXGI, una cadena de intercambio está ligada a una ventana cuando se crea la cadena de intercambio. Este cambio mejora el rendimiento y ahorra memoria. Las versiones anteriores de Direct3D permitían que la cadena de intercambio cambiara la ventana a la que está vinculada la cadena de intercambio.</li>
<li>En DXGI, una cadena de intercambio está asociada a un dispositivo de representación en la creación. El objeto de dispositivo que devuelven las funciones de dispositivo de creación de Direct3D implementa la interfaz <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> . Puede llamar a <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> para consultar la interfaz <a href="/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgidevice2"><strong>IDXGIDevice2</strong></a> correspondiente del dispositivo. Un cambio en el dispositivo de representación requiere que se vuelva a crear la cadena de intercambio.</li>
<li><p>En DXGI, los efectos de intercambio disponibles son DXGI_SWAP_EFFECT_DISCARD y DXGI_SWAP_EFFECT_SEQUENTIAL. A partir de Windows 8, el efecto de intercambio de DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL también está disponible. En la tabla siguiente se muestra una asignación de las definiciones del efecto de intercambio de Direct3D 9 a DXGI. </p>
<table>
<thead>
<tr class="header">
<th>Efecto de intercambio de D3D9</th>
<th>Efecto de intercambio de DXGI</th>
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



 

Los búferes de una cadena de intercambio se crean con un tamaño determinado y en un formato determinado. La aplicación especifica estos valores (o puede heredar el tamaño de la ventana de destino) en el inicio y, después, puede modificarlos opcionalmente a medida que cambia el tamaño de la ventana en respuesta a los eventos del usuario o del programa.

Después de crear la cadena de intercambio, normalmente querrá representar imágenes en ella. A continuación se muestra un fragmento de código que configura un contexto de Direct3D para que se represente en una cadena de intercambio. Este código extrae un búfer de la cadena de intercambio, crea una vista de destino de representación desde ese búfer y, a continuación, lo establece en el dispositivo:


```
ID3D11Resource * pBB;
ThrowFailure( pSwapChain->GetBuffer(0, __uuidof(pBB),    
  reinterpret_cast<void**>(&pBB)), "Couldn't get back buffer");
ID3D11RenderTargetView * pView;
ThrowFailure( pD3D11Device->CreateRenderTargetView(pBB, NULL, &pView), 
  "Couldn't create view" );
pD3D11DeviceContext->OMSetRenderTargets(1, &pView, 0);
        
```



Una vez que la aplicación representa un fotograma en un búfer de la cadena de intercambio, llame a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). La aplicación puede entonces representar la siguiente imagen.

### <a name="care-and-feeding-of-the-swap-chain"></a>Atención e alimentación de la cadena de intercambio

Después de representar la imagen, llame a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) y vaya a representar la siguiente imagen. Eso es el alcance de su responsabilidad.

Si anteriormente llamó a [**IDXGIFactory:: MakeWindowAssociation**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation), el usuario puede presionar la combinación de teclas Alt-Enter y DXGI pasará la aplicación entre el modo de pantalla completa y el de ventana. Se recomienda **IDXGIFactory:: MakeWindowAssociation** porque se desea un mecanismo de control estándar para el usuario.

Aunque no es necesario escribir más código del que se ha descrito, algunos sencillos pasos pueden hacer que la aplicación tenga mayor capacidad de respuesta. La consideración más importante es el cambio de tamaño de los búferes de la cadena de intercambio en respuesta al cambio de tamaño de la ventana de salida. Naturalmente, la mejor ruta de la aplicación es responder al tamaño de WM \_ y llamar a [**IDXGISwapChain:: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers), pasando el tamaño contenido en los parámetros del mensaje. Obviamente, este comportamiento hace que la aplicación responda bien al usuario cuando arrastra los bordes de la ventana, pero también es exactamente lo que permite una transición de pantalla completa suave. La ventana recibirá un mensaje de tamaño de WM \_ siempre que se produzca una transición, y la llamada a **IDXGISwapChain:: ResizeBuffers** es la posibilidad de que la cadena de intercambio vuelva a asignar el almacenamiento de los búferes para una presentación óptima. Este es el motivo por el que la aplicación debe liberar todas las referencias que tiene en los búferes existentes antes de llamar a **IDXGISwapChain:: ResizeBuffers**.

Si no se llama a [**IDXGISwapChain:: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) en respuesta a cambiar al modo de pantalla completa (lo que es más natural, en respuesta al tamaño de WM \_ ), puede impedir la optimización del volteo, en la que DXGI puede simplemente cambiar el búfer que se muestra, en lugar de copiar los datos de una pantalla completa.

[**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) le informará si la ventana de salida es totalmente ocluidos a través de la **\_ \_ ocluidos de estado de DXGI**. Cuando esto ocurre, se recomienda que la aplicación entre en modo de espera (mediante una llamada a **IDXGISwapChain1::P resent1** con la **\_ \_ prueba de presencia de DXGI**), ya que se desperdician los recursos utilizados para representar el marco. El uso de **DXGI \_ present \_ Test** impedirá que se presenten los datos mientras se sigue realizando la comprobación de la oclusión. Una vez que **IDXGISwapChain1::P resent1** devuelve S \_ OK, debe salir del modo de espera; no use el código de retorno para cambiar al modo de espera, ya que esto puede dejar que la cadena de intercambio no pueda abandonar el modo de pantalla completa.

El tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8, proporciona una cadena de intercambio de volteo del modelo (es decir, una cadena de intercambio que tenga el efecto de intercambio de dxgi, el valor [**\_ \_ \_ \_ secuencial de volteo**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) se establece en el miembro **SwapEffect** de la cadena de intercambio de dxgi o en la [**cadena de intercambio de dxgi \_ \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). [**\_ \_ \_**](/windows/win32/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) Cuando se presentan fotogramas en una salida con una cadena de intercambio de modelo Flip, DXGI desenlaza el búfer de reserva de todas las ubicaciones de estado de canalización, como un destino de representación de combinación de salida, que escriben en el búfer de reserva 0. Por lo tanto, se recomienda llamar a [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets) inmediatamente antes de representarlo en el búfer de reserva. Por ejemplo, no llame a **OMSetRenderTargets** y, a continuación, realice el trabajo del sombreador de cálculo que no termine de representar el recurso. Para obtener más información sobre las cadenas de intercambio de modelo flip y sus ventajas, vea [modelo de volteo de DXGI](dxgi-flip-model.md).

> [!NOTE]  
> En Direct3D 10 y Direct3D 11, no es necesario llamar a [**IDXGISwapChain:: getBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) para recuperar el búfer de reserva 0 después de llamar a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) porque, por comodidad, cambian las identidades de los búferes de reserva. Esto no ocurre en Direct3D 12 y, en su lugar, la aplicación debe realizar manualmente el seguimiento de los índices de búfer.

### <a name="handling-window-resizing"></a>Control de cambio de tamaño de ventana

Puede usar el método [**IDXGISwapChain:: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) para controlar el cambio de tamaño de las ventanas. Antes de llamar a **ResizeBuffers**, debe liberar todas las referencias pendientes a los búferes de la cadena de intercambio. El objeto que normalmente contiene una referencia a un búfer de la cadena de intercambio es una vista de destino de representación.

En el ejemplo de código siguiente se muestra cómo llamar a [**ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) desde el controlador de WindowProc para mensajes de tamaño de WM \_ :


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



### <a name="choosing-the-dxgi-output-and-size"></a>Elección del tamaño y la salida de DXGI

De forma predeterminada, DXGI elige la salida que contiene la mayor parte del área de cliente de la ventana. Esta es la única opción disponible en DXGI cuando se pasa a la pantalla completa en respuesta a Alt + Entrar. Si la aplicación decide ir al modo de pantalla completa, puede llamar a [**IDXGISwapChain:: SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) y pasar un [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) explícito (o **null** si la aplicación está feliz para permitir que DXGI decida).

Para cambiar el tamaño de la salida mientras se está en la pantalla completa o en la ventana, se recomienda llamar a [**IDXGISwapChain:: ResizeTarget**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget), ya que este método también cambia el tamaño de la ventana de destino. Dado que se cambia el tamaño de la ventana de destino, el sistema operativo envía el **\_ tamaño de WM** y el código llamará de forma natural a [**IDXGISwapChain:: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) en respuesta. Por lo tanto, se pierde el esfuerzo de cambiar el tamaño de los búferes y, posteriormente, se cambia el tamaño del destino.

### <a name="debugging-in-full-screen-mode"></a>Depuración en modo de pantalla completa

Una cadena de intercambio de DXGI deja el modo de pantalla completa solo cuando es absolutamente necesario. Esto significa que puede depurar una aplicación de pantalla completa mediante varios monitores, siempre y cuando la ventana de depuración no se superponga a la ventana de destino de la cadena de intercambio. Como alternativa, puede evitar que el cambio de modo se configure por completo si no se establece la marca de **\_ \_ \_ \_ \_ \_ cambio de modo permitir del marcador de cadena de intercambio de DXGI** .

Si se permite el cambio de modo, una cadena de intercambio liberará el modo de pantalla completa siempre que otra ventana ocluidos la ventana de salida. La comprobación de la oclusión se realiza durante [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), o por un subproceso independiente cuyo propósito es ver si la aplicación deja de responder (y ya no llama a **IDXGISwapChain1::P resent1**). Para deshabilitar la posibilidad de que el subproceso independiente cause un cambio, establezca la siguiente clave del registro en cualquier valor distinto de cero.

**HKCU \\ software \\ Microsoft \\ DXGI \\ DisableFullscreenWatchdog**

### <a name="destroying-a-swap-chain"></a>Destruir una cadena de intercambio

No puede liberar una cadena de intercambio en el modo de pantalla completa, ya que si lo hace, puede crear contención de subprocesos (lo que hará que DXGI genere una excepción no continuada). Antes de liberar una cadena de intercambio, cambie primero a modo de ventana (mediante [**IDXGISwapChain:: SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)( **false**, **null** )) y, a continuación, llame a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

### <a name="using-a-rotated-monitor"></a>Uso de un monitor girado

Una aplicación no necesita preocuparse por la orientación del monitor, DXGI girará un búfer de cadena de intercambio durante la presentación, si es necesario. Por supuesto, esta rotación adicional puede afectar al rendimiento. Para obtener el mejor rendimiento, haga lo siguiente para realizar la rotación en la aplicación:

-   Use el **indicador de cadena de intercambio de DXGI \_ \_ \_ \_ NONPREROTATED**. Esto notifica a DXGI que la aplicación generará una imagen girada (por ejemplo, modificando su matriz de proyección). Un aspecto que se debe tener en cuenta es que esta marca solo es válida mientras se está en modo de pantalla completa.
-   Asigne cada búfer de la cadena de intercambio en su tamaño girado. Use [**IDXGIOutput:: GetDesc**](/windows/win32/api/DXGI/nf-dxgi-idxgioutput-getdesc) para obtener estos valores, si es necesario.

Al realizar la rotación en la aplicación, DXGI simplemente realizará una copia en lugar de una copia y una rotación.

El tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8, proporciona una cadena de intercambio de volteo del modelo (es decir, una cadena de intercambio que tiene el efecto de intercambio de dxgi, volteo de valor [**\_ \_ \_ \_ secuencial**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) establecido en el miembro **SwapEffect** de la [**cadena de intercambio de dxgi \_ \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Para maximizar las optimizaciones de presentación disponibles con una cadena de intercambio de modelo Flip, se recomienda hacer que las aplicaciones orienten el contenido para que coincida con la salida determinada en la que reside el contenido cuando ese contenido ocupe por completo el resultado. Para obtener más información sobre las cadenas de intercambio de modelo flip y sus ventajas, vea [modelo de volteo de DXGI](dxgi-flip-model.md).

### <a name="switching-modes"></a>Cambiar modos

La cadena de intercambio de DXGI podría cambiar el modo de visualización de una salida cuando se realiza una transición de pantalla completa. Para habilitar el cambio de modo de presentación automático, debe especificar el **\_ \_ \_ \_ \_ \_ modificador de modo permitir del marcador de cadena de intercambio de DXGI** en la descripción de la cadena de intercambio. Si el modo de presentación cambia automáticamente, DXGI elegirá el modo más modesto (el tamaño y la resolución no cambiarán, pero es posible que la profundidad de color). Cambiar el tamaño de los búferes de cadena de intercambio no producirá un cambio de modo. La cadena de intercambio realiza una promesa implícita que si elige un búfer de reserva que coincida exactamente con un modo de presentación admitido por la salida de destino, cambiará a ese modo de presentación al entrar en el modo de pantalla completa en esa salida. Por lo tanto, elija un modo de presentación eligiendo el tamaño y el formato del búfer de reserva.

### <a name="full-screen-performance-tip"></a>Sugerencia de rendimiento de pantalla completa

Cuando se llama a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) en una aplicación de pantalla completa, la cadena de intercambio se voltea (en lugar de blits) el contenido del búfer de reserva en el búfer frontal. Esto requiere que la cadena de intercambio se haya creado mediante un modo de presentación enumerado (especificado en la [**cadena de intercambio de DXGI \_ \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Si no puede enumerar los modos de presentación o especifica incorrectamente el modo de presentación en la descripción, la cadena de intercambio puede realizar una transferencia de bloque de bits (bitblt) en su lugar. El bitblt produce una copia de ampliación adicional, así como un mayor uso de la memoria de vídeo, y es difícil de detectar. Para evitar este problema, enumere los modos de presentación e inicialice la descripción de la cadena de intercambio correctamente antes de crear la cadena de intercambio. Esto garantizará el máximo rendimiento al voltear en el modo de pantalla completa y evitar la sobrecarga de memoria adicional.

### <a name="multithread-considerations"></a>Consideraciones sobre subprocesos

Al usar DXGI en una aplicación con varios subprocesos, debe tener cuidado de evitar la creación de un interbloqueo, donde dos subprocesos diferentes están esperando a que se completen. Hay dos situaciones en las que esto puede ocurrir.

-   El subproceso de representación no es el subproceso de bombeo de mensajes.
-   El subproceso que ejecuta una API de DXGI no es el mismo subproceso que creó la ventana.

Tenga cuidado de que nunca tenga el subproceso de bombeo de mensajes en el subproceso de representación cuando use cadenas de intercambio de pantalla completa. Por ejemplo, al llamar a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (desde el subproceso de representación) puede provocar que el subproceso de representación espere en el subproceso de bombeo de mensajes. Cuando se produce un cambio de modo, este escenario es posible si **Present1** llama a:: SetWindowPos () o:: SetWindowStyle () y cualquiera de estos métodos llama a:: SendMessage (). En este escenario, si el subproceso de bombeo de mensajes tiene una sección crítica que lo protege o si el subproceso de representación está bloqueado, los dos subprocesos se interbloquearán.

Para obtener más información sobre el uso de DXGI con varios subprocesos, vea [multithreading y DXGI](../direct3d11/overviews-direct3d-11-render-multi-thread-intro.md).

## <a name="dxgi-responses-from-dllmain"></a>Respuestas de DXGI desde DLLMain

Dado que una función [**DllMain**](../dlls/dllmain.md) no puede garantizar el orden en que carga y descarga los archivos dll, se recomienda que la función **DllMain** de la aplicación no llame a las funciones o métodos de Direct3D o DXGI, incluidas las funciones o los métodos que crean o liberan objetos. Si la función **DllMain** de la aplicación llama a un componente determinado, ese componente podría llamar a otro archivo DLL que no está presente en el sistema operativo, lo que hace que el sistema operativo se bloquee. Direct3D y DXGI pueden cargar un conjunto de archivos dll, normalmente un conjunto de controladores, que difieren de un equipo a otro. Por lo tanto, incluso si la aplicación no se bloquea en los equipos de desarrollo y pruebas cuando su función **DllMain** llama a las funciones o métodos de Direct3D o DXGI, podría bloquearse cuando se ejecuta en otro equipo.

Para evitar la creación de una aplicación que puede hacer que el sistema operativo se bloquee, DXGI proporciona las siguientes respuestas en las situaciones especificadas:

-   Si la función [**DllMain**](../dlls/dllmain.md) de la aplicación libera su última referencia a una fábrica de DXGI, dxgi genera una excepción.
-   Si la función [**DllMain**](../dlls/dllmain.md) de la aplicación crea una fábrica de DXGI, dxgi devuelve un código de error.

## <a name="dxgi-11-changes"></a>Cambios en DXGI 1,1

Hemos agregado la siguiente funcionalidad en DXGI 1,1.

-   Compatibilidad con superficies compartidas sincronizadas

    Las superficies compartidas sincronizadas para Direct3D 10,1 y Direct3D 11 permiten el uso compartido de la superficie de lectura y escritura eficaz entre varios dispositivos de Direct3D (es posible el uso compartido entre dispositivos Direct3D 10 y Direct3D 11). Vea [**IDXGIKeyedMutex:: AcquireSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-acquiresync) y [**IDXGIKeyedMutex:: ReleaseSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-releasesync).

-   Compatibilidad con colores de alto nivel

    Admite el formato de DXGI \_ formato \_ R10G10B10 \_ XR \_ \_ a2 \_ UNORM.

-   [**IDXGIDevice1:: SetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) y [ **IDXGIDevice1:: GetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-getmaximumframelatency)
-   [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) enumera los adaptadores locales sin monitores o salidas conectados, así como los adaptadores con salidas adjuntas. El primer adaptador devuelto será el adaptador local en el que se muestra el servidor principal de escritorio.
-   Compatibilidad con el formato BGRA

    Formato \_ \_ de dxgi B8G8R8A8 \_ UNORM y dxgi \_ format \_ B8G8R8A8 \_ UNORM \_ sRGB, vea [**IDXGISurface1:: GetDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-getdc) y [**IDXGISurface1:: ReleaseDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-releasedc).

## <a name="dxgi-12-changes"></a>Cambios en DXGI 1,2

Hemos agregado la siguiente funcionalidad en DXGI 1,2.

-   Cadena de intercambio estéreo
-   [Cadena de intercambio de modelo de volteo](dxgi-flip-model.md)
-   Presentación optimizada (desplazamiento, rectángulos modificados y giro)
-   Sincronización y recursos compartidos mejorados
-   [Duplicación de escritorio](desktop-dup-api.md)
-   Uso optimizado de la memoria de vídeo
-   Compatibilidad con formatos de 16 bits por píxel (BPP) ( \_ formato de dxgi \_ B5G6R5 \_ UNORM, formato de dxgi \_ \_ B5G5R5A1 \_ UNORM, formato de dxgi \_ \_ B4G4R4A4 \_ UNORM)
-   API de depuración

Para obtener más información sobre DXGI 1,2, consulte [mejoras de dxgi 1,2](dxgi-1-2-improvements.md).

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)

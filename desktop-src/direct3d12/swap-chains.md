---
title: Cadenas de intercambio
description: Las cadenas de intercambio controlan la rotación del búfer de reserva, formando la base de la animación gráfica.
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbc7ec1b62ba620b42bc85c1c1f491ff7ba952d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072867"
---
# <a name="swap-chains"></a>Cadenas de intercambio

Las cadenas de intercambio controlan la rotación del búfer de reserva, formando la base de la animación gráfica.

## <a name="overview"></a>Información general

El modelo de programación para cadenas de intercambio en Direct3D 12 no es idéntico al de versiones anteriores de D3D. La comodidad de programación, por ejemplo, de admitir la rotación automática de recursos que estaba presente en D3D10 y D3D11 no se admite ahora. La rotación automática de recursos permite a las aplicaciones representar el mismo objeto de API mientras la superficie real que se representa cambia cada fotograma. El comportamiento de las cadenas de intercambio se cambia con Direct3D 12 para permitir que otras características de Direct3D 12 tengan una sobrecarga de CPU baja. La clave de color automática y la multimuestreo no se admiten, aunque todavía se admiten el ajuste y la rotación.

### <a name="buffer-lifetime"></a>Duración del búfer

Las aplicaciones pueden almacenar descriptores creados previamente que hacen referencia a búferes de reserva. Esto se habilita al garantizar que el conjunto de búferes propiedad de una cadena de intercambio nunca cambia durante la duración de la cadena de intercambio. El conjunto de búferes devuelto por [**IDXGISwapChain::GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) no cambia hasta que se llama a ciertas API:

-   [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

El orden de los búferes devueltos [**por GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) nunca cambia.

[**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) devuelve el índice del búfer de reserva actual a la aplicación.

### <a name="swap-effects"></a>Efectos de intercambio

Los únicos efectos de intercambio admitidos [**son DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) [**y DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect), que requiere que el número de búferes sea mayor que uno.

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>Transición entre los modos de ventana y de pantalla completa

Direct3D 12 no admite el modo exclusivo de pantalla completa (FSE). En su lugar, cuando un juego es la única aplicación visible en pantalla, el sistema operativo usa una estrategia denominada optimizaciones de pantalla completa (FSO) para lograr un efecto similar al de FSE sin los inconvenientes de rendimiento. Para obtener más información sobre FSO, consulte [Desmitificación de](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/)optimizaciones de pantalla completa.

Direct3D 12 mantiene la restricción de que las aplicaciones deben llamar a [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) después de realizar la transición entre los modos de ventana y de pantalla completa (las cadenas de intercambio de modelos de volteo D3D11 tienen las mismas restricciones).

Las [**transiciones IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) no cambian el conjunto de búferes visibles para la aplicación en la cadena de intercambio. Solo las [**llamadas ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) y [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) crean o destruyen búferes visibles para la aplicación. Sin embargo, en [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) de Direct3D 12 no entra en modo exclusivo de pantalla completa y simplemente cambia las resoluciones y las tasas de actualización para permitir optimizaciones a pantalla completa. Estos cambios se pueden realizar mediante una aplicación sin el uso de este método

Cuando se llama a [**o IDXGISwapChain::P resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) o [**IDXGISwapChain1::P resent,**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) el búfer de reserva que se va a presentar debe estar en el estado [**D3D12 \_ RESOURCE STATE \_ \_ PRESENT.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) Si no es así, se producirá un error en la llamada no válida a **DXGI \_ \_ \_** ERROR.

Las cadenas de intercambio de pantalla completa siguen teniendo la restricción de que se debe llamar a [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(FALSE, NULL) antes de la versión final de la cadena de intercambio. **SetFullscreenState**(FALSE) se realiza correctamente en cadenas de intercambio que se ejecutan en dispositivos Direct3D 12.

Las operaciones presentes se producen en la cola 3D proporcionada en la creación de la cadena de intercambio, y las aplicaciones pueden presentar simultáneamente varias cadenas de intercambio y registrar y ejecutar listas de comandos.

Cuando la parte final del trabajo de gráficos (por ejemplo, el procesamiento posterior de fotogramas) se realiza en una cola de proceso o no implica la cola de gráficos del dispositivo, la creación de una segunda cola 3D en la que se va a presentar puede ser beneficiosa y evitar la latencia de presentación que retrasa el inicio del fotograma siguiente. 

### <a name="example"></a>Ejemplo

El código de ejemplo siguiente estaría presente en el bucle de representación principal:

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>Creación de cadenas de intercambio

Al usar las llamadas [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**CreateSwapChainForComposition,**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) tenga en cuenta que el parámetro *pDevice* realmente requiere un puntero a una cola de comandos directos en Direct3D 12 y no un dispositivo.

### <a name="presenting-on-windows-7"></a>Presentación en Windows 7

Cuando el destino es Direct3D 12 en Windows 7, los tipos DXGI necesarios para Direct3D 12 no están presentes, por lo que debe usar el ID3D12On7 proporcionado por **D3D12CommandQueueDownLevel** (que se consulta fuera de la cola de comandos directos) para presentar.

Proporcione una lista de comandos abierta al método presente Windows 7, que se usará, cerrará y se envía automáticamente al dispositivo. Debe proporcionar un búfer de reserva que debe crearse mediante la aplicación, debe ser un recurso confirmado, debe ser de ejemplo único y debe tener uno de los siguientes formatos.

* **DXGI_FORMAT_R16G16B16A16_FLOAT**
* **DXGI_FORMAT_R10G10B10A2_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**
* **DXGI_FORMAT_B8G8R8X8_UNORM**
* **DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**

## <a name="related-topics"></a>Temas relacionados

* [D3D12_HEAP_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)
* [Tutoriales de vídeo de aprendizaje avanzado de DirectX: Velocidad de fotogramas sinthrottled](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [Representación](rendering.md)

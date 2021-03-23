---
title: Cadenas de intercambio
description: Las cadenas de intercambio controlan la rotación del búfer de reserva, formando la base de la animación de gráficos.
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbc7ec1b62ba620b42bc85c1c1f491ff7ba952d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104549127"
---
# <a name="swap-chains"></a>Cadenas de intercambio

Las cadenas de intercambio controlan la rotación del búfer de reserva, formando la base de la animación de gráficos.

## <a name="overview"></a>Información general

El modelo de programación para las cadenas de intercambio en Direct3D 12 no es idéntico al de las versiones anteriores de D3D. La comodidad de la programación, por ejemplo, la compatibilidad con la rotación de recursos automática que se encontraba en D3D10 y D3D11 no se admite ahora. Las aplicaciones habilitadas para la rotación automática de recursos para representar el mismo objeto de API mientras que la superficie real que se representa cambia cada fotograma. El comportamiento de las cadenas de intercambio cambia con Direct3D 12 para permitir que otras características de Direct3D 12 tengan una sobrecarga de CPU baja. La clave de color automática y el muestreo múltiple no se admiten, aunque en particular la ampliación y la rotación siguen siendo.

### <a name="buffer-lifetime"></a>Duración del búfer

Las aplicaciones pueden almacenar descriptores creados previamente que hacen referencia a búferes de reserva que se habilitan al garantizar que el conjunto de búferes que pertenecen a una cadena de intercambio no cambia nunca durante la duración de la cadena de intercambio. El conjunto de búferes devueltos por [**IDXGISwapChain:: getBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) no cambia hasta que se llama a determinadas API:

-   [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

El orden de los búferes devueltos por [**getBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) nunca cambia.

[**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) devuelve el índice del búfer de retroceso actual a la aplicación.

### <a name="swap-effects"></a>Efectos de intercambio

Los únicos efectos de intercambio admitidos son [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) y [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect), que requiere que el número de búferes sea mayor que uno.

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>Transición entre los modos de ventana y de pantalla completa

Direct3D 12 no es compatible con el modo exclusivo de pantalla completa (FSE). En su lugar, cuando un juego es la única aplicación visible en pantalla, el sistema operativo usa una estrategia denominada optimizaciones de pantalla completa (FSO) para lograr un efecto similar en FSE sin las desventajas de rendimiento. Para obtener más información acerca de FSO, consulte [desmitificación de las optimizaciones de pantalla completa](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/).

Direct3D 12 mantiene la restricción de que las aplicaciones deben llamar a [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) después de la transición entre los modos de ventana y de pantalla completa (las cadenas de intercambio de D3D11 Flip-Model tienen las mismas restricciones).

Las transiciones [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) no cambian el conjunto de búferes visibles para la aplicación en la cadena de intercambio. Solo las llamadas a [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) y [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) crean o destruyen búferes visibles para la aplicación. Sin embargo, en Direct3D 12 [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) no entra en modo exclusivo de pantalla completa y simplemente cambia las resoluciones y las tasas de actualización para permitir las optimizaciones de pantalla completa. Estos cambios pueden realizarse mediante una aplicación sin el uso de este método.

When o [**IDXGISwapChain::P reenviar**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) o IDXGISwapChain1: se llama a [**reenviar:P**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) , el búfer de reserva que se va a presentar debe estar en el estado de la [**presentación de estado de recursos de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) . Present producirá un **error en la \_ \_ \_ llamada no válida de DXGI** si no es así.

Las cadenas de intercambio de pantalla completa continúan teniendo la restricción de que se debe llamar a [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(false, null) antes de la versión final de la cadena de intercambio. **SetFullscreenState**(false) se realiza correctamente en las cadenas de intercambio que se ejecutan en dispositivos de Direct3D 12.

Las operaciones de presentación se producen en la cola 3D proporcionada en la creación de intercambio y las aplicaciones pueden presentar simultáneamente varias cadenas de intercambio y grabar y ejecutar listas de comandos.

Cuando la parte final del trabajo de gráficos (por ejemplo, el procesamiento de fotogramas) se realiza en una cola de proceso o no implica la cola de gráficos del dispositivo, la creación de una segunda cola 3D para presentarla puede ser beneficiosa y evitar que la latencia de la presentación retrase el inicio del fotograma siguiente. 

### <a name="example"></a>Ejemplo

El siguiente código de ejemplo aparecería en el bucle de representación principal:

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>Crear cadenas de intercambio

Al usar las llamadas a [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) , tenga en cuenta que el parámetro *pDevice* realmente requiere un puntero a una cola de comandos directa en Direct3D 12, y no un dispositivo.

### <a name="presenting-on-windows-7"></a>Presentación en Windows 7

Cuando el destino es Direct3D 12 en Windows 7, los tipos de DXGI necesarios para Direct3D 12 no están presentes, por lo que debe usar el **ID3D12CommandQueueDownLevel** proporcionado por D3D12On7 (consultado fuera de la cola de comandos directa) para presentar.

Debe proporcionar una lista de comandos abierta al método de presentación de Windows 7, que se usará, se cerrará y se enviará automáticamente al dispositivo. Debe proporcionar un búfer de reserva que se debe crear en la aplicación, debe ser un recurso confirmado, tener una sola muestra y debe tener uno de los siguientes formatos.

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
* [Tutoriales de vídeo de aprendizaje avanzado de DirectX: velocidad de fotogramas no limitada](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [Representación](rendering.md)

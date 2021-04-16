---
description: Las tarjetas de identificación múltiple son aquellas que tienen un acelerador y un búfer de fotogramas comunes, convertidores digitales-analógicos (DAC) independientes y salidas de monitor.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494728"
---
# <a name="multihead-direct3d-9"></a>Multihead (Direct3D 9)

Las tarjetas de identificación múltiple son aquellas que tienen un acelerador y un búfer de fotogramas comunes, convertidores digitales-analógicos (DAC) independientes y salidas de monitor. Estos dispositivos pueden ofrecer compatibilidad con varios monitores más utilizable que un número similar de adaptadores de pantalla heterogéneos.

Las tarjetas de múltiples cabezales se exponen en la API como un único dispositivo de nivel de API que puede controlar varias cadenas de intercambio de pantalla completa. Por lo tanto, todos los recursos se comparten con todos los cabezales y cada encabezado tiene exactamente las mismas funcionalidades. Cada encabezado se puede establecer en modos de presentación independientes. Puede usar llamadas independientes a [**IDirect3DSwapChain9::P reenviar**](/windows/desktop/api) para actualizar cada cabeza. También puede usar una llamada a [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para actualizar cada encabezado secuencialmente.

> [!Note]  
> La actualización de cada encabezado no se realiza simultáneamente con una única llamada a [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Presentar estadísticas en Direct3D 9Ex puede usar la estructura [**D3DPRESENTSTATS**](d3dpresentstats.md) para mantener las actualizaciones en cada una de ellas cerca de otras para limitar los efectos de desgarro en varios cabezales de adaptadores. Para obtener información sobre cómo sincronizar marcos de aplicaciones de 9Ex Flip Model de Direct3D, consulte [mejoras de 9Ex de Direct3D](../direct3darticles/direct3d-9ex-improvements.md).

 

Cada cadena de intercambio para un dispositivo con más cabezales debe estar en pantalla completa. Cuando un dispositivo ha entrado en modo de Multihead, debe permanecer en pantalla completa. La transición de vuelta al modo de ventana requiere la destrucción del dispositivo (excepto la operación normal ALT + TAB para minimizar).

El método anterior para dividir la memoria de vídeo entre los cabezales y tratar cada cabeza como un acelerador totalmente independiente seguirá siendo un escenario de uso común. Esta propuesta no sustituye a ese mecanismo a menos que la aplicación se haya codificado específicamente para que funcione en el modo de Multihead de Direct3D 9.

A los controladores se les proporciona el conocimiento adecuado para cambiar entre los dos modos de funcionamiento.

Un encabezado se llamará la cabeza maestra y todos los demás cabezales de la misma tarjeta se denominarán cabezas subordinadas. Si hay más de un adaptador de varios cabezales en un sistema, el maestro y sus subordinados de un adaptador de varios cabezales se denominan grupo. Los grupos se indican mediante el ordinal del adaptador de su cabeza maestra.

La estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) se ha actualizado para exponer los nuevos límites de hardware siguientes.


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   NumberOfAdaptersInGroup es 1 para los adaptadores convencionales y mayor que 1 para el adaptador maestro de una tarjeta de varios cabezales. El valor será 0 para un adaptador subordinado de una tarjeta de varios cabezales. Cada tarjeta puede tener como máximo un maestro, pero puede tener muchos subordinados.
-   MasterAdapterOrdinal indica qué dispositivo es el maestro de este subordinado.
-   AdapterOrdinalInGroup indica el orden en el que la API hace referencia a los encabezados. El adaptador Maestro siempre tiene AdapterOrdinalInGroup 0. Estos valores no se corresponden con los ordinales del adaptador que se pasan a los métodos IDirect3D9, pero solo se aplican a los encabezados de un grupo.

Esta definición permite que las tarjetas de múltiples cabezales sigan presentando varios adaptadores como si fueran tarjetas independientes, al igual que en DirectX 8.

Para crear un dispositivo con más cabezal, especifique la marca de comportamiento D3DCREATE \_ ADAPTERGROUP \_ Device in [**IDirect3D9:: CreateDevice**](/windows/desktop/api). Los parámetros de presentación (una matriz [**de \_ parámetros D3DPRESENT**](d3dpresent-parameters.md)) deben contener elementos NumberOfAdaptersInGroup. El tiempo de ejecución asignará cada elemento a cada encabezado en el orden numérico AdapterOrdinalInGroup. Cuando \_ \_ se establece D3DCREATE ADAPTERGROUP Device, cada parámetro de presentación debe tener:

-   El miembro de ventana establecido en **false** (es decir, debe ser una pantalla completa).
-   El mismo valor para el miembro EnableAutoDepthStencil de [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md).

Además, si EnableAutoDepthStencil es **true**, cada uno de los campos siguientes debe tener el mismo valor para cada uno de los [**\_ parámetros de D3DPRESENT**](d3dpresent-parameters.md):

-   AutoDepthStencilFormat
-   BackBufferWidth
-   BackBufferHeight
-   BackBufferFormat

Si se establece DAC, las llamadas adicionales a [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) no son válidas.

Si el dispositivo se creó con la DAC, [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) esperará una matriz de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md).

Cada estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) que se pasa a [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) debe ser de pantalla completa. Para volver al modo de ventana, la aplicación debe destruir el dispositivo y volver a crear un dispositivo que no sea de multidirector en modo de ventana.

Este es un escenario de uso básico:


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



Para obtener más información, vea [**IDirect3D9:: CreateDevice**](/windows/desktop/api) y [**IDirect3DDevice9:: GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 

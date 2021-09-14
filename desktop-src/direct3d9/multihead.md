---
description: Las tarjetas de varias puntas son aquellas que tienen un búfer y un acelerador de fotogramas comunes, convertidores digitales a análogos independientes (DAC) y salidas de supervisión.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966584"
---
# <a name="multihead-direct3d-9"></a>Multihead (Direct3D 9)

Las tarjetas de varias puntas son aquellas que tienen un búfer y un acelerador de fotogramas comunes, convertidores digitales a análogos independientes (DAC) y salidas de supervisión. Estos dispositivos pueden ofrecer una compatibilidad con varios monitores mucho más utilizable que un número similar de adaptadores de pantalla heterogéneos.

Las tarjetas multihead se exponen en la API como un único dispositivo de nivel de API que puede impulsar varias cadenas de intercambio de pantalla completa. Por lo tanto, todos los recursos se comparten con todos los jefes y cada uno tiene exactamente las mismas funcionalidades. Cada cabeza se puede establecer en modos de presentación independientes. Puede usar llamadas independientes a [**IDirect3DSwapChain9::P resent**](/windows/desktop/api) para actualizar cada head. También puede usar una llamada a [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para actualizar cada cabeza secuencialmente.

> [!Note]  
> La actualización de cada principal no se produce simultáneamente con una sola llamada a [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Las estadísticas presentes en Direct3D 9Ex pueden usar la estructura [**D3DPRESENTSTATS**](d3dpresentstats.md) para mantener las actualizaciones de cada cabeza cerca unas de otras para limitar los efectos de desgarro en varias cabezas de adaptadores. Para obtener información sobre cómo sincronizar fotogramas de aplicaciones de modelo de volteo de Direct3D 9Ex, vea [Mejoras de Direct3D 9Ex.](../direct3darticles/direct3d-9ex-improvements.md)

 

Cada cadena de intercambio de un dispositivo de varias puntas debe ser de pantalla completa. Cuando un dispositivo ha entrado en modo multihead, debe permanecer en pantalla completa. La transición al modo de ventana requiere la destrucción del dispositivo (excepto para la operación normal ALT+TAB para minimizar).

El método anterior de dividir la memoria de vídeo entre los caras y tratar cada cabeza como un acelerador totalmente independiente seguirá siendo un escenario de uso común. Esta propuesta no reemplaza ese mecanismo a menos que la aplicación se haya codificado específicamente para funcionar en el modo multihead de Direct3D 9.

Los controladores tienen conocimientos adecuados para cambiar entre los dos modos de funcionamiento.

Una cabeza se denominará principal y todas las demás caras de la misma tarjeta se denominarán jefes subordinados. Si hay más de un adaptador multihead en un sistema, el maestro y sus subordinados de un adaptador multihead se denominan un grupo. Los grupos se indican mediante el ordinal del adaptador de su principal.

La [**estructura D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) se ha actualizado para exponer los siguientes nuevos límites de hardware.


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   NumberOfAdaptersInGroup es 1 para los adaptadores convencionales y mayor que 1 para el adaptador maestro de una tarjeta multihead. El valor será 0 para un adaptador subordinado de una tarjeta multihead. Cada tarjeta puede tener como máximo un maestro, pero puede tener muchos subordinados.
-   MasterAdapterOrdinal indica qué dispositivo es el maestro para este subordinado.
-   AdapterOrdinalInGroup indica el orden en el que la API hace referencia a los caras. El adaptador maestro siempre tiene AdapterOrdinalInGroup 0. Estos valores no se corresponden con los ordinales del adaptador pasados a los métodos IDirect3D9, sino que solo se aplican a los responsables de un grupo.

Esta definición permite que las tarjetas de varias puntas sigan presentando varios adaptadores como si fueran tarjetas independientes, como lo hacían en DirectX 8.

Para crear un dispositivo multihead, especifique la marca de comportamiento D3DCREATE ADAPTERGROUP DEVICE en \_ \_ [**IDirect3D9::CreateDevice**](/windows/desktop/api). Los parámetros de presentación (una matriz [**de parámetros D3DPRESENT \_**](d3dpresent-parameters.md)) deben contener elementos NumberOfAdaptersInGroup. El tiempo de ejecución asignará cada elemento a cada elemento principal en el orden numérico AdapterOrdinalInGroup. Cuando se establece D3DCREATE \_ ADAPTERGROUP \_ DEVICE, cada parámetro de presentación debe tener:

-   El miembro Windowed establecido en **FALSE** (en otras palabras, será de pantalla completa).
-   El mismo valor para el miembro EnableAutoDepthStencil de [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).

Además, si EnableAutoDepthStencil es **TRUE,** cada uno de los campos siguientes debe tener el mismo valor para cada [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md):

-   AutoDepthStencilFormat
-   BackBufferWidth
-   BackBufferHeight
-   BackBufferFormat

Si se establece DAC, las llamadas adicionales a [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) no son compatibles.

Si el dispositivo se creó con la DAC, [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) esperará una matriz de [**PARÁMETROS D3DPRESENT \_**](d3dpresent-parameters.md).

Cada [**estructura PARAMETERS D3DPRESENT \_ pasada**](d3dpresent-parameters.md) a [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) debe ser de pantalla completa. Para volver al modo de ventana, la aplicación debe destruir el dispositivo y volver a crear un dispositivo no multihead en modo de ventana.

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



Para obtener más información, vea [**IDirect3D9::CreateDevice**](/windows/desktop/api) e [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 

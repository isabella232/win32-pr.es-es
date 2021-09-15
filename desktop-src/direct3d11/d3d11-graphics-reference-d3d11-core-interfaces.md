---
title: Interfaces principales de Direct3D 11
description: Esta sección contiene información sobre las interfaces principales.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- interfaces, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2485e633158d3eb1f8448249812eb6699b37a6ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575296"
---
# <a name="direct3d-11-core-interfaces"></a>Interfaces principales de Direct3D 11

Esta sección contiene información sobre las interfaces principales.

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a><br /> | Esta interfaz encapsula métodos para recuperar datos de la GPU de forma asincrónica.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a><br /> | La interfaz blend-state contiene una descripción del estado de mezcla que puede enlazar a la fase <a href="d3d10-graphics-programming-guide-output-merger-stage.md">de fusión de salida.</a><br /> | 
| <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a><br /> | La interfaz blend-state contiene una descripción del estado de mezcla que puede enlazar a la fase <a href="d3d10-graphics-programming-guide-output-merger-stage.md">de fusión de salida.</a> Esta interfaz de estado de mezcla admite operaciones lógicas, así como operaciones de combinación.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a><br /> | La <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>interfaz ID3D11CommandList</strong></a> encapsula una lista de comandos gráficos para reproducir.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a><br /> | Esta interfaz encapsula métodos para medir el rendimiento de GPU.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a><br /> | La interfaz depth-stencil-state contiene una descripción del estado de la galería de símbolos de profundidad que puede enlazar a la fase de fusión <a href="d3d10-graphics-programming-guide-output-merger-stage.md">de salida.</a><br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a><br /> | La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos.<br /> | 
| <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a><br /> | La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.<br /> | 
| <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a><br /> | La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.<br /> | 
| <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a><br /> | La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2.</strong></a><br /> | 
| <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a><br /> | La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3,</strong></a>como <strong>RegisterDeviceRemovedEvent</strong> y <strong>UnregisterDeviceRemoved</strong>. <br /> | 
| <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a><br /> | La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5 agrega</strong></a> nuevos métodos a los de <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a><br /> | Una interfaz de dispositivo-secundario accede a los datos usados por un dispositivo.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a><br /> | La <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>interfaz ID3D11DeviceContext</strong></a> representa un contexto de dispositivo que genera comandos de representación.<br /><blockquote>[!Note]<br />La versión más reciente de esta interfaz <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>es ID3D11DeviceContext4</strong></a> introducida en el Windows 10 Creators Update. Las aplicaciones que Windows 10 Creators Update deben usar la <strong>interfaz ID3D11DeviceContext4</strong> en lugar de <strong>ID3D11Device</strong>.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a><br /> | La interfaz de contexto de dispositivo representa un contexto de dispositivo; se usa para representar comandos. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.<br /> | 
| <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a><br /> | La interfaz de contexto de dispositivo representa un contexto de dispositivo; se usa para representar comandos. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.<br /> | 
| <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a><br /> | La interfaz de contexto de dispositivo representa un contexto de dispositivo; se usa para representar comandos. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2.</strong></a> <br /> | 
| <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a><br /> | La interfaz de contexto de dispositivo representa un contexto de dispositivo; se usa para representar comandos. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3.</strong></a><br /> | 
| <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a><br /> | La <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>interfaz ID3DDeviceContextState</strong></a> representa un objeto de estado de contexto, que contiene información de estado y comportamiento sobre un dispositivo Microsoft Direct3D.<br /> | 
| <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a><br /> | Representa una barrera, un objeto utilizado para la sincronización de la CPU y una o varias GPU.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a><br /> | Una interfaz de diseño de entrada contiene una definición de cómo alimentar los datos de vértices que se disposición en memoria en la fase de <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">ensamblador</a> de entrada de la canalización <a href="overviews-direct3d-11-graphics-pipeline.md">de gráficos</a>.<br /> | 
| <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a><br /> | Proporciona protección contra subprocesos para secciones críticas de una aplicación multiproceso.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a><br /> | Una interfaz de predicado determina si se debe procesar la geometría en función de los resultados de una llamada a draw anterior.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a><br /> | Una interfaz de consulta consulta información de la GPU.<br /> | 
| <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a><br /> | Representa un objeto de consulta para consultar información de la unidad de procesamiento gráfico (GPU).<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a><br /> | La interfaz de estado del rasterizador contiene una descripción del estado del rasterizador que puede enlazar a la fase <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">del rasterizador</a>.<br /> | 
| <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a><br /> | La interfaz de estado del rasterizador contiene una descripción del estado del rasterizador que puede enlazar a la fase <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">del rasterizador</a>. Esta interfaz de estado rasterizador admite el recuento forzado de muestras.<br /> | 
| <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a><br /> | La interfaz de estado del rasterizador contiene una descripción del estado del rasterizador que puede enlazar a la fase <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">del rasterizador</a>. Esta interfaz de estado rasterizador admite el recuento forzado de muestras y el modo de rasterización conservadora.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a><br /> | La interfaz sampler-state contiene una descripción del estado del muestreador <a href="overviews-direct3d-11-graphics-pipeline.md"></a> que puede enlazar a cualquier fase del sombreador de la canalización para que las operaciones de muestra de textura las haga referencia.<br /> | 




 

Direct3D 11 implementa interfaces para:

-   [Recursos](d3d11-graphics-reference-resource-interfaces.md)
-   [Sombreadores](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia principal](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>


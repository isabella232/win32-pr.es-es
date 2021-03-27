---
title: Interfaces principales de Direct3D 11
description: Esta sección contiene información sobre las interfaces principales.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- interfaces, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104488426"
---
# <a name="direct3d-11-core-interfaces"></a>Interfaces principales de Direct3D 11

Esta sección contiene información sobre las interfaces principales.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a><br/></td>
<td>Esta interfaz encapsula los métodos para recuperar datos de la GPU de forma asincrónica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a><br/></td>
<td>La interfaz de estado de Blend contiene una descripción del estado de mezcla que se puede enlazar a la <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase de combinación de salida</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a><br/></td>
<td>La interfaz de estado de Blend contiene una descripción del estado de mezcla que se puede enlazar a la <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase de combinación de salida</a>. Esta interfaz de estado de Blend admite operaciones lógicas, así como operaciones de fusión.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a><br/></td>
<td>La interfaz <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> encapsula una lista de comandos de gráficos para reproducir.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a><br/></td>
<td>Esta interfaz encapsula métodos para medir el rendimiento de la GPU.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a><br/></td>
<td>La interfaz Depth-cliché-State contiene una descripción del estado de la galería de símbolos de profundidad que se puede enlazar a la <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase de combinación de salida</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a><br/></td>
<td>La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a><br/></td>
<td>La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a><br/></td>
<td>La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a><br/></td>
<td>La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a><br/></td>
<td>La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, como <strong>RegisterDeviceRemovedEvent</strong> y <strong>UnregisterDeviceRemoved</strong>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a><br/></td>
<td>La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a><br/></td>
<td>Una interfaz de dispositivo-secundario obtiene acceso a los datos que usa un dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a><br/></td>
<td>La interfaz <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> representa un contexto de dispositivo que genera comandos de representación.<br/>
<blockquote>
[!Note]<br />
La versión más reciente de esta interfaz es <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introducida en Windows 10 Creators Update. Las aplicaciones destino Windows 10 Creators Update deben usar la interfaz <strong>ID3D11DeviceContext4</strong> en lugar de <strong>ID3D11Device</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a><br/></td>
<td>La interfaz de contexto de dispositivo representa un contexto de dispositivo. se utiliza para representar comandos. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a><br/></td>
<td>La interfaz de contexto de dispositivo representa un contexto de dispositivo. se utiliza para representar comandos. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a><br/></td>
<td>La interfaz de contexto de dispositivo representa un contexto de dispositivo. se utiliza para representar comandos. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a><br/></td>
<td>La interfaz de contexto de dispositivo representa un contexto de dispositivo. se utiliza para representar comandos. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a><br/></td>
<td>La interfaz <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> representa un objeto de estado de contexto, que contiene información sobre el estado y el comportamiento de un dispositivo de Microsoft Direct3D.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a><br/></td>
<td>Representa una barrera, un objeto que se usa para la sincronización de la CPU y una o varias GPU.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a><br/></td>
<td>Una interfaz de diseño de entrada contiene una definición de cómo alimentar los datos de vértices que se colocan en la memoria en la <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">fase de ensamblador de entrada</a> de la <a href="overviews-direct3d-11-graphics-pipeline.md">canalización de gráficos</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a><br/></td>
<td>Proporciona protección de subprocesos para las secciones críticas de una aplicación multiproceso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a><br/></td>
<td>Una interfaz de predicado determina si la geometría se debe procesar en función de los resultados de una llamada a Draw anterior.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a><br/></td>
<td>Una interfaz de consulta consulta información de la GPU.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a><br/></td>
<td>Representa un objeto de consulta para consultar información de la unidad de procesamiento de gráficos (GPU).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a><br/></td>
<td>La interfaz de estado de rasterizador contiene una descripción del estado de rasterizador que puede enlazar a la <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase de rasterizador</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a><br/></td>
<td>La interfaz de estado de rasterizador contiene una descripción del estado de rasterizador que puede enlazar a la <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase de rasterizador</a>. Esta interfaz de estado de rasterizador admite el recuento de muestras forzada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a><br/></td>
<td>La interfaz de estado de rasterizador contiene una descripción del estado de rasterizador que puede enlazar a la <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase de rasterizador</a>. Esta interfaz de estado de rasterizador admite el recuento de muestras forzada y el modo de rasterización conservador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a><br/></td>
<td>La interfaz de estado de muestra contiene una descripción de estado de muestra que se puede enlazar a cualquier fase del sombreador de la <a href="overviews-direct3d-11-graphics-pipeline.md">canalización</a> como referencia a las operaciones de ejemplo de textura.<br/></td>
</tr>
</tbody>
</table>



 

Direct3D 11 implementa interfaces para:

-   [Recursos](d3d11-graphics-reference-resource-interfaces.md)
-   [Sombreadores](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia básica](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>


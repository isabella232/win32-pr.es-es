---
title: Interfaces de capas
description: Esta sección contiene información sobre las interfaces de capas.
ms.assetid: 100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d
keywords:
- interfaces, capa de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57945866e8dea1b04c4066362105c8ac6e259a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997185"
---
# <a name="layer-interfaces"></a>Interfaces de capas

Esta sección contiene información sobre las interfaces de capas.


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
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a><br/></td>
<td>Una interfaz de depuración controla la configuración de depuración, valida el estado de la canalización y solo se puede usar si la capa de depuración está activada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a><br/></td>
<td>Una interfaz de cola de información almacena, recupera y filtra los mensajes de depuración. La cola está formada por una cola de mensajes, una pila de filtros de almacenamiento opcional y una pila de filtros de recuperación opcional.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a><br/></td>
<td>La interfaz de seguimiento predeterminada establece las opciones de seguimiento predeterminadas de referencia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a><br/></td>
<td>La interfaz de seguimiento establece las opciones de seguimiento de referencia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La interfaz <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> y sus métodos no se admiten en Direct3D 11.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a><br/></td>
<td>La interfaz de dispositivo de seguimiento establece la información de seguimiento del sombreador, que permite el registro y la reproducción precisos de la ejecución del sombreador.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de capas](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 






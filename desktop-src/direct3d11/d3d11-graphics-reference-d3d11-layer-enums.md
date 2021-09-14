---
title: Enumeraciones de capas
description: Esta sección contiene información sobre las enumeraciones de capas.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- enumeraciones, Capa 11 de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361282"
---
# <a name="layer-enumerations"></a>Enumeraciones de capas

Esta sección contiene información sobre las enumeraciones de capas.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CATEGORÍA DE MENSAJE D3D11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | Categorías de mensajes de depuración. Esto identificará la categoría de un mensaje al recuperar un mensaje con [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) y al agregar un mensaje con [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). Al crear un [**filtro de cola de información**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), estos valores se pueden usar para permitir o denegar cualquier categoría de mensajes que pasen a través de los filtros de almacenamiento y recuperación.<br/> |
| [**ID. DE MENSAJE D3D11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | Depurar mensajes para configurar un filtro de cola de información (consulte [**D3D11 \_ INFO \_ QUEUE \_ FILTER**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); use estos mensajes para permitir o denegar categorías de mensajes para pasar a través de los filtros de almacenamiento y recuperación. Estos identificadores los usan métodos como [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) o [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). <br/>                                                             |
| [**GRAVEDAD DEL MENSAJE D3D11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | Depuración de los niveles de gravedad del mensaje para una cola de información.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**MARCAS RLDO D3D11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | Opciones para la cantidad de información que se va a notificar sobre la duración de un objeto de dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**OPCIONES DE SEGUIMIENTO DE SOMBREADORES D3D11 \_ \_ \_**](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | Opciones que especifican cómo realizar el seguimiento de depuración del sombreador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**TIPO DE RECURSO DE SEGUIMIENTO DE SOMBREADORES D3D11 \_ \_ \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | Indica los tipos de recursos de los que se va a realizar el seguimiento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de capas](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 






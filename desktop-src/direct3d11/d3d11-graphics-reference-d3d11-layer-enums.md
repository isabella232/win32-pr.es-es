---
title: Enumeraciones de capas
description: Esta sección contiene información sobre las enumeraciones de capas.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- enumeraciones, capa de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104984119"
---
# <a name="layer-enumerations"></a>Enumeraciones de capas

Esta sección contiene información sobre las enumeraciones de capas.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Categoría de mensaje D3D11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | Categorías de mensajes de depuración. Esto identificará la categoría de un mensaje cuando se recupere un mensaje con [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) y al agregar un mensaje con [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). Al crear un [**filtro de cola de información**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), estos valores se pueden usar para permitir o denegar que las categorías de mensajes pasen por los filtros de almacenamiento y recuperación.<br/> |
| [**\_Identificador de mensaje de D3D11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | Depuración de mensajes para configurar un filtro de info-Queue (consulte [**D3D11 \_ info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); Utilice estos mensajes para permitir o denegar que las categorías de mensajes pasan a través de los filtros de almacenamiento y recuperación. Estos identificadores son usados por métodos como [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) o [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). <br/>                                                             |
| [**\_Gravedad del mensaje de D3D11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | Depurar los niveles de gravedad del mensaje para una cola de información.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**D3D11 \_ marcas de RLDO \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | Opciones para la cantidad de información que se va a notificar sobre la duración de un objeto de dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_Opciones de seguimiento del sombreador de D3D11 \_ \_**](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | Opciones que especifican cómo realizar el seguimiento de depuración del sombreador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_Tipo de recurso de seguimiento del sombreador de D3D11 \_ \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | Indica los tipos de recursos de los que se va a realizar un seguimiento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de capas](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 






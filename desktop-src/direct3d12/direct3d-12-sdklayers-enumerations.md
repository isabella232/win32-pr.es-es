---
title: Enumeraciones de las capas de depuración
description: Las enumeraciones siguientes se declaran en d3d12sdklayers. h.
ms.assetid: 6E76C857-128E-4F0E-9711-72C4CF6C835C
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746c0def35c8eb282264cb4ab0b40eb5c08f0f9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651314"
---
# <a name="debug-layer-enumerations"></a>Enumeraciones de las capas de depuración

Las enumeraciones siguientes se declaran en d3d12sdklayers. h.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Tipo de \_ parámetro de lista de comandos de depuración D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)<br/>                                 | Indica el tipo de parámetro de depuración usado por [**ID3D12DebugCommandList1:: SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter) y [**ID3D12DebugCommandList1:: GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter).<br/>                                                                                                                                                                                                      |
| [**\_Tipo de \_ parámetro de dispositivo de depuración D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)<br/>                                              | Especifica el tipo de datos de la memoria a la que apunta el parámetro *pdata* de [**ID3D12DebugDevice1:: SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) y [**ID3D12DebugDevice1:: GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter).<br/>                                                                                                                                                                                        |
| [**\_Característica de depuración D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature)<br/>                                                                            | Marcas para las características opcionales de la capa de depuración D3D12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**D3D12 \_ \_ marcas de \_ validación basadas en GPU \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags)<br/>                                                | Describe el nivel de validación basada en GPU que se realizará en tiempo de ejecución.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_Estado de \_ canalización de validación basada en GPU D3D12 \_ \_ \_ \_ crear \_ marcas**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)<br/> | Especifica cómo controla la validación de GPU-Based los Estados de canalización revisados durante [**ID3D12Device:: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) y [**ID3D12Device:: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate).<br/>                                                                                                                                                                             |
| [**D3D12 \_ \_ modo de \_ \_ revisión del sombreador de validación basada \_ en GPU \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)<br/>                      | Especifica el tipo de revisión del sombreador utilizado por GPU-Based validación en el nivel de dispositivo o de lista de comandos.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_Categoría de mensaje D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category)<br/>                                                                      | Especifica categorías de mensajes de depuración. Esto identificará la categoría de un mensaje cuando se recupere un mensaje con [**ID3D12InfoQueue:: GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) y al agregar un mensaje con [**ID3D12InfoQueue:: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). Al crear un filtro de cola de información, estos valores se pueden usar para permitir o denegar que las categorías de mensajes pasen por los filtros de almacenamiento y recuperación. <br/> |
| [**\_Identificador de mensaje de D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id)<br/>                                                                                  | Especifica los identificadores de mensaje de depuración para configurar un filtro de info-Queue (consulte [**D3D12 \_ info \_ Queue \_ Filter**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)); Utilice estos mensajes para permitir o denegar que las categorías de mensajes pasen por los filtros de almacenamiento y recuperación. Estos identificadores son usados por métodos como [**ID3D12InfoQueue:: GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) o [**ID3D12InfoQueue:: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). <br/>                        |
| [**\_Gravedad del mensaje de D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity)<br/>                                                                      | Depurar los niveles de gravedad del mensaje para una cola de información.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| [**D3D12 \_ marcas de RLDO \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags)<br/>                                                                                  | Especifica las opciones para la cantidad de información que se va a notificar sobre la duración de un objeto de dispositivo activo. <br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno de programación de Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referencia de la capa de depuración](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 






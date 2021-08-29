---
title: Enumeraciones de las capas de depuración
description: Las enumeraciones siguientes se declaran en d3d12sdklayers.h.
ms.assetid: 6E76C857-128E-4F0E-9711-72C4CF6C835C
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108e8bce1627c37cd0c6f9ffbacfeb1bea991bb0fca97adda116a3c8f0e1b9fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069645"
---
# <a name="debug-layer-enumerations"></a>Enumeraciones de las capas de depuración

Las enumeraciones siguientes se declaran en d3d12sdklayers.h.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D12 \_ DEBUG \_ COMMAND \_ LIST \_ PARAMETER \_ TYPE**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)<br/>                                 | Indica el tipo de parámetro de depuración utilizado por [**ID3D12DebugCommandList1::SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter) e [**ID3D12DebugCommandList1::GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter).<br/>                                                                                                                                                                                                      |
| [**TIPO DE PARÁMETRO DE DISPOSITIVO \_ DE DEPURACIÓN D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)<br/>                                              | Especifica el tipo de datos de la memoria a la que apunta el parámetro *pData* de [**ID3D12DebugDevice1::SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) e [**ID3D12DebugDevice1::GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter).<br/>                                                                                                                                                                                        |
| [**CARACTERÍSTICA DE DEPURACIÓN D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature)<br/>                                                                            | Marcas para las características opcionales de la capa de depuración D3D12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**MARCAS DE VALIDACIÓN BASADAS EN \_ GPU D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags)<br/>                                                | Describe el nivel de validación basada en GPU que se debe realizar en tiempo de ejecución.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**MARCAS CREATE DE ESTADO DE CANALIZACIÓN DE VALIDACIÓN BASADA EN GPU D3D12 \_ \_ \_ \_ \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)<br/> | Especifica cómo GPU-Based validación controla los estados de canalización con revisión durante [**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate).<br/>                                                                                                                                                                             |
| [**MODO DE REVISIÓN DEL SOMBREADOR DE VALIDACIÓN BASADO EN GPU D3D12 \_ \_ \_ \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)<br/>                      | Especifica el tipo de aplicación de revisiones de sombreador que GPU-Based validación en el nivel de lista de dispositivos o comandos.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**CATEGORÍA DE MENSAJES D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category)<br/>                                                                      | Especifica categorías de mensajes de depuración. Esto identificará la categoría de un mensaje al recuperar un mensaje con [**ID3D12InfoQueue::GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) y al agregar un mensaje con [**ID3D12InfoQueue::AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). Al crear un filtro de cola de información, estos valores se pueden usar para permitir o denegar cualquier categoría de mensajes para pasar a través de los filtros de almacenamiento y recuperación. <br/> |
| [**ID. DE MENSAJE D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id)<br/>                                                                                  | Especifica los valores de los mensajes de depuración para configurar un filtro de cola de información (consulte FILTRO DE COLA DE INFORMACIÓN de [**D3D12); \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)use estos mensajes para permitir o denegar categorías de mensajes para pasar a través de los filtros de almacenamiento y recuperación. Estos identificadores los usan métodos como [**ID3D12InfoQueue::GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) o [**ID3D12InfoQueue::AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). <br/>                        |
| [**GRAVEDAD DEL MENSAJE D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity)<br/>                                                                      | Depuración de los niveles de gravedad del mensaje para una cola de información.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| [**MARCAS RLDO D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags)<br/>                                                                                  | Especifica opciones para la cantidad de información que se va a notificar sobre la duración de un objeto de dispositivo en directo. <br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno de programación de Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referencia de la capa de depuración](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 






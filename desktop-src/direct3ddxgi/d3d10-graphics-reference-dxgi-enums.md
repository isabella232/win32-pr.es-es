---
description: Esta sección contiene información sobre las enumeraciones proporcionadas por DXGI.
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: Enumeraciones de DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49f8309552662d0edd9833ce037a256c3c09c48
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805594"
---
# <a name="dxgi-enumerations"></a>Enumeraciones de DXGI

Esta sección contiene información sobre las enumeraciones proporcionadas por DXGI.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                         | Descripción                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_marca de adaptador de DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | Identifica el tipo de adaptador de DXGI.<br/>                                                                                                                                   |
| [**\_Personalizado3 del adaptador de DXGI \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | Identifica el tipo de adaptador de DXGI.<br/>                                                                                                                                   |
| [**\_modo alfa de DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | Identifica el valor alfa, el comportamiento de transparencia, de una superficie.<br/>                                                                                                       |
| [**\_tipo de \_ espacio de colores de DXGI \_**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | Especifica los tipos de espacio de colores.<br/>                                                                                                                                           |
| [**\_ \_ GRANULARIDAD de adelantamiento de proceso de DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | Identifica la granularidad con la que se puede tener preferencia a la unidad de procesamiento de gráficos (GPU) de realizar su tarea de proceso actual.<br/>                                      |
| [**marcas de DXGI \_ Debug \_ RLO \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | Marcas usadas con [**ReportLiveObjects**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) para especificar la cantidad de información que se va a notificar sobre la duración de un objeto. <br/>                         |
| [**característica de DXGI \_**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | Especifica un intervalo de características de hardware que se utilizará al comprobar la compatibilidad de las características.<br/>                                                                                  |
| [**formato de DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | Formatos de datos de recursos, incluidos los formatos con tipos completos y sin tipo. Una lista de modificadores en la parte inferior de la página describe más detalladamente cada tipo de formato. <br/>               |
| [**\_modo de presentación de fotogramas de DXGI \_ \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | Indica las opciones para presentar fotogramas a la cadena de intercambio. <br/>                                                                                                            |
| [**\_preferencias de GPU de DXGI \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | Preferencia de la GPU en la que se va a ejecutar la aplicación.<br/>                                                                                                                           |
| [**\_granularidad de \_ prevacía de \_ gráficos de DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | Identifica la granularidad con la que se puede retrasar la GPU para realizar su tarea actual de representación de gráficos.<br/>                                                      |
| [**\_marcas de \_ \_ compatibilidad con \_ composición de hardware de DXGI**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | describe qué niveles de composición de hardware son compatibles.<br/>                                                                                                          |
| [**\_tipo de \_ metadatos de HDR de DXGI \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | Especifica el tipo de metadatos de encabezado.<br/>                                                                                                                                    |
| [**Categoría de mensajes de la \_ cola de información de DXGI \_ \_ \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | Valores que especifican categorías de mensajes de depuración.<br/>                                                                                                                      |
| [**\_gravedad del \_ mensaje de cola de información de DXGI \_ \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | Valores que especifican los niveles de gravedad de los mensajes de depuración para una cola de información.<br/>                                                                                            |
| [**\_grupo de \_ segmentos de memoria de DXGI \_**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | Especifica el grupo de segmentos de memoria que se va a usar.<br/>                                                                                                                             |
| [**\_rotación del modo de DXGI \_**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | Marcas que indican cómo se deben girar los búferes de reserva para ajustarse a la rotación física de un monitor.<br/>                                                                  |
| [**\_escala del modo de DXGI \_**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | Marcas que indican cómo se ajusta una imagen para ajustarla a la resolución de un monitor determinado.<br/>                                                                                        |
| [**\_ \_ orden SCANLINE del modo DXGI \_**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | Marcas que indican el método que el trazo utiliza para crear una imagen en una superficie.<br/>                                                                                           |
| [**\_ \_ Marcas YCbCr de superposición de DXGI \_ \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | Opciones de espacio de colores de la cadena de intercambio.<br/>                                                                                                                                    |
| [**marcas de recursos de la oferta de DXGI \_ \_ \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | Especifica marcas para el método [**OfferResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) .<br/>                                                                                |
| [**\_prioridad de \_ recursos de oferta de DXGI \_**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | Identifica la importancia del contenido de un recurso s cuando se llama al método [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) para ofrecer el recurso. <br/> |
| [**\_tipo de \_ forma de puntero OUTDUPL \_ de DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | Identifica el tipo de forma de puntero.<br/>                                                                                                                                  |
| [**marca de compatibilidad de espacio de colores de la \_ superposición de DXGI \_ \_ \_ \_**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | Especifica la compatibilidad con el espacio de colores superpuesto.<br/>                                                                                                                             |
| [**\_marca de \_ soporte técnico de la superposición de DXGI \_**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | Especifica la compatibilidad con la superposición para buscar en una llamada a [**IDXGIOutput3:: CheckOverlaySupport**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport).<br/>                                     |
| [**resultados de recursos de la recuperación de DXGI \_ \_ \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | Especifica marcas de resultado para el método [**ReclaimResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) .<br/>                                                                     |
| [**residencia de DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | Marcas que indican la ubicación de memoria de un recurso.<br/>                                                                                                                    |
| [**\_escalado de DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | Identifica el comportamiento de cambiar el tamaño cuando el tamaño del búfer de reserva no coincide con el tamaño de la salida de destino.<br/>                                                                     |
| [**\_marca de \_ \_ compatibilidad de \_ espacio de colores \_ \_ de la cadena de intercambio de DXGI**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | Especifica la compatibilidad del espacio de colores para la cadena de intercambio.<br/>                                                                                                                      |
| [**\_marca de \_ cadena de intercambio de DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | Opciones de comportamiento de la cadena de intercambio.<br/>                                                                                                                                       |
| [**\_efecto de intercambio de DXGI \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | Opciones para controlar los píxeles en una superficie de presentación después de llamar a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). <br/>                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 


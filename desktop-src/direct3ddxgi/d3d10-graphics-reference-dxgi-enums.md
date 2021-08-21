---
description: Esta sección contiene información sobre las enumeraciones proporcionadas por DXGI.
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: Enumeraciones DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9347fdf39f2cde6bb50e3ae4c65f2601c570e084516bf817c4dc66169a83925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987145"
---
# <a name="dxgi-enumerations"></a>Enumeraciones DXGI

Esta sección contiene información sobre las enumeraciones proporcionadas por DXGI.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                         | Descripción                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MARCA DEL ADAPTADOR DE DXGI \_ \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | Identifica el tipo de adaptador DXGI.<br/>                                                                                                                                   |
| [**DXGI \_ ADAPTER \_ FLAG3**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | Identifica el tipo de adaptador DXGI.<br/>                                                                                                                                   |
| [**MODO \_ ALFA DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | Identifica el valor alfa, el comportamiento de transparencia, de una superficie.<br/>                                                                                                       |
| [**TIPO DE \_ ESPACIO DE \_ COLOR \_ DXGI**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | Especifica los tipos de espacio de color.<br/>                                                                                                                                           |
| [**GRANULARIDAD DE \_ \_ ADELANTAMIENTO DE \_ PROCESO DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | Identifica la granularidad en la que se puede adelantar a la unidad de procesamiento gráfico (GPU) para que no realice su tarea de proceso actual.<br/>                                      |
| [**MARCAS DE \_ RLO DE \_ DEPURACIÓN \_ DXGI**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | Marcas usadas con [**ReportLiveObjects para**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) especificar la cantidad de información que se va a notificar sobre la duración de un objeto. <br/>                         |
| [**CARACTERÍSTICA \_ DXGI**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | Especifica una serie de características de hardware que se usarán al comprobar la compatibilidad con características.<br/>                                                                                  |
| [**FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | Formatos de datos de recursos, incluidos los formatos totalmente tipo y sin tipo. Una lista de modificadores en la parte inferior de la página describe más completamente cada tipo de formato. <br/>               |
| [**MODO DE PRESENTACIÓN DE MARCO DXGI \_ \_ \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | Indica las opciones para presentar fotogramas a la cadena de intercambio. <br/>                                                                                                            |
| [**PREFERENCIA DE \_ GPU DXGI \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | Preferencia de GPU para que se ejecute la aplicación.<br/>                                                                                                                           |
| [**GRANULARIDAD DE \_ ADELANTAMIENTO \_ DE GRÁFICOS \_ DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | Identifica la granularidad en la que se puede adelantar a la GPU para que no realice su tarea de representación de gráficos actual.<br/>                                                      |
| [**MARCAS DE COMPATIBILIDAD \_ CON LA COMPOSICIÓN DE HARDWARE \_ \_ DXGI \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | describe qué niveles de composición de hardware son compatibles.<br/>                                                                                                          |
| [**TIPO DE \_ \_ METADATOS DXGI HDR \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | Especifica el tipo de metadatos de encabezado.<br/>                                                                                                                                    |
| [**CATEGORÍA DE MENSAJES \_ DE COLA DE INFORMACIÓN \_ \_ \_ DXGI**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | Valores que especifican categorías de mensajes de depuración.<br/>                                                                                                                      |
| [**GRAVEDAD DEL MENSAJE \_ DE COLA DE INFORMACIÓN \_ \_ \_ DXGI**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | Valores que especifican los niveles de gravedad del mensaje de depuración para una cola de información.<br/>                                                                                            |
| [**GRUPO DE \_ SEGMENTOS \_ DE MEMORIA \_ DXGI**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | Especifica el grupo de segmentos de memoria que se usará.<br/>                                                                                                                             |
| [**ROTACIÓN DEL \_ MODO \_ DXGI**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | Marcas que indican cómo se deben girar los búferes de reserva para ajustarse a la rotación física de un monitor.<br/>                                                                  |
| [**ESCALADO DEL \_ MODO DXGI \_**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | Marcas que indican cómo se ajusta una imagen para ajustarse a la resolución de un monitor determinado.<br/>                                                                                        |
| [**MODO DXGI \_ \_ SCANLINE \_ ORDER**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | Marcas que indican el método que usa el trama para crear una imagen en una superficie.<br/>                                                                                           |
| [**DXGI \_ MULTIPLANE \_ OVERLAY \_ YCbCr \_ FLAGS**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | Opciones para el espacio de colores de la cadena de intercambio.<br/>                                                                                                                                    |
| [**MARCAS DE RECURSOS \_ DE OFERTA \_ \_ DE DXGI**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | Especifica marcas para el [**método OfferResources1.**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1)<br/>                                                                                |
| [**PRIORIDAD DE RECURSOS \_ DE LA OFERTA DE \_ \_ DXGI**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | Identifica la importancia del contenido de un recurso cuando se llama al método [**IDXGIDevice2::OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) para ofrecer el recurso. <br/> |
| [**TIPO DE FORMA DE PUNTERO \_ OUTDUPL \_ \_ DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | Identifica el tipo de forma de puntero.<br/>                                                                                                                                  |
| [**MARCA DE COMPATIBILIDAD CON \_ EL ESPACIO DE COLORES DE \_ \_ \_ SUPERPOSICIÓN DXGI \_**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | Especifica la compatibilidad con el espacio de colores de superposición.<br/>                                                                                                                             |
| [**MARCA DE COMPATIBILIDAD DE \_ \_ SUPERPOSICIÓN \_ DXGI**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | Especifica la compatibilidad de superposición que se debe comprobar en una llamada a [**IDXGIOutput3::CheckOverlaySupport**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport).<br/>                                     |
| [**RESULTADOS DE RECURSOS \_ DE \_ RECLAMACIÓN DE DXGI \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | Especifica marcas de resultado para el [**método ReclaimResources1.**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1)<br/>                                                                     |
| [**RESIDENCIA DE DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | Marcas que indican la ubicación de memoria de un recurso.<br/>                                                                                                                    |
| [**ESCALADO \_ DE DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | Identifica el comportamiento de cambio de tamaño cuando el tamaño del búfer de reserva no coincide con el tamaño de la salida de destino.<br/>                                                                     |
| [**MARCA DE COMPATIBILIDAD \_ CON EL ESPACIO DE COLORES DE LA CADENA DE INTERCAMBIO \_ \_ \_ \_ \_ DXGI**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | Especifica la compatibilidad del espacio de color para la cadena de intercambio.<br/>                                                                                                                      |
| [**MARCA DE CADENA \_ DE \_ INTERCAMBIO DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | Opciones para el comportamiento de la cadena de intercambio.<br/>                                                                                                                                       |
| [**EFECTO DE \_ INTERCAMBIO \_ DXGI**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | Opciones para controlar píxeles en una superficie de presentación después de llamar a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). <br/>                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 


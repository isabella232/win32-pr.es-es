---
title: Estructuras de XAudio2
description: Esta sección contiene información sobre las estructuras que proporciona la API de Microsoft XAudio2.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b67e0312c5ac6b753881d895dff3972564f2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817659"
---
# <a name="xaudio2-structures"></a>Estructuras de XAudio2

Esta sección contiene información sobre las estructuras que proporciona la API de Microsoft XAudio2.



| Estructura                                                                                 | Descripción                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Búfer de XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Representa un búfer de datos de audio.<br/>                                                                                                    |
| [**Búfer de XAUDIO2 \_ \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Representa un búfer de datos de audio WMA.<br/>                                                                                                 |
| [**\_Configuración de depuración de XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Establece una nueva configuración de depuración global para XAudio2 cuando la usa la función SetDebugConfiguration.                                             |
| [**\_Cadena de efectos de XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Define una cadena de efectos.<br/>                                                                                                            |
| [**Descriptor de efectos de XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Define un efecto.<br/>                                                                                                                  |
| [**\_Parámetros de filtro de XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Define los parámetros de filtro para una voz de origen.<br/>                                                                                       |
| [**\_Datos de rendimiento de XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Recupera información de rendimiento.<br/>                                                                                                  |
| [**Descriptor de envío de XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Describe un destino de envío de voz.<br/>                                                                                                 |
| [**Detalles de la voz de XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Contiene información sobre las marcas de creación, los canales de entrada y la velocidad de muestra de una voz.<br/>                                          |
| [**\_Envío de voz de XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Define un conjunto de voces para recibir datos de una sola voz de salida.<br/>                                                                 |
| [**Estado de la voz de XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Devuelve el estado actual de la voz y los datos de la posición del cursor.<br/>                                                                         |
| [**\_Parámetros de I3DL2 de reverberación XAUDIO2FX \_ \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Describe los parámetros I3DL2 (2,0 nivel de directrices de representación de audio 3D interactivo) para su uso en la función ReverbConvertI3DL2ToNative.           |
| [**\_Parámetros de reverberación XAUDIO2FX \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Describe los parámetros que se usan en el APO de reverberación.                                                                                                |
| [**\_Niveles de VOLUMEMETER de XAUDIO2FX \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Describe los parámetros para usar con el APO de medidor de volumen.                                                                                        |
| [**\_parámetros de \_ búfer \_ LOCKFORPROCESS XAPO**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Define los parámetros de búfer que permanecen constantes mientras un XAPO está bloqueado.<br/>                                                             |
| [**\_parámetros de \_ búfer de proceso de XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Define los parámetros de búfer que pueden cambiar de una llamada a la siguiente.<br/>                                                                |
| [**\_propiedades de registro de XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Describe las características generales de un XAPO.<br/>                                                                                       |
| [**FXECHO \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Parámetros de inicialización para su uso con el XAPO FXECHO.<br/>                                                                             |
| [**parámetros de FXECHO \_**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Parámetros para usar con el XAPO FXECHO.<br/>                                                                                            |
| [**parámetros de FXEQ \_**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Parámetros para usar con el XAPO FXEQ.<br/>                                                                                              |
| [**parámetros de FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Parámetros para usar con el XAPO FXMasteringLimiter.<br/>                                                                                |
| [**parámetros de FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Parámetros para usar con el XAPO FXReverb.<br/>                                                                                          |
| [**\_Cono X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Especifica la direccionalidad para un emisor no LFE de canal único mediante el escalado del comportamiento de DSP con respecto a la orientación del emisor.<br/>    |
| [**\_Curva de distancia X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Define una curva a trozos explícita formada por segmentos lineales, lo que define directamente el comportamiento del DSP con respecto a la distancia normalizada.<br/> |
| [**\_Punto de \_ curva de distancia X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Define una configuración de DSP en una distancia normalizada determinada.<br/>                                                                               |
| [**\_Configuración de DSP de X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Recibe los resultados de una llamada a X3DAudioCalculate.<br/>                                                                              |
| [**\_Emisor X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Define un origen de audio 3D único o de punto múltiple que se usa con un número arbitrario de canales de sonido.<br/>                                    |
| [**Agente de escucha de X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Define un punto de recepción de audio 3D.<br/>                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

 





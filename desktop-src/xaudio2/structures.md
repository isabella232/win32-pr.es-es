---
title: Estructuras XAudio2
description: Esta sección contiene información sobre las estructuras proporcionadas por la API de Microsoft XAudio2.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59dcbdf454f282ca696a040aa7c1a3fe84c372ca4e0607c0a60f18b59d5f5e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962594"
---
# <a name="xaudio2-structures"></a>Estructuras XAudio2

Esta sección contiene información sobre las estructuras proporcionadas por la API de Microsoft XAudio2.



| Estructura                                                                                 | Descripción                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BÚFER \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Representa un búfer de datos de audio.<br/>                                                                                                    |
| [**XAUDIO2 \_ BUFFER \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Representa un búfer de datos de audio WMA.<br/>                                                                                                 |
| [**CONFIGURACIÓN DE \_ DEPURACIÓN DE XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Establece una nueva configuración de depuración global para XAudio2 cuando la usa la función SetDebugConfiguration.                                             |
| [**CADENA DE EFECTOS \_ XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Define una cadena de efectos.<br/>                                                                                                            |
| [**DESCRIPTOR DE EFECTO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Define un efecto.<br/>                                                                                                                  |
| [**PARÁMETROS DE FILTRO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Define parámetros de filtro para una voz de origen.<br/>                                                                                       |
| [**DATOS DE RENDIMIENTO DE XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Recupera información de rendimiento.<br/>                                                                                                  |
| [**DESCRIPTOR DE ENVÍO DE XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Describe un destino de envío de voz.<br/>                                                                                                 |
| [**DETALLES DE VOZ DE XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Contiene información sobre las marcas de creación, los canales de entrada y la frecuencia de muestreo de una voz.<br/>                                          |
| [**ENVÍOS DE VOZ DE XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Define un conjunto de voces para recibir datos de una sola voz de salida.<br/>                                                                 |
| [**ESTADO DE VOZ \_ XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Devuelve el estado actual de la voz y los datos de posición del cursor.<br/>                                                                         |
| [**PARÁMETROS DE XAUDIO2FX \_ REVERB \_ I3DL2 \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Describe los parámetros I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) para su uso en la función ReverbConvertI3DL2ToNative.           |
| [**PARÁMETROS DE \_ XAUDIO2FX REVERB \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Describe los parámetros para su uso en el APÓver de reverberación.                                                                                                |
| [**NIVELES DE \_ VOLUMEMETER DE XAUDIO2FX \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Describe los parámetros para su uso con el medidor de volumen APO.                                                                                        |
| [**PARÁMETROS DE \_ BÚFER LOCKFORPROCESS \_ DE XAPO \_**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Define parámetros de búfer que permanecen constantes mientras un XAPO está bloqueado.<br/>                                                             |
| [**PARÁMETROS DE BÚFER \_ DE PROCESO \_ XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Define los parámetros de búfer que pueden cambiar de una llamada a la siguiente.<br/>                                                                |
| [**PROPIEDADES DE REGISTRO \_ DE XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Describe las características generales de un XAPO.<br/>                                                                                       |
| [**FXECHO \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Parámetros de inicialización para su uso con FXECHO XAPO.<br/>                                                                             |
| [**PARÁMETROS \_ FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Parámetros para su uso con FXECHO XAPO.<br/>                                                                                            |
| [**PARÁMETROS DE \_ FXEQ**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Parámetros para su uso con FXEQ XAPO.<br/>                                                                                              |
| [**PARÁMETROS DE \_ FXMASTERINGLIMITER**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Parámetros para su uso con FXMasteringLimiter XAPO.<br/>                                                                                |
| [**PARÁMETROS FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Parámetros para su uso con FXReverb XAPO.<br/>                                                                                          |
| [**X3DAUDIO \_ CONE**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Especifica la direccionalidad de un emisor que no es LFE de un solo canal mediante el escalado del comportamiento de DSP con respecto a la orientación del emisor.<br/>    |
| [**CURVA DE DISTANCIA DE X3DAUDIO \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Define una curva por partes explícita que se forma con segmentos lineales, definiendo directamente el comportamiento de DSP con respecto a la distancia normalizada.<br/> |
| [**PUNTO DE CURVA DE DISTANCIA \_ X3DAUDIO \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Define una configuración de DSP a una distancia normalizada determinada.<br/>                                                                               |
| [**CONFIGURACIÓN DE DSP DE X3DAUDIO \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Recibe los resultados de una llamada a X3DAudioCalculate.<br/>                                                                              |
| [**EMISOR X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Define un origen de audio 3D de uno o varios puntos que se usa con un número arbitrario de canales de sonido.<br/>                                    |
| [**AGENTE DE ESCUCHA X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Define un punto de recepción de audio 3D.<br/>                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

 





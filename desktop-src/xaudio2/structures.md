---
title: Estructuras XAudio2
description: Esta sección contiene información sobre las estructuras proporcionadas por la API XAudio2 de Microsoft.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b67e0312c5ac6b753881d895dff3972564f2c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246987"
---
# <a name="xaudio2-structures"></a>Estructuras XAudio2

Esta sección contiene información sobre las estructuras proporcionadas por la API XAudio2 de Microsoft.



| Estructura                                                                                 | Descripción                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BÚFER \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Representa un búfer de datos de audio.<br/>                                                                                                    |
| [**XAUDIO2 \_ BUFFER \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Representa un búfer de datos de audio WMA.<br/>                                                                                                 |
| [**CONFIGURACIÓN DE \_ DEPURACIÓN DE XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Establece una nueva configuración de depuración global para XAudio2 cuando la usa la función SetDebugConfiguration.                                             |
| [**CADENA DE \_ EFECTOS XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Define una cadena de efectos.<br/>                                                                                                            |
| [**DESCRIPTOR DE \_ EFECTO XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Define un efecto.<br/>                                                                                                                  |
| [**PARÁMETROS DE FILTRO \_ XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Define los parámetros de filtro para una voz de origen.<br/>                                                                                       |
| [**DATOS DE RENDIMIENTO DE XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Recupera información de rendimiento.<br/>                                                                                                  |
| [**DESCRIPTOR DE ENVÍO DE XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Describe un destino de envío de voz.<br/>                                                                                                 |
| [**DETALLES DE VOZ DE XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Contiene información sobre las marcas de creación, los canales de entrada y la frecuencia de muestreo de una voz.<br/>                                          |
| [**ENVÍOS DE VOZ DE XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Define un conjunto de voces para recibir datos de una sola voz de salida.<br/>                                                                 |
| [**ESTADO DE VOZ \_ XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Devuelve el estado actual de la voz y los datos de posición del cursor.<br/>                                                                         |
| [**PARÁMETROS DE XAUDIO2FX \_ REVERB \_ I3DL2 \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Describe los parámetros I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) para su uso en la función ReverbConvertI3DL2ToNative.           |
| [**PARÁMETROS DE \_ XAUDIO2FX REVERB \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Describe los parámetros para su uso en el APPO de reverberación.                                                                                                |
| [**NIVELES DE \_ VOLUMEMETER DE XAUDIO2FX \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Describe los parámetros para su uso con el medidor de volúmenes APO.                                                                                        |
| [**PARÁMETROS DE BÚFER \_ LOCKFORPROCESS \_ DE XAPO \_**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Define parámetros de búfer que permanecen constantes mientras se bloquea un XAPO.<br/>                                                             |
| [**PARÁMETROS DE BÚFER \_ DE PROCESO \_ \_ XAPO**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Define los parámetros de búfer que pueden cambiar de una llamada a la siguiente.<br/>                                                                |
| [**PROPIEDADES DE REGISTRO \_ DE XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Describe las características generales de un XAPO.<br/>                                                                                       |
| [**FXECHO \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Parámetros de inicialización para su uso con FXECHO XAPO.<br/>                                                                             |
| [**PARÁMETROS \_ FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Parámetros para su uso con FXECHO XAPO.<br/>                                                                                            |
| [**PARÁMETROS \_ FXEQ**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Parámetros para su uso con FXEQ XAPO.<br/>                                                                                              |
| [**PARÁMETROS DE FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Parámetros para su uso con el XAPO FXMasteringLimiter.<br/>                                                                                |
| [**PARÁMETROS FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Parámetros para su uso con el XAPO FXReverb.<br/>                                                                                          |
| [**CONO X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Especifica direccionalidad para un emisor de un solo canal que no es LFE mediante el escalado del comportamiento de DSP con respecto a la orientación del emisor.<br/>    |
| [**CURVA DE DISTANCIA DE X3DAUDIO \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Define una curva por partes explícita que se forma en segmentos lineales, definiendo directamente el comportamiento de DSP con respecto a la distancia normalizada.<br/> |
| [**PUNTO DE CURVA DE \_ DISTANCIA X3DAUDIO \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Define una configuración de DSP a una distancia normalizada determinada.<br/>                                                                               |
| [**CONFIGURACIÓN DE \_ DSP X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Recibe los resultados de una llamada a X3DAudioCalculate.<br/>                                                                              |
| [**EMISOR X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Define un origen de audio 3D de uno o varios puntos que se usa con un número arbitrario de canales de sonido.<br/>                                    |
| [**AGENTE DE ESCUCHA X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Define un punto de recepción de audio 3D.<br/>                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

 





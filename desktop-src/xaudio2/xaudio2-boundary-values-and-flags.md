---
description: Constantes XAudio2 que especifican parámetros predeterminados, valores máximos y marcas.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: Valores y marcas de límite de XAudio2 (Xaudio2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11293b55a44b0aefdeacf95b9e36e90a626de2c1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470711"
---
# <a name="xaudio2-boundary-values-and-flags"></a>Valores y marcas de límite de XAudio2

Constantes XAudio2 que especifican parámetros predeterminados, valores máximos y marcas.

**Valores de límite de XAudio2**



| Constante                                                                                                                                                                                                     | Descripción                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**BYTES DE BÚFER MÁXIMO DE XAUDIO2 \_ \_ \_**</dt> </dl>             | Valor máximo permitido para [**el búfer de XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) AudioBytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**BÚFERES \_ EN COLA \_ MÁXIMOS DE XAUDIO2 \_**</dt> </dl>       | Búferes máximos permitidos en una cola de voz.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**SISTEMA DE \_ BÚFERES \_ MÁXIMOS XAUDIO2 \_**</dt> </dl>       | Búferes máximos permitidos para subprocesos del sistema (Xbox 360 solo).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**XAUDIO2 \_ MAX \_ AUDIO \_ CHANNELS**</dt> </dl>       | Valor máximo permitido para **ESTANDOATEX.nChannels.**<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**FRECUENCIA DE MUESTREO MÍNIMA DE XAUDIO2 \_ \_ \_**</dt> </dl>                | Velocidad de muestreo de audio mínima admitida.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**FRECUENCIA DE MUESTREO MÁXIMA DE XAUDIO2 \_ \_ \_**</dt> </dl>                | Velocidad máxima de muestreo de audio admitida.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**NIVEL DE VOLUMEN MÁXIMO DE XAUDIO2 \_ \_ \_**</dt> </dl>             | Nivel de volumen máximo permitido.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**PROPORCIÓN DE \_ \_ FRECUENCIA DE FRECUENCIA DE XAUDIO2 \_ MIN**</dt> </dl>                   | Frecuencia mínima permitida en una voz de origen.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**PROPORCIÓN DE \_ \_ FRECUENCIA DE FRECUENCIA MÁXIMA DE XAUDIO2 \_**</dt> </dl>                   | Frecuencia máxima permitida en una voz de origen.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**PROPORCIÓN DE \_ \_ FRECUENCIA DE FRECUENCIA PREDETERMINADA DE XAUDIO2 \_**</dt> </dl>       | Valor predeterminado para **el argumento MaxFrequencyRatio** [**de IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**FILTRO MÁXIMO DE XAUDIO2 \_ \_ \_ ONEOVERQ**</dt> </dl>    | Valor máximo de [**XAUDIO2 \_ FILTER \_ PARAMETERS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**OneOverQ**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**FRECUENCIA MÁXIMA DE FILTRO DE XAUDIO2 \_ \_ \_**</dt> </dl> | Valor máximo de [**XAUDIO2 \_ FILTER \_ PARAMETERS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Frecuencia**.<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**NÚMERO MÁXIMO \_ DE \_ BUCLES XAUDIO2 \_**</dt> </dl>                   | Valor máximo que no se tratará como bucle infinito para [**el búfer de XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**INSTANCIAS \_ MÁXIMAS DE XAUDIO2 \_**</dt> </dl>                       | Número máximo de instancias simultáneas de XAudio2 permitidas en Xbox 360.<br/>                                                                       |



**Valores XAudio2 con significado especial**



| Constante                                                                                                                                                                                              | Descripción                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**CONFIRMACIÓN DE XAUDIO2 \_ \_ AHORA**</dt> </dl>                         | Se usa como parámetro para los métodos con un argumento OperationSet. Consulte [Conjuntos de operaciones XAudio2](xaudio2-operation-sets.md) para obtener más información.<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**CONFIRMACIÓN DE XAUDIO2 \_ \_ ALL**</dt> </dl>                         | Se usa como parámetro [**en IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges).<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**OPSET no válido de XAUDIO2 \_ \_**</dt> </dl>                | Especifica un valor no válido para los argumentos OperationSet. Consulte [Conjuntos de operaciones XAudio2](xaudio2-operation-sets.md) para obtener más información.<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**REGIÓN DE BUCLE NO DE XAUDIO2 \_ \_ \_**</dt> </dl>            | Especifica ninguna región de bucle, que se usa en [**el búfer de XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**BUCLE XAUDIO2 \_ \_ INFINITO**</dt> </dl>                | Especifica un bucle infinito, que se usa en [**el búfer de XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**CANALES PREDETERMINADOS DE XAUDIO2 \_ \_**</dt> </dl>       | Especifica el número predeterminado de canales para la plataforma actual, que se usa [**en IXAudio2::CreateMasteringVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**SAMPLERATE PREDETERMINADA DE XAUDIO2 \_ \_**</dt> </dl> | Especifica la frecuencia de muestreo predeterminada para la plataforma actual, que se usa [**en IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/>        |



**Marcas XAudio2**




| Constante | Descripción | 
|----------|-------------|
| <span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl><dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt></dl> | Especifica que se debe usar la versión depurada o comprobada del motor de audio en lugar de la versión de lanzamiento. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br /><blockquote>[!Note]<br />Esta marca no se admite en Windows 8 o Windows 10.</blockquote><br /> | 
| <span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl><dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt></dl> | Especifica que una voz de origen no usará el desplazamiento de tono, vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a>.<br /> | 
| <span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl><dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt></dl> | Especifica que no hay ninguna conversión de frecuencia de muestreo disponible en una voz de origen, las salidas de la voz deben tener la misma frecuencia de muestreo. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a>.<br /> | 
| <span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl><dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt></dl> | Especifica que el efecto de filtro debe estar disponible en una voz. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a> e <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2::CreateSubmixVoice</strong></a>.<br /> | 
| <span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl><dt><strong>XAUDIO2_PLAY_TAILS</strong></dt></dl> | Especifica que una voz debe seguir emitiendo la salida del efecto una vez detenida. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice::Stop</strong></a>.<br /> | 
| <span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl><dt><strong>XAUDIO2_END_OF_STREAM</strong></dt></dl> | Indica el último búfer de una secuencia. Vea <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Marca</strong>.<br /> | 
| <span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl><dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt></dl> | Especifica que el motor de audio debe detenerse cuando no se inicia ninguna voz de origen e iniciarse cuando se inicia una voz. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br /> | 
| <span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl><dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt></dl> | Indica que se debe usar un filtro en un envío de voz. Vea <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Marca</strong>.<br /> | 
| <span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl><dt><strong>XAUDIO2_1024_QUANTUM</strong></dt></dl> | Especifica un cuántico de procesamiento no predeterminado de 21,33 ms (1024 muestras a 48 KHz). Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br /> | 
| <span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl><dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt></dl> | Especifica que no se debe usar un cliente de audio virtual. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2::CreateMasteringVoice</strong></a>.<br /><blockquote>[!Note]<br />En los dispositivos de la familia de dispositivos móviles, siempre se usa un cliente de audio virtual, independientemente de si se usa esta marca.</blockquote><br /> | 




**Parámetros predeterminados de XAudio2 para el filtro de voz integrado**



| Constante                                                                                                                                                                                                                 | Descripción                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**TIPO DE FILTRO PREDETERMINADO DE XAUDIO2 \_ \_ \_**</dt> </dl>                | Especifica el tipo de filtro predeterminado que se usará con las voces y los envíos de voz.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**FRECUENCIA DE FILTRO PREDETERMINADA DE XAUDIO2 \_ \_ \_**</dt> </dl> | Especifica la frecuencia de filtro predeterminada que se usará con las voces y los envíos de voz.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**FILTRO PREDETERMINADO DE XAUDIO2 \_ \_ \_ ONEOVERQ**</dt> </dl>    | Especifica la tasa de decadencia de filtro predeterminada que se usará con las voces y los envíos de voz.<br/> |



## <a name="remarks"></a>Comentarios

### <a name="platform-requirements"></a>Requisitos de la plataforma

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); SDK de DirectX (XAudio 2.7)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Xaudio2.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[XAudio2::Constants](constants.md)
</dt> </dl>

 

 

---
description: Constantes de XAudio2 que especifican los parámetros predeterminados, los valores máximos y las marcas.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: Marcas y valores de límite de XAudio2 (xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59f229ea406eb5bf6c6b3f5c124d6d0d19c047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718951"
---
# <a name="xaudio2-boundary-values-and-flags"></a>Marcas y valores de límite de XAudio2

Constantes de XAudio2 que especifican los parámetros predeterminados, los valores máximos y las marcas.

**Valores de límite de XAudio2**



| Constante                                                                                                                                                                                                     | Descripción                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**\_Bytes máximos del \_ búfer de XAUDIO2 \_**</dt> </dl>             | Valor máximo permitido para [**el \_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer). AudioBytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**\_ \_ Búferes máximos en cola de XAUDIO2 \_**</dt> </dl>       | Máximo de búferes permitidos en una cola de voz.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**\_Sistema de \_ búferes \_ máximo de XAUDIO2**</dt> </dl>       | Máximo de búferes permitidos para los subprocesos del sistema (solo Xbox 360).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**\_Canales de \_ audio \_ Max de XAUDIO2**</dt> </dl>       | Valor máximo permitido para **WAVEFORMATEX. nChannels**.<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**\_Velocidad de \_ muestra \_ mínima de XAUDIO2**</dt> </dl>                | Velocidad de muestra de audio mínima admitida.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**\_Velocidad de \_ muestra \_ máxima de XAUDIO2**</dt> </dl>                | Velocidad de muestra de audio máxima admitida.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**\_Nivel máximo de \_ volumen \_ de XAUDIO2**</dt> </dl>             | Nivel máximo de volumen permitido.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**Relación de la \_ frecuencia mínima de XAUDIO2 \_ \_**</dt> </dl>                   | Relación de frecuencia mínima permitida en una voz de origen.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**Relación de la \_ frecuencia máxima de XAUDIO2 \_ \_**</dt> </dl>                   | Relación de frecuencia máxima permitida en una voz de origen.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**\_ \_ Relación frec predeterminada de XAUDIO2 \_**</dt> </dl>       | Valor predeterminado para el argumento **MaxFrequencyRatio** de [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**\_Filtro Max de XAUDIO2 \_ \_ ONEOVERQ**</dt> </dl>    | Valor máximo para [**\_ \_ los parámetros de filtro de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**OneOverQ**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**\_Frecuencia de \_ filtro \_ máxima de XAUDIO2**</dt> </dl> | Valor máximo para [**\_ \_ los parámetros de filtro de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Frecuencia**.<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**\_Recuento máximo de \_ bucles de XAUDIO2 \_**</dt> </dl>                   | Valor máximo que no se tratará como bucle infinito para el [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**\_Instancias máximas de XAUDIO2 \_**</dt> </dl>                       | Número máximo de instancias simultáneas de XAudio2 permitidas en Xbox 360.<br/>                                                                       |



**Valores de XAudio2 con significado especial**



| Constante                                                                                                                                                                                              | Descripción                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**\_Confirmar XAUDIO2 \_ ahora**</dt> </dl>                         | Se usa como parámetro para los métodos con un argumento OperationSet. Consulte [conjuntos de operaciones de XAudio2](xaudio2-operation-sets.md) para obtener más información.<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**\_Confirmar \_ todo en XAUDIO2**</dt> </dl>                         | Se utiliza como parámetro en [**IXAudio2:: commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges).<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**\_OPSET no válido de XAUDIO2 \_**</dt> </dl>                | Especifica un valor no válido para los argumentos de OperationSet. Consulte [conjuntos de operaciones de XAudio2](xaudio2-operation-sets.md) para obtener más información.<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**\_Región de \_ bucle \_ no de XAUDIO2**</dt> </dl>            | No especifica ninguna región de bucle, usada en el [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**Bucle de XAUDIO2 \_ \_ infinito**</dt> </dl>                | Especifica bucles infinitos, que se usa en el [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**\_Canales predeterminados de XAUDIO2 \_**</dt> </dl>       | Especifica el número predeterminado de canales para la plataforma actual, usados en [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**\_SampleRate predeterminado de XAUDIO2 \_**</dt> </dl> | Especifica la velocidad de muestreo predeterminada para la plataforma actual, usada en [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/>        |



**Marcas de XAudio2**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl> <dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que debe usarse la versión de depuración/comprobada del motor de audio en lugar de la versión de lanzamiento. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/>
<blockquote>
[!Note]<br />
Esta marca no se admite en Windows 8 ni Windows 10.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl> <dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que una voz de origen no usará el desplazamiento de tono, vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: CreateSourceVoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl> <dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que no hay ninguna conversión de velocidad de muestra disponible en una voz de origen, las salidas de la voz deben tener la misma velocidad de muestra. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: CreateSourceVoice</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl> <dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que el efecto de filtro debe estar disponible en una voz. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: CreateSourceVoice</strong></a> y <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2:: CreateSubmixVoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl> <dt><strong>XAUDIO2_PLAY_TAILS</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que una voz debe continuar emitiendo la salida de efecto después de detenerse. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice:: Stop</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl> <dt><strong>XAUDIO2_END_OF_STREAM</strong></dt> </dl></td>
<td style="text-align: left;">Indica el último búfer de una secuencia. Vea <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Marcas</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl> <dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que el motor de audio debe detenerse cuando no se inicia ninguna voz de origen y se inicia cuando se inicia una voz. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl> <dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Indica que se debe usar un filtro en un envío de voz. Vea <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Marcas</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl> <dt><strong>XAUDIO2_1024_QUANTUM</strong></dt> </dl></td>
<td style="text-align: left;">Especifica un cuanto de procesamiento no predeterminado de 21,33 MS (1024 ejemplos a 48 kHz). Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl> <dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que no se debe usar un cliente de audio virtual. Vea <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2:: CreateMasteringVoice</strong></a>.<br/>
<blockquote>
[!Note]<br />
En los dispositivos de la familia de dispositivos móviles, siempre se usa un cliente de audio virtual, independientemente de si se usa esta marca.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



**Parámetros predeterminados de XAudio2 para el filtro de voz integrado**



| Constante                                                                                                                                                                                                                 | Descripción                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**\_Tipo de \_ filtro \_ predeterminado de XAUDIO2**</dt> </dl>                | Especifica el tipo de filtro predeterminado que se va a utilizar con las voces y los envíos de voz.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**\_Frecuencia de \_ filtro \_ predeterminado de XAUDIO2**</dt> </dl> | Especifica la frecuencia de filtro predeterminada que se va a utilizar con las voces y los envíos de voz.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**\_Filtro predeterminado de XAUDIO2 \_ \_ ONEOVERQ**</dt> </dl>    | Especifica la tasa de filtro predeterminada de la caída que se va a utilizar con las voces y los envíos de voz.<br/> |



## <a name="remarks"></a>Observaciones

### <a name="platform-requirements"></a>Requisitos de la plataforma

Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); SDK de DirectX (XAudio 2,7)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[XAudio2:: constantes](constants.md)
</dt> </dl>

 

 

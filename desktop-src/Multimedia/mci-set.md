---
title: MCI_SET comando (Mmsystem.h)
description: El comando MCI \_ SET establece la información del dispositivo. Los dispositivos cd audio, digital-video, secuenciador MIDI, VCR, videodisc, superposición de vídeo y audio de onda reconocen este comando.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- MCI_SET comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369932"
---
# <a name="mci_set-command"></a>Comando MCI \_ SET

> [!NOTE]
> La comunicación sin sesgos de Microsoft admite un entorno diverso e inclusario.  Dentro de este documento, hay referencias a la palabra "subordinada". La Guía de estilo de Microsoft [Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra excluyente.  Esta redacción se usa, ya que actualmente es la que se usa en los comandos. Por coherencia, este documento contiene esta palabra. Cuando esta palabra se modifica en los comandos, corregiremos este documento para que esté alineado.

El comando MCI \_ SET establece la información del dispositivo. Los dispositivos cd audio, digital-video, secuenciador MIDI, VCR, videodisc, superposición de vídeo y audio de onda reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, para dispositivos de vídeo digital y VCR, MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*
</dt> <dd>

Puntero a una [**estructura MCI \_ SET \_ PARMS.**](mci-set-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ SET:

<dl> <dt>

<span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ SET \_ AUDIO
</dt> <dd>

Se incluye un número de canal de audio en el miembro dwAudio de la estructura identificada *por lpSet*. Esta marca debe usarse con MCI \_ SET \_ ON o MCI SET \_ \_ OFF. Use una de las constantes siguientes para indicar el número de canal:

</dd> <dt>

<span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ SET \_ AUDIO \_ ALL
</dt> <dd>

Todos los canales de audio.

</dd> <dt>

<span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI \_ SET \_ AUDIO \_ LEFT
</dt> <dd>

Canal izquierdo.

</dd> <dt>

<span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ SET \_ AUDIO \_ RIGHT
</dt> <dd>

Canal derecho.

</dd> <dt>

<span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI \_ SET \_ DOOR \_ CLOSED
</dt> <dd>

Cierra la cobertura multimedia (si la hay).

</dd> <dt>

<span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI \_ SET \_ DOOR \_ OPEN
</dt> <dd>

Abre la cobertura multimedia (si la hay).

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Deshabilita el canal de audio o vídeo especificado.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Habilita el canal de audio o vídeo especificado.

</dd> <dt>

<span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>FORMATO DE HORA DE MCI \_ SET \_ \_
</dt> <dd>

Se incluye un parámetro de formato de hora en el **miembro dwTimeFormat** de la estructura identificada por *lpSet*. Las marcas siguientes se usan con esta marca:

</dd> <dt>

<span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>BYTES DE FORMATO MCI \_ \_
</dt> <dd>

Dentro de un formato de datos PCM (pulse Code Estampada), cambia la descripción del miembro de hora a bytes para la entrada o salida. Reconocido por el tipo **de dispositivo waveaudio.**

</dd> <dt>

<span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MARCOS DE FORMATO MCI \_ \_
</dt> <dd>

Los comandos posteriores usarán fotogramas. Lo reconocen los tipos **de dispositivo digitalvideo,** **vcr** y **videodisc.**

</dd> <dt>

<span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI \_ FORMAT \_ HMS
</dt> <dd>

Cambia el formato de hora a horas, minutos y segundos. Reconocido por los tipos **de dispositivo vcr** y **videodisc.**

</dd> <dt>

<span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MILISEGUNDOS DE FORMATO MCI \_ \_
</dt> <dd>

Cambia el formato de hora a milisegundos. Reconocido por todos los tipos de dispositivos.

</dd> <dt>

<span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI \_ FORMAT \_ MSF
</dt> <dd>

Cambia el formato de hora a minutos, segundos y fotogramas. Reconocido por los tipos **de dispositivo cdaudio** **y vcr.**

</dd> <dt>

<span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>EJEMPLOS DE FORMATO \_ MCI \_
</dt> <dd>

Cambia el formato de hora a ejemplos de entrada o salida. Reconocido por el tipo **de dispositivo waveaudio.**

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI \_ FORMAT \_ SMPTE \_ 24, MCI \_ FORMAT \_ SMPTE \_ 25 y MCI \_ FORMAT \_ SMPTE \_ 30
</dt> <dd>

Establece el formato de hora en 24, 25 y 30 fotogramas SMPTE (Society of Motion Picture and Tv Engineers), respectivamente. Reconocido por los tipos **de dispositivo sequencer** **y vcr.**

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI \_ FORMAT \_ SMPTE \_ 30DROP
</dt> <dd>

Establece el formato de hora en 30 SMPTE de fotogramas desplegables. Reconocido por los tipos **de dispositivo sequencer** **y vcr.**

</dd> <dt>

<span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_TMSF CON \_ FORMATO MCI
</dt> <dd>

Cambia el formato de hora a pistas, minutos, segundos y fotogramas. (MCI usa números de seguimiento continuos). Reconocido por los tipos **de dispositivo cdaudio** **y vcr.**

</dd> <dt>

<span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>VÍDEO DE MCI \_ SET \_
</dt> <dd>

Establece la señal de vídeo en on o off. Esta marca debe usarse con MCI \_ SET \_ ON o MCI SET \_ \_ OFF. Los dispositivos que no tienen vídeo devuelven LA \_ FUNCIÓN MCIERR UNSUPPORTED. \_

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ SET \_ FILEFORMAT
</dt> <dd>

Se incluye un parámetro de formato de archivo en el **miembro dwFileFormat** de la estructura identificada *por lpSet*. En el caso de los dispositivos de vídeo digital, el formato de archivo se usa para los comandos de guardado o captura. Si se omite, esto podría tener como valor predeterminado un formato definido por el controlador de dispositivo. Si el formato de archivo especificado entra en conflicto con el algoritmo y la calidad seleccionados actualmente, se cambian a los valores predeterminados para el formato de archivo. Se definen las siguientes constantes de formato de archivo:

</dd> <dt>

<span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI
</dt> <dd>

Formato AVI.

</dd> <dt>

<span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ AVSS
</dt> <dd>

Formato avss.

</dd> <dt>

<span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB
</dt> <dd>

Formato DIB.

</dd> <dt>

<span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF
</dt> <dd>

Formato JFIF.

</dd> <dt>

<span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG
</dt> <dd>

Formato JPEG.

</dd> <dt>

<span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG
</dt> <dd>

Formato MPEG.

</dd> <dt>

<span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB
</dt> <dd>

Formato DIB de RLE.

</dd> <dt>

<span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG
</dt> <dd>

Formato RJPEG.

</dd> <dt>

<span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI \_ DGV \_ SET \_ SEEK \_ EXACTLY
</dt> <dd>

Establece el formato utilizado para el posicionamiento. Esta marca debe usarse con MCI \_ SET \_ ON o MCI SET \_ \_ OFF. Si se especifica MCI SET ON, reproducir o grabar accede con precisión al marco especificado con la \_ \_ marca MCI \_ FROM. Esto podría agregar algún retraso adicional si el marco solicitado no es un fotograma clave. Si se especifica MCI SET OFF, el dispositivo buscará una imagen de fotograma clave \_ que precede al fotograma \_ solicitado. Para algunos archivos y dispositivos, podría ser el primer fotograma del archivo. El valor predeterminado de esta marca depende del dispositivo.

</dd> <dt>

<span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI \_ DGV \_ SET \_ SPEED
</dt> <dd>

Se incluye un parámetro de velocidad en el **miembro dwSpeed** de la estructura identificada por *lpSet*. La velocidad se especifica como una relación entre la velocidad de fotogramas nominal y la velocidad de fotogramas deseada, donde la velocidad nominal de fotogramas se designa como 1000. La media velocidad es 500 y la doble es 2000. El intervalo de velocidad permitido depende del dispositivo y, posiblemente, del archivo también.

</dd> <dt>

<span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI \_ DGV \_ SET \_ STILL
</dt> <dd>

Cuando se usa con MCI \_ DGV \_ SET \_ FILEFORMAT, MCI SET establece el formato de archivo \_ utilizado para los comandos de captura.

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

En el caso de los dispositivos de vídeo digital, el *parámetro lpSet* apunta a una estructura [**\_ MCI DGV \_ SET \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms)

Las siguientes marcas adicionales se usan con el **tipo de dispositivo sequencer:**

<dl> <dt>

<span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>FORMATO MCI \_ SEQ \_ \_ SONGPTR
</dt> <dd>

Establece el formato de hora en unidades de puntero de canción.

</dd> <dt>

<span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI \_ SEQ \_ SET \_ MASTER
</dt> <dd>

Establece el secuenciador como origen de datos de sincronización e indica que el tipo de sincronización se especifica en el **miembro dwMaster** de la estructura identificada por *lpSet*. MCISEQ devuelve MCIERR \_ UNSUPPORTED \_ FUNCTION. Las siguientes constantes se definen para el tipo de sincronización:

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ SEQ \_ MIDI
</dt> <dd>

El secuenciador enviará datos de sincronización de formato MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ SEQ \_ SMPTE
</dt> <dd>

El secuenciador enviará datos de sincronización de formato SMPTE.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ NONE
</dt> <dd>

El secuenciador no enviará datos de sincronización.

</dd> <dt>

<span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>DESPLAZAMIENTO DE CONJUNTO \_ DE MCI SEQ \_ \_
</dt> <dd>

Cambia el desplazamiento SMPTE de una secuencia a la especificada por el **miembro dwOffset** de la estructura identificada *por lpSet*. Esto solo afecta a las secuencias con un tipo de división SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>PUERTO DE CONJUNTO \_ DE MCI SEQ \_ \_
</dt> <dd>

Establece el puerto MIDI de salida de una secuencia en el especificado por el identificador de dispositivo MIDI en el **miembro dwPort** de la estructura identificada *por lpSet*. El dispositivo cierra el puerto anterior (si lo hay) e intenta abrir y usar el nuevo puerto. Si se produce un error, devuelve un error y vuelve a abrir el puerto usado anteriormente (si lo hubiera). Se definen las siguientes constantes para los puertos:

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ NONE
</dt> <dd>

Cierra el puerto usado anteriormente (si lo hubiera). El secuenciador se comporta exactamente igual que si un puerto estuviera abierto, salvo que no se envía ningún mensaje MIDI.

</dd> <dt>

<span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>ASIGNADOR DE MIDI \_
</dt> <dd>

Establece el puerto abierto al asignador de MIDI.

</dd> <dt>

<span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ SEQ \_ SET \_ SLAVE
</dt> <dd>

Establece el secuenciador para recibir los datos de sincronización e indica que el tipo de sincronización se especifica en el **miembro dw Escape de** la estructura identificada por *lpSet*. MCISEQ devuelve MCIERR \_ UNSUPPORTED \_ FUNCTION. Las siguientes constantes se definen para el tipo de sincronización:

</dd> <dt>

<span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>ARCHIVO MCI \_ \_ SEQ
</dt> <dd>

Establece el secuenciador para recibir los datos de sincronización contenidos en el archivo MIDI.

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ SEQ \_ MIDI
</dt> <dd>

Establece el secuenciador para recibir los datos de sincronización de MIDI.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ NONE
</dt> <dd>

Establece el secuenciador para pasar por alto los datos de sincronización en una secuencia de MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ SEQ \_ SMPTE
</dt> <dd>

Establece el secuenciador para recibir datos de sincronización de SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI \_ SEQ \_ SET \_ TEMPO
</dt> <dd>

Cambia el tempo de la secuencia MIDI al especificado por el **miembro dwTempo** de la estructura a la que *apunta lpSet*. Para las secuencias con el tipo de división PPQN, el tempo se especifica en latidos por minuto; para las secuencias con el tipo de división SMPTE, el tempo se especifica en fotogramas por segundo.

</dd> </dl>

En el caso de los dispositivos secuenciador, *el parámetro lpSet* apunta a una estructura [**MCI \_ SEQ SET \_ \_ PARMS.**](mci-seq-set-parms.md)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>REGISTRO DE \_ ENSAMBLADO DE CONJUNTO DE VCR \_ \_ DE \_ MCI
</dt> <dd>

Establece el dispositivo que se va a registrar en los modos de ensamblado o inserción (cuando el ensamblado está desactivado, la inserción está en funcionamiento y viceversa). Use con una de las marcas siguientes:

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Establece el registro de ensamblado en y desactiva el registro de inserción. Registra todas las pistas de vídeo, audio y código de tiempo.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Establece el registro de ensamblado desactivado y activa el registro de inserción. Cuando el registro de ensamblado está desactivado, se pueden seleccionar pistas individuales de vídeo, audio y código de tiempo para la grabación.

</dd> <dt>

<span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI \_ VCR \_ SET \_ CLOCK
</dt> <dd>

El **miembro dwClock** de la estructura identificada por *lpSet* contiene la nueva hora del reloj.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI \_ VCR \_ SET \_ COUNTER \_ FORMA
</dt> <dd>

El **miembro dwCounterFormat** de la estructura identificada por *lpSet* contiene una constante que especifica el nuevo formato de tiempo de contador que usará el contador de estado. Para obtener una lista de constantes válidas, vea MCI SET TIME FORMAT en la lista de marcas \_ \_ \_ adicionales para este comando.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>VALOR DEL CONTADOR \_ DE MCI VCR \_ \_ \_ SET
</dt> <dd>

El **miembro dwCounterValue** de la estructura identificada por *lpSet* contiene el nuevo valor del contador.

</dd> <dt>

<span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI \_ VCR \_ SET \_ INDEX
</dt> <dd>

El **miembro dwIndex** de la estructura identificada por *lpSet* contiene una constante que indica el contenido de la pantalla y debe ser uno de los siguientes:

</dd> <dt>

<span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>CONTADOR DE ÍNDICE \_ DE VCR \_ DE MCI \_
</dt> <dd>

Muestra el contador.

</dd> <dt>

<span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI \_ VCR \_ INDEX \_ DATE
</dt> <dd>

Muestra la fecha.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>TIEMPO DE ÍNDICE \_ DE VCR \_ DE MCI \_
</dt> <dd>

Muestra la hora.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>CÓDIGO DE \_ TIEMPO DEL ÍNDICE DE VCR \_ \_ DE MCI
</dt> <dd>

Muestra el código de tiempo.

Para obtener más información, vea el [comando MCI \_ INDEX.](mci-index.md)

</dd> <dt>

<span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>TIEMPO DE ESPERA \_ DE PAUSA DE MCI VCR \_ \_ \_ SET
</dt> <dd>

El **miembro dwPauseTimeout** de la estructura identificada por *lpSet* contiene la duración máxima, en milisegundos, de un comando de pausa.

</dd> <dt>

<span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>DURACIÓN DEL \_ POSTROLL DEL CONJUNTO DE VCR \_ \_ DE MCI \_
</dt> <dd>

El **miembro dwPostrollDuration** de la estructura identificada por *lpSet* contiene la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para interrumpir el transporte de VCR cuando se emite un comando de detenerse o pausar.

</dd> <dt>

<span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI \_ VCR \_ SET \_ POWER
</dt> <dd>

Establece el encendido o apagado. Debe usarse con una de las marcas siguientes:

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Desactiva la alimentación.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Activa la alimentación.

</dd> <dt>

<span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>DURACIÓN DE \_ LA INSCRIPCIÓN PREVIA DEL CONJUNTO DE VCR \_ \_ DE \_ MCI
</dt> <dd>

El **miembro dwPrerollDuration** de la estructura identificada por *lpSet* contiene la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para estabilizar la salida de VCR.

</dd> <dt>

<span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI \_ VCR \_ SET \_ RECORD \_ FORMAT
</dt> <dd>

El **miembro dwRecordFormat** de la estructura identificada por *lpSet* contiene una constante que describe la velocidad del registro, que debe ser una de las siguientes:

</dd> <dt>

<span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI \_ VCR \_ FORMAT \_ EP
</dt> <dd>

Registros a velocidad lenta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI \_ VCR \_ FORMAT \_ LP
</dt> <dd>

Registros a velocidad media-lenta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI \_ VCR \_ FORMAT \_ SP
</dt> <dd>

Registros a velocidad estándar.

</dd> <dt>

<span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI \_ VCR \_ SET \_ SPEED
</dt> <dd>

El **miembro dwSpeed** de la estructura identificada por *lpSet* contiene la nueva configuración de velocidad, donde 1000 es la velocidad normal, 2000 es de doble velocidad, 500 es de media velocidad, y así sucesivamente.

</dd> <dt>

<span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI \_ VCR \_ SET \_ TAPE \_ LENGTH
</dt> <dd>

El **miembro dwTapeLength** de la estructura identificada por *lpSet* contiene la nueva longitud de la cinta, siempre que la longitud de la cinta sea indetectable.

</dd> <dt>

<span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI \_ VCR \_ SET \_ TIME \_ MODE
</dt> <dd>

El **miembro dwTimeMode** de la estructura identificada por *lpSet* contiene una constante que indica el nuevo modo de tiempo posicional. Las siguientes constantes son válidas:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>CONTADOR DE TIEMPO \_ DE VCR \_ de MCI \_
</dt> <dd>

Obliga al dispositivo a usar el contador exclusivamente.

</dd> <dt>

<span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI \_ VCR \_ TIME \_ DETECT
</dt> <dd>

Cada vez que se inserta una nueva cinta de vídeo en el dispositivo o el modo cambia de no listo a listo, el dispositivo debe intentar determinar si hay código de tiempo disponible en la cinta de vídeo. Si el código de tiempo está disponible, use el código de tiempo en todos los comandos posteriores que especifiquen posiciones. De lo contrario, use el contador .

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>CÓDIGO DE \_ TIEMPO DE VCR \_ \_ de MCI
</dt> <dd>

Obliga al dispositivo a usar exclusivamente el código de tiempo.

</dd> <dt>

<span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>SEGUIMIENTO DE \_ MCI VCR \_ \_ SET
</dt> <dd>

Ajuste la velocidad del transporte de cinta vcr con un ajuste preciso y debe usarse con una de las marcas siguientes:

</dd> <dt>

<span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI \_ VCR \_ PLUS
</dt> <dd>

Aumenta la velocidad de transporte de cinta.

</dd> <dt>

<span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI \_ VCR \_ MENOS
</dt> <dd>

Reduce la velocidad de transporte de cinta.

</dd> <dt>

<span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>RESTABLECIMIENTO \_ DE VCR de MCI \_
</dt> <dd>

Devuelve el ajuste de seguimiento en cero.

</dd> </dl>

En el caso de los dispositivos VCR, el *parámetro lpSet* apunta a una [**estructura MCI \_ VCR SET \_ \_ PARMS.**](mci-vcr-set-parms.md)

La siguiente marca adicional se usa con el **tipo de dispositivo videodisc:**

<dl> <dt>

<span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI \_ VD \_ FORMAT \_ TRACK
</dt> <dd>

Cambia el formato de hora a pistas. MCI usa números de seguimiento continuos.

</dd> </dl>

Las siguientes marcas adicionales se usan con el **tipo de dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>ENTRADA DE \_ MCI WAVE \_
</dt> <dd>

Establece la entrada utilizada para grabar en el **miembro wInput** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>SALIDA DE MCI \_ WAVE \_
</dt> <dd>

Establece la salida utilizada para reproducir en el **miembro wOutput** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI \_ WAVE \_ SET \_ ANYINPUT
</dt> <dd>

Cualquier entrada de onda compatible con el formato actual se puede usar para la grabación.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI \_ WAVE \_ SET \_ ANYOUTPUT
</dt> <dd>

Cualquier salida de onda compatible con el formato actual se puede usar para reproducir.

</dd> <dt>

<span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI \_ WAVE \_ SET \_ AVGBYTESPERSEC
</dt> <dd>

Establece los bytes por segundo usados para reproducir, grabar y guardar en el **miembro nAvgBytesPerSec** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>\_BITSPERSAMPLE DE MCI WAVE \_ SET \_
</dt> <dd>

Establece los bits por ejemplo usados para reproducir, grabar y guardar en el **miembro nBitsPerSample** del formato de datos PCM identificado por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI \_ WAVE \_ SET \_ BLOCKALIGN
</dt> <dd>

Establece la alineación de bloques utilizada para reproducir, grabar y guardar en el **miembro nBlockAlign** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>CANALES DE MCI \_ WAVE \_ \_ SET
</dt> <dd>

El número de canales se indica en el **miembro nChannels** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI \_ WAVE \_ SET \_ FORMATTAG
</dt> <dd>

Establece el tipo de formato utilizado para reproducir, grabar y guardar en el **miembro wFormatTag** de la estructura identificada por *lpSet*. Al especificar WAVE \_ FORMAT \_ PCM, se cambia el formato a PCM.

</dd> <dt>

<span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>EJEMPLOS DE \_ MCI WAVE \_ \_ SETPERSEC
</dt> <dd>

Establece los ejemplos por segundo usados para reproducir, grabar y guardar en el **miembro nSamplesPerSec** de la estructura identificada por *lpSet*.

</dd> </dl>

En el caso de los dispositivos de audio de forma de onda, el *parámetro lpSet* apunta a una [**estructura \_ MCI WAVE SET \_ \_ PARMS.**](mci-wave-set-parms.md)

Cuando se crea el archivo para almacenar los datos, se definen varias propiedades de los datos de forma de onda. Estas propiedades describen cómo se estructuran los datos dentro del archivo y no se pueden cambiar una vez que comienza la grabación. La siguiente lista de marcas identifica estas propiedades:

-   MCI \_ WAVE \_ SET \_ AVGBYTESPERSEC
-   \_BITSPERSAMPLE DE MCI WAVE \_ SET \_
-   MCI \_ WAVE \_ SET \_ BLOCKALIGN
-   CANALES DE MCI \_ WAVE \_ \_ SET
-   MCI \_ WAVE \_ SET \_ FORMATTAG
-   EJEMPLOS DE \_ MCI WAVE \_ \_ SETPERSEC

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 


---
title: Comando MCI_SET (mmsystem. h)
description: El \_ comando set de MCI establece la información del dispositivo. Los dispositivos de audio de CD, vídeo digital, secuencia de MIDI, VCR, vídeo, superposición de vídeo y de audio y de onda reconocen este comando.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- Comando de MCI_SET de Windows multimedia
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
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "105678605"
---
# <a name="mci_set-command"></a>\_Comando MCI set

> [!NOTE]
> Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.  Dentro de este documento, hay referencias a la palabra ' Slave '. La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.  Este texto se usa tal como está actualmente el texto que se usa en los comandos. Para mantener la coherencia, este documento contiene esta palabra. Cuando se modifique esta palabra en los comandos, se corregirá este documento para que esté alineado.

El \_ comando set de MCI establece la información del dispositivo. Los dispositivos de audio de CD, vídeo digital, secuencia de MIDI, VCR, vídeo, superposición de vídeo y de audio y de onda reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms de set MCI**](mci-set-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ set:

<dl> <dt>

<span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ set \_ audio
</dt> <dd>

Un número de canal de audio se incluye en el miembro dwAudio de la estructura identificada por *lpSet*. Esta marca debe usarse con MCI \_ establecido \_ en o MCI \_ \_ desactivado. Use una de las siguientes constantes para indicar el número de canal:

</dd> <dt>

<span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ set \_ audio \_ All
</dt> <dd>

Todos los canales de audio.

</dd> <dt>

<span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI \_ set \_ audio \_ izquierda
</dt> <dd>

Canal izquierdo.

</dd> <dt>

<span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ establecer \_ audio a la \_ derecha
</dt> <dd>

Canal derecho.

</dd> <dt>

<span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>\_cerrar la \_ puerta del conjunto de MCI \_
</dt> <dd>

Cierra la cubierta multimedia (si existe).

</dd> <dt>

<span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>\_abrir la \_ puerta del conjunto de MCI \_
</dt> <dd>

Abre la cubierta multimedia (si existe).

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_
</dt> <dd>

Deshabilita el canal de audio o vídeo especificado.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_
</dt> <dd>

Habilita el canal de audio o vídeo especificado.

</dd> <dt>

<span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>\_formato de \_ hora del conjunto de MCI \_
</dt> <dd>

Un parámetro de formato de hora se incluye en el miembro **dwTimeFormat** de la estructura identificada por *lpSet*. Las marcas siguientes se usan con esta marca:

</dd> <dt>

<span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>\_bytes de formato de MCI \_
</dt> <dd>

Dentro de un formato de datos PCM (modulación por pulsos de código), cambia la descripción del miembro de hora a bytes para la entrada o salida. Reconocido por el tipo de dispositivo **WaveAudio** .

</dd> <dt>

<span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>\_marcos de formato MCI \_
</dt> <dd>

Los comandos subsiguientes usarán los marcos. Reconocido por los tipos de dispositivo **DigitalVideo**, **VCR** y **VideoDisc** .

</dd> <dt>

<span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>\_formato MCI \_ HMS
</dt> <dd>

Cambia el formato de hora a horas, minutos y segundos. Reconocido por los tipos de dispositivo **VCR** y **VideoDisc** .

</dd> <dt>

<span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>formato MCI en \_ \_ milisegundos
</dt> <dd>

Cambia el formato de hora a milisegundos. Reconocido por todos los tipos de dispositivos.

</dd> <dt>

<span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>\_formato MCI \_ MSF
</dt> <dd>

Cambia el formato de hora a minutos, segundos y fotogramas. Reconocido por los tipos de dispositivo **cdaudio** y **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>\_ejemplos de formato de MCI \_
</dt> <dd>

Cambia el formato de hora a los ejemplos de entrada o salida. Reconocido por el tipo de dispositivo **WaveAudio** .

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>\_Formato MCI \_ SMPTE \_ 24, \_ formato MCI \_ SMPTE \_ 25 y formato MCI \_ \_ SMPTE \_ 30
</dt> <dd>

Establece el formato de hora en 24, 25 y 30 fotogramas SMPTE (sociedad de los ingenieros de cine y televisión), respectivamente. Reconocido por los tipos de dispositivo **secuenciador** y **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>\_Formato MCI \_ SMPTE \_ 30DROP
</dt> <dd>

Establece el formato de hora en 30 fotograma eliminado SMPTE. Reconocido por los tipos de dispositivo **secuenciador** y **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_formato MCI \_ TMSF
</dt> <dd>

Cambia el formato de hora a pistas, minutos, segundos y fotogramas. (MCI usa números de pista continuos). Reconocido por los tipos de dispositivo **cdaudio** y **VCR** .

</dd> <dt>

<span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>\_vídeo de set MCI \_
</dt> <dd>

Establece la señal de vídeo activada o desactivada. Esta marca debe usarse con MCI \_ establecido \_ en o MCI \_ establecido en \_ OFF. Los dispositivos que no tienen vídeo devuelven MCIERR \_ función no admitida \_ .

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ set \_ FILEFORMAT
</dt> <dd>

En el miembro **dwFileFormat** de la estructura identificada por *lpSet* se incluye un parámetro de formato de archivo. En el caso de los dispositivos de vídeo digital, el formato de archivo se usa para los comandos guardar o capturar. Si se omite, puede que el valor predeterminado sea un formato definido por el controlador de dispositivo. Si el formato de archivo especificado entra en conflicto con el algoritmo y la calidad seleccionados actualmente, se cambian a los valores predeterminados para el formato de archivo. Se definen las siguientes constantes de formato de archivo:

</dd> <dt>

<span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI
</dt> <dd>

Formato AVI.

</dd> <dt>

<span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ AVSS
</dt> <dd>

Formato AVSS.

</dd> <dt>

<span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>\_DGV MCI \_ FF \_ DIB
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

<span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>\_DGV MCI \_ set \_ Seek \_ exactly
</dt> <dd>

Establece el formato utilizado para la posición. Esta marca debe usarse con MCI \_ establecido \_ en o MCI \_ \_ desactivado. Si \_ \_ se especifica MCI SET ON, la reproducción o grabación tiene acceso con precisión al marco especificado con la \_ marca MCI from. Esto podría agregar algún retraso adicional si el fotograma solicitado no es un fotograma clave. Si \_ \_ se especifica MCI SET OFF, el dispositivo buscará una imagen de fotogramas clave que preceda a la trama solicitada. En algunos archivos y dispositivos, este podría ser el primer fotograma del archivo. El valor predeterminado para esta marca depende del dispositivo.

</dd> <dt>

<span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>\_velocidad del \_ conjunto de DGV MCI \_
</dt> <dd>

Un parámetro de velocidad se incluye en el miembro **dwSpeed** de la estructura identificada por *lpSet*. La velocidad se especifica como una relación entre la velocidad de fotogramas nominal y la velocidad de fotogramas deseada, donde la velocidad de fotogramas nominal se designa como 1000. La velocidad media es 500 y la velocidad doble es 2000. El intervalo de velocidad permitido depende también del dispositivo y, posiblemente, del archivo.

</dd> <dt>

<span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_DGV MCI \_ set \_
</dt> <dd>

Cuando se usa con MCI \_ DGV \_ set \_ FILEFORMAT, \_ el conjunto de MCI establece el formato de archivo utilizado para los comandos de captura.

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpSet* apunta a una estructura [**parms de MCI \_ DGV \_ set \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **Sequencer** :

<dl> <dt>

<span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>\_ \_ formato \_ SONGPTR de MCI SEQ
</dt> <dd>

Establece el formato de hora para las unidades del puntero de la canción.

</dd> <dt>

<span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI \_ Seq \_ set \_ Master
</dt> <dd>

Establece Sequencer como un origen de datos de sincronización e indica que el tipo de sincronización se especifica en el miembro **dwMaster** de la estructura identificada por *lpSet*. MCISEQ devuelve MCIERR \_ función no admitida \_ . Las siguientes constantes se definen para el tipo de sincronización:

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ MIDI
</dt> <dd>

Sequencer enviará los datos de sincronización de formato MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE
</dt> <dd>

Sequencer enviará los datos de sincronización de formato SMPTE.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ ninguno
</dt> <dd>

Sequencer no enviará los datos de sincronización.

</dd> <dt>

<span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>desplazamiento de set de MCI \_ Seq \_ \_
</dt> <dd>

Cambia el desplazamiento SMPTE de una secuencia a la especificada por el miembro **dwOffset** de la estructura identificada por *lpSet*. Esto solo afecta a las secuencias con un tipo de división SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>\_ \_ Puerto set de MCI SEQ \_
</dt> <dd>

Establece el puerto MIDI de salida de una secuencia en el especificado por el identificador de dispositivo MIDI en el miembro **dwPort** de la estructura identificada por *lpSet*. El dispositivo cierra el puerto anterior (si existe) e intenta abrir y usar el nuevo puerto. Si se produce un error, devuelve un error y vuelve a abrir el puerto usado previamente (si existe). Las siguientes constantes se definen para los puertos:

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ ninguno
</dt> <dd>

Cierra el puerto usado previamente (si existe). Sequencer se comporta exactamente igual que si se hubiese abierto un puerto, excepto en que no se envía ningún mensaje MIDI.

</dd> <dt>

<span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>\_asignador MIDI
</dt> <dd>

Establece el puerto abierto en el asignador MIDI.

</dd> <dt>

<span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ Seq \_ set \_ Slave
</dt> <dd>

Establece el secuenciador para recibir los datos de sincronización e indica que el tipo de sincronización se especifica en el miembro **dwSlave** de la estructura identificada por *lpSet*. MCISEQ devuelve MCIERR \_ función no admitida \_ . Las siguientes constantes se definen para el tipo de sincronización:

</dd> <dt>

<span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>\_archivo de SEQ de MCI \_
</dt> <dd>

Establece Sequencer para recibir los datos de sincronización contenidos en el archivo MIDI.

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ MIDI
</dt> <dd>

Establece el secuenciador para recibir los datos de sincronización MIDI.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ ninguno
</dt> <dd>

Establece el secuenciador para omitir los datos de sincronización en una secuencia MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE
</dt> <dd>

Establece el secuenciador para recibir los datos de sincronización de SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>\_ \_ tempo set de MCI \_
</dt> <dd>

Cambia el tempo de la secuencia MIDI a la especificada por el miembro **dwTempo** de la estructura a la que apunta *lpSet*. En el caso de las secuencias con el tipo de división PPQN, el tempo se especifica en pulsaciones por minuto. en el caso de las secuencias con el tipo de división SMPTE, el tempo se especifica en fotogramas por segundo.

</dd> </dl>

En el caso de los dispositivos del secuenciador, el parámetro *lpSet* apunta a una estructura [**MCI \_ Seq \_ set \_ parms**](mci-seq-set-parms.md) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>\_registro de \_ montaje del conjunto de VCR MCI \_ \_
</dt> <dd>

Establece el dispositivo para grabar en los modos de montaje o inserción (cuando el ensamblado está desactivado, INSERT es on y viceversa). Use con una de las marcas siguientes:

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_
</dt> <dd>

Establece el registro de ensamblado en y activa la opción insertar registro. Registra todas las pistas de vídeo, audio y código de tiempo.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_
</dt> <dd>

Establece el conjunto de registros en OFF y activa insertar registro. Cuando el registro de ensamblado está desactivado, se pueden seleccionar pistas individuales de vídeo, audio y código de tiempo para la grabación.

</dd> <dt>

<span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>\_reloj del \_ conjunto de VCR MCI \_
</dt> <dd>

El miembro **dwClock** de la estructura identificada por *lpSet* contiene la nueva hora de reloj.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>forma de \_ contador de VCR MCI \_ set \_ \_
</dt> <dd>

El miembro **dwCounterFormat** de la estructura identificada por *lpSet* contiene una constante que especifica el nuevo formato de tiempo de contador que va a usar el contador de estado. Para obtener una lista de constantes válidas, consulte \_ formato de hora del conjunto de MCI \_ \_ en la lista de marcas adicionales para este comando.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>\_valor de \_ contador del conjunto de VCR MCI \_ \_
</dt> <dd>

El miembro **dwCounterValue** de la estructura identificada por *lpSet* contiene el nuevo valor de contador.

</dd> <dt>

<span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>\_Índice del \_ conjunto de VCR de MCI \_
</dt> <dd>

El miembro **dwIndex** de la estructura identificada por *lpSet* contiene una constante que indica el contenido de la presentación en pantalla y debe ser uno de los siguientes:

</dd> <dt>

<span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>\_contador de \_ Índice de VCR de MCI \_
</dt> <dd>

Muestra Counter.

</dd> <dt>

<span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>\_fecha de \_ Índice de VCR MCI \_
</dt> <dd>

Muestra la fecha.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>\_tiempo de \_ Índice de VCR MCI \_
</dt> <dd>

Muestra la hora.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>\_código de \_ tiempo del índice de VCR MCI \_
</dt> <dd>

Muestra el código de tiempo.

Para obtener más información, consulte el comando [MCI \_ index](mci-index.md) .

</dd> <dt>

<span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>\_tiempo de \_ espera de pausa de conjunto de VCR MCI \_ \_
</dt> <dd>

El miembro **dwPauseTimeout** de la estructura identificada por *lpSet* contiene la duración máxima, en milisegundos, de un comando PAUSE.

</dd> <dt>

<span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>\_duración de \_ PostRoll de conjunto de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwPostrollDuration** de la estructura identificada por *lpSet* contiene la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para frenar el transporte de VCR cuando se emite un comando de detención o pausa.

</dd> <dt>

<span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>\_energía del \_ juego de VCR MCI \_
</dt> <dd>

Permite activar o desactivar la alimentación. Debe usarse con una de las marcas siguientes:

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_
</dt> <dd>

Desactiva el apagado.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_
</dt> <dd>

Activa el encendido.

</dd> <dt>

<span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>\_duración del \_ preajuste del vídeo de \_ MCI \_
</dt> <dd>

El miembro **dwPrerollDuration** de la estructura identificada por *lpSet* contiene la longitud de la cinta de vídeo, en el formato de hora actual, necesaria para estabilizar la salida del VCR.

</dd> <dt>

<span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>\_formato de \_ registro del conjunto de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwRecordFormat** de la estructura identificada por *lpSet* contiene una constante que describe la velocidad del registro, que debe ser uno de los siguientes:

</dd> <dt>

<span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>formato de VCR de MCI \_ \_ \_ EP
</dt> <dd>

Registros a velocidad lenta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>formato de VCR de MCI \_ \_ \_ LP
</dt> <dd>

Registros a velocidad lenta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>\_SP de \_ formato \_ VCR MCI
</dt> <dd>

Registros a velocidad estándar.

</dd> <dt>

<span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>\_velocidad del \_ conjunto de VCR MCI \_
</dt> <dd>

El miembro **dwSpeed** de la estructura identificada por *lpSet* contiene la nueva configuración de velocidad, donde 1000 es la velocidad normal, 2000 es la velocidad doble y 500 es la velocidad media, y así sucesivamente.

</dd> <dt>

<span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>\_longitud de \_ cinta del conjunto de VCR MCI \_ \_
</dt> <dd>

El miembro **dwTapeLength** de la estructura identificada por *lpSet* contiene la nueva longitud de la cinta, siempre que no se detecte la longitud de la cinta.

</dd> <dt>

<span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>\_modo de \_ tiempo de conjunto de VCR MCI \_ \_
</dt> <dd>

El miembro **dwTimeMode** de la estructura identificada por *lpSet* contiene una constante que indica el nuevo modo de hora posicional. Las constantes siguientes son válidas:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_contador de \_ tiempo de VCR de MCI \_
</dt> <dd>

Obliga al dispositivo a usar el contador de forma exclusiva.

</dd> <dt>

<span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>\_detección de \_ tiempo de VCR MCI \_
</dt> <dd>

Cada vez que se inserta una nueva cinta de vídeo en el dispositivo o el modo cambia de no está listo a listo, el dispositivo debe intentar determinar si hay código de tiempo disponible en la cinta de vídeo. Si el código de tiempo está disponible, use el código de tiempo en todos los comandos subsiguientes que especifiquen posiciones. De lo contrario, use el contador.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_código de \_ tiempo de vídeo de MCI \_
</dt> <dd>

Obliga al dispositivo a usar el código de tiempo exclusivamente.

</dd> <dt>

<span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>\_seguimiento del \_ conjunto de VCR de MCI \_
</dt> <dd>

Ajusta la velocidad del transporte de cinta de VCR con un ajuste fino y debe usarse con una de las marcas siguientes:

</dd> <dt>

<span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>VCR de MCI \_ \_ Plus
</dt> <dd>

Aumenta la velocidad de transporte de la cinta.

</dd> <dt>

<span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>VCR de MCI \_ \_ menos
</dt> <dd>

Disminuye la velocidad de transporte de cinta.

</dd> <dt>

<span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>\_restablecimiento de VCR de MCI \_
</dt> <dd>

Devuelve el ajuste de seguimiento a cero.

</dd> </dl>

En el caso de los dispositivos VCR, el parámetro *lpSet* apunta a una estructura [**\_ parms de VCR VCR \_ set \_**](mci-vcr-set-parms.md) .

La siguiente marca adicional se usa con el tipo de dispositivo de **videodisco** :

<dl> <dt>

<span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>pista de formato de MCI \_ Vd \_ \_
</dt> <dd>

Cambia el formato de hora a las pistas. MCI usa números de pista continuos.

</dd> </dl>

Con el tipo de dispositivo **WaveAudio** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda de MCI \_
</dt> <dd>

Establece la entrada que se usa para la grabación en el miembro **WInput** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_salida de onda de MCI \_
</dt> <dd>

Establece la salida usada para reproducirla en el miembro **wOutput** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>ANYINPUT de onda de MCI \_ \_ set \_
</dt> <dd>

Cualquier entrada de onda compatible con el formato actual se puede usar para la grabación.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>ANYOUTPUT de onda de MCI \_ \_ set \_
</dt> <dd>

Cualquier salida de onda compatible con el formato actual se puede usar para la reproducción.

</dd> <dt>

<span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>AVGBYTESPERSEC de onda de MCI \_ \_ set \_
</dt> <dd>

Establece los bytes por segundo que se usan para reproducir, grabar y guardar en el miembro **nAvgBytesPerSec** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>BitsPerSample de onda de MCI \_ \_ set \_
</dt> <dd>

Establece los bits por muestra que se usan para reproducir, grabar y guardar en el miembro **nBitsPerSample** del formato de datos PCM identificado por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>BLOCKALIGN de onda de MCI \_ \_ set \_
</dt> <dd>

Establece la alineación de bloque utilizada para reproducir, grabar y guardar en el miembro **nBlockAlign** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>\_canales de \_ conjunto de ondas MCI \_
</dt> <dd>

El número de canales se indica en el miembro **nChannels** de la estructura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>FORMATTAG de onda de MCI \_ \_ set \_
</dt> <dd>

Establece el tipo de formato usado para reproducir, grabar y guardar en el miembro **wFormatTag** de la estructura identificada por *lpSet*. Especificar \_ \_ el formato de onda PCM cambia el formato a PCM.

</dd> <dt>

<span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>SAMPLESPERSEC de onda de MCI \_ \_ set \_
</dt> <dd>

Establece las muestras por segundo que se usan para reproducir, grabar y guardar en el miembro **nSamplesPerSec** de la estructura identificada por *lpSet*.

</dd> </dl>

En el caso de los dispositivos de audio de onda, el parámetro *lpSet* apunta a una estructura de [**\_ \_ \_ parms de onda de MCI**](mci-wave-set-parms.md) .

Se definen varias propiedades de los datos de audio de forma de onda cuando se crea el archivo en el que se almacenan los datos. Estas propiedades describen cómo se estructuran los datos en el archivo y no se pueden cambiar una vez que se inicia la grabación. La siguiente lista de marcas identifica estas propiedades:

-   AVGBYTESPERSEC de onda de MCI \_ \_ set \_
-   BitsPerSample de onda de MCI \_ \_ set \_
-   BLOCKALIGN de onda de MCI \_ \_ set \_
-   \_canales de \_ conjunto de ondas MCI \_
-   FORMATTAG de onda de MCI \_ \_ set \_
-   SAMPLESPERSEC de onda de MCI \_ \_ set \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 


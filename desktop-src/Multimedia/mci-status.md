---
title: MCI_STATUS comando (Mmsystem.h)
description: El comando MCI \_ STATUS recupera información sobre un dispositivo MCI. Todos los dispositivos reconocen este comando. Se devuelve información en el miembro dwReturn de la estructura identificada por el parámetro lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- MCI_STATUS comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370112"
---
# <a name="mci_status-command"></a>Comando MCI \_ STATUS

> [!NOTE]
> La comunicación sin sesgos de Microsoft admite un entorno diverso e inclusión.  Dentro de este documento, hay referencias a la palabra "subordinado". La Guía de estilo de Microsoft [Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra excluyente.  Esta redacción se usa, ya que actualmente es la que se usa en los comandos. Por coherencia, este documento contiene esta palabra. Cuando esta palabra se modifica en los comandos, corregiremos este documento para que esté alineado.

El comando MCI \_ STATUS recupera información sobre un dispositivo MCI. Todos los dispositivos reconocen este comando. Se devuelve información en el **miembro dwReturn** de la estructura identificada por el *parámetro lpStatus.*

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
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

<span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*
</dt> <dd>

Puntero a una [**estructura MCI \_ STATUS \_ PARMS.**](mci-status-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas estándar y específicas de comando adicionales se aplican a todos los dispositivos que admiten MCI \_ STATUS:

<dl> <dt>

<span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>ELEMENTO DE ESTADO DE MCI \_ \_
</dt> <dd>

Especifica que el **miembro dwItem** de la estructura identificada por *lpStatus* contiene una constante que especifica qué elemento de estado se va a obtener. Las constantes siguientes definen qué elemento de estado se va a devolver en el **miembro dwReturn** de la estructura :

SEGUIMIENTO ACTUAL DEL ESTADO DE MCI \_ \_ \_

El **miembro dwReturn** se establece en el número de seguimiento actual. MCI usa números de seguimiento continuos.

LONGITUD DE ESTADO DE MCI \_ \_

El **miembro dwReturn** se establece en la longitud total del medio.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MODO DE ESTADO DE MCI \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el modo actual del dispositivo. Entre los modos se incluyen los siguientes:

-   MODO MCI \_ \_ NO \_ LISTO
-   PAUSA DEL MODO MCI \_ \_
-   REPRODUCCIÓN EN MODO MCI \_ \_
-   MCI \_ MODE \_ STOP
-   MODO MCI \_ \_ ABIERTO
-   REGISTRO DEL MODO MCI \_ \_
-   MCI \_ MODE \_ SEEK

</dd> <dt>

<span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>NÚMERO DE PISTAS \_ DE ESTADO \_ \_ DE \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en el número total de pistas que se pueden reproducir.

</dd> <dt>

<span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>POSICIÓN DE ESTADO DE MCI \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en la posición actual.

</dd> <dt>

<span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>ESTADO DE MCI \_ \_ LISTO
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo está listo; de lo contrario, se **establece en FALSE.**

</dd> <dt>

<span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>FORMATO DE HORA \_ DE ESTADO \_ DE MCI \_
</dt> <dd>

El **miembro dwReturn** se establece en el formato de hora actual del dispositivo. Los formatos de hora incluyen:

-   BYTES DE FORMATO MCI \_ \_
-   MARCOS DE FORMATO MCI \_ \_
-   FORMATO MCI \_ \_ HMS
-   MILISEGUNDOS DE FORMATO MCI \_ \_
-   MCI \_ FORMAT \_ MSF
-   EJEMPLOS DE FORMATO \_ MCI \_
-   \_TMSF CON \_ FORMATO MCI

</dd> <dt>

<span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>INICIO DE ESTADO DE MCI \_ \_
</dt> <dd>

Obtiene la posición inicial del medio. Para obtener la posición inicial, combine esta marca con MCI STATUS ITEM y establezca el miembro dwItem de la estructura identificada por \_ \_ *lpStatus* en MCI STATUS  \_ \_ POSITION.

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>SEGUIMIENTO \_ DE MCI
</dt> <dd>

Indica que se incluye un parámetro de seguimiento de estado en el **miembro dwTrack** de la estructura identificada por *lpStatus*. Debe usar esta marca con las constantes MCI \_ STATUS \_ POSITION o MCI STATUS \_ \_ LENGTH. Cuando se usa con MCI \_ STATUS \_ POSITION, MCI TRACK obtiene la posición inicial de la \_ pista especificada. Cuando se usa con MCI \_ STATUS \_ LENGTH, MCI \_ TRACK obtiene la longitud de la pista especificada. MCI usa números de seguimiento continuos.

</dd> </dl>

Las siguientes marcas adicionales se usan con el tipo **de dispositivo cdaudio.** Estas constantes se usan en el **miembro dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando se especifica MCI STATUS ITEM para el \_ parámetro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>SEGUIMIENTO DEL TIPO \_ DE ESTADO DE MCI CDA \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en uno de los siguientes valores:

-   MCI \_ CDA \_ TRACK \_ AUDIO
-   MCI \_ CDA \_ TRACK \_ OTHER

Para usar esta marca, se debe establecer la marca TRACK de MCI y el miembro dwTrack de la estructura identificada por lpStatus debe contener un número de \_ seguimiento válido.  

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MEDIOS DE ESTADO DE MCI \_ \_ \_ PRESENTES
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el medio se inserta en el dispositivo; de lo contrario, se **establece en FALSE.**

</dd> </dl>

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>DISKSPACE \_ DE ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro lpstrDrive** de la estructura identificada por *lpStatus* especifica una unidad de disco o, en algunas implementaciones, una ruta de acceso. El comando STATUS de MCI devuelve la cantidad aproximada de espacio en disco que podría obtener el comando MCI RESERVE en el \_ **miembro dwReturn** de la estructura identificada [ \_](mci-reserve.md) por *lpStatus*. El espacio en disco se mide en unidades del formato de hora actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>ENTRADA DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

La constante especificada por el **miembro dwItem** de la estructura identificada por *lpStatus* se aplica a la entrada.

</dd> <dt>

<span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>ESTADO DE \_ MCI DGV \_ \_ LEFT
</dt> <dd>

La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* se aplica al canal de audio izquierdo.

</dd> <dt>

<span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI \_ DGV \_ STATUS \_ NOMINAL
</dt> <dd>

La constante especificada por el **miembro dwItem** de la estructura identificada por *lpStatus* solicita el valor nominal en lugar del valor actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>SALIDA DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

La constante especificada por el **miembro dwItem** de la estructura identificada por *lpStatus* se aplica a la salida.

</dd> <dt>

<span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>REGISTRO DE ESTADO \_ DE MCI DGV \_ \_
</dt> <dd>

La velocidad de fotogramas devuelta para la marca \_ MCI DGV \_ STATUS FRAME RATE es la velocidad usada para la \_ \_ compresión.

</dd> <dt>

<span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>REFERENCIA DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** de la estructura identificada por *lpStatus* devuelve la imagen de fotograma clave más cercana que precede al marco especificado en el **miembro dwReference.**

</dd> <dt>

<span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>DERECHO DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

La constante especificada por el **miembro dwItem** de la estructura identificada por *lpStatus* se aplica al canal de audio correcto.

</dd> </dl>

Las constantes siguientes se usan con el tipo de dispositivo **digitalvideo** en el **miembro dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando se especifica MCI STATUS ITEM para el \_ parámetro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>SALTOS DE \_ AUDIO DE ESTADO DE MCI AVI \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el número de veces que se interrumpió la parte de audio de la última secuencia AVI. El sistema cuenta una interrupción de audio cada vez que intenta escribir datos de audio en el controlador del dispositivo y detecta que el controlador ya ha reproducidos todos los datos disponibles. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>FOTOGRAMAS DE \_ ESTADO DE MCI AVI \_ \_ \_ OMITIDO
</dt> <dd>

El **miembro dwReturn** devuelve el número de fotogramas que no se dibujaron cuando se reproducía la última secuencia AVI. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>VELOCIDAD DE ÚLTIMA REPRODUCCIÓN DEL ESTADO DE MCI \_ AVI \_ \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve un valor que representa la proximidad de la hora de reproducción real de la última secuencia AVI con la hora de reproducción de destino. El valor 1000 indica que la hora de destino y la hora real eran las mismas. Un valor de 2000, por ejemplo, indicaría que la secuencia AVI tardó el doble de tiempo en reproducirse como debería. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>AUDIO DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve MCI ON o MCI OFF en función de la opción MCI SET AUDIO más reciente para \_ el comando \_ \_ \_ [MCI \_ SET.](mci-set.md) Devuelve MCI \_ ON si uno o ambos hablantes están habilitados, y MCI \_ OFF en caso contrario.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>ENTRADA DE AUDIO DE \_ ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el nivel de audio instantáneo aproximado de la señal de audio análogo. Un valor mayor que 1000 implica que hay distorsión de recorte. Algunos dispositivos solo pueden determinar este valor durante la grabación de audio. Este valor de estado no tiene ningún **comando MCI \_ SET** o [MCI \_ SETAUDIO](mci-setaudio.md) asociado. Este valor está relacionado con el comando MCI WAVE STATUS LEVEL, pero se normaliza de forma \_ \_ \_ diferente.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>REGISTRO DE AUDIO DE \_ ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve MCI ON o MCI OFF que refleja el estado establecido por la marca \_ \_ \_ MCI DGV SETAUDIO RECORD del \_ comando \_ **\_ MCI SETAUDIO.**

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>ORIGEN DE AUDIO \_ DE ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el origen del digitalizador de audio actual:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MEDIA \_ DE \_ SETAUDIO DE MCI DGV \_
</dt> <dd>

Especifica el promedio de los canales de audio izquierdo y derecho.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ LEFT
</dt> <dd>

Especifica el canal de audio izquierdo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT
</dt> <dd>

Especifica el canal de audio derecho.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ SETAUDIO \_ STEREO
</dt> <dd>

Especifica estéreo.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>SECUENCIA DE AUDIO \_ DE ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el número de secuencia de audio actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>ESTADO \_ DE MCI DGV \_ \_ AVGBYTESPERSEC
</dt> <dd>

El **miembro dwReturn** devuelve el número medio de bytes por segundo usado para la grabación.

</dd> <dt>

<span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI \_ DGV \_ STATUSGV STATUS STATUS (ESTADO DE MCI \_ DGV)
</dt> <dd>

El **miembro dwReturn** devuelve el nivel de audio actual. Use MCI \_ DGV \_ STATUS NOMINAL con esta marca para obtener el nivel \_ nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>\_BITSPERPEL DE ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el número de bits por píxel usados para guardar los datos capturados o registrados.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>\_BITSPERSAMPLE DE ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el número de bits por muestra que usa el dispositivo para la grabación. Esto solo se aplica a los dispositivos que admiten el formato PCM.

</dd> <dt>

<span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI \_ DGV \_ STATUS \_ BLOCKALIGN
</dt> <dd>

El **miembro dwReturn** devuelve la alineación de los bloques de datos con respecto al inicio de la forma de onda de entrada.

</dd> <dt>

<span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>BRILLO DEL \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el nivel de brillo del vídeo actual. Use MCI \_ DGV \_ STATUS NOMINAL con esta marca para obtener el nivel \_ nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>COLOR DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el nivel de color actual. Use MCI \_ DGV \_ STATUS NOMINAL con esta marca para obtener el nivel \_ nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>CONTRASTE DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el nivel de contraste actual. Use MCI \_ DGV \_ STATUS NOMINAL con esta marca para obtener el nivel \_ nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI \_ DGV \_ STATUS \_ FILEFORMAT
</dt> <dd>

El **miembro dwReturn** devuelve el formato de archivo actual para grabar o guardar.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MODO DE ARCHIVO \_ DE ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el estado de la operación de archivo:

EDICIÓN DEL \_ MODO DE ARCHIVO MCI DGV \_ \_ \_

Se devuelve durante las operaciones de cortar, copiar, eliminar, pegar y deshacer.

MODO DE \_ ARCHIVO MCI DGV \_ \_ INACTIVO \_

Se devuelve cuando el archivo está listo para la siguiente operación.

CARGA DEL \_ MODO DE ARCHIVO MCI DGV \_ \_ \_

Se devuelve mientras se carga el archivo.

GUARDADO DEL \_ MODO DE ARCHIVO MCI DGV \_ \_ \_

Se devuelve mientras se guarda el archivo.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>FINALIZACIÓN DEL \_ ARCHIVO DE ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el porcentaje estimado de una operación de carga, guardar, capturar, cortar, copiar, eliminar, pegar o deshacer que ha progresado. (Las aplicaciones pueden usar esto para proporcionar un indicador visual del progreso). Esta marca no es compatible con todos los dispositivos de vídeo digital.

</dd> <dt>

<span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>REENVÍO DEL \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve **TRUE si** la dirección del dispositivo es hacia delante o el dispositivo no se está reproduciendo.

</dd> <dt>

<span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>VELOCIDAD DE \_ FOTOGRAMAS DEL ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** debe usarse con MCI \_ DGV STATUS \_ \_ NOMINAL, MCI \_ DGV STATUS RECORD o \_ \_ ambos. Cuando se usa con MCI DGV STATUS RECORD, se devuelve la velocidad de fotogramas actual usada \_ para la \_ \_ grabación. Cuando se usa con MCI DGV STATUS RECORD y \_ \_ \_ MCI \_ DGV STATUS NOMINAL, se devuelve la velocidad \_ \_ de fotogramas nominal asociada a la señal de vídeo de entrada. Cuando se usa con MCI \_ DGV STATUS NOMINAL, se devuelve la velocidad de \_ \_ fotogramas nominal asociada al archivo. En todos los casos, las unidades están en fotogramas por segundo multiplicadas por 1000.

</dd> <dt>

<span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>GAMMA DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el valor gamma actual. Use MCI \_ DGV \_ STATUS NOMINAL con esta marca para obtener el nivel \_ nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI \_ DGV \_ STATUS \_ HPAL
</dt> <dd>

El **miembro dwReturn** devuelve el valor decimal ASCII para el identificador de paleta actual. El identificador está contenido en la palabra de orden bajo del valor devuelto.

</dd> <dt>

<span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>HWND \_ DE ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el valor decimal ASCII para el identificador de ventana predeterminado o explícito actual asociado a esta instancia del controlador de dispositivo. El identificador está contenido en la palabra de orden bajo del valor devuelto.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>COLOR DE LA \_ CLAVE DE ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el valor de color de clave actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>ÍNDICE DE CLAVE \_ DE ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el valor de índice de clave actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MONITOR DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve una constante que indica el origen de la presentación actual. Se definen las siguientes constantes:

ARCHIVO DE \_ SUPERVISIÓN DE MCI DGV \_ \_

Un archivo es el origen.

ENTRADA DEL \_ MONITOR MCI DGV \_ \_

La entrada es el origen.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MÉTODO DE \_ MONITOR DE ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve una constante que indica el método utilizado para la supervisión de entrada. Se definen las siguientes constantes:

MÉTODO \_ MCI DGV \_ \_ DIRECTO

Supervisión de entrada directa.

MCI \_ DGV \_ METHOD \_ POST

Supervisión posterior a la entrada.

MCI \_ DGV \_ METHOD \_ PRE

Supervisión previa a la entrada.

</dd> <dt>

<span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MODO DE PAUSA \_ DEL ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve MCI MODE PLAY si el dispositivo se ha pausado durante la reproducción y devuelve MCI MODE RECORD si el dispositivo se ha pausado \_ durante la \_ \_ \_ grabación. El comando devuelve MCIERR NONAPPLICABLE FUNCTION como una devolución \_ de error si el dispositivo no está en \_ pausa.

</dd> <dt>

<span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>EJEMPLOS DE \_ ESTADO DE MCI DGVPERSECOND \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el número de muestras por segundo grabadas.

</dd> <dt>

<span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI \_ DGV \_ STATUS \_ SEEK \_ EXACTLY
</dt> <dd>

El **miembro dwReturn** devuelve **TRUE** o **FALSE,** lo que indica si se ha establecido o no el formato de búsqueda exactamente. (Las aplicaciones pueden establecer este formato mediante el comando [MCI \_ SET](mci-set.md) con la marca \_ MCI DGV \_ SET SEEK \_ \_ EXACTLY).

</dd> <dt>

<span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_NICIEZ DEL ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el nivel de ni sharpness actual. Use MCI \_ DGV \_ STATUS NOMINAL con esta marca para obtener el nivel \_ nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>TAMAÑO DE ESTADO \_ DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve la duración aproximada de reproducción de los datos comprimidos que contendrán el área de trabajo reservada. Las unidades de duración están en el formato de hora actual. Devuelve cero si no hay espacio en disco reservado. El tamaño devuelto es aproximado, ya que el espacio en disco preciso para los datos comprimidos no se puede predecir, en general, hasta después de que se hayan comprimido los datos.

</dd> <dt>

<span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI \_ DGV \_ STATUS \_ SMPTE
</dt> <dd>

El **miembro dwReturn** devuelve el código de tiempo de SMPTE asociado a la posición actual en el área de trabajo.

</dd> <dt>

<span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>VELOCIDAD DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve la velocidad de reproducción actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI \_ DGV \_ STATUS \_ STILL \_ FILEFORMAT
</dt> <dd>

El **miembro dwReturn** devuelve el formato de archivo actual para el [comando MCI \_ CAPTURE.](mci-capture.md)

</dd> <dt>

<span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>TINT DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el nivel de tono de vídeo actual. Use MCI \_ DGV \_ STATUS NOMINAL con esta marca para obtener el nivel \_ nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI \_ DGV \_ STATUS \_ TREBLE
</dt> <dd>

El **miembro dwReturn** devuelve el nivel de audio triple actual. Use MCI \_ DGV \_ STATUS NOMINAL con esta marca para obtener el nivel \_ nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>ESTADO DE \_ MCI DGV \_ SIN \_ GUARDAR
</dt> <dd>

El **miembro dwReturn** devuelve **TRUE** si hay datos registrados en el área de trabajo que podrían perderse como resultado de un comando [MCI \_ CLOSE,](mci-close.md) [MCI \_ LOAD,](mci-load.md) [MCI \_ RECORD,](mci-record.md) [MCI \_ RESERVE,](mci-reserve.md) [MCI \_ CUT,](mci-cut.md) [MCI \_ DELETE](mci-delete.md)o [MCI \_ PASTE.](mci-paste.md) De lo contrario, el **miembro devuelve FALSE.**

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>VÍDEO DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve MCI \_ ON si el vídeo está habilitado o MCI \_ OFF si está deshabilitado.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>REGISTRO DE \_ VÍDEO DE ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve MCI ON o MCI OFF, lo que refleja el estado establecido por la marca SETVIDEO RECORD de MCI DGV del comando \_ \_ \_ \_ \_ [ \_ SETVIDEO de MCI.](mci-setvideo.md)

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>ORIGEN DEL \_ VÍDEO MCI DGV \_ STATUS \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve una constante que indica el tipo de origen de vídeo establecido por la marca MCI DGV SETVIDEO SOURCE del comando \_ \_ \_ **\_ MCI SETVIDEO.**

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI \_ DGV \_ STATUS \_ VIDEO \_ SRC \_ NUM
</dt> <dd>

El **miembro dwReturn** devuelve el número dentro de su tipo de origen de entrada de vídeo actualmente activo.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>SECUENCIA DE VÍDEO \_ DE ESTADO DE MCI DGV \_ \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el número de secuencia de vídeo actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>VOLUMEN DE \_ ESTADO DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwReturn** devuelve el promedio del volumen a los altavoces izquierdo y derecho. Use MCI \_ DGV \_ STATUS NOMINAL con esta marca para obtener el nivel \_ nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>VENTANA DE \_ ESTADO DE MCI DGV \_ \_ \_ VISIBLE
</dt> <dd>

El **miembro dwReturn** devuelve **TRUE** si la ventana no está oculta.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>VENTANA DE \_ ESTADO DE MCI DGV \_ \_ \_ MINIMIZADA
</dt> <dd>

El **miembro dwReturn** devuelve **TRUE** si se minimiza la ventana.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>VENTANA DE \_ ESTADO DE MCI DGV \_ \_ \_ MAXIMIZADA
</dt> <dd>

El **miembro dwReturn** devuelve **TRUE si** la ventana está maximizada.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MEDIOS DE ESTADO DE MCI \_ \_ \_ PRESENTES
</dt> <dd>

El **miembro dwReturn** devuelve **TRUE.**

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el *parámetro lpStatus* apunta a una estructura [**MCI \_ DGV \_ STATUS \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa)

Las siguientes marcas adicionales se usan con el **tipo de dispositivo sequencer.** Estas constantes se usan en el **miembro dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando se especifica MCI STATUS ITEM para el \_ parámetro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>DIVTYPE DE \_ ESTADO DE MCI SEQ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en uno de los siguientes valores que indican el tipo de división actual de una secuencia:

-   MCI \_ SEQ \_ DIV \_ PPQN
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 24
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 25
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 30
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP

</dd> <dt>

<span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MAESTRO DE ESTADO DE MCI \_ SEQ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el tipo de sincronización utilizado para la operación maestra.

</dd> <dt>

<span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>DESPLAZAMIENTO DE ESTADO DE MCI \_ SEQ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el desplazamiento SMPTE actual de una secuencia.

</dd> <dt>

<span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>PUERTO DE ESTADO DE MCI \_ SEQ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el identificador de dispositivo MIDI para el puerto actual utilizado por la secuencia.

</dd> <dt>

<span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>SUBORDINADO DE ESTADO DE MCI \_ SEQ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el tipo de sincronización utilizado para la operación subordinada.

</dd> <dt>

<span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>TEMPO DE ESTADO DE MCI \_ SEQ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el tempo actual de una secuencia DE MIDI en latidos por minuto para archivos PPQN o fotogramas por segundo para archivos SMPTE.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MEDIOS DE ESTADO DE MCI \_ \_ \_ PRESENTES
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el medio se inserta en el dispositivo; de lo contrario, se **establece en FALSE.**

</dd> </dl>

Las siguientes marcas adicionales se usan con el tipo **de dispositivo vcr.** Estas constantes se usan en el **miembro dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando se especifica MCI STATUS ITEM para el \_ parámetro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MEDIOS DE ESTADO DE MCI \_ \_ \_ PRESENTES
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el medio se inserta en el dispositivo; de lo contrario, se **establece en FALSE.**

</dd> <dt>

<span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>REGISTRO MCI \_ VCR \_ STATUS \_ ASSEMBLE \_
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE si** el modo de ensamblado está activo; de lo contrario, se **establece en FALSE.**

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MONITOR DE \_ AUDIO DE ESTADO DE VCR \_ \_ de \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en una constante, que indica el tipo de monitor de audio seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>NÚMERO DE MONITOR \_ DE AUDIO DE ESTADO DE MCI VCR \_ \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el número del tipo de monitor de audio seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>REGISTRO DE AUDIO \_ DE ESTADO DE VCR \_ \_ de \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE si** se grabará audio cuando se haya dado el siguiente comando de registro; de lo contrario, se **establece en FALSE.** Si especifica MCI TRACK en el parámetro \_ *dwFlags* de este comando, **dwTrack** contiene el seguimiento al que se aplica esta consulta.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>ORIGEN DE AUDIO \_ DE ESTADO DE VCR \_ \_ MCI \_
</dt> <dd>

El **miembro dwReturn** se establece en una constante, que indica el tipo de origen de audio actual.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>NÚMERO DE ORIGEN \_ DE AUDIO DE ESTADO DE MCI VCR \_ \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el número del tipo de origen de audio seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>RELOJ DE ESTADO \_ DE VCR \_ de MCI \_
</dt> <dd>

El **miembro dwReturn** se establece en el valor del reloj actual, en incrementos de reloj totales.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>ID. DE RELOJ \_ DE ESTADO DE VCR \_ \_ de \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en un número que describe de forma única el reloj en uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>FORMATO DEL CONTADOR \_ DE ESTADO DE MCI VCR \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en una constante que describe el formato de contador actual. Para obtener más información, vea la marca MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>RESOLUCIÓN DEL CONTADOR \_ DE ESTADO DE MCI VCR \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en una constante que describe la resolución del contador y es uno de los valores siguientes:

-   MARCOS \_ RES DE MCI VCR \_ \_ \_ COUNTER: el contador tiene resolución de fotogramas.
-   MCI \_ VCR \_ COUNTER \_ RES \_ SECONDS: el contador tiene una resolución de segundos.
-   VALOR DEL CONTADOR DE ESTADO DE MCI \_ VCR: el miembro dwReturn se establece en la lectura del contador \_ \_ \_ actual, en el formato de tiempo de contador actual. 

</dd> <dt>

<span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>VELOCIDAD DE \_ FOTOGRAMAS DE ESTADO DE VCR \_ \_ DE \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en la velocidad de fotogramas nativa actual del dispositivo.

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>ÍNDICE DE ESTADO \_ DE VCR \_ DE MCI \_
</dt> <dd>

El **miembro dwReturn** se establece en una constante, que describe el contenido actual de la pantalla y es uno de los siguientes:

-   CONTADOR DE \_ ÍNDICE DE VCR \_ DE MCI \_
-   MCI \_ VCR \_ INDEX \_ DATE
-   HORA DEL \_ ÍNDICE DE VCR \_ \_ DE MCI
-   CÓDIGO DE \_ TIEMPO DEL ÍNDICE DE VCR \_ \_ DE MCI

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>ÍNDICE DE \_ ESTADO DE VCR \_ \_ MCI \_ ON
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si la pantalla está en pantalla; de lo contrario, se **establece en FALSE.**

</dd> <dt>

<span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>TIPO DE MEDIO \_ DE ESTADO DE MCI VCR \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en uno de los siguientes elementos:

-   MCI \_ VCR \_ MEDIA \_ 8MM
-   MCI \_ VCR \_ MEDIA \_ HI8
-   VHS \_ MULTIMEDIA MCI VCR \_ \_
-   MCI \_ VCR \_ MEDIA \_ SVHS
-   MCI \_ VCR \_ MEDIA \_ BETA
-   MCI \_ VCR \_ MEDIA \_ EDBETA
-   MCI \_ VCR \_ MEDIA \_ OTHER

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>NÚMERO DE ESTADO \_ DE VCR \_ de MCI \_
</dt> <dd>

El **miembro dwNumber** se establece en el número de ajuste lógico cuando se usa esta marca con la marca \_ MCI VCR \_ STATUS \_ TUNER \_ CHANNEL.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>NÚMERO DE ESTADO DE VCR DE MCI \_ \_ DE PISTAS DE \_ \_ \_ \_ AUDIO
</dt> <dd>

El **miembro dwReturn** se establece en el número de pistas de audio que se pueden seleccionar de forma independiente.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>NÚMERO DE \_ PISTAS DE VÍDEO DE ESTADO DE VCR \_ \_ \_ \_ DE \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en el número de pistas de vídeo que se pueden seleccionar de forma independiente.

</dd> <dt>

<span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>TIEMPO DE ESPERA \_ DE PAUSA DE ESTADO DE VCR MCI \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en la duración máxima, en milisegundos, de un comando pause. El valor devuelto de cero indica que no se producirá ningún tiempo de espera.

</dd> <dt>

<span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>FORMATO DE REPRODUCCIÓN \_ DE ESTADO DE MCI VCR \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en uno de los siguientes elementos:

-   MCI \_ VCR \_ FORMAT \_ EP
-   MCI \_ VCR \_ FORMAT \_ LP
-   MCI \_ VCR \_ FORMAT \_ OTHER
-   MCI \_ VCR \_ FORMAT \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>DURACIÓN DEL \_ POSTROLL DEL ESTADO DE MCI VCR \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en la longitud de la cinta de vídeo que se reproducirá después del lugar en el que se detuvo, en el formato de hora actual. Esto es necesario para interrumpir el transporte de cinta vcr desde un comando de detenerse o pausar.

</dd> <dt>

<span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI \_ VCR \_ STATUS \_ POWER \_ ON
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si la alimentación está encendido; de lo contrario, se **establece en FALSE.**

</dd> <dt>

<span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>DURACIÓN DE \_ LA INSCRIPCIÓN PREVIA DEL ESTADO DE VCR \_ \_ \_ DE MCI
</dt> <dd>

El **miembro dwReturn** se establece en la longitud de la cinta de vídeo que se reproducirá antes del lugar en el que se inició, en el formato de hora actual. Esto es necesario para estabilizar la salida de VCR.

</dd> <dt>

<span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>FORMATO DE REGISTRO \_ DE ESTADO DE MCI VCR \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en uno de los siguientes elementos:

-   MCI \_ VCR \_ FORMAT \_ EP
-   MCI \_ VCR \_ FORMAT \_ LP
-   MCI \_ VCR \_ FORMAT \_ OTHER
-   MCI \_ VCR \_ FORMAT \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>VELOCIDAD DE ESTADO \_ DE VCR \_ de MCI \_
</dt> <dd>

El **miembro dwReturn** se establece en la velocidad actual. Para obtener más información, vea la marca \_ MCI VCR \_ SET SPEED del comando \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MODO DE TIEMPO \_ DE ESTADO DE VCR \_ \_ DE \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en uno de los siguientes elementos:

-   CONTADOR DE TIEMPO \_ DE VCR \_ de MCI \_
-   MCI \_ VCR \_ TIME \_ DETECT
-   CÓDIGO DE \_ TIEMPO DE VCR \_ \_ de MCI

Para obtener más información, vea la marca \_ MCI VCR \_ SET TIME MODE del comando \_ \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>TIPO DE HORA \_ DE ESTADO DE VCR \_ \_ MCI \_
</dt> <dd>

El **miembro dwReturn** se establece en una constante que describe el tipo de hora actual en uso (utilizado por [play](play.md), [record](record.md), [seek,](seek.md)y así sucesivamente) y es uno de los siguientes:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>CONTADOR DE TIEMPO \_ DE VCR \_ de MCI \_
</dt> <dd>

El contador está en uso.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>CÓDIGO DE \_ TIEMPO DE VCR \_ \_ de MCI
</dt> <dd>

El código de tiempo está en uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>CÓDIGO DE \_ TIEMPO DE ESTADO DE VCR DE MCI \_ \_ \_ PRESENTE
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE si** el código de tiempo está presente en la posición actual del contenido; de lo contrario, se **establece en FALSE.**

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>REGISTRO DE \_ CÓDIGO DE TIEMPO DE ESTADO DE VCR \_ \_ DE \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE si** el código de tiempo se registrará cuando se haya dado el siguiente comando de registro; de lo contrario, se **establece en FALSE.**

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>TIPO DE \_ CÓDIGO DE TIEMPO DE ESTADO \_ \_ DE \_ MCI VCR
</dt> <dd>

El **miembro dwReturn** se establece en una constante, que describe el tipo de código de tiempo que es compatible directamente con el dispositivo y es uno de los siguientes:

-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ NONE: este dispositivo no usa un código de tiempo.
-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ OTHER: este dispositivo usa un código de tiempo no especificado.
-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ SMPTE: este dispositivo usa el código de tiempo SMPTE.
-   MCI \_ VCR \_ TIMECODE TYPE SMPTE DROP: este dispositivo usa el código de tiempo de colocación \_ \_ de \_ SMPTE.

</dd> <dt>

<span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>CANAL DE \_ TUNER DE ESTADO DE VCR \_ \_ \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en el número de canal actual. Si especifica MCI VCR STATUS NUMBER en el parámetro dwFlags de este \_ \_ \_ comando, **dwNumber**  contiene el número de afinador lógico al que se aplica este comando.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MONITOR DE \_ VÍDEO DE ESTADO DE MCI VCR \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en una constante, que indica el tipo de monitor de vídeo seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>NÚMERO DE \_ MONITOR DE VÍDEO DE ESTADO \_ \_ DE \_ MCI VCR \_
</dt> <dd>

El **miembro dwReturn** se establece en el número del tipo de monitor de vídeo seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>REGISTRO DE \_ VÍDEO DE ESTADO DE MCI VCR \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE si** el vídeo se grabará cuando se haya dado el siguiente comando de registro; de lo contrario, se **establece en FALSE.** Si especifica MCI TRACK en el parámetro \_ *dwFlags* de este comando, **dwTrack** contiene el seguimiento al que se aplica esta consulta.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>ORIGEN DEL \_ VÍDEO MCI VCR \_ STATUS \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en una constante que indica el tipo de origen de vídeo seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>NÚMERO DE ORIGEN \_ DEL VÍDEO DE ESTADO DE MCI VCR \_ \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el número del tipo de origen de vídeo seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI \_ VCR \_ STATUS \_ WRITE \_ PROTECTED
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el medio está protegido por escritura; de lo contrario, se **establece en FALSE.**

</dd> </dl>

En el caso de los dispositivos VCR, el *parámetro lpStatus* apunta a una estructura [**MCI \_ VCR \_ STATUS \_ PARMS.**](mci-vcr-status-parms.md)

El uso de la marca STATUS LENGTH de MCI para determinar la longitud del medio siempre devuelve 2 horas para los dispositivos VCR, a menos que la longitud se haya cambiado explícitamente mediante el \_ \_ comando [MCI \_ SET.](mci-set.md)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo de** superposición. Estas constantes se usan en el **miembro dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando se especifica MCI STATUS ITEM para el \_ parámetro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>HWND DE ESTADO DE MCI \_ OVLY \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el identificador de la ventana asociada al dispositivo de superposición de vídeo.

</dd> <dt>

<span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI \_ OVLY \_ STATUS \_ STRETCH
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE si** el ajuste está habilitado; de lo contrario, se **establece en FALSE.**

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MEDIOS DE ESTADO DE MCI \_ \_ \_ PRESENTES
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el medio se inserta en el dispositivo; de lo contrario, se **establece en FALSE.**

</dd> </dl>

Las marcas adicionales siguientes se usan con el tipo **de dispositivo videodisc.** Estas constantes se usan en el **miembro dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando se especifica MCI STATUS ITEM para el \_ parámetro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MEDIOS DE ESTADO DE MCI \_ \_ \_ PRESENTES
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el medio se inserta en el dispositivo; de lo contrario, se **establece en FALSE.**

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MODO DE ESTADO DE MCI \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el modo actual del dispositivo. Los dispositivos Videodisc pueden devolver la constante MCI VD MODE PARK, además de las constantes que cualquier dispositivo puede devolver, como se documenta con el \_ \_ parámetro \_ *dwFlags.*

</dd> <dt>

<span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>TAMAÑO DEL \_ DISCO DE ESTADO DE MCI VD \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el tamaño del disco cargado en pulgadas (8 o 12).

</dd> <dt>

<span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI \_ VD \_ STATUS \_ FORWARD
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE si** se reproduce hacia delante; de lo contrario, se **establece en FALSE.**

El dispositivo de vídeo de MCI no admite esta marca.

</dd> <dt>

<span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>TIPO DE MEDIO \_ DE \_ ESTADO VD \_ DE \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en el tipo de medio del medio insertado. Se pueden devolver los siguientes tipos de medios:

MCI \_ VD \_ MEDIA \_ VEZ

MCI \_ VD \_ MEDIA \_ CLV

MCI \_ VD \_ MEDIA \_ OTHER

</dd> <dt>

<span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>LADO DE ESTADO VD DE MCI \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en 1 o 2 para indicar qué lado del disco se carga. No todos los dispositivos videodisc admiten esta marca.

</dd> <dt>

<span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>VELOCIDAD DE ESTADO VD de MCI \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en la velocidad de reproducción en fotogramas por segundo. The MCIPIONR. El controlador de dispositivo DRV devuelve MCIERR \_ UNSUPPORTED \_ FUNCTION.

</dd> </dl>

Las siguientes marcas adicionales se usan con el **tipo de dispositivo waveaudio.** Estas constantes se usan en el **miembro dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando se especifica MCI STATUS ITEM para el \_ parámetro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI \_ WAVE \_ FORMATTAG
</dt> <dd>

El **miembro dwReturn** se establece en la etiqueta de formato actual que se usa para reproducir, grabar y guardar.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>ENTRADA DE \_ MCI WAVE \_
</dt> <dd>

El **miembro dwReturn** se establece en el dispositivo de entrada de onda que se usa para la grabación. Si no hay ningún dispositivo en uso y no se ha establecido explícitamente ningún dispositivo, la devolución del error es MCIERR \_ WAVE \_ INPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>SALIDA DE MCI \_ WAVE \_
</dt> <dd>

El **miembro dwReturn** se establece en el dispositivo de salida de onda que se usa para la reproducción. Si no hay ningún dispositivo en uso y no se ha establecido explícitamente ningún dispositivo, la devolución del error es MCIERR \_ WAVE \_ OUTPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>ESTADO DE ONDA DE MCI \_ \_ \_ AVGBYTESPERSEC
</dt> <dd>

El **miembro dwReturn** se establece en los bytes actuales por segundo usados para reproducir, grabar y guardar.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>\_BITSPERSAMPLE DE ESTADO DE ONDA \_ \_ MCI
</dt> <dd>

El **miembro dwReturn** se establece en los bits actuales por ejemplo usados para reproducir, grabar y guardar datos con formato PCM.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI \_ WAVE \_ STATUS \_ BLOCKALIGN
</dt> <dd>

El **miembro dwReturn** se establece en la alineación del bloque actual que se usa para reproducir, grabar y guardar.

</dd> <dt>

<span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>CANALES DE \_ ESTADO DE MCI WAVE \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el recuento de canales actual que se usa para reproducir, grabar y guardar.

</dd> <dt>

<span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>NIVEL DE ESTADO \_ DE MCI WAVE \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el nivel de reproducción o registro actual de los datos con formato PCM. El valor se devuelve como un valor de 8 o 16 bits, según el tamaño de la muestra utilizado. El nivel de canal derecho o mono se devuelve en la palabra de orden inferior. El nivel de canal izquierdo se devuelve en la palabra de orden superior.

</dd> <dt>

<span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>EJEMPLOS DE ESTADO \_ DE MCI \_ \_ WAVEPERSEC
</dt> <dd>

El **miembro dwReturn** se establece en los ejemplos actuales por segundo que se usan para reproducir, grabar y guardar.

</dd> </dl>

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
</dt> <dt>

[MCI \_ CUT](mci-cut.md)
</dt> <dt>

[MCI \_ DELETE](mci-delete.md)
</dt> <dt>

[PEGAR \_ MCI](mci-paste.md)
</dt> <dt>

[MCI \_ RESERVE](mci-reserve.md)
</dt> <dt>

[MCI \_ SET](mci-set.md)
</dt> <dt>

[Jugar](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[Buscar](seek.md)
</dt> </dl>

 


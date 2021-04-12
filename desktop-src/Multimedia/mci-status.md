---
title: Comando MCI_STATUS (mmsystem. h)
description: El \_ comando MCI status recupera información acerca de un dispositivo MCI. Todos los dispositivos reconocen este comando. La información se devuelve en el miembro dwReturn de la estructura identificada por el parámetro lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- Comando de MCI_STATUS de Windows multimedia
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
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "104361737"
---
# <a name="mci_status-command"></a>Comando de estado de MCI \_

> [!NOTE]
> Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.  Dentro de este documento, hay referencias a la palabra ' Slave '. La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.  Este texto se usa tal como está actualmente el texto que se usa en los comandos. Para mantener la coherencia, este documento contiene esta palabra. Cuando se modifique esta palabra en los comandos, se corregirá este documento para que esté alineado.

El \_ comando MCI status recupera información acerca de un dispositivo MCI. Todos los dispositivos reconocen este comando. La información se devuelve en el miembro **dwReturn** de la estructura identificada por el parámetro *lpStatus* .

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms de estado de MCI**](mci-status-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Se aplican las siguientes marcas estándar y específicas del comando adicionales a todos los dispositivos que admiten el estado de MCI \_ :

<dl> <dt>

<span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_elemento de estado de MCI \_
</dt> <dd>

Especifica que el miembro **dwItem** de la estructura identificada por *lpStatus* contiene una constante que especifica qué elemento de estado se debe obtener. Las constantes siguientes definen qué elemento de estado se va a devolver en el miembro **dwReturn** de la estructura:

\_ \_ pista actual de estado de MCI \_

El miembro **dwReturn** se establece en el número de seguimiento actual. MCI usa números de pista continuos.

\_longitud de estado de MCI \_

El miembro **dwReturn** se establece en la longitud total del medio.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modo de estado de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el modo actual del dispositivo. Entre los modos se incluyen los siguientes:

-   \_modo MCI \_ no \_ listo
-   \_pausar modo MCI \_
-   \_reproducción en modo MCI \_
-   \_detención del modo MCI \_
-   \_modo MCI \_ abierto
-   \_registro en modo MCI \_
-   \_búsqueda en modo MCI \_

</dd> <dt>

<span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_ \_ número \_ de seguimiento de estado de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el número total de pistas que se van a reproducir.

</dd> <dt>

<span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>\_posición de estado de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en la posición actual.

</dd> <dt>

<span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>Estado de MCI \_ \_ preparado
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo está listo; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>\_formato de \_ hora de estado de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el formato de hora actual del dispositivo. Los formatos de hora incluyen:

-   \_bytes de formato de MCI \_
-   \_marcos de formato MCI \_
-   \_formato MCI \_ HMS
-   formato MCI en \_ \_ milisegundos
-   \_formato MCI \_ MSF
-   \_ejemplos de formato de MCI \_
-   \_formato MCI \_ TMSF

</dd> <dt>

<span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>\_Inicio de estado de MCI \_
</dt> <dd>

Obtiene la posición inicial del elemento multimedia. Para obtener la posición inicial, combine esta marca con el \_ elemento de estado \_ de MCI y establezca el miembro **dwItem** de la estructura identificada por *lpStatus* en la posición de estado de MCI \_ \_ .

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>pista de MCI \_
</dt> <dd>

Indica que un parámetro de seguimiento de estado se incluye en el miembro **dwTrack** de la estructura identificada por *lpStatus*. Debe usar esta marca con las constantes de \_ posición de estado de MCI o de \_ longitud de estado de MCI \_ \_ . Cuando se usa con \_ la \_ posición de estado de MCI, MCI \_ Track obtiene la posición inicial de la pista especificada. Cuando se usa con \_ la \_ longitud del estado de MCI, MCI \_ Track obtiene la longitud de la pista especificada. MCI usa números de pista continuos.

</dd> </dl>

Se usan las siguientes marcas adicionales con el tipo de dispositivo **cdaudio** . Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .

<dl> <dt>

<span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>\_pista de \_ tipo de estado \_ \_ de MCI CDA
</dt> <dd>

El miembro **dwReturn** se establece en uno de los siguientes valores:

-   \_audio de \_ rastreo de de MCI CDA \_
-   pista de MCI \_ CDA \_ \_ otro

Para usar esta marca, \_ se debe establecer la marca de pista de MCI y el miembro **dwTrack** de la estructura identificada por *lpStatus* debe contener un número de seguimiento válido.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .

</dd> </dl>

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>\_Estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **lpstrDrive** de la estructura identificada por *lpStatus* especifica una unidad de disco o, en algunas implementaciones, una ruta de acceso. El \_ comando MCI status devuelve la cantidad aproximada de espacio en disco que podría obtener el comando de [ \_ reserva de MCI](mci-reserve.md) en el miembro **dwReturn** de la estructura identificada por *lpStatus*. El espacio en disco se mide en unidades del formato de hora actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>\_entrada de \_ Estado de DGV de MCI \_
</dt> <dd>

La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* se aplica a la entrada.

</dd> <dt>

<span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>Estado de DGV de MCI \_ \_ \_ restante
</dt> <dd>

La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* se aplica al canal de audio izquierdo.

</dd> <dt>

<span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>Estado de DGV de MCI \_ \_ \_ nominal
</dt> <dd>

La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* solicita el valor nominal en lugar del valor actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>\_salida de \_ Estado de DGV de MCI \_
</dt> <dd>

La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* se aplica a la salida.

</dd> <dt>

<span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>registro de estado de MCI \_ DGV \_ \_
</dt> <dd>

La velocidad de fotogramas devuelta para la \_ \_ marca de velocidad de fotogramas de estado de MCI DGV \_ \_ es la velocidad usada para la compresión.

</dd> <dt>

<span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>\_referencia de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** de la estructura identificada por *lpStatus* devuelve la imagen de fotograma clave más cercana que precede al marco especificado en el miembro **dwReference** .

</dd> <dt>

<span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>\_derecho de \_ Estado de DGV de MCI \_
</dt> <dd>

La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* se aplica al canal de audio derecho.

</dd> </dl>

Las constantes siguientes se usan con el tipo de dispositivo **DigitalVideo** en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .

<dl> <dt>

<span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>dessaltos de audio de estado de MCI \_ AVI \_ \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve el número de veces que se ha interrumpido la parte de audio de la última secuencia AVI. El sistema cuenta una interrupción de audio cada vez que intenta escribir datos de audio en el controlador de dispositivo y detecta que el controlador ya ha reproducido todos los datos disponibles. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>\_tramas de estado de MCI AVI \_ \_ \_ omitidas
</dt> <dd>

El miembro **dwReturn** devuelve el número de fotogramas que no se dibujaron cuando se reprodujo la última secuencia AVI. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>\_velocidad de \_ \_ última \_ reproducción \_ de estado de MCI AVI
</dt> <dd>

El miembro **dwReturn** devuelve un valor que representa la proximidad del tiempo de reproducción real de la última secuencia de AVI con el tiempo de reproducción del destino. El valor 1000 indica que la hora de destino y la hora real eran iguales. Un valor de 2000, por ejemplo, indicaría que la secuencia AVI tardó dos veces más en ejecutarse que debiera. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>\_audio de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve MCI \_ on o MCI \_ OFF según la opción de audio Set MCI más reciente \_ \_ para el comando [MCI \_ set](mci-set.md) . Devuelve MCI \_ en caso de que uno o ambos altavoces estén habilitados y MCI esté \_ desactivado.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>\_entrada de \_ audio de estado DGV \_ de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el nivel de audio instantáneo aproximado de la señal de audio analógico. Un valor mayor que 1000 implica que hay distorsión de recorte. Algunos dispositivos pueden determinar este valor solo al grabar audio. Este valor de estado no tiene asociado ningún comando MCI **\_ set** o [ \_ SETAUDIO MCI](mci-setaudio.md) . Este valor está relacionado con el nivel de estado de onda MCI de comando de audio de onda, pero normalizado de forma diferente a este \_ \_ \_ .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>\_registro de \_ audio de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve MCI \_ on o MCI \_ OFF para reflejar el estado establecido por la \_ marca MCI DGV \_ SETAUDIO \_ Record del comando **MCI \_ SETAUDIO** .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>\_origen de \_ audio de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve el origen del digitalizador de audio actual:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>media de DGV de MCI \_ \_ SETAUDIO \_
</dt> <dd>

Especifica el promedio de los canales de audio izquierdo y derecho.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_DGV MCI \_ SETAUDIO \_ izquierda
</dt> <dd>

Especifica el canal de audio izquierdo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>\_DGV MCI \_ SETAUDIO \_ derecha
</dt> <dd>

Especifica el canal de audio derecho.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ SETAUDIO \_ estéreo
</dt> <dd>

Especifica estéreo.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>\_secuencia de \_ audio de estado DGV \_ de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el número de secuencia de audio actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI \_ DGV \_ status \_ AVGBYTESPERSEC
</dt> <dd>

El miembro **dwReturn** devuelve el número promedio de bytes por segundo que se usan para la grabación.

</dd> <dt>

<span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>\_ \_ graves estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el nivel de graves de audio actual. Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>Estado de DGV de MCI \_ \_ \_ BITSPERPEL
</dt> <dd>

El miembro **dwReturn** devuelve el número de bits por píxel que se usa para guardar los datos capturados o grabados.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI \_ DGV \_ status \_ BitsPerSample
</dt> <dd>

El miembro **dwReturn** devuelve el número de bits por muestra que el dispositivo usa para la grabación. Esto solo se aplica a los dispositivos que admiten el formato PCM.

</dd> <dt>

<span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI \_ DGV \_ status \_ BLOCKALIGN
</dt> <dd>

El miembro **dwReturn** devuelve la alineación de los bloques de datos en relación con el inicio de la onda de entrada.

</dd> <dt>

<span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>\_brillo de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el nivel de brillo del vídeo actual. Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>\_color de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el nivel de color actual. Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>\_contraste de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el nivel de contraste actual. Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI \_ DGV \_ status \_ FILEFORMAT
</dt> <dd>

El miembro **dwReturn** devuelve el formato de archivo actual para grabar o guardar.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>\_modo de \_ archivo de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve el estado de la operación de archivo:

\_edición del \_ modo de archivo MCI DGV \_ \_

Se devuelve durante las operaciones de cortar, copiar, eliminar, pegar y deshacer.

\_modo de archivo DGV de MCI \_ \_ \_ inactivo

Se devuelve cuando el archivo está listo para la siguiente operación.

\_carga del \_ modo de archivo MCI DGV \_ \_

Se devuelve mientras se carga el archivo.

\_guardado del \_ modo de archivo MCI DGV \_ \_

Se devuelve mientras se guarda el archivo.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>\_ \_ \_ finalización del archivo de estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el porcentaje estimado de progreso de una operación de carga, guardado, captura, cortar, copiar, eliminar, pegar o deshacer. (Las aplicaciones pueden utilizar esto para proporcionar un indicador visual de progreso). Esta marca no es compatible con todos los dispositivos de vídeo digital.

</dd> <dt>

<span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>Estado de DGV de MCI \_ \_ \_ hacia delante
</dt> <dd>

El miembro **dwReturn** devuelve **true** si la dirección del dispositivo es reenviar o si el dispositivo no se está reproduciendo.

</dd> <dt>

<span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>\_velocidad de \_ \_ fotogramas de estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** debe usarse con el \_ Estado de DGV de MCI \_ \_ nominal, el registro de estado de \_ DGV MCI \_ \_ o ambos. Cuando se usa con \_ el registro de estado de DGV de MCI \_ \_ , se devuelve la velocidad de fotogramas actual utilizada para la grabación. Cuando se usa con el estado de MCI DGV status \_ \_ \_ y MCI \_ DGV \_ status \_ , la velocidad de fotogramas nominal asociada a la señal de vídeo de entrada se devuelve. Cuando se usa con el \_ Estado DGV de MCI \_ \_ , se devuelve la velocidad de fotogramas nominal asociada al archivo. En todos los casos, las unidades están en fotogramas por segundo multiplicada por 1000.

</dd> <dt>

<span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>\_gamma de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el valor gamma actual. Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI \_ DGV \_ status \_ HPAL
</dt> <dd>

El miembro **dwReturn** devuelve el valor decimal ASCII para el identificador de la paleta actual. El identificador está contenido en la palabra de orden inferior del valor devuelto.

</dd> <dt>

<span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>\_DGV de \_ estado \_ hWnd de MCI
</dt> <dd>

El miembro **dwReturn** devuelve el valor decimal ASCII para el identificador de ventana explícito o predeterminado asociado a esta instancia de controlador de dispositivo. El identificador está contenido en la palabra de orden inferior del valor devuelto.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>\_color de \_ clave de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve el valor de color de la clave actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>\_Índice de \_ clave de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve el valor de índice de clave actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>\_monitor de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve una constante que indica el origen de la presentación actual. Se definen las constantes siguientes:

\_archivo de \_ supervisión MCI DGV \_

Un archivo es el origen.

\_entrada de \_ monitor de DGV de MCI \_

La entrada es el origen.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>\_método de \_ supervisión de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve una constante que indica el método que se usa para la supervisión de entradas. Se definen las constantes siguientes:

\_método DGV de MCI \_ \_ directo

Supervisión de entrada directa.

\_post del \_ método \_ DGV de MCI

Supervisión posterior a la entrada.

\_método MCI \_ DGV \_ pre

Supervisión de entrada previa.

</dd> <dt>

<span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>\_modo de \_ pausa de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve el \_ modo MCI \_ Play si el dispositivo se pausó mientras se reproduce y devuelve \_ un registro en modo MCI \_ si el dispositivo se pausó durante la grabación. El comando devuelve la \_ función MCIERR \_ no aplicable como un error devuelto si el dispositivo no está en pausa.

</dd> <dt>

<span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI \_ DGV \_ status \_ SAMPLESPERSECOND
</dt> <dd>

El miembro **dwReturn** devuelve el número de muestras por segundo grabadas.

</dd> <dt>

<span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>el \_ Estado de DGV de MCI \_ \_ busca \_ exactamente
</dt> <dd>

El miembro **dwReturn** devuelve **true** o **false** que indica si se ha establecido o no el formato de búsqueda exactamente. (Las aplicaciones pueden establecer este formato con el comando [MCI \_ set](mci-set.md) con el \_ marcador MCI DGV \_ set \_ Seek \_ Exactly).

</dd> <dt>

<span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_nitidez de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el nivel de nitidez actual. Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>\_tamaño de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve la duración de reproducción aproximada de los datos comprimidos que conservará el área de trabajo reservada. Las unidades de duración están en el formato de hora actual. Devuelve cero si no hay espacio en disco reservado. El tamaño devuelto es aproximado, ya que el espacio en disco preciso para los datos comprimidos no puede predecirse hasta que se hayan comprimido los datos.

</dd> <dt>

<span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>Estado de DGV de MCI \_ \_ \_ SMPTE
</dt> <dd>

El miembro **dwReturn** devuelve el código de tiempo SMPTE asociado a la posición actual en el área de trabajo.

</dd> <dt>

<span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>\_velocidad de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve la velocidad de reproducción actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>Estado de DGV de MCI \_ \_ \_ todavía \_ FILEFORMAT
</dt> <dd>

El miembro **dwReturn** devuelve el formato de archivo actual para el comando [MCI \_ Capture](mci-capture.md) .

</dd> <dt>

<span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>\_matiz de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el nivel de matiz de vídeo actual. Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>Estado de DGV de MCI \_ \_ \_ agudos
</dt> <dd>

El miembro **dwReturn** devuelve el nivel de agudos de audio actual. Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>Estado de DGV de MCI sin \_ \_ \_ Guardar
</dt> <dd>

El miembro **dwReturn** devuelve **true** si hay datos registrados en el área de trabajo que podrían perderse como resultado de un [comando MCI \_ Close](mci-close.md), MCI [ \_ Load](mci-load.md), [MCI \_ Record](mci-record.md), MCI [ \_ reserva](mci-reserve.md), MCI [ \_ CUT](mci-cut.md), [MCI \_ Delete](mci-delete.md)o [MCI \_ Paste](mci-paste.md) . De lo contrario, el miembro devuelve **false** .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>\_vídeo de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve MCI \_ en si el vídeo está HABILITAdo o MCI \_ desactivado si está deshabilitado.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>\_registro de \_ vídeo de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve MCI \_ on o MCI \_ OFF, que refleja el estado establecido por la \_ marca MCI DGV \_ SETVIDEO \_ Record del comando [MCI \_ SETVIDEO](mci-setvideo.md) .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>\_origen de \_ vídeo de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve una constante que indica el tipo de origen de vídeo establecido por la \_ marca de origen MCI DGV \_ SETVIDEO \_ del comando **MCI \_ SETVIDEO** .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>Estado de DGV de MCI \_ \_ vídeo de estado \_ \_ src \_ NUM
</dt> <dd>

El miembro **dwReturn** devuelve el número dentro de su tipo de origen de entrada de vídeo activo actualmente.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>\_secuencia de \_ vídeo de estado de DGV de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** devuelve el número de secuencia de vídeo actual.

</dd> <dt>

<span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>\_volumen de \_ Estado de DGV de MCI \_
</dt> <dd>

El miembro **dwReturn** devuelve el promedio del volumen a los altavoces izquierdo y derecho. Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>ventana de estado de DGV de MCI \_ \_ \_ \_ visible
</dt> <dd>

El miembro **dwReturn** devuelve **true** si la ventana no está oculta.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>ventana de estado de DGV de MCI \_ \_ \_ \_ minimizada
</dt> <dd>

El miembro **dwReturn** devuelve **true** si la ventana está minimizada.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>ventana de estado de DGV de MCI \_ \_ \_ \_ maximizada
</dt> <dd>

El miembro **dwReturn** devuelve **true** si la ventana está maximizada.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes
</dt> <dd>

El miembro **dwReturn** devuelve **true**.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpStatus* apunta a una estructura [**MCI \_ DGV \_ status \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **Sequencer** . Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .

<dl> <dt>

<span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI \_ Seq \_ status \_ DIVTYPE
</dt> <dd>

El miembro **dwReturn** se establece en uno de los siguientes valores que indican el tipo de división actual de una secuencia:

-   MCI \_ Seq \_ div \_ PPQN
-   MCI \_ Seq \_ div \_ SMPTE \_ 24
-   MCI \_ Seq \_ div \_ SMPTE \_ 25
-   MCI \_ Seq \_ div \_ SMPTE \_ 30
-   MCI \_ Seq \_ div \_ SMPTE \_ 30DROP

</dd> <dt>

<span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>\_maestro de \_ Estado de SEQ de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el tipo de sincronización que se usa para la operación maestra.

</dd> <dt>

<span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>\_desplazamiento de \_ Estado de SEQ de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el desplazamiento SMPTE actual de una secuencia.

</dd> <dt>

<span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>\_Puerto de \_ Estado de sec. \_
</dt> <dd>

El miembro **dwReturn** se establece en el identificador de dispositivo MIDI para el puerto actual utilizado por la secuencia.

</dd> <dt>

<span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI \_ Seq \_ status \_ esclavo
</dt> <dd>

El miembro **dwReturn** se establece en el tipo de sincronización que se usa para la operación subordinada.

</dd> <dt>

<span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>Temp. de \_ Estado de sec. \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en el tempo actual de una secuencia MIDI en pulsaciones por minuto para archivos PPQN o fotogramas por segundo para archivos SMPTE.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .

</dd> </dl>

Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** . Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>\_registro de \_ Estado de VCR \_ de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el modo de ensamblaje es on; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>\_monitor de \_ audio de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en una constante, que indica el tipo de monitor de audio seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>\_número de \_ monitor de audio de estado de VCR de \_ \_ MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el número del tipo de monitor de audio seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>\_registro de \_ audio de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el audio se grabará cuando se proporcione el siguiente comando de registro; en caso contrario, se establece en **false** . Si especifica MCI \_ Track en el parámetro *dwFlags* de este comando, **dwTrack** contiene el seguimiento al que se aplica esta consulta.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>\_origen de \_ audio de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en una constante, que indica el tipo de origen de audio actual.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>\_número de \_ origen de audio de estado de VCR de \_ \_ MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el número del tipo de origen de audio seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>\_reloj de \_ Estado de VCR MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el valor del reloj actual, en incrementos de reloj totales.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>\_identificador de \_ reloj de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en un número que describe de forma única el reloj en uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>\_formato de \_ contador de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en una constante que describe el formato del contador actual. Para obtener más información, consulte la \_ \_ \_ marca de formato de hora de set MCI del comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>\_resolución de \_ contador de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en una constante que describe la resolución del contador y es uno de los valores siguientes:

-   \_ \_ \_ Fotogramas res \_ de contador de VCR MCI: el contador tiene resolución de fotogramas.
-   \_Recuento \_ de contadores de VCR MCI \_ \_ segundos: el contador tiene una resolución de segundos.
-   \_Valor del \_ contador de estado de VCR \_ de MCI \_ : el miembro **dwReturn** se establece en la lectura del contador actual, en el formato de tiempo de contador actual.

</dd> <dt>

<span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>\_velocidad de \_ \_ fotogramas de estado VCR de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en la velocidad actual de fotogramas nativa del dispositivo.

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_Índice de \_ Estado de VCR de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en una constante, que describe el contenido actual de la presentación en pantalla, y es uno de los siguientes:

-   \_contador de \_ Índice de VCR de MCI \_
-   \_fecha de \_ Índice de VCR MCI \_
-   \_tiempo de \_ Índice de VCR MCI \_
-   \_código de \_ tiempo del índice de VCR MCI \_

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_ \_ \_ Índice \_ de estado del VCR de MCI en
</dt> <dd>

El miembro **dwReturn** se establece en **true** si la presentación en pantalla está activada; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>\_tipo de medio MCI VCR \_ status \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en uno de los siguientes:

-   Medios de vídeo de MCI \_ \_ \_ 8mm
-   \_Medios VCR de MCI \_ \_ Hi8
-   \_ \_ SHV multimedia de VCR de MCI \_
-   \_medios VCR de MCI \_ \_ SVHS
-   \_ \_ versión beta de medios VCR de MCI \_
-   \_medios VCR de MCI \_ \_ EDBETA
-   \_medios de VCR MCI \_ \_ otros

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_número de \_ Estado de VCR de MCI \_
</dt> <dd>

El miembro **dwNumber** se establece en el número de sintonizador lógico cuando se usa esta marca con la \_ marca MCI VCR \_ status \_ Tuner \_ Channel.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ \_ número \_ de estado del VCR de MCI de \_ pistas de audio \_
</dt> <dd>

El miembro **dwReturn** se establece en el número de pistas de audio que se pueden seleccionar de manera independiente.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ \_ número \_ de estado del VCR de MCI de \_ pistas de vídeo \_
</dt> <dd>

El miembro **dwReturn** se establece en el número de pistas de vídeo que pueden seleccionarse de forma independiente.

</dd> <dt>

<span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>\_tiempo de \_ espera de estado del VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en la duración máxima, en milisegundos, de un comando PAUSE. El valor devuelto de cero indica que no se producirá ningún tiempo de espera.

</dd> <dt>

<span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>\_formato de \_ reproducción de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en uno de los siguientes:

-   formato de VCR de MCI \_ \_ \_ EP
-   formato de VCR de MCI \_ \_ \_ LP
-   \_formato de VCR de MCI \_ \_
-   \_SP de \_ formato \_ VCR MCI

</dd> <dt>

<span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>\_duración de \_ PostRoll de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en la longitud de la cinta de vídeo que se reproducirá después del punto en el que se detuvo, en el formato de hora actual. Esto es necesario para frenar el transporte de cinta VCR desde un comando detener o pausar.

</dd> <dt>

<span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>\_ \_ \_ encendido \_ de estado de VCR de MCI
</dt> <dd>

El miembro **dwReturn** se establece en **true** si la alimentación está activada; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>\_duración del \_ prelanzamiento de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en la longitud de la cinta de vídeo que se reproducirá antes del punto en el que se inició, en el formato de hora actual. Esto es necesario para estabilizar la salida del VCR.

</dd> <dt>

<span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_formato de \_ registro de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en uno de los siguientes:

-   formato de VCR de MCI \_ \_ \_ EP
-   formato de VCR de MCI \_ \_ \_ LP
-   \_formato de VCR de MCI \_ \_
-   \_SP de \_ formato \_ VCR MCI

</dd> <dt>

<span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_velocidad de \_ Estado de VCR de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en la velocidad actual. Para obtener más información, consulte la \_ \_ \_ marca de velocidad del conjunto de VCR MCI del comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>\_modo de \_ tiempo de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en uno de los siguientes:

-   \_contador de \_ tiempo de VCR de MCI \_
-   \_detección de \_ tiempo de VCR MCI \_
-   \_código de \_ tiempo de vídeo de MCI \_

Para obtener más información, consulte la \_ \_ marca del \_ modo de tiempo Set VCR \_ de MCI del comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>\_tipo de \_ hora de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en una constante que describe el tipo de hora actual en uso (usado por [Play](play.md), [Record](record.md), [Seek](seek.md), etc.) y es uno de los siguientes:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_contador de \_ tiempo de VCR de MCI \_
</dt> <dd>

El contador está en uso.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_código de \_ tiempo de vídeo de MCI \_
</dt> <dd>

El código de tiempo está en uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>el \_ código de tiempo de estado del VCR de MCI \_ \_ \_ está presente
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el código de tiempo está presente en la posición actual del contenido. en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>\_registro de \_ código de \_ tiempo de estado VCR \_ de MCI
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el código de tiempo se registrará cuando se proporcione el siguiente comando de registro; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>\_tipo de \_ código de tiempo de estado de VCR de \_ MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en una constante, que describe el tipo de código de tiempo que el dispositivo admite directamente, y es uno de los siguientes:

-   \_ \_ Tipo de código de tiempo de VCR de MCI \_ \_ ninguno: este dispositivo no usa un código de tiempo.
-   Tipo de código de tiempo de VCR de MCI \_ \_ \_ \_ : este dispositivo usa un código de tiempo no especificado.
-   \_Tipo SMPTE de código de tiempo de VCR de MCI \_ \_ \_ : este dispositivo usa código de tiempo SMPTE.
-   Tipo de código de tiempo del VCR de MCI \_ \_ \_ \_ \_ Drop SMPTE: este dispositivo usa el código de tiempo Drop SMPTE.

</dd> <dt>

<span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>\_canal de \_ \_ sintonizador de estado de VCR de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el número de canal actual. Si especifica MCI \_ VCR \_ status \_ Number en el parámetro *dwFlags* de este comando, **dwNumber** contiene el número de sintonizador lógico al que se aplica este comando.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>\_monitor de \_ vídeo de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en una constante, que indica el tipo de monitor de vídeo seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_número de \_ monitor de vídeo de estado de VCR de \_ \_ MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el número del tipo de monitor de vídeo seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_grabación de \_ vídeo de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el vídeo se registrará cuando se proporcione el siguiente comando de registro; en caso contrario, se establece en **false** . Si especifica MCI \_ Track en el parámetro *dwFlags* de este comando, **dwTrack** contiene el seguimiento al que se aplica esta consulta.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>\_origen de \_ vídeo de estado de VCR de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en una constante que indica el tipo de origen de vídeo seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_número de \_ origen de vídeo de estado de VCR de \_ \_ MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el número del tipo de origen de vídeo seleccionado actualmente.

</dd> <dt>

<span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>Estado de VCR de MCI \_ \_ \_ \_ protegido contra escritura
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el medio está protegido contra escritura; en caso contrario, se establece en **false** .

</dd> </dl>

En el caso de los dispositivos VCR, el parámetro *lpStatus* apunta a una estructura [**MCI \_ VCR \_ status \_ parms**](mci-vcr-status-parms.md) .

El uso de \_ la \_ marca de longitud de estado de MCI para determinar la longitud de los medios siempre devuelve 2 horas para los dispositivos VCR, a menos que la longitud se haya cambiado explícitamente mediante el comando [MCI \_ set](mci-set.md) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** . Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .

<dl> <dt>

<span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>\_OVLY de \_ estado \_ hWnd de MCI
</dt> <dd>

El miembro **dwReturn** se establece en el identificador de la ventana asociada con el dispositivo de superposición de vídeo.

</dd> <dt>

<span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>\_Stretch OVLY de \_ estado \_ de MCI
</dt> <dd>

El miembro **dwReturn** se establece en **true** si está habilitada la expansión; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .

</dd> </dl>

Se usan las siguientes marcas adicionales con el tipo de dispositivo de **videodisco** . Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modo de estado de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el modo actual del dispositivo. Los dispositivos de videodisco pueden devolver la \_ constante de estacionamiento del modo MCI Vd \_ \_ , además de las constantes que puede devolver cualquier dispositivo, tal y como se documenta con el parámetro *dwFlags* .

</dd> <dt>

<span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>\_tamaño de \_ disco de estado \_ \_ de MCI Vd
</dt> <dd>

El miembro **dwReturn** se establece en el tamaño del disco cargado en pulgadas (8 o 12).

</dd> <dt>

<span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>Estado de MCI \_ Vd \_ \_ hacia delante
</dt> <dd>

El miembro **dwReturn** se establece en **true** si se está jugando hacia delante; en caso contrario, se establece en **false** .

El dispositivo de videodisco de MCI no es compatible con esta marca.

</dd> <dt>

<span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>\_tipo de \_ medio de estado \_ \_ de MCI Vd
</dt> <dd>

El miembro **dwReturn** se establece en el tipo de medio del medio insertado. Se pueden devolver los siguientes tipos de medios:

CAV de medios de MCI \_ Vd \_ \_

CLV de medios de MCI \_ Vd \_ \_

medios de MCI \_ Vd \_ \_ otros

</dd> <dt>

<span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>Estado de MCI \_ Vd \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en 1 o 2 para indicar el lado del disco que se va a cargar. No todos los dispositivos de videodisco admiten esta marca.

</dd> <dt>

<span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>velocidad de estado de MCI \_ Vd \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en la velocidad de reproducción en fotogramas por segundo. MCIPIONR. El controlador de dispositivo DRV devuelve la \_ función MCIERR no admitida \_ .

</dd> </dl>

Se usan las siguientes marcas adicionales con el tipo de dispositivo **WaveAudio** . Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .

<dl> <dt>

<span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>\_FORMATTAG de onda de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en la etiqueta de formato actual utilizada para reproducir, grabar y guardar.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el dispositivo de entrada de onda que se usa para la grabación. Si no hay ningún dispositivo en uso y no se ha establecido explícitamente ningún dispositivo, el error devuelto es MCIERR \_ Wave \_ INPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_salida de onda de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el dispositivo de salida de onda que se usa para la reproducción. Si no hay ningún dispositivo en uso y no se ha establecido explícitamente ningún dispositivo, el error devuelto es MCIERR \_ Wave \_ OUTPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>Estado de onda de MCI \_ \_ \_ AVGBYTESPERSEC
</dt> <dd>

El miembro **dwReturn** se establece en los bytes actuales por segundo utilizados para reproducir, grabar y guardar.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>Estado de onda de MCI \_ \_ \_ BitsPerSample
</dt> <dd>

El miembro **dwReturn** se establece en los bits actuales por muestra que se usan para reproducir, grabar y guardar datos con formato PCM.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>Estado de onda de MCI \_ \_ \_ BLOCKALIGN
</dt> <dd>

El miembro **dwReturn** se establece en la alineación de bloque actual utilizada para reproducir, grabar y guardar.

</dd> <dt>

<span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>\_canales de \_ Estado de onda de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el número de canales actual usado para reproducir, grabar y guardar.

</dd> <dt>

<span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>\_nivel de \_ Estado de onda de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el nivel de reproducción o registro actual de los datos con formato PCM. El valor se devuelve como un valor de 8 o 16 bits, dependiendo del tamaño de muestra utilizado. El nivel de canal derecho o mono se devuelve en la palabra de orden inferior. El nivel de canal izquierdo se devuelve en la palabra de orden superior.

</dd> <dt>

<span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>Estado de onda de MCI \_ \_ \_ SAMPLESPERSEC
</dt> <dd>

El miembro **dwReturn** se establece en las muestras actuales por segundo que se usan para reproducir, grabar y guardar.

</dd> </dl>

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
</dt> <dt>

[corte de MCI \_](mci-cut.md)
</dt> <dt>

[eliminación de MCI \_](mci-delete.md)
</dt> <dt>

[\_pegar MCI](mci-paste.md)
</dt> <dt>

[Reserva de MCI \_](mci-reserve.md)
</dt> <dt>

[MCI \_ set](mci-set.md)
</dt> <dt>

[reproducción](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[desean](seek.md)
</dt> </dl>

 


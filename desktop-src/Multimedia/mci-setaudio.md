---
title: MCI_SETAUDIO comando (Mmsystem.h)
description: El comando MCI \_ SETAUDIO establece valores asociados a la reproducción y captura de audio. Los dispositivos de vídeo digital y VCR reconocen este comando.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- MCI_SETAUDIO comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171589"
---
# <a name="mci_setaudio-command"></a>Comando \_ SETAUDIO de MCI

El comando MCI \_ SETAUDIO establece valores asociados a la reproducción y captura de audio. Los dispositivos de vídeo digital y VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
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

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las marcas siguientes se aplican al tipo **de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ SETAUDIO \_ ALG
</dt> <dd>

El **miembro lpstrAlgorithm** de la estructura identificada por *lpSetAudio* contiene una dirección de un búfer que contiene el nombre de un algoritmo de compresión de audio. Los siguientes comandos [MCI \_ RESERVE](mci-reserve.md) o [MCI \_ RECORD](mci-record.md) usan el algoritmo de compresión. Los algoritmos disponibles dependen del dispositivo. Si el algoritmo no es compatible con el formato de archivo actual, el formato de archivo se cambia al formato predeterminado para el algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ SETAUDIO \_ CLOCKTIME
</dt> <dd>

El tiempo especificado es en milisegundos y es el tiempo absoluto cuando se usa con MCI \_ DGV \_ SETAUDIO \_ OVER. (Esta vez no está en proceso con la reproducción del área de trabajo).

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>ENTRADA \_ SETAUDIO DE MCI DGV \_ \_
</dt> <dd>

Modifica la marca de volumen, triple o de sonido para que afecte a la señal de entrada y modifique lo que se registra. Si es posible, este es el valor predeterminado al supervisar la entrada.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>ELEMENTO SETAUDIO de MCI \_ DGV \_ \_
</dt> <dd>

Se especifica una constante de audio en el **miembro dwItem** de la estructura identificada *por lpSetAudio*. La constante identifica el valor que se va a establecer. Se definen las siguientes constantes:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ SETAUDIO \_ AVGBYTESPERSEC
</dt> <dd>

El número medio de bytes se especifica en el **miembro dwValue** de la estructura identificada por *lpSetAudio*. Este valor establece el número medio de bytes por segundo para reproducir o grabar en los formatos PCM (pulse Code Adaptive) y ADPCM (Adaptive Differential Pulse Code Adaptive). El archivo se guarda en este formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>SETAUDIOAUDIO DE MCI \_ DGV \_ \_
</dt> <dd>

El nivel de frecuencia baja de audio se especifica como un factor en el **miembro dwValue** de la estructura identificada *por lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ SETAUDIO \_ BITSPERSAMPLE
</dt> <dd>

El número de bits por muestra se especifica en el **miembro dwValue** de la estructura identificada *por lpSetAudio*. Este valor establece el número de bits por muestra reproducía o grababa en formato PCM. El archivo se guarda en este formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ SETAUDIO \_ BLOCKALIGN
</dt> <dd>

La alineación del bloque de datos se especifica en el **miembro dwValue** de la estructura identificada *por lpSetAudio*. Este valor establece la alineación de los bloques de datos con respecto al inicio de los datos de forma de onda de entrada.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ SETAUDIO \_ SAMPLESPERSEC
</dt> <dd>

La frecuencia de muestreo se especifica en el **miembro dwValue** de la estructura identificada *por lpSetAudio*. Este valor establece la frecuencia de muestreo para reproducir y grabar con los algoritmos PCM y ADPCM. El archivo se guarda en este formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>ORIGEN SETAUDIO de MCI \_ DGV \_ \_
</dt> <dd>

Una constante que especifica el origen de la entrada de audio se incluye en el **miembro dwValue** de la estructura identificada *por lpSetAudio*. Las siguientes constantes se definen para los orígenes de entrada de audio:

MEDIA DE \_ ORIGEN DE MCI DGV \_ SETAUDIO \_ \_

Promedio de los canales de audio izquierdo y derecho.

MCI \_ DGV \_ SETAUDIO \_ SOURCE \_ LEFT

Canal de audio izquierdo.

MCI \_ DGV \_ SETAUDIO \_ SOURCE \_ RIGHT

Canal de audio derecho.

ESTÉREO DE \_ ORIGEN DE MCI DGV \_ SETAUDIO \_ \_

Estéreo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>SECUENCIA SETAUDIO DE MCI \_ DGV \_ \_
</dt> <dd>

Se especifica una secuencia de audio en el **miembro dwValue** de la estructura identificada *por lpSetAudio*. El valor entero especifica la secuencia de audio que se reproduce desde el área de trabajo. Si no se especifica la secuencia, se reproduce la primera secuencia de audio intercalada físicamente.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ SETAUDIO \_ TREBLE
</dt> <dd>

El nivel de alta frecuencia de audio se especifica como un factor en el **miembro dwValue** de la estructura identificada *por lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>VOLUMEN SETAUDIO DE MCI \_ DGV \_ \_
</dt> <dd>

El nivel de audio de uno o ambos canales de audio se especifica como un factor en el **miembro dwValue** de la estructura identificada *por lpSetAudio*. Si los volúmenes izquierdo y derecho se han establecido en valores diferentes, la proporción del volumen de izquierda a derecha es aproximadamente inalterada.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ LEFT
</dt> <dd>

Habilita el canal de audio izquierdo cuando se usa con MCI \_ SET \_ ON. Deshabilita el canal de audio izquierdo cuando se usa con MCI \_ SET \_ OFF. Cuando esta marca se usa con la combinación de MCI \_ DGV SETAUDIO VALUE y \_ \_ MCI \_ DGV \_ SETAUDIO VOLUME, establece el volumen del \_ canal de audio izquierdo. Cuando esta marca se usa con MCI DGV SETAUDIO SOURCE, especifica el canal de audio izquierdo como origen del \_ \_ \_ digitalizador de entrada de audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ SETAUDIO \_ OVER
</dt> <dd>

Se incluye un parámetro de longitud de transición en el **miembro dwOver** de la estructura identificada *por lpSetAudio*. El valor de longitud especifica cuánto tiempo (en unidades del formato de hora actual) debe tardar en realizar un cambio que usa un factor. Si no se usa esta marca, los cambios se producen inmediatamente.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI \_ DGV \_ SETAUDIO \_ QUALITY
</dt> <dd>

El **miembro lpstrQuality** de la estructura identificada por *lpSetAudio contiene* una dirección de un búfer que define la calidad del audio. Una cadena de texto dentro del búfer especifica las características del algoritmo de compresión de audio.

La marca \_ MCI DGV SETAUDIO ALG se puede usar para seleccionar \_ un descriptor de calidad para el algoritmo \_ especificado. Si se omite esta marca, se usa el algoritmo actual.

Los algoritmos y los nombres de descriptor disponibles dependen del dispositivo. Cada dispositivo proporciona documentación para los algoritmos disponibles y una descripción de los nombres de descriptor aplicables. El [comando MCI \_ QUALITY](mci-quality.md) puede definir nombres de descriptor adicionales.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>REGISTRO SETAUDIO DE MCI \_ DGV \_ \_
</dt> <dd>

Especifica si la grabación incluye o excluye datos de audio. Cuando se combina con MCI \_ SET \_ ON, se graban los datos de audio. Cuando se combina con MCI \_ SET \_ OFF, se excluyen los datos de audio. El valor predeterminado incluye datos de audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT
</dt> <dd>

Habilita el canal de audio correcto cuando se usa con MCI \_ SET \_ ON. Deshabilita el canal de audio correcto cuando se usa con MCI \_ SET \_ OFF. Cuando esta marca se usa con la combinación de MCI \_ DGV SETAUDIO VALUE y \_ \_ MCI \_ DGV \_ SETAUDIO VOLUME, establece el volumen del \_ canal de audio derecho.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>VALOR SETAUDIO de MCI \_ DGV \_ \_
</dt> <dd>

Se especifica un valor en el miembro **dwValue** de la estructura identificada *por lpSetAudio*. La constante definida para la marca MCI DGV SETAUDIO ITEM especifica el significado \_ \_ del \_ valor.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Deshabilita el canal de audio especificado.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Habilita el canal de audio especificado.

</dd> <dt>

<span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>SALIDA \_ DE MCI SETAUDIO \_
</dt> <dd>

Modifica la marca de volumen, triple o de sonido para que solo modifique la señal reproducible y no lo que se registra. Si es posible, este es el valor predeterminado al supervisar la entrada.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpSetAudio* apunta a una estructura [**\_ MCI DGV \_ SETAUDIO \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>REGISTRO \_ SETAUDIO DE VCR DE MCI \_ \_
</dt> <dd>

Establece la grabación de audio en on o off, que se usa junto con una de las marcas siguientes:

MCI \_ SET \_ ON

Grabación de audio en.

MCI \_ SET \_ OFF

Grabación de audio desactivada. Es posible que sea necesario desactivar primero la grabación de ensamblado (mediante el comando [MCI \_ SET](mci-set.md) con la marca MCI VCR SET ASSEMBLE RECORD establecida en off) antes de que se pueda desactivar la grabación \_ \_ de \_ \_ audio.

MCI \_ TRACK

El **miembro dwTrack** de la estructura identificada por *lpSetAudio* especifica qué pista se ve afectada por el comando.

ORIGEN \_ DE MCI VCR \_ SETAUDIO \_

Establece el origen de audio. Esta marca debe usarse con la marca \_ MCI VCR \_ SETAUDIO \_ TO.

MONITOR \_ SETAUDIO DE VCR DE MCI \_ \_

Establece el monitor de origen de audio. Esta marca debe usarse con la marca \_ MCI VCR \_ SETAUDIO \_ TO.

MCI \_ VCR \_ SETAUDIO \_ EN

El **miembro dwTo** de la estructura identificada por *lpSetAudio* contiene una constante que describe el tipo de entrada o entrada supervisada. Debe ser uno de los siguientes:

<dl> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ TUNER

El tipo es el afinador.

</dd> <dd>

LÍNEA DE TIPO SRC DE MCI \_ VCR \_ \_ \_

El tipo es line.

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ AUX

El tipo es auxiliar.

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ GENERIC

El tipo es genérico.

</dd> <dd>

MCI \_ VCR \_ SRC \_ TYPE \_ MUTE

El tipo es mute. Esto solo se puede usar con la marca \_ MCI VCR \_ SETAUDIO \_ SOURCE.

</dd> <dd>

SALIDA DEL TIPO SRC de MCI \_ VCR \_ \_ \_

El tipo es la salida.

</dd> <dd>

MCI \_ VCR \_ SETAUDIO \_ NUMBER

El miembro dwNumber de la estructura identificada por lpSetAudio contiene la entrada de audio (del tipo especificado en el miembro dwTo) que se usará.

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

En el caso de los dispositivos VCR, el *parámetro lpSetAudio* apunta a una estructura [**\_ MCI VCR \_ SETAUDIO \_ PARMS.**](mci-vcr-setaudio-parms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 


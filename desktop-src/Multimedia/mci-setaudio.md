---
title: Comando MCI_SETAUDIO (mmsystem. h)
description: El \_ comando MCI SETAUDIO establece los valores asociados a la reproducción y la captura de audio. Los dispositivos digitales-vídeo y VCR reconocen este comando.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- Comando de MCI_SETAUDIO de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274542"
---
# <a name="mci_setaudio-command"></a>\_Comando MCI SETAUDIO

El \_ comando MCI SETAUDIO establece los valores asociados a la reproducción y la captura de audio. Los dispositivos digitales-vídeo y VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las marcas siguientes se aplican al tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>\_DGV MCI \_ SETAUDIO \_ alg
</dt> <dd>

El miembro **lpstrAlgorithm** de la estructura identificada por *lpSetAudio* contiene una dirección de un búfer que contiene el nombre de un algoritmo de compresión de audio. El algoritmo de compresión lo usan los comandos de [ \_ reserva de MCI](mci-reserve.md) o de [ \_ registro MCI](mci-record.md) posteriores. Los algoritmos disponibles dependen del dispositivo. Si el algoritmo es incompatible con el formato de archivo actual, el formato de archivo se cambia al formato predeterminado para el algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ SETAUDIO \_ CLOCKTIME
</dt> <dd>

La hora especificada se encuentra en milisegundos y es la hora absoluta cuando se usa con MCI \_ DGV \_ SETAUDIO \_ over. (Esta vez no está en el paso con la reproducción del área de trabajo).

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>\_ \_ entrada SETAUDIO de MCI DGV \_
</dt> <dd>

Modifica la marca de graves, agudos o de volumen para que afecte a la señal de entrada y modifique lo que se registra. Si es posible, es el valor predeterminado al supervisar la entrada.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>\_ \_ elemento SETAUDIO de DGV MCI \_
</dt> <dd>

Una constante de audio se especifica en el miembro **dwItem** de la estructura identificada por *lpSetAudio*. La constante identifica el valor que se establece. Se definen las constantes siguientes:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ SETAUDIO \_ AVGBYTESPERSEC
</dt> <dd>

El número promedio de bytes se especifica en el miembro **dwValue** de la estructura identificada por *lpSetAudio*. Este valor establece el número medio de bytes por segundo para reproducir o grabar en los formatos PCM (modulación por pulsos de código) y ADPCM (modulación de código de impulso diferencial adaptativo). El archivo se guarda en este formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>\_DGV MCI \_ SETAUDIO \_ Bass
</dt> <dd>

El nivel de baja frecuencia de audio se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ SETAUDIO \_ BitsPerSample
</dt> <dd>

El número de bits por muestra se especifica en el miembro **dwValue** de la estructura identificada por *lpSetAudio*. Este valor establece el número de bits por muestra reproducido o grabado en el formato PCM. El archivo se guarda en este formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ SETAUDIO \_ BLOCKALIGN
</dt> <dd>

La alineación del bloque de datos se especifica en el miembro **dwValue** de la estructura identificada por *lpSetAudio*. Este valor establece la alineación de los bloques de datos en relación con el inicio de los datos de la manera de onda de entrada.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ SETAUDIO \_ SAMPLESPERSEC
</dt> <dd>

La frecuencia de muestreo se especifica en el miembro **dwValue** de la estructura identificada por *lpSetAudio*. Este valor establece la velocidad de muestreo para reproducir y grabar con los algoritmos PCM y ADPCM. El archivo se guarda en este formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>origen de DGV de MCI \_ \_ SETAUDIO \_
</dt> <dd>

Una constante que especifica el origen de la entrada de audio se incluye en el miembro **dwValue** de la estructura identificada por *lpSetAudio*. Las siguientes constantes se definen para los orígenes de entrada de audio:

media de origen de DGV de MCI \_ \_ SETAUDIO \_ \_

Promedio de los canales de audio izquierdo y derecho.

\_DGV MCI \_ SETAUDIO \_ source \_ left

Canal de audio izquierdo.

MCI \_ DGV \_ SETAUDIO \_ source \_ right

Canal de audio derecho.

estéreo de origen de DGV de MCI \_ \_ SETAUDIO \_ \_

Casa.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>\_flujo de \_ SETAUDIO de DGV MCI \_
</dt> <dd>

Se especifica una secuencia de audio en el miembro **dwValue** de la estructura identificada por *lpSetAudio*. El valor entero especifica la secuencia de audio que se reproduce desde el área de trabajo. Si no se especifica la secuencia, se reproduce la primera secuencia de audio intercalada físicamente.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ SETAUDIO \_ agudos
</dt> <dd>

El nivel de alta frecuencia de audio se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>\_volumen de \_ SETAUDIO de DGV MCI \_
</dt> <dd>

El nivel de audio de uno o ambos canales de audio se especifica como factor en el miembro **dwValue** de la estructura identificada por *lpSetAudio*. Si los volúmenes izquierdo y derecho se han establecido en valores diferentes, la relación entre el volumen de izquierda a derecha es prácticamente inalterada.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_DGV MCI \_ SETAUDIO \_ izquierda
</dt> <dd>

Habilita el canal de audio izquierdo cuando se usa con MCI \_ establecido \_ en. Deshabilita el canal de audio izquierdo cuando se usa con MCI \_ establecido en \_ OFF. Cuando esta marca se usa con la combinación de MCI \_ DGV \_ SETAUDIO \_ value y MCI \_ DGV \_ SETAUDIO \_ Volume, establece el volumen del canal de audio izquierdo. Cuando esta marca se usa con el \_ origen MCI DGV \_ SETAUDIO \_ , especifica el canal de audio izquierdo como el origen del digitalizador de entrada de audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ SETAUDIO \_
</dt> <dd>

Un parámetro de longitud de transición se incluye en el miembro **dwOver** de la estructura identificada por *lpSetAudio*. El valor de longitud especifica cuánto tiempo (en unidades del formato de hora actual) debe tardar en realizar un cambio que use un factor. Si no se usa esta marca, los cambios se producen inmediatamente.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>calidad de SETAUDIO de MCI \_ DGV \_ \_
</dt> <dd>

El miembro **lpstrQuality** de la estructura identificada por *lpSetAudio* contiene una dirección de un búfer que define la calidad del audio. Una cadena de texto dentro del búfer especifica las características del algoritmo de compresión de audio.

La \_ marca MCI DGV \_ SETAUDIO \_ alg se puede usar para seleccionar un descriptor de calidad para el algoritmo especificado. Si se omite esta marca, se utiliza el algoritmo actual.

Los algoritmos y los nombres de descriptor disponibles dependen del dispositivo. Cada dispositivo proporciona documentación para los algoritmos disponibles y una descripción de los nombres de descriptor aplicables. El comando [MCI \_ Quality](mci-quality.md) puede definir nombres de descriptores adicionales.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>registro de DGV de MCI \_ \_ SETAUDIO \_
</dt> <dd>

Especifica si la grabación incluye o excluye datos de audio. Cuando se combina con MCI \_ establecido \_ en, se registran los datos de audio. Cuando se combina con MCI \_ establecido en \_ OFF, se excluyen los datos de audio. El valor predeterminado incluye datos de audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>\_DGV MCI \_ SETAUDIO \_ derecha
</dt> <dd>

Habilita el canal de audio adecuado cuando se usa con MCI \_ establecido \_ en. Deshabilita el canal de audio derecho cuando se usa con MCI \_ establecido en \_ OFF. Cuando esta marca se usa con la combinación de MCI \_ DGV \_ SETAUDIO \_ value y MCI \_ DGV \_ SETAUDIO \_ Volume, establece el volumen del canal de audio adecuado.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>\_ \_ valor SETAUDIO de MCI DGV \_
</dt> <dd>

Se especifica un valor en el miembro **dwValue** de la estructura identificada por *lpSetAudio*. El significado del valor se especifica mediante la constante definida para la marca MCI \_ DGV \_ SETAUDIO \_ Item.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_
</dt> <dd>

Deshabilita el canal de audio especificado.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_
</dt> <dd>

Habilita el canal de audio especificado.

</dd> <dt>

<span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>salida de MCI \_ SETAUDIO \_
</dt> <dd>

Modifica la marca de graves, agudos o de volumen para que solo modifique la señal de reproducción y no lo que se grabe. Si es posible, es el valor predeterminado al supervisar la entrada.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpSetAudio* apunta a una estructura [**MCI \_ DGV \_ SETAUDIO \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>\_registro de \_ SETAUDIO de VCR de MCI \_
</dt> <dd>

Establece la grabación de audio en activado o desactivado, que se usa junto con una de las marcas siguientes:

MCI \_ activado \_

Grabación de audio activada.

Desactivación de MCI \_ \_

Grabación de audio desactivada. Es posible que sea necesario desactivar primero la grabación de ensamblados (con el comando [MCI \_ set](mci-set.md) con la \_ marca de montaje del conjunto de VCR de MCI \_ \_ \_ establecida en OFF) antes de que se pueda desactivar la grabación de audio.

pista de MCI \_

El miembro **dwTrack** de la estructura identificada por *lpSetAudio* especifica qué pista se ve afectada por el comando.

\_origen de \_ SETAUDIO de VCR de MCI \_

Establece el origen de audio. Esta marca debe usarse con la SETAUDIO de VCR de MCI \_ \_ \_ para marcar.

\_monitor de \_ SETAUDIO de VCR de MCI \_

Establece el monitor de origen de audio. Esta marca debe usarse con la SETAUDIO de VCR de MCI \_ \_ \_ para marcar.

MCI \_ VCR \_ SETAUDIO \_

El miembro **dwTo** de la estructura identificada por *lpSetAudio* contiene una constante que describe el tipo de entrada o entrada supervisada. Debe ser uno de los siguientes:

<dl> <dd>

\_ \_ \_ sintonizador de tipo \_ src VCR de MCI

El tipo es sintonizador.

</dd> <dd>

\_línea de \_ \_ tipo src VCR de \_ MCI

El tipo es line.

</dd> <dd>

tipo de origen de VCR de MCI \_ \_ \_ \_ AUX

El tipo es auxiliar.

</dd> <dd>

tipo de origen de VCR de MCI \_ \_ \_ \_ genérico

El tipo es genérico.

</dd> <dd>

Desactivación de \_ \_ tipo src VCR \_ de MCI \_

El tipo es MUTE. Esto solo se puede usar con la \_ marca de \_ origen SETAUDIO VCR VCR \_ .

</dd> <dd>

\_salida de \_ tipo de origen de VCR de MCI \_ \_

El tipo es output.

</dd> <dd>

\_ \_ número SETAUDIO de VCR de MCI \_

El miembro dwNumber de la estructura identificada por lpSetAudio contiene la entrada de audio (del tipo especificado en el miembro dwTo) que se va a usar.

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

En el caso de los dispositivos VCR, el parámetro *lpSetAudio* apunta a una estructura [**MCI \_ VCR \_ SETAUDIO \_ parms**](mci-vcr-setaudio-parms.md) .

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

 


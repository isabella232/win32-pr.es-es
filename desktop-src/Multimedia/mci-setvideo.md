---
title: MCI_SETVIDEO comando (Mmsystem.h)
description: El comando MCI \_ SETVIDEO establece valores asociados a la reproducción de vídeo. Los dispositivos de vídeo digital y VCR reconocen este comando.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- MCI_SETVIDEO comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23206d169ad5e273927ead247c44194660c8d6b201c725e1b4d4ab24fd5e1544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803391"
---
# <a name="mci_setvideo-command"></a>Comando MCI \_ SETVIDEO

El comando MCI \_ SETVIDEO establece valores asociados a la reproducción de vídeo. Los dispositivos de vídeo digital y VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
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

**MCI \_ NOTIFY,** **MCI \_ WAIT** o **MCI \_ TEST**. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Las siguientes marcas adicionales se usan con el tipo de dispositivo "digitalvideo":

<dl> <dt>

<span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ SETVIDEO \_ ALG
</dt> <dd>

El **miembro lpstrAlgorithm** de la estructura identificada por *lpSetVideo* contiene una dirección de un búfer que contiene el nombre de un algoritmo de compresión de vídeo. Los siguientes comandos [MCI \_ RESERVE](mci-reserve.md) o [MCI \_ RECORD](mci-record.md) usan el algoritmo de compresión. Los algoritmos disponibles dependen del dispositivo.

Si el algoritmo especificado no es compatible con el formato de archivo actual, el formato de archivo se cambia al formato predeterminado para el algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ SETVIDEO \_ CLOCKTIME
</dt> <dd>

Cuando se usa **con MCI \_ DGV \_ SETVIDEO \_ OVER**, indica que la hora se especifica en milisegundos y es la hora absoluta. (Esta vez no está en juego con la reproducción del área de trabajo).

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>ENTRADA SETVIDEO DE MCI \_ DGV \_ \_
</dt> <dd>

Modifica **MCI \_ DGV \_ SETVIDEO \_ BRIGHTNESS,** **MCI \_ DGV \_ SETVIDEO \_ COLOR,** **MCI \_ DGV \_ SETVIDEO \_ CONTRAST,** **MCI \_ DGV \_ SETVIDEO \_ GAMMA,** **MCI \_ DGV \_ SETVIDEO \_ SHARPNESS** o **MCI \_ DGV \_ SETVIDEO \_ TINT** para que afecte a la señal de entrada y modifique lo que se registra. Si es posible, este es el valor predeterminado al supervisar la entrada.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>ELEMENTO SETVIDEO DE MCI \_ DGV \_ \_
</dt> <dd>

Se especifica una constante de vídeo en el **miembro dwItem** de la estructura identificada por *lpSetVideo*. La constante identifica el valor que se va a establecer. Puede especificar las siguientes constantes con esta marca:

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>PROCEDIMIENTO DE DIBUJO DE MCI \_ AVI \_ SETVIDEO \_ \_
</dt> <dd>

Se especifica una nueva dirección de procedimiento de dibujo en el **miembro dwValue** de la estructura identificada por *lpSetVideo*. Solo puede especificar un nuevo procedimiento de dibujo cuando el dispositivo está inactivo. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI. No hay ningún equivalente a esta marca en la interfaz de comandos de cadena.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI \_ AVI \_ SETVIDEO \_ PALETTE \_ COLOR
</dt> <dd>

Se especifica un nuevo color de paleta en los **miembros dwOver** y **dwValue** de la estructura identificada *por lpSetVideo*. El **miembro dwOver** especifica el índice de la paleta del color que se va a cambiar y el miembro **dwValue** especifica el nuevo color, como un valor RGB. También debe especificar las marcas **MCI \_ DGV \_ SETVIDEO \_ OVER** y **MCI \_ DGV \_ SETVIDEO \_ VALUE** con **MCI \_ DGV \_ SETVIDEO \_ ITEM** al usar esta constante. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI \_ AVI \_ SETVIDEO \_ PALETTE \_ HALFTONE
</dt> <dd>

Indica que se debe usar la paleta de medio tono, en lugar de la paleta predeterminada. Esta marca solo la reconoce el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ SETVIDEO \_ BITSPERPEL
</dt> <dd>

El número de bits por píxel se especifica en el **miembro dwValue** de la estructura identificada por *lpSetVideo*. El número de bits por píxel se usa para guardar los datos capturados o registrados.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI \_ DGV \_ SETVIDEO \_ BRIGHTNESS
</dt> <dd>

El nivel de brillo del vídeo se especifica como un factor en el **miembro dwValue** de la estructura identificada *por lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI \_ DGV \_ SETVIDEO \_ COLOR
</dt> <dd>

El nivel de saturación de color del vídeo se especifica como un factor en el **miembro dwValue** de la estructura identificada *por lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI \_ DGV \_ SETVIDEO \_ CONTRAST
</dt> <dd>

El nivel de contraste de vídeo se especifica como un factor en el **miembro dwValue** de la estructura identificada *por lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>VELOCIDAD DE \_ FOTOGRAMAS DE MCI DGV \_ SETVIDEO \_ \_
</dt> <dd>

Se especifica una velocidad de fotogramas en el **miembro dwValue** de la estructura identificada por *lpSetVideo*. La velocidad se especifica en unidades de fotogramas por segundo por 1000. Por ejemplo, 29,97 fotogramas por segundo se especifica como 29970.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI \_ DGV \_ SETVIDEO \_ GAMMA
</dt> <dd>

Se especifica un valor exponente de corrección gamma en el **miembro dwValue** de la estructura identificada *por lpSetVideo*. La corrección gamma ajusta la asignación entre la intensidad codificada en el origen de la presentación y el brillo mostrado. El valor es el exponente multiplicado por 1000. Por ejemplo, 2200 indica un exponente de 2,2. Un valor de 1000 indica un exponente de 1, que no aplica ninguna corrección gamma.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ COLOR
</dt> <dd>

Se especifica un color de clave en el **miembro dwValue** de la estructura identificada por *lpSetVideo*. El color de la clave es un valor RGB.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ INDEX
</dt> <dd>

Se especifica un valor de índice de clave en el **miembro dwValue** de la estructura identificada *por lpSetVideo*. El parámetro index es un índice de paleta física.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ SETVIDEO \_ PALHANDLE
</dt> <dd>

Se especifica un identificador de paleta en el **miembro dwValue** de la estructura identificada por *lpSetVideo*. El identificador de la paleta se encuentra en la palabra de orden bajo. Los dispositivos de vídeo digital no deben liberar la paleta pasada con este comando. Las aplicaciones deben liberarla después de cerrar el dispositivo. Esta marca solo es compatible con dispositivos que usan paletas. Si este identificador de paleta especificado es cero, se usa la paleta predeterminada.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI \_ DGV \_ SETVIDEO \_ SHARPNESS
</dt> <dd>

Un valor de nidez de vídeo se especifica como un factor en el **miembro dwValue** de la estructura identificada *por lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>ORIGEN DE \_ MCI DGV \_ SETVIDEO \_
</dt> <dd>

Se especifica una constante que especifica el origen de la entrada de vídeo en el **miembro dwValue** de la estructura identificada *por lpSetVideo*. Se definen las siguientes constantes:

-   **MCI \_ DGV \_ SETVIDEO \_ SRC \_ GV:** televisión de GV.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ PAL: TELEVISIÓN PAL.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB: vídeo RGB.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM: SECAM tv.
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO: S-Video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>SECUENCIA SETVIDEO DE MCI \_ DGV \_ \_
</dt> <dd>

Se especifica una secuencia de vídeo en el **miembro dwValue** de la estructura identificada *por lpSetVideo*. El valor entero especifica la secuencia de vídeo que se reproduce desde el área de trabajo. Si no se especifica la secuencia y el formato de archivo no define una secuencia predeterminada, se reproduce la primera secuencia de vídeo intercalada físicamente.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI \_ DGV \_ SETVIDEO \_ TINT
</dt> <dd>

Un valor de tono de vídeo se especifica como un factor en el **miembro dwValue** de la estructura identificada *por lpSetVideo*. Normalmente, este ajuste se modela después del control de tono de muchos conjuntos de televisión de color, con 250 definidos como verdes, 750 definidos como rojos y 0 (o 1000) definidos como azules. El valor nominal siempre es 500.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>SALIDA DE \_ MCI DGV \_ SETVIDEO \_
</dt> <dd>

La marca **MCI \_ DGV \_ SETVIDEO \_ BRIGHTNESS,** **MCI \_ DGV \_ SETVIDEO \_ COLOR,** **MCI \_ DGV \_ SETVIDEO \_ CONTRAST,** **MCI \_ DGV \_ SETVIDEO \_ GAMMA,** **MCI \_ DGV \_ SETVIDEO \_ SHARPNESS** o **MCI \_ DGV \_ SETVIDEO \_ TINT** se modifica para que afecte solo a la señal mostrada y no a lo que se registra. Si es posible, este es el valor predeterminado al supervisar un archivo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ SETVIDEO \_ OVER
</dt> <dd>

Se incluye un parámetro de longitud de transición en el **miembro dwOver** de la estructura identificada *por lpSetVideo*. La longitud de la transición especifica cuánto tiempo (en el formato de hora actual) debe tardar en realizar un cambio. Si no se usa esta marca, el cambio se produce inmediatamente.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI \_ DGV \_ SETVIDEO \_ QUALITY
</dt> <dd>

El **miembro lpstrQuality** de la estructura identificada por *lpSetVideo* contiene una dirección de un búfer que describe la calidad del vídeo. Una cadena de texto en el búfer especifica las características del algoritmo de compresión de vídeo.

La **marca \_ MCI DGV \_ SETVIDEO \_ ALG** se puede usar para seleccionar un descriptor de calidad para el algoritmo especificado. Si se omite esta marca, se usa el algoritmo actual.

Los algoritmos y los nombres de descriptor disponibles dependen del dispositivo. Cada dispositivo proporciona documentación para los algoritmos disponibles y una descripción de los nombres de descriptor aplicables. El [comando MCI \_ QUALITY](mci-quality.md) puede definir nombres de descriptor adicionales. Todos los dispositivos admiten los descriptores "low", "medium" y "high". El valor predeterminado es específico del controlador.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>REGISTRO SETVIDEO DE MCI \_ DGV \_ \_
</dt> <dd>

Especifica si la grabación incluye o excluye los datos de vídeo. Cuando se combina con **MCI \_ SET \_ ON,** se graban los datos de vídeo. Cuando se combina **con MCI \_ SET \_ OFF,** se excluyen los datos de vídeo. El valor predeterminado incluye datos de vídeo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI \_ DGV \_ SETVIDEO \_ SRC \_ NUMBER
</dt> <dd>

Se especifica un número para el origen de vídeo en el **miembro dwSourceNumber** de la estructura identificada *por lpSetVideo*. Si hay más de una entrada del tipo especificado por **MCI \_ DGV \_ SETVIDEO \_ VALUE,** el valor selecciona la entrada. Esta marca siempre debe usarse con **MCI \_ DGV \_ SETVIDEO \_ SOURCE**. Sin embargo, si se omite **\_ MCI DGV \_ SETVIDEO \_ VALUE,** el número de origen especificado indica el origen absoluto que se usará como se especifica en el [comando MCI \_ LIST.](mci-list.md)

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ DGV \_ SETVIDEO \_ STILL
</dt> <dd>

El nombre del algoritmo o el valor de calidad especificado se aplica a las imágenes fijas.

Cada controlador de dispositivo debe admitir un algoritmo de "none", lo que significa que no hay compresión. Este es el valor predeterminado. En este caso, los dispositivos de vídeo digital guardarán imágenes fijas como mapas de bits independientes del dispositivo RGB (DIB).

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>VALOR SETVIDEO DE MCI \_ DGV \_ \_
</dt> <dd>

Se incluye un valor en el **miembro dwValue** de la estructura identificada *por lpSetVideo*. El significado del valor se especifica mediante la marca **\_ MCI DGV \_ SETVIDEO \_ ITEM.**

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Deshabilita la salida de vídeo. En el caso de los dispositivos de vídeo digital, la deshabilitación de vídeo establece los píxeles del rectángulo de destino definidos por el comando PUT de [MCI \_ ](mci-put.md) (o su valor predeterminado, la región de cliente de la ventana actual) en un color sólido, pero no tiene ningún efecto en el búfer de fotogramas. Puede ocultar la ventana con el [comando VENTANA \_ de MCI](mci-window.md) si lo desea. Es posible que el origen del vídeo, ya sea el área de trabajo o una entrada externa, siga almacenando nuevas imágenes en el búfer de fotogramas, pero no se mostrarán hasta que el vídeo esté habilitado. Aunque las aplicaciones deben usar el comando MCI SETVIDEO para controlar esta función, los dispositivos de vídeo digital deben \_ seguir siendo compatibles con esta marca. El valor predeterminado después de una apertura está en on.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Habilita la salida de vídeo.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpSetVideo* apunta a una estructura [**\_ MCI DGV \_ SETVIDEO \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa)

Las siguientes marcas adicionales se usan con el tipo de dispositivo "vcr":

<dl> <dt>

<span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>REGISTRO DE \_ MCI VCR \_ SETVIDEO \_
</dt> <dd>

Establece la grabación de vídeo en on o off. Se usa junto con una de las marcas siguientes:

-   **MCI \_ ESTABLEZCA \_ EN**. Grabación de vídeo en.
-   **MCI \_ SET \_ OFF**. Grabación de vídeo desactivada. Es posible que sea necesario desactivar primero la grabación de ensamblado (mediante el comando [MCI \_ SET](mci-set.md) con la marca **\_ MCI VCR \_ SET ASSEMBLE \_ \_ RECORD** establecida en off) antes de que se pueda desactivar la grabación de vídeo.

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>MCI \_ TRACK
</dt> <dd>

El **miembro dwTrack** de la estructura identificada por *lpSetVideo* especifica qué pista se ve afectada por el comando.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>ORIGEN DE \_ MCI VCR \_ SETVIDEO \_
</dt> <dd>

Establece el origen del vídeo y debe usarse con la marca **\_ MCI VCR \_ SETVIDEO \_ TO.**

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MONITOR DE \_ MCI VCR \_ SETVIDEO \_
</dt> <dd>

Establece el monitor de origen de vídeo y debe usarse con la marca \_ MCI VCR \_ SETVIDEO \_ TO.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI \_ VCR \_ SETVIDEO \_ EN
</dt> <dd>

El **miembro dwTo** de la estructura identificada por *lpSetVideo* contiene una de las constantes siguientes:

<dl> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ TUNER**</dd> <dd>**LÍNEA DE TIPO SRC DE MCI \_ VCR \_ \_ \_**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ AUX**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ GENERIC**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ MUTE**</dd> <dd>**SALIDA DEL TIPO SRC de MCI \_ VCR \_ \_ \_**</dd> <dd>**MCI \_ VCR \_ SRC \_ TYPE \_ RGB**</dd> <dd>**MCI \_ VCR \_ SETVIDEO \_ NUMBER**</dd> </dl>

El **miembro dwNumber** de la estructura identificada por *lpSetVideo* contiene la entrada de vídeo (del tipo especificado en el **miembro dwTo)** que se usará.

</dd> </dl>

En el caso de los dispositivos *VCR, el parámetro lpSetVideo* apunta a una estructura [**\_ MCI VCR \_ SETVIDEO \_ PARMS.**](mci-vcr-setvideo-parms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 


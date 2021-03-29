---
title: Comando MCI_SETVIDEO (mmsystem. h)
description: El \_ comando MCI SETVIDEO establece los valores asociados a la reproducción de vídeo. Los dispositivos digitales-vídeo y VCR reconocen este comando.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- Comando de MCI_SETVIDEO de Windows multimedia
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
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490774"
---
# <a name="mci_setvideo-command"></a>\_Comando MCI SETVIDEO

El \_ comando MCI SETVIDEO establece los valores asociados a la reproducción de vídeo. Los dispositivos digitales-vídeo y VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

**MCI \_ NOTIFICAr**, **\_ espera de MCI** o **\_ prueba de MCI**. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Se usan las siguientes marcas adicionales con el tipo de dispositivo "DigitalVideo":

<dl> <dt>

<span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>\_DGV MCI \_ SETVIDEO \_ alg
</dt> <dd>

El miembro **lpstrAlgorithm** de la estructura identificada por *lpSetVideo* contiene una dirección de un búfer que contiene el nombre de un algoritmo de compresión de vídeo. El algoritmo de compresión lo usan los comandos de [ \_ reserva de MCI](mci-reserve.md) o de [ \_ registro MCI](mci-record.md) posteriores. Los algoritmos disponibles dependen del dispositivo.

Si el algoritmo especificado no es compatible con el formato de archivo actual, el formato del archivo se cambia al formato predeterminado para el algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ SETVIDEO \_ CLOCKTIME
</dt> <dd>

Cuando se usa con **MCI \_ DGV \_ SETVIDEO \_ over**, indica que el tiempo se especifica en milisegundos y es una hora absoluta. (Esta vez no está en el paso con la reproducción del área de trabajo).

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>\_ \_ entrada SETVIDEO de MCI DGV \_
</dt> <dd>

Modifica los **DGV de \_ MCI \_ SETVIDEO \_ Brightness**, MCI **\_ DGV \_ SETVIDEO \_ color**, **MCI \_ DGV \_ SETVIDEO \_ Contrast**, **MCI \_ DGV \_ SETVIDEO \_ gamma**, **MCI \_ DGV \_ SETVIDEO \_ nitidez** o **MCI \_ DGV \_ SETVIDEO \_ tinte** para que afecte a la señal de entrada y modifique lo que se registra. Si es posible, es el valor predeterminado al supervisar la entrada.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>\_ \_ elemento SETVIDEO de DGV MCI \_
</dt> <dd>

Una constante de vídeo se especifica en el miembro **dwItem** de la estructura identificada por *lpSetVideo*. La constante identifica el valor que se establece. Puede especificar las siguientes constantes con esta marca:

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>\_ \_ procedimiento SETVIDEO de \_ MCI \_ AVI
</dt> <dd>

Se especifica una nueva dirección de procedimiento de dibujo en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. Solo puede especificar un nuevo procedimiento de dibujo cuando el dispositivo está inactivo. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI. No hay ningún equivalente a esta marca en la interfaz de comandos de cadena.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>\_color de \_ la \_ paleta \_ SETVIDEO de MCI AVI
</dt> <dd>

Se especifica un nuevo color de la paleta en los miembros **dwOver** y **dwValue** de la estructura identificada por *lpSetVideo*. El miembro **dwOver** especifica el índice de la paleta del color que se va a cambiar y el miembro **dwValue** especifica el nuevo color, como un valor RGB. También debe especificar las marcas de valor **MCI \_ DGV \_ SETVIDEO \_ over** y **MCI \_ DGV \_ SETVIDEO \_** con **el \_ \_ \_ elemento MCI DGV SETVIDEO** al usar esta constante. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>\_semitono de \_ la \_ paleta \_ SETVIDEO de MCI AVI
</dt> <dd>

Indica que se debe usar la paleta de semitonos, en lugar de la paleta predeterminada. Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ SETVIDEO \_ BITSPERPEL
</dt> <dd>

El número de bits por píxel se especifica en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. El número de bits por píxel se usa para guardar los datos capturados o grabados.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>brillo de DGV de MCI \_ \_ SETVIDEO \_
</dt> <dd>

El nivel de brillo del vídeo se especifica como un factor en el miembro de **dwValue** de la estructura identificada por *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>\_color de \_ SETVIDEO de DGV MCI \_
</dt> <dd>

El nivel de saturación de color de vídeo se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>contraste de DGV de MCI \_ \_ SETVIDEO \_
</dt> <dd>

El nivel de contraste del vídeo se especifica como un factor en el miembro de **dwValue** de la estructura identificada por *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>\_velocidad de \_ \_ fotogramas de MCI DGV SETVIDEO \_
</dt> <dd>

Una velocidad de fotogramas se especifica en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. La tasa se especifica en unidades de fotogramas por segundo veces 1000. Por ejemplo, 29,97 fotogramas por segundo se especifica como 29970.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI \_ DGV \_ SETVIDEO \_ gamma
</dt> <dd>

Se especifica un valor de exponente de corrección gamma en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. La corrección gamma ajusta la asignación entre la intensidad codificada en el origen de presentación y el brillo mostrado. El valor es el exponente multiplicado por 1000. Por ejemplo, 2200 indica un exponente de 2,2. Un valor de 1000 indica un exponente de 1, que no se aplica ninguna corrección gamma.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>COLOR de clave de DGV de MCI \_ \_ SETVIDEO \_ \_
</dt> <dd>

Se especifica un color de clave en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. El color de la clave es un valor RGB.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>\_Índice de \_ clave de SETVIDEO de DGV MCI \_ \_
</dt> <dd>

Un valor de índice de clave se especifica en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. El parámetro de índice es un índice de paleta física.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ SETVIDEO \_ PALHANDLE
</dt> <dd>

Se especifica un identificador de paleta en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. El identificador de la paleta está contenido en la palabra de orden inferior. Los dispositivos de vídeo digital no deben liberar la paleta pasada con este comando. Las aplicaciones deben liberarla después de cerrar el dispositivo. Esta marca solo es compatible con dispositivos que usan paletas. Si el identificador de la paleta especificada es cero, se usa la paleta predeterminada.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>\_nitidez de \_ SETVIDEO de DGV MCI \_
</dt> <dd>

Un valor de nitidez de vídeo se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>origen de DGV de MCI \_ \_ SETVIDEO \_
</dt> <dd>

Una constante que especifica el origen de la entrada de vídeo se especifica en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. Se definen las constantes siguientes:

-   **MCI \_ DGV \_ SETVIDEO \_ src \_ NTSC**: televisión NTSC.
-   MCI \_ DGV \_ SETVIDEO \_ src \_ PAL: televisión PAL.
-   MCI \_ DGV \_ SETVIDEO \_ src \_ RGB: RGB video.
-   MCI \_ DGV \_ SETVIDEO \_ src \_ SECAM: el televisor SECAM.
-   MCI \_ DGV \_ SETVIDEO \_ src \_ Svideo: S-video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>\_flujo de \_ SETVIDEO de DGV MCI \_
</dt> <dd>

Se especifica una secuencia de vídeo en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. El valor entero especifica la secuencia de vídeo que se reproduce desde el área de trabajo. Si no se especifica la secuencia y el formato de archivo no define una secuencia predeterminada, se reproduce la primera secuencia de vídeo intercalada físicamente.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>\_matiz DGV \_ SETVIDEO de MCI \_
</dt> <dd>

Un valor de matiz de vídeo se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. Normalmente, este ajuste se modela después del control de matiz de muchos conjuntos de televisión de color, con 250 definido como verde, 750 definido como rojo y 0 (o 1000) definido como azul. El valor nominal siempre es 500.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>\_salida de DGV \_ SETVIDEO \_ de MCI
</dt> <dd>

La marca de **\_ \_ brillo DGV SETVIDEO \_ Brightness**, MCI **\_ DGV \_ SETVIDEO \_ color**, **MCI \_ DGV \_ SETVIDEO \_ Contrast**, **MCI \_ DGV \_ SETVIDEO \_ gamma**, **MCI \_ DGV \_ SETVIDEO \_ nitidez** o **MCI \_ DGV \_ SETVIDEO \_ tinte** se modifica para que solo afecte a la señal mostrada y no a lo que se registra. Si es posible, es el valor predeterminado al supervisar un archivo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ SETVIDEO \_
</dt> <dd>

Un parámetro de longitud de transición se incluye en el miembro **dwOver** de la estructura identificada por *lpSetVideo*. La longitud de la transición especifica cuánto tiempo (en el formato de hora actual) debe tardar en realizar un cambio. Si no se usa esta marca, el cambio se produce inmediatamente.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>calidad de SETVIDEO de MCI \_ DGV \_ \_
</dt> <dd>

El miembro **lpstrQuality** de la estructura identificada por *lpSetVideo* contiene una dirección de un búfer que describe la calidad del vídeo. Una cadena de texto en el búfer especifica las características del algoritmo de compresión de vídeo.

La marca **MCI \_ DGV \_ SETVIDEO \_ alg** se puede usar para seleccionar un descriptor de calidad para el algoritmo especificado. Si se omite esta marca, se utiliza el algoritmo actual.

Los algoritmos y los nombres de descriptor disponibles dependen del dispositivo. Cada dispositivo proporciona documentación para los algoritmos disponibles y una descripción de los nombres de descriptor aplicables. El comando [MCI \_ Quality](mci-quality.md) puede definir nombres de descriptores adicionales. Todos los dispositivos admiten los descriptores "Low", "Medium" y "High". El valor predeterminado es específico del controlador.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>registro de DGV de MCI \_ \_ SETVIDEO \_
</dt> <dd>

Especifica si la grabación incluye o excluye datos de vídeo. Cuando se combina con **MCI \_ establecido \_ en**, se registran los datos de vídeo. Cuando se combina con **MCI \_ set \_ OFF**, se excluyen los datos de vídeo. El valor predeterminado incluye datos de vídeo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI \_ DGV \_ SETVIDEO \_ \_ número src
</dt> <dd>

Se especifica un número para el origen de vídeo en el miembro **dwSourceNumber** de la estructura identificada por *lpSetVideo*. Si hay más de una entrada del tipo especificado por el **\_ \_ \_ valor SETVIDEO de MCI DGV**, el valor selecciona la entrada. Esta marca siempre debe usarse con **el \_ \_ \_ origen MCI DGV SETVIDEO**. Sin embargo, si se omite **MCI \_ DGV \_ SETVIDEO \_ Value** , el número de origen especificado indica el origen absoluto que se usará como se especifica en el comando [MCI \_ List](mci-list.md) .

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ DGV \_ SETVIDEO \_
</dt> <dd>

El nombre del algoritmo o el valor de calidad especificado se aplica a las imágenes fijas.

Cada controlador de dispositivo debe admitir un algoritmo de "ninguno", lo que significa que no hay compresión. Este es el valor predeterminado. En este caso, los dispositivos de vídeo digital guardan las imágenes seguidas como mapas de bits independientes del dispositivo RGB (DIB).

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>\_ \_ valor SETVIDEO de MCI DGV \_
</dt> <dd>

Un valor se incluye en el miembro **dwValue** de la estructura identificada por *lpSetVideo*. El significado del valor se especifica mediante la marca **de \_ \_ \_ elemento SETVIDEO DGV de MCI** .

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_
</dt> <dd>

Deshabilita la salida de vídeo. En el caso de los dispositivos de vídeo digital, al deshabilitar un vídeo, se establecen los píxeles del rectángulo de destino definido por el comando [MCI \_ Put](mci-put.md) (o su valor predeterminado, la región cliente de la ventana actual) en un color sólido, pero no tiene ningún efecto en el búfer de fotogramas. Si lo desea, puede ocultar la ventana con el comando de la [ \_ ventana MCI](mci-window.md) . El origen del vídeo, ya sea el área de trabajo o una entrada externa, puede continuar almacenando imágenes nuevas en el búfer de fotogramas, pero no se muestran hasta que se habilite el vídeo. Mientras que las aplicaciones deben usar el \_ comando MCI SETVIDEO para controlar esta función, los dispositivos de vídeo digital deben seguir admitiendo esta marca. El valor predeterminado después de un abierto es on.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_
</dt> <dd>

Habilita la salida de vídeo.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpSetVideo* apunta a una estructura [**MCI \_ DGV \_ SETVIDEO \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo "VCR":

<dl> <dt>

<span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>\_registro de \_ SETVIDEO de VCR de MCI \_
</dt> <dd>

Establece la grabación de vídeo en activado o desactivado. Se usa junto con una de las marcas siguientes:

-   **MCI \_ ESTABLEZCA \_ en**. Grabación de vídeo activada.
-   **MCI \_ ESTABLECER como \_ desactivado**. Grabación de vídeo desactivada. Es posible que sea necesario desactivar primero la grabación de ensamblados (con el comando [MCI \_ set](mci-set.md) con la marca de montaje del conjunto de VCR de MCI establecida en OFF) antes de que se pueda desactivar la grabación de vídeo. **\_ \_ \_ \_**

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>pista de MCI \_
</dt> <dd>

El miembro **dwTrack** de la estructura identificada por *lpSetVideo* especifica qué pista se ve afectada por el comando.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>\_origen de \_ SETVIDEO de VCR de MCI \_
</dt> <dd>

Establece el origen del vídeo y debe usarse con el **\_ VCR VCR \_ SETVIDEO \_ para** marcarlo.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>\_monitor de \_ SETVIDEO de VCR de MCI \_
</dt> <dd>

Establece el monitor de origen de vídeo y debe usarse con el \_ VCR VCR \_ SETVIDEO \_ para marcarlo.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI \_ VCR \_ SETVIDEO \_
</dt> <dd>

El miembro **dwTo** de la estructura identificada por *lpSetVideo* contiene una de las constantes siguientes:

<dl> <dd>**\_ \_ \_ sintonizador de tipo \_ src VCR de MCI**</dd> <dd>**\_línea de \_ \_ tipo src VCR de \_ MCI**</dd> <dd>**tipo de origen de VCR de MCI \_ \_ \_ \_ AUX**</dd> <dd>**tipo de origen de VCR de MCI \_ \_ \_ \_ genérico**</dd> <dd>**Desactivación de \_ \_ tipo src VCR \_ de MCI \_**</dd> <dd>**\_salida de \_ tipo de origen de VCR de MCI \_ \_**</dd> <dd>**tipo de origen de VCR de MCI \_ \_ \_ \_ RGB**</dd> <dd>**\_ \_ número SETVIDEO de VCR de MCI \_**</dd> </dl>

El miembro **dwNumber** de la estructura identificada por *lpSetVideo* contiene la entrada de vídeo (del tipo especificado en el miembro **dwTo** ) que se va a usar.

</dd> </dl>

En el caso de los dispositivos VCR, el parámetro *lpSetVideo* apunta a una estructura [**MCI \_ VCR \_ SETVIDEO \_ parms**](mci-vcr-setvideo-parms.md) .

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

 


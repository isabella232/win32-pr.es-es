---
title: MCI_GETDEVCAPS comando (Mmsystem.h)
description: El comando GETDEVCAPS de MCI \_ recupera información estática sobre un dispositivo.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- MCI_GETDEVCAPS comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7798f72405209f9834c3b67f84e57508c58ffc6153bce860b91f089005648905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803974"
---
# <a name="mci_getdevcaps-command"></a>Comando \_ GETDEVCAPS de MCI

El comando GETDEVCAPS de MCI \_ recupera información estática sobre un dispositivo. Todos los dispositivos reconocen este comando. Los parámetros y marcas disponibles para este comando dependen del dispositivo seleccionado. Se devuelve información en el **miembro dwReturn** de la estructura identificada *por lpCapsParms*.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
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

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*
</dt> <dd>

Puntero a una [**estructura \_ MCI GETDEVCAPS \_ PARMS.**](mci-getdevcaps-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Las siguientes marcas estándar y específicas de comandos adicionales se aplican a todos los dispositivos que admiten MCI \_ GETDEVCAPS:

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>DISPOSITIVO \_ COMPUESTO MCI GETDEVCAPS \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo usa el almacenamiento de datos que se debe abrir y cerrar explícitamente; de lo contrario, se establece **en FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>TIPO \_ DE DISPOSITIVO MCI GETDEVCAPS \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en uno de los valores enumerados en [Tipos de dispositivo de MCI.](mci-device-types.md)

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ TIENE \_ AUDIO
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo tiene salida de audio; de lo contrario, se establece **en FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ TIENE \_ VÍDEO
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo tiene salida de vídeo; de lo contrario, se establece **en FALSE.** Por ejemplo, el miembro se establece en **TRUE para** los dispositivos que admiten el conjunto de comandos videodisc.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>ELEMENTO \_ GETDEVCAPS DE MCI \_
</dt> <dd>

Especifica que el **miembro dwItem** de la estructura [**\_ MCI GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) contiene una de las siguientes constantes:

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS \_ PUEDE \_ EXPULSAR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede expulsar el medio; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ GETDEVCAPS \_ PUEDE \_ REPRODUCIR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede reproducir el medio; de lo contrario, se establece en **FALSE.** Si un dispositivo especifica **TRUE,** implica que el dispositivo admite los comandos [MCI \_ PAUSE](mci-pause.md) y [MCI \_ STOP,](mci-stop.md) así como el [comando MCI \_ PLAY.](mci-play.md)

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ GETDEVCAPS \_ PUEDE \_ GRABAR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo admite grabación; de lo contrario, se establece en **FALSE.** Si un dispositivo especifica **TRUE,** implica que el dispositivo admite los comandos MCI PAUSE y MCI STOP, así como \_ el comando \_ [MCI \_ RECORD.](mci-record.md)

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ PUEDE \_ GUARDAR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede guardar un archivo; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ USA \_ ARCHIVOS
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo requiere un nombre de archivo; de lo contrario, se establece **en FALSE.** Solo los dispositivos compuestos usan archivos.

</dd> </dl>

Las marcas siguientes se pueden especificar en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para el tipo **de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ SE PUEDE \_ INMOVILIZAR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede inmovilizar fotogramas; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUEDE \_ BLOQUEAR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede bloquearse; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUEDE \_ INVERTIR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede reproducirse a la inversa; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ CAN \_ STR \_ IN
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede ajustar la entrada; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUEDE \_ EXTENDER
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede ajustar una imagen; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ PUEDE \_ PROBAR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede realizar pruebas; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ TODAVÍA \_ TIENE
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede mostrar imágenes fijas; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

El **miembro dwReturn** se establece en el número máximo de ventanas que el dispositivo puede controlar simultáneamente.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>VELOCIDAD \_ MÁXIMA DE MCI DGV \_ GETDEVCAPS \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en la velocidad de reproducción máxima del dispositivo, en fotogramas por segundo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>VELOCIDAD \_ MÍNIMA DE MCI DGV \_ GETDEVCAPS \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en la velocidad de reproducción mínima del dispositivo, en fotogramas por segundo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>PALETAS \_ \_ GETDEVCAPS DE MCI DGV \_
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede devolver un identificador de paleta; de lo contrario, se establece en **FALSE.**

</dd> </dl>

Las marcas siguientes se pueden especificar en el **miembro dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para el tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>VELOCIDAD DE INCREMENTO \_ DEL RELOJ DE MCI GETDEVCAPS \_ \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el número de incrementos por segundo.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUEDE DETECTAR \_ \_ LONGITUD
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo es capaz de detectar la longitud del medio; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ GETDEVCAPS \_ SE PUEDE \_ INMOVILIZAR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo es capaz de inmovilizar la imagen de salida; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUEDE SUPERVISAR \_ ORÍGENES \_
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo es capaz de supervisar orígenes; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUEDE REALIZAR LA INSCRIPCIÓN \_ PREVIA
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo es capaz de realizar la inscripción previa; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUEDE OBTENER UNA VISTA \_ PREVIA
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo es capaz de obtener vistas previas; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUEDE \_ INVERTIR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo es capaz de reproducirse a la inversa; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI \_ VCR \_ GETDEVCAPS \_ PUEDE \_ PROBAR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo es capaz de realizar pruebas; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ VCR \_ GETDEVCAPS \_ TIENE \_ CLOCK
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo admite un reloj externo; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI \_ VCR \_ GETDEVCAPS \_ TIENE CÓDIGO DE \_ TIEMPO
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo tiene funcionalidad de código de tiempo o si se desconoce esta funcionalidad. de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>NÚMERO DE \_ MARCAS DE MCI VCR \_ \_ GETDEVCAPS \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en el número de marcas (99).

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI \_ VCR \_ GETDEVCAPS \_ SEEK \_ ACCURACY
</dt> <dd>

El **miembro dwReturn** se establece en la precisión de búsqueda del dispositivo.

</dd> </dl>

Las marcas siguientes se pueden especificar en el **miembro dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para el tipo **de dispositivo de** superposición:

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS \_ SE PUEDE \_ INMOVILIZAR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede inmovilizar la imagen; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ GETDEVCAPS \_ SE PUEDE \_ EXTENDER
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el dispositivo puede ajustar la imagen para rellenar el marco; de lo contrario, se establece en **FALSE.**

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

El **miembro dwReturn** se establece en el número máximo de ventanas que el dispositivo puede controlar simultáneamente.

</dd> </dl>

Las marcas siguientes se pueden especificar en el **miembro dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para el tipo de **dispositivo videodisc:**

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ PUEDE \_ INVERTIR
</dt> <dd>

El **miembro dwReturn** se establece en **TRUE** si el reproductor de videodisc puede reproducirse a la inversa. de lo contrario, se establece en **FALSE.** Algunos reproductores pueden reproducir discos CLV a la inversa, así como discos DE MOMENTO.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ GETDEVCAPSCAPAZ \_
</dt> <dd>

Cuando se combina con otros elementos, especifica que la información de devolución se aplica al formato CSV videodiscs. Este es el valor predeterminado si no se inserta videodisc.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ GETDEVCAPS \_ CLV
</dt> <dd>

Cuando se combina con otros elementos, especifica que la información de devolución se aplica a los vídeos en formato CLVdiscs.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ FAST \_ RATE
</dt> <dd>

El **miembro dwReturn** se establece en la velocidad de reproducción rápida estándar en fotogramas por segundo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>VELOCIDAD \_ NORMAL DE MCI VD \_ GETDEVCAPS \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en la velocidad de reproducción normal en fotogramas por segundo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>VELOCIDAD LENTA \_ DE MCI VD \_ GETDEVCAPS \_ \_
</dt> <dd>

El **miembro dwReturn** se establece en la velocidad de reproducción lenta estándar en fotogramas por segundo.

</dd> </dl>

Las marcas siguientes se pueden especificar en el **miembro dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para el tipo **de dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>ENTRADA \_ \_ GETDEVCAPS DE MCI WAVE \_
</dt> <dd>

El **miembro dwReturn** se establece en el número total de dispositivos de entrada de forma de onda (grabación).

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>SALIDA \_ \_ GETDEVCAPS DE MCI WAVE \_
</dt> <dd>

El **miembro dwReturn** se establece en el número total de dispositivos de salida de forma de onda (reproducción).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 


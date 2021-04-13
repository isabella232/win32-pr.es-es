---
title: Comando MCI_GETDEVCAPS (mmsystem. h)
description: El \_ comando MCI GETDEVCAPS recupera información estática sobre un dispositivo.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- Comando de MCI_GETDEVCAPS de Windows multimedia
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
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535428"
---
# <a name="mci_getdevcaps-command"></a>\_Comando MCI GETDEVCAPS

El \_ comando MCI GETDEVCAPS recupera información estática sobre un dispositivo. Todos los dispositivos reconocen este comando. Los parámetros y las marcas disponibles para este comando dependen del dispositivo seleccionado. La información se devuelve en el miembro **dwReturn** de la estructura identificada por *lpCapsParms*.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*
</dt> <dd>

Puntero a una [**estructura \_ GETDEVCAPS de \_ parms de MCI**](mci-getdevcaps-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas estándar y específicas del comando adicionales se aplican a todos los dispositivos que admiten MCI \_ GETDEVCAPS:

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_ \_ dispositivo compuesto MCI \_ GETDEVCAPS
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo usa almacenamiento de datos que se debe abrir y cerrar explícitamente; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_tipo de \_ dispositivo MCI GETDEVCAPS \_
</dt> <dd>

El miembro **dwReturn** se establece en uno de los valores enumerados en [tipos de dispositivo MCI](mci-device-types.md).

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ tiene \_ audio
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo tiene salida de audio; en caso contrario, se establece en **false** .

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ tiene \_ vídeo
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo tiene salida de vídeo. en caso contrario, se establece en **false** . Por ejemplo, el miembro se establece en **true** para los dispositivos que admiten el conjunto de comandos VideoDisc.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_elemento GETDEVCAPS de MCI \_
</dt> <dd>

Especifica que el miembro **dwItem** de la [**estructura \_ \_ parms de MCI GETDEVCAPS**](mci-getdevcaps-parms.md) contiene una de las constantes siguientes:

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS se \_ puede \_ expulsar
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede expulsar el medio; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>se \_ \_ puede \_ reproducir MCI GETDEVCAPS
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede reproducir el medio; de lo contrario, se establece en **false**. Si un dispositivo especifica **true**, significa que el dispositivo es compatible con los comandos [de \_ detención](mci-stop.md) de [ \_ MCI y](mci-pause.md) MCI, así como con el comando de [ \_ reproducción de MCI](mci-play.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>\_ \_ puede grabar GETDEVCAPS \_ de MCI
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo admite la grabación; de lo contrario, se establece en **false**. Si un dispositivo especifica **true**, significa que el dispositivo es compatible con los \_ comandos MCI PAUSE y MCI STOP, así \_ como con el comando [MCI \_ Record](mci-record.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ puede \_ Guardar
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede guardar un archivo; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ usa \_ archivos
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo requiere un nombre de archivo; en caso contrario, se establece en **false** . Solo los dispositivos compuestos usan archivos.

</dd> </dl>

Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS se \_ puede \_ inmovilizar
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede inmovilizar fotogramas; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ bloquear
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede bloquearse; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ invertir
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede reproducirse en orden inverso; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ Str \_
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede ajustar la entrada; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ ajustarse
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede ajustar una imagen; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ probar
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede realizar pruebas; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ \_ todavía
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede mostrar imágenes fijas; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ Max \_ Windows
</dt> <dd>

El miembro **dwReturn** se establece en el número máximo de ventanas que el dispositivo puede controlar simultáneamente.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>\_ \_ \_ velocidad máxima de DGV de MCI GETDEVCAPS \_
</dt> <dd>

El miembro **dwReturn** se establece en la velocidad máxima de reproducción del dispositivo, en fotogramas por segundo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>\_ \_ \_ tasa mínima de DGV de MCI GETDEVCAPS \_
</dt> <dd>

El miembro **dwReturn** se establece en la velocidad de reproducción mínima del dispositivo, en fotogramas por segundo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ paletas de GETDEVCAPS DGV MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede devolver un identificador de paleta; de lo contrario, se establece en **false**.

</dd> </dl>

Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>\_velocidad de \_ incremento de reloj de GETDEVCAPS de MCI \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en el número de incrementos por segundo.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ detectar \_ longitud
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de detectar la longitud del medio. de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ congelarse
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de inmovilizar la imagen de salida; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ supervisar \_ orígenes
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de supervisar los orígenes; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ prevertir
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de prehacer; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ obtener una vista previa
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de obtener vistas previas; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ invertir
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de reproducirse en orden inverso; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ probar
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de realizar pruebas; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ VCR \_ GETDEVCAPS \_ tiene \_ reloj
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo admite un reloj externo; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI \_ VCR \_ GETDEVCAPS \_ tiene \_ código de tiempo
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo tiene capacidad de código de tiempo o si esta funcionalidad es desconocida. de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_ \_ GETDEVCAPS de vídeo MCI \_ número \_ de \_ marcas
</dt> <dd>

El miembro **dwReturn** se establece en el número de marcas (99).

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>\_precisión de búsqueda de VCR VCR \_ GETDEVCAPS \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en la precisión de búsqueda del dispositivo.

</dd> </dl>

Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo **superpuesto** :

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS se \_ puede \_ inmovilizar
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede inmovilizar la imagen; de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ GETDEVCAPS \_ puede \_ ajustarse
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el dispositivo puede ajustar la imagen para rellenar el fotograma. de lo contrario, se establece en **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ Max \_ Windows
</dt> <dd>

El miembro **dwReturn** se establece en el número máximo de ventanas que el dispositivo puede controlar simultáneamente.

</dd> </dl>

Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo de **videodisco** :

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ Vd \_ GETDEVCAPS \_ puede \_ invertir
</dt> <dd>

El miembro **dwReturn** se establece en **true** si el reproductor de CD puede reproducirse en orden inverso; de lo contrario, se establece en **false**. Algunos jugadores pueden reproducir discos CLV en discos inversos y CAV.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ Vd \_ GETDEVCAPS \_ CAV
</dt> <dd>

Cuando se combina con otros elementos, especifica que la información de devolución se aplica al formato de CAV de videodisco. Este es el valor predeterminado si no se inserta ningún CD.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ Vd \_ GETDEVCAPS \_ CLV
</dt> <dd>

Cuando se combina con otros elementos, especifica que la información de devolución se aplica al formato de CLV de videodisco.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_ \_ \_ tasa rápida de GETDEVCAPS \_ de MCI Vd
</dt> <dd>

El miembro **dwReturn** se establece en la velocidad de reproducción rápida estándar en fotogramas por segundo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>tasa normal de MCI \_ Vd \_ GETDEVCAPS \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en la velocidad de reproducción normal en fotogramas por segundo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>velocidad lenta de MCI \_ Vd \_ GETDEVCAPS \_ \_
</dt> <dd>

El miembro **dwReturn** se establece en la velocidad de reproducción lenta estándar en fotogramas por segundo.

</dd> </dl>

Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_ \_ entrada GETDEVCAPS de onda de MCI \_
</dt> <dd>

El miembro **dwReturn** se establece en el número total de dispositivos de entrada de onda (grabación).

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>salida de MCI \_ Wave \_ GETDEVCAPS \_
</dt> <dd>

El miembro **dwReturn** se establece en el número total de dispositivos de salida de forma de onda (reproducción).

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
</dt> </dl>

 


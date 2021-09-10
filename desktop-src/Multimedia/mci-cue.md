---
title: MCI_CUE comando (Mmsystem.h)
description: El comando MCI \_ CUE muestra un dispositivo para que la reproducción o grabación comience con un retraso mínimo. Los dispositivos de audio y vídeo digital, VCR y forma de onda reconocen este comando.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- MCI_CUE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369961"
---
# <a name="mci_cue-command"></a>Comando MCI \_ CUE

El comando MCI \_ CUE muestra un dispositivo para que la reproducción o grabación comience con un retraso mínimo. Los dispositivos de audio y vídeo digital, VCR y forma de onda reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
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

<span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>ENTRADA DE \_ INDICACIÓN DE MCI DGV \_ \_
</dt> <dd>

Una instancia de vídeo digital debe prepararse para la grabación. Si la aplicación no tiene espacio en disco reservado, el dispositivo reserva el espacio en disco mediante sus parámetros predeterminados. La aplicación puede omitir esta marca si el origen de presentación actual ya es la entrada externa. (Esta marca no tiene ningún efecto en la selección del origen de la presentación).

</dd> <dt>

<span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI \_ DGV \_ CUE \_ NOSHOW
</dt> <dd>

Una instancia de vídeo digital debe prepararse para reproducir el fotograma especificado con el comando sin mostrarlo. Cuando se especifica esta marca, la pantalla sigue mostrando la imagen en el búfer de fotogramas aunque su marco correspondiente no sea la posición actual. Por ejemplo, si el búfer de fotogramas contiene la imagen del fotograma 7, el dispositivo sigue mostrando el fotograma 7 cuando se usa esta marca para marcar el dispositivo en cualquier otra posición. Un comando cue posterior sin esta marca y sin la marca MCI \_ TO muestra el marco actual.

</dd> <dt>

<span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>SALIDA DE \_ LA INDICACIÓN de MCI DGV \_ \_
</dt> <dd>

Una instancia de vídeo digital debe prepararse para la reproducción. Si el área de trabajo está en pausa, no se produce ningún posicionamiento. Si se detiene el área de trabajo, la posición podría cambiar a una imagen de fotograma clave anterior. La aplicación puede omitir esta marca si el origen de presentación actual ya es el área de trabajo.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Se incluye una posición de área de trabajo en el **miembro dwTo** de la estructura identificada *por lpCue*. Las unidades asignadas a los valores de posición se especifican mediante la marca MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md) Esto equivale a buscar una posición, salvo que el dispositivo se pausa después del comando.

</dd> </dl>

En el caso de los dispositivos **digitalvideo,** *el parámetro lpCue* apunta a una estructura [**MCI \_ DGV CUE \_ \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

El **miembro dwFrom** de la estructura a la que *apunta lpCue* contiene la ubicación inicial especificada en el formato de hora actual.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

El **miembro dwTo** de la estructura a la que *apunta lpCue* contiene la ubicación final (pausa) especificada en el formato de hora actual.

</dd> <dt>

<span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>ENTRADA DE \_ INDICACIÓN DE VCR \_ DE MCI \_
</dt> <dd>

Prepárese para la grabación.

</dd> <dt>

<span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>SALIDA DE \_ LA INDICACIÓN DE VCR \_ de MCI \_
</dt> <dd>

Prepárese para la reproducción. Si no se especifica \_ MCI VCR \_ CUE INPUT ni MCI VCR CUE OUTPUT, se supone que \_ \_ \_ \_ MCI \_ VCR CUE \_ \_ OUTPUT.

</dd> <dt>

<span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>INSCRIPCIÓN PREVIA \_ DE LA INDICACIÓN DE VCR \_ \_ DE MCI
</dt> <dd>

Apunte el dispositivo a la posición actual o **a la posición dwFrom,** menos la duración de la inscripción previa. Esto permitirá que el dispositivo se prepare antes de entrar en el modo de grabación o reproducción.

</dd> <dt>

<span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>INVERTIDA \_ DE LA INDICACIÓN DE VCR \_ de MCI \_
</dt> <dd>

La dirección del siguiente comando de reproducción o registro es inversa.

</dd> </dl>

Al realizar indicaciones para la reproducción mediante el comando MCI CUE con la marca MCI VCR CUE OUTPUT, puede cancelar la indicación de MCI mediante la emisión del comando MCI PLAY con \_ \_ \_ \_ \_ MCI FROM, MCI TO o [ \_ ](mci-play.md) \_ \_ MCI \_ VCR \_ PLAY \_ REVERSE.

Al realizar indicaciones para la grabación mediante MCI CUE con la marca MCI VCR CUE INPUT, puede cancelar la indicación de MCI mediante la emisión del comando MCI RECORD con \_ \_ \_ \_ \_ [MCI \_ ](mci-record.md) \_ FROM, MCI TO o \_ MCI \_ VCR RECORD \_ \_ INITIALIZE.

En **el caso de los dispositivos vcr,** el parámetro *lpCue* apunta a una estructura [**MCI \_ VCR CUE \_ \_ PARMS.**](mci-vcr-cue-parms.md)

Las siguientes marcas adicionales se usan con el **tipo de dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>ENTRADA DE \_ MCI WAVE \_
</dt> <dd>

Un dispositivo de entrada de audio de forma de onda debe ser cued.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>SALIDA DE MCI \_ \_ WAVE
</dt> <dd>

Un dispositivo de salida de audio de forma de onda debe ser cued. Esta es la marca predeterminada si no se especifica una marca.

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
</dt> </dl>

 


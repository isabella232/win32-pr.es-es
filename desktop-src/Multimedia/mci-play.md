---
title: MCI_PLAY comando (Mmsystem.h)
description: El comando MCI PLAY indica al dispositivo que \_ empiece a transmitir los datos de salida. Los dispositivos cd audio, digital-video, secuenciador MIDI, videodisc, VCR y audio de onda reconocen este comando.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- MCI_PLAY comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369956"
---
# <a name="mci_play-command"></a>Comando MCI \_ PLAY

El comando MCI PLAY indica al dispositivo que \_ empiece a transmitir los datos de salida. Los dispositivos cd audio, digital-video, secuenciador MIDI, videodisc, VCR y audio de onda reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
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

<span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*
</dt> <dd>

Puntero a una [**estructura \_ MCI PLAY \_ PARMS.**](mci-play-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ PLAY:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Se incluye una ubicación inicial en el **miembro dwFrom** de la estructura identificada por *lpPlay*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md) Si no se especifica MCI FROM, la ubicación inicial tiene como valor predeterminado \_ la posición actual.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Se incluye una ubicación final en el **miembro dwTo** de la estructura identificada por *lpPlay*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT de \_ \_ MCI \_ SET. Si no se especifica MCI TO, la ubicación final tiene como valor predeterminado \_ el final del medio.

</dd> </dl>

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI \_ DGV \_ PLAY \_ REPEAT
</dt> <dd>

La reproducción debe iniciarse de nuevo al principio cuando se alcanza el final del contenido.

</dd> <dt>

<span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI \_ DGV \_ PLAY \_ REVERSE
</dt> <dd>

La reproducción debe producirse a la inversa.

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>VENTANA DE \_ REPRODUCCIÓN DE MCI MCIAVI \_ \_
</dt> <dd>

La reproducción debe producirse en la ventana asociada a una instancia de dispositivo (valor predeterminado). (Esta marca es específica de MCIAVI. DRV).

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>PANTALLA COMPLETA \_ DE MCI MCIAVI \_ PLAY \_
</dt> <dd>

La reproducción debe usar una pantalla completa. Use esta marca solo al reproducir archivos comprimidos o de 8 bits.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpPlay* apunta a una estructura [**MCI \_ DGV \_ PLAY \_ PARMS.**](/previous-versions//dd743396(v=vs.85))

Las siguientes marcas adicionales se usan con el tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI \_ VCR \_ PLAY \_ AT
</dt> <dd>

El **miembro dwAt** de la estructura identificada por *lpPlay* contiene una hora en la que comienza todo el comando, o si el dispositivo es cued, cuando el dispositivo alcanza la posición desde dada por el comando [MCI \_ CUE.](mci-cue.md)

</dd> <dt>

<span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI \_ VCR \_ PLAY \_ REVERSE
</dt> <dd>

La reproducción debe producirse a la inversa.

</dd> <dt>

<span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI \_ VCR \_ PLAY \_ SCAN
</dt> <dd>

La reproducción debe ser lo más rápida posible mientras se mantiene la salida del vídeo.

</dd> </dl>

En el caso de los dispositivos *VCR, lpPlay* apunta a una [**estructura \_ MCI VCR \_ PLAY \_ PARMS.**](mci-vcr-play-parms.md)

Las marcas adicionales siguientes se usan con el **tipo de dispositivo videodisc:**

<dl> <dt>

<span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI \_ VD \_ PLAY \_ FAST
</dt> <dd>

Reproducir rápidamente.

</dd> <dt>

<span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI \_ VD \_ PLAY \_ REVERSE
</dt> <dd>

Reproducir en orden inverso.

</dd> <dt>

<span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI \_ VD \_ PLAY \_ SCAN
</dt> <dd>

Examinar rápidamente.

</dd> <dt>

<span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI \_ VD \_ PLAY \_ SLOW
</dt> <dd>

Reproducir lentamente.

</dd> <dt>

<span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>VELOCIDAD DE \_ REPRODUCCIÓN VD \_ DE MCI \_
</dt> <dd>

La velocidad de reproducción se incluye en el **miembro dwSpeed** en la estructura identificada por *lpPlay*.

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

 


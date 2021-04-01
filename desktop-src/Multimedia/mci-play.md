---
title: Comando MCI_PLAY (mmsystem. h)
description: El \_ comando MCI Play indica al dispositivo que empiece a transmitir los datos de salida. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- Comando de MCI_PLAY de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905660"
---
# <a name="mci_play-command"></a>Comando de reproducción de MCI \_

El \_ comando MCI Play indica al dispositivo que empiece a transmitir los datos de salida. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*
</dt> <dd>

Puntero a una estructura de [**\_ \_ parms de reproducción de MCI**](mci-play-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ Play:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde
</dt> <dd>

Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpPlay*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) . Si \_ no se especifica MCI desde, la ubicación inicial toma como valor predeterminado la posición actual.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpPlay*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de MCI \_ set. Si \_ no se especifica MCI en, el valor predeterminado de la ubicación final es el final del medio.

</dd> </dl>

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>\_reproducción de DGV de MCI \_ \_
</dt> <dd>

La reproducción debe comenzar de nuevo al principio cuando se alcanza el final del contenido.

</dd> <dt>

<span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI \_ DGV \_ Play \_ Reverse
</dt> <dd>

La reproducción debe realizarse en orden inverso.

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>ventana de reproducción de MCI \_ MCIAVI \_ \_
</dt> <dd>

La reproducción debe realizarse en la ventana asociada a una instancia de dispositivo (valor predeterminado). (Esta marca es específica de MCIAVI. DRV).

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI \_ MCIAVI \_ Play \_ Fullscreen
</dt> <dd>

La reproducción debe usar una presentación en pantalla completa. Use esta marca solo cuando se reproduzcan archivos comprimidos u de 8 bits.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpPlay* apunta a una estructura [**MCI \_ DGV \_ Play \_ parms**](/previous-versions//dd743396(v=vs.85)) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>\_ \_ reproducción de VCR \_ de MCI en
</dt> <dd>

El miembro **dwAt** de la estructura identificada por *lpPlay* contiene la hora a la que comienza el comando completo, o bien, si el dispositivo está preparado, cuando el dispositivo llega a la posición a partir del comando [MCI \_ CUE](mci-cue.md) .

</dd> <dt>

<span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>reproducción de VCR de MCI \_ \_ \_ inverso
</dt> <dd>

La reproducción debe realizarse en orden inverso.

</dd> <dt>

<span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>\_recorrido de \_ reproducción de VCR de MCI \_
</dt> <dd>

La reproducción debe ser lo más rápida posible mientras se mantiene la salida de vídeo.

</dd> </dl>

En el caso de los dispositivos VCR, *lpPlay* apunta a una estructura [**MCI \_ VCR \_ Play \_ parms**](mci-vcr-play-parms.md) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo de **videodisco** :

<dl> <dt>

<span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI \_ Vd \_ Play \_ Fast
</dt> <dd>

Reproducción rápida.

</dd> <dt>

<span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI \_ Vd \_ Play \_ Reverse
</dt> <dd>

Reproducir en orden inverso.

</dd> <dt>

<span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>examen de reproducción de MCI \_ Vd \_ \_
</dt> <dd>

Digitalice rápidamente.

</dd> <dt>

<span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI \_ Vd \_ play reproducción \_ lenta
</dt> <dd>

Reproducir lentamente.

</dd> <dt>

<span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>velocidad de reproducción de MCI \_ Vd \_ \_
</dt> <dd>

La velocidad de reproducción se incluye en el miembro **dwSpeed** de la estructura identificada por *lpPlay*.

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

 


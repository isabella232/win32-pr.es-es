---
title: Comando MCI_STOP (mmsystem. h)
description: El comando de detención de MCI \_ detiene todas las secuencias de reproducción y grabación, descarga todos los búferes de reproducción y deja de mostrar las imágenes de vídeo. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- Comando de MCI_STOP de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422368"
---
# <a name="mci_stop-command"></a>Comando de detención de MCI \_

El comando de detención de MCI \_ detiene todas las secuencias de reproducción y grabación, descarga todos los búferes de reproducción y deja de mostrar las imágenes de vídeo. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
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

<span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La diferencia entre los \_ comandos MCI STOP y [MCI \_ PAUSE](mci-pause.md) depende del dispositivo. Si es posible, \_ la pausa de MCI suspende el funcionamiento del dispositivo pero deja el dispositivo listo para reanudar la reproducción inmediatamente.

En el caso del dispositivo de audio de CD, MCI \_ Stop restablece la posición de pista actual a cero; por el contrario, la [ \_ pausa de MCI](mci-pause.md) mantiene la posición de pista actual, lo que prevé que el dispositivo se reanudará la reproducción.

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

 


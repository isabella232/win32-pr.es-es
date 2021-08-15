---
title: MCI_STOP comando (Mmsystem.h)
description: El comando MCI STOP detiene todas las secuencias de reproducción y grabación, descarga todos los búferes de reproducción y deja de \_ mostrar imágenes de vídeo. Los dispositivos cd audio, digital-video, secuenciador MIDI, videodisc, VCR y audio de onda reconocen este comando.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- MCI_STOP comando Windows Multimedia
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
ms.openlocfilehash: e02830dde544e025447cb72df6ff3720857985384ff6bd074c5e0718b114697c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374607"
---
# <a name="mci_stop-command"></a>Comando MCI \_ STOP

El comando MCI STOP detiene todas las secuencias de reproducción y grabación, descarga todos los búferes de reproducción y deja de \_ mostrar imágenes de vídeo. Los dispositivos cd audio, digital-video, secuenciador MIDI, videodisc, VCR y audio de onda reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, para dispositivos de vídeo digital y VCR, MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

La diferencia entre los comandos MCI STOP y \_ [MCI \_ PAUSE](mci-pause.md) depende del dispositivo. Si es posible, MCI PAUSE suspende la operación del dispositivo, pero deja el \_ dispositivo listo para reanudar la reproducción inmediatamente.

En el caso del dispositivo de audio de CD, MCI STOP restablece la posición actual de la pista en cero; en \_ cambio, [MCI \_ PAUSE](mci-pause.md) mantiene la posición actual de la pista, lo que anticipa que el dispositivo reanudará la reproducción.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 


---
title: Comando MCI_COPY (mmsystem. h)
description: El comando de copia de MCI \_ copia los datos en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- Comando de MCI_COPY de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996452"
---
# <a name="mci_copy-command"></a>Comando de copia de MCI \_

El comando de copia de MCI \_ copia los datos en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
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

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*
</dt> <dd>

Puntero a una estructura [**MCI \_ DGV \_ Copy \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_ \_ copia de DGV \_ de MCI en
</dt> <dd>

Se incluye un rectángulo en el miembro **RC** de la estructura identificada por *lpCopy*. El rectángulo especifica la parte de cada fotograma que se va a copiar. Si se omite la marca, \_ la copia de MCI copia todo el marco.

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>\_secuencia de \_ audio de copia DGV \_ de MCI \_
</dt> <dd>

Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpCopy*. Si usa esta marca y también quiere copiar vídeo, también debe usar la \_ marca MCI DGV \_ Copy \_ vídeo \_ Stream. (Si no se especifica ninguna marca, se copian los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_secuencia de \_ vídeo de copiar DGV \_ de MCI \_
</dt> <dd>

Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpCopy*. Si usa esta marca y también quiere copiar audio, también debe usar la \_ marca MCI DGV \_ Copy \_ audio \_ Stream. (Si no se especifica ninguna marca, se copian los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde
</dt> <dd>

Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpCopy*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpCopy*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del \_ comando MCI set.

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

 


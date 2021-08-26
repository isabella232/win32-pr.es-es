---
title: MCI_COPY comando (Mmsystem.h)
description: El comando COPY de MCI \_ copia los datos en el Portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- MCI_COPY comando Windows Multimedia
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
ms.openlocfilehash: 590acf61b352fa9abab00dfd49f3f54b166bfc340eaf12061e3d90b7a3025d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039295"
---
# <a name="mci_copy-command"></a>Comando COPY de MCI \_

El comando COPY de MCI \_ copia los datos en el Portapapeles. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*
</dt> <dd>

Puntero a una [**estructura MCI \_ DGV \_ COPY \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>COPIA \_ DE MCI DGV \_ \_ EN
</dt> <dd>

Se incluye un rectángulo en el **miembro rc** de la estructura identificada por *lpCopy*. El rectángulo especifica la parte de cada marco que se copiará. Si se omite la marca, MCI \_ COPY copia todo el marco.

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>SECUENCIA DE \_ AUDIO DE COPIA DE MCI DGV \_ \_ \_
</dt> <dd>

Se incluye un número de secuencia de audio en el **miembro dwAudioStream** de la estructura identificada *por lpCopy*. Si usa esta marca y también desea copiar vídeo, también debe usar la marca MCI \_ DGV \_ COPY VIDEO \_ \_ STREAM. (Si no se especifica ninguna marca, se copian los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>SECUENCIA DE \_ VÍDEO DE COPIA DE MCI DGV \_ \_ \_
</dt> <dd>

Se incluye un número de secuencia de vídeo en el **miembro dwVideoStream** de la estructura identificada *por lpCopy*. Si usa esta marca y también desea copiar audio, también debe usar la marca MCI \_ DGV \_ COPY AUDIO \_ \_ STREAM. (Si no se especifica ninguna marca, se copian los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Se incluye una ubicación inicial en el **miembro dwFrom** de la estructura identificada *por lpCopy*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Se incluye una ubicación final en el **miembro dwTo** de la estructura identificada *por lpCopy*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT del comando \_ \_ MCI \_ SET.

</dd> </dl>

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

 


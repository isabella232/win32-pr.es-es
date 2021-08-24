---
title: MCI_DELETE comando (Mmsystem.h)
description: El comando MCI \_ DELETE quita los datos del archivo. Los dispositivos de audio y vídeo digital reconocen este comando.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- MCI_DELETE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada80894f9260d0c37323d645694e10b0bcef92e52ebd670764bb9a0c436f837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784585"
---
# <a name="mci_delete-command"></a>Comando MCI \_ DELETE

El comando MCI \_ DELETE quita los datos del archivo. Los dispositivos de audio y vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
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

MCI \_ NOTIFY, MCI \_ WAIT o, para dispositivos de vídeo digital, MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Las marcas siguientes se aplican al tipo **de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ DELETE \_ AT
</dt> <dd>

Se incluye un rectángulo en el **miembro rc** de la estructura identificada por *lpDelete*. El rectángulo especifica la parte de cada marco que se eliminará. Cuando se usa esta marca, el marco se conserva en el área de trabajo y el área especificada por el rectángulo se vuelve negra. Si se omite la marca, MCI DELETE tiene como valor predeterminado todo el marco y \_ lo quita del área de trabajo.

</dd> <dt>

<span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ DELETE \_ AUDIO \_ STREAM
</dt> <dd>

Se incluye un número de secuencia de audio en el **miembro dwAudioStream** de la estructura identificada *por lpDelete*. Si usa esta marca y también desea eliminar vídeo, también debe usar la marca MCI \_ DGV \_ DELETE VIDEO \_ \_ STREAM. (Si no se especifica ninguna marca, se eliminan los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI \_ DGV \_ DELETE \_ VIDEO \_ STREAM
</dt> <dd>

Se incluye un número de secuencia de vídeo en el **miembro dwVideoStream** de la estructura identificada *por lpDelete*. Si usa esta marca y también desea eliminar audio, también debe usar la marca \_ MCI DGV \_ DELETE AUDIO \_ \_ STREAM. (Si no se especifica ninguna marca, se eliminan los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Se incluye una ubicación inicial en el **miembro dwFrom** de la estructura identificada por *lpDelete*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Se incluye una ubicación final en el **miembro dwTo** de la estructura identificada por *lpDelete*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT de \_ \_ MCI \_ SET.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpDelete* apunta a una estructura [**MCI \_ DGV \_ DELETE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms)

Las marcas siguientes se aplican al tipo **de dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Se incluye una ubicación inicial en el **miembro dwFrom** de la estructura identificada por *lpDelete*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT de \_ \_ [MCI \_ SET](mci-set.md).

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Se incluye una ubicación final en el **miembro dwTo** de la estructura identificada por *lpDelete*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT de \_ \_ MCI \_ SET.

</dd> </dl>

En el caso de los dispositivos de audio de forma de onda, el parámetro *lpDelete* apunta a una estructura [**\_ MCI WAVE \_ DELETE \_ PARMS.**](mci-wave-delete-parms.md)

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

 


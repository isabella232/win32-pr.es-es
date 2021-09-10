---
title: MCI_PASTE comando (Mmsystem.h)
description: El comando MCI \_ PASTE pega los datos del Portapapeles en un archivo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- MCI_PASTE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370051"
---
# <a name="mci_paste-command"></a>Comando MCI \_ PASTE

El comando MCI \_ PASTE pega los datos del Portapapeles en un archivo. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
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

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*
</dt> <dd>

Puntero a una [**estructura MCI \_ DGV \_ PASTE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI \_ DGV \_ PASTE \_ AT
</dt> <dd>

Se incluye un rectángulo en el **miembro rc** de la estructura identificada por *lpPaste*. Los dos primeros valores del rectángulo especifican el punto dentro del marco para colocar la información del Portapapeles. Si el alto y el ancho del rectángulo son distintos de cero, el contenido del Portapapeles se escala a esas dimensiones cuando se pegan en el marco. Si se omite la marca, MCI PASTE tiene como valor predeterminado \_ todo el rectángulo del marco.

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ PASTE \_ AUDIO \_ STREAM
</dt> <dd>

Se incluye un número de secuencia de audio en el **miembro dwAudioStream** de la estructura identificada *por lpPaste.* Si solo existe una secuencia de audio en el Portapapeles, los datos de audio se pegan en la secuencia designada. Si hay más de una secuencia de audio en el Portapapeles, la secuencia indica el número inicial de las secuencias de secuencia. Si usa esta marca y también quiere pegar vídeo, también debe usar la marca \_ MCI DGV \_ PASTE VIDEO \_ \_ STREAM. (Si no se especifica ninguna marca, todas las secuencias de audio y vídeo se pegan a partir de la primera secuencia de audio y vídeo. Cada secuencia pegada conserva su número de secuencia original).

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>INSERCIÓN \_ DE PEGAR DE MCI DGV \_ \_
</dt> <dd>

Los datos del Portapapeles se deben insertar en el área de trabajo existente en la posición especificada por la marca MCI \_ TO. Los datos existentes después del punto de inserción se mueven en el área de trabajo para hacer espacio. Este es el valor predeterminado.

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>SOBRESCRITURA \_ DE PEGADO DE MCI DGV \_ \_
</dt> <dd>

Los datos del Portapapeles deben reemplazar los datos que ya están presentes en el área de trabajo. Los datos del área de trabajo reemplazados siguen al punto de inserción.

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI \_ DGV \_ PASTE \_ VIDEO \_ STREAM
</dt> <dd>

Se incluye un número de secuencia de vídeo en el **miembro dwVideoStream** de la estructura identificada *por lpPaste*. Si solo existe una secuencia de vídeo en el Portapapeles, los datos de vídeo se pegan en la secuencia designada. Si existe más de una secuencia de vídeo en el Portapapeles, la secuencia indica el número inicial de las secuencias de secuencia. Si usa esta marca y también quiere pegar audio, también debe usar la marca \_ MCI DGV \_ PASTE AUDIO \_ \_ STREAM. (Si no se especifica ninguna marca, todas las secuencias de audio y vídeo se pegan a partir de la primera secuencia de audio y vídeo. Cada secuencia pegada conserva su número de secuencia original).

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Se incluye un valor de posición en el **miembro dwTo** de la estructura identificada por *lpPaste*. El valor de posición especifica la posición para empezar a pegar datos en el área de trabajo. Si se omite esta marca, la posición tiene como valor predeterminado la posición actual.

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

 


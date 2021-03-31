---
title: Comando MCI_PASTE (mmsystem. h)
description: El \_ comando MCI Paste pega los datos del portapapeles en un archivo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- Comando de MCI_PASTE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801021"
---
# <a name="mci_paste-command"></a>\_Comando de pegado de MCI

El \_ comando MCI Paste pega los datos del portapapeles en un archivo. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*
</dt> <dd>

Puntero a una estructura de [**\_ DGV de copia de \_ \_ parms de MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>\_pegar DGV \_ \_ de MCI
</dt> <dd>

Se incluye un rectángulo en el miembro **RC** de la estructura identificada por *lpPaste*. Los dos primeros valores del rectángulo especifican el punto dentro del marco para colocar la información del portapapeles. Si el alto y el ancho del rectángulo son distintos de cero, el contenido del portapapeles se escala a esas dimensiones cuando se pegan en el marco. Si se omite la marca, el pegado de MCI tiene como \_ valor predeterminado el rectángulo del marco completo.

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ pegar \_ secuencia de audio \_
</dt> <dd>

Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpPaste*. Si solo existe una secuencia de audio en el portapapeles, los datos de audio se pegan en la secuencia designada. Si existe más de una secuencia de audio en el portapapeles, la secuencia indica el número de inicio de las secuencias de la secuencia. Si usa esta marca y también quiere pegar vídeo, también debe usar la \_ marca MCI DGV \_ pegar vídeo de \_ la \_ secuencia. (Si no se especifica ninguna marca, todas las secuencias de audio y vídeo se pegarán a partir de la primera secuencia de audio y vídeo. Cada secuencia pegada conserva su número de secuencia original).

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>\_DGV MCI \_ pegar \_ inserción
</dt> <dd>

Los datos del portapapeles se deben insertar en el área de trabajo existente en la posición especificada por el MCI \_ para la marca. Los datos existentes después del punto de inserción se mueven en el área de trabajo para dejar espacio. Este es el valor predeterminado.

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>SOBRESCRITURA de la copia de DGV de MCI \_ \_ \_
</dt> <dd>

Los datos del portapapeles deben reemplazar los datos que ya están presentes en el área de trabajo. Los datos del área de trabajo reemplazan después del punto de inserción.

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>\_secuencia de \_ vídeo de pegado de MCI DGV \_ \_
</dt> <dd>

Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpPaste*. Si solo existe una secuencia de vídeo en el portapapeles, los datos de vídeo se pegan en la secuencia designada. Si existe más de una secuencia de vídeo en el portapapeles, la secuencia indica el número de inicio de las secuencias de la secuencia. Si usa esta marca y también quiere pegar audio, también debe usar la \_ marca MCI DGV \_ pegar audio de \_ la \_ secuencia. (Si no se especifica ninguna marca, todas las secuencias de audio y vídeo se pegarán a partir de la primera secuencia de audio y vídeo. Cada secuencia pegada conserva su número de secuencia original).

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

Un valor de posición se incluye en el miembro **dwTo** de la estructura identificada por *lpPaste*. El valor de posición especifica la posición en la que se comienzan a pegar los datos en el área de trabajo. Si se omite esta marca, la posición tiene como valor predeterminado la posición actual.

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

 


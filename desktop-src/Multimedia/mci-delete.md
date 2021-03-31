---
title: Comando MCI_DELETE (mmsystem. h)
description: El \_ comando de eliminación de MCI quita los datos del archivo. Los dispositivos de audio digital y de onda-vídeo reconocen este comando.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- Comando de MCI_DELETE de Windows multimedia
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
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996701"
---
# <a name="mci_delete-command"></a>Comando de eliminación de MCI \_

El \_ comando de eliminación de MCI quita los datos del archivo. Los dispositivos de audio digital y de onda-vídeo reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las marcas siguientes se aplican al tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ eliminar \_ en
</dt> <dd>

Se incluye un rectángulo en el miembro **RC** de la estructura identificada por *lpDelete*. El rectángulo especifica la parte de cada fotograma que se va a eliminar. Cuando se usa esta marca, el marco se conserva en el área de trabajo y el área especificada por el rectángulo se vuelve negra. Si se omite la marca, la \_ eliminación de los valores predeterminados de MCI es todo el marco y quita el marco del área de trabajo.

</dd> <dt>

<span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ eliminar \_ secuencia de audio \_
</dt> <dd>

Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpDelete*. Si usa esta marca y también quiere eliminar vídeo, también debe usar la \_ marca MCI DGV \_ Delete \_ video \_ Stream. (Si no se especifica ninguna marca, se eliminarán los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>\_secuencia de \_ vídeo de eliminación de DGV de MCI \_ \_
</dt> <dd>

Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpDelete*. Si usa esta marca y también quiere eliminar audio, también debe usar la \_ marca MCI DGV \_ Delete \_ audio \_ Stream. (Si no se especifica ninguna marca, se eliminarán los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde
</dt> <dd>

Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpDelete*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpDelete*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de MCI \_ set.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpDelete* apunta a una estructura [**MCI \_ DGV \_ Delete \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) .

Las marcas siguientes se aplican al tipo de dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde
</dt> <dd>

Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpDelete*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de [MCI \_ set](mci-set.md).

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpDelete*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de MCI \_ set.

</dd> </dl>

En el caso de los dispositivos de audio de onda, el parámetro *lpDelete* apunta a una estructura parms de la [**\_ \_ eliminación \_ de onda MCI**](mci-wave-delete-parms.md) .

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

 


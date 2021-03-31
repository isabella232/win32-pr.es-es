---
title: Comando MCI_CUT (mmsystem. h)
description: El \_ comando MCI CUT quita los datos del archivo y los copia en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- Comando de MCI_CUT de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996702"
---
# <a name="mci_cut-command"></a>Comando de corte de MCI \_

El \_ comando MCI CUT quita los datos del archivo y los copia en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
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

<span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*
</dt> <dd>

Puntero a una estructura de [**parms de DGV de MCI \_ \_ \_ cortada**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>\_DGV \_ de MCI cortado \_ en
</dt> <dd>

Se incluye un rectángulo en el miembro **RC** de la estructura identificada por *lpCut*. El rectángulo especifica la parte de cada fotograma que se va a cortar. Si se omite la marca, \_ el corte de MCI corta todo el marco.

</dd> <dt>

<span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>\_flujo de \_ audio de cortar DGV \_ de MCI \_
</dt> <dd>

Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpCut*. Si usa esta marca y también desea cortar vídeo, también debe usar la \_ marca MCI DGV \_ Cut \_ video \_ Stream. (Si no se especifica ninguna marca, se cortarán los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_flujo de \_ vídeo de cortar DGV \_ de MCI \_
</dt> <dd>

Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpCut*. Si usa esta marca y también desea cortar audio, también debe usar la \_ marca MCI DGV \_ Cut \_ audio \_ Stream. (Si no se especifica ninguna marca, se cortarán los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde
</dt> <dd>

Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpCut*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a
</dt> <dd>

Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpCut*. Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de MCI \_ set.

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

 


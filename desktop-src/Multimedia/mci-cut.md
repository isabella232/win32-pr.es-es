---
title: MCI_CUT comando (Mmsystem.h)
description: El comando MCI \_ CUT quita los datos del archivo y los copia en el Portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- MCI_CUT comando Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246086"
---
# <a name="mci_cut-command"></a>Comando MCI \_ CUT

El comando MCI \_ CUT quita los datos del archivo y los copia en el Portapapeles. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*
</dt> <dd>

Puntero a una [**estructura MCI \_ DGV \_ CUT \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI \_ DGV \_ CUT \_ AT
</dt> <dd>

Se incluye un rectángulo en el **miembro rc** de la estructura identificada por *lpCut*. El rectángulo especifica la parte de cada marco que se debe cortar. Si se omite la marca, MCI \_ CUT corta todo el marco.

</dd> <dt>

<span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>SECUENCIA DE AUDIO DE \_ CORTE DE MCI DGV \_ \_ \_
</dt> <dd>

Se incluye un número de secuencia de audio en el **miembro dwAudioStream** de la estructura identificada por *lpCut*. Si usa esta marca y también quiere cortar vídeo, también debe usar la marca \_ MCI DGV \_ CUT VIDEO \_ \_ STREAM. (Si no se especifica ninguna marca, se cortan los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>SECUENCIA DE \_ VÍDEO DE CORTE DE MCI DGV \_ \_ \_
</dt> <dd>

Se incluye un número de secuencia de vídeo en el **miembro dwVideoStream** de la estructura identificada por *lpCut*. Si usa esta marca y también desea cortar audio, también debe usar la marca \_ MCI DGV \_ CUT AUDIO \_ \_ STREAM. (Si no se especifica ninguna marca, se cortan los datos de todas las secuencias de audio y vídeo).

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Se incluye una ubicación inicial en el **miembro dwFrom** de la estructura identificada por *lpCut*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Se incluye una ubicación final en el **miembro dwTo** de la estructura identificada por *lpCut*. Las unidades asignadas a los valores de posición se especifican con la marca MCI \_ SET TIME FORMAT de \_ \_ MCI \_ SET.

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

 


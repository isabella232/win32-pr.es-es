---
title: MCI_STEP comando (Mmsystem.h)
description: El comando MCI \_ STEP guía al reproductor uno o varios fotogramas. Los dispositivos de vídeo en formato vídeo digital, VCR y CSV reconocen este comando.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- MCI_STEP comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526d5f69d0b0c02d977cc8fc73cd81a7a1bf06c3e55088f11d53c05cfa72c0c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986173"
---
# <a name="mci_step-command"></a>Comando STEP de MCI \_

El comando MCI \_ STEP guía al reproductor uno o varios fotogramas. Los dispositivos de vídeo en formato vídeo digital, VCR y CSV reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
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

<span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

Este comando admite dispositivos que devuelven **TRUE** a la marca \_ MCI GETDEVCAPS \_ HAS VIDEO del comando \_ [ \_ GETDEVCAPS de MCI.](mci-getdevcaps.md)

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MARCOS DE PASOS \_ DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwFrames** de la estructura identificada por *lpStep* especifica el número de fotogramas que se avanzarán antes de mostrar otra imagen.

</dd> <dt>

<span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>PASO INVERSO \_ DE MCI DGV \_ \_
</dt> <dd>

Pasos inversos.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el *parámetro lpStep* apunta a una estructura [**\_ MCI DGV \_ STEP \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MARCOS DE PASOS \_ DE VCR \_ DE MCI \_
</dt> <dd>

El **miembro dwFrames** de la estructura identificada por *lpStep* especifica el número de fotogramas que se avanzarán antes de mostrar otra imagen.

</dd> <dt>

<span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>PASO INVERSO \_ DE VCR \_ DE MCI \_
</dt> <dd>

Pasos inversos.

</dd> </dl>

En el caso de los dispositivos VCR, el *parámetro lpStep* apunta a una estructura [**\_ MCI VCR \_ STEP \_ PARMS.**](mci-vcr-step-parms.md)

Las marcas adicionales siguientes se usan con el **tipo de dispositivo videodisc:**

<dl> <dt>

<span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MARCOS DE PASOS VD DE MCI \_ \_ \_
</dt> <dd>

El **miembro dwFrames** de la estructura identificada por *lpStep* especifica el número de fotogramas para el paso.

</dd> <dt>

<span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>PASO DE VD DE MCI \_ \_ \_ INVERSO
</dt> <dd>

Pasos inversos.

</dd> </dl>

En el caso de los dispositivos videodisc, el *parámetro lpStep* apunta a una [**estructura \_ MCI VD STEP \_ \_ PARMS.**](mci-vd-step-parms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 


---
title: MCI_SIGNAL comando (Mmsystem.h)
description: El comando MCI \_ SIGNAL establece una posición especificada en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando. MCIAVI solo admite una señal activa a la vez.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- MCI_SIGNAL comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370100"
---
# <a name="mci_signal-command"></a>Comando MCI \_ SIGNAL

El comando MCI \_ SIGNAL establece una posición especificada en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando. MCIAVI solo admite una señal activa a la vez.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
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

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*
</dt> <dd>

Puntero a una [**estructura \_ MCI DGV \_ SIGNAL \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

La ventana cuyo identificador especifique en el **miembro dwCallback** de la estructura [**MCI \_ DGV \_ SIGNAL \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) recibe el mensaje MM \_ MCISIGNAL.

Las marcas siguientes se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI \_ DGV \_ SIGNAL \_ AT
</dt> <dd>

Se incluye una posición de señal en el **miembro dwPosition** de la estructura identificada por *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI \_ DGV \_ SIGNAL \_ CANCEL
</dt> <dd>

Quita la posición de señal especificada por el valor asociado a MCI \_ DGV \_ SIGNAL \_ USERVAL.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI \_ DGV \_ SIGNAL \_ EVERY
</dt> <dd>

Se incluye un valor de período de señal en el **miembro dwPeriod** de la estructura identificada *por lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>POSICIÓN DE \_ LA SEÑAL DE MCI DGV \_ \_
</dt> <dd>

El dispositivo enviará el valor de posición con el Windows en lugar del valor especificado por el usuario.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI \_ DGV \_ SIGNAL \_ USERVAL
</dt> <dd>

Se incluye un valor de datos en el **miembro dwUserParm** de la estructura identificada *por lpSignal*. El valor de datos asociado a esta solicitud se notifica de nuevo con Windows mensaje.

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

 


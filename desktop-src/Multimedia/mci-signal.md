---
title: Comando MCI_SIGNAL (mmsystem. h)
description: El \_ comando MCI Signal establece una posición especificada en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando. MCIAVI solo admite una señal activa a la vez.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- Comando de MCI_SIGNAL de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422222"
---
# <a name="mci_signal-command"></a>Comando de señal de MCI \_

El \_ comando MCI Signal establece una posición especificada en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando. MCIAVI solo admite una señal activa a la vez.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*
</dt> <dd>

Puntero a una estructura de parms de DGV de la [**\_ \_ señal \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La ventana cuyo identificador se especifica en el miembro **dwCallback** de la estructura [**MCI \_ DGV \_ Signal \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) recibe el mensaje mm \_ MCISIGNAL.

Las marcas siguientes se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_ \_ señal de MCI DGV \_ en
</dt> <dd>

Una posición de la señal se incluye en el miembro **dwPosition** de la estructura identificada por *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>\_cancelación de \_ señal de DGV MCI \_
</dt> <dd>

Quita la posición de la señal especificada por el valor asociado a MCI \_ DGV \_ Signal \_ USERVAL.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>señal de MCI \_ DGV \_ \_ cada
</dt> <dd>

Un valor de período de señal se incluye en el miembro **dwPeriod** de la estructura identificada por *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>posición de la señal de MCI \_ DGV \_ \_
</dt> <dd>

El dispositivo enviará el valor de posición con el mensaje de Windows en lugar del valor especificado por el usuario.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>\_USERVAL de \_ señal MCI DGV \_
</dt> <dd>

Un valor de datos se incluye en el miembro **dwUserParm** de la estructura identificada por *lpSignal*. El valor de datos asociado a esta solicitud se devuelve con el mensaje de Windows.

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

 


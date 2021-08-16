---
title: MCI_SPIN comando (Mmsystem.h)
description: El comando SPIN de MCI \_ inicia el dispositivo girando hacia arriba o hacia abajo. Los dispositivos videodiscos reconocen este comando.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- MCI_SPIN comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41457cbd04de7ffc85248912224819f9c7549c8aebd34d60c4a7efcd70bbcada
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374597"
---
# <a name="mci_spin-command"></a>Comando SPIN de MCI \_

El comando SPIN de MCI \_ inicia el dispositivo girando hacia arriba o hacia abajo. Los dispositivos videodiscos reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
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

MCI \_ NOTIFY o MCI \_ WAIT. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

Las marcas adicionales siguientes se aplican a los dispositivos videodisc:

<dl> <dt>

<span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI \_ VD \_ SPIN \_ DOWN
</dt> <dd>

Detiene el giro del disco.

</dd> <dt>

<span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI \_ VD \_ SPIN \_ UP
</dt> <dd>

Inicia el disco girando.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 


---
title: MCI_CLOSE comando (Mmsystem.h)
description: El comando MCI \_ CLOSE libera el acceso a un dispositivo o archivo. Todos los dispositivos reconocen este comando.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- MCI_CLOSE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369925"
---
# <a name="mci_close-command"></a>Comando MCI \_ CLOSE

El comando MCI \_ CLOSE libera el acceso a un dispositivo o archivo. Todos los dispositivos reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
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

<span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (También puede usar una estructura **MCI \_ CLOSE \_ PARMS.** Para obtener más información, vea los comentarios de **MCI \_ GENERIC \_ PARMS).**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Salir de una aplicación sin cerrar ningún dispositivo MCI que haya abierto puede dejar el dispositivo inaccesible. La aplicación debe cerrar explícitamente cada dispositivo o archivo cuando haya terminado con él. MCI descarga el dispositivo cuando se cierran todas las instancias del dispositivo o todos los archivos asociados.

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

 


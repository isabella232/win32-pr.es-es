---
title: MCI_BREAK comando (Mmsystem.h)
description: El comando BREAK de MCI \_ establece una clave de interrupción para un dispositivo MCI. MCI admite este comando directamente en lugar de pasarlo al dispositivo. Cualquier aplicación MCI puede usar este comando.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- MCI_BREAK comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169666"
---
# <a name="mci_break-command"></a>Comando BREAK de MCI \_

El comando BREAK de MCI \_ establece una clave de interrupción para un dispositivo MCI. MCI admite este comando directamente en lugar de pasarlo al dispositivo. Cualquier aplicación MCI puede usar este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
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

MCI NOTIFY, MCI WAIT o, para dispositivos de grabadora de vídeo digital y vídeo \_ \_ (VCR), MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*
</dt> <dd>

Puntero a una [**estructura \_ MCI BREAK \_ PARMS.**](mci-break-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Es posible que tenga que presionar la tecla de interrupción varias veces para interrumpir una operación de espera. Al presionar la tecla de interrupción después de cancelarse una espera del dispositivo, se puede enviar la interrupción a una aplicación. Si una aplicación tiene una acción definida para el código de clave virtual, puede responder involuntariamente a la interrupción. Por ejemplo, una aplicación que usa VK CANCEL para una tecla de aceleración puede responder a la tecla CTRL+BREAK predeterminada si se presiona después de cancelar \_ una espera.

Las siguientes marcas adicionales se aplican a todos los dispositivos:

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI \_ BREAK \_ HWND
</dt> <dd>

El **miembro hwndBreak** de la estructura identificada por *lpBreak* contiene un identificador de ventana que debe ser la ventana actual para habilitar la detección de saltos para ese dispositivo MCI. Esta suele ser la ventana principal de la aplicación. Si se omite, MCI no comprueba el identificador de ventana de la ventana actual.

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>CLAVE DE \_ INTERRUPCIÓN DE MCI \_
</dt> <dd>

El **miembro nVirtKey** de la estructura identificada por *lpBreak* especifica el código de clave virtual usado para la clave de interrupción. De forma predeterminada, MCI asigna CTRL+BREAK como tecla de interrupción. Esta marca es necesaria si no se especifica MCI \_ BREAK \_ OFF.

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI \_ BREAK \_ OFF
</dt> <dd>

Deshabilita cualquier clave de interrupción existente para el dispositivo indicado.

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

 


---
title: Comando MCI_BREAK (mmsystem. h)
description: El \_ comando de interrupción de MCI establece una tecla de interrupción para un dispositivo MCI. MCI admite este comando directamente en lugar de pasarlo al dispositivo. Cualquier aplicación MCI puede usar este comando.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- Comando de MCI_BREAK de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490132"
---
# <a name="mci_break-command"></a>Comando de interrupción de MCI \_

El \_ comando de interrupción de MCI establece una tecla de interrupción para un dispositivo MCI. MCI admite este comando directamente en lugar de pasarlo al dispositivo. Cualquier aplicación MCI puede usar este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Las \_ notificaciones de MCI, espera de MCI \_ o, para dispositivos de grabadora de vídeo digital y vídeo (VCR), prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms de interrupción de MCI**](mci-break-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Es posible que tenga que presionar la tecla interrumpir varias veces para interrumpir una operación de espera. Al presionar la tecla interrumpir después de que se cancele un dispositivo, puede enviar la interrupción a una aplicación. Si una aplicación tiene una acción definida para el código de tecla virtual, puede responder accidentalmente a la interrupción. Por ejemplo, una aplicación que use VK \_ Cancel para una tecla de aceleración puede responder a la tecla Ctrl + Inter predeterminada si se presiona después de que se cancele la espera.

Las siguientes marcas adicionales se aplican a todos los dispositivos:

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>\_hWnd de interrupción de MCI \_
</dt> <dd>

El miembro **hwndBreak** de la estructura identificada por *lpBreak* contiene un identificador de ventana que debe ser la ventana actual para habilitar la detección de interrupciones para ese dispositivo MCI. Esta suele ser la ventana principal de la aplicación. Si se omite, MCI no comprueba el identificador de ventana de la ventana actual.

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_tecla de interrupción de MCI \_
</dt> <dd>

El miembro **nVirtKey** de la estructura identificada por *lpBreak* especifica el código de la clave virtual que se usa para la tecla interrumpir. De forma predeterminada, MCI asigna CTRL + INTER como tecla de salto. Esta marca es necesaria si \_ no se especifica la interrupción de MCI \_ .

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>interrupción de MCI \_ \_
</dt> <dd>

Deshabilita cualquier clave de interrupción existente para el dispositivo indicado.

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

 


---
title: Comando MCI_CLOSE (mmsystem. h)
description: El \_ comando MCI Close libera el acceso a un dispositivo o archivo. Todos los dispositivos reconocen este comando.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- Comando de MCI_CLOSE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150175"
---
# <a name="mci_close-command"></a>Comando de cierre de MCI \_

El \_ comando MCI Close libera el acceso a un dispositivo o archivo. Todos los dispositivos reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificación de MCI o \_ espera de MCI. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (También puede usar una estructura **\_ \_ parms de cierre de MCI** . Para obtener más información, vea los comentarios de **MCI \_ Generic \_ parms**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Salir de una aplicación sin cerrar los dispositivos MCI abiertos puede dejar el dispositivo inaccesible. La aplicación debe cerrar explícitamente cada dispositivo o archivo cuando termine de usarlo. MCI descarga el dispositivo cuando se cierran todas las instancias del dispositivo o todos los archivos asociados.

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

 


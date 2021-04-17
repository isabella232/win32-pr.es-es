---
title: Comando MCI_ESCAPE (mmsystem. h)
description: El \_ comando MCI escape envía una cadena directamente al dispositivo. Los dispositivos de videodisco reconocen este comando.
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- Comando de MCI_ESCAPE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676775"
---
# <a name="mci_escape-command"></a>Comando de escape de MCI \_

El \_ comando MCI escape envía una cadena directamente al dispositivo. Los dispositivos de videodisco reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
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

<span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*
</dt> <dd>

Puntero a una [**estructura \_ parms de secuencias de \_ escape \_ de MCI Vd**](mci-vd-escape-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Los datos que se envían con el escape de MCI \_ dependen del dispositivo y normalmente se pasan directamente al hardware asociado con el dispositivo.

La marca adicional siguiente se aplica a los dispositivos de videodisco:

<dl> <dt>

<span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>cadena de escape de MCI \_ Vd \_ \_
</dt> <dd>

Una cadena de comandos se especifica en el miembro **lpstrCommand** de la estructura identificada por *lpEscape*. Esta marca es obligatoria.

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

 


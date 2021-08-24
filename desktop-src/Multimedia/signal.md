---
title: comando signal
description: El comando signal identifica una posición especificada en el área de trabajo mediante el envío de un mensaje MM MCISIGNAL a la \_ aplicación. Los dispositivos de vídeo digital reconocen este comando. MCIAVI solo admite una señal activa a la vez.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- Comando signal Windows Multimedia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db007a03738f13bb9acc0733b67bcd38de4b97f2b194bb16cdfcd85f798cfdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037185"
---
# <a name="signal-command"></a>comando signal

El comando signal identifica una posición especificada en el área de trabajo mediante el envío de un [mensaje \_ MM MCISIGNAL](mm-mcisignal.md) a la aplicación. Los dispositivos de vídeo digital reconocen este comando. MCIAVI solo admite una señal activa a la vez.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*
</dt> <dd>

Una de las marcas siguientes.



| Value            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en la posición      | Especifica el marco para invocar una señal.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| cancel           | Quita las señales del área de trabajo. Se especifica una señal individual mediante la marca "uservalue". Si la marca "uservalue" no se especifica mediante "cancel", el dispositivo cancela todas las señales. La marca "cancel" no es compatible con las marcas "at", "every" y "return position".                                                                                                                                                                                                                                                                                          |
| cada *intervalo* | Especifica el período de las señales. El *valor* de intervalo se especifica en el formato de hora actual. Si se usa con la posición *"at",* las señales se colocan en todo el área de trabajo con una marca de señal colocada en *la posición*.<br/> Sin la marca "at", las señales se colocan en todo el área de trabajo con una señal en la posición actual.<br/> Si se omite esta marca, solo se marca la posición indicada por la marca "at".<br/> Si el *valor de* intervalo es menor que la frecuencia mínima admitida por un dispositivo, usará su valor mínimo.<br/> |
| posición de devolución  | Indica que el dispositivo debe enviar el valor de posición en lugar del identificador "uservalue" en el mensaje de señalización. El identificador "uservalue" todavía se puede usar para cancelar o volver a definir las marcas de señal.                                                                                                                                                                                                                                                                                                                                                                      |
| id. de *valor de usuario*   | Especifica un identificador que se notifica con el mensaje de señalización. Este identificador actúa como un identificador que se puede usar con otros comandos **de** señal para hacer referencia a esta **configuración de** señal. Si se omite, el valor predeterminado es cero.                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

El identificador de ventana utilizado para la notificación de mensajes de finalización de comandos también se usa para la señalización.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[MM \_ MCISIGNAL](mm-mcisignal.md)
</dt> </dl>

 


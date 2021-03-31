---
title: Reserve (comando)
description: El comando Reserve asigna espacio en disco contiguo para el área de trabajo de la instancia del dispositivo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- comando Reserve de Windows multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995955"
---
# <a name="reserve-command"></a>Reserve (comando)

El comando Reserve asigna espacio en disco contiguo para el área de trabajo de la instancia del dispositivo. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*
</dt> <dd>

Una o varias de las marcas siguientes.



| Value           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *ruta de acceso*       | Especifica la unidad y la ruta de acceso del directorio (pero no el nombre) de un archivo temporal que se usa para almacenar los datos registrados. El dispositivo especifica el nombre de este archivo. El archivo temporal se elimina cuando se cierra el dispositivo. Si se omite esta marca, el dispositivo especifica la ubicación del espacio en disco.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *duración* del tamaño | Especifica la cantidad aproximada de espacio en disco que se va a reservar en el área de trabajo. El valor *Duration* se especifica en el formato de hora actual. El dispositivo basa su estimación del espacio en disco necesario en los parámetros siguientes: la hora solicitada, el formato de archivo, el algoritmo de compresión de audio y vídeo, y los valores de calidad de compresión en vigor. Si [setvideo](setvideo.md) "registro" es "desactivado", el espacio solo se reserva para el audio. Si [SetAudio](setaudio.md) "registro" es "desactivado", el espacio solo se reserva para vídeo. Si ambos son "OFF", o si *Duration* es cero, no se reserva ningún espacio y se cancela la asignación de cualquier espacio reservado existente. Si se omite esta marca, el dispositivo usará un valor predeterminado definido por el dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify", "Test" o una combinación de estos. Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si es necesario, los comandos [registro](record.md) o [Guardar](save.md) subsiguientes usan el espacio reservado por este comando. Si el área de trabajo contiene datos no guardados, se perderán los datos. Algunos dispositivos no requieren reserva y lo omiten. Si no se reserva espacio en disco antes de la grabación, el comando de registro realiza una reserva implícita con las marcas predeterminadas específicas del dispositivo. Use un comando de reserva explícito si desea tener un mayor control sobre cuándo se produce el retraso de la asignación de disco, el control de cuánto espacio se asigna y el control de dónde se asigna el espacio en disco. La aplicación puede cambiar la cantidad y la ubicación del espacio en disco reservado previamente con comandos de reserva posteriores. Cualquier espacio en disco asignado y todavía sin usar no se cancela hasta que se guardan los datos grabados, o hasta que se cierra la instancia del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[guardar](save.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 


---
title: comando reserve
description: El comando reserve asigna espacio en disco contiguo para el área de trabajo de la instancia del dispositivo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- comando reserve Windows Multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83f4573f5a630bbf1243b7126867c2d6c6beef61810210624fe87958e12b02ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892925"
---
# <a name="reserve-command"></a>comando reserve

El comando reserve asigna espacio en disco contiguo para el área de trabajo de la instancia del dispositivo. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

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
| en la *ruta de acceso*       | Especifica la unidad y la ruta de acceso del directorio (pero no el nombre) de un archivo temporal que se usa para contener los datos registrados. El dispositivo especifica el nombre de este archivo. El archivo temporal se elimina cuando se cierra el dispositivo. Si se omite esta marca, el dispositivo especifica la ubicación del espacio en disco.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| duración *del tamaño* | Especifica la cantidad aproximada de espacio en disco que se reserva en el área de trabajo. El *valor* de duración se especifica en el formato de hora actual. El dispositivo basa su estimación del espacio en disco necesario en los parámetros siguientes: la hora solicitada, el formato de archivo, el algoritmo de compresión de audio y vídeo y los valores de calidad de compresión en vigor. Si [setvideo](setvideo.md) "record" está "desactivado", el espacio se reserva solo para audio. Si [setaudio](setaudio.md) "record" está "desactivado", el espacio se reserva solo para vídeo. Si ambos están "desactivados" o si *la* duración es cero, no se reserva ningún espacio y se desasigna cualquier espacio reservado existente. Si se omite esta marca, el dispositivo usará un valor predeterminado definido por el dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Si es necesario, [los comandos de](record.md) registro [o](save.md) guardado posteriores usan el espacio reservado por este comando. Si el área de trabajo contiene datos no guardados, los datos se pierden. Algunos dispositivos no requieren reserva y la omiten. Si el espacio en disco no está reservado antes de la grabación, el comando record realiza una reserva implícita con marcas predeterminadas específicas del dispositivo. Use un comando de reserva explícito si desea un mejor control de cuándo se produce el retraso en la asignación de disco, el control de la cantidad de espacio asignado y el control de dónde se asigna el espacio en disco. La aplicación puede cambiar la cantidad y la ubicación del espacio en disco previamente reservado con los comandos de reserva posteriores. Cualquier espacio en disco asignado y sin usar no se desasigna hasta que se guarden los datos registrados o hasta que se cierre la instancia del dispositivo.

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

[record](record.md)
</dt> <dt>

[guardar](save.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 


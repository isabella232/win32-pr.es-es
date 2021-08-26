---
title: comando monitor
description: El comando monitor especifica el origen de la presentación. (El origen de presentación predeterminado es el área de trabajo). Al cambiar el origen de presentación, se cambian todas las secuencias de audio y vídeo del origen. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- comando monitor Windows Multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef9a47db68856196dc84aefb3c5f110941189dec80f62b369eae13c60932d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038815"
---
# <a name="monitor-command"></a>comando monitor

El comando monitor especifica el origen de la presentación. (El origen de presentación predeterminado es el área de trabajo). Al cambiar el origen de presentación, se cambian todas las secuencias de audio y vídeo del origen. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*
</dt> <dd>

Una o varias de las marcas siguientes.



| Value           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| archivo            | Especifica que el área de trabajo es el origen de la presentación. Este es el origen predeterminado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| input           | Especifica que la entrada externa es el origen de la presentación. Si un [comando de](play.md) reproducción está en curso, primero se pausa. Si [setvideo](setvideo.md) está "on", esta marca muestra una ventana oculta predeterminada. Los dispositivos pueden limitar lo que otras instancias de dispositivo pueden hacer durante la supervisión de la entrada.                                                                                                                                                                                                                                                                                                                                                                    |
| método  | Cuando se usa **con la** "entrada" del monitor, esta marca selecciona el método de supervisión. El *método* es "pre", "post" o "direct". La supervisión directa solicita que el dispositivo se configure para una calidad de visualización óptima durante la supervisión. El método de supervisión directa puede ser incompatible con la grabación de vídeo en movimiento. Grabación de vídeo de movimiento previa y posterior a la supervisión. La supervisión previa muestra la entrada externa antes de la compresión, mientras que la supervisión posterior muestra la entrada externa después de la compresión. Normalmente, los distintos métodos de supervisión tienen implicaciones de hardware diferentes. El dispositivo selecciona el método de supervisión predeterminado.<br/> |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

El origen de la presentación cambia automáticamente al área de trabajo después de una [reproducción,](play.md) [paso](step.md), [pausa,](pause.md) [indicación](cue.md) de "salida" o [comando de](seek.md) búsqueda. El [comando record](record.md) no cambia automáticamente los orígenes de presentación, lo que ofrece a la aplicación la opción de no mostrar vídeo mientras se graba.

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

[Cue](cue.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Jugar](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[Buscar](seek.md)
</dt> <dt>

[Paso](step.md)
</dt> </dl>

 


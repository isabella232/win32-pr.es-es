---
title: comando record
description: El comando record inicia la grabación de datos. Los dispositivos VCR y audio de forma de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- comando record Windows Multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370129"
---
# <a name="record-command"></a>comando record

El comando record inicia la grabación de datos. Los dispositivos VCR y audio de forma de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*
</dt> <dd>

Marca para registrar datos. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **de** registro y las marcas usadas por cada tipo.



| Value        | Significado                                                | Significado                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| digitalvideo | at *rectangle* audio stream *stream from* *position* hold | inserción de sobrescritura *para colocar la secuencia* de streaming de *vídeo* |
| sequencer    | desde *inserción de* posición                                  | sobrescribir a *la posición*                             |
| Vcr          | en el *momento de* la *inicialización de la* posición                     | insertar sobrescritura en *la posición*                      |
| waveaudio    | desde *inserción de* posición                                  | sobrescribir a *la posición*                             |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRecordFlags** y sus significados.



| Value                 | Significado                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *rectángulo*        | Especifica una región rectangular de la entrada externa utilizada como origen de los píxeles comprimidos y guardados. Si no se especifica, el rectángulo tiene como valor predeterminado el rectángulo especificado para [put](put.md) "video". Cuando se establece de forma diferente al rectángulo "vídeo", la imagen mostrada no es lo que se graba. |
| a *la vez*             | Indica cuándo debe comenzar el dispositivo a realizar este comando o, si el dispositivo se ha cued, cuando comienza el comando cued. Para obtener más información, vea el [comando cue.](cue.md)                                                                                                                             |
| secuencia *de* audio | Especifica la secuencia de audio utilizada para la grabación. Si no se especifica esta marca y el formato de archivo no define un valor predeterminado, se registra en la secuencia que está físicamente primero.                                                                                                                             |
| desde *la posición*       | Especifica una posición inicial para la grabación. Si no se especifica la marca "from", el dispositivo comienza a grabar en la posición actual.                                                                                                                                                                       |
| Mantener                  | Inmoviliza la imagen cuando la grabación ha finalizado en lugar de mostrar vídeo en directo. Cuando se detiene la grabación, [se realiza un comando](monitor.md) "archivo" de supervisión automática. Para volver al vídeo en directo, emita el **comando** de "entrada" del monitor.                                                                              |
| initialize            | Inicialice la cinta (multimedia), que implica la grabación de código de tiempo (si es posible) para vídeo y audio en blanco. Este comando puede tardar varias horas si se debe inicializar toda la cinta.                                                                                                                            |
| insert                | Especifica que se agregan nuevos datos al archivo en la posición actual.                                                                                                                                                                                                                                            |
| sobrescribir             | Especifica que los nuevos datos reemplazarán los datos del archivo.                                                                                                                                                                                                                                                           |
| para *colocar*         | Especifica una posición final para la grabación. Si no se especifica la marca "to", el dispositivo registra hasta que recibe un [comando stop](stop.md) [o pause.](pause.md)                                                                                                                                        |
| secuencia de *vídeo* | Especifica la secuencia de vídeo utilizada para la grabación. Si no se especifica y el formato de archivo no define un valor predeterminado, se registra en la secuencia que está físicamente primero.                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

La grabación se detiene cuando se [emite](stop.md) [un](pause.md) comando stop o pause. Para el controlador MCIWAVE, todos los datos registrados después de abrir un archivo se descartan si el archivo se cierra sin guardarlo.

Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el [comando set.](set.md) Las pistas que se van a grabar se especifican mediante los comandos [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record" y [setaudio](setaudio.md) "record".

## <a name="examples"></a>Ejemplos

El siguiente comando inicia la grabación en la posición actual.

``` syntax
record mysound
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[Cue](cue.md)
</dt> <dt>

[Monitor](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Poner](put.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[settimecode](settimecode.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 


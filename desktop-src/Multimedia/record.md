---
title: comando grabar
description: El comando grabar inicia la grabación de datos. Los dispositivos VCR y de onda-audio reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- comando grabar Windows multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905018"
---
# <a name="record-command"></a>comando grabar

El comando grabar inicia la grabación de datos. Los dispositivos VCR y de onda-audio reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca para la grabación de datos. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **registro** y las marcas usadas por cada tipo.



| Value        | Significado                                                | Significado                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| digitalvideo | *secuencia* de flujo de audio de *rectángulo* desde la *posición* de espera | insertar la *secuencia* de flujo de vídeo sobrescribir en la *posición* |
| sequencer    | desde la *posición* Insert                                  | sobrescribir en *posición*                             |
| vídeos          | en *el momento* de la inicialización de la *posición*                     | Insertar Sobrescribir en *posición*                      |
| waveaudio    | desde la *posición* Insert                                  | sobrescribir en *posición*                             |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRecordFlags** y su significado.



| Value                 | Significado                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en el *rectángulo*        | Especifica una región rectangular de la entrada externa usada como origen para los píxeles comprimidos y guardados. Si no se especifica, el rectángulo tiene como valor predeterminado el rectángulo especificado para [Put](put.md) "vídeo". Cuando se establece de manera diferente del rectángulo de "vídeo", la imagen mostrada no es lo que se graba. |
| a la *hora*             | Indica que el dispositivo debe comenzar a ejecutar este comando, o bien, si el dispositivo está preparado, cuando comienza el comando de la cuenta. Para obtener más información, consulte el comando [CUE](cue.md) .                                                                                                                             |
| *secuencia* de flujo de audio | Especifica la secuencia de audio utilizada para la grabación. Si no se especifica esta marca y el formato de archivo no define un valor predeterminado, se registra en el flujo que es físicamente primero.                                                                                                                             |
| desde la *posición*       | Especifica una posición inicial para la grabación. Si no se especifica la marca "desde", el dispositivo inicia la grabación en la posición actual.                                                                                                                                                                       |
| contener                  | Inmoviliza la imagen cuando ha terminado la grabación en lugar de mostrar vídeo en directo. Cuando se detiene la grabación, se realiza un comando de [supervisión](monitor.md) automática del "archivo". Para volver a vídeo en directo, emita el comando **supervisar** "entrada".                                                                              |
| initialize            | Inicialice la cinta (multimedia), que implica el registro del código de tiempo (si es posible) para vídeo y audio en blanco. Este comando puede tardar varias horas si se debe inicializar toda la cinta.                                                                                                                            |
| insert                | Especifica que los nuevos datos se agregan al archivo en la posición actual.                                                                                                                                                                                                                                            |
| sobrescribir             | Especifica que los nuevos datos reemplazarán los datos del archivo.                                                                                                                                                                                                                                                           |
| para *colocar*         | Especifica una posición final para la grabación. Si no se especifica la marca "para", el dispositivo registra hasta que recibe un comando [detener](stop.md) o [pausar](pause.md) .                                                                                                                                        |
| *secuencia* de flujo de vídeo | Especifica la secuencia de vídeo que se usa para la grabación. Si no se especifica y el formato de archivo no define un valor predeterminado, se registra en el flujo que es físicamente primero.                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La grabación se detiene cuando se emite un comando [detener](stop.md) o [pausar](pause.md) . En el caso del controlador MCIWAVE, todos los datos registrados después de abrir un archivo se descartan si el archivo se cierra sin guardarlo.

Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) . Las pistas que se van a grabar se especifican mediante los comandos [settimecode](settimecode.md) "registro", "ensamblar registro", [setvideo](setvideo.md) "registro" y [SetAudio](setaudio.md) "registro".

## <a name="examples"></a>Ejemplos

El comando siguiente inicia la grabación en la posición actual.

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

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> <dt>

[indicación](cue.md)
</dt> <dt>

[control](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[pondrán](put.md)
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

 


---
title: reproducir comando
description: El comando PLAY comienza a reproducir un dispositivo. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- comando PLAY Windows multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676700"
---
# <a name="play-command"></a>reproducir comando

El comando PLAY comienza a reproducir un dispositivo. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*
</dt> <dd>

Marca para reproducir un dispositivo. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Play** y las marcas usadas por cada tipo.



| Value        | Significado                          | Significado                           |
|--------------|----------------------------------|-----------------------------------|
| cdaudio      | desde la *posición*                  | para *colocar*                     |
| digitalvideo | repetir desde la *posición* de pantalla completa | invertir en la ventana de *posición*       |
| sequencer    | desde la *posición*                  | para *colocar*                     |
| vídeos          | en *el tiempo* desde la *posición* inversa  | Buscar en *posición*                |
| videodisco    | exploración inversa rápida desde la *posición* | *entero* de velocidad lenta que se va a *colocar* |
| waveaudio    | desde la *posición*                  | para *colocar*                     |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszPlayFlags** y su significado.



| Value           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| a la *hora*       | Indica que el dispositivo debe comenzar a ejecutar este comando, o bien, si el dispositivo está preparado, cuando comienza el comando de la cuenta. Para obtener más información, consulte el comando [CUE](cue.md) .                                                                                                                                                                                                                                                                 |
| fast            | Indica que el dispositivo debe reproducirse más rápido que el normal. Para determinar la velocidad exacta en un reproductor de videodisco, use la marca "Speed" del comando [status](status.md) . Para especificar la velocidad de forma más precisa, use la marca "Speed" de este comando.                                                                                                                                                                                                   |
| desde la *posición* | Especifica una posición inicial para la reproducción. Si no se especifica la marca "from", la reproducción comienza en la posición actual. En el caso de los dispositivos **cdaudio** , si la posición "desde" es mayor que la posición final del disco o si la posición "desde" es mayor que la posición "hasta", el controlador devuelve un error. En el caso de los dispositivos de **videodisco** , las posiciones predeterminadas están en fotogramas para los discos CAV y en horas, minutos y segundos para los discos CLV. |
| completa      | Especifica que debe usarse una presentación en pantalla completa. Use esta marca solo cuando se reproduzcan archivos comprimidos. (Los archivos sin comprimir no se reproducirán en pantalla completa).                                                                                                                                                                                                                                                                                                  |
| pueden          | Especifica que la reproducción debe reiniciarse cuando se alcanza el final del contenido.                                                                                                                                                                                                                                                                                                                                                                       |
| reverse         | Especifica que la dirección de reproducción está hacia atrás. No se puede especificar una ubicación final con el marcador "REVERSE". En el caso de los videodisco, "SCAN" solo se aplica al formato CAV.                                                                                                                                                                                                                                                                                     |
| revisar            | Se reproduce lo más rápido posible sin deshabilitar el vídeo (aunque es posible que el audio esté deshabilitado). En el caso de los videodisco, "SCAN" solo se aplica al formato CAV.                                                                                                                                                                                                                                                                                                             |
| lento            | Se reproduce lentamente. Para determinar la velocidad exacta en un reproductor de videodisco, use la marca "Speed" del comando [status](status.md) . Para especificar la velocidad de forma más precisa, use la marca "Speed" de este comando. En el caso de los videodisco, "slow" solo se aplica al formato CAV.                                                                                                                                                                                            |
| *entero* de velocidad | Reproduce un CD a la velocidad especificada, en fotogramas por segundo. Esta marca solo se aplica a discos CAV.                                                                                                                                                                                                                                                                                                                                                 |
| para *colocar*   | Especifica una posición final para la reproducción. Si no se especifica la marca "to", la reproducción se detiene al final del contenido. En el caso de los dispositivos **cdaudio** , si la posición "para" es mayor que la posición final del disco, el controlador devuelve un error. En el caso de los dispositivos de **videodisco** , las posiciones predeterminadas están en fotogramas para los discos CAV y en horas, minutos y segundos para los discos CLV.                                                                  |
| periodo          | Especifica que la reproducción debe usar la ventana asociada a la instancia del dispositivo. Esta es la configuración predeterminada.                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Antes de emitir comandos que usan valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) . Este comando empieza a reproducirse en la velocidad actual, como se establece con el comando SET "Speed". La dirección es inversa si se especifica la marca "REVERSE", o si la marca "to" se especifica como un valor menor que la marca "from". Si no se especifica la marca "from", la reproducción comienza en la posición actual. Las marcas "to" y "REVERSE" no se pueden usar juntas.

## <a name="examples"></a>Ejemplos

El siguiente comando reproduce el dispositivo "" de "" de la posición 1000 a la posición 2000 y envía un mensaje de notificación cuando se completa la reproducción.

``` syntax
play mysound from 1000 to 2000 notify
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

[set](set.md)
</dt> </dl>

 


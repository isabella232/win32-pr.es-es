---
title: comando de búsqueda
description: El comando Seek se desplaza a la posición y se detiene especificados. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, VCR, Videodisc y de onda-audio reconocen este comando.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- comando Buscar multimedia de Windows
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421946"
---
# <a name="seek-command"></a>comando de búsqueda

El comando Seek se desplaza a la posición y se detiene especificados. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, VCR, Videodisc y de onda-audio reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*
</dt> <dd>

Marca que se va a mover a una posición especificada. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Seek** y las marcas usadas por cada tipo.



| Value        | Significado                          | Significado                      |
|--------------|----------------------------------|------------------------------|
| cdaudio      | hasta el final de la *posición*             | para iniciar                     |
| digitalvideo | hasta el final de la *posición*             | para iniciar                     |
| sequencer    | hasta el final de la *posición*             | para iniciar                     |
| vídeos          | en marca de marca de *tiempo* *\_ número* inverso | para finalizar la *posición* de inicio |
| videodisco    | invertir hasta el final                   | para *colocar* en Start        |
| waveaudio    | hasta el final de la *posición*             | para iniciar                     |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszSeekFlags** y su significado.



| Value            | Significado                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| a la *hora*        | Indica que el dispositivo debe comenzar a ejecutar este comando, o bien, si el dispositivo está preparado, cuando comienza el comando de la cuenta. Para obtener más información, consulte el comando [CUE](cue.md) .                             |
| marcar *\_ núm* . | Busca la marca relativa indicada por *Mark \_ NUM*, que debe ser un valor entero positivo. Las marcas son señales escritas en la cinta VCR con el comando [Mark](mark.md) y se usan para la búsqueda de alta velocidad. |
| reverse          | Indica que la dirección de búsqueda en los videodiscos VCR y CAV está hacia atrás. Esta marca no es válida si se especifica la marca "to". En el caso de los VCR, esta marca se debe usar con el marcador "Mark".                             |
| hasta el final           | Busca el final del contenido.                                                                                                                                                                                 |
| para *colocar*    | Especifica la posición para detener la búsqueda. En el caso de los dispositivos **cdaudio** , MCI devuelve un error fuera de intervalo si la posición especificada es mayor que la longitud del disco.                                            |
| para iniciar         | Busca el inicio del contenido.                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el comando [set](set.md) .

Los dispositivos de vídeo digital admiten dos modos de búsqueda, que se pueden cambiar mediante el comando [set](set.md) . El modo "Buscar exactamente en" hace que el comando de búsqueda se mueva al marco especificado. El modo "Buscar exactamente desactivado" hace que el comando Buscar se mueva al fotograma clave más cercano antes del marco especificado.

Si se está reproduciendo un dispositivo de audio de CD cuando se emite el comando de búsqueda, se detiene la reproducción. Cuando el comando de búsqueda se emite con un dispositivo de videodisco, el dispositivo realiza búsquedas mediante el uso del avance rápido o el desactivado rápido con vídeo y audio.

Cuando el comando de búsqueda se emite con un dispositivo de audio de forma de onda, el comportamiento depende del tamaño de la muestra. Si el tamaño de la muestra es de 16 bits o superior, la búsqueda se desplaza al principio del ejemplo más cercano cuando una posición especificada no coincide con el inicio de un ejemplo.

## <a name="examples"></a>Ejemplos

El siguiente comando busca el inicio del archivo multimedia asociado con el dispositivo "de".

``` syntax
seek mysound to start
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

[Rasa](mark.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 


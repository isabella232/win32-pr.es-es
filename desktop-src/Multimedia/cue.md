---
title: Comando cue
description: El comando cue se prepara para reproducir o grabar. Los dispositivos de audio y vídeo digital, VCR y forma de onda reconocen este comando.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- Comando cue Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6398d4773b6c92332e8a95996e4d81941a073fe
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369831"
---
# <a name="cue-command"></a>Comando cue

El comando cue se prepara para reproducir o grabar. Los dispositivos de audio y vídeo digital, VCR y forma de onda reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*
</dt> <dd>

Marca que prepara un dispositivo para reproducir o grabar. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen **el comando cue** y las marcas usadas por cada tipo.




| Value | Pila | Pila | 
|-------|-----|-----|
| digitalvideo | <ul><li>input</li><li>noshow</li></ul> | <ul><li>output</li><li>para <em>colocar</em></li></ul> | 
| Vcr | <ul><li>desde <em>la posición</em></li><li>input</li><li>output</li></ul> | <ul><li>Predesplazamiento</li><li>reverse</li><li>para <em>colocar</em></li></ul> | 
| waveaudio | input | output | 




 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro *lpszInOutTo* y sus significados.



| Value           | Significado                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| desde *la posición* | Indica por dónde empezar.                                                                                                                                                                                                                                                                                      |
| input           | Se prepara para la grabación. En el caso de los dispositivos de vídeo digital, esta marca se puede omitir si el origen de presentación actual ya es la entrada externa.                                                                                                                                                                  |
| noshow          | Se prepara para reproducir un fotograma sin mostrarlo. Cuando se especifica esta marca, la pantalla sigue mostrando la imagen en el búfer de fotogramas aunque su marco correspondiente no sea la posición actual. Un comando cue posterior sin esta marca y sin la marca "to" muestra el marco actual. |
| output          | Se prepara para la reproducción. Si no se especifica "input" ni "output", el valor predeterminado es "output".                                                                                                                                                                                                           |
| Predesplazamiento         | Mueve la distancia de inscripción previa desde *el punto de entrada.* El punto de entrada es la posición actual o la posición especificada por la marca "from".                                                                                                                                                                            |
| reverse         | Indica que la dirección del juego es inversa (hacia atrás).                                                                                                                                                                                                                                                             |
| para *colocar*   | Mueve el área de trabajo a la posición especificada. En el caso de los dispositivos VCR, esta marca indica dónde se debe detener.                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Aunque no es necesario, la emisión del comando cue antes de reproducir o grabar en algunos dispositivos podría reducir el retraso antes de que el dispositivo inicie la acción.

Este comando produce un error si la reproducción o la grabación están en curso o si el dispositivo está en pausa.

Al realizar indicaciones para la reproducción (mediante la indicación "output"), la emisión del comando [play](play.md) con la marca "from", "to" o "reverse" cancela el comando cue.

Al hacer indicaciones para grabar (mediante la indicación "input"), la emisión del comando [record](record.md) con la marca "from", "to" o "initialize" cancela el comando cue.

## <a name="examples"></a>Ejemplos

El comando siguiente prepara el dispositivo "my sound" para la grabación.

``` syntax
cue mysound input
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

[Jugar](play.md)
</dt> <dt>

[record](record.md)
</dt> </dl>

 


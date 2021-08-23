---
title: Comando info
description: El comando info recupera una descripción de hardware de un dispositivo. Todos los dispositivos MCI reconocen este comando.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- Comando info Windows Multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f15675923f37a80ce694a400f18113f5178a54a3f75664008644919c6d9fc128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690475"
---
# <a name="info-command"></a>Comando info

El comando info recupera una descripción de hardware de un dispositivo. Todos los dispositivos MCI reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*
</dt> <dd>

Marca que identifica el tipo de información necesaria. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **info** y las marcas usadas por cada tipo.



| Valor        | Significado                                                             | Significado                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| cdaudio      | info identityinfo upc                                               | product                                             |
| digitalvideo | audio algorithmaudio qualityfileproductstfund algorithmstill quality | usageversionvideo algorithmvideo qualitywindow text |
| overlay      | fileproduct                                                         | texto de la ventana                                         |
| sequencer    | copyrightfile                                                       | nameproduct                                         |
| Vcr          | product                                                             | version                                             |
| videodisk    | product                                                             |                                                     |
| waveaudio    | fileinput                                                           | outputproduct                                       |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszInfoType** y sus significados.



| Valor           | Significado                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo de audio | Devuelve el nombre del algoritmo de compresión de audio actual.                                                                                                                                       |
| calidad del audio   | Devuelve el nombre del descriptor de calidad de audio actual. Esto podría devolver "desconocido" si la aplicación ha establecido parámetros en valores específicos que no se corresponden con calidades definidas.       |
| copyright       | Recupera el aviso de copyright del archivo MIDI del meta evento de copyright.                                                                                                                            |
| archivo            | Recupera el nombre del archivo utilizado por el dispositivo compuesto. Si el dispositivo se abre sin un archivo y no se ha usado el comando [load,](load.md) se devuelve una cadena null.                  |
| identidad de información   | Genera un identificador único para el CD de audio cargado actualmente en el reproductor que se está consultando.                                                                                                        |
| upc de información        | Genera el código de producto universal (UPC) que se codifica en un CD de audio. El UPC es una cadena de dígitos. Es posible que no esté disponible para todos los CD.                                                    |
| input           | Recupera la descripción del dispositivo de entrada actual. Devuelve "none" si no se establece un dispositivo de entrada.                                                                                               |
| name            | Recupera el nombre de secuencia del meta evento de nombre de secuencia o pista.                                                                                                                               |
| output          | Recupera la descripción del dispositivo de salida actual. Devuelve "none" si no se establece un dispositivo de salida.                                                                                             |
| product         | Recupera una descripción del dispositivo. Esta información a menudo incluye el nombre y el modelo del producto. La longitud de la cadena será de 31 caracteres o menos.                                               |
| algoritmo still | Devuelve el nombre del algoritmo de compresión de imágenes fijas actual.                                                                                                                                 |
| calidad de todavía   | Devuelve el nombre del descriptor de calidad de imagen fija actual. Esto podría devolver "desconocido" si la aplicación ha establecido parámetros en valores específicos que no se corresponden con calidades definidas. |
| usage           | Devuelve una cadena que describe las restricciones de uso que podría imponer el propietario de los datos visuales o de audio del área de trabajo.                                                                    |
| version         | Devuelve el nivel de versión del controlador de dispositivo y el hardware.                                                                                                                                       |
| algoritmo de vídeo | Devuelve el nombre del algoritmo de compresión de vídeo actual.                                                                                                                                       |
| calidad de vídeo   | Devuelve el nombre del descriptor de calidad de vídeo actual. Esto podría devolver "desconocido" si la aplicación ha establecido parámetros en valores específicos que no se corresponden con calidades definidas.       |
| texto de la ventana     | Recupera el título de la ventana que usa el dispositivo.                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="examples"></a>Ejemplos

El comando siguiente recupera una descripción del hardware asociado al dispositivo "my sound".

``` syntax
info mysound product
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[carga](load.md)
</dt> </dl>

 


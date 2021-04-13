---
title: info (comando)
description: El comando info recupera una descripción de hardware de un dispositivo. Todos los dispositivos MCI reconocen este comando.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- comando info Windows multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422554"
---
# <a name="info-command"></a>info (comando)

El comando info recupera una descripción de hardware de un dispositivo. Todos los dispositivos MCI reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca que identifica el tipo de información necesaria. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **info** y las marcas usadas por cada tipo.



| Value        | Significado                                                             | Significado                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| cdaudio      | info identityinfo UPC                                               | product                                             |
| digitalvideo | audio algorithmaudio qualityfileproductstill algorithmstill Quality | usageversionvideo algorithmvideo qualitywindow Text |
| overlay      | fileproduct                                                         | texto de la ventana                                         |
| sequencer    | copyrightfile                                                       | nameproduct                                         |
| vídeos          | product                                                             | version                                             |
| videodisco    | product                                                             |                                                     |
| waveaudio    | fileinput                                                           | outputproduct                                       |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszInfoType** y su significado.



| Value           | Significado                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo de audio | Devuelve el nombre del algoritmo de compresión de audio actual.                                                                                                                                       |
| calidad de audio   | Devuelve el nombre del descriptor de calidad de audio actual. Esto podría devolver "Unknown" si la aplicación tiene parámetros establecidos en valores específicos que no se corresponden con calidades definidas.       |
| copyright       | Recupera el aviso de copyright del archivo MIDI del evento meta de copyright.                                                                                                                            |
| archivo            | Recupera el nombre del archivo utilizado por el dispositivo compuesto. Si el dispositivo se abre sin un archivo y no se ha usado el comando [Load](load.md) , se devuelve una cadena nula.                  |
| identidad de información   | Genera un identificador único para el CD de audio cargado actualmente en el reproductor que se consulta.                                                                                                        |
| UPC de información        | Genera el código universal de producto (UPC) que está codificado en un CD de audio. UPC es una cadena de dígitos. Es posible que no esté disponible para todos los CD.                                                    |
| input           | Recupera la descripción del dispositivo de entrada actual. Devuelve "none" si no se ha establecido un dispositivo de entrada.                                                                                               |
| name            | Recupera el nombre de secuencia del evento meta de nombre de secuencia/pista.                                                                                                                               |
| output          | Recupera la descripción del dispositivo de salida actual. Devuelve "none" si no se ha establecido un dispositivo de salida.                                                                                             |
| product         | Recupera una descripción del dispositivo. Esta información suele incluir el nombre del producto y el modelo. La longitud de la cadena será de 31 caracteres como máximo.                                               |
| algoritmo de todavía | Devuelve el nombre del algoritmo de compresión de imagen fija actual.                                                                                                                                 |
| calidad todavía   | Devuelve el nombre del descriptor de calidad de imagen todavía actual. Esto podría devolver "Unknown" si la aplicación tiene parámetros establecidos en valores específicos que no se corresponden con calidades definidas. |
| usage           | Devuelve una cadena que describe las restricciones de uso que puede imponer el propietario de los datos visuales o de audio en el área de trabajo.                                                                    |
| version         | Devuelve el nivel de versión del controlador de dispositivo y el hardware.                                                                                                                                       |
| algoritmo de vídeo | Devuelve el nombre del algoritmo de compresión de vídeo actual.                                                                                                                                       |
| calidad del vídeo   | Devuelve el nombre del descriptor de calidad de vídeo actual. Esto podría devolver "Unknown" si la aplicación tiene parámetros establecidos en valores específicos que no se corresponden con calidades definidas.       |
| texto de la ventana     | Recupera el título de la ventana que usa el dispositivo.                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="examples"></a>Ejemplos

El siguiente comando recupera una descripción del hardware asociado al dispositivo "".

``` syntax
info mysound product
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

[carga](load.md)
</dt> </dl>

 


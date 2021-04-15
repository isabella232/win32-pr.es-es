---
title: detener (comando)
description: El comando Stop detiene la reproducción o grabación. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- detener comando de Windows multimedia
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422304"
---
# <a name="stop-command"></a>detener (comando)

El comando Stop detiene la reproducción o grabación. Los dispositivos de audio de CD, digital-video, MIDI Sequencer, Videodisc, VCR y de onda-audio reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*
</dt> <dd>

En el caso de los dispositivos de vídeo digital, puede ser la marca siguiente.



| Value | Significado                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| contener  | Impide que se liberen los recursos necesarios para volver a dibujar una imagen fija en la pantalla. El búfer de marco sigue estando disponible para su uso en la actualización de la pantalla cuando, por ejemplo, la ventana se mueve. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

En el caso de los dispositivos de audio de CD, el comando Stop detiene la reproducción y restablece la posición de pista actual en cero.

## <a name="examples"></a>Ejemplos

El comando siguiente detiene la reproducción o grabación en el dispositivo "".

``` syntax
stop mysound
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
</dt> </dl>

 


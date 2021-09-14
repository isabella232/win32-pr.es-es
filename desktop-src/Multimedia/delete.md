---
title: comando delete
description: El comando delete elimina un segmento de datos de un archivo. Los dispositivos de audio y vídeo digital reconocen este comando.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- comando delete Windows Multimedia
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fad34059ec75b0077fdc409cee8cd35a5495699
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074261"
---
# <a name="delete-command"></a>comando delete

El comando delete elimina un segmento de datos de un archivo. Los dispositivos de audio y vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*
</dt> <dd>

Marca que identifica un segmento de datos que se eliminará. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el **comando delete** y las marcas usadas por cada tipo.




| Value | Significado | Significado | 
|-------|---------|---------|
| digitalvideo | <ul><li>en <em>rectángulo</em></li><li>secuencia <em>de</em> audio</li><li>desde <em>la posición</em></li></ul> | <ul><li>para <em>colocar</em></li><li>secuencia de <em>vídeo</em></li></ul> | 
| waveaudio | desde <em>la posición</em> | para <em>colocar</em> | 




 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el *parámetro lpszPosition* y sus significados.



| Value                 | Significado                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *rectángulo*        | Especifica la parte de cada fotograma eliminada. Si se omite, el valor predeterminado es todo el marco. Cuando se especifica este elemento, no se eliminan los fotogramas. En su lugar, el área dentro del rectángulo se vuelve negra.                                          |
| secuencia *de* audio | Especifica la secuencia de audio en el área de trabajo afectada por el comando . Si usa esta marca y también desea eliminar vídeo, también debe usar la marca "secuencia de vídeo". (Si no se especifica ninguna marca, se eliminan todas las secuencias de audio y vídeo). |
| desde *la posición*       | Especifica la posición en la que comienza la eliminación. Si se omite esta marca, la eliminación comienza en la posición actual.                                                                                                                       |
| para *colocar*         | Especifica la posición en la que finaliza la eliminación. Si se omite esta marca, la eliminación continúa hasta el final del contenido o del área de trabajo.                                                                                                       |
| secuencia de *vídeo* | Especifica la secuencia de vídeo en el área de trabajo afectada por el comando . Si usa esta marca y también desea eliminar audio, también debe usar la marca "secuencia de audio". (Si no se especifica ninguna marca, se eliminan todas las secuencias de audio y vídeo).     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Antes de emitir cualquier comando que use valores de posición, debe establecer el formato de hora deseado mediante el [comando set.](set.md)

## <a name="examples"></a>Ejemplos

El siguiente comando elimina los datos de audio de forma de onda de 1 milisegundo a 900 milisegundos (suponiendo que el formato de hora esté establecido en milisegundos).

``` syntax
delete mysound from 1 to 900
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 


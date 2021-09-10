---
title: comando save
description: El comando save guarda un archivo MCI. Los dispositivos de superposición de vídeo y audio de forma de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo admiten.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- guardar comando Windows Multimedia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370141"
---
# <a name="save-command"></a>comando save

El comando save guarda un archivo MCI. Los dispositivos de superposición de vídeo y audio de forma de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo admiten.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*
</dt> <dd>

Marca que especifica el nombre del archivo que se va a guardar y, opcionalmente, marcas adicionales que modifican la operación de guardado. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **save** y las marcas usadas por cada tipo.



| Value        | Significado              | Significado               |
|--------------|----------------------|-----------------------|
| digitalvideo | abort at *rectangle* | *filename* keepreserve |
| overlay      | en *rectángulo*       | *filename*            |
| sequencer    | *filename*           |                       |
| waveaudio    | *filename*           |                       |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszFilename** y sus significados.



| Value          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| anular          | Detiene una **operación de** guardado en curso. Si se usa, debe ser el único elemento presente.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| en *rectángulo* | Especifica un rectángulo relativo al origen del búfer de marco. El *rectángulo* se especifica como *X1 Y1 X2 Y2*. Las coordenadas *X1 Y1 especifican* la esquina superior izquierda y las coordenadas *X2 Y2* especifican el ancho y el alto. En el caso de los dispositivos de vídeo digital, el [comando capture](capture.md) se usa para capturar el contenido del búfer de fotogramas.<br/>                                                                                                                                               |
| *filename*     | Especifica el nombre de archivo que se asignará al archivo de datos. Si no se especifica una ruta de acceso, el archivo se colocará en el disco y en el directorio especificado anteriormente en el comando de reserva explícito [o implícito.](reserve.md) Si **no** se ha emitido la reserva, la unidad y el directorio predeterminados son los asociados a la tarea de la aplicación. Si se especifica una ruta de acceso, el dispositivo podría requerir que esté en la unidad de disco especificada por la reserva explícita o **implícita**. Esta marca es obligatoria. |
| keepreserve    | Especifica que no se desasigna el espacio en disco sin usar que se deja desde el comando **de** reserva original.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La *variable de* nombre de archivo es necesaria si el dispositivo se abrió con el identificador de dispositivo "nuevo".

## <a name="examples"></a>Ejemplos

El siguiente comando guarda todo el búfer de vídeo en un archivo denominado VCAPFILE. TGA.

``` syntax
save vboard c:\vcap\vcapfile.tga
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

[capturar](capture.md)
</dt> <dt>

[reserva](reserve.md)
</dt> </dl>

 


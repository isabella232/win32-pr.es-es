---
title: guardar (comando)
description: El comando Guardar guarda un archivo MCI. Los dispositivos de audio y la superposición de vídeo y de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo admiten.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- comando guardar de Windows multimedia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676569"
---
# <a name="save-command"></a>guardar (comando)

El comando Guardar guarda un archivo MCI. Los dispositivos de audio y la superposición de vídeo y de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo admiten.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca que especifica el nombre del archivo que se va a guardar y, opcionalmente, marcas adicionales que modifican la operación de guardar. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Save** y las marcas usadas por cada tipo.



| Value        | Significado              | Significado               |
|--------------|----------------------|-----------------------|
| digitalvideo | anular en el *rectángulo* | *nombre de archivo* keepreserve |
| overlay      | en el *rectángulo*       | *filename*            |
| sequencer    | *filename*           |                       |
| waveaudio    | *filename*           |                       |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszFilename** y su significado.



| Value          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| anular          | Detiene una operación de **Guardar** en curso. Si se utiliza, debe ser el único elemento presente.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| en el *rectángulo* | Especifica un rectángulo con respecto al origen de búfer de fotogramas. El *rectángulo* se especifica como *x1 Y1 x2 Y2*. Las coordenadas *x1 Y1* especifican la esquina superior izquierda y las coordenadas *x2 Y2* especifican el ancho y el alto. En el caso de los dispositivos de vídeo digital, el comando [Capture](capture.md) se usa para capturar el contenido del búfer de fotogramas.<br/>                                                                                                                                               |
| *filename*     | Especifica el nombre de archivo que se va a asignar al archivo de datos. Si no se especifica una ruta de acceso, el archivo se colocará en el disco y en el directorio especificado anteriormente en el comando de [reserva](reserve.md) explícito o implícito. Si no se ha emitido **Reserve** , la unidad y el directorio predeterminados son los asociados a la tarea de la aplicación. Si se especifica una ruta de acceso, el dispositivo podría requerir que esté en la unidad de disco especificada por la **reserva** explícita o implícita. Esta marca es obligatoria. |
| keepreserve    | Especifica que no se cancela la asignación del espacio en disco no utilizado que queda del comando de **reserva** original.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La variable *filename* es necesaria si el dispositivo se abrió con el identificador de dispositivo "nuevo".

## <a name="examples"></a>Ejemplos

El siguiente comando guarda el búfer de vídeo completo en un archivo denominado VCAPFILE. TGA.

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

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> <dt>

[grabar](capture.md)
</dt> <dt>

[reserva](reserve.md)
</dt> </dl>

 


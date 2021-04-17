---
title: comando de calidad
description: El comando calidad define un nivel de calidad personalizado para la compresión de datos audio, vídeo o imagen fija. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- comando de calidad multimedia de Windows
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666065"
---
# <a name="quality-command"></a>comando de calidad

El comando calidad define un nivel de calidad personalizado para la compresión de datos audio, vídeo o imagen fija. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*
</dt> <dd>

Una o varias de las marcas siguientes. (Una de las tres marcas "audio", "todavía" y "vídeo" debe estar presente.



| Value                 | Significado                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *algoritmo* de algoritmo | Asocia el nivel de calidad con el *algoritmo* especificado. Este *algoritmo* debe ser compatible con el dispositivo y ser compatible con la marca "audio", "todavía" o "vídeo" que se usa. Si se omite, se usa el algoritmo actual. |
| *nombre* de audio          | Indica que este comando especifica un nivel de calidad de "audio" identificado con *el nombre*.                                                                                                                                                   |
| diálogo                | Solicita que el dispositivo muestre un cuadro de diálogo. Este cuadro de diálogo tiene campos específicos del algoritmo que el dispositivo usa internamente para crear la estructura que describe un nivel de calidad específico.                                    |
| identificador *de controlador*       | Especifica un *identificador* para una estructura que contiene datos específicos del algoritmo que describen un nivel de calidad específico. Las estructuras de los datos a los que hace referencia este identificador son específicas del dispositivo.                                         |
| *nombre* todavía          | Indica que el comando especifica un nivel de calidad "todavía" identificado con *el nombre.*                                                                                                                                                     |
| *nombre* de vídeo          | Indica que el comando especifica un nivel de calidad "vídeo" identificado con *el nombre*.                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify", "Test" o una combinación de estos. Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando define un nombre de cadena para el nivel de calidad, que se puede usar en un comando [setvideo](setvideo.md) "Quality", setvideo "Quality" o [SetAudio](setaudio.md) "Quality" para establecerlo como el nivel de calidad de vídeo, todavía o compresión de audio actual.

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

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 


---
title: comando quality
description: El comando de calidad define un nivel de calidad personalizado para la compresión de datos de audio, vídeo o imágenes fijas. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- comando quality Windows Multimedia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476778"
---
# <a name="quality-command"></a>comando quality

El comando de calidad define un nivel de calidad personalizado para la compresión de datos de audio, vídeo o imágenes fijas. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

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

Una o varias de las marcas siguientes. (Una de las tres marcas "audio", "still" y "video" debe estar presente).



| Value                 | Significado                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo de *algoritmo* | Asocia el nivel de calidad al algoritmo *especificado.* Este *algoritmo* debe ser compatible con el dispositivo y ser compatible con la marca "audio", "still" o "video" que se usa. Si se omite, se usa el algoritmo actual. |
| nombre de *audio*          | Indica que este comando especifica un nivel de calidad "audio" identificado con *el nombre*.                                                                                                                                                   |
| diálogo                | Solicita que el dispositivo muestre un cuadro de diálogo. Este cuadro de diálogo tiene campos específicos del algoritmo que el dispositivo usa internamente para crear la estructura que describe un nivel de calidad específico.                                    |
| identificador *de identificador*       | Especifica un identificador *para* una estructura que contiene datos específicos del algoritmo que describen un nivel de calidad específico. Las estructuras de los datos a los que hace referencia este identificador son específicas del dispositivo.                                         |
| still *name*          | Indica que el comando especifica un nivel de calidad "todavía" identificado con *el nombre.*                                                                                                                                                     |
| nombre del *vídeo*          | Indica que el comando especifica un nivel de calidad de "vídeo" identificado con *el nombre*.                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando define un nombre de cadena para el nivel de calidad, que luego se puede usar en un comando [setvideo](setvideo.md) "quality", setvideo "still quality" o [setaudio](setaudio.md) "quality" para establecerlo como el nivel actual de calidad de compresión de audio, vídeo o vídeo.

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

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 


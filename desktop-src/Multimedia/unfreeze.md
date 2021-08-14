---
title: comando unfreeze
description: El comando unfreeze vuelve a deshabilitar la adquisición de vídeo en el búfer de fotogramas después de que el comando freeze lo haya deshabilitado. Los dispositivos de vídeo digital, VCR y superposición de vídeo reconocen este comando.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- descongelar el comando Windows Multimedia
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fe45b1346872483a4012c5f5d161dcd61020c64349fee254ae4bf337b4be8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370815"
---
# <a name="unfreeze-command"></a>comando unfreeze

El comando unfreeze vuelve a deshabilitar la adquisición de vídeo en el búfer de fotogramas después de que el comando freeze lo [haya](freeze.md) deshabilitado. Los dispositivos de vídeo digital, VCR y superposición de vídeo reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*
</dt> <dd>

Marca para volver a buscar la adquisición de vídeo en el búfer de fotogramas. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **unfreeze** y las marcas usadas por cada tipo.



| Valor        | Significado        |
|--------------|----------------|
| digitalvideo | en *rectángulo* |
| overlay      | en *rectángulo* |
| Vcr          | salida de entrada   |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszUnfreeze** y sus significados.



| Valor          | Significado                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *rectángulo* | Especifica la región en la que se volverá a habilitar la adquisición de vídeo. El rectángulo es relativo al origen del búfer de vídeo y se especifica como *X1 Y1 X2 Y2*. Las coordenadas *X1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *X2 Y2* especifican el ancho y el alto. |
| input          | Descongele la imagen de entrada.                                                                                                                                                                                                                                                                  |
| output         | Descongele la imagen de salida. Si no se da "entrada" ni "salida", se supone "salida".                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="examples"></a>Ejemplos

El comando siguiente descongela una región del búfer de vídeo.

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[Congelar](freeze.md)
</dt> </dl>

 


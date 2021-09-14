---
title: comando unfreeze
description: El comando unfreeze vuelve a liberar la adquisición de vídeo en el búfer de fotogramas después de que el comando freeze lo haya deshabilitado. Los dispositivos de vídeo digital, VCR y superposición de vídeo reconocen este comando.
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
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260588"
---
# <a name="unfreeze-command"></a>comando unfreeze

El comando unfreeze vuelve a liberar la adquisición de vídeo en el búfer de fotogramas después de que el comando [freeze](freeze.md) lo haya deshabilitado. Los dispositivos de vídeo digital, VCR y superposición de vídeo reconocen este comando.

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

Marca para volver a enmarcar la adquisición de vídeo en el búfer de fotogramas. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **unfreeze** y las marcas usadas por cada tipo.



| Value        | Significado        |
|--------------|----------------|
| digitalvideo | en *rectángulo* |
| overlay      | en *rectángulo* |
| Vcr          | salida de entrada   |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszUnfreeze** y sus significados.



| Value          | Significado                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *rectángulo* | Especifica la región en la que se volverá a habilitar la adquisición de vídeo. El rectángulo es relativo al origen del búfer de vídeo y se especifica como *X1 Y1 X2 Y2.* Las coordenadas *X1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *X2 Y2* especifican el ancho y el alto. |
| input          | Descongele la imagen de entrada.                                                                                                                                                                                                                                                                  |
| output         | Descongele la imagen de salida. Si no se da "entrada" ni "salida", se supone que "salida".                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="examples"></a>Ejemplos

El comando siguiente descongela una región del búfer de vídeo.

``` syntax
unfreeze vboard at 10 20 90 165
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

[Congelar](freeze.md)
</dt> </dl>

 


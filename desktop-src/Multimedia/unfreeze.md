---
title: unfreeze (comando)
description: El comando unfreeze permite volver a habilitar la adquisición de vídeo en el búfer de fotogramas después de que el comando Freeze lo haya deshabilitado. Los dispositivos digitales-vídeo, VCR y superposición de vídeo reconocen este comando.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- unfreeze (comando) multimedia de Windows
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803818"
---
# <a name="unfreeze-command"></a>unfreeze (comando)

El comando unfreeze permite volver a habilitar la adquisición de vídeo en el búfer de fotogramas después de que el comando [Freeze](freeze.md) lo haya deshabilitado. Los dispositivos digitales-vídeo, VCR y superposición de vídeo reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca para volver a habilitar la adquisición de vídeo en el búfer de fotogramas. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **unfreeze** y las marcas usadas por cada tipo.



| Value        | Significado        |
|--------------|----------------|
| digitalvideo | en el *rectángulo* |
| overlay      | en el *rectángulo* |
| vídeos          | salida de entrada   |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszUnfreeze** y su significado.



| Value          | Significado                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en el *rectángulo* | Especifica la región en la que se volverá a habilitar la adquisición de vídeo. El rectángulo es relativo al origen del búfer de vídeo y se especifica como *x1 Y1 x2 Y2*. Las coordenadas *x1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *x2 Y2* especifican el ancho y el alto. |
| input          | Libere la imagen de entrada.                                                                                                                                                                                                                                                                  |
| output         | Libere la imagen de salida. Si no se especifica "Input" ni "Output", se asume "Output".                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="examples"></a>Ejemplos

El siguiente comando libera una región del búfer de vídeo.

``` syntax
unfreeze vboard at 10 20 90 165
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

[Inmovilice](freeze.md)
</dt> </dl>

 


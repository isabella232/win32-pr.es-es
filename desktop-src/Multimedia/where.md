---
title: where (comando)
description: El comando where recupera el rectángulo que especifica el área de origen o destino. Este rectángulo se especificó mediante el comando put. Los dispositivos de vídeo digital y de superposición de vídeo reconocen este comando.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- where command Windows Multimedia
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071691"
---
# <a name="where-command"></a>where (comando)

El comando where recupera el rectángulo que especifica el área de origen o destino. Este rectángulo se especificó mediante el [comando put.](put.md) Los dispositivos de vídeo digital y de superposición de vídeo reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*
</dt> <dd>

Marca que identifica el rectángulo cuyas dimensiones se recuperan. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **where** y las marcas usadas por cada tipo.



| Value        | Significado                                                       | Significado                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| digitalvideo | destinationdestination [**max**](max.md)frameframe maxsource | source maxvideovideo maxwindowwindow max |
| overlay      | destinationframe                                              | sourcevideo                              |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRequestRect** y sus significados.



| Value                          | Significado                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                    | Recupera el desplazamiento de destino y la extensión. En el caso de los dispositivos de superposición de vídeo, el rectángulo de destino define el área del área cliente de la ventana de presentación que muestra los datos de imagen del búfer de fotogramas.                                                                                             |
| destination [ **max**](max.md) | Recupera el tamaño actual del rectángulo del cliente.                                                                                                                                                                                                                                                  |
| frame                          | Recupera el desplazamiento y la extensión del rectángulo del búfer de marco. El rectángulo del búfer de marco define el área del búfer de fotogramas que recibe los datos de vídeo entrantes. Las imágenes del rectángulo "vídeo" se escalan a esta región.                                                                     |
| máximo de [ **fotogramas**](max.md)       | Devuelve el tamaño máximo del búfer de fotogramas.                                                                                                                                                                                                                                                        |
| source                         | Recupera el desplazamiento y la extensión de origen. En el caso de los dispositivos de superposición de vídeo, el rectángulo de origen define la región del búfer de fotogramas que se muestra en la ventana de destino. El dispositivo usa este rectángulo para recortar la imagen antes de que se ajuste al rectángulo de destino en la pantalla. |
| source [ **max**](max.md)      | Recupera el tamaño máximo del búfer de fotogramas.                                                                                                                                                                                                                                                      |
| video                          | Recupera el desplazamiento y la extensión del rectángulo de vídeo. El rectángulo de vídeo define la región de los datos de vídeo entrantes que se transfieren al búfer de fotogramas.                                                                                                                                   |
| máximo [ **de vídeo**](max.md)       | Devuelve el tamaño máximo de la entrada.                                                                                                                                                                                                                                                               |
| periodo                         | Recupera el tamaño y la posición actuales del marco de la ventana de presentación.                                                                                                                                                                                                                                 |
| máximo de [ **ventana**](max.md)      | Recupera el tamaño de toda la pantalla.                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un rectángulo en el *parámetro lpszReturnString* de la [**función mciSendString.**](/previous-versions//dd757161(v=vs.85)) El rectángulo describe el área especificada en el *parámetro lpszRequestRect* de este comando. El rectángulo se especifica como *X1 Y1 X2 Y2*. Las coordenadas *X1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *X2 Y2* especifican el ancho y el alto.

## <a name="examples"></a>Ejemplos

El comando siguiente devuelve el rectángulo de presentación del dispositivo "movie".

``` syntax
where movie destination
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

[Poner](put.md)
</dt> </dl>

 


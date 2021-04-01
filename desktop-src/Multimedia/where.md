---
title: Where (comando)
description: El comando Where recupera el rectángulo que especifica el área de origen o de destino. Este rectángulo se especificó mediante el comando Put. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- comando Where Windows multimedia
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996950"
---
# <a name="where-command"></a>Where (comando)

El comando Where recupera el rectángulo que especifica el área de origen o de destino. Este rectángulo se especificó mediante el comando [Put](put.md) . Los dispositivos de vídeo digital y de superposición reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Marca que identifica el rectángulo cuyas dimensiones se recuperan. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Where** y las marcas usadas por cada tipo.



| Value        | Significado                                                       | Significado                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| digitalvideo | destinationdestination [**Max**](max.md)frameFrame maxsource | Source maxvideovideo maxwindowwindow Max |
| overlay      | destinationframe                                              | sourcevideo                              |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRequestRect** y su significado.



| Value                          | Significado                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                    | Recupera el desplazamiento y la extensión de destino. En el caso de los dispositivos de superposición de vídeo, el rectángulo de destino define el área del área de cliente de la ventana de presentación que muestra los datos de imagen del búfer de fotogramas.                                                                                             |
| destino [ **máximo**](max.md) | Recupera el tamaño actual del rectángulo del cliente.                                                                                                                                                                                                                                                  |
| frame                          | Recupera el desplazamiento y la extensión del rectángulo de búfer del marco. El rectángulo de búfer de marco define el área del búfer de fotogramas que recibe los datos de vídeo entrantes. Las imágenes del rectángulo "vídeo" se escalan en esta región.                                                                     |
| fotograma [ **máximo**](max.md)       | Devuelve el tamaño máximo del búfer de marco.                                                                                                                                                                                                                                                        |
| source                         | Recupera el desplazamiento de origen y la extensión. En el caso de los dispositivos de superposición de vídeo, el rectángulo de origen define la región del búfer de fotogramas que se muestra en la ventana de destino. El dispositivo usa este rectángulo para recortar la imagen antes de que se ajuste para ajustarse al rectángulo de destino de la pantalla. |
| [ **número máximo** de orígenes](max.md)      | Recupera el tamaño máximo del búfer de fotogramas.                                                                                                                                                                                                                                                      |
| video                          | Recupera el desplazamiento y la extensión del rectángulo de vídeo. El rectángulo de vídeo define la región de los datos de vídeo entrantes que se transfieren al búfer de fotogramas.                                                                                                                                   |
| vídeo [ **máx** .](max.md)       | Devuelve el tamaño máximo de la entrada.                                                                                                                                                                                                                                                               |
| periodo                         | Recupera el tamaño y la posición actuales del marco de la ventana de presentación.                                                                                                                                                                                                                                 |
| ventana [ **máx** .](max.md)      | Recupera el tamaño de la pantalla completa.                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "Test". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un rectángulo en el parámetro *lpszReturnString* de la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . El rectángulo describe el área especificada en el parámetro *lpszRequestRect* de este comando. El rectángulo se especifica como *x1 Y1 x2 Y2*. Las coordenadas *x1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *x2 Y2* especifican el ancho y el alto.

## <a name="examples"></a>Ejemplos

El siguiente comando devuelve el rectángulo de visualización del dispositivo "Movie".

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

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> <dt>

[pondrán](put.md)
</dt> </dl>

 


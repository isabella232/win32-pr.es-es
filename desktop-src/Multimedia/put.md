---
title: Put (comando)
description: El comando Put define el área de la imagen de origen y la ventana de destino que se usan para la presentación. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- poner comando en Windows multimedia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150961"
---
# <a name="put-command"></a>Put (comando)

El comando Put define el área de la imagen de origen y la ventana de destino que se usan para la presentación. Los dispositivos de vídeo digital y de superposición reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*
</dt> <dd>

Marca para definir el área. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando Put y las marcas usadas por cada tipo.



| Value        | Significado                                                                                      | Significado                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| digitalvideo | destino de destino *en el* marco del marco del rectángulo en el origen del *rectángulo* de origen en el *rectángulo* | vídeo en vídeo en la ventana de la ventana de *rectángulo* en la ventana de *rectángulo* cliente Window Client en *rectángulo* |
| overlay      | destino de destino en el marco del marco del *rectángulo* en el *rectángulo*                             | vídeo de origen en vídeo en rectángulo *en el* rectángulo                                           |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRegions** y su significado.



| Value                        | Significado                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                  | Selecciona el área de cliente completa de la ventana de destino para mostrar los datos.                                                                                                                                                                                                                                                                         |
| destino en el *rectángulo*   | Selecciona una parte del área de cliente de la ventana de destino que se usa para mostrar la imagen. Cuando se especifica un área de la ventana de presentación y el dispositivo admite la expansión, la imagen de origen se ajusta al desplazamiento y la extensión de destino.                                                                                                     |
| frame                        | Selecciona todo el búfer de fotogramas para recibir las imágenes de vídeo entrantes.                                                                                                                                                                                                                                                                                 |
| marco en *rectángulo*         | Selecciona una parte del búfer de fotogramas para recibir las imágenes de vídeo entrantes.                                                                                                                                                                                                                                                                           |
| source                       | Selecciona toda la imagen que se va a mostrar en la ventana de destino.                                                                                                                                                                                                                                                                                       |
| origen en el *rectángulo*        | Selecciona una parte de la imagen que se va a mostrar en la ventana de destino. Cuando se especifica un área de la imagen de origen y el dispositivo admite la expansión, la imagen de origen se ajusta al desplazamiento y la extensión de destino.                                                                                                                           |
| video                        | Selecciona la imagen de vídeo entrante completa que se va a capturar en el búfer de fotogramas.                                                                                                                                                                                                                                                                               |
| vídeo en *rectángulo*         | Selecciona una parte de la imagen de vídeo entrante para capturar en el búfer de fotogramas.                                                                                                                                                                                                                                                                         |
| periodo                       | Restaura el tamaño inicial de la ventana en la pantalla. Este comando también muestra la ventana.                                                                                                                                                                                                                                                               |
| ventana en *rectángulo*        | Cambia el tamaño y la ubicación de la ventana de presentación. El rectángulo especificado es relativo a la ventana primaria de la ventana de presentación (normalmente el escritorio) si se ha usado la marca "secundario de estilo" para el comando [abrir](open.md) . Para cambiar la ubicación de la ventana sin cambiar su alto o ancho, especifique cero para el alto y el ancho. |
| cliente de Windows                | Restaura el área cliente de la ventana.                                                                                                                                                                                                                                                                                                               |
| cliente de ventana en *rectángulo* | Cambia el tamaño y la ubicación del área de cliente de la ventana. El rectángulo especificado es relativo a la ventana primaria de la ventana de cliente. Para cambiar la ubicación de la ventana sin cambiar su alto o ancho, especifique cero para el alto y el ancho.                                                                                      |



 

Cuando una marca incluye un rectángulo, las coordenadas del rectángulo se relacionan con el origen de la ventana o el origen de la imagen, según corresponda, y se especifican como **x1 Y1 x2 Y2**. Las coordenadas **X1Y1** especifican la esquina superior izquierda y las coordenadas **X2Y2** especifican el ancho y el alto del rectángulo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "Test". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El comando Put define uno o varios de los siguientes rectángulos cuando se trabaja con dispositivos de superposición de vídeo:

-   El rectángulo de vídeo define la región de la imagen de vídeo entrante que se va a capturar.
-   El rectángulo del marco define la región del búfer de fotogramas que recibe la imagen de vídeo entrante.
-   El rectángulo de origen define qué región del búfer de fotogramas se copia en el rectángulo de destino.
-   El rectángulo de destino define la región del área de cliente de la ventana de presentación que recibe la imagen de vídeo.

El rectángulo de vídeo está relacionado con el rectángulo del marco de la misma manera que el rectángulo de origen está relacionado con el rectángulo de destino. La expansión puede producirse desde el rectángulo del vídeo hasta el rectángulo del marco y desde el rectángulo de origen hasta el rectángulo de destino. No todos los dispositivos admiten la ampliación y la expansión debe estar habilitada (mediante el comando [set](set.md) ).

El comando siguiente define tres regiones para el vídeo, el marco y el origen.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

Las regiones de este ejemplo se definen de la siguiente manera:

-   Una región de 200 x 200 píxeles de los datos de vídeo entrantes, a partir de un origen de 120 píxeles desde la esquina superior izquierda, se capturará en el búfer de fotogramas.
-   Los datos de vídeo se colocarán en una región de 200 x 200 píxeles en la esquina superior izquierda del búfer de fotogramas.
-   Las transferencias se realizan desde la región 200-by 200-pixel en la esquina superior izquierda del búfer de fotogramas hasta la ventana de destino.

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

[open](open.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 


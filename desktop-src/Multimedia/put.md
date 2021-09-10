---
title: Comando put
description: El comando put define el área de la imagen de origen y la ventana de destino que se usa para la presentación. Los dispositivos de superposición de vídeo digital y vídeo reconocen este comando.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- Comando put Windows Multimedia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369839"
---
# <a name="put-command"></a>Comando put

El comando put define el área de la imagen de origen y la ventana de destino que se usa para la presentación. Los dispositivos de superposición de vídeo digital y vídeo reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

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

Marca para definir el área. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando put y las marcas usadas por cada tipo.



| Value        | Significado                                                                                      | Significado                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| digitalvideo | destino en el marco *del marco* del rectángulo en *el origen* del rectángulo en el *rectángulo* | vídeo de vídeo en *la ventana de* rectángulo en el *cliente* de ventana de cliente de la ventana de rectángulo en el *rectángulo* |
| overlay      | destino en el *marco de* marco del rectángulo en el *rectángulo*                             | source source at *rectangle* video video at *rectangle*                                           |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszRegions** y sus significados.



| Value                        | Significado                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                  | Selecciona el área de cliente completa de la ventana de destino para mostrar los datos.                                                                                                                                                                                                                                                                         |
| destination at *rectangle*   | Selecciona una parte del área de cliente de la ventana de destino utilizada para mostrar la imagen. Cuando se especifica un área de la ventana de presentación y el dispositivo admite el ajuste, la imagen de origen se extiende hasta el desplazamiento y la extensión de destino.                                                                                                     |
| frame                        | Selecciona todo el búfer de fotogramas para recibir las imágenes de vídeo entrantes.                                                                                                                                                                                                                                                                                 |
| marco en *rectángulo*         | Selecciona una parte del búfer de fotogramas para recibir las imágenes de vídeo entrantes.                                                                                                                                                                                                                                                                           |
| source                       | Selecciona la imagen completa para mostrarla en la ventana de destino.                                                                                                                                                                                                                                                                                       |
| source at *rectangle*        | Selecciona una parte de la imagen que se mostrará en la ventana de destino. Cuando se especifica un área de la imagen de origen y el dispositivo admite el ajuste, la imagen de origen se extiende hasta el desplazamiento y la extensión de destino.                                                                                                                           |
| video                        | Selecciona toda la imagen de vídeo entrante que se capturará en el búfer de fotogramas.                                                                                                                                                                                                                                                                               |
| vídeo en *rectángulo*         | Selecciona una parte de la imagen de vídeo entrante que se capturará en el búfer de fotogramas.                                                                                                                                                                                                                                                                         |
| periodo                       | Restaura el tamaño inicial de la ventana en la pantalla. Este comando también muestra la ventana.                                                                                                                                                                                                                                                               |
| ventana en *rectángulo*        | Cambia el tamaño y la ubicación de la ventana de presentación. El rectángulo especificado es relativo a la ventana primaria de la ventana para mostrar (normalmente el escritorio) si se ha usado la marca "elemento secundario de estilo" para el [comando](open.md) open. Para cambiar la ubicación de la ventana sin cambiar su alto o ancho, especifique cero para el alto y el ancho. |
| cliente de ventana                | Restaura el área de cliente de la ventana.                                                                                                                                                                                                                                                                                                               |
| cliente de ventana en *rectángulo* | Cambia el tamaño y la ubicación del área de cliente de la ventana. El rectángulo especificado es relativo a la ventana primaria de la ventana de cliente. Para cambiar la ubicación de la ventana sin cambiar su alto o ancho, especifique cero para el alto y el ancho.                                                                                      |



 

Cuando una marca incluye un rectángulo, las coordenadas del rectángulo son relativas al origen de la ventana o al origen de la imagen, según corresponda, y se especifican como **X1 Y1 X2 Y2**. Las coordenadas **X1Y1 especifican** la esquina superior izquierda y las coordenadas **X2Y2** especifican el ancho y alto del rectángulo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El comando put define uno o varios de los rectángulos siguientes al trabajar con dispositivos de superposición de vídeo:

-   El rectángulo de vídeo define la región de la imagen de vídeo entrante que se capturará.
-   El rectángulo de marco define la región del búfer de fotogramas que recibe la imagen de vídeo entrante.
-   El rectángulo de origen define qué región del búfer de marco se copia en el rectángulo de destino.
-   El rectángulo de destino define la región del área de cliente de la ventana de presentación que recibe la imagen de vídeo.

El rectángulo de vídeo está relacionado con el rectángulo de marco de la misma manera que el rectángulo de origen está relacionado con el rectángulo de destino. El stretch puede producirse desde el rectángulo de vídeo hasta el rectángulo de marco y desde el rectángulo de origen hasta el rectángulo de destino. No todos los dispositivos admiten el ajuste, y el ajuste debe estar habilitado (mediante el [comando set).](set.md)

El comando siguiente define tres regiones para el vídeo, el fotograma y el origen.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

Las regiones de este ejemplo se definen de la siguiente manera:

-   Se capturará una región de 200 por 200 píxeles de los datos de vídeo entrantes, empezando en un origen de 120 píxeles desde la esquina superior izquierda, en el búfer de fotogramas.
-   Los datos de vídeo se colocarán en una región de 200 por 200 píxeles en la esquina superior izquierda del búfer de fotogramas.
-   Las transferencias se realizan desde la región de 200 por 200 píxeles en la esquina superior izquierda del búfer de fotogramas a la ventana de destino.

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

[open](open.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 


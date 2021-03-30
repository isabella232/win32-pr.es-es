---
title: pegar (comando)
description: El comando pegar copia el contenido del portapapeles en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- pegar comandos de Windows multimedia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079058"
---
# <a name="paste-command"></a>pegar (comando)

El comando pegar copia el contenido del portapapeles en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Una o varias de las marcas siguientes.



| Value                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en el *rectángulo*        | Especifica la ubicación dentro del marco donde se pegan los datos. La esquina superior izquierda del *rectángulo* corresponde a la esquina superior izquierda de los datos agregados. Si el rectángulo tiene un tamaño distinto de cero en X o Y, el contenido del portapapeles se escala en esas dimensiones cuando se pegan en el marco. Si se omite, el *rectángulo* tiene como valor predeterminado el marco completo. Si esta marca se especifica en el modo "Insertar" (valor predeterminado), cualquier región fuera del rectángulo se dibuja como un color sólido.                       |
| *secuencia* de flujo de audio | Especifica la secuencia de audio en el área de trabajo afectada por el comando. Si solo existe una secuencia de audio en el portapapeles, los datos de audio se pegan en la *secuencia* designada. Si existe más de una secuencia de audio en el portapapeles, la *secuencia* indica el número de inicio de las secuencias de la secuencia. Si usa esta marca y también quiere pegar vídeo, también debe usar la marca "secuencia de vídeo". (Si no se especifica ninguna marca, se pegan todas las secuencias de audio y vídeo y se conservan los números de secuencia originales). |
| insert                | Especifica que los datos se insertan en el área de trabajo. Los datos después del punto de inserción se mueven hacia delante en el área de trabajo para dejar espacio. Este es el valor predeterminado.                                                                                                                                                                                                                                                                                                                                                    |
| sobrescribir             | Especifica que los datos se copian en el área de trabajo escribiendo los datos existentes después del punto de inserción. Las marcas "Insertar" y "Sobrescribir" afectan a si los marcos se destruyen o se mueven durante la operación de pegar, no al modo en que los datos se pegan dentro de cada marco.                                                                                                                                                                                                                                              |
| para *colocar*         | Especifica la posición en el área de trabajo en la que se pegan los datos. Si se omite, el valor predeterminado es la posición actual.                                                                                                                                                                                                                                                                                                                                                                                                    |
| *secuencia* de flujo de vídeo | Especifica la secuencia de vídeo en el área de trabajo afectada por el comando. Si solo existe una secuencia de vídeo en el portapapeles, los datos de vídeo se pegan en la *secuencia* designada. Si existe más de una secuencia de vídeo en el portapapeles, la *secuencia* indica el número de inicio de las secuencias de la secuencia. Si usa esta marca y también desea pegar audio, también debe usar la marca de "secuencia de audio". (Si no se especifica ninguna marca, se pegan todas las secuencias de audio y vídeo y se conservan los números de secuencia originales). |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify", "Test" o una combinación de estos. Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

No hay señales en los datos copiados desde el portapapeles. El cambio solo se convierte en permanente cuando se guardan los datos explícitamente; sin embargo, la reproducción actúa como si se agregaran los datos.

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
</dt> </dl>

 


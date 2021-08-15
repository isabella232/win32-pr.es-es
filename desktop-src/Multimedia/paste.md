---
title: comando paste
description: El comando paste copia el contenido del Portapapeles en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- comando paste Windows Multimedia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b93f042193c50a810ac23285224ddd234a23b2070f8db2d56d216fee037c37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373220"
---
# <a name="paste-command"></a>comando paste

El comando paste copia el contenido del Portapapeles en el área de trabajo. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

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



| Valor                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *rectángulo*        | Especifica la ubicación dentro del marco donde se pegan los datos. La esquina superior izquierda del *rectángulo* corresponde a la esquina superior izquierda de los datos agregados. Si el rectángulo tiene un tamaño distinto de cero en X o Y, el contenido del Portapapeles se escala en esas dimensiones cuando se pegan en el marco. Si se omite, el *rectángulo tiene* como valor predeterminado todo el marco. Si esta marca se especifica en modo de "inserción" (valor predeterminado), cualquier región fuera del rectángulo se pinta con un color sólido.                       |
| secuencia *de* audio | Especifica la secuencia de audio en el área de trabajo afectada por el comando . Si solo existe una secuencia de audio en el Portapapeles, los datos de audio se pegan en la secuencia *designada.* Si hay más de una secuencia de audio en el Portapapeles, la *secuencia* indica el número inicial de las secuencias de secuencia. Si usa esta marca y también quiere pegar vídeo, también debe usar la marca "secuencia de vídeo". (Si no se especifica ninguna marca, todas las secuencias de audio y vídeo se pegan y conservan sus números de secuencia originales). |
| insert                | Especifica que los datos se insertan en el área de trabajo. Los datos después del punto de inserción se mueven hacia delante en el área de trabajo para hacer espacio. Este es el valor predeterminado.                                                                                                                                                                                                                                                                                                                                                    |
| sobrescribir             | Especifica que los datos se copian en el área de trabajo escribiendo sobre los datos existentes después del punto de inserción. Las marcas "insert" y "overwrite" afectan a si los fotogramas se destruyen o se mueven durante la operación de pegado, no a cómo se pegan los datos dentro de cada fotograma.                                                                                                                                                                                                                                              |
| para *colocar*         | Especifica la posición en el área de trabajo en la que se pegan los datos. Si se omite, el valor predeterminado es la posición actual.                                                                                                                                                                                                                                                                                                                                                                                                    |
| secuencia de *vídeo* | Especifica la secuencia de vídeo en el área de trabajo afectada por el comando . Si solo existe una secuencia de vídeo en el Portapapeles, los datos de vídeo se pegan en la secuencia *designada.* Si hay más de una secuencia de vídeo en el Portapapeles, la *secuencia* indica el número inicial de las secuencias de secuencia. Si usa esta marca y también quiere pegar audio, también debe usar la marca "secuencia de audio". (Si no se especifica ninguna marca, todas las secuencias de audio y vídeo se pegan y conservan sus números de secuencia originales). |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

No hay señales presentes en los datos copiados del Portapapeles. El cambio se convierte en permanente solo cuando los datos se guardan explícitamente; sin embargo, la reproducción actúa como si se hubieran agregado los datos.

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
</dt> </dl>

 


---
title: copiar comando
description: El comando copiar copia los datos en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- copiar comando de Windows multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801525"
---
# <a name="copy-command"></a>copiar comando

El comando copiar copia los datos en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
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

Una de las marcas siguientes que identifican el elemento que se va a copiar.



| Value                 | Significado                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en el *rectángulo*        | Especifica la parte de cada fotograma que se copiará. Si se omite, el valor predeterminado es todo el marco.                                                                                                                             |
| *secuencia* de flujo de audio | Especifica la secuencia de audio en el área de trabajo afectada por el comando. Si usa esta marca y también quiere copiar vídeo, también debe usar la marca "secuencia de vídeo". (Si no se especifica ninguna marca, se copian todas las secuencias de audio y vídeo). |
| desde la *posición*       | Especifica el inicio del intervalo copiado. Si se omite, el valor predeterminado es la posición actual.                                                                                                                                         |
| para *colocar*         | Especifica el final del intervalo copiado. Los datos de audio y vídeo copiados son exclusivos de esta posición. Si se omite, el valor predeterminado es el final del área de trabajo.                                                                       |
| *secuencia* de flujo de vídeo | Especifica la secuencia de vídeo en el área de trabajo afectada por el comando. Si usa esta marca y también quiere copiar audio, también debe usar la marca de "secuencia de audio". (Si no se especifica ninguna marca, se copian todas las secuencias de audio y vídeo). |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify", "Test" o una combinación de estos. Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

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

 


---
title: comando copy
description: El comando copy copia los datos en el Portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- comando copy Windows Multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369872"
---
# <a name="copy-command"></a>comando copy

El comando copy copia los datos en el Portapapeles. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

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

Una de las siguientes marcas identifica el elemento que se copiará.



| Value                 | Significado                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *rectángulo*        | Especifica la parte de cada fotograma que se va a copiar. Si se omite, la configuración predeterminada es todo el marco.                                                                                                                             |
| secuencia *de* audio | Especifica la secuencia de audio en el área de trabajo afectada por el comando . Si usa esta marca y también desea copiar vídeo, también debe usar la marca "secuencia de vídeo". (Si no se especifica ninguna marca, se copian todas las secuencias de audio y vídeo). |
| desde *la posición*       | Especifica el inicio del intervalo copiado. Si se omite, la configuración predeterminada es la posición actual.                                                                                                                                         |
| para *colocar*         | Especifica el final del intervalo copiado. Los datos de audio y vídeo copiados son exclusivos de esta posición. Si se omite, la configuración predeterminada es el final del área de trabajo.                                                                       |
| secuencia de *vídeo* | Especifica la secuencia de vídeo en el área de trabajo afectada por el comando . Si usa esta marca y también desea copiar audio, también debe usar la marca "secuencia de audio". (Si no se especifica ninguna marca, se copian todas las secuencias de audio y vídeo). |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

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
</dt> </dl>

 

